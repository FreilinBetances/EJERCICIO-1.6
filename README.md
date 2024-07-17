# EJERCICIO-1.6
Claro, aquí tienes una descripción del ejercicio 1.6 en un archivo README para tu proyecto de GitHub:

```markdown
# Unicafe Feedback Application

## Descripción

Este proyecto es una aplicación web simple para recopilar comentarios de los clientes de Unicafe. La aplicación permite a los usuarios dar su opinión en tres categorías: bueno, neutral y malo. El objetivo del ejercicio es implementar la funcionalidad básica de recolección y visualización de comentarios utilizando React.

## Estructura del Proyecto

El proyecto está basado en `create-react-app` para facilitar la configuración y el desarrollo. Contiene los siguientes archivos y directorios principales:

- `src/App.jsx`: Contiene el componente principal de la aplicación, que maneja el estado y la lógica de los comentarios.
- `src/index.js`: Punto de entrada de la aplicación React.
- Otros archivos y directorios generados por `create-react-app`.

## Instrucciones

1. **Instalación**
   
   Clona el repositorio e instala las dependencias necesarias:
   ```sh
   git clone https://github.com/tu-usuario/unicafe-feedback.git
   cd unicafe-feedback
   npm install
   ```

2. **Ejecutar la Aplicación**
   
   Inicia la aplicación en modo de desarrollo:
   ```sh
   npm start
   ```

   Abre [http://localhost:3000](http://localhost:3000) para ver la aplicación en tu navegador.

3. **Estructura del Código**
   
   - `App.jsx`: 
     ```jsx
     import { useState } from 'react';

     const App = () => {
       const [good, setGood] = useState(0);
       const [neutral, setNeutral] = useState(0);
       const [bad, setBad] = useState(0);

       const handleGoodClick = () => setGood(good + 1);
       const handleNeutralClick = () => setNeutral(neutral + 1);
       const handleBadClick = () => setBad(bad + 1);

       return (
         <div>
           <h1>Give feedback</h1>
           <button onClick={handleGoodClick}>good</button>
           <button onClick={handleNeutralClick}>neutral</button>
           <button onClick={handleBadClick}>bad</button>
           <h2>Statistics</h2>
           <p>good: {good}</p>
           <p>neutral: {neutral}</p>
           <p>bad: {bad}</p>
         </div>
       );
     };

     export default App;
     ```

   - `index.js`:
     ```jsx
     import React from 'react';
     import ReactDOM from 'react-dom/client';
     import './index.css';
     import App from './App';

     const root = ReactDOM.createRoot(document.getElementById('root'));
     root.render(
       <React.StrictMode>
         <App />
       </React.StrictMode>
     );
     ```

## Notas

- La aplicación solo almacena los comentarios durante la sesión actual del navegador. Una vez que se actualiza la página, los comentarios recopilados se reinician.
- Este proyecto es parte de los ejercicios del curso de Fullstack Open.

## Contribución

Si deseas contribuir a este proyecto, por favor, crea una bifurcación del repositorio, realiza tus cambios y abre una solicitud de extracción.



