# Code Review - [Guidelines]

## Motivos para dominar o processo de Code Review

1. ⭐ **Crie um processo melhor**: para ajudar seu time a entregar um software melhor e mais rápido.

2. 📈 **Faça melhores code reviews**: que impulsionam a qualidade do código e eleva as skills de seus colegas.

3. ✅ **Escreva um código melhor**: que é aprovado na primeira review.

### 1. Crie um processo melhor
Capacite seu time a entregar um software de alta qualidade, mais rápido

**Tópicos**
- Por que meu time realiza code reviews?
- Sinais de um processo de code review irregular 🚩
- Como funciona um bom processo de code review 🚢

#### Por que meu time realiza code reviews
  - 😞 Erros
  - 👥 Responsabilidade distribuída
  - 👍 Colaboração
  - 📋 Ensino
 
#### Sinais de um processo de code review irregular 🚩

> 💬 "LGTM! 👍" [3 segundos depois]

> 💬 "Esse código é horrível. Não tem como realizarmos a manutenção do que você escreveu."

> 💬 "Esse método é ilegível, nós devemos refatorar ele."

Outros exemplos:
- Você não tem um processo de code review
- Você tem uma lista grande de pequenos bugs
- Raramente tem comentários em code reviews
- Faz você se tornar ansioso
- É comum 1 PR passar por muitos ciclos de revisão (7+)
- Longas discussões; vai e volta;
- Code reviews são bloqueadas por coisas minuciosas (exemplo estilo de código)

#### Como funciona um bom processo de code review 🚢

- PR precisa ser pequena
  - Mais fácil de revisar
  - Menos risco
  - Tempo efetivo para o autor

- PR precisa ter o escopo adequado
  - Funcional; Incluir testes
  - Passar na build
  - Pode ser realizado o deploy e o rollback de forma segura
 
### Expectativas para o autor e revisor das PR's

#### Boas code reviews - (Expectativas para o `autor`) 🚢

- Incluir o que aquela PR resolve
- Incluir o motivo na descrição da PR
- Extras, se necessário
  - Tarefas relacionadas
  - Cobertura de testes
  - Print de telas
  - Rollback de forma segura
- Marcar os revisores "corretos"
- Impulsionar a resolução de conflitos
- Impulsionar a escrever um código melhor

#### Boas code reviews - (Expectativas para o `revisor`) 🚢

- Exibir autoridade e responsabilidade
- Priorizar a correção dos comentários (evitando levar + de 24/48 horas)
- Favorecer o pragmatismo, e não perfeccionismo
- Ser gentil
- Ser minucioso
- Não comentar code style! Usar linters

- Bloqueio justificado
  - PR muito grande
  - Falhas, gaps de teste, build quebradas
  - Riscos
  - Over-engineering, código e lógicas muito complexas, bibliotecas desnecessárias
 
- Bloqueio injustificado
  - Críticas (especialmente code style)
  - Emergências
  - Utilizar *comentar e aprovar* quando for apropriado

#### Boas code reviews - construção de uma Guideline 🚢
- Documentada no Github, Notion ou Wiki do time - colaboração com o time! (Documento compartilhado)
- Boas guidelines tem:
  - Quando e como abrir uma code review
  - Tamanho e escopo das PR's. Example: `database_migrations`, `bug fix`, `feature`
  - Expectativas para o autor e revisor das PR's
  - PR templates (github description)
  - Quando deve refatorar

#### Key Perfomance Indicators - estamos no caminho?

- Diminuiu o número de bugs
- Diminuiu o número de ciclos de revisões
- Velocidade de um novo dev em onboarding
- Qualidade da discussão na PR

### 2. Faça melhores code reviews
Impulsionar a qualidade do código e elevar as skills do time

**Tópicos**
- O que olhar em uma code review 🔎
- Como realizar uma code review (passo a passo) ⚙
- Escrever comentários eficazes nas code reviews 📝

### O que olhar em uma code review 👀

- Falhas primeiro
- Legibilidade do código
- Oportunidades de aprendizado

O que procurar - Antes de ler o `diff` do código

- Escopo da task
- Build, check, tests
- Conflitos
- Screenshots
- Ela resolve o problema - o problema certo?
- Gaps de regras de negócio
- Mudanças de comportamento inesperadas
- Otimização / perfomance
- Documentação
- Complexidade / over-engineering
- Code Style?
- Efeitos colaterais

O que procurar - Gaps de legibilidade

- Intenção precisa ser óbvia
- Defina nomes significativos
- Convenções
- Implementação e testes

Lembre-se
> *“Any fool can write code that a computer can understand. Good programmers write code that humans can understand.”* — Martin Fowler

### Como realizar uma code review (passo a passo)

- Leia a descrição da code review, e as tasks relacionadas
- Verifique se você é o revisor apropriado
- Reserve um tempo
- Otimização para velocidade ou qualidade?

#### Como revisar (Leia para entender)

- Comece pelo ponto  crucial
- Leia aleatoriamente
- Leia classe por classe depois que você entender
- Procure falhas - você é um detetive

#### Como revisar (Comentando)
- Escreva comentários 
- Reescreva comentários 
- Deixe comentários positivos (quando necessário)
- Faça uma decisão clara sobre aprovação

#### Como revisar (Escreva comentários eficazes)

- Reduzir desentendimentos
- Colegas vão respeitar sua opinião
- Exemplo prático de um bom trabalho

#### Comentário eficazes - `O código, não a pessoa`

> ❌ "Você não checou o valor `null`."

> ✅ "Esse valor do input pode ser `null`, o que vai causar um erro no servidor. Se o valor for `null`, você pode lançar uma exception `client/side`." ou

> ✅ "O que poderia acontecer se for setado um valor `null`?"

#### Comentário eficazes - `Críticas`

> ❌ "Mude o nome da variável."

> ✅ "Mudança, não bloqueante: Eu recomendaria mudar o nome da variável de `purchaseStatus` para `orderStatus`. A variável armazena o status de um pedido, não a compra."

#### Comentário eficazes - `Explique o motivo`

> ❌ "Use o `Promise.all`"

> ✅ "`Promise.all` nesse caso de várias requisições vai rodar todas elas de forma assíncrona e finalizar somente depois de todas terem rodado, otimizando a velocidade do carregamento da página"

#### Comentário eficazes - `Explique o motivo` + `background`

> ❌ "Use o `Promise.all`"

> ✅ "`Promise.all` nesse caso de várias requisições vai rodar todas elas de forma assíncrona e finalizar somente depois de todas terem rodado, otimizando a velocidade do carregamento da página. Para mais contexto: https://dev.to/cristuker/javascript-porque-usar-promiseall-4jc3"

#### Comentário eficazes - `Recap`
- Comente sobre o código, não a pessoa
- Proponha um caminho para seguir, ou colaborar
- Explique os motivos
- Forneça um background

## Referências

- [Master the Code Review](https://curtiseinsmann.gumroad.com/l/code-review-course) (Course)
- [Google's Engineering Practices documentation](https://google.github.io/eng-practices/) (Guide)
- [Dropbox career framework](https://dropbox.github.io/dbx-career-framework/) (Site)
- [There’s a human on the other side of your code review by Tadas Antanavicius](https://medium.com/@tadasant/theres-a-human-on-the-other-side-of-your-code-review-9732cc15bfee) (Post)
- [Implementing a Strong Code-Review Culture by Derek Prior](https://www.youtube.com/watch?v=PJjmw9TRB7s&index=2&list=LLd_50AreJiQvwohSFlvH99w&ab_channel=Confreaks) (Talk)
- [Clean Code como tornar nossos códigos legíveis para seres humanos](https://slides.com/viniciusalonso/clean-code-meetup-guarapuava) (Slides)
- [Master the Code Review - Slides](https://slides.com/renanthompsom/master-the-code-review) (Slides)
