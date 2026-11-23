# Semana 1: endpoint /api/version

## Objetivo

Agregar el endpoint `GET /api/version`, que devuelva la versión definida en `app/proyecto.py`, con su prueba.

## Herramienta y modelo

Claude Code en VS Code, modelo Claude Opus 5.5.

## Prompt

> Lee AGENTS.md. Agrega el endpoint GET /api/version, que devuelva la versión definida en app/proyecto.py, con su prueba en tests/test_inicio.py. Antes de escribir código, explícame qué archivos vas a modificar y espera mi aprobación.

## Resultado

- Rama `tarea/version`.
- Prueba primero: `test_api_devuelve_la_version_del_proyecto` en `tests/test_inicio.py` (falló antes de escribir el código).
- Endpoint `GET /api/version` en `app/rutas/api.py`, que responde `{"version": proyecto.VERSION}`.
- Verificación: 7 pruebas pasaron y `ruff check .` sin errores.
- Correcciones: ninguna.
