# arduino-library-camera
Arduino Camera Library for stm32 platform 

# CAMERA API definition _(Proposal)_

**Camera.begin(_resolution_):** Initialize the Camera module 
* _int **resolution**_: set the resolution of the acquired image. 

**Camera.readRegister(_address_):** Read the value contained in a given register  
* _int **register**_: contain the memory address of the register to be read.

**Camera.writeRegister(address, value):** write data into a given register
* _int **address**_: contain the memory address of the register to be write
* _int **value**_: contain the value to be written into the regiter

**Camera.setMode(mode):** Set the image output format
* _**mode**_: 
  * _jpg_: set the output format to jpeg
  * _bmp_: set the output format to bitmap

**Camera.getBufferLen(len):** get the length of image buffer
* _int **len**_: contain the length of buffer

**Camera.setBufferLen(len):** set the length of image buffer
* _int **len**_: contain the desired length of buffer 

**Camera.readBuffer(buf):** read the buffer containing the image and transfer data to buf
* _int **buf**_: contain the image data

**Camera.flushBuffer():** empty the camera buffer

**Camera.start():** this start the picture acquisition 

**Camera.getVsync():** this value contain _“true”_  if VSYNC is ok or _"false"_ otherwise

**Camera.getHsync():** this value contain _“true”_ if HSYNC is ok or _"false"_ otherwise

**Camera.newFrame():** this value is _“true”_ if a new frame is ready to transfer from camera to MCU or _"false"_ otherwise
