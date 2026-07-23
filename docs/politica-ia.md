# Política de uso de IA — ST1630

## Principio rector

Usar agentes de IA (Claude Code, Copilot, ChatGPT, etc.) es **legítimo**
en este curso. **No saber explicar el resultado, no lo es.** Evaluamos tu
criterio como ingeniero, no si sabes escribir cada línea a mano.

> Regla mnemotécnica del taller de S2: *"la IA dibuja y pule; tú decides
> y firmas."*

## La bitácora de delegación

Cada entregable calificado (labs, talleres, proyecto final) debe incluir,
al final del documento o del README de tu entrega, una tabla como esta:

```markdown
## Bitácora de delegación

| Tarea | ¿Delegado a agente? | Justificación |
|---|---|---|
| Setup de credenciales AWS | Sí | Troubleshooting repetitivo, bajo valor de aprendizaje |
| Elección de partición del datalake | No | Decisión de diseño central del lab |
| Script de ingesta batch | Parcial | Boilerplate del agente + lógica de negocio propia |
```

**No hay penalización por delegar tareas de bajo valor pedagógico.**
**Sí hay penalización por:**
1. No declarar una delegación.
2. Delegar algo que la rúbrica específica de esa actividad marque
   explícitamente como "debe hacerse a mano".

## Qué se permite delegar por defecto (salvo que la rúbrica diga lo contrario)

- Generar diagramas (Mermaid, etc.) a partir de un diseño que TÚ ya definiste.
- Formatear o pulir la redacción de un documento.
- Resolver dudas puntuales de sintaxis o de una tecnología específica.
- Troubleshooting de instalación/configuración de entornos.
- Boilerplate repetitivo (imports, estructura básica de un script).

## Qué debe hacerse a mano por defecto (salvo que la rúbrica diga lo contrario)

- Extracción de requisitos y decisiones de arquitectura.
- Elección del patrón/tecnología y su justificación.
- Architecture Decision Records (ADR) completos.
- Revisión cruzada del trabajo de otro equipo.
- Cualquier pregunta de un parcial marcada como "sin agentes".

## Reglas específicas por evaluación

| Evaluación | Uso de agentes |
|---|---|
| Parcial 1 (S8) | **Prohibido** — individual, supervisado, sin agentes. |
| Parcial 2 (S14) | Permitido, con preguntas de criterio que un agente no resuelve por ti. |
| Labs 1–5 | Permitido según la rúbrica de cada lab; bitácora obligatoria. |
| Talleres formativos (S2, etc.) | Permitido según se indique en el taller; bitácora obligatoria. |
| Proyecto final | Permitido con bitácora; se audita en la sustentación oral. |

## Por qué existe esta política

La IA agéntica está cambiando el rol del ingeniero de datos: construir
pipelines es cada vez más rápido, pero decidir qué construir, verificar
que sea correcto y hacerse responsable del resultado sigue siendo
trabajo humano. Este curso evalúa esa segunda parte.
