# Flujo de trabajo en equipo

1. **Al empezar el día** → `git switch main` + `git pull origin main`
2. **Crear tu rama** → `git switch -c feat/nombre`
3. **Trabajar y guardar** → `git add .` + `git commit -m "mensaje"`
4. **Subir y pedir revisión** → `git push -u origin feat/nombre` + abrir Pull Request en GitHub
5. **Cuando se mergea** → volver a `main`, hacer `pull` y sacar nueva rama desde ahí

**WARNING** Nunca trabajar directamente en `main`.

## crear una rama
```bash
git checkout -b nueva-rama # crea y cambia a una rama nueva (forma clasica)
git switch -c nueva-rama   # crea y cambia a una rama nueva (forma moderna)
```

## comprobar la rama
git branch