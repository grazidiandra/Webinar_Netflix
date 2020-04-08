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
  <link rel="stylesheet" type="text/css" href="style.css" />
  <title>NETFLIX CLONE</title>
</head>

</html>
```

**IMPORTANTE!**

Antes de continuar, abra o navegador, clique em arquivo -> abrir e escolha o arquivo index.html que você criou e que esta no diretório netflix no seu desktop.
Lembre-se de validar as alteraçōes voltando para a janela do navegador e recarregando a página.


Como pode-se notar, neste ponto já temos uma página mas, com pouca ou nenhuma apresentação.

### Folhas de estilo/CSS

1. Vamos colocar a folha de estilo que irá deixar a aparência da página de login de acordo com nossa referência. Para fazer isso, edite o arquivo style.css e coloque todo o conteúdo abaixo:

```
body {
  padding: 0;
  margin: 0;
  color: white;
  font-family: Helvetica;
}

```
2. Agora que já temos nosso arquivo de estilo, vamos dizer que nosso HTML deve utilizá-lo. Para isso, basta acrescentar mais uma linha no head conforme indicação abaixo:

```html
<link rel="stylesheet" type="text/css" href="style.css" />
```

3. Agora volte no navegador e atualize a página!
