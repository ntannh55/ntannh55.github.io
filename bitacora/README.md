# Bitácora de Jornada

Registro diario de actividades (7:00 a.m. – 9:00 p.m.) con cronómetro, categorías y análisis de productividad por día, semana, mes, trimestre, semestre, año o rango personalizado.

## Cómo funciona el acceso

- La app es pública, pero **no contiene datos personales**.
- Los registros se guardan en un **repositorio privado** de GitHub (por ejemplo `usuario/bitacora-datos`), en archivos `data/AAAA-MM.json` y `data/categorias.json`.
- Para leer y escribir ese repositorio se usa un *token* de GitHub con permiso solo sobre él. El token se guarda **cifrado** (AES-GCM, clave derivada con PBKDF2-SHA256, 600 000 iteraciones) en `auth.json`. Solo se descifra en el navegador con la contraseña del usuario.
- Usa una contraseña fuerte (12 caracteres o más).

## Configuración inicial

1. Crea un repositorio **privado** para los datos.
2. Crea un token *fine-grained* en GitHub → Settings → Developer settings → Personal access tokens → Fine-grained tokens:
   - Repository access: *Only select repositories* → el repositorio de datos.
   - Permissions → Repository permissions → **Contents: Read and write**.
3. Abre la app → «Configurar acceso por primera vez» → correo, repositorio, token y contraseña.
4. Copia el código de acceso generado y guárdalo como `auth.json` en esta carpeta.
