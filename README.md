# Agentic-Headquarters

Personal AI Agent Headquarter compatible con OpenCode y Claude Code.

## Estructura

```
.
├── .agents/                       # Directorio principal
│   ├── skills/                    # Skills instalados
│   │   ├── ask-questions-if-underspecified/
│   │   ├── writing-plans/
│   │   ├── systematic-debugging/
│   │   ├── verification-before-completion/
│   │   └── test-driven-development/
│   └── commands/                   # Comandos personalizados
│       ├── learn.md
│       ├── finish-work.md
│       └── session-summary.md
├── .opencode -> .agents            # Symlink para OpenCode
├── .claude -> .agents              # Symlink para Claude Code
├── planificacion/
├── ia-core/
├── knowledge/
├── finanzas/
├── life-metrics/
└── package.json
```

## Instalación

```bash
npm install
```

Esto instala automáticamente:
- [bun](https://bun.sh)
- [opencode-ai](https://opencode.ai)

## Skills instalados

| Skill | Descripción | Origen |
|-------|-------------|--------|
| `ask-questions-if-underspecified` | Obliga a hacer preguntas antes de actuar en objetivos difusos | [trailofbits/skills](https://github.com/trailofbits/skills) |
| `writing-plans` | Obliga a crear planes paso a paso antes de modificar código | [obra/superpowers](https://github.com/obra/superpowers) |
| `systematic-debugging` | Fuerza investigación de causa raíz antes de proponer fixes | [obra/superpowers](https://github.com/obra/superpowers) |
| `verification-before-completion` | No permite claims de éxito sin evidencia fresca | [obra/superpowers](https://github.com/obra/superpowers) |
| `test-driven-development` | Evita que el agente omita el paso de "test fallando" | [obra/superpowers](https://github.com/obra/superpowers) |

## Comandos instalados

| Comando | Descripción |
|---------|-------------|
| `/learn` | Extrae aprendizajes no-obvios de la sesión a AGENTS.md |
| `/finish-work` | Pre-commit gate: calidad, docs, API, cross-layer |
| `/session-summary` | Captura acciones, costos, ineficiencias para handoff |

## Referencias útiles

- [12 OpenCode Skills Every Dev Team Should Steal](https://hackernoon.com/twelve-opencode-skills-every-dev-team-should-steal) - Guía completa de skills y comandos

## Uso

```bash
opencode
```

El agente detectará las carpetas y usará las skills/comandos instalados.