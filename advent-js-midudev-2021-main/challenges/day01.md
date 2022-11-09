# Día 1 - Contando ovejas para dormir 

> Con la emoción de que llega la navidad, nos está costando dormir bastante últimamente. Vamos a intentar usar este pequeño truco que nos ayudará a dormir más rápido 🐑.

Dificultad: Fácil

## Enunciado

Considera una lista/array de ovejas. Cada oveja tiene un nombre y un color. Haz una función que devuelva una lista con todas las ovejas que sean de color `rojo` **y que además** su nombre contenga tanto las letras `n` Y `a`, sin importar el orden, las mayúsculas o espacios.

Por ejemplo, si tenemos las ovejas:

```js
const ovejas = [
  { name: 'Noa', color: 'azul' },
  { name: 'Euge', color: 'rojo' },
  { name: 'Navidad', color: 'rojo' },
  { name: 'Ki Na Ma', color: 'rojo'},
  { name: 'AAAAAaaaaa', color: 'rojo' },
  { name: 'Nnnnnnnn', color: 'rojo'}
]
```

Al ejecutar el método debería devolver lo siguiente:

```js
const ovejasFiltradas = contarOvejas(ovejas)

console.log(ovejasFiltradas)

// [{ name: 'Navidad', color: 'rojo' },
//  { name: 'Ki Na Ma', color: 'rojo' }]
```

Recuerda. **Debe contener las dos letras 'a' y 'n' en el nombre**. No cuentes ovejas que sólo tenga una de las letras, debe tener ambas.

## Solución

```js
function contarOvejas(ovejas) {
  return ovejas.filter(
    ({ name, color }) => color === 'rojo' && /^(?=.*a)(?=.*n).*$/gi.test(name)
  );
}
```

## Referencias

| Command | Source |
| --- | --- |
| Organizar la información en tablas | [docs.github.com](https://docs.github.com/es/get-started/writing-on-github/working-with-advanced-formatting/organizing-information-with-tables) |
| Expresiones regulares | [developer.mozilla.org](https://developer.mozilla.org/es/docs/Web/JavaScript/Guide/Regular_Expressions) |
| | [w3schools.com](https://www.w3schools.com/js/js_regexp.asp) |
| | [eloquentjavascript.net](https://eloquentjavascript.net/09_regexp.html) |
| | [regxr](https://regexr.com) |
| | [How to Use Regular Expressions in JavaScript – Tutorial for Beginners](https://www.freecodecamp.org/news/regular-expressions-for-beginners) |
