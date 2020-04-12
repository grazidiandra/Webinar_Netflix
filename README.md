![Iron Hack](https://raw.githubusercontent.com/grazidiandra/netflix_workshop/master/images/ih.png)

# Netflix Login by Ironhack

O objetivo deste tutorial é montar a página de login do Netflix para passar os conceitos básicos do HTML e CSS.

### Configurando o ambiente

Recomendamos a utilização do editor [Visual Studio Code](https://code.visualstudio.com/Download) para fazer esse exercício porém, qualquer editor pode ser utilizado.

Vamos começar montando o esquelto da nossa página:

1. Crie um diretório com o nome netflix no seu desktop;

2. Dentro desse diretório, crie 2 arquivos (index.html e style.css) e um diretório (images);

3. Clique com o botão direito do mouse nas imagens abaixo, escolha a opção "Salvar imagem como..." e grave as imagens dentro do diretório images do seu projeto com os seguintes nomes:

logo.png

![logo](https://raw.githubusercontent.com/grazidiandra/netflix_workshop/master/images/logo.png)

background.jpg

![background](https://raw.githubusercontent.com/grazidiandra/netflix_workshop/master/images/background.jpg)

logoFace.png

![facebook](https://raw.githubusercontent.com/grazidiandra/netflix_workshop/master/images/logoFace.png)

4. Agora vamos pegar o código abaixo e colocar no arquivo index.html que está na raiz do nosso projeto

```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
 <!-- <link rel="stylesheet" type="text/css" href="style.css" /> -->
  <title>NETFLIX CLONE</title>
</head>
<body>
  <main class="login">
    <div class="login__background-image"></div>
    <nav class="login__nav">
      <img class="login__logo" src="./images/logo.png" alt="logo">
    </nav>
    <section class="login__form-container">
      <div class="login__form">
        <form>
          <h1 class="form__title">Entrar</h1>
          <input class="form__input" type="text" placeholder="Email ou número de telefone">
          <input class="form__input" type="text" placeholder="Senha">
          <button class="form__button"> Entrar</button>
        </form>
        <div class="form__links">
          <span class="form__checkbox">
            <input class="form__checkbox_input" type="checkbox"> 
            <label>Lembre-se de mim</label>
          </span>
          <span>
            <a href="#">Precisa de ajuda?</a>
          </span>
        </div>
        <div class="form__info">
          <span class="form__info-facebook">
            <img src="./images/logoFace.png" alt="facebook">
            <a class="form__info-link" href="">Conectar com facebook</a>
          </span>
          <p class="form__info-signup">Novo por aqui? <a href="#">Assine agora</a>.</p>
          <p class="form__info-secure">Esta página é protegida pelo Google reCAPTCHA para garantir que você não é um robô.<a href="#">Saiba mais</a>.</p>
        </div>
      </div>
    </section>
  </main>
</body>
</html>
```

**IMPORTANTE!**

Antes de continuar, abra o navegador, clique em arquivo -> abrir e escolha o arquivo index.html que você criou e que esta no diretório netflix no seu desktop.
Lembre-se de validar as alteraçōes voltando para a janela do navegador e recarregando a página.


Como pode-se notar, neste ponto já temos uma página mas, com pouca ou nenhuma apresentação.

### Folhas de estilo/CSS

1. Vamos colocar a folha de estilo que irá deixar a aparência da página de login de acordo com nossa referência. Para fazer isso, edite o arquivo style.css e coloque todo o conteúdo abaixo:

```
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
  font-family: Helvetica;
}

.login {
  height: 100vh;
  background-color: black;
  position: relative;
  z-index: 0;
}

.login__background-image {
  position: absolute;
  opacity: 0.5;
  z-index: -1;
  height: 100vh;
  width: 100%;
  background-image: url("./images/background.jpg");
}

.login__nav {
  height: 90px;
  margin-bottom: 10px;
}

.login__logo {
  width: 190px;
  margin-left: 30px;
}

.login__form-container {
  display: flex;
  justify-content: center;
  align-items: center;
}

.login__form {
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: flex-start;
  background-color: rgba(0,0,0,0.75);
  width: 450px;
  height: 650px;
  padding: 60px 68px 40px 68px;
  box-sizing: border-box;
  border-radius: 4px;
}

.form__title {
  color: #fff;
  font-weight: bold;
  margin-bottom: 28px;
  font-size: 32px;
}

.form__input {
  box-sizing: border-box;
  background-color: #333;
  border-radius: 4px;
  border: 0;
  color: #fff;
  height: 50px;
  line-height: 50px;
  padding: 0px 20px 0;
  width:100%;
  margin-bottom: 16px;
}

.form__input::placeholder {
  font-size: 16px;
  color: #8c8c8c;
}


.form__button {
  background-color: #E50914;
  height: 48px;
  border: 0;
  border-radius: 4px;
  width: 100%;
  font-size: 16px;
  font-weight: bold;
  margin: 24px 0 12px;
  color: #fff;
  cursor: pointer;
}

.form__links {
  color: #b3b3b3;
  width: 100%;
  display: flex;
  justify-content: space-between;
  font-size: 13px;
  margin-bottom: 50px;
}

.form__checkbox {
  display: flex;
  align-items: flex-start;
  height: 20px;
}

.form__checkbox_input {
  width: 20px;
  height: 20px;
}

.form__links a {
  color: #b3b3b3;
  text-decoration: none;
}

.form__links a:hover{
  text-decoration: underline;
}

.form__info {
  color: #737373;
}

.form__info-facebook {
  display: flex;
  align-items: center;
}

.form__info-facebook img {
  width: 20px;
  margin-right: 5px;
}

.form__info-link {
  text-decoration: none;
  color: #737373;
  font-size: 13px;
}

.form__info-signup {
  color: #737373;
  font-size: 16px;
  margin-top: 16px;
  margin-bottom: 11px;
}

.form__info-signup a{
  color: white;
  text-decoration: none;
}

.form__info-signup a:hover{
  text-decoration: underline;
}

.form__info-secure {
  color: #737373;
  font-size: 13px;
}

.form__info-secure a {
  color: #0071eb;
  text-decoration: none;
}

.form__info-secure a:hover{
  text-decoration: underline;
}
```
2. Agora que já temos nosso arquivo de estilo, vamos dizer que nosso HTML deve utilizá-lo. Para isso, basta descomentar a linha no head indicada abaixo:

```html
<link rel="stylesheet" type="text/css" href="style.css" />
```

3. Agora volte no navegador e atualize a página!
