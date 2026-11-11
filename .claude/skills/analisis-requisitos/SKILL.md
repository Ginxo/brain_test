---
name: analisis-requisitos
description: Analiza un documento de requisitos (Word/PDF), lo cruza con el esquema de base de datos y otras fuentes, y genera el documento funcional a partir de un flujo de preguntas y respuestas con el usuario. Úsalo cuando se pida analizar requisitos o elaborar un documento funcional.
---

# Análisis de requisitos → documento funcional

Contexto: proyecto de Typ para un cliente del sector farmacéutico (ver README.md). Trabaja siempre en español.

## Entradas

- Documento de requisitos (.docx o .pdf).
- Esquema de base de datos (SQL, DDL, diagrama o export).
- Otras fuentes opcionales (documentación previa, capturas, correos, funcionales anteriores).

Si falta alguna entrada, pídela antes de continuar.

## Flujo

1. **Lectura**: lee todas las fuentes y extrae los requisitos, entidades, actores y reglas de negocio.
2. **Cruce**: compara los requisitos con el esquema de BD y detecta:
   - Campos o tablas mencionados en los requisitos que no existen en el esquema.
   - Elementos del esquema sin requisito asociado.
   - Ambigüedades, contradicciones o huecos entre fuentes.
3. **Preguntas**: formula las dudas al usuario en pequeños bloques (máximo 5 preguntas por turno), priorizando las que bloquean el diseño. Indica de qué fuente surge cada duda. No inventes respuestas: lo no confirmado queda marcado como pendiente.
4. **Iteración**: incorpora las respuestas y repite el paso 3 hasta que no queden dudas bloqueantes o el usuario indique que basta.
5. **Generación**: redacta el documento funcional con las respuestas obtenidas.

## Estructura del documento funcional

1. Objetivo y alcance
2. Actores / roles
3. Requisitos funcionales (identificador, descripción, reglas de negocio, trazabilidad con tablas/campos de BD)
4. Casos de uso o flujos principales
5. Modelo de datos relevante
6. Supuestos y decisiones tomadas (con la respuesta que las originó)
7. Puntos pendientes

## Reglas

- Mantén trazabilidad: cada requisito referencia su fuente.
- Distingue lo que viene de los documentos de lo que viene de las respuestas del usuario.
- Datos sensibles (p. ej. datos de pacientes): no los copies al documento; usa descripciones genéricas.
- Entrega el documento en el formato que pida el usuario (por defecto Word).
