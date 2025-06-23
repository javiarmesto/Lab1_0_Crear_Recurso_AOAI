# Guía Paso a Paso: Crear un Recurso de Azure OpenAI y Desplegar un Modelo

Esta guía está pensada para ayudarte, aunque no tengas experiencia técnica, a crear un recurso de Azure OpenAI y a desplegar tu primer modelo. Usaremos el portal web de Azure, pero al final te mostraré otras formas alternativas para hacer el proceso.

---

## ¿Qué es Azure OpenAI?

Azure OpenAI te permite usar la inteligencia artificial avanzada de OpenAI (como GPT o DALL·E) desde la nube de Microsoft Azure. Así puedes aprovechar el poder de los modelos de IA sin tener que ser experto en programación.

---

## Paso 1: Acceder al Portal de Azure

1. Abre tu navegador web y ve a [https://portal.azure.com](https://portal.azure.com).
2. Inicia sesión con tu cuenta de Microsoft. Si no tienes una, puedes crearla gratis.

---

## Paso 2: Crear un Recurso de Azure OpenAI

1. En el menú de la izquierda, haz clic en "**Crear un recurso**".
2. Escribe `Azure OpenAI` en la barra de búsqueda y selecciona **Azure OpenAI**.
3. Haz clic en "**Crear**".

### Rellena el formulario:

- **Suscripción**: Elige tu suscripción de Azure.
- **Grupo de recursos**: Puedes crear uno nuevo, por ejemplo: `OpenAIGrupo`.
- **Nombre del recurso**: Ponle un nombre fácil de recordar, como `mi-openai`.
- **Región**: Selecciona la región más cercana a ti (por ejemplo, `West Europe`).
- **Plan de tarifa**: Elige según tus necesidades; para comenzar suele estar bien la opción predeterminada.
- **Aceptar términos**: Marca la casilla de aceptación.

4. Haz clic en "**Revisar + crear**" y luego en "**Crear**".
5. Espera a que se complete la creación y haz clic en "**Ir al recurso**".

---

## Paso 3: Desplegar un Modelo (Deployment)

1. Dentro de tu recurso recién creado, en el menú de la izquierda, haz clic en "**Model deployments**" (Despliegues de modelos).
2. Haz clic en "**+ Create**" (Crear).

### Completa los datos del despliegue:

- **Model**: Elige el modelo que deseas usar (por ejemplo, `gpt-35-turbo` o el que esté disponible).
- **Nombre del deployment**: Ponle un nombre sencillo, como `mi-gpt-deployment`.
- **Version**: Elige la versión por defecto o la recomendada.
- **Configuración adicional**: Generalmente puedes dejar los valores por defecto.

3. Haz clic en "**Create**" (Crear).

¡Listo! Ahora tienes un modelo de OpenAI desplegado en Azure.

---

## Otras Opciones para Crear Recursos y Desplegar Modelos

### 1. Usando la Extensión de VS Code

- Instala [Visual Studio Code](https://code.visualstudio.com/) en tu computadora.
- Agrega la extensión "**Azure OpenAI**" desde el marketplace de extensiones.
- Inicia sesión con tu cuenta de Azure.
- Usa la extensión para crear recursos y despliegues desde una interfaz gráfica amigable, similar al portal web.

### 2. Usando la Línea de Comandos (Azure CLI)

Si te animas a probar una forma más técnica:

1. Instala [Azure CLI](https://docs.microsoft.com/es-es/cli/azure/install-azure-cli).
2. Abre una terminal y ejecuta:
   ```sh
   az login
   ```
3. Para crear un recurso de Azure OpenAI:
   ```sh
   az cognitiveservices account create \
     --name mi-openai \
     --resource-group OpenAIGrupo \
     --kind OpenAI \
     --location westeurope \
     --sku S0
   ```
4. Para desplegar un modelo, puedes usar comandos adicionales desde la documentación oficial.

---

## Recursos Útiles

- [Documentación oficial de Azure OpenAI (Microsoft)](https://learn.microsoft.com/es-es/azure/ai-services/openai/)
- [Preguntas frecuentes sobre Azure OpenAI](https://learn.microsoft.com/es-es/azure/ai-services/openai/faq)
- [Crear y administrar recursos en Azure](https://learn.microsoft.com/es-es/azure/azure-portal/azure-portal-overview)

---

### ¡Enhorabuena!  
Ahora sabes cómo crear tu propio recurso de Azure OpenAI y desplegar un modelo de IA, incluso si nunca lo habías hecho antes. Si tienes dudas, consulta los enlaces de ayuda o contacta con soporte de Azure.
