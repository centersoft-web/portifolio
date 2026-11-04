# Alberto de Campos Neto - Portfólio

Portfólio pessoal desenvolvido em HTML, CSS e JavaScript puro, com integração à API do GitHub para exibir automaticamente os repositórios públicos do usuário.

## ✨ Funcionalidades

- Exibição automática dos projetos hospedados no GitHub.
- Interface moderna e responsiva.
- Design com tema escuro.
- Navegação suave entre seções.
- Contador dinâmico de projetos.
- Carregamento dos repositórios por meio da API do GitHub.
- Exibição do nome, descrição e linguagem de cada projeto.
- Link para o repositório no GitHub.
- Link para a aplicação publicada, quando configurado no campo `homepage` do repositório.
- Tratamento de erro caso a API do GitHub não esteja disponível.

## 🚀 Tecnologias utilizadas

- HTML5
- CSS3
- JavaScript (Vanilla JS)
- GitHub REST API

## 📂 Estrutura do projeto

```text
/
├── index.html
└── README.md
```

## 🔧 Como funciona

O portfólio realiza uma requisição para a API pública do GitHub usando o nome de usuário definido no arquivo `index.html`:

```javascript
const USUARIO_GITHUB = "alcane1959";
```

A URL da API é montada dinamicamente:

```javascript
https://api.github.com/users/${USUARIO_GITHUB}/repos?per_page=100&sort=updated&type=owner
```

Depois de receber os dados, o código:

1. Remove repositórios que são forks.
2. Remove repositórios arquivados.
3. Exclui da listagem o repositório principal do GitHub Pages.
4. Atualiza o contador de projetos.
5. Gera automaticamente os cards dos projetos.
6. Exibe o link da página publicada quando o repositório possui uma URL válida no campo `homepage`.

## ▶️ Como executar

### Opção 1: abrir diretamente

Baixe ou clone o projeto e abra o arquivo `index.html` no navegador.

### Opção 2: usar um servidor local

Você também pode executar o projeto utilizando uma extensão como Live Server ou qualquer servidor HTTP local.

Exemplo com Python:

```bash
python -m http.server 8000
```

Depois, acesse no navegador:

```text
http://localhost:8000
```

## 🎨 Principais seções

### Início

Apresentação do portfólio, descrição profissional e atalhos para os projetos e para o perfil no GitHub.

### Projetos

Listagem dinâmica dos repositórios públicos encontrados pela API do GitHub.

### Sobre

Resumo das áreas de atuação, das tecnologias utilizadas e da proposta do portfólio.

### Contato

Acesso direto ao perfil do autor no GitHub.

## 📱 Responsividade

O layout possui ajustes para diferentes tamanhos de tela:

- Desktop
- Tablet
- Smartphone

Em telas menores, os cards são reorganizados e o menu principal é ocultado para preservar o espaço disponível.

## ⚙️ Personalização

### Alterar o usuário do GitHub

No arquivo `index.html`, localize:

```javascript
const USUARIO_GITHUB = "alcane1959";
```

Substitua `alcane1959` pelo nome do usuário desejado.

### Alterar os textos

Edite diretamente no HTML:

- Título da página
- Nome do autor
- Texto de apresentação
- Seção Sobre
- Botões e chamadas de ação

### Alterar as cores

As principais cores do projeto estão definidas nas variáveis CSS:

```css
:root {
  --bg: #07111f;
  --card: #0f1d30;
  --card2: #132741;
  --text: #f3f7ff;
  --muted: #a5b6cc;
  --gold: #e8b94d;
  --line: rgba(255, 255, 255, 0.1);
}
```

## 🌐 Publicação

Por ser um projeto estático, o portfólio pode ser publicado em serviços como:

- GitHub Pages
- Netlify
- Vercel
- Firebase Hosting

### Instalação no computador

### No Google Chrome ou Microsoft Edge:

  1. Abra o endereço publicado do projeto.
  2. Aguarde o carregamento completo da página.
  3. Clique no ícone de instalação exibido na barra de endereço ou abra o menu do navegador.
  4. Selecione Instalar aplicativo ou Instalar este site como aplicativo.
  5. Confirme a instalação.

Depois disso, o aplicativo poderá ser aberto pelo menu Iniciar, pela área de trabalho ou pelo gerenciador de aplicativos do sistema.

### Instalação no celular ou tablet

### Em navegadores compatíveis:

1. Abra o endereço do projeto.
2. Acesse o menu do navegador.
3. Selecione Instalar aplicativo ou Adicionar à tela inicial.
4. Confirme o nome e a instalação.

O ícone será adicionado à tela inicial do dispositivo.

**Observações**

A disponibilidade e o nome da opção de instalação podem variar conforme o navegador e o sistema operacional.
Abrir somente o arquivo index.html pelo computador não garante a instalação como PWA.
O projeto deve ser publicado em HTTPS para utilizar os recursos completos de instalação e service worker.
O funcionamento offline depende da configuração do service-worker.js e dos arquivos adicionados ao cache.
Atualizações no projeto podem exigir a atualização da versão do cache do service worker.

## 👨‍💻 Autor

**Alberto de Campos Neto**

- GitHub: [alcane1959](https://github.com/alcane1959)

## 📄 Licença

Este projeto não possui uma licença definida no código fornecido. Caso deseje permitir formalmente o uso, a modificação e a distribuição do projeto, adicione um arquivo `LICENSE` ao repositório.

## Aviso

> Este projeto é uma demonstração educacional desenvolvida para estudos de HTML, CSS e JavaScript. A empresa mencionada é fictícia e qualquer semelhança com empresas reais é mera coincidência.
