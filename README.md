# Usage

This project is a mirror of [The Tree Command For Linux Homepage](http://mama.indstate.edu/users/ice/tree/). I have modified it so that you can use it on Mac. 

Open a new `Terminal`, and

```bash
cd Desktop # Navigate to Desktop where we'll be downloading the repo
git clone https://github.com/hongtaoh/tree-1.8.0 # Clone the repo
mv ~/Desktop/tree-1.8.0/tree /usr/local/bin/ # Move tree to /usr/local/bin
```
Done. 

You can generate the directory tree under the current directory. For example, 

```bash
cd tree-1.8.0
tree
```

or generate the directory by specifying the exact path following `tree`

```bash
tree /anywhere/you/like/
```

To remove `tree-1.8.0` from Desktop:

```bash
rm -rf tree-1.8.0
```

The following is the original README:

## The Original README

  Please read the INSTALL file for installation instructions, particularly if
you are installing on a non-Linux machine.

  This is a handy little utility to display a tree view of directories that
I wrote some time ago and just added color support to.  I've decided that
since no one else has done something similar I would go ahead and release
it, even though it's barely a 1st year CS student hack.  I've found it damn
handy to peruse a directory tree though, especially when someone is trying to
hide something from you.

  The main distribution site for tree is here:

  http://mama.indstate.edu/users/ice/tree/
  ftp://mama.indstate.edu/linux/tree/

  If you don't like the way it looks let me know how you think it should be
formatted. Feel free to suggest modifications and additions.

  Thanks go out so the following people who have helped bring tree to the
pinnacle of perfection that it is: ;)

Francesc Rocher
  - Added HTML output (-H).
  - Added options -o, -L and -R.

Gerald Scheidl
  - Added -S option to print ASCII graphics lines for use under linux
    console when an alternate console font has been selected (might also
    work under DOS telnet).

Guido Socher (and others)
  - Made tree more portable.  Should compile under solaris.

Mitja Lacen
  - Discovered bug where tree will segmentation fault on long pathnames.
  - Discovered in -L argument processing.

Nathaniel Delage
  - Discovered problem with recursive symlink detection

A. Karthik
  - Suggested option to remove file and directory report at end of tree
    listing.

Roger Luethi
  - Spotted memory over-allocation bug in read_dir().
  - Submitted several patches to fix various memory leaks.

Daniel Lee
  - Reported that Tru64 defines TRUE/FALSE in sys/types.h (OSF1 standard?)

Paolo Violini
  - Found bug in tree that caused it to seg-fault if 50 file arguments where
    given and directory coloring was turned on.

Mitsuaki Masuhara
  - Discovered tree crashed on missing arguments.
  - Discovered that tree did not properly encode characters in filenames
    when used as URLs when using the -H option.
  - Fixed issue with --charset option processing.

Johan Fredrik
  - Pointed out that tree did not list large files.

Ted Tiberio
  - Submitted patch which fixed a compiler issue and cleaned up HTML and CSS
    code, applied CSS to all output, and fixed up HTML to 4.01 strict
    standards.

David MacMahon
  - Added '|' support to the pattern matching routines.

Dan Jacobson
  - Pointed out that -t did not sort properly for files with the same
    timestamp.
  - Suggested option to change HTML title and H1 string.
  - Suggested -r option for reversed alphanumeric sort ala 'ls -r'.

Kyosuke Tokoro
  - Provided patch to support OS/2, fix HTML encoding, provide charset
    support. Added to authors list.

Florian Ernst
  - Debian maintainer who pointed out problems and applied fire to feet to fix
    stuff.

Jack Cuyler
  - Suggested -h option for human readable output for -s, ala ls -lh.

Jonathon Cranford
  - Supplied patch to make tree under cygwin.

Richard Houser
  - Provided patch to fix a colorization bug when dealing with special
    files and directories that seem to have an extension.

Zurd (?)
  - Suggested removing trailing slash on user supplied directory names if -f
    option is used.

John Nintendud
  - Pointed out broken HTML output in 1.5.1.

Mark Braker
  - Suggested --filelimit option.

Michael Vogt
  - Suggested -v option (version sort).

Wang Quanhong
  - Provided build options for Solaris.

Craig McDaniel
  - Provided build options and source mods for HP NonStop support.

Christian Grigis
  - Noted that setlocale() should come before MB_CUR_MAX check.

Kamaraju Kusumanchi
  - Submitted patch to remove compiler warnings for Solaris.

Martin Nagy
  - Provided patch which fixes issue where indent may output more than it
    should when dirs[*] is not properly cleared before use.

William C. Lathan III
  - Showed that tree was not properly quoting arguments to recursively called
    tree instances when using -R.

Ulrich Eckhardt
  - Submitted patch for --si option.

Tim Waugh (redhat)
  - Pointed out a potential memory leak in listdir().

Markus Schnalke
  - Tracked down bug where tree would print "argetm" before the filename of a
    symbolic link when the "target" option was specified for LINK in dircolors.

Ujjwal Kumar
  - Suggested that tree backslash spaces like ls does for script use.  Made
    output more like ls.

Ivan Shmakov
  - Pointed out multiple CLI defenciencies (via Debian)

Mantas Mikulnas
  - Provided patch to make tree more reliably detect the UTF-8 locale.

Tim Mooney
  - Noticed S_ISDOOR/S_IFDOOR spelling mistake for under Solaris.

Han Hui
  - Pointed out possible memory overflow in read_dir (path/lbuf not equal in size
    to pathsize/lbufsize.)

Ryan Hollis
  - Pointed out problems with the Makefile w/ respect to OSX.

Philipp M?ller
  - Provided patch for filesize sorting.

Sascha Zorn
  - Pointed out that the HTML output was broken when -L 1 option was used.

Alexandre Wendling
  - Pointed out that modern systems may use 32 bit uid/gids which could lead
    to a potential buffer overflow in the uid/gid to name mapping functions.

Florian Sesser
  - Provided patch to add JSON support.

Brian Mattern & Jason A. Donenfeld
  - Provided patch to add --matchdirs functionality.

Jason A. Donenfeld
  - Added --caseinsentive, renamed --ignore-case option.
  - Bugged me a lot.

Stephan Gabert
  - Found a bug where the wrong inode (and device) information would be printed
    for symbolic links.


And many others whom I've failed to keep track of.  I should have started
this list years ago.

						- Steve Baker
						  ice@mama.indstate.edu
