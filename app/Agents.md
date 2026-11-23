# Guía para Agentes — AGENTS.md

Instrucción previa: revisa este documento completo antes de tocar cualquier archivo del repositorio[cite: 1].

## Visión general
Aplicación educativa interactiva enfocada en estudiantes de primaria (6 a 12 años) para introducir fundamentos de lógica y programación mediante desafíos visuales (secuencias, patrones y bucles básicos como avanzar, girar y repetir)[cite: 1]. El progreso se premia con 1 a 3 estrellas según el desempeño, habilitando nuevos intentos para perfeccionar resultados[cite: 1]. Existen dos perfiles: profesorado y alumnado; los estudiantes acceden mediante un código de aula y un avatar, sin requerir correo electrónico[cite: 1].

## Arquitectura y tecnologías
- Backend en Python 3.11+ con FastAPI y renderizado mediante Jinja2[cite: 1].
- Persistencia con SQLModel: SQLite durante el trabajo local y PostgreSQL en producción[cite: 1].
- Suite de pruebas con pytest (incluyendo TestClient) y control de calidad con Ruff[cite: 1].
- Automatización de integración continua en GitHub Actions y alojamiento en Render[cite: 1].

## Flujo de trabajo en terminal
- Dependencias: `pip install -r requirements-dev.txt`[cite: 1]
- Servidor local: `uvicorn app.main:app --reload`[cite: 1]
- Suite de tests: `pytest -v`[cite: 1]
- Análisis de código: `ruff check .`[cite: 1]

## Organización del código
- `app/rutas/`: puntos de entrada HTTP que delegan en la capa de servicios sin contener lógica de dominio[cite: 1].
- `app/servicios/`: lógica de negocio aislada y respaldada por su propia batería de pruebas[cite: 1].
- `app/modelos/`: esquemas y tablas definidos con SQLModel[cite: 1].
- `app/templates/` y `app/static/`: vistas, estilos y recursos de la PWA[cite: 1].
- `tests/`: pruebas unitarias y de integración; `tests/aceptacion/`: validaciones frente a los requisitos funcionales[cite: 1].
- `app/proyecto.py`: metadatos del sistema y dirección web publicada[cite: 1].

## Pautas de desarrollo
- Redactar identificadores y nombres descriptivos en español, evitando abreviaturas ambiguas[cite: 1].
- Mantener parches acotados, trabajar una funcionalidad por rama y ejecutar verificaciones antes de entregar cambios[cite: 1].
- Consultar `STATE.md` al comienzo de cada sesión de trabajo[cite: 1].

## Restricciones críticas
- Jamás incorporar credenciales, tokens o secretos en el código fuente; obtenerlos siempre desde variables de entorno[cite: 1].
- No añadir paquetes sin confirmar previamente su disponibilidad en PyPI[cite: 1].
- Está prohibido alterar o eliminar tests existentes únicamente para forzar su aprobación[cite: 1].
- Nunca emplear información real o identificable de menores[cite: 1].
- No realizar `git commit` ni `git push`; esas acciones corresponden exclusivamente al desarrollador[cite: 1].

## Bitácora de errores
Registra aquí cada fallo detectado junto con la medida preventiva para no volver a cometerlo[cite: 1].