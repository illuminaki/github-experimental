# Guía simplificada para crear y usar llaves SSH en GitHub

## 1. Abre una terminal
- En Linux o Mac: abre la terminal.
- En Windows: abre Git Bash.

## 2. Genera una nueva llave SSH
Escribe este comando y presiona Enter:
```bash
ssh-keygen -t rsa -b 4096
```
- Cuando te pregunte por el nombre del archivo, solo presiona Enter para usar el nombre por defecto (`id_rsa`).
- Cuando te pida una contraseña, puedes dejarla vacía y presionar Enter (esto es más fácil, pero menos seguro).

## 3. Asegúrate de que el agente SSH esté funcionando
Ejecuta:
```bash
eval "$(ssh-agent -s)"
```
- Si todo está bien, verás un mensaje como: `Agent pid 12345`.

## 4. Agrega tu llave privada al agente SSH
Ejecuta:
```bash
ssh-add ~/.ssh/id_rsa
```

## 5. Copia tu llave pública
- En Linux o Mac:
  ```bash
  cat ~/.ssh/id_rsa.pub
  ```
- En Windows (Git Bash):
  ```bash
  cat ~/.ssh/id_rsa.pub
  ```
- Copia todo el texto que aparece.

## 6. Agrega la llave a tu cuenta de GitHub
1. Entra a GitHub y ve a: **Settings > SSH and GPG keys**.
2. Haz clic en **New SSH key**.
3. Pega la llave pública que copiaste.
4. Ponle un nombre (por ejemplo, el nombre de tu computador).

## 7. Usa la conexión SSH en tus repositorios
- Si ya tienes un repositorio descargado, cambia la URL remota de HTTP a SSH.
- Si vas a clonar uno nuevo, en GitHub selecciona la opción SSH y usa esa URL para clonar.
