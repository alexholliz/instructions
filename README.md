# Wind Waker Instructions

## Assumptions
* You have already installed Emudeck on your SteamDeck: <https://www.emudeck.com/#how_to_install>
  * From Desktop Mode on the SteamDeck, download the installer, and run it. Use simple mode.
  * If you have a secondary SD card popped in for storage, make sure that is formatted correctly: <https://help.steampowered.com/en/faqs/view/69E3-14AF-9764-4C28> Scroll down to data storage heading.
    * The installer will ask about your secondary SD card, so check the box if you do have one installed, it will install the Emulators directory there.
* You have a mouse and keyboard and/or SSH access to the steamdeck to transfer files

## Process
1. Download the file from google drive, either to the deck itself, or to your desktop and transfer it
    * To Download to the deck itself, I'd copy the Google Drive link, and drop that in a steam chat to yourself or someone else so that you can bring it up in steam chat in desktop mode, and download it from there.
2. Unzip the downloaded file on the steamdeck.
    * At this point it might behoove you to start using terminal for things. If you downloaded it to the downloads directory, you can get there in terminal with `cd ~/Downloads` (change directory, ~ means "home" and ~/Downloads means "Downloads directory relative to the steam deck user "deck" "home")
    * Unzipping would look like:
      ```
      cd ~/Downloads
      unzip WindWaker.zip
      ```
3. Your unzipped files will be a Wind Waker iso that is prepatched with the widescreen mod, and the betterww mods, so those are installed. The other directory, "GZL" is the high-res texture pack.
4. Move the Wind Waker iso to the Emulator rom folder. With terminal, (if you have your SD card set up) that is:
    ```
    mv Legend\ of\ Zelda,\ The\ \-\ The\ Wind\ Waker\ \(USA\).iso /run/media/mmcblk0p1/Emulation/roms/wii/
    ```
5. Now copy your high res textures to the Dolphin texture mods directory:
    ```
    mv GZL ~/.var/app/org.DolphinEmu.dolphin-emu/data/dolphin-emu/Load/Textures/
    ```
6. Now run the Emudeck "Steam Rom Manager" from the Desktop of the steamdeck. On the bottom... middle-ish, you'll see "Generate Previews". Click that, then when it's done, hit "Save App List"
7. Close Steam Rom Manager, and return to Steam Deck Mode. Voila!
