# Fdutils-aux

`Fdutils-aux` is an auxiliary script package for [fdutils](https://fdutils.linux.lu/) and [ddrescue](http://www.gnu.org/software/ddrescue/ddrescue.html) to operate any floppy disks of retro computers more easily. Some old floppy disk might have any damages, and so [Ddrescue](http://www.gnu.org/software/ddrescue/ddrescue.html) tries to rescue the good parts first in case of read errors and retries the bad parts.

## Setup

`Fdutils-aux` requires [fdutils](https://fdutils.linux.lu/) and [ddrescue](http://www.gnu.org/software/ddrescue/ddrescue.html) on your Linux platform. On Debian and Ubuntu based distributions, install these required packages with the following command.

```
sudo apt install -y fdutils gddrescue
```

## Ddrescue-*

`Ddrescue-*` are auxiliary scripts to be able to use [ddrescue](http://www.gnu.org/software/ddrescue/ddrescue.html) more easily. `ddrescue-*` set the following standard floppy parameters using `setfdprm` of [fdutils](https://fdutils.linux.lu/).

|Command         |Maker  |Computer|Structure|Media|density|head|cyl|sect|ssize|stretch|
|----------------|-------|--------|---------|-----|-------|----|---|----|-----|-------|
|ddrescue-x1     |Sharp  |X1      |5.25     |2D   |dd     |2   |40 |16  |256  |-      |
|ddrescue-x1-hd  |       |X1      |5.25     |2HD  |hd     |2   |77 |16  |256  |-      |
|ddrescue-mz     |       |MZ-2500 |3.5      |2DD  |dd     |2   |80 |16  |256  |-      |
|ddrescue-68     |       |X68000  |5.25     |2HD  |hd     |2   |77 |8   |1024 |-      |
|ddrescue-fm     |Fujitsu|FM-77   |3.5      |2D   |dd     |2   |40 |16  |256  |1      |
|ddrescue-fm-dd  |       |FM77AV  |3.5      |2DD  |dd     |2   |80 |16  |256  |-      |
|ddrescue-88     |NEC    |8801    |5.25     |2D   |dd     |2   |40 |16  |256  |-      |
|ddrescue-88-hd  |       |8801    |5.25     |2HD  |hd     |2   |80 |26  |256  |-      |
|ddrescue-98     |       |9801    |5.25     |2HD  |hd     |2   |77 |8   |1024 |-      |
|ddrescue-msx    |Any    |MSX     |3.5      |2DD  |dd     |2   |80 |9   |512  |-      |
|ddrescue-msx-1dd|       |        |3.5      |1DD  |dd     |1   |80 |9   |512  |-      |
|ddrescue-smc    |Sony   |SMC-777 |3.5      |1DD  |dd     |1   |70 |16  |256  |-      |
|ddrescue-pc     |Any    |PC/AT   |3.5      |2HD  |hd     |2   |80 |18  |512  |-      |
|ddrescue-pc5    |       |        |5.25     |2HD  |hd     |2   |80 |15  |512  |-      |

[Fdutils](https://fdutils.linux.lu/) supports only legacy (FDC-based) floppy drives, and so `ddrescue-*` can't use other floppy drives such as USB floppy drives.
You can pass any parameters same as [ddrescue](http://www.gnu.org/software/ddrescue/ddrescue.html) to `ddrescue-*`, but `ddrescue-*` set the above parameters to `/dev/fd0` statically.

## References

- [ddrescue - GNU Project - Free Software Foundation (FSF)](http://www.gnu.org/software/ddrescue/ddrescue.html)
- [fdutils - Linux floppy tuning utilities](https://fdutils.linux.lu/)
- [fdutils - tools.ietf.org](https://tools.ietf.org/doc/fdutils/Fdutils.html)
- [Floppy Drive Tech Info](http://www.retrotechnology.com/herbs_stuff/drive.html)
