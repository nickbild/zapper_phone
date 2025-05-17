# Zapper Phone

*More info coming soon...*

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

## About the Author

[Nick A. Bild, MS](https://nickbild79.firebaseapp.com/#!/)
