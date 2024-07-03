# This is my first project, it's a password generator.

When you click the "Gerar Senha" button (in English: Generate Password), it will generate a password with numbers and letters based on the number of characters you want.


### Explaining the password generator
The function that creates the random password is made using a string outside the function which has every character of the alphabet and numbers, called charset. Inside the function, a string variable called pass will receive the character at the specified index of charset.

```
 function criarSenha(){
    
    let pass = "";

    for(let i = 0, n = charset.length; i < sliderElement.value; ++i){
    pass += charset.charAt(Math.floor(Math.random() * n));
    }

    containerPassword.classList.remove('hide');
    password.innerHTML = pass;
    novaSenha = pass;
}
```
Using the Math library in JS, the Math.random method will return a number between 0 and 1, which is then multiplied by the variable n (which holds the length of charset). The Math.floor method will return this multiplication as an integer, providing a specified index that is concatenated in the variable pass.


### Explaining how copying works
```
function copiarSenha(){
    alert('Senha copiada com sucesso');
    navigator.clipboard.writeText(novaSenha);
}
```

In this function, we use a Web API called Clipboard API (typically used in JavaScript) to copy the text in the variable novaSenha to the system clipboard.

### Credits and final considerations
In this project, I applied some basic concepts about JS and CSS to increase my knowledge. This is not an original project; it is a project created by the YouTuber Sujeito Programador.