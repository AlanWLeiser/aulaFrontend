# Formulários HTML e Introdução ao CSS Inline

## 1. Formulários HTML - A Tag `<form>`

### O que é um formulário HTML?
Os formulários são componentes essenciais para a interação entre usuário e aplicação web, permitindo a coleta de dados que podem ser enviados ao servidor para processamento.

### Sintaxe básica da tag `<form>`

```html
<form action="URL" method="metodo_http">
    <!-- Elementos do formulário -->
</form>
```

### Atributos principais da tag `<form>`

| Atributo | Descrição |
|----------|-----------|
| `action` | URL para onde os dados serão enviados quando o formulário for submetido |
| `method` | Método HTTP a ser usado para enviar os dados (GET, POST) |
| `name` | Nome do formulário, utilizado para referência em scripts |
| `target` | Define onde a resposta do formulário será exibida (`_self`, `_blank`, etc.) |


### Exemplo básico de formulário

```html
<form action="/processar-login" method="POST" name="formLogin">
    <label for="usuario">Usuário:</label>
    <input type="text" id="usuario" name="usuario" required>
    
    <label for="senha">Senha:</label>
    <input type="password" id="senha" name="senha" required>
    
    <button type="submit">Entrar</button>
</form>
```

## 2. A Tag `<button>`

A tag `<button>` cria um botão clicável em páginas HTML. É altamente personalizável e pode conter texto e outros elementos.

### Sintaxe básica

```html
<button type="tipo">Texto do botão</button>
```

### Atributos principais

| Atributo | Descrição |
|----------|-----------|
| `type` | Define o comportamento do botão (`submit`, `reset`, `button`) |
| `name` | Nome do botão para referência em scripts |
| `value` | Valor associado ao botão quando enviado ao servidor |
| `disabled` | Desativa o botão quando presente |
| `form` | ID do formulário ao qual o botão está associado (permite posicionar o botão fora do formulário) |


### Tipos de botões

**1. Botão de envio (submit)**
```html
<button type="submit">Enviar Formulário</button>
```
Função: Envia os dados do formulário para o servidor.

**2. Botão de reset**
```html
<button type="reset">Limpar Campos</button>
```
Função: Limpa todos os campos do formulário, retornando-os ao valor inicial.

**3. Botão regular**
```html
<button type="button">Clique Aqui</button>
```
Função: Não possui comportamento padrão, geralmente usado com JavaScript.

### Exemplo avançado

```html
<button type="submit" name="btn-cadastro" value="cadastrar" form="form-usuario">
    <img src="icon-save.png" alt="Salvar"> Salvar Cadastro
</button>
```

## 3. Elementos `<input>` - Os Campos de Entrada

A tag `<input>` é uma das mais versáteis e utilizadas em formulários HTML, permitindo diversos tipos de entrada de dados.

### Sintaxe básica

```html
<input type="tipo" name="nome" id="id">
```

### Atributos comuns para todos os tipos de input

| Atributo | Descrição |
|----------|-----------|
| `type` | Define o tipo de input (text, password, checkbox, etc.) |
| `name` | Nome para identificar o campo quando enviado ao servidor |
| `id` | Identificador único para o elemento (usado com labels) |
| `value` | Valor inicial do campo |
| `disabled` | Desativa o campo quando presente |
| `readonly` | Torna o campo apenas leitura |
| `required` | Define que o campo deve ser preenchido obrigatoriamente |
| `placeholder` | Texto de exemplo exibido quando o campo está vazio |

### Principais tipos de input

**1. Text (Texto)**
```html
<input type="text" name="nome" placeholder="Digite seu nome">
```
Função: Campo de texto de linha única para inserção de texto simples.

**2. Password (Senha)**
```html
<input type="password" name="senha" placeholder="Digite sua senha">
```
Função: Similar ao texto, mas oculta os caracteres digitados.

**3. Checkbox (Caixa de seleção)**
```html
<input type="checkbox" name="aceito" id="termos">
<label for="termos">Aceito os termos e condições</label>
```
Função: Permite selecionar múltiplas opções.

**4. Radio (Botão de opção)**
```html
<input type="radio" name="genero" id="masculino" value="M">
<label for="masculino">Masculino</label>
<input type="radio" name="genero" id="feminino" value="F">
<label for="feminino">Feminino</label>
```
Função: Permite selecionar apenas uma opção de um grupo.

**5. Number (Número)**
```html
<input type="number" name="idade" min="18" max="100">
```
Função: Campo para inserção de valores numéricos.

**6. Email**
```html
<input type="email" name="email" placeholder="exemplo@dominio.com">
```
Função: Campo específico para endereços de email, com validação básica.

**7. Date (Data)**
```html
<input type="date" name="data_nascimento">
```
Função: Seletor de data.

**8. File (Arquivo)**
```html
<input type="file" name="documento" accept=".pdf,.doc">
```
Função: Permite o upload de arquivos.

**9. Hidden (Oculto)**
```html
<input type="hidden" name="user_id" value="12345">
```
Função: Campo invisível para o usuário, usado para passar informações.

**10. Color (Cor)**
```html
<input type="color" name="cor_perfil">
```
Função: Seletor de cores.

**11. Range (Intervalo)**
```html
<input type="range" name="volume" min="0" max="100" step="10">
```
Função: Controle deslizante para selecionar um valor em um intervalo.

**12. Search (Busca)**
```html
<input type="search" name="busca" placeholder="Pesquisar...">
```
Função: Campo de texto otimizado para buscas.

**13. Tel (Telefone)**
```html
<input type="tel" name="telefone" pattern="[0-9]{10,11}">
```
Função: Campo específico para números de telefone.

**14. URL**
```html
<input type="url" name="website" placeholder="https://exemplo.com">
```
Função: Campo para URLs, com validação básica.

## 4. Introdução ao CSS Inline

O CSS Inline é aplicado diretamente nos elementos HTML através do atributo `style`.

### Sintaxe básica
```html
<elemento style="propriedade1: valor1; propriedade2: valor2;">Conteúdo</elemento>
```

### Propriedades principais abordadas nesta aula

#### 1. Width (Largura)
Define a largura de um elemento.

```html
<div style="width: 200px;">Elemento com largura fixa</div>
<div style="width: 50%;">Elemento com largura relativa</div>
```

Valores possíveis:
- Pixel (`px`) - Tamanho fixo
- Porcentagem (`%`) - Tamanho relativo ao elemento pai
- Auto - Tamanho automático baseado no conteúdo

#### 2. Height (Altura)
Define a altura de um elemento.

```html
<div style="height: 100px;">Elemento com altura fixa</div>
<div style="height: 50%;">Elemento com altura relativa</div>
```

Valores possíveis:
- Pixel (`px`) - Tamanho fixo
- Porcentagem (`%`) - Tamanho relativo ao elemento pai
- Auto - Tamanho automático baseado no conteúdo

#### 3. Color (Cor do texto)
Define a cor do texto dentro de um elemento.

```html
<p style="color: red;">Texto em vermelho</p>
<p style="color: #00FF00;">Texto em verde</p>
<p style="color: rgb(0, 0, 255);">Texto em azul</p>
```

Formas de especificar cores:
- Nome da cor (`red`, `blue`, `green`, etc.)
- Código hexadecimal (`#FF0000`, `#00FF00`, etc.)
- RGB (`rgb(255, 0, 0)`, `rgb(0, 255, 0)`, etc.)

#### 4. Background (Fundo)
Define a cor ou imagem de fundo de um elemento.

```html
<div style="background: yellow;">Elemento com fundo amarelo</div>
<div style="background: #CCCCCC;">Elemento com fundo cinza</div>
```

Valores comuns:
- Cor sólida (nome, hexadecimal, RGB)
- Imagem (`background: url('imagem.jpg')`)

## 7. Recursos Adicionais

- [MDN Web Docs - Botões](https://developer.mozilla.org/pt-BR/docs/Web/HTML/Element/button)
- [MDN Web Docs - Inputs](https://developer.mozilla.org/pt-BR/docs/Web/HTML/Element/input)
- [MDN Web Docs - CSS Básico](https://developer.mozilla.org/pt-BR/docs/Learn/Getting_started_with_the_web/CSS_basics)
