[README.md](https://github.com/user-attachments/files/26834661/README.md)
# NathsBalderas.com — Instrucciones de Deploy

## Archivos del sitio

| Archivo | Descripción |
|---------|-------------|
| `naths-balderas.html` | → Renombrar a `index.html` antes de subir |
| `codigo-alma.html` | Landing del Código del ALMA™ |

---

## 1. Deploy en GitHub Pages (gratis, paso a paso)

### Paso 1 — Crear el repositorio
1. Ir a [github.com](https://github.com) → botón verde **New**
2. Repository name: `nathsbalderas.com` (o cualquier nombre)
3. Visibilidad: **Public** (requerido para GitHub Pages gratis)
4. Crear sin README → **Create repository**

### Paso 2 — Subir los archivos
**Opción A (sin instalar nada):**
1. En el repo vacío → clic en **uploading an existing file**
2. Arrastrar `index.html` y `codigo-alma.html`
3. Commit changes → **Commit directly to main**

**Opción B (con Git):**
```bash
git init
git add index.html codigo-alma.html
git commit -m "Lanzamiento sitio"
git remote add origin https://github.com/TU_USUARIO/nathsbalderas.com.git
git push -u origin main
```

### Paso 3 — Activar GitHub Pages
1. En el repo → **Settings** → sección **Pages** (menú izquierdo)
2. Source: **Deploy from a branch**
3. Branch: **main** → carpeta: **/ (root)** → **Save**
4. Esperar ~2 minutos → tu sitio estará en:
   `https://TU_USUARIO.github.io/nathsbalderas.com`

---

## 2. Dominio personalizado (nathsbalderas.com)

### En GitHub:
Settings → Pages → Custom domain → escribe `nathsbalderas.com` → Save

### En tu proveedor de dominio (GoDaddy, Namecheap, etc.):
Añade estos registros DNS:

**Registros A (4 entradas):**
```
Tipo: A    Nombre: @    Valor: 185.199.108.153
Tipo: A    Nombre: @    Valor: 185.199.109.153
Tipo: A    Nombre: @    Valor: 185.199.110.153
Tipo: A    Nombre: @    Valor: 185.199.111.153
```

**Registro CNAME (para www):**
```
Tipo: CNAME    Nombre: www    Valor: TU_USUARIO.github.io
```

Propagación DNS: 10 min a 24h. GitHub activará HTTPS automáticamente.

---

## 3. Tally.so — La Señal™

### Crear el form en Tally:
1. Ir a [tally.so](https://tally.so) → **New form**
2. Añadir campo: Email (requerido)
3. Añadir campo: Nombre (opcional)
4. Personalizar colores si quieres → **Publish**

### Obtener el ID:
- En tu form publicado, la URL será: `https://tally.so/r/XXXXXXXX`
- El ID es esa parte final (ej: `wMRlob`)

### Pegar en el HTML:
En `index.html`, busca:
```
https://tally.so/embed/TU_FORM_ID
```
Reemplaza `TU_FORM_ID` con tu ID real. Ejemplo:
```
https://tally.so/embed/wMRlob?alignLeft=0&hideTitle=1&transparentBackground=1&dynamicHeight=1
```

### Estilo oscuro (opcional):
En Tally → tu form → **Share** → **Embed** → activar **Transparent background**
El sitio ya tiene el contenedor estilizado en terracota/oscuro.

---

## 4. Cal.com — Ya integrado en codigo-alma.html

El código de Cal.com ya está instalado en `codigo-alma.html`.
El botón "Agendar conversación gratuita" abre tu calendario automáticamente.

**Si cambias el nombre del evento en Cal.com:**
En el HTML busca `nathsbalderas/30min` y reemplaza `30min` con el slug de tu evento.

---

## 5. URLs ya configuradas

| Plataforma | URL |
|-----------|-----|
| Instagram | https://www.instagram.com/nathsbalderas |
| YouTube | https://youtube.com/@nathsbalderas |
| Substack | https://substack.com/@nathsbalderas |
| Cal.com | https://app.cal.com/nathsbalderas/30min |

---

## 6. Actualizaciones futuras

Para cambiar contenido después del deploy:
1. Editar el HTML localmente
2. En GitHub → abrir el archivo → ícono de lápiz ✏️ → editar → Commit
3. GitHub Pages se actualiza automáticamente en ~1 minuto

---

*Naths Balderas · Alquimista de Negocios™ · Coach en Neuroconsciencia*
