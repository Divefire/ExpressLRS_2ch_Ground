My attempt at a respin to have 12 bit resolution over 2 channels with low latency for ground racing use. 

Notes to myself: 

ELRS and CRSF being focused for drone and flight use have a lot of paramters and features that won't be used in a ground 2 channel racing envviroment. I've looked at not breaking what's there, but until CRSF add a proper revision of 0x17 https://github.com/tbs-fpv/tbs-crsf-spec/blob/main/crsf.md adding in a less channels for more bit rate won't be possible without breaking everything. 

So this will have to be disasembling ELRS to bare bones, fixing it for 2 channels on PPM, reading 12bits (0-4095), sending it over a protocal (maybe I can adapt what's here, otherwise it will be based on the same hardware, but a simpler protocal) then outputting over PWM on the reciever side at 12bits again. 

It might well be simpler to start from scratch to do this, however. 
