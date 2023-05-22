# GTKthings

A small collection of GNOME-related things I made for <a href="https://www.reddit.com/r/gnome/comments/13oic6h/i_3_gnome_but_the_one_thing_i_want_to_steal_from/">this Reddit post</a>.


# extensions/custom-accent-colors@rgbmew/
This folder contains a small fork of <a href="https://extensions.gnome.org/extension/5547/custom-accent-colors/">Custom Accent Colors by demiskp</a> to add titlebar tint. Just like with the original extension, you need to relog for it to take full effect.

It's also worth mentioning that the way I added the titlebar tint, some GTK3 windows don't play well with it, and just use the default white/black. This happens because I set transparency for the titlebar color, so it works in both dark and light mode. <b>If anybody knows a way to change colors based on dark/light without using transparency to overlay it on the original titlebar color, please send a PR!</b> Although they SHOULD work with all normal titlebars for legacy apps, and all libadwaita titlebars.

# config/gtk-4.0/more.css
This is another change that I made to <a href="https://extensions.gnome.org/extension/5547/custom-accent-colors/">Custom Accent Colors</a>. You can load other custom CSS in addition to the custom accent color. The original extension would just overwrite any CSS that was in ~/.config/gtk-4.0/ and ~/.config/gtk-3.0/, the edit I made is that it will still overwrite those files, but ALSO look for more css in ~/.config/gtk-4.0/more.css, if you have more custom CSS you want to load (like the Unite extension, or small edits to libadwaita).

The file in there right now is a small example of what you can do with it. I changed the roundness of tabs, the sharpness of window corners, and added and example for how to add Unite support.

# themes/adw-gtk3-compact/
A compact version of <a href="https://github.com/lassekongo83/adw-gtk3">adw-gtk3</a>! This basically only effects the size of window titlebars. I also added comments in /gtk-3.0/libadwaita.css that say "EDIT HERE!!!!!!!!!!!!!!!!!!!!!!!!1" if you want to change the sharpness of window corners. All other changes can be easily understood by comparing the original adw-gtk3, and adw-gtk3-compact in <a href="https://flathub.org/apps/org.gnome.meld">Meld</a>.


Special thanks to demiskp for making an awesome extension, and lassekongo83 for making an awesome theme!
