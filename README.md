# Aerosandwich: página web (demo)

Página de muestra para **Aerosandwich**, sandwichería y cafetería. Usa un tema de aviación ("Sabor que despega").

## Qué incluye

- **Carta digital** por categorías, con fotos, precios y códigos de "vuelo".
- **Pedido por WhatsApp**: el cliente arma su pedido y se abre WhatsApp con el mensaje y el total ya escritos.
- **Tablero "Salidas de hoy"**, al estilo de un aeropuerto, con lo más pedido.
- **Califica tu vuelo**: sección para conseguir reseñas en Google, con la maqueta de la tarjeta de mesa (QR + NFC).
- **Visítanos**: horario con indicador "Abierto ahora", dirección y redes.
- Funciona en celular y computador, con modo claro y oscuro.

## Propuesta para la dueña

`demo/propuesta.html` es una página aparte, para presentar el proyecto. Incluye:

- Diseño de la tarjeta NFC
- Maquetas en la mesa y en la barra
- Códigos QR reales
- Mejoras para Google Maps, Instagram y WhatsApp
- Ideas extra
- Plan de 4 semanas

Los enlaces de los QR están en `LINKS`, al final del archivo.

## Tarjeta NFC y carta

- `demo/tarjeta-nfc.html`: diseño de la tarjeta NFC. El frente es tipo pasaporte y el reverso tipo tarjeta de embarque. Incluye una planilla A4 lista para imprimir (10 tarjetas por lado, tamaño real 85,6 × 54 mm).
- `demo/carta.html`: carta "Menú a bordo". Son dos hojas A4 para imprimir, y en el celular se ve como carta digital. Los productos y precios están en `CARTA`, dentro del script.

Para imprimir, abre la página en el navegador, usa el botón "Imprimir" y elige A4 sin márgenes. La carta se imprime con "Gráficos de fondo" activado.

## Ver la demo

Abre `demo/index.html` en el navegador, o levanta un servidor local:

```bash
python -m http.server 5500 --directory demo
```

y entra a http://localhost:5500

## Editar datos

Todo está en el bloque `CONFIG` y en el arreglo `MENU`, al inicio del `<script>` de `demo/index.html`:

- `whatsapp`, `instagram`, `direccion`, `comuna`, `horario`
- `resenaGoogle`: enlace de reseña del Perfil de Empresa de Google (`https://g.page/r/XXXX/review`)
- `MENU`: productos, descripciones, precios y fotos

> Los datos y precios actuales son de ejemplo. Las fotos son provisorias; para la versión final se deben usar fotos propias del local.

## Publicar

Es un sitio estático (HTML + imágenes). Se puede publicar gratis en GitHub Pages, Netlify o Vercel apuntando a la carpeta `demo/`.
