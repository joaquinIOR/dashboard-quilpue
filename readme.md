# Dashboard Quilpué

Plataforma web de dashboard y visualización de datos para la Municipalidad de Quilpué.

## Requisitos

- Python 3.12 (instalado desde python.org, con "Add python.exe to PATH")
- Git
- Se recomienda VS Code 

## Instalación local

```powershell
git clone <https://github.com/joaquinIOR/dashboard-quilpue>
cd dashboard-quilpue

python -m venv .venv
.venv\Scripts\Activate.ps1  #(todos tenemos windows )

pip install -r requirements.txt
copy .env.example .env             
```

Generar una clave propia y pegarla en `DJANGO_SECRET_KEY` dentro de `.env`:

```powershell
python -c "from django.core.management.utils import get_random_secret_key; print(get_random_secret_key())"
```

Levantar el proyecto:

```powershell
python manage.py migrate
python manage.py runserver
```

## Flujo de trabajo

- `main`: versión estable. Sin commits directos.
- `develop`: integración. Todos los PR apuntan aquí.
- Ramas de trabajo desde `develop`: `feature/...`, `fix/...`, `docs/...`
- Cada PR requiere 1 aprobación de otro integrante.

## Problemas comunes

- **"No te encontró Python" / abre la Microsoft Store**: desactivar los alias en Configuración → Aplicaciones → Configuración avanzada de aplicaciones → Alias de ejecución de aplicaciones, y reabrir la terminal.
- **PowerShell bloquea `Activate.ps1`**: ejecutar `Set-ExecutionPolicy -Scope CurrentUser RemoteSigned` y listo .
- **`KeyError: 'DJANGO_SECRET_KEY'`**: falta el archivo `.env` o la clave está vacía.

## Equipo

<!-- Cada integrante se agrega aquí mediante su propio PR --># Dashboard Quilpué

