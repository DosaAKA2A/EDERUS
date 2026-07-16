# EDERUS — Tienda oficial

Sitio estático (GitHub Pages) + Cloudflare Worker como backend.
Todo el frontend vive en un solo archivo por página: HTML + CSS + JS inline.

## Estructura
- `index.html` — landing completa
- `assets/` — marca, insignias, imágenes
- `worker/` — código del Cloudflare Worker (se pega a mano en el panel de CF)

## Validar antes de cada push
El JS va inline; un error de sintaxis rompe la página entera sin avisar.

```bash
python3 -c "
import re; html=open('index.html').read()
open('/tmp/check.js','w').write(re.findall(r'<script>(.*?)</script>',html,re.S)[-1])"
node --check /tmp/check.js
```

## Marca
Azules Ederus: `#0081B9` · `#00B2FF` · `#A1D8FF`
