# asp32

asp32 is a fork of `asp` to work with the Archlinux32 packages.
It is currently hosted on https://git.archlinux32.org/archlinux32/asp32.
The original for Archlinux can be found at https://github.com/falconindy/asp.

`asp32` is a tool to manage the build source files used to create Arch Linux
packages. It replaces the `abs` tool, offering more up to date sources (via the
svntogit repositories) and uses a sparse checkout model to conserve diskspace.
This probably won't be interesting to users who want a full checkout (for
whatever reason that may be).

# Setup

None! Though, it should be noted that the `ASPROOT` environment variable
will control where `asp32` keeps its local git repo. By default, this is
`${XDG_CACHE_HOME:-$HOME/.cache}/asp32`.

# Examples

Get the source files for some packages:

~~~
asp32 export pacman testing/systemd extra/pkgfile
~~~

Get a fully functional git checkout of a single package:

~~~
asp32 checkout pkgfile
~~~

List the repositories a package has been pushed to:

~~~
asp32 list-repos pacman
~~~

