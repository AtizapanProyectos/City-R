# City R · Román Cortés

Copia independiente y completa de la aplicación City V, con identidad guinda, iconografía SVG y diseño adaptable a teléfonos, tablets y escritorio. Conserva mapa electoral, resultados y proyecciones, padrón, cargas Excel, encuestas, escucha social, administrador Django y datos locales.

## Ejecutar localmente

Crear un entorno con Python 3.12, instalar requirements.txt y definir DEBUG=True. Ejecutar python manage.py migrate y python manage.py runserver. Los usuarios y contraseñas se conservan en el SQLite copiado; el login utiliza la autenticación de Django.

## Publicar

Rama main del repositorio https://github.com/AtizapanProyectos/City-R.git. La identidad del inicio es Román Cortés. Railway usa Railpack y Procfile; no se usa Docker. Consultar DEPLOY_RAILWAY.md para configurar SECRET_KEY, dominio, volumen exclusivo /data y transferencia de media/escucha social cuando corresponda.

## Diseño

Guinda principal #681b38; acento #8d284c; neutros cálidos y acentos rosados. Encabezados y controles usan fondos guinda sólidos, sin mezclas con verde. Los partidos y el sentimiento mantienen sus colores semánticos. Las cuatro pestañas táctiles están disponibles hasta 1200 px y la leyenda del mapa se puede desplegar. La interfaz no incluye emojis; se utilizan iconos SVG accesibles.

## Verificar

python manage.py test maps elections territory

node --test scripts/test_dashboard.cjs

## Validación de esta copia

Pasaron 25 pruebas de Django, 4 de JavaScript y 3 de inicialización de SQLite. La interfaz se comprobó en Chromium con interacción táctil, en 320, 360, 390, 600, 768, 820, 1024, 1180, 1194, 1200, 1366 y 1920 px, además de orientación horizontal. Se verificaron login, las cuatro pestañas, filtros, paginación, gráficas, formularios, captura y cargas de archivos, sin errores de JavaScript ni desbordamiento horizontal. El contenido completo de SQLite y los archivos del backend se compararon con City V.
