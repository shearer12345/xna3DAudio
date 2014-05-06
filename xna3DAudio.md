#3D Audio in XNA

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

- time differences between ears
  - sound from the right side reaches the right ear earlier than the left ear
  - the auditory system evaluates interaural time differences from:
    - phase delays at low frequencies
    - group delays at high frequencies
- level differences between ears
- spectral (frequency) information
- correlation analysis
- pattern matching

(http://en.wikipedia.org/wiki/Sound_localization)


##Head-related transfer function

- the way sounds arrive at the ear (outer end of auditory canal) is non-trivial
- it depends on the shape of the ears as well as the shape of the head and torso
- these can be simulated to varying degrees

http://en.wikipedia.org/wiki/Head-related_transfer_function



##Other acoustic effects

- size of the space
  - reverberation delays
- kind of surfaces in the space (hard, soft)
  - how fast reverb attenuates
- sound refracts around corners
- sound bounces off objects
  - can lead to audio focusing (e.g. acoustic mirrors)
    <img src="http://upload.wikimedia.org/wikipedia/commons/9/94/WW1AcousticMirrorKilnsea%28PaulGlazzard%29Jan2007.jpg" alt="acoustic mirror" height="200">
- NOTE: being **very** general, simplistic here



##What (physical) equipment is needed?

- headphones - speakers collocated with ears so can provide some very power effects (try the previous examples with headphones)

<img src="http://upload.wikimedia.org/wikipedia/commons/thumb/f/f3/4_adapter.jpg/800px-4_adapter.jpg" alt="headphones" height="400">


- multiple speakers - used together to simulate sound from any locations. Normal surround sound options include:
  - 2.1 (two channels of medium/high frequency (which give location), and one subwoofer (low frequency, which humans can't locate))
  - 4.1 (front left, front right, back left, back right, sub) - not very common
  - 5.1 (centre, front left, front right, back left, back right, sub)
    <img src="http://upload.wikimedia.org/wikipedia/commons/c/cc/5_1_channels_%28surround_sound%29_label.svg" alt="5.1 surround sound" height="200"> <img src="http://www.richersounds.com/images/tips/surroundSetup.gif" alt="5.1 surround sound" height="200">
  - 7.1 (centre, front left, front right, left, right, back left, back right, sub)



##What libraries exist (for real-time games)

- built into XNA
- OpenAL (which isn't open in the way OpenGL is, but ...)
  - OpenAL soft most useful implementation for Desktop (http://kcat.strangesoft.net/openal.html)
  - OpenAL binding in OpenTK (C# library for OpenGL etc) (http://www.opentk.com/doc/audio)
  - OpenAL (soft) also ported to Android (https://github.com/apportable/openal-soft)
- OpenSL ES (on mobile platforms)
- FMOD (commercial, free for indie), used in Forza 5 (http://fmod.org)


##What can those libraries do?

- only a **small** subset of auralization techniques:
  - time differences between ears
  - level differences between ears
  - Head-related transfer function if you write a function for it
- in general, nothing else
  - but you can manually setup reverb etc to simulate spaces, but doing this properly, dynamically, in real-time is an open research problem


##Research

- http://gamma.cs.unc.edu/PrecompWaveSim/
  - <iframe width="420" height="315" src="//www.youtube.com/embed/MQt1jtDBNK4" frameborder="0" allowfullscreen></iframe>
  - <iframe width="420" height="315" src="//www.youtube.com/embed/FDL39J-i0yQ" frameborder="0" allowfullscreen></iframe>
    - around 2:20



##Hands on

- there are a variety of XNA audio tutorials, I recommended the following:
  - MSDN
    - http://msdn.microsoft.com/en-us/library/dd940200.aspx
    - http://msdn.microsoft.com/en-us/library/bb447686.aspx
  - RB Whitaker's Wiki - http://rbwhitaker.wikidot.com/audio-tutorials
