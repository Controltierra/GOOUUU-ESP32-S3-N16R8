ESP32-S3 OLED + DHT11 + WS2812 Project

Descripción

Este proyecto está diseñado para la placa Goouuu ESP32-S3 N16R8 junto con su placa de expansión, que integra:

Sensor de temperatura y humedad DHT11.

Pantalla OLED 0.96" (128x64 px) controlada vía I2C.

Un LED WS2812 RGB integrado en el ESP32-S3 (GPIO48).

Se muestran los datos de temperatura y humedad de forma alterna en la pantalla OLED, acompañados por un icono ilustrativo (termómetro o gota de agua), mientras el LED RGB cambia suavemente de color en función de la temperatura.

Hardware Utilizado

Placa Goouuu ESP32-S3 N16R8

Módulo de expansión compatible Goouuu

Sensor DHT11 (conectado a GPIO2)

Pantalla OLED 0.96" I2C (SDA: GPIO42, SCL: GPIO41)

LED WS2812 RGB (integrado, conectado a GPIO48)

Conexiones

Componente

GPIO

Función

DHT11

GPIO2

Entrada digital

OLED SDA

GPIO42

I2C SDA

OLED SCL

GPIO41

I2C SCL

WS2812 LED

GPIO48

Salida digital RGB

Librerías Necesarias

Instalables desde el Gestor de Librerías de Arduino IDE:

Adafruit GFX Library (>= 1.11.5)

Adafruit SSD1306 (>= 2.5.7)

FastLED (>= 3.5.0)

DHT sensor library

Wire (incluida en Arduino IDE)

Características del Software

Lectura de temperatura y humedad cada 2 segundos.

Visualización alterna de temperatura y humedad en pantalla OLED:

Temperatura: icono de termómetro y valor en grados Celsius (°C).

Humedad: icono de gota de agua y porcentaje (%).

Transición de colores en el LED WS2812 según la temperatura:

<22°C: Azul

22-24°C: Fundido Azul → Verde

24-26°C: Fundido Verde → Rojo



26°C: Rojo

Texto de gran tamaño usando la fuente FreeSansBold18pt7b para mejorar la legibilidad.

Configuración en Arduino IDE

Placa: ESP32S3 Dev Module

Velocidad de carga: 921600 baudios (o 115200 si hay problemas)

CPU Frequency: 240 MHz (WiFi)

USB CDC On Boot: Enabled

PSRAM: Enabled

Partition Scheme: Default 4MB with spiffs

Notas

El proyecto está optimizado para pantallas OLED de pequeño formato (128x64 px).

El ESP32-S3 permite realizar fácilmente futuros proyectos de AIoT gracias a su soporte SIMD y TensorFlow Lite Micro.

El LED WS2812 puede ser utilizado también para indicar estados críticos, alarmas, o animaciones personalizadas.

Mejoras Futuras

Animaciones suaves en la transición de datos OLED (scroll lateral, fade-in/fade-out).

Alarmas visuales en el LED si se superan umbrales críticos.

Incorporación de RTC para mostrar fecha y hora.

Autor

Proyecto creado y adaptado para la placa Goouuu ESP32-S3 N16R8.
