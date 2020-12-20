# Fdutils-aux

`Fdutils-aux` is an auxiliary script package for [fdutils](https://fdutils.linux.lu/) and [ddrescue](http://www.gnu.org/software/ddrescue/ddrescue.html) to operate any floppy disks of Japanese retro computers more easily.

## Setup

`Fdutils-aux` requires [fdutils](https://fdutils.linux.lu/) and [ddrescue](http://www.gnu.org/software/ddrescue/ddrescue.html) on your platform. On Debian and Ubuntu based distributions, install these required packages with the following command.

```
sudo apt install -y fdutils gddrescue
```

## Ddrescue-*

`Ddrescue-*` are auxiliary scripts to be able to use [ddrescue](http://www.gnu.org/software/ddrescue/ddrescue.html) for Japanese retro computers easily. `ddrescue-*` set the following standard floppy parameters before executing [ddrescue](http://www.gnu.org/software/ddrescue/ddrescue.html).

|Script        |Maker  |Computer|Media|density|head|cyl|sect|ssize|
|--------------|-------|--------|-----|-------|----|---|----|-----|
|ddrescue-x1   |Sharp  |X1      |2D   |dd     |2   |40 |16  |256  |
|ddrescue-x1-hd|       |X1      |2HD  |hd     |2   |77 |16  |256  |
|ddrescue-mz   |       |MZ-2500 |2DD  |dd     |2   |80 |16  |256  |
|ddrescue-68   |       |X68000  |2HD  |hd     |2   |77 |8   |1024 |
|ddrescue-fm   |Fujitsu|FM-77   |2D   |dd     |2   |40 |16  |256  |
|ddrescue-fm-dd|       |FM77AV  |2DD  |dd     |2   |80 |16  |256  |
|ddrescue-88   |NEC    |8801    |2D   |dd     |2   |40 |16  |256  |
|ddrescue-88-hd|       |8801    |2HD  |hd     |2   |80 |26  |256  |
|ddrescue-98   |       |9801    |2HD  |hd     |2   |77 |8   |1024 |
|ddrescue-smc  |Sony   |SMC-777 |1DD  |dd     |1   |70 |16  |256  |

You can pass any parameters same as [ddrescue](http://www.gnu.org/software/ddrescue/ddrescue.html) to `ddrescue-*`, but `ddrescue-*` set the above parameters to `/dev/fd0` statically.
[Fdutils](https://fdutils.linux.lu/) supports only legacy (FDC-based) floppy drives, and so `ddrescue-*` can't use other floppy drives such as USB floppy drives.

## References

- [Floppy Drive Tech Info](http://www.retrotechnology.com/herbs_stuff/drive.html)- [ddrescue - GNU Project - Free Software Foundation (FSF)](http://www.gnu.org/software/ddrescue/ddrescue.html)
- [fdutils - Linux floppy tuning utilities](https://fdutils.linux.lu/)
- [fdutils - tools.ietf.org](https://tools.ietf.org/doc/fdutils/Fdutils.html)
