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

  * [alpha](https://st.suckless.org/patches/alpha/) - This patch allows users to change the opacity of the background. Note that you need an X composite manager (e.g. picom, xcompmgr) to make this patch effective.
  * [bold is not bright](https://st.suckless.org/patches/bold-is-not-bright/) - In st, bold text is rendered with a bold font in the bright variant of the current color. This patch makes bold text rendered simply as bold, leaving the color unaffected.
  * [boxdraw](https://st.suckless.org/patches/boxdraw/) - Custom rendering of lines/blocks/braille characters for gapless alignment.
  * [copyurl](https://st.suckless.org/patches/copyurl/) - Select and copy the last URL displayed with `ctrl+u`. Multiple invocations cycle through the available URLs.
  * [externalpipe](https://st.suckless.org/patches/externalpipe/) - Reading and writing st's screen through a pipe.
  * [open_copied_url](https://st.suckless.org/patches/open_copied_url/) -  Open contents of the clipboard in a user-defined browser.
  * [keyboard select](https://st.suckless.org/patches/keyboard_select/) - This patch allows you to select and copy text to primary buffer with keyboard shortcuts like the perl extension keyboard-select for urxvt.
  * [scrollback](https://st.suckless.org/patches/scrollback/) - Scroll back through terminal output using `ctrl+shift+{k, j}` or `shift+mousewheel`.
  * [vertcenter](https://st.suckless.org/patches/vertcenter/) - Vertically center lines in the space available if you have set a larger chscale in config.h.
  * [xresources](https://st.suckless.org/patches/xresources/) - This patch adds the ability to configure st via Xresources. At startup, st will read and apply the resources named in the resources[] array in config.h.

## Credits

Based on Aurélien APTEL <aurelien dot aptel at gmail dot com> bt source code.

