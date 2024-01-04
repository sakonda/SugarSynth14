"msp Granular Synthesis" is a patch that performs granular synthesis using only basic Max/MSP objects. It has been a favorite of many Max users because of the simplicity of the algorithm, the richness of the effect, and the ease of extension. Although it is classical in audio quality and functionality compared to other recent granular synthesizers, I upload it to Github because I still sometimes get contacted by people inquiring about how to get it.

"msp Granular Synthesis" is a simple 8-voice granular synthesis patch. It allows independent control of playback speed and pitch for audio loaded (or recorded) into a buffer. It also implements several special control methods that take advantage of the characteristics of grains (small sound fragments). This allows you to customize the playback pitch, playback position, and stereo pan for each grain, as well as manually scrub the audio.

The unique point of my algorithm is that when looping small sound fragments from the audio in the buffer, it synchronizes the envelope of the window function (cosine by default) so that the noise generated at the loop point is inaudible. Furthermore, by synchronizing this envelope with the sample and hold, the noise generated when changing any parameter is also not heard. Check out what's inside the sub-patch.

"SugarSynth" uses the same algorithm, but extends it with a poly~ object that allows the number of grains to be freely changed. We have also made numerous improvements to the user interface to make it easier for the player to control.
