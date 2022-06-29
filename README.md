pySim - Read, Write and Browse Programmable SIM/USIM Cards
====================================================

This repository contains Python programs that can be used
to read, program (write) and browse certain fields/parameters on so-called programmable
SIM/USIM cards.

Such SIM/USIM cards are special cards, which - unlike those issued by
regular commercial operators - come with the kind of keys that allow you
to write the files/fields that normally only an operator can program.

This is useful particularly if you are running your own cellular
network, and want to issue your own SIM/USIM cards for that network.


Homepage and Manual
-------------------

Please visit the [official homepage](https://osmocom.org/projects/pysim/wiki) for usage instructions, manual and examples.

Git Repository
--------------

You can clone from the official Osmocom  git repository using
```
git clone git://git.osmocom.org/pysim.git
```

There is a cgit interface at <https://git.osmocom.org/pysim>


Installation
------------

Please install the following dependencies:

 - pyscard
 - serial
 - pytlv
 - cmd2 >= 1.3.0 but < 2.0.0
 - jsonpath-ng
 - construct
 - bidict
 - gsm0338

Example for Debian:
```
apt-get install python3-pyscard python3-serial python3-pip python3-yaml
pip3 install -r requirements.txt
```

After installing all dependencies, the pySim applications ``pySim-read.py``, ``pySim-prog.py`` and ``pySim-shell.py`` may be started directly from the cloned repository.

### Archlinux Package

Archlinux users may install the package ``python-pysim-git``
[![](https://img.shields.io/aur/version/python-pysim-git)](https://aur.archlinux.org/packages/python-pysim-git)
from the [Arch User Repository (AUR)](https://aur.archlinux.org).
The most convenient way is the use of an [AUR Helper](https://wiki.archlinux.org/index.php/AUR_helpers),
e.g. [yay](https://aur.archlinux.org/packages/yay) or [pacaur](https://aur.archlinux.org/packages/pacaur).
The following example shows the installation with ``yay``.

```sh
# Install
yay -Sy python-pysim-git

# Uninstall
sudo pacman -Rs python-pysim-git
```


Mailing List
------------

There is no separate mailing list for this project. However,
discussions related to pysim-prog are happening on the
<openbsc@lists.osmocom.org> mailing list, please see
<https://lists.osmocom.org/mailman/listinfo/openbsc> for subscription
options and the list archive.

Please observe the [Osmocom Mailing List
Rules](https://osmocom.org/projects/cellular-infrastructure/wiki/Mailing_List_Rules)
when posting.


Contributing
------------

Our coding standards are described at
<https://osmocom.org/projects/cellular-infrastructure/wiki/Coding_standards>

We are using a gerrit-based patch review process explained at
<https://osmocom.org/projects/cellular-infrastructure/wiki/Gerrit>


Documentation
-------------

The pySim user manual can be built from this very source code by means
of sphinx (with sphinxcontrib-napoleon and sphinx-argparse).  See the
Makefile in the 'docs' directory.

A pre-rendered HTML user manual of the current pySim 'git master' is
available from <https://downloads.osmocom.org/docs/latest/pysim/> and
a downloadable PDF version is published at
<https://downloads.osmocom.org/docs/latest/osmopysim-usermanual.pdf>.

A slightly dated video presentation about pySim-shell can be found at
<https://media.ccc.de/v/osmodevcall-20210409-laforge-pysim-shell>.


pySim-shell vs. legacy tools
----------------------------

While you will find a lot of online resources still describing the use of
pySim-prog.py and pySim-read.py, those tools are considered legacy by
now and have by far been superseded by the much more capable
pySim-shell.  We strongly encourage users to adopt pySim-shell, unless
they have very specific requirements like batch programming of large
quantities of cards, which is about the only remaining use case for the
legacy tools.

