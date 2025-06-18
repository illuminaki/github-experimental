# Guía de Trabajo Colaborativo en GitHub

Bienvenido al repositorio de prácticas de Git y GitHub. Aquí aprenderás a colaborar con tu equipo de manera profesional, enfrentando conflictos reales, usando Pull Requests y siguiendo convenciones.

## Flujo de trabajo recomendado

1. Clona el repositorio.
2. Crea una nueva rama:

   ```bash
   git checkout -b feature/nombre-claro
   ```

3. Trabaja en tus cambios.
4. Haz commit y push de tus cambios:

   ```bash
   git commit -m "feat: agregar formulario de login"
   git push origin feature/nombre-claro
   ```

5. Abre un Pull Request (PR) hacia `main`.


## Reglas del Repositorio

- Todas las ramas deben seguir la convención:
  - `feature/*`, `bugfix/*`, `hotfix/*`, `release/*`
- No se permite hacer push directo a `main`.
- Todos los PRs deben:
  - Tener al menos 1 aprobación.
  - Pasar los test automáticos.
  - Estar actualizados con `main`.

---

## ¿Qué es un Pull Request (PR)?

Un Pull Request es una solicitud para que tus cambios sean revisados y fusionados al código principal. Es una oportunidad para recibir retroalimentación y asegurar la calidad del código antes de integrarlo.

---

## ¿Cómo resolver conflictos?

Un conflicto ocurre cuando dos ramas modifican la misma parte del código. Para resolverlo:

1. Actualiza tu rama local con la base (`main`):

   ```bash
   git fetch origin
   git merge origin/main
   ```

2. Verás los archivos con conflicto. Ábrelos y verás algo como:

   ```diff
   <<<<<<< HEAD
   código desde tu rama
   =======
   código desde main
   >>>>>>> main
   ```

3. Decide qué partes conservar, edita y guarda el archivo.
4. Marca el conflicto como resuelto:

   ```bash
   git add archivo-afectado
   git commit
   ```

5. Finalmente:

   ```bash
   git push
   ```

---

## Buenas prácticas de colaboración

- Haz commits pequeños y descriptivos.
- Revisa Pull Requests de tus compañeros.
- Usa draft PRs si aún no has terminado tu trabajo.
- Nunca trabajes en `main` directamente.

---

## Estructura de ramas sugerida

| Tipo     | Convención         | Ejemplo                  |
|----------|--------------------|--------------------------|
| Feature  | feature/*          | feature/login-form       |
| Bugfix   | bugfix/*           | bugfix/email-validation  |
| Hotfix   | hotfix/*           | hotfix/checkout-error    |
| Release  | release/vX.X.X     | release/v1.2.0           |

---

## Reglas de protección activadas

- `main` es una rama protegida.
- Todos los Pull Requests deben pasar pruebas automáticas.
- Se requiere al menos un revisor.
- Debes actualizar tu rama con `main` antes de poder hacer merge.

---

## Objetivo del repositorio

El propósito de este repositorio es que experimentes:

- Cómo trabajar en equipo con Git.
- Cómo resolver conflictos reales.
- Cómo usar Pull Requests y revisiones.
- Qué hacer cuando Git te pone a prueba.

¡Buena suerte y colabora como en un proyecto real!
