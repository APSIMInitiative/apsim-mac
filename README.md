# apsim-mac

Gtk dependencies for running apsim on a mac. These are bundled with the apsim mac installer, so no one should really need to use this directly.

These deps were generated with the help of the [gtk-mac-bundler](https://gitlab.gnome.org/GNOME/gtk-mac-bundler) and [gtk-osx](https://gitlab.gnome.org/gtk-osx) tools. gtk-osx was used to compile and install gtk and its dependencies on a mac, and gtk-mac-bundler is used to bundle the runtime dependencies of apsim in a convenient format.

# Rebuilding

In order to rebuild the dependencies, you will need a mac. You should be able to generally follow the instructions on [these](https://wiki.gnome.org/Projects/GTK/OSX/Building) [two] (https://wiki.gnome.org/Projects/GTK/OSX/Bundling) pages, however I've provided scripts in this repository to mostly automate the experience. Nonetheless, the general procedure is listed below.

## Requirements

- As mentioned on [this page](https://wiki.gnome.org/Projects/GTK/OSX/Building), if you have HomeBrew, MacPorts or Fink installed, you must remove all traces of them from your environment before you try to run jhbuild. The easiest way is to create a new user and run jhbuild while logged in as that user. **Mixing HomeBrew, MacPorts, or Fink with gtk-osx will fail.**

## Instructions

- Run build.sh (this will take a long time)
- After rebuilding the dependencies, you will likely need to update the docker image used to build the apsim mac installer - at the time of writing, this is apsiminitiative/apsimng-complete.
