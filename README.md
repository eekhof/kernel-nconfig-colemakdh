= Kernel nconfig ColemakDH-Bindings

This patch applies ColemakDH-Bindings to the kernel config. All controls remain the same, except the movement keys `n e i o` instead of `h j k l` are now used to go left, down, up and right, and also select or deselect ("o") options. In ColemakDH-Bindings "h" is conveniently placed to summon the help of any selected option. `nconf.gui.c` was also modified to allow closing e.g. help windows with another press of `h`

== Installation:
To install, replace the files `.scripts/kconfig/nconf{,.gui}.c` with the file `nconf{,.gui}.c` from this repo, or apply the patches.

Then run `make nconfig` as usual.

== Typical workflow:
- Use `e i` to navigate up and down through options
    - Use `n o` to go up or down hierarchy
- Use `h` to show help window for currently selected option
    - Use `e i` in the option window to scroll up and down in the help text
    - Use `h` again to close the help window
- Use `SPACE` to select or deselect (or change into module) an option
- Use `F6` to save to a filename that can be set and `ESC` exit
