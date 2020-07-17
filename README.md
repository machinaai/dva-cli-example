# dva-cli-example

Un ejemplo de ejecución de la página de inicio de [dva-cli] (https://github.com/dvajs/dva-cli) 0.8.0

Por favor refiérase a la [documentación](https://github.com/ant-motion/dva-cli-example/blob/2.0/src/routes/Home/documentation.md)

### 2.0 Cambios

2.0 Los cambios aquí se basan en los cambios en el andamio dva 2.x. Si no es el andamio dva-cli, elimine el código relacionado con mostrar en index.js:

1. stage interior [show](https://github.com/machinaai/dva-cli-example/blob/2.0/src/routes/Home/index.jsx#L20);
2. didMount interior [if](https://github.com/machinaai/dva-cli-example/blob/2.0/src/routes/Home/index.jsx#L29-L37)
```jsx
    // dva 2.0 El estilo se carga dinámicamente después de renderizar el componente, lo que hace que el componente de desplazamiento no surta efecto; no se verá afectado en línea;
    if (location.port) {
      // El tiempo de construcción del estilo es de entre 200 y 300 ms;
      setTimeout(() => {
        this.setState({
          show: true,
        });
      }, 500);
    }
```

3. return ev [El manejo de children](https://github.com/machinaai/dva-cli-example/blob/2.0/src/routes/Home/index.jsx#L64), Reemplazar con `{children}`

0.7.8 Ejemplo, vuelva a cambiar [master](https://github.com/machinaai/dva-cli-example/tree/master)

