# Taller de arquitecturas — Casos (Semana 2)

Cada equipo trabaja **un solo caso** (asignación rotativa: equipo 1 →
caso 1, equipo 2 → caso 2, equipo 3 → caso 3; si hay más de 3 equipos,
se repite el ciclo). Los tres casos se discuten en plenaria al cierre.

---

## Caso 1 · Fraude bancario

Un banco necesita **detectar transacciones fraudulentas en tiempo real**.

- Decisión de bloqueo/aprobación en **menos de 300 ms**.
- Volumen pico: **80.000 transacciones por segundo**.
- Requiere **conciliación contable exacta** a fin de día (los números
  deben cuadrar centavo a centavo con el core bancario).
- Regulación estricta: trazabilidad completa de cada decisión.

**Pregunta guía:** ¿qué eje (latencia, throughput, consistencia, costo)
manda la decisión de arquitectura, y qué patrón lo resuelve sin
sacrificar la conciliación?

---

## Caso 2 · Analítica retail

Una cadena de **400 tiendas + canal e-commerce** quiere centralizar su
analítica de ventas.

- Los tableros de gerencia se refrescan **cada hora** (no en tiempo real).
- Necesitan **histórico de 5 años, re-procesable** ante cambios de
  definición de métricas (p. ej., redefinir qué cuenta como "venta neta").
- **Presupuesto ajustado**: no pueden mantener dos equipos de ingeniería
  (uno para batch, otro para streaming).

**Pregunta guía:** ¿qué patrón minimiza la complejidad operativa dado
que la latencia NO es el requisito dominante?

---

## Caso 3 · AgroIoT

Una empresa agrícola despliega **500.000 sensores de riego y clima**
en el campo.

- **Conectividad intermitente**: los sensores transmiten en ráfagas
  cuando hay señal, con datos que pueden llegar horas después.
- Necesitan **alertas de helada en menos de 1 minuto** desde que el
  sensor detecta la condición (cuando hay señal).
- Deben conservar los **datos crudos por 10 años** (trazabilidad para
  certificaciones de exportación).

**Pregunta guía:** ¿cómo afecta la conectividad intermitente a las
garantías de "tiempo real" que ofrecen Kappa o el streaming de
Lakehouse? ¿Aparece algún eje que los 4 vistos en clase no cubren?

---

## Formato de entrega

Cada equipo entrega, en su carpeta `equipo-N/`:

1. Un diagrama de arquitectura (`diagrama.md` con bloque \`\`\`mermaid o
   imagen exportada).
2. `arquitectura.md` completado (ver plantilla en `../plantillas/`).
3. `adr.md` completado (ver plantilla en `../plantillas/`).
4. Pull request abierto hacia `main` **antes del cierre de la sesión**.
