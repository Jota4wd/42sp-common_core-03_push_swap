
# push_swap

O **push_swap** é um projeto da 42SP focado em **algoritmos de ordenação** e **análise de complexidade**.
O desafio não é apenas ordenar números, mas fazer isso usando um **conjunto extremamente limitado de operações**, buscando sempre o **menor número possível de instruções**.

Em resumo: ordenar é fácil. Ordenar bem é o problema.

---

## 📦 Descrição do projeto

O programa recebe uma lista de inteiros como argumento e imprime, na saída padrão, uma sequência de instruções que ordena esses números em ordem crescente utilizando duas pilhas:

- **Pilha A**: contém os números iniciais
- **Pilha B**: começa vazia e é usada como apoio

As instruções permitidas são apenas as definidas pelo enunciado (`sa`, `pb`, `ra`, `rra`, etc.).
Qualquer solução fora disso não conta — aqui o jogo tem regras claras.

---

## 🧠 Conceitos aprendidos

Durante o desenvolvimento deste projeto, trabalhei principalmente com:

- Estruturas de dados (pilhas / listas encadeadas)
- Algoritmos de ordenação
- Análise de complexidade
- Otimização de número de operações
- Manipulação precisa de memória em C
- Validação rigorosa de argumentos
- Escrita de código limpo seguindo a **Norma da 42**
- Pensar antes de codar (e mesmo assim refatorar depois)

Esse projeto deixa bem claro que **uma solução que funciona nem sempre é uma solução aceitável**.

---

## 🛠️ Compilação

O projeto possui um `Makefile` com as regras obrigatórias.

```bash
make
```
Isso irá gerar o executável:

push_swap

Caso o bônus esteja implementado:

make bonus

▶️ Como usar

O programa recebe uma lista de inteiros como argumento:
```bash
./push_swap 2 1 3 6 5 8
```
Saída esperada (exemplo):

sa
pb
pb
pb
sa
pa
pa
pa


Cada instrução é impressa em uma linha (\n), e nada além disso.

Se os números já estiverem ordenados, o programa não imprime nada.

❌ Tratamento de erros

Em caso de erro, o programa imprime:

Error


Exemplos de erro:

Argumentos não numéricos

Valores fora do limite de int

Números duplicados

Nenhum argumento inválido

Exemplo:
```bash
./push_swap 0 one 2 3
Error
```
🧪 Testes

Teste simples
```bash
./push_swap 3 2 1
```
Testando com o checker

Durante a avaliação, um programa checker é usado para validar se a sequência realmente ordena os números.

Exemplo:
```bash
ARG="4 67 3 87 23"
./push_swap $ARG | ./checker_OS $ARG
```
Se tudo estiver correto:
OK


Se não ordenar corretamente:
KO

📊 Benchmark

O desempenho do programa é avaliado pelo número de operações:

100 números

Excelente: < 700 operações

500 números

Excelente: < 5500 operações

Esses limites são levados em consideração durante a avaliação.
Aqui, cada operação conta — literalmente.

⭐ Bônus

O bônus consiste na implementação de um checker próprio, capaz de:

Ler instruções da entrada padrão

Executar essas instruções sobre as pilhas

Verificar se a pilha A está ordenada ao final

O bônus só é avaliado se a parte obrigatória estiver 100% correta, incluindo os benchmarks.

📁 Estrutura do projeto
```bash
.
├── Makefile
├── push_swap.c
├── src/
├── includes/
│   └── push_swap.h
├── checker/ (bônus)
└── libft/ (se aplicável)
```
🧩 Observações finais

Este projeto faz parte da minha formação na 42SP e está disponível aqui como parte do meu portfólio pessoal.

O foco foi desenvolver uma solução:

Correta
Otimizada
Legível

E dentro das regras (mesmo quando elas parecem injustas)
Se ordenar números fosse fácil, não perguntariam isso em entrevistas 😄
