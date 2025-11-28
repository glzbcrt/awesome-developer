# Linux

## Distros

### Omarchy

- [Omarchy](https://omarchy.org/)

## Features

### FUSE

- [FUSE: Filesystem in Userspace Explained](https://www.abhik.xyz/concepts/linux/fuse-filesystem)
- [FUSE: get process context](https://github.com/fusepy/fusepy/blob/master/examples/context.py#L17)
- [fusepy](https://github.com/fusepy/fusepy)
- [FUSE (filesystem in user space)](https://georgesims21.github.io/posts/fuse/)
- [To FUSE or Not to FUSE: Performance of User-Space File Systems](https://www.usenix.org/system/files/conference/fast17/fast17-vangoor.pdf)

```python
#!/usr/bin/env python3
import os
import errno
from fuse import FUSE, Operations, fuse_get_context


class HelloFS(Operations):
    def __init__(self):
        self.files = {
            '/': dict(st_mode=0o755 | 0o040000),  # Directory
            '/hello.txt': dict(
                st_mode=0o644 | 0o100000,  # Regular file
                st_size=17,
                content=b'Hello World!\nglzbcrt\n'
            )
        }

    def getattr(self, path, fh=None):
        """Get file attributes."""
        if path not in self.files:
            raise OSError(errno.ENOENT)

        attrs = self.files[path].copy()
        attrs['st_nlink'] = 1
        attrs['st_uid'] = os.getuid()
        attrs['st_gid'] = os.getgid()
        return attrs

    def readdir(self, path, fh):
        """List directory contents."""
        if path == '/':
            return ['.', '..', 'hello.txt']
        raise OSError(errno.ENOENT)

    def open(self, path, flags):
        """Open a file."""
        if path not in self.files:
            raise OSError(errno.ENOENT)
        return 0

    def read(self, path, length, offset, fh):
        """Read from a file."""
        if path not in self.files:
            raise OSError(errno.ENOENT)

        # Use fuse_get_context() to get info about who is calling.
        uid, gid, pid = fuse_get_context()

        # Now use that info to return different content based on the user id for the same file.
        if uid == 1000:
            content = self.files[path].get('content', b'')
            return content[offset:offset + length]
        else:
            return b'Riders on the storm!'

if __name__ == '__main__':
    import sys

    #
    # In order to allow different users from the one who mounted to read files add the **allow_other** parameter.
    # Ref#1: https://stackoverflow.com/questions/38676937/allow-other-with-fusepy
    # Ref#2: https://superuser.com/questions/1758100/how-to-mount-fuse-e-g-unionfs-so-that-all-users-will-have-access-to-it
    #
    FUSE(HelloFS(), sys.argv[1], foreground=True, **{'allow_other': True})

```
