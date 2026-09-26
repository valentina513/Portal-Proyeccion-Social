# COMANDOS FRONTEND — versión Laura (su PC, su cuenta, su repo)

Escenario: Laura ya tiene GitHub en su PC y creó el repo
`valentina513/Portal-Proyeccion-Social`. Solo pega estos comandos en orden.

Cada línea = un comando. Se pega, Enter, y al siguiente.

---

## PASO 1 — Traer el repo a su PC (una sola vez)

Abre PowerShell y pega:

```
git clone https://github.com/valentina513/Portal-Proyeccion-Social.git
```

```
cd Portal-Proyeccion-Social
```

## PASO 2 — Pegar los archivos

Dentro de la carpeta `Portal-Proyeccion-Social` (que acaba de crear el clone),
pegar el contenido que le pasaron, es decir, estas carpetas/archivos:

- `src`
- `index.html`
- `package.json`
- `package-lock.json`
- `vite.config.js`
- `.gitignore`
- `docs`

Ojo: pegar ASÍ ENCIMA (sobrescribir), no borrar nada. El README de la carpeta puede quedarse.

## PASO 3 — Crear la rama de integración (una sola vez)

```
git branch develop
```

```
git push -u origin develop
```

```
git switch develop
```

## PASO 4 — Comprobar que los archivos están ahí

```
git status
```

Debe mostrar archivos "untracked" (src, index.html, ...). Si no aparecen, la
carpeta donde pegó los archivos no es la del repo (está en el paso 2).

Test rápido (opcional):

```
npm install
```

```
npm run dev
```
(se abre http://localhost:5173; cerrar con Ctrl+C)

---

## PASO 5 — Las 12 tareas

**No cambiar nada**: cada bloque está completo. Se pega bloque por bloque
(12 bloques en total).

### Tarea 1 — base-vite
```
git switch develop
git pull origin develop
git switch -c feature/base-vite develop
git add index.html package.json package-lock.json vite.config.js src/main.jsx src/App.jsx src/index.css src/routes/AppRouter.jsx docs
git commit -m "feat(base): estructura vite del portal"
git push -u origin feature/base-vite
git switch develop
git merge feature/base-vite --no-ff -m "Merge feature/base-vite"
git push origin develop
```

### Tarea 2 — autenticacion
```
git switch develop
git pull origin develop
git switch -c feature/autenticacion develop
git add src/services/authService.js src/services/api.js src/pages/publico/Login.jsx src/pages/publico/Registro.jsx src/routes/RutaAutenticada.jsx
git commit -m "feat(auth): login, registro y sesion"
git push -u origin feature/autenticacion
git switch develop
git merge feature/autenticacion --no-ff -m "Merge feature/autenticacion"
git push origin develop
```

### Tarea 3 — layout-admin
```
git switch develop
git pull origin develop
git switch -c feature/layout-admin develop
git add src/components/layout/AdminLayout.jsx src/components/layout/Navbar.jsx src/components/layout/Footer.jsx src/pages/publico/NoAutorizado.jsx src/routes/RutaPrivada.jsx
git commit -m "feat(admin): layout del panel de administrador"
git push -u origin feature/layout-admin
git switch develop
git merge feature/layout-admin --no-ff -m "Merge feature/layout-admin"
git push origin develop
```

### Tarea 4 — portal-publico
```
git switch develop
git pull origin develop
git switch -c feature/portal-publico develop
git add src/pages/publico/Inicio.jsx src/pages/publico/Buscar.jsx src/pages/publico/Filtros.jsx src/pages/publico/DetallePublicacion.jsx src/pages/publico/MisProyectos.jsx src/pages/publico/Propuesta.jsx src/pages/publico/Solicitud.jsx src/components/SolicitudModal.jsx src/services/publicacionesService.js src/services/solicitudesService.js
git commit -m "feat(portal): catalogo, busqueda, detalle y solicitud"
git push -u origin feature/portal-publico
git switch develop
git merge feature/portal-publico --no-ff -m "Merge feature/portal-publico"
git push origin develop
```

### Tarea 5 — gestion-publicaciones
```
git switch develop
git pull origin develop
git switch -c feature/gestion-publicaciones develop
git add src/pages/admin/Publicaciones.jsx src/pages/admin/NuevaPublicacion.jsx src/components/FormularioPublicacion.jsx
git commit -m "feat(admin): gestion de publicaciones"
git push -u origin feature/gestion-publicaciones
git switch develop
git merge feature/gestion-publicaciones --no-ff -m "Merge feature/gestion-publicaciones"
git push origin develop
```

### Tarea 6 — moderacion-comentarios
```
git switch develop
git pull origin develop
git switch -c feature/moderacion-comentarios develop
git add src/pages/admin/Comentarios.jsx src/services/comentariosService.js
git commit -m "feat(admin): moderacion de comentarios"
git push -u origin feature/moderacion-comentarios
git switch develop
git merge feature/moderacion-comentarios --no-ff -m "Merge feature/moderacion-comentarios"
git push origin develop
```

### Tarea 7 — usuarios-roles
```
git switch develop
git pull origin develop
git switch -c feature/usuarios-roles develop
git add src/pages/admin/Usuarios.jsx src/services/usuariosService.js src/utils/roles.js
git commit -m "feat(admin): usuarios y roles"
git push -u origin feature/usuarios-roles
git switch develop
git merge feature/usuarios-roles --no-ff -m "Merge feature/usuarios-roles"
git push origin develop
```

### Tarea 8 — gestion-solicitudes
```
git switch develop
git pull origin develop
git switch -c feature/gestion-solicitudes develop
git add src/pages/admin/Solicitudes.jsx src/services/solicitudesService.js
git commit -m "feat(admin): gestion de solicitudes"
git push -u origin feature/gestion-solicitudes
git switch develop
git merge feature/gestion-solicitudes --no-ff -m "Merge feature/gestion-solicitudes"
git push origin develop
```

### Tarea 9 — galeria-imagenes
```
git switch develop
git pull origin develop
git switch -c feature/galeria-imagenes develop
git add src/pages/admin/Imagenes.jsx
git commit -m "feat(admin): galeria de imagenes"
git push -u origin feature/galeria-imagenes
git switch develop
git merge feature/galeria-imagenes --no-ff -m "Merge feature/galeria-imagenes"
git push origin develop
```

### Tarea 10 — reportes
```
git switch develop
git pull origin develop
git switch -c feature/reportes develop
git add src/pages/admin/Reportes.jsx src/services/reportesService.js
git commit -m "feat(admin): reportes y estadisticas"
git push -u origin feature/reportes
git switch develop
git merge feature/reportes --no-ff -m "Merge feature/reportes"
git push origin develop
```

### Tarea 11 — trazabilidad
```
git switch develop
git pull origin develop
git switch -c feature/trazabilidad develop
git add src/pages/admin/Actividad.jsx src/services/actividadService.js
git commit -m "feat(admin): trazabilidad de actividad"
git push -u origin feature/trazabilidad
git switch develop
git merge feature/trazabilidad --no-ff -m "Merge feature/trazabilidad"
git push origin develop
```

### Tarea 12 — dashboard
```
git switch develop
git pull origin develop
git switch -c feature/dashboard develop
git add src/pages/admin/Dashboard.jsx
git commit -m "feat(admin): dashboard del panel"
git push -u origin feature/dashboard
git switch develop
git merge feature/dashboard --no-ff -m "Merge feature/dashboard"
git push origin develop
```

---

## PASO 6 — Cerrar el git-flow (opcional, recomendado)

```
git switch -c release/v1.0 develop
git push -u origin release/v1.0
git switch main
git pull origin main
git merge release/v1.0 --no-ff -m "Merge release/v1.0"
git push origin main
git tag v1.0.0
git push origin v1.0.0
```
