#3D Audio in XNA


##Structure

[http://shearer12345.github.io/xna3DAudio/](http://shearer12345.github.io/xna3DAudio/)

- source [https://github.com/shearer12345/xna3DAudio](https://github.com/shearer12345/xna3DAudio)



##What is 3D audio anyway?
![3d Audio image, from http://q2s.ntnu.no/_media/projects/3d_audio/3d-audio.jpg
](assets/3d-audio.jpg)

- Audio (sound) which gives the listener cues about the 3D world, including:
  - location of audio sources
  - size of the space
  - kind of surfaces in the space (hard, soft)


##Also known as:

- positional audio
- spatialized audio
- surround sound



##Some examples

###Doppler Effect
<audio controls>
  <source src="assets/Speeding-car-horn_doppler_effect_sample.ogg" type="audio/ogg">
  Your browser does not support the audio element.
</audio>

###Virtual Barbershop and Haircut
<iframe width="420" height="315" src="//www.youtube.com/embed/IUDTlvagjJA" frameborder="0" allowfullscreen></iframe>



##Describing the location of sound

- we usually describe sound locations from the first person perspective and talk about the:
  - azimuth (horizontal angle)
  - elevation (vertical angle)
  - distance (how far)
  - velocity (how fast)


##How do we (humans) determine the direction/location of sound?

Our auditory systems use several cues for sound source localization, including:

- time differences between ears (gives azimuth)
- level differences between ears
- spectral (frequency) information
- timing analysis
- correlation analysis
- pattern matching

(http://en.wikipedia.org/wiki/Sound_localization)


##Head-related transfer function

- the way sounds arrive at the ear (outer end of auditory canal) is non-trivial
- it depends on the shape of the ears as well as the shape of the head and torso
- these can be simulated to varying degrees

http://en.wikipedia.org/wiki/Head-related_transfer_function



##What (physical) equipment is needed?

- headphones - speakers collocated with ears so can provide some very power effects (try the previous examples with headphones)

<img src="http://upload.wikimedia.org/wikipedia/commons/thumb/f/f3/4_adapter.jpg/800px-4_adapter.jpg" alt="headphones" height="400">


- multiple speakers - used together to simulate sound from any locations. Normal surround sound options include:
  - 2.1 (two channels of medium/high frequency (which give location), and one subwoofer (low frequency, which humans can't locate))
  - 4.1 (front left, front right, back left, back right, sub) - not very common
  - 5.1 (centre, front left, front right, back left, back right, sub)
    <img src="http://upload.wikimedia.org/wikipedia/commons/c/cc/5_1_channels_%28surround_sound%29_label.svg" alt="5.1 surround sound" height="200">
  - 7.1 (centre, front left, front right, left, right, back left, back right, sub)


##What libraries exist (for real-time games)

- mainly OpenAL (which isn't open in the way OpenGL is, but ...)
- 
##Further / alternative sources

- most of the demo code etc is from RB Whitaker's Wiki - http://rbwhitaker.wikidot.com/audio-tutorials
