---
layout : page  
subtitle : Ableton Live et Max4 Live

---
# Composition et Showcontrol

## Ableton Live ?

* clip launcher (changer de mode avec la touche TAB)
* mode timeline
* Automation d'un segment de temps / automation d'un clip
* Midi Mapping / Mapping de touches
* Outil de composition
* Outil d'échantillonnage

## Max 4 Live
* permet à MAX de vivre dans Ableton LIVE
* 3 types de Device M4L
  * Audio Effect (Audio In,  Audio Out)
  * Midi Instrument (Midi in, Audio Out)
  * Midi Effect (Midi in,  Midi Out)
* 32 bits vs 64 bits : (architecture MAX et LIVE)


## Signaux

#### Midi
[Intro au protocole Midi (PDF)](http://www.midi.org/aboutmidi/intromidi.pdf)

* notes
  * noteon/noteoff
  * pitch/vélocité
  * durée ...
  * midichannel
  * [patchs/sortieMidi.maxpat](../patchs/sortieMidi.maxpat)
* control change (CC)
  * 0 -127 (7 bits)
    * CTLIN / CTLOUT
  * 0 - 16383 (14 bits)
    * [patches/14bitMidiCC.maxpat](../patches/14bitMidiCC.maxpat)
    * [forum Max](https://cycling74.com/forums/topic/14bit-cc-to-ableton/)
    * xbendin / xbendout (14 bits aussi)


#### OSC (open sound control)
* adresse / port
  * UDPsend pour envoyer
  * UDPreceive pour recevoir   

* Interapplication
  * (localHost:port soit 127.0.0.1:9999 )
  * interordinateur
    * unicast = abc.def.uvw.xyz:port
    * broadcast= abc.def.uvw.255:port

* tuio (est un protocole de formatage OSC)
        * [http://www.tuio.org](http://www.tuio.org)
        * [http://www.tuio.org/?software](http://www.tuio.org/?software)

#### Audio ...
* exemple de l'envelope follower
  * [patches/EnvelopeFollower.amxd](../patches/EnvelopeFollower.amxd)
* timecode (smpte~)

#### Proposition d'exercices :

* Créer une composition midi qui influence des paramètres visibles dans Max ( par exemple un slider )
  * l'objectif ici est de maitriser le protocole midi Interapplication
* Créer un patch avec un générateur de hasard qui envoie des notes midi vers ableton Live
  * Même objectif que précédant,  mais dans le sens contraire
* Créer un patch avec un générateur de hasard qui envoie des paramètres de contrôle (CC) à ableton live et qui affecte les paramètres d'un synthétiseur
  * L'objectif est de ce familiariser avec les principes du mapping dans live,  ainsi qu'aux entrées midi de contrôle.
* Créer un instrument M4L : soit un Instrument dans live qui reçoit  des notes et qui produit des sons
* Créer un effet audio M4L : soit un processeur d'effet qui reçoit de l'audio et qui sort de l'audio traité (bonus s'il a un wet/dry)
* Créer un effet midi M4l : soit un effet midi qui altère une composition midi (un arpégiateur par exemple)  


##### Pour aller plus loin
* Max for live
  * [m4l dans le manuel ](https://www.ableton.com/en/manual/max-for-live/)
  * [communauté M4L](http://maxforlive.com)


* Synchro MIDI  
    * [MIDI_timecode](https://en.wikipedia.org/wiki/MIDI_timecode)
    * [MIDI_beatclock](https://en.wikipedia.org/wiki/MIDI_beat_clock)
    * rtin

* Synchro audio
  * Générateur (master)
    *  [smpte~](https://cycling74.com/toolbox/smpte/#.VhKbH7TY7Qc)
  * écouteur (slave)

* Rewired
  * slave
  * master
  * voir : [https://www.ableton.com/en/manual/synchronization-and-rewire/](https://www.ableton.com/en/manual/synchronization-and-rewire/)
  *


Protocole de contrôle de lumière  

* DMX
  * Enttec-USB
  * [MAX-USB_DMX](https://github.com/gllmAR/MAX-USB_DMX)
* artnet
  * [the impersonal Stereo](http://www.theimpersonalstereo.com/software/maxmspjitter/)
  *
Pour aller plus loin

* Show Networks and Control Systems:
de  John Huntington (juillet 2012) [http://controlgeek.net/bookinfo/](http://controlgeek.net/bookinfo/)


* Richmond sound design [http://www.richmondsounddesign.com/bibliographies-articles.html](http://www.richmondsounddesign.com/bibliographies-articles.html)


http://www.synthgear.com/2009/software/audio-to-midi
