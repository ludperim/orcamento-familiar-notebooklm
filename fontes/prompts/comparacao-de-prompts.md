# Comparação de prompts

Este documento registra um teste com diferentes níveis de detalhamento de prompts no NotebookLM. O objetivo foi observar como a formulação da pergunta influencia o conteúdo, a organização, as referências e a utilidade da resposta.

## Variação 1 — Prompt genérico

### Prompt utilizado

> Explique como organizar um orçamento familiar.

### Resultado observado

A resposta apresentou um guia organizado sobre orçamento familiar, incluindo:

- Participação da família;
- Registro de receitas e despesas;
- Classificação dos gastos;
- Planejamento mensal;
- Acompanhamento e avaliação do saldo;
- Referências às quatro fontes selecionadas.

Entretanto, o prompt genérico permitiu que o NotebookLM acrescentasse recomendações específicas, como reservar pelo menos 10% da renda e utilizar a regra 50/30/20. Essas orientações podem não ser adequadas à realidade de todas as famílias.

A resposta também não apresentou um exemplo numérico fictício nem diferenciou claramente os valores planejados dos realizados.

## Variação 2 — Prompt com fonte, sequência e categorias

### Prompt utilizado

> Com base exclusivamente nas fontes selecionadas, explique como uma família pode organizar seu orçamento mensal. Apresente as etapas em ordem, diferencie receitas e tipos de despesas e inclua as referências utilizadas.

### Resultado observado

A segunda resposta ficou mais controlada e organizada. Ela:

- Utilizou as fontes selecionadas como referência;
- Organizou o processo em cinco etapas;
- Diferenciou receitas fixas e variáveis;
- Diferenciou despesas fixas, variáveis, eventuais e sazonais;
- Evitou percentuais rígidos e a regra 50/30/20;
- Indicou as quatro fontes utilizadas.

Apesar da melhoria, a resposta ainda não apresentou um exemplo numérico nem demonstrou na prática o cálculo do saldo familiar.

## Variação 3 — Prompt detalhado e orientado ao resultado

### Prompt utilizado

> Com base exclusivamente nas quatro fontes selecionadas, crie um guia para uma família iniciante organizar seu orçamento mensal.
>
> Organize a resposta em:
>
> 1. Preparação e participação da família;
> 2. Registro e classificação das receitas e despesas;
> 3. Planejamento do mês;
> 4. Acompanhamento do planejado e do realizado;
> 5. Avaliação e ajustes.
>
> Inclua um exemplo numérico fictício e simples, mostrando receitas, despesas, saldo e a identificação de superávit, equilíbrio ou déficit. Não apresente percentuais ou regras financeiras que não sirvam para todas as famílias. Inclua citações das fontes ao longo da resposta.

### Resultado observado

A terceira resposta foi a mais completa. Ela:

- Seguiu as cinco etapas solicitadas;
- Utilizou linguagem adequada para iniciantes;
- Evitou recomendações percentuais rígidas;
- Apresentou um exemplo explicitamente fictício;
- Informou receitas de R$ 2.500,00;
- Informou despesas de R$ 2.200,00;
- Calculou corretamente o saldo de R$ 300,00;
- Classificou corretamente o orçamento como superavitário;
- Indicou as fontes utilizadas.

Entretanto, embora a resposta explicasse os conceitos de valor orçado e realizado, o exemplo numérico não comparava esses dois valores.

## Ajuste do exemplo numérico

### Prompt de correção

> A resposta está adequada, mas revise apenas o exemplo numérico final. Acrescente uma comparação simples entre despesas orçadas e realizadas, mantendo os valores fictícios e demonstrando a diferença entre elas. Preserve o cálculo do saldo final de R$ 300,00 e sua classificação como orçamento superavitário. Mantenha também as citações das fontes ao longo da resposta.

### Resultado após o ajuste

Após a correção, o exemplo passou a demonstrar:

- O total de receitas;
- As despesas orçadas;
- As despesas realizadas;
- A diferença entre os valores previstos e realizados;
- O saldo final de R$ 300,00;
- A classificação do orçamento como superavitário.

A resposta corrigida foi salva no NotebookLM como:

> Resposta 4 — Guia prático de orçamento familiar

## Comparação dos resultados

| Critério | Variação 1 | Variação 2 | Variação 3 ajustada |
|---|---|---|---|
| Uso explícito das fontes | Parcialmente controlado | Solicitado | Solicitado com citações ao longo da resposta |
| Organização das etapas | Definida pelo NotebookLM | Solicitada em ordem | Estrutura definida no prompt |
| Classificação de receitas e despesas | Presente | Solicitada diretamente | Presente dentro do guia |
| Exemplo numérico | Não | Não | Sim |
| Comparação entre orçado e realizado | Não | Apenas conceitual | Sim, após correção |
| Restrições a regras rígidas | Não | Indiretamente | Explicitamente solicitadas |
| Necessidade de ajuste | Conteúdo pouco controlado | Faltou exemplo prático | Faltou inicialmente comparar orçado e realizado |

## Conclusão

O teste demonstrou que prompts mais detalhados produzem respostas mais próximas do objetivo desejado.

O primeiro prompt gerou uma resposta útil, mas deu ao NotebookLM liberdade para escolher o conteúdo e incluir recomendações que não se aplicam igualmente a todas as famílias.

O segundo prompt melhorou o controle das fontes, da sequência e das categorias, mas ainda não solicitou uma aplicação prática.

O terceiro prompt definiu o público, a estrutura, o exemplo, as restrições e a forma de apresentar as referências. Por isso, produziu o resultado mais completo. Mesmo assim, foi necessário revisar a resposta e solicitar um ajuste específico no exemplo numérico.

Conclui-se que um bom prompt deve indicar com clareza:

- A base de informações que deve ser utilizada;
- O público da resposta;
- O objetivo da atividade;
- A estrutura esperada;
- Os exemplos necessários;
- As restrições de conteúdo;
- A forma de apresentação das referências.

Também é indispensável revisar o resultado, pois mesmo um prompt detalhado pode gerar uma resposta que atenda apenas parcialmente ao que foi solicitado.
