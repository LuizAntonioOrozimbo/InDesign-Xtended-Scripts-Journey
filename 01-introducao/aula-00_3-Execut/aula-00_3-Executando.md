# 📘 AULA 00.3 — Como Executar um Arquivo .jsx no InDesign

##

### 🎯 Objetivo da Aula

Ao final desta aula, você será capaz de:

- Executar scripts .jsx de três maneiras diferentes no InDesign.

- Entender quando usar cada método.

- Testar seu primeiro script real de criação de documento.

- Preparar a base para o início do Módulo 1.

## 🧭 1. Métodos oficiais para executar um script .jsx

Existem **três maneiras** recomendadas de rodar scripts no InDesign.

Cada uma serve para um tipo de situação.

## 🔵 Método 1 — Painel Scripts (recomendado para iniciantes)

Este é o método mais seguro e direto.

### Como acessar

Window › Utilities › Scripts

Você verá duas pastas:

- **Application →** scripts padrão da Adobe

- **User →** onde ficam seus scripts

### Como instalar

**1.** Clique com botão direito em **User → Reveal in Explorer**.

**2.** Coloque seu arquivo .jsx ali.

### Como executar

**👉 Dê duplo clique no arquivo.**

### Quando usar este método?

- Para testar scripts simples.

- Para aulas e exercícios.

- Para automatizar tarefas rápidas.

## 🟣 Método 2 — VSCode + ExtendScript Debugger

Requer a extensão:  
**Adobe ExtendScript Debugger**

### Como funciona

- Abra o .jsx no VSCode

- Pressione **F5**

- O script é enviado ao InDesign

- Breakpoints funcionam normalmente

### Quando usar?

- Para scripts longos e complexos

- Para depurar, inspecionar variáveis

- Para detectar erros invisíveis no painel Scripts

### ⚠️ Importante

É obrigatório ter a primeira linha:

```jsx
#target indesign
```

## 🟡 Método 3 — ExtendScript Toolkit (ESTK)

(antigo, mas ainda útil)

O ESTK:

- funciona como editor + console

- mostra variáveis e objetos

- ainda pode rodar scripts no InDesign

### Não recomendado para

- Novos projetos

- Scripts complexos

- Uso profissional contínuo

### Útil para

- Checar valores rapidamente

- Testar pequenas funções

- Inspecionar a DOM (quando funciona)

## 🧪 2. Teste rápido com um script real (introdução ao Módulo 1)

Crie um arquivo:

```jsx
exemplo-aula-00-3.jsx
```

```js
#target indesign

// Aula 00.3 — Criando um documento e adicionando conteúdo

// Cria um novo documento
var doc = app.documents.add();

// Cria uma página extra
doc.pages.add();

// Seleciona a primeira página
var page = doc.pages[0];

// Adiciona um frame de texto
var frame = page.textFrames.add({
    geometricBounds: [20, 20, 200, 200],
    contents: "Primeiro script completo da Aula 00.3!"
});

alert("Script executado com sucesso!");
```

**👉 Execute usando os 3 métodos para fixar o aprendizado.**

### Conclusão

Você agora domina as três formas de executar scripts no InDesign e está preparado para iniciar o Módulo 1, onde começaremos a explorar o DOM e os fundamentos do ExtendScript.
