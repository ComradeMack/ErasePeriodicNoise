# ErasePeriodicNoise

Step 1: Use fourier transform and visualize magnitude spectrum to notice periodic noise frequency.\
Step 2: Then create bandreject filter to filter out noise frequency positions on magnitude spectrum.\
Step 3: Apply bandreject filter to the fourier transform of noisy picture.\
Step 4: Convert filtered fourier transform (after applying filter) to the spatial domain (real image) by inverse fourier transform.\
Step 5: Save filtered image.





# Requirements

Python 3.8\
numpy==1.19.0\
opencv-python==4.5.3.56\
matplotlib==3.2.2

# Appendix

### fourier transform; 
np.fft.fft2(img)
### magnitude spectrum (for visualizing fourier transform); 
np.log(1+np.abs(FShift))
### inverse fourier transform; 
np.fft.ifft2(f_ishift_br)
### Purpose of shifting after applying fourier transform: 
Easily visualize frequency. Center cluster of shifted fourier transform represents low frquency (detail). Outer cluster represents high frequency (contour).   
