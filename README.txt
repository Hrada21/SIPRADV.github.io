# SIPRADV: Sistema Integrado de Percepción y Respuesta Auditiva para Discapacitados Visuales

## Descripción del Proyecto
El Sistema Integrado de Percepción y Respuesta Auditiva para Discapacitados Visuales (SIPRADV) es un dispositivo diseñado para asistir a personas con discapacidad visual en su movilidad diaria. Utilizando un casco equipado con sensores ultrasónicos y un sistema de retroalimentación auditiva, el dispositivo detecta objetos cercanos y alerta al usuario, mejorando su percepción del entorno y facilitando su independencia y seguridad.

### Contexto Nacional
En la Universidad Tecnológica de Panamá, se desarrolló previamente un dispositivo similar utilizando el sensor ultrasónico HC-SR04 montado en una caja. Sin embargo, este diseño tenía limitaciones de ergonomía y comodidad. El proyecto SIPRADV se creó con el objetivo de mejorar este diseño, proponiendo una solución más compacta y eficiente sin sacrificar la funcionalidad.

### Funcionalidad Principal
- Detección de objetos en la periferia del usuario a través de sensores ultrasónicos.
- Retroalimentación auditiva mediante un reproductor de audio que alerta al usuario cuando se detectan obstáculos cercanos.
- Indicaciones visuales a través de LEDs que proporcionan confirmación adicional del funcionamiento de los sensores.

## Metodología

### Materiales Necesarios:
- 1 Arduino Nano
- 4 Sensores ultrasónicos GY-US42V2 (en modo UART)
- 1 Módulo DFPlayer Mini
- 1 Memoria de 32 GB
- 2 Altavoces mini de 3 watts
- 4 LEDs
- 4 Resistencias de 220Ω para los LEDs
- 1 Batería (incluye cargador)
- Cables de conexión y una placa de pruebas (breadboard)

### Conexión del Arduino Nano:
1. Alimentar el Arduino Nano conectando la batería al pin Vin y GND.
2. Asegurarse de que todos los componentes compartan una conexión a GND.

### Conexión de los Sensores GY-US42V2 (UART Mode):
1. Conectar el pin VCC de cada sensor al pin 5V del Arduino Nano.
2. Conectar el pin GND de cada sensor al pin GND del Arduino Nano.
3. Conectar los pines TX de los sensores al pin RX (D0) del Arduino, y los pines RX de los sensores al pin TX (D1) del Arduino.

### Conexión del DFPlayer Mini:
1. Conectar el pin VCC del DFPlayer Mini al pin 5V del Arduino.
2. Conectar el pin GND al GND del Arduino.
3. Conectar el pin RX del DFPlayer Mini al pin digital D6 del Arduino.

### Conexión de los LEDs:
1. Conectar el ánodo (pata larga) de cada LED a los pines D2, D3, D4 y D5 del Arduino.
2. Conectar una resistencia de 220Ω en serie entre el ánodo y el pin del Arduino.

### Programación del Arduino Nano:
- Escribir el código para recibir datos de los sensores GY-US42V2 y controlar los LEDs según la distancia detectada.
- Añadir lógica para que el DFPlayer Mini reproduzca un sonido cuando un sensor detecte un objeto a menos de 20 cm.
- Encender los LEDs cuando los sensores detecten obstáculos.

### Pruebas del Circuito:
- Verificar que los sensores midan distancias correctamente.
- Probar el funcionamiento de los LEDs y del DFPlayer Mini con los altavoces.
- Ajustar el código y la configuración de los sensores según los resultados de las pruebas.

## Recomendaciones:
- **Evaluación de sensores**: Comparar el rendimiento de los sensores HC-SR04 y GY-US42V2.
- **Uso del modo UART**: Priorizar este modo de comunicación en los sensores GY-US42V2.
- **Fuente de energía**: Seleccionar la fuente de energía más adecuada según el consumo total del proyecto.
- **Optimización del sistema de sonido**: Implementar distintos tonos según la proximidad de los obstáculos.
- **Spacial Audio**: Incluir sonido direccional para una mejor percepción del entorno.
- **Reducción de tamaño y peso**: Diseñar una carcasa más compacta para mayor comodidad.
- **Pruebas en distintos entornos**: Evaluar el dispositivo en diferentes condiciones para asegurar su funcionalidad.
- **Compatibilidad**: Explorar la integración con otros dispositivos de asistencia.

## Referencias
1. Lee, J., Smith, R., & Johnson, T. (2022). *Advances in Ultrasonic Sensor Technology*. Journal of Assistive Technologies.
2. Miller, A. (2019). *Spatial Audio for Accessibility*. Audio Engineering Society.
3. Smith, K., & Johnson, M. (2020). *Technological Innovations in Mobility Assistance for the Visually Impaired*. Disability and Rehabilitation.
4. Tactile, R. (2018). *Exploring Spatial Perception in Individuals with Visual Impairments*. Journal of Visual Impairment & Blindness.
5. Wang, X., & Chen, Y. (2021). *Integrating Sensor and Audio Feedback Systems for Enhanced Navigation*. IEEE Transactions on Human-Machine Systems.
