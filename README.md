# 🔒 Cerradura electrónica de 6 dígitos con GAL G22V10

Proyecto académico desarrollado para implementar una **cerradura digital programable** de 6 dígitos utilizando una **GAL G22V10**, microinterruptores, una barra de LEDs y un pulsador.

---

## ⚙️ Descripción general

El sistema simula una cerradura digital en la que el usuario introduce una combinación de 6 dígitos mediante interruptores (BCD).  
Cuando la secuencia correcta se introduce y se pulsa el botón de validación, el sistema activa la salida (LED de apertura).

La lógica se ha implementado mediante una **máquina de estados** programada en lenguaje **WinCUPL** y verificada mediante simulación en **Proteus**.

---

## 🧩 Componentes principales

| Componente | Función |
|-------------|----------|
| GAL G22V10 | Dispositivo lógico programable donde se implementa la lógica de la cerradura |
| 6 microinterruptores | Introducción del código BCD (1 dígito por interruptor) |
| 1 pulsador | Confirmación de la secuencia introducida |
| Barra de LEDs | Indicación de estado y apertura |
| Resistencias | Limitación de corriente y pull-up |
| Fuente 5V | Alimentación del circuito |

---

## 🧠 Funcionamiento

1. El usuario introduce una **secuencia de 6 dígitos** mediante los interruptores.  
2. Cada pulsación del botón actualiza el estado interno de la máquina.  
3. Si los 6 dígitos coinciden con la clave programada, se activa el **LED de apertura**.  
4. Si hay error en la secuencia, el sistema vuelve al estado inicial.

---

## 🧾 Archivos incluidos

- `/src/` → Código fuente WinCUPL (`.pld`)
- `/proteus/` → Esquema y simulación (`.dsn`)
- `/docs/` → Documentación y diagrama de estados (`.pdf`)
- `/images/` → Fotos o capturas del circuito

---

## 🧮 Máquina de estados

La GAL implementa una máquina de tipo **Moore**, con estados que representan el progreso de la introducción correcta del código.  
Ejemplo:  
`S0 → S1 → S2 → S3 → S4 → S5 → S6 (open)`  
Cada transición ocurre tras un pulso del botón si el dígito es correcto.

---

## 🧰 Herramientas utilizadas

- **WinCUPL** → Programación de la GAL  
- **Proteus** → Simulación del circuito lógico  
- **Multisim / TinkerCAD** → Alternativas para comprobaciones simples  
- **Excel / Draw.io** → Diseño de tabla de verdad y máquina de estados

---

## 🚀 Resultados

- Funcionamiento correcto del sistema tras validación de secuencia.  
- Diseño modular fácilmente adaptable a contraseñas de distinta longitud.  
- Simulación funcional y programable en hardware real.

---

## 📸 Ejemplo visual

*(Incluye aquí una imagen del circuito o la simulación)*  
```markdown
![Simulación en Proteus](images/proteus-simulation.png)
