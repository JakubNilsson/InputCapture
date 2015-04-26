InputCapture
============

A simple tool for capturing user input like mouse positions, movement, key strokes and plotting them.

## Usage

For capturing mouse movement and keystrokes, just run the java code and press CTRL + Q to save. If you have trouble starting it, import it as a Eclipse project and it should work.

Remember: **[ESC]** _saves_ the log files and **overwrites** the old log files. So you might save your files after a run.

For starting a new capture, I suggest to run the Code, and press [ESC] if you're ready (that will override the existing data). Then capture your run (or let the users do the tests) and at the end, hit [ESC] again to save the data until to that point. You can then end the running java code without writing that back into files by pressing CTRL+C.

Standard output variables includes (first three in *summary.txt*):

* time duration
* distance covered by mouse movement
* number of clicks
* a csv with all the position data of the mouse (*positions.csv*)
* A PNG file (*plot.png*) file which in older versions would be generated by the python script.


The java code makes use of the [jnativehook](http://code.google.com/p/jnativehook/) library (you guys are awesome!) which can capture mouse gestures and keyboard movement system-wide. 

You can visualize the data by applying the `plot.py` program (you'll need python installed) _DEPRECATED_ - now it is handled by the application itself. It will plot all the given positions from **positions.csv** to a transparent PNG-image, which you can then combine with a screenshot of the scene the capture took place.

It will automatically determine your screen resolution. 


## Disclaimer
This code is mostly untested and was written for quick use in the course Human-Computer-Interaction. It should work on Ubuntu 12.04, no clue if it works on Windows. Use at your own risk.
(*) Fixed by rfg1: It should work on Windows, just be careful in multi-monitor settings as mouse positioning most likely will fail when on secondary display. This project was expanded as a part of my Java class and it wasn't thoroughly tested.
