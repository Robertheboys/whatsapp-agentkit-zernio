# WhatsApp Agentreply — instrucciones para Gemini CLI

> Gemini CLI lee este archivo (`GEMINI.md`) como contexto. La fuente canónica del onboarding
> es `CLAUDE.md`; sigue ese proceso.

Este repositorio conecta números de **WhatsApp** (vía **Zernio**) con **IA** (vía **OpenRouter**).

## Si el usuario te pide "configura/usa este repositorio"

Lee el archivo **`CLAUDE.md`** de este repo y sigue su flujo de onboarding (FASE 1 a 6). Reglas clave:

- Habla **SIEMPRE en español**, **una pregunta a la vez**, no avances de fase sin confirmar.
- **NUNCA** escribas claves en archivos versionados. Van **solo en `.env`** (está en `.gitignore`).
- Verifica Python 3.11+, instala dependencias, crea `.env` desde `.env.example`.
- Genera `config/businesses.yaml` desde `config/businesses.example.yaml` con los datos del usuario.
- Prueba con `python tests/test_local.py`; luego guía el deploy (Railway MCP / Coolify / Docker) y
  el alta del webhook en Zernio.

Credenciales: `OPENROUTER_API_KEY`, `ZERNIO_API_KEY`, `account_id` por número. Anuncios opcional.
