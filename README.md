# MC_Inalambrico
Este proyecto contiene lo necesario para implementar un monitor cardíaco inálambrico para Ratas

**Versión prototipo 1:**

- 1) Adquisición: (módulo AD8232, amplificador de la señal del corazón)

- 2) Procesamiento: Binarisa la señal del corazón y la empaqueta para la transmisión

- 3) Transmisión: (Xbee). 


**Mejoras:**

- 1) Procesamiento: Soluciones que pueden resumir en un encapsulado la adquisición y la transmisión.

- 2) Transmisión: Para la señal del corazón los 256Kbytes de la xbee funcionan, pero como la señal del corazón de la rata es más rápida entonces hay que muestrear más rápido y transmitir más cantidad de datos entonces el ancho de banda está al límite y se comienza a quedar corto entonces no es muy confiable, adicionalmente la xbee es una tarjeta de más que está ocupando espacio (vertical)


**Solucion**

Reemplazar procesamiento y transmisión por una ESP32, cambiar xbee a bluetooth ya que el ancho de banda es de 2MHz de esa forma se resume a una sola tarjeta la adquisición y la transmisión.
