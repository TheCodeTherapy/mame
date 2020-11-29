
# **MAME** #

[![Join the chat at https://gitter.im/mamedev/mame](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/mamedev/mame?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

What is MAME?
=============

MAME is a multi-purpose emulation framework.

This particular fork aims to be compiled on Debian / Ubuntu based Linux distributions. Tested on PopOS 20.04.

How to get this particular fork?
================================

```
git clone -b mame0226 --depth 1 https://github.com/TheCodeTherapy/mame.git mame0226
```

How to get the build dependencies?
==================================

```
sudo apt install git build-essential python libsdl2-dev libsdl2-ttf-dev libfontconfig-dev qt5-default
```

How to compile?
===============

```
cd mame0226
make TOOLS=1 REGENIE=1 -j5 ARCHOPTS=-U_FORTIFY_SOURCE
```

See the [Compiling MAME](http://docs.mamedev.org/initialsetup/compilingmame.html) page on our documentation site for more information, including prerequisites for Mac OS X and popular Linux distributions.

How to compile the documentation?
=================================

## Basic required packages
```
sudo apt install python3-sphinx python3-pip
```

## SVG handler dependencies
```
pip3 install sphinxcontrib-svg2pdfconverter
```

## PDF-via-LaTeX dependencies
```
sudo apt install latexmk texlive texlive-science texlive-formats-extra
```

## Compiling HTML docs
```
make html
```
_Note: the default output will be docs/build/html_

## Compiling latexpdf
```
make latexpdf
```

Where can I find out more?
=============

* [Official MAME Development Team Site](http://mamedev.org/) (includes binary downloads, wiki, forums, and more)
* [Official MESS Wiki](http://mess.redump.net/)
* [MAME Testers](http://mametesters.org/) (official bug tracker for MAME and MESS)


Contributing
=============

## Coding standard

MAME source code should be viewed and edited with your editor set to use four spaces per tab. Tabs are used for initial indentation of lines, with one tab used per indentation level. Spaces are used for other alignment within a line.

Some parts of the code follow [Allman style](https://en.wikipedia.org/wiki/Indent_style#Allman_style); some parts of the code follow [K&R style](https://en.wikipedia.org/wiki/Indent_style#K.26R_style) -- mostly depending on who wrote the original version. **Above all else, be consistent with what you modify, and keep whitespace changes to a minimum when modifying existing source.** For new code, the majority tends to prefer Allman style, so if you don't care much, use that.

All contributors need to either add a standard header for license info (on new files) or inform us of their wishes regarding which of the following licenses they would like their code to be made available under: the [BSD-3-Clause](http://opensource.org/licenses/BSD-3-Clause) license, the [LGPL-2.1](http://opensource.org/licenses/LGPL-2.1), or the [GPL-2.0](http://opensource.org/licenses/GPL-2.0).

License
=======
The MAME project as a whole is made available under the terms of the
[GNU General Public License, version 2](http://opensource.org/licenses/GPL-2.0)
or later (GPL-2.0+), since it contains code made available under multiple
GPL-compatible licenses.  A great majority of the source files (over 90%
including core files) are made available under the terms of the
[3-clause BSD License](http://opensource.org/licenses/BSD-3-Clause), and we
would encourage new contributors to make their contributions available under the
terms of this license.

Please note that MAME is a registered trademark of Gregory Ember, and permission
is required to use the "MAME" name, logo, or wordmark.

<a href="http://opensource.org/licenses/GPL-2.0" target="_blank">
<img align="right" src="http://opensource.org/trademarks/opensource/OSI-Approved-License-100x137.png">
</a>

    Copyright (C) 1997-2020  MAMEDev and contributors

    This program is free software; you can redistribute it and/or modify it
    under the terms of the GNU General Public License version 2, as provided in
    docs/legal/GPL-2.0.

    This program is distributed in the hope that it will be useful, but WITHOUT
    ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or
    FITNESS FOR A PARTICULAR PURPOSE.  See the GNU General Public License for
    more details.

Please see COPYING for more details.
