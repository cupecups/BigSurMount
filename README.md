# BigSurMount
Mount BigSur as r/w Filesystem

# 1. Disable csrutill & authenticated-root
    - boot into recovery
    - type on terminal "csrutil disable"
    - and then type "csrutil authenticated-root disable"
    - reboot
    
# 2. create directory to your user home
    - open terminal type " mkdir ~/rootbs "
    - install ntfs-3g with brew
    - type "sudo mount -o nobrowse -t apfs /dev/disk*s* ~/rootbs"
    - type "sudo mv ~/rootbs/sbin/mount_ntfs ~/rootbs/sbin/mount_ntfs.original3"
    - type "sudo ln -s /usr/local/Celllar/ntfs-3g?*/sbin/mount_ntfs ~/rootbs/sin/mount_ntfs"
    - type "sudo bless --folder ~/rootbs/System/Library/CoreServices --bootefi --create-snaphot "
    - reboot
    
# 3. how to mount filesystem
    - open terminal
    - type "sudo mount -o nobrowse -t apfs /dev/disk*s* ~/rootbs"
    - now you can edit and change the file system

# cons
    - you can replace disk*s* with your mount point, for example type on terminal and type "mount" 
      you can see example /dev/disk1s5 <-- this mount point
    - dont disable authenticated-root
    - you can change name of rootbs folder if you want
    - ntfs-3g is optional, you can use tuxera to mount ntfs filesystem
