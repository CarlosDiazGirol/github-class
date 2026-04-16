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
git branch# Flujo de trabajo en equipo

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
```bash
git branch # lista ramas locales y marca en cual estas
```

## Traernos todo
```bash
git pull             # trae y fusiona los ultimos cambios de main
git pull origin main # trae y fusiona los ultimos cambios de main
```

## Cuando se lía
```bash
git fetch origin           # descarga cambios remotos sin mezclar nada aun
git rebase origin/main     # reaplica tus commits encima de main (historial limpio)
git pull --no-rebase       # alternativa: fusiona con merge en vez de rebase (crea commit de merge)
```

## cambio de ramas sin commits
```bash
git stash     # guarda cambios temporales sin hacer commit
git stash pop # recupera lo guardado en stash y lo saca de la pila
```

## volver a un commit antigua funcional
```bash
git log --oneline # muestra historial corto para encontrar el hash
git switch -c rescate <hash-del-commit> # crea rama desde ese commit para rescatar trabajo
```

## PR (Pull Request)
```bash
git push -u origin nueva-rama # sube la rama y deja upstream configurado
# luego abrir Pull Request en GitHub para que alguien revise y mergee a main
```