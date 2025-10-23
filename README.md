ofdm tv challenge

fs = 48khz

signal starts with a lfm chirp signal.

the chirp signal details:

fs = 48e3;

dt = 1/fs;

pw = 100e-3;

bw = 12e3;

slope = bw/pw;

t = [dt:dt:pw];

t = t - pw/2;

lfm = exp(1i*  pi  *slope  *t.^2);

you will need a matched filter to find this chirp signal in I/Q wave file.




after chirp signal is ofdm tv signal 
this ofdm signal has  480*1024 samples in total

best to reshape these samples into a  480 x 1024 matrix

then take fft of each row in the matrix

then do a fftshift of each row in the matrix

let's call this matrix X

the first line in the image is   angle(  X(2,:)  ./   X(1,:)   )

the second line in the image is   angle(   X(3,:)  ./   X(2,:)   )

and so on

the image contains a amazon gift card.


if image is neg,  then just x by -1  

imagesc( -1 * pic)


