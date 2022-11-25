# Hey! I'm Filing Here

This code creates a valid ext2 filesystem that can be 
mounted to a directory

## Building

Use "make" to create an ext2-create.c file executable.
Use "./ext2-create" to run the executable and create a cs111-base.img file.

## Running

Run the command "fsck.ext2 cs111 -base.img" to verify that the file system is valid. 
Once there are no errors, create a directory with "mkdir mnt" to mount the file to. 
Use "sudo mount -o loop cs111 -base.img mnt" to mount the file system to the directory

Example output (ls -ain):
'''
total 7
      2 drwxr-xr-x 3    0    0 1024 Nov 24 21:04 .
1092131 drwxr-xr-x 5 1000 1000 4096 Nov 24 21:04 ..
     13 lrw-r--r-- 1 1000 1000   11 Nov 24 21:04 hello -> hello-world
     12 -rw-r--r-- 1 1000 1000   12 Nov 24 21:04 hello-world
     11 drwxr-xr-x 2    0    0 1024 Nov 24 21:04 lost+found

'''
## Cleaning up

Use command "sudo umount mnt" to unmount directory.
Remove directory with "rmdir mnt".
Run "make clean" to remove .img file and binary files
