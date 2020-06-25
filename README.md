![Captura de pantalla 2020-06-25 13 20 34](https://user-images.githubusercontent.com/67433384/85776977-d164d100-b6e6-11ea-840e-72f4ee861261.png)

## Programa

** Para compilar el programa  es necesario intalar las siguientes librerias TFT desde el archivo ZIP **

Descarga la libreria e instala dentro de  Arduino IDE (Sketch -> Include library -> Add .ZIP library)

Bodmer TFT_ST7735 v0.17

Estas librerias pueden ser intsaladas desde el  Arduino IDE  (Sketch -> Include library -> Manage libraries...)

Adafruit_GFX_Library v1.8.3

Adafruit_BusIO v1.3.0

Modifica la libreria  TFT_ST7735 para que pueda caber dentro de la memoria de Arduino Nano.

modify ${HOME}/Arduino/libraries/TFT_ST7735/User_Setup.h

Uncoment las siguientes lineas
```
#define TAB_COLOUR INITR_BLACKTAB
```
Comenta cualquier otra linea  TAB_COLOUR .
```
//#define TAB_COLOUR INITB
//#define TAB_COLOUR INITR_GREENTAB
//#define TAB_COLOUR INITR_REDTAB
#define TAB_COLOUR INITR_BLACKTAB
//#define TAB_COLOUR INITR_GREENTAB
```
Solo debe quedar  activa la  Fuente 1 y 2 , de lo contrario no cabra dentro de la memoria de el Arduino Nano 
```
#define LOAD_GLCD   // Font 1. Original Adafruit 8 pixel font needs ~1820 bytes in FLASH
#define LOAD_FONT2  // Font 2. Small 16 pixel high font, needs ~3534 bytes in FLASH, 96 characters
//#define LOAD_FONT4  // Font 4. Medium 26 pixel high font, needs ~5848 bytes in FLASH, 96 characters
//#define LOAD_FONT6  // Font 6. Large 48 pixel font, needs ~2666 bytes in FLASH, only characters 1234567890:-.apm
//#define LOAD_FONT7  // Font 7. 7 segment 48 pixel font, needs ~2438 bytes in FLASH, only characters 1234567890:.
//#define LOAD_FONT8  // Font 8. Large 75 pixel font needs ~3256 bytes in FLASH, only characters 1234567890:-.
```
