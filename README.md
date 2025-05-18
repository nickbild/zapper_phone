# Zapper Phone

You didn't think the NES Zapper was just for shooting ducks, did you? I turned mine into a wireless phone.

![](https://raw.githubusercontent.com/nickbild/zapper_phone/refs/heads/main/media/logo.jpg)

**Check out the video on YouTube:**
<a href="https://www.youtube.com/watch?v=N6qzJRUytfU">![](https://raw.githubusercontent.com/nickbild/zapper_phone/refs/heads/main/media/youtube_preview.jpg)</a>

I came up with this idea after doing two other projects — reproducing [Alexander Graham Bell's photophone](https://www.youtube.com/watch?v=XQ86fkRRS5M) (the world's first wireless phone from 1880), then doing a deep dive into the [hardware of the NES Zapper](https://www.youtube.com/watch?v=cWvGYfH0B30). Both of these devices have a photosensor that is crucial to their operation. It plays very different roles in each case, but it gave me the idea (and requisite knowledge) to merge the technologies.

## How It Works

### The receiver

The NES Zapper has anti-cheating mechanisms built into it that prevent it from being used for anything other than a light sensor that is tuned to the specific frequency of the electron beam of a CRT TV. After making my [Zapper deep dive video](https://www.youtube.com/watch?v=cWvGYfH0B30), I realized that I could bypass these protections by rerouting the "hit" indicator signal directly to the photodiode itself.

Because of this mod, the hit indicator now gives me an analog signal representing the intensity of the light striking it. That means I can encode audio into light by modulating its intensity, and shine it at the Zapper. Then I can feed the signal from the hit indicator line directly into an audio amplifier and the sound will be reproduced.

![](https://raw.githubusercontent.com/nickbild/zapper_phone/refs/heads/main/media/zapper_mod_annotated.jpg)

### The transmitter

Here is a schematic for the transmitter. It is quite simple. The audio comes in through a TRRS jack, from a microphone, phone, or whatever else you want to use. That signal is passed through a transformer, which removes any DC components from the signal.

The other side of the transformer is in series with the power supply for the laser. Because it is coupled with the audio input, it modulates the intensity of the laser beam, encoding the audio.

![](https://raw.githubusercontent.com/nickbild/zapper_phone/refs/heads/main/media/transmitter_schematic_crop.jpg)

![](https://raw.githubusercontent.com/nickbild/zapper_phone/refs/heads/main/media/top_sm.jpg)

### Putting it all together

Check out the [video](https://www.youtube.com/watch?v=N6qzJRUytfU) to see a demo of the Zapper Phone in action.

While the audio quality is very good, the Zapper Phone makes a very bad phone. It requires a direct line-of-sight with a laser, and it has to be aligned almost perfectly to work. But I think it's interesting that this old dog could learn a new trick after all these years just the same.

![](https://raw.githubusercontent.com/nickbild/zapper_phone/refs/heads/main/media/zapper_mount_point_sm.jpg)

## Bill of Materials

- 1 x NES Zapper (with the mod mentioned above)
- 1 x Laser Diode — 5mW 650nm Red
- 1 x Audio transformer
- 1 x TRRS breakout board
- 1 x Speaker
- 1 x Adafruit Mono 2.5W Class D Audio Amplifier

## About the Author

[Nick A. Bild, MS](https://nickbild79.firebaseapp.com/#!/)
