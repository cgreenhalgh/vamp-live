# VAMP notes

Chris Greenhalgh, 2015-11-05

ubuntu
```
sudo apt-get install libsndfile1-dev
```

get [The main SDK](https://code.soundsoftware.ac.uk/attachments/download/1520/vamp-plugin-sdk-2.6.tar.gz).
Extract.

See `build/README.xxx`, e.g. `linux`

```
./configure
make
make install
```

e.g. [03 Heathery Breeze.mp3](http://www.cs.nott.ac.uk/~pszcmg/Music/Happy%20by%20Da%20Dog/03%20Heathery%20Breeze.mp3)

e.g. [Silvet note transcription](http://www.cs.nott.ac.uk/~pszcmg/Music/Happy%20by%20Da%20Dog/03%20Heathery%20Breeze.mp3)

```
vamp-plugin-sdk-2.6/host/vamp-simple-host -L
vamp-plugin-sdk-2.6/host/vamp-simple-host silvet:silvet 03\ Heathery\ Breeze.wav 2 -p mode 0
```

Note want plugin silvet:silvet, but parameter 'mode' value 0 (live), rather than default (1, intensive).
Output 2, onoffset.


																																	
