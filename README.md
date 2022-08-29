# zelda3-flatpak

Flatpak manifest to build @lukeusher's [fork of zelda3](https://github.com/LukeUsher/zelda3).

## Instructions

First, clone this repository.

Next, you need your *own copy* of the ROM 'SNS-ZL-USA'. Copy that into the folder where you cloned this repo. Name it 'zelda3.sfc'.

Then, build and install the flatpak with:

    $ flatpak-builder build-dir org.lukeusher.Zelda3.yml --user --install --force-clean
    
To export it to another device (e.g. Steam Deck), create a bundle with:

    $ flatpak build-bundle ~/.local/share/flatpak/repo org.lukeusher.Zelda3.flatpak org.lukeusher.Zelda3
    
This pulls the version you just built and installed as a user and puts it into a bundle that you can transfer (maybe kinda, not super sure on that).
    
To install from bundle:
   
    $ flatpak install --user org.lukeusher.Zelda3.flatpak
    
Note that installing as a user is required for reasons that are flatpak arcana.

## Running

After installing the flatpak, an entry named 'Zelda3' can be found in your desktop environment's applications menu or you can run it from a terminal with:

    $ flatpak run org.lukeusher.Zelda3

## TODO

 - [X] ~~Add .desktop file and icon~~ (MarkkusBoi)
 - [ ] Remove python dependencies from final package
