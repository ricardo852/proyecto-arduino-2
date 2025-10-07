# 🌡️ Monitor de Temperatura con Arduino y Pantalla LCD

Este proyecto mide la **temperatura ambiente** usando un sensor **TMP36** y muestra el valor en una **pantalla LCD 16x2**.  
Dependiendo del valor detectado, controla un **LED** y un **motor de corriente continua** para simular un sistema automático de climatización.

---

## 🧠 Descripción del funcionamiento

El sistema lee la temperatura a través del sensor **TMP36**, convierte la señal analógica a grados Celsius y la muestra en la pantalla LCD.  
Luego, realiza validaciones para activar o desactivar los actuadores según el nivel térmico:

- 🌬️ **Clima frío (≤ 10 °C):** el **LED parpadea** y el **motor se apaga**.  
- 🌤️ **Clima normal (11 °C a 25 °C):** el **LED** y el **motor permanecen apagados**.  
- 🔥 **Clima cálido (≥ 26 °C):** el **LED** y el **motor se encienden** de forma continua.

De esta manera, el sistema simula un **control automático de temperatura**.

---

## 🧩 Componentes utilizados
___________________________________________________
| Nombre | Cantidad |         Componente          |
|--------|----------|-----------------------------|
| U1     |     1    | Arduino Uno R3              |
| M1     |     1    | Motor de corriente continua |
| R4     |     1    | Resistencia de 250 Ω        |
| D4     |     1    | Diodo                       |
| R5     |     1    | Resistencia de 1 kΩ         |
| U2     |     1    | Pantalla LCD de 16 x 2      |
| Rpot1  |     1    | Potenciómetro de 250 kΩ     |
| D1     |     1    | LED rojo                    |
| U3     |     1    | Sensor de temperatura TMP36 |

---

## ⚙️ Conexiones principales

- **TMP36:**  
  - Pin 1 → 5V  
  - Pin 2 → A0  
  - Pin 3 → GND  

- **Pantalla LCD (16x2):**  
  RS → 12  
  E → 11  
  D4 → 5  
  D5 → 4  
  D6 → 3  
  D7 → 2  
  V0 → Potenciómetro (250 kΩ)

- **LED rojo:**  
  Ánodo (+) → Pin 13 (con resistencia de 250 Ω)  
  Cátodo (–) → GND  

- **Motor DC:**  
  Positivo → Pin 9 (a través de diodo de protección)  
  Negativo → GND  
