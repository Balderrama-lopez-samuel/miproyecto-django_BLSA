# Proyecto Django — Balderrama López Samuel Alberto

Proyecto Django conectado a MySQL en Aiven y desplegado en Render.

## Producción
https://miproyecto-django-blsa.onrender.com

- Servicios: https://miproyecto-django-blsa.onrender.com/servicios/
- Panel de administración: https://miproyecto-django-blsa.onrender.com/admin/

## Cómo correrlo localmente
1. Crear y activar un entorno virtual
2. pip install -r requirements.txt
3. Copiar .env.example a .env y completar con credenciales propias de Aiven, un SECRET_KEY y DEBUG=True
4. python manage.py migrate
5. python manage.py createsuperuser
6. python manage.py runserver

## Despliegue en Render
- **Build Command:** `pip install -r requirements.txt && python manage.py collectstatic --noinput`
- **Start Command:** `gunicorn miproyecto.wsgi`
- **Variables de entorno:** `DB_NAME`, `DB_USER`, `DB_PASSWORD`, `DB_HOST`, `DB_PORT`, `SECRET_KEY`, `DEBUG=False`, `ALLOWED_HOSTS=miproyecto-django-blsa.onrender.com`

## Evidencia
- Semana 3 (Django + MySQL en Aiven): capturas de `migrate`, tablas en Aiven y vistas locales en la carpeta [/evidencia](evidencia).
- Semana 4 (modelo Servicio + Render): capturas del panel /admin, /servicios/ en producción y el Web Service en Render en la carpeta [/evidencia/unidad2_Django_OnRender](evidencia/unidad2_Django_OnRender).
