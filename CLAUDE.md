# Guadalupana Digital — contexto del proyecto

## Qué es
Sitio web para promover la devoción guadalupana entre latinos en EE. UU., con foco en los
"No Sabo kids" (latinos nacidos en EE. UU., más cómodos en inglés). Monetiza como **gestores**
(no agencia): hacemos en persona, en la Basílica de Guadalupe (CDMX), intenciones de misa,
entrega de rosas y veladoras para quien no puede viajar, y cobramos solo una tarifa de servicio.

## El usuario
- Parte de cero en programación; explicar cada paso en español, sencillo.
- Preferencia: rigor en los datos, no inventar. Citar fuentes; marcar lo no verificado.

## Reglas de contenido (no romper)
- Siempre visible: servicio independiente, sin afiliación con la Basílica; la ofrenda oficial se entrega
  íntegra y solo cobramos tarifa de servicio. Usar la palabra "gestores".
- La "Tarjeta de Devoción" NO es certificado de la Basílica (la Basílica vende un
  "Certificado de Bendición Guadalupana" oficial; no imitarlo).
- No testimonios ni reseñas inventadas. No fotos sin derechos.
- La frase «El mexicano nace donde le da la gana» va en Guadalupe 101, sin atribuir autor (no verificado).
- Símbolos de la imagen = "lecturas tradicionales", no doctrina oficial.

## Archivos
- `index.html` — página única bilingüe EN/ES (textos en el objeto `T` del script; claves `data-i18n`).
  Config arriba del script: `var WHATSAPP_NUMBER = "";` (pendiente; formato internacional, solo dígitos).
- `privacidad.html` — aviso de privacidad EN/ES, BORRADOR con campos `[DATO]` pendientes; requiere abogado.
- `og-image.png` (1200×630) + etiquetas Open Graph en `<head>`; `og:url` apunta a
  https://donllopo-dev.github.io/guadalupana-digital/ (cambiar si hay dominio propio).
- `favicon.svg`; `img/` — fotos por nombre fijo (ver `img/LEEME.md`); si falta el archivo se ve un marco.
  Ya existe `img/guadalupe-101.jpg` (pendiente confirmar licencia de la imagen).

## Diseño
Paleta (tokens `--guadalupe-*` en `:root`): manto-turquesa #1E656D, tunica-rosa #C46D6D, oro-solar #D4AF37,
cinto-negro #1A1A1A, luna-ceniza #2D3136, tez-morena #B98A66, ala-verde #2D6A4F, ala-roja #9E2A2B.
Fuentes: Gloock (títulos) + Figtree (texto). Mobile-first, modo claro y oscuro.
Pendiente opcional: el texto dorado pequeño sobre turquesa tiene contraste bajo (~3.3:1).

## Flujo de trabajo
- Rama `desarrollo` = borrador (aquí van los cambios). `main` = versión publicable (GitHub Pages publica `main`).
  Publicar = merge de `desarrollo` a `main`, solo cuando el usuario lo pida.
- Repo: https://github.com/DonLlopo-dev/guadalupana-digital (público).
- Vista previa privada: https://claude.ai/artifact/FM5YDghT5aHokmyjbz3L26 — se publica desde una copia de
  `index.html` sin `<!doctype>/<html>/<head>/<body>` (el visor añade su esqueleto), con `privacidad.html`,
  `favicon.svg`, `og-image.png` e `img/*` como archivos adjuntos.

## Datos verificados de la Basílica (virgendeguadalupe.org.mx, consultado 6 nov 2026)
- Módulo de Misas y Donativos: misa diaria sin fecha $150 por intención; rosario con intención $150;
  misa rezada comunitaria (sáb/dom 7:45) $200; misa comunitaria 13:00 $350; misa capitular 9:00 transmitida
  $500 por intención; novenario virtual $3,500; misa individual Altar Mayor $2,500. La página no indica moneda
  (asumido MXN). Solicitudes con formatos de la oficina; "Ceremonia Grupal (NO agencia)".
- Canales en línea propios: intenciones.virgendeguadalupe.org.mx, velas.virgendeguadalupe.org.mx, tienda en línea.
- Bendición de veladoras: lun–vie 12:15, Templo Expiatorio. Sacristía: sacristia@inbg.mx, 55 5118 0500 ext. 514/515.

## Pendientes
Número de WhatsApp · más fotos (`img/`) · datos del aviso de privacidad + revisión legal · tarifas y política de
reembolso · formulario real (hoy es demo) · pagos (Stripe) · dominio propio · activar/decidir GitHub Pages ·
posible campaña "Paquete 12 de diciembre".
