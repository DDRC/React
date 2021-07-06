# Conceptos obtenidos del modulo 'star match game'

Los conceptos aprendidos listan a continuacion dentro de cada capitulo del modulo

*  *[React]( #react)*
    - [componentes flexibles](#componentes-flexibles)
    - [extraccion de componentes](#componentes-modulares)
    - [palabra clave key](#palabra-reservada-key)
    - [tip 1](#tip-1)
*  *[Componentes y hooks](#componentes-y-hooks)*
    - [useState](#usestate)
    - [useEffect](#userffect)
    - [useContext](#usecontext)
    - [useReducer](#usereducer)
    - [useRef]()
*  *[Virtual DOM](#virtual-dom)*
*  *[React-DOM](#react-dom)*
*  *[Metodo: render()](#método-render)*
*  *[¿QUE ES JSX?](#qué-es-jsx)*


# React

>React es una libreria de javascript, enfocada en el desarrollo de interfaces


## _Recomendaciones generales_

### Componentes flexibles

Al igual que otros lenguajes React puede valerse de otros lenguajes para conseguir interfaces mas interacticas

### Componentes modulares

Es preciso diferenciar los componentes que pueden tener mas de un uso, ya que podemos separarlos en un archivos para usarlos las veces que necesitemos.

### Palabra Reservada Key

Esta palabra trabajo de manera similar a un Id de html, etiqutando a cada componente para que sea unico.
> ### tip 1: 
>intente usar siempre funciones de areglos para recorrerlos (como map, filter,reduce, ect.), en vez de usar bucles como for, while, do while.  

# Componentes y hooks
Los componentes son piezas de codigo que se renderizan y representan las interfaces de usuario; ademas estan puedn estar escritas en forma de funcion o clase.

Los Hooks son funciones que te permiten “enganchar” el estado de React y el ciclo de vida desde componentes de función. Los hooks no funcionan dentro de las clases — te permiten usar React sin clases. (No recomendamos reescribir tus componentes existentes de la noche a la mañana, pero puedes comenzar a usar Hooks en los nuevos si quieres).
### useState()
Se usa para cambiar el valor(estado) de una variable
```javascript
function ExampleWithManyStates() {
  // Declarar múltiple variables de estado!
  const [age, setAge] = useState(42);
  const [fruit, setFruit] = useState('banana');
  const [todos, setTodos] = useState([{ text: 'Learn Hooks' }]);
  // ...
}
```
### useEffect()
Es probable que hayas realizado recuperación de datos, suscripciones o modificación manual del DOM desde los componentes de React. Llamamos a estas operaciones “efectos secundarios” (o “efectos” para abreviar) porque pueden afectar a otros componentes y no se pueden hacer durante el renderizado.

El Hook de efecto, useEffect, agrega la capacidad de realizar efectos secundarios desde un componente de función. Tiene el mismo propósito que componentDidMount,componentDidUpdate y componentWillUnmount en las clases React, pero unificadas en una sola API. (Mostraremos ejemplos comparando useEffect con estos métodos en Usando el Hook de efecto).
```javascript
// Similar a componentDidMount y componentDidUpdate:
  useEffect(() => {
    // Actualiza el título del documento usando la Browser API
    document.title = `You clicked ${count} times`;
  });
}
```
### useContext()
useContext te permite suscribirte al contexto React sin introducir el anidamiento:
```javascript
function Example() {
  const locale = useContext(LocaleContext);
  const theme = useContext(ThemeContext);
  // ...
}
}
```

### useReducer()
useReducer te permite manejar el estado local de componentes complejos con un reducer:
```javascript
function Todos() {
  const [todos, dispatch] = useReducer(todosReducer);
  // ...
```
### useRef()
useRef sirve para un par de propósitos principales:

* Acceder a elementos DOM

* Conservar los valores en sucesivas representaciones
```javascript
function TextInputWithFocusButton() {
 const inputEl = useRef(null);
 const onButtonClick = () => {
   // `current` apunta al elemento de entrada de texto montado
   inputEl.current.focus();
 };
 return (
   <>
     <input ref={inputEl} type="text" />
     <button onClick={onButtonClick}>Focus the input</button>
   </>
 );
}
```
## Virtual DOM
Es una representacio real del DOM del navegador, la cual actua comointermediario entre la interfaz de usuario y la aplicación.

## React-DOM
Es una libreria de javascript que trabaja en conjunto con react para renderizar contenido en el navegador.

```javascript
   import ReactDOM from 'react-dom'
```

## Método render
Renderiza un elemento React al DOM en el contenedor suministrado y retorna una referencia al componente (o devuelve null para componentes sin estado).

```javascript
   ReactDOM.render(<App />, document.getElementById('app'));
```
## QUÉ ES JSX
Se llama JSX, y es una extensión de la sintaxis de JavaScript

```javascript
const element = <h1>Hello, world!</h1>;
```

