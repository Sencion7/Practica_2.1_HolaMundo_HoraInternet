# Practica_2.1
# 2.1.1 Practica De inicio es la básico de Desplegar algo en pantalla
# Diagrama del circuito
![image](https://github.com/Sencion7/Practica_2.1_HolaMundo_HoraInternet/assets/80359457/ff92581b-3f85-45d3-95d5-173792de2874)

## Circuito en funcionamiento
![](Evidencia_Practica_2.1.1.jpg)
![](Evidencia_Practicaa_2.1.1.jpg)

# CÓDIGO
```python
from machine import Pin, I2C
from ssd1306 import SSD1306_I2C
import framebuf

i2c = I2C(0, sda=Pin(0), scl=Pin(1), freq=400000)
oled = SSD1306_I2C(128, 64, i2c)

# Crea un buffer de imagen en blanco
buf = bytearray(b'\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00'
               b'\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00'
               b'\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00'
               b'\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00'
               b'\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00'
               b'\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00'
               b'\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00'
               b'\x00\x00\x00\x00\x00\x00\x00\x00')

# Crea un frame buffer para la imagen
fb = framebuf.FrameBuffer(buf, 128, 64, framebuf.MONO_HLSB)

# Limpia la pantalla
oled.fill(0)
oled.show()

# Establece el tamaño de fuente y la posición de inicio
font_size = 1
x = 0
y = 0

# Dibuja "Hola, mundo" en la pantalla
oled.text("Hola, mundo", x, y, 1)

# Muestra la pantalla con el mensaje
oled.show()
```
# Resultados
![](Evidencia_Practicaaa_2.1.1.jpg)

# 2.1.2  Desplegar la hora de Internet en la Pico usando su Wifi integrada para que interrogue un servidor NTP Time Server, en el OLED DIsplay

# Diagrama del circuito
![image](https://github.com/Sencion7/Practica_2.1_HolaMundo_HoraInternet/assets/80359457/ff92581b-3f85-45d3-95d5-173792de2874)

## Circuito en funcionamiento
(Pendiente de elaborar)

# CÓDIGO
```python
from machine import Pin, I2C
from ssd1306 import SSD1306_I2C
import framebuf

i2c = I2C(0, sda=Pin(0), scl=Pin(1), freq=400000)
oled = SSD1306_I2C(128, 64, i2c)

# Crea un buffer de imagen en blanco
buf = bytearray(b'\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00'
               b'\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00'
               b'\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00'
               b'\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00'
               b'\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00'
               b'\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00'
               b'\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00'
               b'\x00\x00\x00\x00\x00\x00\x00\x00')

# Crea un frame buffer para la imagen
fb = framebuf.FrameBuffer(buf, 128, 64, framebuf.MONO_HLSB)

# Limpia la pantalla
oled.fill(0)
oled.show()

# Establece el tamaño de fuente y la posición de inicio
font_size = 1
x = 0
y = 0

# Dibuja "Hola, mundo" en la pantalla
oled.text("Hola, mundo", x, y, 1)

# Muestra la pantalla con el mensaje
oled.show()
```
# Resultados
(Pendiente de elaborar)
