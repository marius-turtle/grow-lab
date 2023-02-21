# grow-lab

## set up raspi image ...

... after not having used an old pi for a loooong time, the and just to have a fresh start taking the SD card of the old pi
and oops, two partitions and it looks like the sd card has not its full capacity e.g. 32 GB

Found this [resource][1] and the following steps helped:

- inserting your sd card
- opening the terminal and using `diskutil list` to take a look at its partitions, which should reveal that there is still actually the whole space left (lucky one)
- using `sudo diskutil eraseDisk FAT32 SDCARD MBRFormat /dev/disk2` to format it with FAT32 and name `SDCARD` 

[1]: https://thomas.vanhoutte.be/miniblog/reclaim-the-full-storage-capacity-of-an-sd-card-on-macos/ 'link formatting sd card on terminal'