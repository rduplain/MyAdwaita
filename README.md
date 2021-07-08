## MyAdwaita - Personalization of the GNOME Adwaita Theme

For both GTK 2 and GTK 3 applications, using dark mode, like old-school
Zenburn, but emphasizing just three colors: dark gray, not-quite white, and
alien-fruit-salad blue.


### Installation

On GNU/Linux systems:

* Clone to `~/.themes/MyAdwaita`.
* Set `~/.gtkrc-2.0` to
  `include "/home/USERNAME/.themes/MyAdwaita/gtk-2.0/gtkrc"`.
* Use `gnome-tweaks` (e.g. `sudo apt install gnome-tweaks`) to set GTK 3 theme.

Changes are often picked up immediately with new windows, but it's useful to
restart the desktop session when verifying changes. For GTK 2, it's useful to
have a tool such as `gtk-chtheme` (e.g. `sudo apt install gtk-chtheme`) to hit
"Apply" on the selected theme.


### Development

For GTK 2, edit theme files in place.

For GTK 3, edit Sass .scss files to compile to gtk.css. A single-command build
is available with GNU Make, just run `make` in the `gtk-3.0` directory (`make
-C gtk-3.0`). Alternatively, see the `gtk` [README][README] for guidance on
build instructions.

Ruby is required for Sass.

Note that theme personalization forces dark mode; the light variant is unused.

[README]: https://gitlab.gnome.org/GNOME/gtk/-/tree/e0ad573/gtk/theme/Adwaita


### Upstream

* gtk-2.0 theme is a clone of Adwaita-dark from Ubuntu 18.04.
* gtk-3.0 theme originates from [gtk source][gtk] at tag 3.22.14.

[gtk]: https://gitlab.gnome.org/GNOME/gtk.git
