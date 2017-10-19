# beamerthemepolimi
Beamer port of the official PoliMi presentation theme.

Requires the package [PGF/TikZ](https://www.ctan.org/pkg/pgf) to be installed in your LaTeX distribution.

Demo
----
![](https://github.com/elauksap/beamerthemepolimi/blob/master/demo-bgphoto.jpg)
![](https://github.com/elauksap/beamerthemepolimi/blob/master/demo-bgwhite.jpg)
![](https://github.com/elauksap/beamerthemepolimi/blob/master/demo-sectionpage.jpg)
![](https://github.com/elauksap/beamerthemepolimi/blob/master/demo-slide.jpg)

Instructions
============
Download the latest release by following [this](https://github.com/elauksap/beamerthemepolimi/releases) link.

Then copy the files named beamer*themepolimi.sty and the folder beamerthemepolimi_img/ into the same folder as your LaTeX source file.

Finally write in your preamble:
```latex
\documentclass{beamer}

\usetheme{polimi}
```

Custom options and logo
-----------------------
The standard background photo on the title page (instead of a default white background) can be selected through the optional parameter _bgphoto_:
```latex
\usetheme[bgphoto]{polimi}
```

In order to hide the default logo shown on the title page, the option _nologo_ is available:
```latex
\usetheme[nologo]{polimi}
```

Then you can customize your own title page by typing, for instance, the following commands on the first slide, right after the _\maketitle_ command (see _demo.tex_):
```latex
\begin{tikzpicture}[overlay, remember picture]
    \node at (current page.north) [anchor=north, inner sep=2cm]
    {
        \includegraphics[width=0.3\paperwidth]{logo_centrato_BN_negativo.png}
    };
\end{tikzpicture}
```

Set a custom font
-----------------
You can set a custom font, which has to be installed on your system, by adding the following commands to the preamble and by using XeLaTeX as compiler:
```latex
\usepackage{ifxetex}
\ifxetex
    \usepackage{fontspec}
    \setsansfont[Scale=0.95]{Arial}
\fi
```

Change the default block style
------------------------------
The default block style can be modified by adding either
```latex
\setbeamertemplate{blocks}[rounded][shadow=false]
```
or
```latex
\setbeamertemplate{blocks}[default][shadow=false]
```
to your preamble after loading the theme.
