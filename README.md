Smooth-Panorama
===============

This is a set of abstraction that pans an audio signal smoothly between any number of speakers.
The speakers are expected to be setup in a circle with equal angles between them.

The panorama *position* is controlled with an audio signal, where 0=1=2=...=0°=360° etc. 
The Algorithm uses both amplitude and timebased panning. The position defines two bell curves. One is used for the level of signal sent to speakers and is 1 at *the position* and 0 180° from it. the other is used for a delay and is 0 at *the position* and 1x[delayTime] 180° from it.

[pancontrol] offers three controls:
- (maximum) delay time
- width of delay bell
- width of amplitude bell

It is advisable to have narrower bell curves for more speakers (smaller angles).
the combination of smoothly moving signals and (thus changing delay times) produces a doppler-like frequency modulation.


(c) 2011-2017 Dominik Schmidt-Philipp