# TLE9012_Lib_STM32
Port of the TLE9012 Arduino Library in Plain C for STM32 https://github.com/MaxMax-embedded/TLE9012_Arduino_Lib
The port was made a bit quick and dirty so there might be nicer ways so if you want to contribute feel free to raise an issue or make a PR

As a result of porting from C++ to C the tle9012.function() notation can not be used and is replaces with tle9012_function(). The devices variable and errorcallbacks are exported as external variables and therefore accessible in the rest of the program.

To use this library you need to configure the following things: 
- Include the TLE9012_Lib Folder as a Source Folder in you Cube MX Project
- A USART Interface with 2Mbit and MSB First. DMA and Interupts need to be activated in non-cyclic mode. 
- A Timer configured with Enabled interrupts and a prescaler configured for 1us per Count

See the Arduino Library for examples and information about the physical wirering with TLE9015 or TLE9012 
