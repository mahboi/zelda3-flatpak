# zelda3-flatpak

Flatpak manifest to build @lukeusher's [fork of zelda3](https://github.com/LukeUsher/zelda3).

## Instructions

First, clone this repository.

Next, you need your *own copy* of the ROM 'SNS-ZL-USA'. Copy that into the folder where you cloned this repo. Name it 'zelda3.sfc'.

Then, build and install the flatpak with:

    $ flatpak-builder build-dir org.lukeusher.Zelda3.yml --user --install --force-clean
    
Then, you can run it with:

    $ flatpak run org.lukeusher.Zelda3
    
To export it to another device (i.e. Steam Deck), create a bundle with:

    $ flatpak build-bundle ~/.local/share/flatpak/repo org.lukeusher.Zelda3.flatpak org.lukeusher.Zelda3
    
This pulls the version you just built and installed as a user and puts it into a bundle that you can transfer (maybe kinda, not super sure on that).
    
    
## TODO

 - [ ] Add .desktop file and icon
 - [ ] Remove python dependencies from final package
