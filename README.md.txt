# RELACIONAMENTO.EXE

### Jogo educativo digital sobre relacionamentos, respeito e prevenção da violência de gênero

Projeto desenvolvido para o **Concurso para Jovens Aprendizes do CIEE**, dentro do **Projeto Se Liga Moçada — Programa Bem Querer Mulher**.

**Categoria III — Fanzine, jogos educativos ou materiais lúdicos**

> **"Você está no controle. Será que está controlando a pessoa também?"**

---

## 🎮 Sobre o projeto

**RELACIONAMENTO.EXE** é um jogo educativo interativo que apresenta situações fictícias relacionadas a relacionamentos, respeito, autonomia, controle, violência psicológica e cultura digital.

A proposta é utilizar uma narrativa em formato de conversa para colocar o jogador diante de diferentes situações e permitir que ele tome decisões.

Após cada escolha, o jogo apresenta uma **consequência educativa**, explicando o que está envolvido naquela situação e incentivando a reflexão sobre comportamentos, limites e respeito.

O resultado final apresenta indicadores relacionados a:

* ❤️ Respeito
* 🎯 Controle
* 🧠 Consciência

**Importante:** o resultado do jogo não é um diagnóstico, teste psicológico ou avaliação de personalidade. Ele representa exclusivamente as escolhas realizadas pelo jogador dentro da história fictícia.

---

## 📖 Como funciona

A história é apresentada como uma conversa de aplicativo de mensagens entre personagens fictícios:

* Lia
* Rafa
* Bea
* Teo

O jogador passa por **6 capítulos**, com **12 decisões** ao longo da história.

Em cada decisão:

1. Uma situação é apresentada.
2. O jogador escolhe uma das alternativas disponíveis.
3. A escolha gera uma consequência educativa.
4. Os indicadores do jogador são atualizados.
5. A história continua até o resultado final.

Ao terminar, o jogador recebe um dos **6 resultados possíveis**.

Também é possível iniciar uma nova partida a qualquer momento.

---

## ▶️ Como abrir

O projeto foi desenvolvido para funcionar diretamente no navegador.

### No computador

1. Baixe ou descompacte o projeto.
2. Abra a pasta do projeto.
3. Clique duas vezes no arquivo `index.html`.
4. O jogo será aberto no navegador padrão.

Não é necessário:

* instalar programas;
* configurar servidor;
* utilizar banco de dados;
* instalar bibliotecas;
* possuir conexão com a internet.

### No celular

O arquivo `index.html` também pode ser transferido para o celular por meios como:

* WhatsApp;
* Google Drive;
* cabo USB;
* e-mail.

O layout é responsivo e se adapta a diferentes tamanhos de tela.

---

## 💻 Tecnologias utilizadas

O projeto foi desenvolvido utilizando tecnologias web básicas, sem frameworks ou bibliotecas externas.

### HTML5

Responsável pela estrutura e organização do conteúdo da página.

### CSS3

Responsável pela interface visual, incluindo:

* tema escuro;
* balões de mensagens;
* indicadores;
* barras de progresso;
* botões;
* animações;
* layout responsivo.

### JavaScript

Responsável pela lógica do jogo, incluindo:

* narrativa;
* escolhas;
* pontuação;
* consequências educativas;
* progressão dos capítulos;
* cálculo dos indicadores;
* definição do resultado final;
* reinício da partida.

### Estrutura independente

Todo o projeto está concentrado em um único arquivo:

`index.html`

O arquivo contém o **HTML, CSS e JavaScript**, permitindo que o jogo funcione mesmo sem conexão com a internet.

---

## 📁 Estrutura do projeto

```text
RELACIONAMENTO_EXE_3.0/
│
├── index.html
└── README.md
```

### `index.html`

Contém todo o jogo, incluindo:

* estrutura da interface;
* estilos CSS;
* personagens;
* capítulos;
* diálogos;
* alternativas;
* sistema de pontuação;
* consequências educativas;
* resultados finais;
* lógica de navegação.

### `README.md`

Documento com informações sobre o projeto, funcionamento, tecnologias e instruções de utilização.

---

## 🧩 Organização do código

Dentro do `index.html`, o código está dividido principalmente em três partes:

### 1. Dados do jogo

Contém as estruturas responsáveis pelos capítulos, diálogos, escolhas, pontuações e resultados.

```javascript
CHAPTERS
RESULTS
```

### 2. Estado e lógica

Responsável por armazenar as escolhas realizadas e calcular o resultado final.

Entre as principais funções está:

```javascript
computeResult()
```

### 3. Renderização

Responsável por construir e atualizar as telas do jogo.

Entre as principais funções estão:

```javascript
renderHome()
renderAbout()
renderChapter()
playSteps()
renderChoice()
pickOption()
renderResult()
```

---

## ✏️ Como modificar a história

Para alterar os capítulos, perguntas ou alternativas, abra o arquivo `index.html` em um editor de texto, como:

* Bloco de Notas;
* Visual Studio Code;
* outro editor de código.

Procure por:

```javascript
var CHAPTERS = [
```

Cada capítulo possui informações como:

```javascript
{
    id: 1,
    title: "PRIMEIRO SINAL",
    theme: "Privacidade...",
    steps: [...]
}
```

Os principais tipos de conteúdo são:

```text
t:"narr"   → narração
t:"them"   → fala de outro personagem
t:"me"     → fala do jogador
t:"choice" → momento de escolha
```

Nas escolhas:

```text
q   → pergunta apresentada ao jogador
opts → alternativas disponíveis
x   → texto da alternativa
f   → consequência educativa
```

É possível adicionar ou modificar capítulos e decisões diretamente nessa estrutura.

A quantidade de capítulos e a barra de progresso são atualizadas automaticamente pela lógica do jogo.

---

## 📊 Sistema de pontuação

Cada alternativa possui três indicadores:

```text
r = RESPEITO
c = CONTROLE
s = CONSCIÊNCIA
```

Os valores são utilizados pela lógica do jogo para determinar os indicadores finais.

Exemplo:

```javascript
{
    x: "Digo que prefiro manter minha privacidade.",
    r: 2,
    c: 0,
    s: 2,
    f: "Respeitar limites também é uma forma de cuidado."
}
```

O jogo calcula automaticamente as porcentagens finais, não sendo necessário alterar manualmente os valores exibidos nas barras.

---

## 🏆 Resultados

O jogo possui **6 resultados possíveis**.

A função:

```javascript
computeResult()
```

analisa os indicadores obtidos durante a partida e determina qual resultado será apresentado.

Os textos, títulos e demais informações dos resultados podem ser encontrados em:

```javascript
var RESULTS = [
```

---

## 🧪 Testes realizados

Durante o desenvolvimento foram realizados testes de funcionamento e compatibilidade.

### Funcionalidade

Foram verificados:

* botão Iniciar;
* alternativas;
* botão Continuar;
* botão Próximo capítulo;
* botão Ver resultado;
* botão Jogar novamente;
* tela Sobre o projeto;
* botão Voltar;
* botão Recomeçar.

### Conteúdo

* 6 capítulos acessíveis;
* 12 decisões funcionais;
* 6 resultados possíveis.

### Simulação

Foi realizada uma simulação automática de **5.000 partidas** para verificar a distribuição dos resultados.

Os **6 resultados possíveis foram alcançados**, indicando que nenhum resultado configurado ficou inacessível durante a simulação.

### Compatibilidade

O projeto foi testado em:

* computador;
* tela de celular com aproximadamente 390 px de largura;
* navegador sem conexão com a internet.

### Funcionamento offline

O jogo foi executado com a conexão de internet desativada e continuou funcionando normalmente.

Não são utilizados:

* APIs externas;
* banco de dados;
* servidores;
* imagens externas;
* bibliotecas externas;
* fontes externas;
* links necessários para o funcionamento do jogo.

---

## 🎯 Temas abordados

O conteúdo foi desenvolvido considerando os temas previstos para o projeto, incluindo:

* machismo e misoginia;
* Lei Maria da Penha;
* Lei do Feminicídio;
* tipos e ciclo da violência;
* violência psicológica;
* gaslighting;
* mansplaining;
* manterrupting;
* cultura digital;
* machosfera e discursos de ódio;
* masculinidades;
* respeito e autonomia nos relacionamentos.

Todos os personagens e situações apresentados são **fictícios**.

O jogo não apresenta conteúdo gráfico ou descrição explícita de violência física.

---

## 🆘 Canais de apoio

O jogo disponibiliza informações sobre canais públicos de apoio:

**Ligue 180** — Central de Atendimento à Mulher

**190** — Polícia Militar em situações de emergência

Em situações reais de violência ou risco, procure os canais oficiais de atendimento e emergência.

---

## 🤖 Uso de Inteligência Artificial

Ferramentas de Inteligência Artificial foram utilizadas como **apoio durante o processo de desenvolvimento**, principalmente para auxiliar na estruturação, implementação e revisão de elementos do projeto.

A proposta, conteúdo, narrativa, personagens, decisões, indicadores e funcionamento do jogo foram definidos e organizados de acordo com os objetivos do projeto.

---

## 🌐 Publicação

Por utilizar apenas tecnologias web básicas e não depender de um servidor ou banco de dados, o projeto pode ser hospedado em serviços de páginas estáticas.

Isso permite disponibilizar o jogo na internet mantendo a mesma estrutura do arquivo `index.html`.

---

## 📌 Informações do projeto

**Projeto:** RELACIONAMENTO.EXE
**Programa:** Se Liga Moçada
**Instituição:** CIEE
**Programa relacionado:** Bem Querer Mulher
**Categoria:** III — Fanzine, jogos educativos ou materiais lúdicos

---

## 👥 Equipe

Projeto desenvolvido por:

**[Nome dos participantes]**

---

### Projeto educativo

**RELACIONAMENTO.EXE**
*Você está no controle. Será que está controlando a pessoa também?*
