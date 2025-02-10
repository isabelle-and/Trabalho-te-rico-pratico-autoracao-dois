# Trabalho-te-rico-pratico-autoracao-dois
[TRABALHO 01] Trabalho Teórico-Prático de HTML5, CSS e JavaScript
# questão 1
### Estrutura Básica do HTML5:
```html
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <title>Minha Página Inicial</title>
</head>
<body>
    <h1>Minha Página Inicial</h1>
    <p>Este é um parágrafo.</p>
    <a href="https://www.example.com">Link para outra página</a>
</body>
</html>
```

### `<!DOCTYPE html>`:
Define o tipo de documento como HTML5, garantindo que o navegador interprete o código corretamente.

### `<html lang="pt-br">`:
A tag raiz do documento. O atributo `lang` define o idioma principal da página (no caso, português do Brasil).

### `<head>`:
Contém metadados sobre o documento, como codificação de caracteres, configurações de viewport e o título da página. Essas informações não são exibidas diretamente no navegador, mas são essenciais para o funcionamento e acessibilidade da página.

### `<meta charset="UTF-8">`:
Define a codificação de caracteres como UTF-8, que suporta a maioria dos caracteres especiais e idiomas.

### `<meta name="viewport" content="width=device-width, initial-scale=1.0">`:
Configura a viewport para garantir que a página seja exibida corretamente em dispositivos móveis.

### `<title>`:
Define o título da página, que aparece na aba do navegador e nos resultados de busca.

# questão 2
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <style>.bloco {
    padding: 20px;
    margin-bottom: 10px;
  }
  
  .bloco-1 {
    background-color: #f0f0f0;
    border: 1px solid #ccc;
    font-size: 16px;
  }
  
  .bloco-2 {
    background-color: #e0f0e0;
    border: 2px dashed #999;
    font-size: 18px;
  }
  
  .bloco-3 {
    background-color: #f0e0e0;
    border: 3px dotted #f00;
    font-size: 20px;
    
  }</style>
    <section id="bloco1">
        <h2>Título da Seção 1</h2>
        <p>Texto do bloco 1.</p>
    </section>
    
    <section id="bloco2">
        <h2>Título da Seção 2</h2>
        <p>Texto do bloco 2.</p>
    </section>
    
    <section id="bloco3">
        <h2>Título da Seção 3</h2>
        <p>Texto do bloco 3.</p>
    </section>
</body>
</html>
```

### Classes:
- São mais flexíveis, pois você pode aplicar a mesma classe a vários elementos.

### IDs:
- São únicos para cada elemento, o que pode ser útil para estilos muito específicos ou para manipulação com JavaScript.

### Dica:
Você pode combinar classes e IDs para ter o melhor dos dois mundos. Por exemplo, você pode usar uma classe para estilos comuns a todos os blocos e IDs para estilos específicos de cada bloco.

Com essa estrutura HTML e CSS, você terá blocos de texto semanticamente corretos e estilizados de forma diferenciada, facilitando a manutenção e a acessibilidade do seu código.

# questão 3
### Adicionar `padding-top` ao conteúdo principal:
- **Vantagem**: Garante que o conteúdo não fique escondido e é mais simples de implementar por meio do CSS.
- **Desvantagem**: O valor do `padding-top` deve ser ajustado manualmente para que fique igual à altura da barra de navegação. Além disso, para a barra ficar responsiva, é mais difícil fazer esse ajuste.

### Adicionar `margin-top` no conteúdo principal:
- **Vantagem**: Facilita a manutenção do `margin-top`, pois ele respeita a hierarquia de layout e permite separar a barra de navegação do conteúdo.
- **Desvantagem**: Precisa ser ajustado manualmente e pode causar problemas de espaçamento e margem.

### Exemplo:

```html

<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Exemplo de Barra de Navegação Fixa</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
    }

    /* Barra de navegação fixa */
    .navbar {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 60px;
      background-color: #333;
      color: white;
      display: flex;
      align-items: center;
      padding: 0 20px;
      z-index: 1000;
    }

    .navbar a {
      color: white;
      margin-right: 15px;
      text-decoration: none;
    }

    .navbar a:hover {
      text-decoration: underline;
    }

    /* Conteúdo principal */
    .main-content {
      padding-top: 60px; /* Compensa a altura da barra de navegação */
    }

    section {
      height: 100vh;
      padding: 20px;
      border-bottom: 1px solid #ddd;
    }

    /* Ajuste para âncoras */
    .section-anchor {
      scroll-margin-top: 60px; /* Ajusta a posição do scroll ao navegar para âncoras */
    }
  </style>
</head>
<body>

  <!-- Barra de navegação fixa -->
  <div class="navbar">
    <a href="#section1">Seção 1</a>
    <a href="#section2">Seção 2</a>
    <a href="#section3">Seção 3</a>
  </div>

  <!-- Conteúdo principal -->
  <div class="main-content">
    <section id="section1" class="section-anchor">
      <h2>Seção 1</h2>
      <p>Conteúdo da primeira seção. Role para baixo para ver mais.</p>
    </section>

    <section id="section2" class="section-anchor">
      <h2>Seção 2</h2>
      <p>Conteúdo da segunda seção. Continue rolando!</p>
    </section>

    <section id="section3" class="section-anchor">
      <h2>Seção 3</h2>
      <p>Conteúdo da terceira seção. Você chegou ao fim!</p>
    </section>
  </div>

</body>
</html>
```
# questão 4
## Design Responsivo Híbrido: A Chave para Evitar Conflitos

A abordagem de **Design Responsivo Híbrido** é fundamental para garantir que seu site funcione perfeitamente em todos os dispositivos, evitando conflitos e proporcionando a melhor experiência para o usuário.

### Priorizando o Mobile First

Comece sempre com o **Mobile First**, projetando a estrutura e o conteúdo do seu site para dispositivos móveis. Essa prática garante que a experiência do usuário seja otimizada para telas menores, que geralmente são o ponto de partida para a maioria dos usuários.

### Desktop First para Seções Específicas

O **Desktop First** deve ser utilizado apenas para seções específicas que exigem layouts distintos em telas maiores. Por exemplo, um menu de navegação complexo ou um layout de página com múltiplos elementos podem se beneficiar dessa abordagem.

### Media Queries: Organização é Fundamental

Utilize **Media Queries** de forma organizada para evitar sobrescrever regras de estilo desnecessariamente. Defina regras específicas para cada faixa de tamanho de tela, garantindo que o layout se adapte de forma eficiente a diferentes dispositivos.

### Código Modularizado para Facilidade

Divida seu código em blocos lógicos e reutilizáveis. Essa prática facilita a leitura, compreensão e manutenção do código, além de evitar que alterações em uma seção afetem outras partes do projeto de forma inesperada.

Ao seguir essas dicas, você estará no caminho certo para criar um site responsivo e eficiente, que oferece a melhor experiência possível para todos os usuários, independentemente do dispositivo que estejam utilizando.

### mobile first
```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mobile First</title>
</head>
<body>
    <header>
        <h1>Mobile First Layout</h1>
    </header>
    <style>
       /* Estilos padrão (Mobile First) */
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 10px;
    text-align: center;
}

.container {
    display: flex;
    flex-direction: column;
    gap: 10px;
}

.box {
    background-color: lightblue;
    padding: 20px;
    border-radius: 5px;
}

/* Ajustes para tablets */
@media (min-width: 768px) {
    .container {
        flex-direction: row;
        justify-content: space-around;
    }

    .box {
        width: 30%;
    }
}

/* Ajustes para desktops */
@media (min-width: 1024px) {
    body {
        font-size: 18px;
        padding: 20px;
    }

    .box {
        background-color: lightcoral;
        transition: background 0.3s ease-in-out;
    }

    .box:hover {
        background-color: tomato;
    }
} 
    </style>
    <main class="container">
        <section class="box">Seção 1</section>
        <section class="box">Seção 2</section>
        <section class="box">Seção 3</section>
    </main>
</body>
</html>
```

### Desktop First:
```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Desktop First</title>
    
</head>
<body>
    <header>
        <h1>Desktop First Layout</h1>
    </header>
    <style>
        /* Estilos padrão (Desktop First) */
body {
    font-family: Arial, sans-serif;
    font-size: 18px;
    margin: 0;
    padding: 20px;
    text-align: center;
}

.container {
    display: flex;
    flex-direction: row;
    justify-content: space-around;
    gap: 20px;
}

.box {
    background-color: lightcoral;
    padding: 30px;
    border-radius: 5px;
    width: 30%;
    transition: background 0.3s ease-in-out;
}

.box:hover {
    background-color: tomato;
}

/* Ajustes para tablets */
@media (max-width: 1024px) {
    body {
        font-size: 16px;
        padding: 15px;
    }

    .container {
        gap: 15px;
    }

    .box {
        padding: 20px;
        width: 40%;
    }
}

/* Ajustes para dispositivos móveis */
@media (max-width: 768px) {
    .container {
        flex-direction: column;
        gap: 10px;
    }

    .box {
        width: 100%;
    }
}

    </style>
    <main class="container">
        <section class="box">Seção 1</section>
        <section class="box">Seção 2</section>
        <section class="box">Seção 3</section>
    </main>
</body>
</html>
```
# questão 5
## Tags semânticas HTML5: acessibilidade, SEO e validação 

Tags como `<header>`, `<section>`, `<article>` e `<nav>` oferecem significado estrutural ao HTML, beneficiando tanto a acessibilidade quanto o SEO.

### Acessibilidade

Leitores de tela, navegação por teclado e outras tecnologias assistivas utilizam tags semânticas para interpretar o conteúdo, facilitando a compreensão e a navegação para usuários com deficiência.

### SEO

Mecanismos de busca como o Google utilizam tags semânticas para entender a estrutura e o tema do conteúdo, melhorando o ranqueamento e a relevância da página nos resultados de pesquisa.

### Validação

Utilizar ferramentas online (ex: Validador HTML do W3C) e extensões de navegador (ex: Accessibility Insights) para verificar a conformidade do código com os padrões WCAG e garantir boas práticas de SEO. Testes manuais com tecnologias assistivas também são recomendados.

Em resumo, o uso correto de tags semânticas resulta em aplicações web mais acessíveis, otimizadas para mecanismos de busca e com melhor experiência para todos os usuários.

# questão 6
# Criando um botão com alerta em JavaScript

Para criar um botão que, ao ser clicado, exibe um alerta no navegador com a mensagem "Olá, mundo!".

O JavaScript "amarra" o código ao botão através do evento `onclick`. 
O `onclick` é um evento que acontece quando o usuário clicar em um elemento HTML, e ao definir `botao.onclick`, está dizendo ao navegador para executar a função especificada `(function() { alert("Olá, mundo!"); })` quando o evento `onclick` acontecer no botão.

## Código HTML

```html
<!DOCTYPE html>
<html>
<head>
  <title>Exemplo de Botão com Alerta</title>
</head>
<body>
  <button id="meuBotao">Clique aqui</button>

  <script>
    const botao = document.getElementById("meuBotao");

    botao.onclick = function() {
      alert("Olá, mundo!");
    };
  </script>
</body>
</html>
```
# questão 7
# Quando o usuário tenta enviar o formulário, o código verifica se as informações preenchidas estão corretas, mostrando mensagens de erro se algo estiver errado. Se tudo estiver certo, ele exibe um alerta dizendo que o formulário foi enviado com sucesso.

## Código html
```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Validação de Formulário</title>
    <style>
        .error { color: red; font-size: 14px; }
        input, textarea { display: block; margin-bottom: 10px; width: 100%; padding: 8px; }
        button { padding: 10px; cursor: pointer; }
    </style>
</head>
<body>
    <form id="contactForm">
        <label for="name">Nome:</label>
        <input type="text" id="name">
        <span class="error" id="nameError"></span>

        <label for="email">E-mail:</label>
        <input type="email" id="email">
        <span class="error" id="emailError"></span>

        <label for="message">Mensagem:</label>
        <textarea id="message"></textarea>
        <span class="error" id="messageError"></span>

        <button type="submit">Enviar</button>
    </form>

    <script>
        document.getElementById("contactForm").addEventListener("submit", function (event) {
            event.preventDefault(); 
      
            const name = document.getElementById("name").value.trim();
            const email = document.getElementById("email").value.trim();
            const message = document.getElementById("message").value.trim();
            
            const nameError = document.getElementById("nameError");
            const emailError = document.getElementById("emailError");
            const messageError = document.getElementById("messageError");

            let isValid = true;

           
            nameError.textContent = "";
            emailError.textContent = "";
            messageError.textContent = "";
           
            if (name === "") {
                nameError.textContent = "O nome é obrigatório.";
                isValid = false;
            }     
            const emailPattern = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
            if (email === "") {
                emailError.textContent = "O e-mail é obrigatório.";
                isValid = false;
            } else if (!emailPattern.test(email)) {
                emailError.textContent = "Digite um e-mail válido.";
                isValid = false;
            }
     
            if (message.length < 10) {
                messageError.textContent = "A mensagem deve ter pelo menos 10 caracteres.";
                isValid = false;
            }

            if (isValid) {
                alert("Formulário enviado com sucesso!");
                
            }
        });
    </script>
</body>
</html>
```
# questãoo 7

# Quando o usuário tenta enviar o formulário, o código verifica se as informações preenchidas estão corretas, mostrando mensagens de erro se algo estiver errado. Se tudo estiver certo, ele exibe um alerta dizendo que o formulário foi enviado com sucesso.


## Código html
```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Validação de Formulário</title>
    <style>
        .error { color: red; font-size: 14px; }
        input, textarea { display: block; margin-bottom: 10px; width: 100%; padding: 8px; }
        button { padding: 10px; cursor: pointer; }
    </style>
</head>
<body>
    <form id="contactForm">
        <label for="name">Nome:</label>
        <input type="text" id="name">
        <span class="error" id="nameError"></span>

        <label for="email">E-mail:</label>
        <input type="email" id="email">
        <span class="error" id="emailError"></span>

        <label for="message">Mensagem:</label>
        <textarea id="message"></textarea>
        <span class="error" id="messageError"></span>

        <button type="submit">Enviar</button>
    </form>

    <script>
        document.getElementById("contactForm").addEventListener("submit", function (event) {
            event.preventDefault(); 

       
            const name = document.getElementById("name").value.trim();
            const email = document.getElementById("email").value.trim();
            const message = document.getElementById("message").value.trim();

            
            const nameError = document.getElementById("nameError");
            const emailError = document.getElementById("emailError");
            const messageError = document.getElementById("messageError");

            let isValid = true;

           
            nameError.textContent = "";
            emailError.textContent = "";
            messageError.textContent = "";

           
            if (name === "") {
                nameError.textContent = "O nome é obrigatório.";
                isValid = false;
            }

      
            const emailPattern = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
            if (email === "") {
                emailError.textContent = "O e-mail é obrigatório.";
                isValid = false;
            } else if (!emailPattern.test(email)) {
                emailError.textContent = "Digite um e-mail válido.";
                isValid = false;
            }

       
            if (message.length < 10) {
                messageError.textContent = "A mensagem deve ter pelo menos 10 caracteres.";
                isValid = false;
            }


            if (isValid) {
                alert("Formulário enviado com sucesso!");
                
            }
        });
    </script>
</body>
</html>
```

# questão 8

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SPA - Manipulação de Conteúdo</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
        }
        nav {
            background-color: #333;
            padding: 10px;
        }
        nav a {
            color: white;
            margin-right: 20px;
            text-decoration: none;
        }
        #content {
            padding: 20px;
        }
    </style>
</head>
<body>

    <nav>
        <a href="#" id="home">Home</a>
        <a href="#" id="about">Sobre</a>
        <a href="#" id="contact">Contato</a>
    </nav>

    <div id="content">
        <h1>Bem-vindo à nossa página!</h1>
        <p>Selecione uma das opções acima para visualizar o conteúdo.</p>
    </div>

    <script>
       
        function loadContent(page) {
            const contentDiv = document.getElementById("content");
            
         
            if (page === 'home') {
                contentDiv.innerHTML = '<h1>Home</h1><p>Bem-vindo à página inicial!</p>';
            } else if (page === 'about') {
                contentDiv.innerHTML = '<h1>Sobre</h1><p>Informações sobre nós.</p>';
            } else if (page === 'contact') {
                contentDiv.innerHTML = '<h1>Contato</h1><p>Entre em contato conosco pelo e-mail: contato@exemplo.com.</p>';
            }
  
            setupEvents();
        }
    
        function setupEvents() {
            document.getElementById("home").addEventListener("click", function() {
                loadContent("home");
            });

            document.getElementById("about").addEventListener("click", function() {
                loadContent("about");
            });

            document.getElementById("contact").addEventListener("click", function() {
                loadContent("contact");
            });
        }

        setupEvents();
    </script>
    
</body>
</html>
```
# Uma vez que o conteúdo foi alterado, a função `setupEvents()` é chamada. Ela reatribui os eventos de clique para os links de navegação. Isso é importante porque, ao alterar o conteúdo de uma página usando `innerHTML`, os eventos podem ser removidos.

# Isso garante que, mesmo após a troca de conteúdo, os links de navegação ainda funcionarão.

# questão 9

### Funções do History API
- **`pushState`**: Adiciona uma nova entrada ao histórico do navegador.
- **`replaceState`**: Similar ao `pushState`, mas substitui a entrada atual do histórico em vez de adicionar uma nova. Ele é útil para evitar acúmulo desnecessário de entradas no histórico.
- **`Popstate`**: Funciona conforme o usuário navega pelo seu histórico. Pode ser usado para detectar mudanças no histórico e atualizar a interface da aplicação.
```javascript
function navigateTo(url) {
    // Quando o usuário clica em um link, usamos pushState para atualizar a URL sem recarregar a página:
    history.pushState({}, "", url);
    handleRoute();
}

window.addEventListener("popstate", handleRoute);

// Quando o usuário usa os botões "Voltar" ou "Avançar" do navegador, o evento popState é acionado:
function handleRoute() {
    const path = window.location.pathname;
    const content = document.getElementById("content");

    if (path === "/home") {
        content.innerHTML = "<h1>Home</h1>";
    } else if (path === "/about") {
        content.innerHTML = "<h1>About</h1>";
    } else {
        content.innerHTML = "<h1>404 - Página não encontrada</h1>";
    }
}

### Quanto às precauções e fallbacks:
- ** Navegadores antigos (IE9 e anteriores) não suportam `pushState`**:  
  Fallback usando `hash`. Em navegadores sem suporte ao History API, pode-se usar `window.location.hash` em vez de `pushState` para gerenciar as rotas.

- **Configuração correta do servidor**:  
  Se a aplicação for SPA e as URLs não forem processadas corretamente pelo servidor, ele pode exibir erro 404. Para evitar isso, configure o servidor para redirecionar todas as solicitações para o arquivo principal da aplicação (ex.: `index.html`).

# questão 10

Para otimizar o desempenho de uma SPA com múltiplos módulos de JavaScript, podemos empregar três técnicas principais: **Code Splitting**, **Lazy Loading** e **Módulos JavaScript Nativos (ES Modules)**. Essas estratégias ajudam a reduzir o tempo de carregamento inicial 
e melhorar a performance geral da aplicação.

O **Code Splitting** permite dividir o código JavaScript em vários arquivos menores, em vez de carregar um único bundle grande.
 Isso reduz o tempo de carregamento inicial, pois a aplicação carrega apenas o código necessário para a primeira renderização.
```javascript
// Importação dinâmica que cria um bundle separado
function loadModule() {
    import('./module.js').then(module => {
        module.default();
    });
}
Isso garante que `module.js` só seja carregado quando `loadModule()` for chamado.

O **Lazy Loading** complementa o Code Splitting, carregando módulos apenas quando são realmente necessários, em vez de incluir tudo no carregamento inicial.
import React, { Suspense, lazy } from 'react';

// Importação dinâmica do componente
const LazyComponent = lazy(() => import('./LazyComponent'));

function App() {
    return (
        <Suspense fallback={<div>Carregando...</div>}>
            <LazyComponent />
        </Suspense>
    );
}
O `LazyComponent` só será carregado quando for renderizado pela primeira vez.

Os **Módulos JavaScript Nativos (ES Modules)** permitem que os navegadores modernos carreguem scripts de forma assíncrona, sem necessidade de um bundler.
<script type="module">
    import { initApp } from './app.js';
    initApp();
</script>
Isso permite que o código seja carregado dinamicamente e cacheado pelo navegador.

Essas estratégias podem ser combinadas para otimizar o carregamento e a performance da SPA, além de reduzir a carga inicial, melhorar a experiência do usuário e evitar desperdício de recursos.

- **Code Splitting** reduz o tamanho do bundle inicial.
- **Lazy Loading** garante que módulos grandes sejam carregados apenas quando necessário.
- **ES Modules** permitem que o navegador lide com carregamento assíncrono sem necessidade de ferramentas adicionais.

# questão 11

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Relógio Dinâmico</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            margin-top: 50px;
        }
        #clock {
            font-size: 2rem;
            font-weight: bold;
        }
    </style>
</head>
<body>

    <h1>Hora Atual</h1>
    <span id="clock">--:--:--</span>

    <script>
        function updateClock() {
            const now = new Date(); // Captura a data/hora atual
            const hours = now.getHours().toString().padStart(2, '0');
            const minutes = now.getMinutes().toString().padStart(2, '0');
            const seconds = now.getSeconds().toString().padStart(2, '0');
            // getHours(), getMinutes() e getSeconds() obtêm as horas, minutos e segundos.
            document.getElementById("clock").textContent = `${hours}:${minutes}:${seconds}`;
        }
    </script>
</body>
</html>

### Explicação:
- ** Atualiza o relógio imediatamente e a cada segundo: **
```javascript
updateClock();
A função `updateClock()` atualiza o `<span id="clock">` com o horário formatado.

```javascript
setInterval(updateClock, 1000);

`setInterval(updateClock, 1000)` executa a função `updateClock()` a cada segundo (1000ms) para evitar o atraso de 1 segundo na primeira atualização.

# questão 12

```javascript
document.addEventListener("DOMContentLoaded", function () {
    const dropdown = document.querySelector(".dropdown");
    const submenu = document.querySelector(".submenu");

    let isTouchDevice = "ontouchstart" in window || navigator.maxTouchPoints > 0;

    if (isTouchDevice) {
        // Dispositivo com toque: Usar clique para abrir/fechar o menu
        dropdown.addEventListener("click", function (event) {
            event.preventDefault(); // Previne navegação direta no link
            submenu.classList.toggle("active");
        });

        // Fechar o menu ao tocar fora dele
        document.addEventListener("click", function (event) {
            if (!dropdown.contains(event.target)) {
                submenu.classList.remove("active");
            }
        });
    } else {
        // Dispositivo com mouse: Usar hover
        dropdown.addEventListener("mouseenter", function () {
            submenu.classList.add("hover");
        });

        dropdown.addEventListener("mouseleave", function () {
            submenu.classList.remove("hover");
        });
    }
});
Ele vai detectar se o dispositivo é touchscreen usando `"ontouchstart" in window` ou `navigator.maxTouchPoints`. Se o dispositivo for touch:

- O clique (`click`) ativa ou desativa a classe `.active`.
- Se o usuário tocar fora do menu, ele fecha automaticamente.

Se o dispositivo for mouse:

- Ele usa `mouseenter` e `mouseleave` para alternar a classe `.hover`, garantindo um comportamento fluido.

O CSS gerencia a visibilidade do menu, ativando-o com `.hover` (mouse) ou `.active` (touch).

Com isso, o dropdown irá funcionar em desktop e dispositivos móveis sem conflitos, evitando problemas com toques duplos em links dentro do menu e deixando a performance otimizada, sem necessidade de frameworks.

# questão 13

### Questão 13:

```javascript
document.addEventListener("DOMContentLoaded", () => {
    const apiUrl = "https://api.example.com/data"; // URL da API
    const container = document.getElementById("data-container");

    async function fetchData() {
        try {
            // 1️ Faz a requisição para a API
            const response = await fetch(apiUrl); // `await fetch(apiUrl)` obtém os dados da API.

            // 2️ Verifica se a resposta foi bem-sucedida
            if (!response.ok) {
                throw new Error(`Erro ${response.status}: ${response.statusText}`); // Se `response.ok` for false, lançamos um erro com o status HTTP.
            }

            // 3️ Converte para JSON
            const data = await response.json(); // `const data = await response.json();` transforma a resposta em um objeto utilizável.

            // 4️ Exibe os dados no DOM
            displayData(data);
        } catch (error) {
            console.error("Erro ao buscar os dados:", error);
            container.innerHTML = `<p class="error">Erro ao carregar os dados. Tente novamente mais tarde.</p>`;
        }
    }

    // Criamos elementos dinamicamente para exibir o conteúdo na tela.
    function displayData(data) {
        container.innerHTML = ""; // Limpa o conteúdo anterior
        data.forEach(item => {
            const div = document.createElement("div");
            div.classList.add("item");
            div.innerHTML = `<h3>${item.title}</h3><p>${item.description}</p>`;
            container.appendChild(div);
        });
    }

    fetchData(); // Chama a função ao carregar a página
});
### Melhorias que podem ser feitas:

1. **Loader de carregamento**:  
   Adicionar um indicador de carregamento, como "Carregando...", enquanto os dados não são recebidos da API.

2. **Cache local**:  
   Armazenar a última resposta da API no `localStorage` para exibição imediata em carregamentos futuros, melhorando a experiência do usuário.

3. **Requisição com timeout**:  
   Usar `setTimeout` com `AbortController` para evitar longas esperas, garantindo que a requisição seja cancelada após um tempo limite definido.




