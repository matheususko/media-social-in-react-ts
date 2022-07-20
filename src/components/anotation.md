# key no React

## Por que única?

3 momentos em que um componente é renderizado novamento no React.

1.  Quando o estado é alterado;
2.  Quando a propriedade altera;
3.  Quando um componente pai renderiza novamente.
---
1, 2, 3, 4
--- 
1, 2, 3, 4, 5

## Por que não posso usar o índice do array?

```js
const posts = [1, 2, 5, 4, 3]
//0, 1, 2, 3, 4
```
## Closures no React

```js
function Comment(props) {
    connst [likes, setLikes] = useState(0)

    funtion addLike() {
        setLikes(likes+1);
    }
}

Comment(props, 1)
```

## O que é typescript?
 1. nasceu como um super set (conjunto ferramental), em cima da linguagem javascript, para você conseguir adicionar tipagem estática em cima de uma linguagem como o js, que tem tipagem dinâmica. " - Typescript trás inteligencia para nosso código".

Tipagem dinâmica:
    - javascript não reclama se declararmos alguma propriedade errada.
    - só iremos ver o erro no console ou quando executarmos em alguma execução.
---
```js
function sumAge(users) {
    const sum = 0;

    for (const user of users) {
        sum += user.age;
    }

    return sum
}

sumAge('teste')
```

Tipagem estática:
    - em tsx posso criar tipagem para determinar o que cada propriedade ou paramentro pode esperar de type data.
    - funcionamento interno do tsx : inferencia de tipo.
```js
    interface User {
        name: string;
        bio: string;
        age: number;
    }

    function sumAge(users: User[]) {
        const sum = 0;

        for (const user of users) {
            sum += user.age;
        }

        return sum
    }

    const sumOfAllUserAges = sumAge([
        {
            name: 'Matheus';
            bio: 'Programador';
            age: '22';
        }
    ])
```