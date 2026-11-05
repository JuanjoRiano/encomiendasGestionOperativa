# Encomiendas · Gestión operativa

Aplicación web para registrar encomiendas y seguir cada guía desde el despacho hasta la entrega. Usa Python, Flask y SQLite. **Chain of Responsibility** valida el registro y **State** controla qué operación se puede realizar en cada etapa.

## Ejecución

Necesitas Python 3.11 o posterior. Si te falta el entorno virtual, instala `python3-venv` con `sudo apt install python3-venv`.

Desde la carpeta que contiene `run.py`, ejecuta:

```bash
python3 -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
python -m flask --app run preparar-demo
python run.py
```

Abre [http://127.0.0.1:5000](http://127.0.0.1:5000). El comando `preparar-demo` crea la base de datos y carga los datos de ejemplo.

## Acceso de demostración

Todas las cuentas usan la contraseña `Demo2026!`.

| Perfil | Correo |
| --- | --- |
| Coordinación (acceso completo) | `coordinador@demo.local` |
| Operación en Bogotá | `operador@demo.local` |
| Operación en Medellín | `medellin@demo.local` |

Para probar la aplicación, entra como coordinador y abre **Guías de envío**. Selecciona una guía de ejemplo para consultar su estado, su historial y la siguiente operación disponible.

## Volver a iniciar

Detén el servidor con `Ctrl+C`. La próxima vez, desde la misma carpeta, ejecuta:

```bash
source .venv/bin/activate
python run.py
```

## Pruebas (opcional)

Con el entorno virtual activo:

```bash
python -m pip install -r requirements-dev.txt
python -m pytest -q
```
