# Dificuldades, ajustes e aprendizados

Este documento registra as dificuldades encontradas durante o uso do NotebookLM, os ajustes realizados nos prompts e os resultados obtidos. Esses registros demonstram o processo de análise crítica e aprimoramento das respostas geradas pela inteligência artificial.

## Cicatriz 1 — Códigos HTML visíveis na tabela

### Contexto

Foi solicitado ao NotebookLM que explicasse as diferenças entre receitas, despesas fixas, despesas variáveis e despesas eventuais. A resposta deveria apresentar definições e exemplos fictícios organizados em uma tabela.

### Dificuldade encontrada

A primeira resposta apresentou códigos HTML `<br>` visíveis na coluna de exemplos. Embora o conteúdo estivesse adequado, esses códigos prejudicaram a legibilidade e a apresentação da tabela.

### Possível causa

O NotebookLM tentou inserir quebras de linha dentro das células da tabela utilizando HTML, mas a interface exibiu os códigos como texto em vez de interpretá-los como formatação.

### Prompt inicial

> Com base exclusivamente nas quatro fontes selecionadas, explique as diferenças entre receitas, despesas fixas, despesas variáveis e despesas eventuais. Apresente uma definição simples e dois exemplos fictícios de cada categoria. Organize a resposta em uma tabela e inclua as referências utilizadas.

### Ajuste realizado

Foi enviado um novo prompt especificando que a resposta não deveria utilizar códigos HTML e que os exemplos deveriam ser separados por ponto e vírgula.

### Prompt de correção

> Refaça a resposta anterior sem utilizar códigos HTML, como `<br>`. Mantenha as quatro categorias, com definição simples e dois exemplos fictícios para cada uma. Organize em uma tabela Markdown limpa, escrevendo cada exemplo separado por ponto e vírgula, e mantenha as citações das fontes.

### Resultado obtido

A resposta corrigida:

- Eliminou os códigos HTML visíveis;
- Manteve as quatro categorias solicitadas;
- Preservou as definições e os exemplos fictícios;
- Separou os exemplos por ponto e vírgula;
- Manteve as citações relacionadas às fontes;
- Apresentou uma tabela mais limpa e legível.

### Aprendizado

O teste demonstrou que uma resposta pode estar correta em conteúdo e ainda precisar de ajustes de apresentação. Instruções específicas sobre formato, separadores e elementos que não devem ser utilizados ajudam a produzir resultados mais adequados.

Também ficou evidente que a primeira resposta da inteligência artificial não deve ser aceita automaticamente. É necessário revisar o conteúdo, verificar as referências e corrigir problemas de clareza ou formatação.
