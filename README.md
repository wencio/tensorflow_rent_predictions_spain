# Red Neuronal Pisos de Alquiler Spain

Este proyecto utiliza una red neuronal entrenada para predecir el precio de alquiler de pisos en España. La interfaz web permite al usuario ingresar características del piso y obtener una estimación del precio de alquiler utilizando TensorFlow.js.

## Contenido del Proyecto

- `index.html`: La interfaz web que permite a los usuarios ingresar las características del piso y ver el precio estimado.
- `model.json`: El modelo de TensorFlow.js que contiene la red neuronal entrenada.
- `redNeuronal.py`: (Descripción de lo que hace este archivo, si es necesario)

## Requisitos

- Navegador web moderno (Chrome, Firefox, Edge, etc.)
- Conexión a internet (para cargar TensorFlow.js desde CDN)

## Configuración y Ejecución

Sigue estos pasos para configurar y ejecutar el proyecto:

1. Clona el repositorio en tu máquina local:

    ```sh
    git clone https://github.com/wencio/tensorflow_rent_predictions_spain
    ```

2. Navega al directorio del proyecto:

    ```sh
    cd tensorflow_rent_predictions_spain
    ```

3. Abre el archivo `index.html` en tu navegador web. Puedes hacerlo simplemente arrastrando el archivo a una ventana de tu navegador o abriéndolo directamente desde el navegador.

4. En la interfaz web, ingresa las características del piso:
    - Metros cuadrados (M²)
    - Número de habitaciones
    - Número de planta
    - Ascensor (Sí/No)
    - Exterior (Sí/No)
    - Estado (No rehabilitado, Rehabilitado, Nuevo)
    - Céntrico (Sí/No)

5. Haz clic en el botón "Calcular precio" para obtener el precio estimado del alquiler.

## Estructura del Proyecto

- **HTML y Bootstrap**: La interfaz de usuario está construida con HTML y Bootstrap para un diseño responsive y fácil de usar.
- **TensorFlow.js**: Se utiliza TensorFlow.js para cargar y ejecutar el modelo de red neuronal en el navegador.

## Código Principal

### Cargar el Modelo

El siguiente código en `index.html` carga el modelo de TensorFlow.js:

```javascript
(async() =>{
    console.log("Cargando el modelo...");
    modelo = await tf.loadLayersModel("model.json");
    console.log("Modelo cargado!");
})();
