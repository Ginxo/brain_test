# brain_test

Repositorio de contexto compartido del proyecto para el equipo. Sirve para que cualquier compañero (y Claude) disponga del mismo punto de partida.

## Contexto del proyecto

- **Typ** es una consultora de software.
- Su **cliente principal** desarrolla una **aplicación farmacéutica**.
- Typ participa en el análisis, diseño y desarrollo de esta aplicación.

> Al tratarse del sector farmacéutico, hay que tener especial cuidado con los datos sensibles (p. ej. datos de pacientes) y con la trazabilidad de los requisitos. No incluyas datos reales en este repositorio.

## Estructura

```
.
├── README.md                              # Este documento: contexto del proyecto
└── .claude/
    └── skills/
        └── analisis-requisitos/
            └── SKILL.md                   # Skill de análisis de requisitos
```

## Skills

### `analisis-requisitos`

Versión básica. Cruza un documento de requisitos (Word/PDF) con el esquema de base de datos y otras fuentes, plantea preguntas al usuario para resolver dudas y genera el **documento funcional** a partir de ese flujo de pregunta/respuesta.

Uso: pide a Claude "analiza este documento de requisitos" adjuntando el documento y el esquema de BD.

## Cómo contribuir

- Añade aquí el contexto relevante del proyecto (glosario, decisiones, arquitectura, contactos) conforme vaya haciendo falta.
- Los nuevos skills van en `.claude/skills/<nombre-del-skill>/SKILL.md`.
