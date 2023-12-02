# WhatsApp Api

Consiste en una API que admite un método POST para enviar mensajes a un número de teléfono determinado.

## Funcionalidad

Admite:

- Texto plano

No admite:

- Mensajes de audio
- Imágenes
- Otros

## Instalación

Para instalar y ejecutar este proyecto localmente, necesitarás Node.js y Docker instalados en tu computadora.

Primero, instala las dependencias del proyecto:

```bash
npm install
```

Luego, construye el proyecto:

```bash
npm run build
```

Para ejecutar el proyecto en modo de desarrollo:

```bash
npm run dev
```

## Uso local

1. Abrir la URL en el navegador:
   http://localhost:3001/qr.svg
2. Escanear código QR para iniciar sesión
3. Abrir postman y ejecutar una petición post:
   - Endpoint: http://localhost:3001/lead
   - Body:
     ```json
     {
       "phone": "3464XXXXXX",
       "message": "prueba"
     }
     ```

## Docker

Para construir la imagen de Docker de este proyecto, usa el siguiente comando:

```bash
docker build -t api-whatsapp-ts .
```

Para ejecutar la imagen de Docker:

```bash
docker run --privileged -e PORT=3001 -p 3001:3001 api-whatsapp-ts:latest
```

## Authors

- [Leifer Méndez](https://github.com/leifermendez)
- [Carlos Martínez](https://github.com/carlosmgv02): forked to update README + couple more changes
