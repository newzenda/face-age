# Face-Age
_Age verification powered by AI_  

Face-Age es una aplicación web desarrollada por **Newzenda** que permite a cualquier software externo verificar de forma automática la edad aproximada de una persona antes de concederle acceso a contenidos restringidos (por ejemplo: sitios para adultos, apuestas, lenguaje explícito, consumo de sustancias, etc.).  
La verificación se realiza mediante una red neuronal de **inteligencia artificial** que estima la edad a partir de los rasgos faciales del usuario.

---

## ✨ Características principales
- **Verificación por IA**: estima la edad de una persona a partir de una captura facial en tiempo real o imagen enviada.
- **Integración sencilla**: cualquier aplicación o sitio puede invocar Face-Age mediante una URL con parámetros.
- **Compatibilidad internacional**: el límite de edad es configurable según las leyes o políticas de cada país o servicio.
- **Redirección automática**: tras la verificación, el sistema responde a una URI de retorno para autorizar o denegar el acceso.
- **No almacenamiento de datos**: Face-Age no almacena ningún dato.  Solamente se centra en evaluar si la persona aparenta determinada edad y entregar el flujo al sitio externo según sea el caso.

---

## 🚀 Uso directo desde GitHub Pages
El repositorio puede ejecutarse sin instalación utilizando **GitHub Pages**.

1. Visita la página pública del proyecto:  https://unix4you2.github.io/face-age/

2. Invoca la aplicación enviando los siguientes **parámetros GET** en la URL:

- **limit**: Edad mínima (entero) requerida para aprobar.  
- **success**: URI de redirección si la verificación aprueba.  
- **failure**: URI de redirección si la verificación no aprueba.

**Ejemplo de uso**  

https://unix4you2.github.io/face-age/?limit=18&success=https://midominio.com/acceso&failure=https://midominio.com/denegado


3. El sistema solicitará al usuario activar su cámara, estimará su edad y:
- Mostrará el resultado en pantalla.
- Redireccionará a la URL indicada en `success` o `failure` según el caso.

---

## ⚡ Integración en otros proyectos
- **Front-end externo**: solo necesitas construir la URL con los parámetros `limit`, `success` y `failure`.
- **Respuesta automática**: el sistema retorna un objeto JSON a la URI de redirección para que tu backend pueda registrar el evento (opcional).
- **Seguridad**: se recomienda usar HTTPS en las URLs de retorno.

---

## 📦 Instalación
Esta aplicación está diseñada para NO requerir instalar nada del lado de la apliación o sitio externo que quiere hacer uso de la verificación así como ninguna instalación del lado del usuario final.

## 📜 Licencia

Este proyecto se distribuye bajo la licencia MIT con cláusula de notificación a usuarios.
Cualquier implementación que ponga Face-Age a disposición de usuarios finales debe informar de manera clara que el sistema utiliza Face-Age de Newzenda.
Consulta el archivo LICENSE para más detalles.

## 💡 Nota legal

Face-Age entrega una estimación estadística de edad. No constituye prueba legal ni reemplaza los mecanismos de verificación exigidos por las autoridades.
El responsable del sitio o servicio que integre Face-Age es quien debe cumplir la normativa de protección de datos y privacidad aplicable.
