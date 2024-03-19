# GRScheller Software Development Blog

The GitHub Pages version of this Blog is still a work in progress.

For a better viewing experience, view the source code for ths blog
[here](https://github.com/grscheller/web/blob/main/src/blog.md)
in its source code tree.

#### My PyPI Project Repositories:

* [grscheller.boring-math](https://pypi.org/project/grscheller.boring-math/)
* [grscheller.datastructures](https://pypi.org/project/grscheller.datastructures/)

#### My GITHUB Repositories:

* [dotfiles](https://github.com/grscheller/dotfiles)
* [boring-math](https://github.com/grscheller/boring-math)
* [circular-array](https://github.com/grscheller/circular-array)
* [datastructures](https://github.com/grscheller/datastructures)
* [grok-lua](https://github.com/grscheller/grok-lua)
* [grok-typescript](https://github.com/grscheller/grok-typescript)
* [fpinScala3Stdlib](https://github.com/grscheller/fpinScala3Stdlib)
* [neovim-notes](https://github.com/grscheller/neovim-notes)
* [git-notes](https://github.com/grscheller/git-notes)
* [scheller-linux-archive](https://github.com/grscheller/scheller-linux-archive)
* [web](https://github.com/grscheller/web)

#### My GitHub Pages:

* [PyPI grscheller Project Repos](https://grscheller.github.io/web/pypi_repos.html)
* [GRScheller Bookmark Page](https://grscheller.github.io/web/bookmark.html)
* [GRScheller Software Development Blog](https://grscheller.github.io/web/blog.html)

### Added a Lua project to master Lua \[2024-03-18\]:

This project is similar to one I created back on 2024-01-21 to take my
first beginning steps with TypeScript (TS). Unlike that project, I am
starting off at an intermediate skill level with Lua. My experience
comes from maintaining my Lua based Neovim configuration files and
helping my daughters with Luau based Roblox code. See

* [grscheller/grok-lua](https://github.com/grscheller/grok-lua)
* [grscheller/grok-typescript](https://github.com/grscheller/grok-typescript)

Most of the front-end developers I work with started off learning React.
Someday I might do so too, with React or whatever its successor might
be, but not before implementing a crude web framework myself.

I wish I lived in a world where Lua, and not TypeScript, was the
embedded language of web browsers. 

### Added another PyPI projects \[2024-03-17\]:

I started another Python Package Index project named
grscheller.circular-array back on 2024-01-28. I split this data
structure out of grscheller.datastructures. It is a stable release at
version 2.0.0 (I was a bit optimistic for version 1.0.0). It is used by
both my other PyPI projects. I thought it might be more useful to the
Python development community if it were its own project and not just
a utility class buried in my grscheller.datastructures project.

The CircularArray class implements the classic circular array datatype
from college level computer science data structure courses. It is
a stateful, auto-resizing, indexable, double sided queue data structure
with O(1) indexing and O(1) pushes and pops from either end. This data
structure is not slicable.

When iterated over, it caches its current state so that the data
structure can safely mutate while the iterator leisurely iterates.

The class wraps a python list. It can be used directly as an improved
version of a Python List, or in the implementation of other data
structures in a "has-a" relationship. It uses `__slots__` for size and
speed efficiency. It is not designed to be used as the base of some sort
of inheritance hierarchy, so if that is what you want to do, you will
need to add a `__dict__` to it. Or just fork it and take out the slots.

### Maintaining two PyPI projects \[2024-01-18\]:

I now maintain two projects on the Python Package Index (PyPI).

* grscheller.boring-math
* grscheller.datastructures

At work last year, late in the summer, I was a bit sort on my
"acquisition continuous learning points." I work for a DoD research lab
and my position is acquisition coded. A coworker suggested I take on
data structures on-line course. I thought it might be a nice review.
I had experience in most of the data structures covered, but I had never
heard of one called a "circular array" before. So I coded one up quickly
in Python. I thought of adding it to my mosh-pit of code snippets I have
in my scheller-linux-archive GitHub repo. Well, over the past several
years I have been struggling to grok the Python packaging ecosystem.
Using this as an opportunity to learn, I decided to make my little
circular array program into its own PyPI project. 

Well, that little circular array program has grown into a data structure
package that supports functional programming. I tried to keep the
package pythonic. It does not force functional programmming onto the
user, nor does it force uncaught exceptions either. The data structures
do not store Python None as a value. This empowers the package to
semantically interpret None as a non-existent value. How does one store
something that does not exist in a concrete data structure anyway? Any
case, I do use None as an implementation detail.

The second project, Daddy's Boring Math Library, is based on a Python
module I wrote back in 2016 when I started to seriously learn Python.
The name was suggested by my then 13 year old daughter Mary. I have
Master degrees in Mathematics and Physics, so I expect this project to
gradually grow over the next few years based on my recreational
mathematical interests.

Both projects use Flit as the build and publishing tool to PyPI.

### Moved blog to new home \[2023-10-21\]:

Moved this blog from the **grscheller/scheller-linux-archive** wiki to
GitHub Pages. I maintain the blog in my **grscheller/web** repo. This
repo is where I have started keeping my software deveopment related web
content. It made more sense just deploying my to GitHub Pages than
making it a part of that repo's wiki.

I will continue maintaining the blog in Markdown, but am using Pandoc to
convert it to HTML. The best thing now is that I can maintain the
Markdown using Neovim.

### New GitHub repo for fpinscala \[2023-07-04\]:

Started new repo: **grscheller/fpinScala3Stdlib** to update the work
done in my **grscheller/scheller-linux-archive** repo where I was
working my way through the book
[Functional Programming in Scala](https://www.manning.com/books/functional-programming-in-scala)
by Paul Chiusano and Runar Bjarnason.

The direction of this effort is no longer to recreate an entire FP
infrastructure from scratch. Instead it is to leverage the Scala
Standard libraries and selected external libraries to give *efficient*
examples of functional programming.

I was originally inspired to do this from
[ShapelessCat/fpinscala3](https://github.com/ShapelessCat/fpinscala3)
updated for Scala 3. At this point, I will use Chiusano's and
Bjarnason's book more for inspiration than as a tutorial.

### Almost forgot about this "blog" \[2023-06-03\]:

While determining how likely one of my GitHub repositories will come up
on an internet search, I stumbled upon this blog of mine. I figured its
time I give it a little love.

One thing I have started doing differently is using only one space
between sentences. Won't have any effect on the rendered Markdown
produced for this blog. At work I noticed that everyone below the age of
about 35 never uses two spaces between sentences. Time to help progress
the English language a little bit.

In Neovim `:help` one way to tell if you're looking at older Vim
documentation is if two spaces are used between sentences.

As I write this, I feel completely handicapped by the native text
editing interface GitHub provides. It is not as bad as the ones provides
by email and Microsoft 360 web clients, but it is not Neovim. I won't
hold my breath waiting for a Vim based interface. Probably start editing
this with nvim in a terminal and cut-n-paste here.

I find it interesting that the GitHub editing client is pegging "Neovim"
and "nvim" as spelling mistakes, but not Emacs, Vim, nor Nano.

### Dropping Gnome 3 in favor of Sway \[2021-12-12\]:

I wish I did this a year ago, maybe several years ago if I went with i3
first.

What was holding me back was the proprietary NVIDIA drives my laptop
used. I had chosen GNOME3 because that was what I was forced to use at
work and it was the only thing that seemed to work with my laptop
several years ago. I knew Wayland was on the horizon and I wanted a WM
that supported it.

I was pleased to hear that the NVIDIA drivers were finally going to
support GBM. My hopes were dashed when I learned this was only for new
video cards. The NVIDIA cards in my personal and work laptops were never
going to support anything other than EGL.

Final I got a laptop at work where the UEFI BIOS was not locked
down. I installed Arch Linux and NOT the NVIDIA proprietary
drivers. I was worried that learning the Sway keybindings would be
a burden, but with Sway the keybindings seem natural and intuitive,
unlike keybindings associated with various IDE's I've used off and on
over the years.

I was pleasantly surprised to find that out-of-the-box Sway is sloppy
mouse focused, though with a tiling WM this is not as important
anymore. The amount of unnecessary window shuffling has become
non-existent. The desktop feels very light weight and fast.

I have decided to abandon using NVIDIA proprietary drives and if
possible NVIDIA hardware. Both personal and work laptops have hybrid
Intel/NVIDIA chip sets. Both Intel i915 and nouveau kernel modules are
loaded. Not entirely sure which chip sets are actually being used by
Wayland.

I am happy that I finally get to use Wayland. Even the X Server/XFree86
release manager, Adam Jackson from Redhat, recommends its time we
start to
[migrate off Xorg](https://ajaxnwnk.blogspot.com/2020/10/on-abandoning-x-server.html).

### Bike shedding my Neovim configuration \[2021-07-11\]:

In the last 2 months I have redone my Neovim configuration several
times. Now I am using `~/.config/nvim/init.lua` for my config. I am
sorting out `neovim/nvim-lspconfig` as well as `scalameta/nvim-metals`
for Scala development and `simrat39/rust-tools.nvim` to configure the
rust-analizer LSP server for Rust development.

I have a lot of tweaking to do, but I finally got Metals to work with
Scala 3 code on Arch Linux. The problem was that it was using the wrong
version of the Scala compiler. By dropping `val scala3Version = "3.0.0"`
from the top of build.sbt and hardcoding the version later on, things
worked. Metals must grok build.sbt at a very early stage to determine
the version of the Scala compiler to use.

The Scala 3 code in question, `grok/Scala3/scalaImplicits` from my
`scheller-linux-archive` GitHub repo, is a translation of a Scala
2 version, `grok/Scala2/learnScala/implicits`, which explored Scala
implicits.

Still can't figure out why lspconf configured pyright is failing to find
my Python libraries in a very simple project where I have a very simple
`$PYTHONPATH`, `lib:../lib`, available in the environment.

### Finally making progress with Scala again \[2021-05-31\]:

After 3 years of stagnating with Scala, I am finally making some forward
progress. I have sorted out many of the various overloaded meanings of
implicit in Scala 2, just in time for this to all change for Scala 3. In
Scala 2, implicit conversions, implicit classes, and implicit values for
implicit parameters are all different concepts. Now I have to learn how
all these have been cleaned up in Scala 3.

I really want to like SBT, but there is still too much opaque magic
going on. When I invoking SBT 1.5.0 on a Scala 3.0.0 project, the first
thing it did was to download, locally install, and use SBT
1.5.2. Nothing in the configuration files I created said anything about
using a different version of SBT. I have no clue where this choice of
SBT is coming from nor is it obvious to me even to know where to start
looking for where this is configured.

Scala 3.0.0 reuses the same standard libraries as Scala 2.13.15. As an
artifact of this, in the Scala 3.0.0 REPL

```
   scala> scala.util.Properties.versionString
   val res1: String = version 2.13.5
```

This is due to this version string being defined in the 2.13.15 standard
library. In Scala 3.0.0, but not any of the out-of-the-box 2.13.*
versions,

```
   scala> dotty.tools.dotc.config.Properties.versionString
   val res0: String = version 3.0.0
```

So, there seems to be no "standard" way to universally check the version
of Scala you are running on at either run time or in the REPL.

### Gnome 3 Startup Behavior \[2021-04-18\]:
Recently I noticed that configuring Alacritty terminal emulator to start
the fish shell caused environment variables to be defined which should
not have been. Also the $PATH was badly munged. Making fish my login
shell fixed the $PATH munging issues, but stuff configured only in my
POSIX startup scripts was still making it into my fish environment.
Turns out, that as of at least Gnome Shell 3.38.4, Gnome Display Manager
was causing this.

GDM __NON-INTERACTIVELY__ sources my `~/.profile` with /etc/gdm/Xsession
using /bin/sh during the Gnome3 startup process!!! Now, ~/.profile is
supposed to be sourced only by interactive shells. Fixed the problem by
putting an interactive shell test in ~/.profile, like I have in my
~/.bashrc and ~/.shrc files.

This sourcing behavior might come in handy, especially if I ever want to
play around alternate $XDG_CONFIG_HOME configurations. Just wished
I would have been given a heads up on this behavior.

### The "POSIX Shell" \[2020-11-12\]:

There is no such thing as the POSIX shell. POSIX shell is an IEEE/Open
Group specification. The original AT&T "Bourne Shell" is not a POSIX
compliant shell. The POSIX Shell specification says what a POSIX
compliant shell must do when given a __POSIX complient__ script. The
specification does not say what a POSIX compliant shell should do, or
not do, when given a non-POSIX complient script. A shell running in
strict POSIX compatibility mode is only limited to what it can do when
given a POSIX compliant feature. If a script runs on one POSIX compliant
shell, there is no guarantee that it will run on another POSIX compliant
shell.

So, how does one test a shell script to make sure it contains only POXIX
compliant features? I find the ShellCheck utility a very valuable
resource. This is especially true when ShellCheck is paired with the
Syntastic Vim plugin.

Writing portable shell scripts can be a challenge. Some people try to
write in the most lowest common denominator of shell to accomplish
this. I think this is a fool's errand. How can one design a script to
work against every possible Bourne descendant shell ever to have
existed, unless one tests it against every possible Bourne descendant
shell ever to have existed?

### Shell startup in historical context \[2020-07-28\]:

Traditionally, a UNIX shell sets up an initial shell environment when
logging into a system via a login shell. The shell would source a file
like ~/.profile to establish an initial $PATH and export shell
variables. Then it would source a file referenced by the environment
variable $ENV, typically ~/.shrc or ~/.shinit, to pick up shell
functions and aliases.

Aliases and shell functions are not exported to the environment but are
picked up afresh with each new shell session via sourcing config files
like ~/.bashrc. (Actually, shell functions can be exported to the
environment, but this is not typically what is done). By shell session,
I am talking about a completely new instance of the shell, not just
a subshell.

This worked well until the age of Display Managers. A Display Manager is
an X-windows client that logs you directly into your
X-session. X-Windows is already running under root and a user owned
Session Manager sets up the Desktop Environment. From this environment,
client programs, including terminal emulators, can be launched. The user
is "logged" into the X-Session, __not__ a login shell. As a result,
.profile does not get sourced.

Why not just use .bashrc to configure an initial Bash environment? The
problem is is that .bashrc will force __every__ bash shell to the
__exact same__ configuration, not just the first initial shell in
a terminal window.

When I first started using AT&T System V UNIX, I would login at a real
terminal, sometimes connected directly to computer, other times through
a network terminal server, and, after logging in, be in a login shell.

Later I would telnet or dial into the UNIX host via a DOS/Windows telnet
or hyperterminal PC client. Again, invoking a login shell.

I first started using UNIX Desktop Environments via a DOS based
protected mode PC X-terminal emulator and the Tab Window Manager
(twm). Later I used CDE on Solaris 2.6 with an actual X-terminal. An
X-terminal was a TCP/IP networked CRT & keyboard that ran an embedded
X-server without a window manager. In both cases, the BOOTP protocol was
used to figured out what UNIX host to contact and display back an
X-windows "console window" client. After logging in with such a "console
window," guess what, you were in a ksh login shell. AFTER logging in,
you would use the startx command to launch a remote Window Manager
client to manage the remote applications displayed in the local
X-Windows server. Back then I think the Window Manager doubled as the
Session Manager, but I could be wrong.

You see the pattern? Configure your initial environment with .profile
and used .kshrc to configure aliases and functions. (Back then I only
used functions in shell scripts and never used aliases at all - I may
not have even known about .kshrc) One file to establish a baseline
environment for the initial shell invocation, and another to configure
shell behaviors which stayed consistent across all subsequent shell
invocations.

So, to correctly configure an initial shell environment, I put a hooks
in my .rc files to source a file called `.envrc` to set up the initial
environment if this had not aleady been done. My .profile also sources
this file.

No shell variables get "exported" in my rc files. Don't need to unless
I wanted programs other than the shell to see them. In that case it
would be better to put such exports in my surrogate for .profile,
`.envrc`.

I see the desktop environment as an extension to the command line
environment. I wish my command line and desktop environments to
complement and interact with each other. I use shell environments to
help manage my programming environments.

### Does Microsoft want ignorant end users? \[2019-03-23\]:

Over the last 3 weeks I lost several days of effort getting an NVIDIA
CUDA environment implemented on Windows 10 using Anaconda Python and the
NVIDIA CUDA development kit. The OEM laptop had a NVIDIA Quadro M620
secondary video card (one not physically hooked up to the display),
primarily for gaming purposes, which "should" be CUDA compatible.

This installation would have only taken me an hour or two if Microsoft
didn't hide Windows Device Manager on me! Installation went fine, apart
from having to install NVIDIA's Visual Studio components to keep the
installation program happy.

When I ran a pyTorch python program, it failed to use CUDA.

So, went to open Control Panel, Control Panel program not on start
menu. Something called "Settings App." OK, cell phone
terminology. Opened this and selected Devices. I just assumed this was
the name of the device configuration tool in Windows now, like how
Windows 3.11 Program Manager evolved into the Taskbar and Windows 3.11
File Manager evolved into Windows Explorer. Bad assumption. Was there no
way to list the devices on the PCI bus and their associated device
drivers anymore???

At this point, all MS had to do was leave a Device Manager link right
there, for me to find, not create something called "Settings App" which
stopped me from looking further. After 3 weeks of installs not failing
but pyTorch not using CUDA, I came across the "Device Manager"
terminology in some 10 year old blog post and, not expecting anything to
happen, typed Device Manager into the Start Menu. Lo and behold, good
old Device Manager launched. With an "!" point on the icon for the
NVIDIA card. Drilling down on the icon I discover an error message:

```text
    Windows cannot verify the digital signature for the drivers
required for this device. A recent hardware or software
change might have installed a file that is signed
incorrectly or damaged, or that might be malicious
software from an unknown source. (Code 52)
```

Some web searching on this terminology and "Code 52" identified the
problem, Windows was using Secure Boot to "blacklist" the NVIDIA drivers
I installed.

After going into the UEFI and turning off Secure Boot, pyTorch worked
flawlessly with CUDA.

Windows Device Manager still exists and provides useful functionality,
but is totally disconnected from any GUI/App/Tool which a naive user
will stumble upon. This says to me that Microsoft does not give a rat's
arse about the curious end user wanting a deeper understanding of, and
ability to leverage, their operating system. This stinks of the same "at
all costs protect end-users from themselves" mentality that we see in
Linux desktops environments where the terminal emulator is made very
difficult for new end-users to find.

### In the name of POSIX compliance \[2019-03-17\]:

On GNU/Linux, at least Arch Linux using the GNU glibc library, there is
a trick used in /usr/include/bits/confname.h, included by
/usr/include/unistd.h, to define the `_SC_*`, `_PC_*`, and `_SC_*`
macros used with the sysconf, pathconf, and confstr library functions.

The POSIX standard calls for `_PC_*`, `_SC_*`, and `_SC_*` to be defined
as C preprocessor macros. GNU/Linux implements them as enumerations, but
then turns around and defines macros with the exact same names and
values as the enumeration symbols.

```
   enum
     {
       _PC_LINK_MAX,
   #define _PC_LINK_MAX            _PC_LINK_MAX
       _PC_MAX_CANON,
   #define _PC_MAX_CANON           _PC_MAX_CANON
       _PC_MAX_INPUT,
   #define _PC_MAX_INPUT           _PC_MAX_INPUT
        .
        .
        .
       _PC_2_SYMLINKS
   #define _PC_2_SYMLINKS          _PC_2_SYMLINKS
     };
```

Kinda silly, the sole purpose of these macros are just to meet the
letter of the POSIX standard. I can think of no other purpose they
could serve.

In my own code I would have used different symbols for the enumerations,
perhaps lowercase. I understand GNU not wanting to pollute the global
namespace.

A comment should have been added to this header file explaining what
was being done. Better yet, POSIX should be amended to allow for these
names to be implemented as enumerations.

I hate having to simultaneously program in more than one language at
a time. The less one has to use the C preprocessor the better.
Hopefully real modules will be coming to C sometime soon; its been
40 years too late. At least in C++ enumerations are typed. C needs
better type safety.

### Advanced Programming in the UNIX Environment (APUE) \[2019-01-16\]:

I am making progress working my way through
"Advanced Programming in the UNIX Environment" 3rd edition
by W. Richard Stevens. The book has a website
[APUE](http://apuebook.com/)
with source code, but the version I am developing on GitHub has a more
robust GNU Make based build.

My
[APUE](https://github.com/grscheller/scheller-linux-archive/tree/master/grok/C/APUE)
project is actually two projects. One is just working through the
chapters of the APUE book. The other is more interesting. I am creating
an implementation of Stevens' UNIX System Programming API:

* API implementation: libapue.a and apue.h
* GNU Make build as an initial template for future projects

Currently I only have access to Linux based systems, but eventually wish
to adapt to and test on other Unix like OS's.

### C and C++ really are different languages \[2018-12-16\]:

In one of my
[scheller-linux-archives](https://github.com/grscheller/scheller-linux-archive)
GIT repo's README.md files, I recently waxed poetic on the related topic
of C and C++ as "systems languages." I thought this blog might be
a better place for this material.

C and C++ are best thought of as different languages. The syntax
of C++ is "more or less" a super set of C. Both can be used to
write anything from device drivers to GUI software, but C has some
natural advantages over C++ as a "low level language" for Linux.

C and its predecessor B, a simplified BCLP, were implemented using the
DEC PDP-7 and PDP-11 assembly languages. The syntax mapped well upon the
assembly languages of the day. C becoming popular, kept future assembly
languages compatible to it. Also, C syntax was designed for easy parsing
by the compiler. Hence leading to the syntax which arose.

Also, C is the standard defacto ABI for Linux/POSIX/UNIX. Before UNIX,
the ABI (Application Binary Interface) used to call into an operating
system was the hardware's assembly language. To port an operating system
to another hardware architecture meant basically rewriting it from the
ground up. With C, once you remapped it onto the new assembly language,
much of what was previously developed could be reused.

Thus the reason C is so natural as a systems language for Unix, is that,
except for the isolated uses of assembly code, Unix kernels and device
drivers are written in C.

Different implementations of C++ are usually binary incompatible. By
using 'extern "C" { ... }' directives, or foreign function interfaces in
other languages, the C ABI becomes the lingua franca that glues code
together. This allows user code to easily communicate with the kernel,
which is written in C. Also, the kernel can easily communicate with
device drivers, also written in C.

As system languages, C & C++ rely heavily on OS resources to do their
work. With the right compiler options, C can produce freestanding
software that can run on the "bare metal," i.e. embedded
software. Without ugly hacks, this can't be done for C++, Rust, Haskell,
and other general purpose languages. When used idiomatically, these
languages have abstractions which require OS infrastructure to
implement.

Standards like POSIX and X/Open are very mature and make porting source
code across architectures and OS's not only possible, but cost
effective. These standards also serve to make C, and to a lesser extent
C++, very hard to change.

With 50 years hindsight, could a better low level language be developed?
Most certainly. Will a better, safer, language ever come along and
replace C? Probably not in our lifetimes. C is "good enough" and the
price to replace it "too high."

### Linux/Unix/POSIX Systems Programming \[2018-12-16\]:

I have always admired W. Richard Steven's books on Unix System
programming. Back in the early to mid 1990's, I thought someday I would
work my way through them. Well, I have finally gotten around to it, in
2018.

Wanting to see what the C++ community was up to, I read Bjarne
Stroustrup's "A Tour of C++" Second Edition. I thought that perhaps more
recent versions of C++ would make for a better, safer systems language
than is ANSI-C.

Before starting such an endeavor, I thought I'd best to learn what it is
I am trying to replace. Thanks to the maturity and stability of the
POSIX and X/Open standards, Steven's books are as relevant today as they
were back in the 1990's.

### Slowing up on FP in Scala \[2018-03-01\]:

I having trouble in chapter 9, Parser Combinators in
[Functional Programming in Scala](https://www.manning.com/books/functional-programming-in-scala).
The concept of parsers is not the problem. It is not having a partial
working implementation of the library I am designing to be most
frustrating. My experience has been to get something real simple
working, even if it just a "Hello World" boilerplate program, and rapid
prototype functionality into it. I am also good at taking a "Big Ball of
Mud" production system and, like a bomb disposal expert, carefully
refactor it to something actually maintainable as well as aesthetically
beautiful. The concept of developing laws for a software design before
it is even implemented, and then letting these laws guide the
implementation, is something I will need to get much better at doing.

### Markdown rendering errors \[2017-11-08\]:

I noticed that both pandoc and GitHub render markdown documents with
HTML errors. Consider my GitHub repo's
[README.md](https://github.com/grscheller/scheller-linux-archive/blob/master/README.md)
file. When I validate the HTML via the
[W3C Markup Validation Service](https://validator.w3.org/),
I found 41 errors in the HTML rendered by pandoc and 20 errors in the
HTML generated by GitHub. If you run Firefox from the command line, both
pandoc and GitHub renderings spew forth JavaScript errors.  Not just for
my markdown, it seems to be universal for all GitHub rendered markdown.

Finding errors in the big-ball-of-mud that HTML has become is not really
that surprising. What I find utterly jaw dropping is the lack of
information and/or interest on the Web regarding the existence of these
types of errors!

### Scala Implicits \[2017-08-01\]:

There's seems to be a big hole in my Scala toolbox, __Implicits__.
I like to make everything explicit. I like code that you can reverse
engineer easily. I don't like hunting all over a code base to figure
out the context in which a piece of code is executing. For that reason,
I have tended not to use Scala implicit parameters and conversions.

After viewing
[Martin Odersky's keynote talk](https://www.youtube.com/watch?v=Oij5V7LQJsA&t=190s)
at Scala Days Chicago 2017, I realize that he has many of the same
concerns. I need to try to understand implicit parameters/conversions
because that is an important direction the language is taking. One good
argument he makes is that the Reader Monad is "too powerful" for just
the purpose of defining a context. Implicit techniques are not only much
simpler, they come with a substantially less computational
price. Supplying context should not require sequencing.

### My evolution as a FP Scala Developer \[2017-07-02\]:

1. Using scala as a better java
2. Mix of OOP + FP elements - avoiding vars and nulls
3. Type level annotation - to get OOP and FP to play nice together
4. Use objects as name spaces; replace inheritance with traits & case classes
5. Majority FP - using monads, functional error-handling, composition
6. Pure FP where only inner most and outer most edges of code is imperative
7. Type level programming using type classes and type level features
8. Category theory based programming using scalaz/cats libraries

Currently, I am somewhere between steps 6 and 7. I might go back and try
Haskell again to help me tackle step 8.

### My Scala programmer background \[2017-07-02\]:

I don't come from a Java OOP background. Python run-time OOP allowed me
to finally understand C++ style compile-time OOP. Professionally I have
been able to apply these OOP skills to write very OOP MATLAB GUI
programs, but my experience has been primarily in imperative non-OOP
scientific applications programming for the Department of Defense and
Bell Laboratories. Pick up a lot of scripting tools while a system admin
in the late 1990's and early 2000's.

I am a Linux based developer having learned System V Unix while at Bell
Laboratories in the late 80's and early 90's. I gave up on Windows based
development after reverse engineering enough of Microsoft Visual C++ 4.0
Foundation Class Libraries to be disgusted by them.

For some reason one day, I decided to teach myself Lisp. This is
something I totally failed at while a physics undergraduate in the early
1980's. I wished to see if my increased level of programming maturity
would allow me to learn it. This led be to Racket (PLT Scheme) and
eventually playing with Haskell. I have struggled with Haskell and I am
not yet beyond a beginner level. Despite a master's degree in
mathematics, I found understanding its Category Theory aspects
difficult. I tried using the book
[Real World Haskell](http://book.realworldhaskell.org/)
by Bryan O'Sullivan, Don Stewart, and John Goerzen but was not ready for
it.
[Learn You a Haskell for Great Good!](http://learnyouahaskell.com/)
by Miran Lipovaca was much more helpful to me.

After reading some of the Functional Programming academic papers,
I decided I needed a good FP tutorial. For the past year or so,
I have been working my way through the book
[Functional Programming in Scala](https://www.manning.com/books/functional-programming-in-scala)
by Paul Chiusano and Runar Bjarnason. This led me to the Scala Programming
Language. You can follow my progress working through this book
[here](https://github.com/grscheller/fpinScala3Stdlib).

At this point, I am best described as a functional programming
enthusiast and hobbyist.
