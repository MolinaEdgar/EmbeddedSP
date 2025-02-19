# Investigación sobre Sensores de Corriente (SHUNT, Efecto Hall, Rogowski)

Los **sensores de corriente** son fundamentales en aplicaciones de medición de energía eléctrica, ya sea para monitorear sistemas industriales, gestionar el consumo en equipos electrónicos o controlar dispositivos en automóviles eléctricos. Los tres tipos más comunes son los **sensores Shunt**, los basados en el **efecto Hall** y los **sensores Rogowski**. Cada uno tiene sus particularidades que los hacen adecuados para diferentes aplicaciones.

---

## 1. Sensor de Corriente SHUNT

### Principio de funcionamiento
El **sensor de corriente Shunt** se basa en una resistencia de bajo valor que se coloca en serie con el conductor cuya corriente se desea medir. La corriente que circula a través de esta resistencia genera una caída de voltaje proporcional al valor de la corriente, siguiendo la ley de Ohm:

\[
V = I \cdot R
\]

- **Ventajas**:
  - **Simplicidad**: El principio de medición es muy sencillo, lo que facilita su implementación.
  - **Bajo costo**: Este tipo de sensor es económico en términos de fabricación.
  - **Precisión**: Si la resistencia del shunt está bien calibrada, las mediciones de corriente pueden ser muy precisas.

- **Desventajas**:
  - **Caída de voltaje**: La resistencia introduce una pequeña caída de voltaje en el circuito, lo que puede afectar el rendimiento, especialmente en aplicaciones de alta eficiencia energética.
  - **Limitación en corriente alta**: Para corrientes muy altas, se requieren shunts de baja resistencia, lo cual puede dificultar la medición precisa.
  - **Sensibilidad a la temperatura**: Las resistencias pueden variar con la temperatura, afectando la precisión.

### Aplicaciones comunes:
- **Fuentes de alimentación**: Son ampliamente utilizados en fuentes de alimentación para monitorear la corriente que fluye hacia o desde el sistema.
- **Medición de corriente en vehículos eléctricos**: Para medir el consumo de batería en vehículos eléctricos.
- **Monitoreo de dispositivos electrónicos**: Para verificar el consumo energético en sistemas de bajo voltaje.
![image](https://github.com/user-attachments/assets/7025bd56-a406-47b0-ad6f-240aa57e49d5)

---

## 2. Sensor de Corriente Basado en el Efecto Hall

### Principio de funcionamiento
El **efecto Hall** es un fenómeno que ocurre cuando un conductor o semiconductor lleva corriente en presencia de un campo magnético. En este contexto, el voltaje transversal inducido (llamado voltaje Hall) es proporcional a la intensidad de la corriente y a la magnitud del campo magnético:

\[
V_H = \frac{B \cdot I \cdot l}{n \cdot q \cdot A}
\]

Este voltaje puede medirse y procesarse para obtener el valor de la corriente que pasa por el conductor.

- **Ventajas**:
  - **Aislamiento galvánico**: No hay contacto directo con el conductor, lo que ofrece un alto nivel de seguridad y protección en sistemas de alta tensión.
  - **Medición de corriente alterna y continua**: Los sensores de efecto Hall pueden medir tanto corriente continua (DC) como corriente alterna (AC), lo que los hace muy versátiles.
  - **Alta precisión y fiabilidad**: Los sensores Hall son extremadamente precisos, y su rendimiento no se ve afectado significativamente por la temperatura o la variación de la carga.

- **Desventajas**:
  - **Costo más alto**: Los sensores de efecto Hall son más costosos en comparación con los sensores Shunt debido a la complejidad del principio de funcionamiento.
  - **Sensibilidad al campo magnético externo**: Los sensores Hall pueden ser sensibles a otros campos magnéticos no deseados en el entorno.
  - **Tamaño**: Algunos modelos pueden ser más voluminosos en comparación con los shunt.

### Aplicaciones comunes:
- **Automóviles eléctricos**: Para monitorear el estado de la batería y la eficiencia del motor eléctrico.
- **Sistemas de energía renovable**: Como en paneles solares o generadores eólicos, donde la medición precisa de corriente es clave.
- **Electrodomésticos y sistemas de energía doméstica**: Los medidores de corriente basados en el efecto Hall se utilizan en sistemas de eficiencia energética para controlar y optimizar el consumo eléctrico.
![image](https://github.com/user-attachments/assets/975313b3-f63e-48b3-b879-6acdbcc7daaf)

---

## 3. Sensor de Corriente Rogowski

### Principio de funcionamiento
El **sensor Rogowski** es un transformador de corriente sin núcleo que mide la derivada de la corriente que pasa por un conductor. Está formado por un lazo de cable enrollado alrededor del conductor, y el voltaje inducido en el lazo es proporcional a la tasa de cambio de la corriente:

\[
V_{Rogowski}(t) = \frac{dI(t)}{dt} \cdot k
\]

Donde el **voltaje inducido** es directamente proporcional a la derivada de la corriente respecto al tiempo.

- **Ventajas**:
  - **Alta respuesta en frecuencia**: Son ideales para medir picos de corriente o transitorios, ya que tienen una respuesta muy rápida.
  - **Aislamiento galvánico completo**: Debido a su diseño sin núcleo, ofrecen un aislamiento galvánico total entre el conductor y la medición, lo que es crucial en aplicaciones de alto voltaje.
  - **Flexibilidad y facilidad de instalación**: Son muy fáciles de instalar en conductores existentes sin interrumpir el flujo de corriente, ya que el sensor es flexible y se puede colocar alrededor del conductor sin necesidad de desconectar el sistema.

- **Desventajas**:
  - **Requieren procesamiento adicional**: Los sensores Rogowski no proporcionan directamente la corriente, sino la derivada de la corriente, por lo que la señal debe ser procesada (integrada) para obtener el valor de la corriente.
  - **No aptos para corriente continua**: Estos sensores están diseñados principalmente para medir corriente alterna (AC). La integración de la señal no es adecuada para corriente continua sin modificaciones adicionales.

### Aplicaciones comunes:
- **Sistemas industriales de monitoreo**: Para medir las corrientes de arranque y picos en motores eléctricos, donde se presentan cambios rápidos de corriente.
- **Monitoreo de red eléctrica**: Para medir grandes corrientes de AC en sistemas de distribución de energía sin riesgo de interferir con la operación de la red.
- **Medición de picos de corriente**: En la industria automotriz o sistemas de protección de equipos eléctricos para evitar sobrecargas.
![image](https://github.com/user-attachments/assets/a9ce7f23-470e-4f7f-b3b4-e598233db738)

---

## Comparación entre los tres tipos de sensores

| **Característica**        | **Sensor Shunt**                  | **Sensor Efecto Hall**        | **Sensor Rogowski**            |
|---------------------------|-----------------------------------|-------------------------------|--------------------------------|
| **Método de medición**     | Medición directa de caída de voltaje | Medición del voltaje Hall inducido por el campo magnético | Medición de la tasa de cambio de la corriente |
| **Precisión**              | Alta precisión en corrientes estables | Alta precisión, especialmente en corriente continua | Buena para mediciones en corriente alterna y transitorios |
| **Aislamiento galvánico**  | No                                 | Sí                            | Sí                             |
| **Costo**                  | Bajo                               | Moderado a alto               | Moderado                       |
| **Aplicaciones típicas**   | Medición en fuentes de alimentación, circuitos electrónicos | Medición en automóviles eléctricos, sistemas de energía renovable | Medición de picos de corriente, aplicaciones industriales |
| **Desventajas**            | Introduce caída de voltaje, afectación por temperatura | Sensible a campos magnéticos externos | Requiere procesamiento adicional, no apto para corriente continua |

---

## Conclusiones

La elección de un sensor de corriente depende de las necesidades específicas de la aplicación. Para aplicaciones de bajo costo y medición de corriente continua en condiciones controladas, los **sensores Shunt** son una opción confiable. En aplicaciones que requieren aislamiento galvánico y precisión tanto en corriente continua como alterna, los **sensores basados en el Efecto Hall** son la opción ideal. Finalmente, para aplicaciones que involucren mediciones rápidas de picos de corriente, **los sensores Rogowski** son la mejor alternativa, aunque requieren procesamiento adicional para obtener la corriente real.

En resumen, la elección del sensor adecuado debe considerar no solo el costo y la precisión, sino también la naturaleza de la corriente a medir (AC o DC), las condiciones del entorno, la necesidad de aislamiento galvánico, y la frecuencia de operación.

