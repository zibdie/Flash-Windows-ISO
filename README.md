# Instructions On Flashing a Windows ISO onto USB (via Rufus)

As a reminder, flashing a Windows ISO using Rufus is not so straightforward if its a Multi-Windows ISO as Rufus autodefaults to Windows Home. These are simple instructions on how to bypass that.

1. You will need a Windows ISO which Microsoft provides [here](https://www.microsoft.com/en-us/software-download/windows10). Remember to change your browser's user agent to a non-Microsoft one to get the ISO

2. Flash the ISO using Rufus as usual. Disable any security settings if needed

3. Once done, you will need to create a `ei.cfg` and a `PID.txt` file in the `sources/` folder (which you can find in the root of the bootable USB)

4. In the `ei.cfg`, add this
```
[EditionID]
Professional
[Channel]
_Default
[VL]
0
```
and in the `PID.txt`, add this
```
[PID]
Value=XXXXX-XXXXX-XXXXX-XXXXX-XXXXX
```

5. Take out the USB and flash it onto another device. You will see it autodefaults to Windows 11 Pro