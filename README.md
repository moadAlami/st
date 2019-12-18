# st - simple terminal

st is a simple terminal emulator for X which sucks less.


## Requirements

In order to build st you need the Xlib header files.


## Installation

Edit config.mk to match your local setup (st is installed into
the /usr/local namespace by default).

Afterwards enter the following command to build and install st (if
necessary as root):

    make clean install


## Running st

If you did not install st with make clean install, you must compile
the st terminfo entry with the following command:

    tic -sx st.info

See the man page for additional details.


## Patches

This build uses the following patches:

  * [alpha](https://st.suckless.org/patches/alpha/) - This patch allows users to change the opacity of the background. Note that you need an X composite manager (e.g. compton, xcompmgr) to make this patch effective.
  * [bold is not bright](https://st.suckless.org/patches/bold-is-not-bright/) - In st, bold text is rendered with a bold font in the bright variant of the current color. This patch makes bold text rendered simply as bold, leaving the color unaffected.

## Credits

Based on Aurélien APTEL <aurelien dot aptel at gmail dot com> bt source code.

