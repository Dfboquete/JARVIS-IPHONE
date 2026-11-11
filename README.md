# JARVIS iPhone — Build 0.2

Esta entrega es una PWA (aplicación web instalable) optimizada para iPhone y Mac.

## Importante sobre la sincronización
Esta versión contiene la interfaz móvil y comandos locales de demostración. **Todavía no sincroniza datos con el Mac ni está conectada a un modelo de IA.** Para sincronizar de verdad necesitamos desplegar un backend seguro compartido y configurar autenticación; no se debe poner ninguna clave de API dentro del HTML.

## Instalar en iPhone 13 Pro Max
1. Publica esta carpeta en un alojamiento HTTPS (por ejemplo, un hosting estático).
2. Abre la URL publicada en Safari en el iPhone.
3. Pulsa Compartir → Añadir a pantalla de inicio → Añadir.
4. Abre JARVIS desde el nuevo icono.

Una PWA necesita HTTPS para instalarse correctamente y activar el modo sin conexión. Abrir el HTML como archivo no activa todas las funciones de instalación.

## Ver en Mac durante pruebas
En Terminal, dentro de esta carpeta, ejecuta:
`python3 -m http.server 8000`
y abre `http://localhost:8000`.

## Funciones de esta demo
- Diseño móvil adaptable con safe areas de iOS.
- Núcleo HUD animado.
- Reloj en directo.
- Entrada de texto y comandos locales básicos.
- Síntesis de voz del navegador.
- Reconocimiento de voz cuando Safari/navegador lo soporte.
- Notas locales en el almacenamiento del navegador.
- Manifiesto PWA y service worker para caché.

## Siguiente etapa técnica
1. Publicar la PWA en HTTPS.
2. Crear backend privado (por ejemplo FastAPI) y autenticación.
3. Conectar un modelo de IA con la clave guardada en el servidor.
4. Crear memoria sincronizada en base de datos.
5. Conectar la app Mac y el iPhone al mismo backend.
6. Añadir permisos explícitos antes de acciones sensibles.

## Privacidad
No introduzcas contraseñas ni datos sensibles en las notas de esta demo. El almacenamiento local no es una bóveda segura ni se comparte entre dispositivos.
