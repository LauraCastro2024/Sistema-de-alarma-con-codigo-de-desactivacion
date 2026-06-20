# Sistema de Alarma con Código de Desactivación

Proyecto de robótica desarrollado con la placa **micro:bit** y el entorno **MakeCode**. Simula el sistema de seguridad de una vivienda: detecta una posible intrusión a través de un cambio brusco en el nivel de luz y permite desactivar la alarma mediante un código de seguridad por secuencia de botones (**A - B - A**).

**Ficha 3 · Robótica** — Integrantes: **Laura Castro** · **Analía Sáenz**
3.º año Informática · Docente: Domingo Pérez

## Cómo funciona

| Acción | Cómo |
|---|---|
| Armar la alarma | Botón **Armar** o tecla **A** |
| Simular una intrusión | Botón **Simular intrusión** o tecla **I** |
| Ingresar el código | Botones **A** y **B** (secuencia correcta: A → B → A) |
| Reiniciar | Botón **Reiniciar** o tecla **Esc** |

Si ingresás un botón fuera de orden, el conteo se reinicia: es la misma lógica de seguridad que el sistema real.

## Cómo funciona el sistema

1. **Armar** — Al presionar A, la micro:bit guarda el nivel de luz actual (`luzInicial`) y muestra el ícono de una casa.
2. **Monitoreo** — Un bucle revisa el sensor de luz de forma continua. Si la luz varía más de 50 unidades respecto al valor guardado, se dispara la alarma.
3. **Intrusión** — El buzzer suena a 988 Hz, los LEDs parpadean con una calavera y el servomotor gira a 90° simulando el cierre de la puerta.
4. **Desactivación** — Se debe ingresar la secuencia A → B → A. La variable `pasoCodigo` controla el avance; si es correcta, el servo vuelve a 0° y la matriz muestra un tilde.

## 🧩 Componentes

- Placa **micro:bit** (cerebro del sistema)
- **Sensor de luz** (matriz de LEDs usada como fotodiodo) — integrado
- **Botones A y B** — integrados
- **Matriz de 5×5 LEDs** (salida visual) — integrada
- **Servomotor** en el pin P0 (puerta) — externo
- **Buzzer** (alarma sonora) — externo
- Protoboard, cables, resistencia y batería

## Conceptos que se trabajan

Variables de estado · estructuras condicionales · bucles · lógica de secuencia · máquinas de estado · razonamiento causa-efecto · depuración.

## 🔗 Enlaces

- **Proyecto en MakeCode:** https://makecode.microbit.org/_KCvAKrbJmTVX

