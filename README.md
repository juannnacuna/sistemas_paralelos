# Sistemas Paralelos

Repositorio compartido para los ejercicios de la materia.

## Ramas

- `juani`
- `octavio`
- `main` → entregas finales acordadas entre los dos

## Setup inicial (solo una vez)

Clonar el repo y crear la rama:

```bash
git clone git@github.com:juannnacuna/sistemas_paralelos.git
cd sistemas_paralelos
git checkout -b juani
git push -u origin juani
```

## Flujo de trabajo

Trabajar directo en la rama:

```bash
git checkout juani
git add .
git commit -m "tp1 ej1: descripción breve"
git push
```

Cuando tenemos una versión final de un ejercicio, abrimos un Pull Request a `main` y el otro lo aprueba. `main` es solo entregas finales.

Para abrir el Pull Request:

1. GitHub muestra un banner "Compare & pull request" si pusheaste recientemente, hacer click ahí
2. Si no aparece, ir a Pull requests → New pull request
3. Seleccionar la rama propia como origen y main como destino
4. Poner un título y descripción breve, y crear el PR

El otro entra al PR, lo revisa, y hace click en Merge pull request.

## Traerse lo de main a tu rama

Si el otro mergeó algo a main y querés tenerlo en tu rama:

```bash
git checkout main
git pull
git checkout juani
git merge main
git push
```

## Ver y comparar el trabajo del otro

**Pararse en la rama del otro:**
```bash
git fetch origin
git checkout juani
```

**Ver las diferencias de un archivo específico:**
```bash
git diff juani -- tp1/ej1/main.c
```

**Traer un archivo de la rama del otro a la tuya** (cuidado, pisa tu versión):
```bash
git checkout juani -- tp1/ej1/main.c
```
