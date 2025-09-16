My attempt at a respin to have 12 bit resolution over 2 channels with low latency for ground racing use. 

Notes to myself: 

ELRS and CRSF being focused for drone and flight use have a lot of paramters and features that won't be used in a ground 2 channel racing envviroment. So rather than break with what's there, I'll see if it's possible to add a specific 2ch mode into elrs that uses a simpler crsf packet. Idealy I'd use https://github.com/tbs-fpv/tbs-crsf-spec/blob/main/crsf.md 0x17 to define 12bit channels, but revisions are in progress. Though given the simplicity of what I'm doing a rewrite when needed wouldn't be too bad. 

So, I'll try and use 0x17 to set the 2 channels. 

The next stage is reading the PPM at 12bits (0-4096) and then on the recivever side PWM values at 12bit. 

With those three things done I should be left with a 12bit, low latency, 2 channel ground mode. 
