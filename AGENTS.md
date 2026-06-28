# WhatsApp Agentreply — instrucciones para agentes de IA

> Este archivo lo leen los agentes de terminal que usan el estándar `AGENTS.md`
> (OpenAI Codex CLI, Cursor, y otros). La fuente canónica del onboarding es `CLAUDE.md`.

Este repositorio es un kit para conectar uno o más números de **WhatsApp** (vía **Zernio**)
con un cerebro de **IA** (vía **OpenRouter**), con personalidad por número y atribución de
anuncios/ROAS opcional.

## Si el usuario te pide "configura/usa este repositorio"

Lee el archivo **`CLAUDE.md`** de este repo y sigue su flujo de onboarding (FASE 1 a 6) al pie de
la letra. Reglas clave:

- Habla **SIEMPRE en español**, **una pregunta a la vez**, y no avances de fase sin confirmar.
- **NUNCA** escribas claves/API keys en archivos versionados. Van **solo en `.env`** (que está en
  `.gitignore`). El `config/businesses.yaml` NO lleva claves.
- Verifica Python 3.11+, `pip install -r requirements.txt`, crea `.env` desde `.env.example`.
- Entrevista al usuario por cada negocio y genera `config/businesses.yaml` desde
  `config/businesses.example.yaml`.
- Prueba con `python tests/test_local.py` (chat en la terminal) antes de hablar de deploy.
- Guía el deploy (Railway vía MCP / Coolify / Docker) y el alta del webhook en Zernio.

Credenciales que necesita el usuario: `OPENROUTER_API_KEY`, `ZERNIO_API_KEY` y el `account_id`
de cada número (dashboard de Zernio). Anuncios/ROAS es opcional (`ENABLE_ADS=true`).
