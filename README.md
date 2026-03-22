<img src="https://github.com/FastEverLast/ESPIR-DB/blob/main/assets/banner.png" width="200%" />

<p align="center">
    A collective of IR codes for a variety of <a href="https://esphome.io/">ESPHome</a> Projects
</p>

> [!IMPORTANT]
> By submitting you agree to license your work under the [CC0-1.0 license](https://choosealicense.com/licenses/cc0-1.0/). 


## Contributing

All contributions are welcome 
If you would like to add IR codes the repository is lacking, **please do so!**

This repo is organised in the following fashion in descending order:
```diff 
Device Type > Device Brand > Device Series (if known/applicable)
```

All files should follow the `<brand>_<model>.yaml` naming scheme and please also ensure the letters in the model name is capatalised:

* :white_check_mark: `LG_OLED65C8PUA.yaml`
* :x: `LG_OLED65C8PUA.txt` (wrong extension)
* :x: `lg_oled65c8pua.yaml` (model numbers not capitalized)
* :x: `tv.yaml` (too generic)

Files should contain a snippet of the ESPHome code, oragnised as shown:

```bash
...
- platform: template
    name: "Vol_dn"
    on_press:
      - remote_transmitter.transmit_rc5:     
          address: 0x10
          command: 0x11
...
```

It's helpful to add further information as a comment directly into the yaml file if possible. Make, model, link, or even a short description can be helpful if the name is changed (or just in general).

### Naming Scheme

We use a standardised naming scheme to more easily identify the purpose of each template. `(Attribution to` [Flipper IRDB](https://github.com/Lucaslhm/Flipper-IRDB/tree/main) `for coming up with this naming scheme)`

| Audio / Video Devices  | ACs       | LEDs            |
| ---------------------- | --------- | --------------- |
| `Power`                | `Off`     | `Power_off`     |
| `Vol_up`               | `Cool_hi` | `Power_on`      |
| `Vol_dn`               | `Cool_lo` | `Brightness_up` |
| `Next`                 | `Heat_hi` | `Brightness_dn` |
| `Prev`                 | `Heat_lo` | `Red`           |
| `Mute`                 | `Dh`      | `Green`         |
| `Play`                 |           | `Blue`          |
| `Pause`                |           | `White`         |
| `Play_pause`           |           | `Yellow`        |
| `Ok`                   |           |                 |
| `Up`                   |           |                 |
| `Down`                 |           |                 |
| `Left`                 |           |                 |
| `Right`                |           |                 |
| `Back`                 |           |                 |
| `Sleep`                |           |                 |
| `Ch_next`              |           |                 |
| `Ch_prev`              |           |                 |




### Attribution

**Banner Text:**  [Pixelated font](https://www.dafont.com/pixelated.font) by Skylar Park [License](http://creativecommons.org/licenses/by-sa/3.0/)\
                  [Skew it](https://www.dafont.com/skew-it.font) by Prask
                  
