# QMK Notes

* [According to a reddit thread in 2020](https://archive.is/Zqeq5), the QMK API was updated to use JSON keymaps. This allows the JSON exports from the [QMK Configurator](https://config.qmk.fm/) to be compiled directly using the [`qmk compile`](https://docs.qmk.fm/cli_commands#qmk-compile) command.
* Regarding `qmk compile`, if both `keymap.json` and `keymap.c` exist in the keymap folder, it will prioritize `keymap.json`.
* The documentation is not very straightforward to follow. I couldn't figure out how to set up lighting layers because enabling the RGB and Backight features pushed the firmware size past the limit of the keyboard's microcontroller. For now, I have to settle for VIA configuration.

## VIA
* The latest VIA firmware (rev6b) can be downloaded from the [keebio docs website](https://docs.keeb.io/iris-rev6-rgb-via). Flash it using 
    ```
    qmk flash keebio_iris_rev6b_via.hex
    ```
* MAKE SURE TO BACK UP THE VIA SETTINGS! I already lost my first keymap due to a weird bug that borked the keyboard. I had to reflash the firmware to fix it.
