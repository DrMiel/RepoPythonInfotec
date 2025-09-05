# Sistema de Login Moderno con Flask

Este proyecto es una aplicación web minimalista de inicio de sesión (login) desarrollada con **Flask**. Está diseñada para ser clara, moderna y fácil de entender, ideal para aprendizaje o como base para proyectos más grandes.

## Características principales

- **Autenticación en memoria:** Los usuarios y contraseñas están definidos en el código, no se usa base de datos.
- **Interfaz moderna:** UI responsiva, con modo oscuro y efectos visuales atractivos (Glassmorphism, gradientes, animaciones).
- **Gestión de sesión:** Al iniciar sesión, se almacena el usuario en la sesión de Flask.
- **Mensajes flash:** Notificaciones para éxito, error y cierre de sesión.
- **Cache busting:** Los archivos estáticos (CSS, imágenes) se actualizan automáticamente en el navegador cuando cambian.
- **Código y comentarios en español.**

## Estructura del proyecto

```
RepoPythonInfotec/
│
├── app.py                # Código principal de la app Flask (rutas, lógica, usuarios)
├── requirements.txt      # Dependencias (solo Flask)
├── static/
│   ├── style.css         # Estilos modernos y modo oscuro
│   └── bg-highres.svg    # Imagen de fondo
├── templates/
│   ├── login.html        # Página de inicio de sesión
│   └── welcome.html      # Página de bienvenida tras login
├── README.md             # (Este archivo)
└── ...
```

## ¿Cómo funciona?

1. **Inicio:**
	- Accede a `/` y verás el formulario de login.
	- Ingresa uno de los usuarios definidos en `app.py` (ver más abajo).
2. **Validación:**
	- Si los datos son correctos, se guarda el usuario en la sesión y se redirige a `/welcome`.
	- Si son incorrectos, aparece un mensaje de error.
3. **Bienvenida:**
	- En `/welcome` se muestra el nombre del usuario y un botón para cerrar sesión.
4. **Cerrar sesión:**
	- Al hacer logout, se limpia la sesión y se muestra un mensaje de despedida.

## Usuarios de prueba

Puedes iniciar sesión con cualquiera de estos usuarios:

| Correo             | Contraseña  | Nombre         |
|--------------------|-------------|---------------|
| admin@test.com     | admin123    | Administrador |
| user@test.com      | user123     | Usuario       |
| demo@demo.com      | demo        | Demo User     |

## Instalación y uso

1. **Clona el repositorio:**
	```
	git clone <url-del-repo>
	cd RepoPythonInfotec
	```
2. **Instala dependencias:**
	```
	pip install -r requirements.txt
	```
3. **Ejecuta la app:**
	```
	python app.py
	```
4. **Abre en tu navegador:**
	[http://localhost:5000](http://localhost:5000)

## Personalización

- **Agregar usuarios:** Edita el diccionario `USERS` en `app.py`.
- **Cambiar estilos:** Modifica `static/style.css`.
- **Editar textos:** Cambia los templates en `templates/`.

## Seguridad

- Este proyecto es solo para fines educativos o prototipos. No almacena contraseñas de forma segura ni implementa buenas prácticas de producción.
- La clave secreta está hardcodeada y los usuarios están en texto plano.

## Créditos y referencias

- Basado en [Flask](https://flask.palletsprojects.com/)
- Iconos: [FontAwesome](https://fontawesome.com/)
- Tipografía: [Google Fonts - Playfair Display](https://fonts.google.com/specimen/Playfair+Display)

---
*Desarrollado para iNFOTEC 1. Actualiza este README si agregas nuevas funciones.*
