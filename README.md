# beamerthemepolimi
Beamer port of the official PoliMi presentation theme.

Demo
----
![](https://github.com/elauksap/beamerthemepolimi/blob/master/demo-bgphoto.jpg)
![](https://github.com/elauksap/beamerthemepolimi/blob/master/demo-bgwhite.jpg)
![](https://github.com/elauksap/beamerthemepolimi/blob/master/demo-slide.jpg)

Instructions
============
Download the latest release by following [this](https://github.com/elauksap/beamerthemepolimi/releases) link.

Then copy the files named beamer*themepolimi.sty and the folder beamerthemepolimi_img/ into the same folder as your LaTeX source file.

Finally write in your preamble:
```
\documentclass{beamer}

\usetheme{polimi}
```

A default background photo on the title page (instead of a white bg) can be selected through the optional parameter:
```
\usetheme[bgphoto]{polimi}
```
