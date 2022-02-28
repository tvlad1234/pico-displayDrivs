ST7789 driver, based on [Adafruit-ST7735-Library](https://github.com/adafruit/Adafruit-ST7735-Library)

## Usage
Add *ST7789* into CMakeLists.txt, in `target_link_libraries`

### Pin mapping
The display uses the default SPI peripheral of the RP2040, on the default pins. \
The CS, RST and DC pins can be changed in *st7789.h*

### Functions:
`LCD_initDisplay();` initializes the GPIO, SPI interface and display driver\
`LCD_setRotation(uint8_t m);` sets the rotation \
`LCD_WriteBitmap(uint16_t x, uint16_t y, uint16_t w, uint16_t h, uint16_t *bitmap);` writes a bitmap to the screen

### DMA usage
DMA  usage is disabled by default, but can be enabled by uncommenting `#define USE_DMA 1` in *st7735.h*
