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
