# Copilot-Studio
Um breve resumo do que é o copilot studio com alguns exemplos praticos
## O que é ?
É uma plataforma da Microsoft para criar chatbots com IA generativa, integrados ao ecossistema do Power Platform. <br>Ele permite que usuários criem assistentes com fluxos lógicos e personalizados, conectando-se a APIs, bancos de dados e outros serviços.
É uma plataforma low-code, ou seja, não é necessário ter um conhecimento prévio na área de programação.

## Itens importantes para a criação do seu agente
### Tópicos:
Definem, basicamente, o que o agente pode conversar, a direção que ele vai seguir de acordo com o que o usuário pedir.
- Estrutura:
    - Frases de gatilho -> Usadas para detectar a intenção do usuário. Normamelnte damos alguns sinônimos para ajudar nosso agente a compreender diferentes formas de pedir a mesma coisa;
    - Fluxo de conversa -> Através de blocos de ação, mensagens, condições, etc. fazemos com que através das respostas do usuário tenhamos respostas para atender suas expectativas e seguir, literalmente, o fluxo da conversa.
- Tipos de tópicos:
    - Tópicos personalizados -> Criados por você;
    - Tópicos de sistema -> Já embutidos na criação do seu copiloto, fornecidos pelo ambiente.
### Entidades:
Usadas para reconhecer e extrair dados importantes da mensagem do usuário.
- Tipos de entidades:
    - Padrão -> Por exemplo: número, moeda, data;
    - Personalizadas -> definidas por você para capturar termos específicos do seu domínio.
###Variáveis
Armazenam informações temporárias durante a conversa. Podem ser usadas para controlar fluxos, passar dados para APIs ou personalizar respostas.
- Tipos de variáveis:
    - De sistema -> criadas automaticamente (ex: nome do usuário);
    - De usuário -> definidas no fluxo (ex: userId, respostaEndereco).
# Exemplo prático 
## Cenário : "Marcar Consulta médica"
### Objetivo do agente: 
Marcar a consulta do usuário após ser informado a especialidade que precisa a data e o horário 
## 1. Tópico: "Agendar consulta"
- Frases de gatilho:
     - "Quero marcar uma consulta"
     - "Preciso de um médico"
     - "Agendar consulta"
## 2. Entidades 
|Entidade | Tipo | Exemplo|
|-------|---------|---------|
|```datetime```| Padrão| "amanhã às 9h"
|```specialty```| Personalizada| "dermatologista"|

# Parte 2 - Um guia prático para aprimorar seu agente
## Passo a passo:
### Como customizar um tópico no Copilot Studio 

#### Vamos customizar nosso agente adicionando tópicos customizados 

1- Indo na aba Tópicos vamos adicionar um novo tópico <br> 
2- Não se esqueça de nomeá-lo de forma intuitiva! Além disso adicione as frases de gatilho<br> 
3-No fluxo de conversa adicionaremos condições, utilizaremos variáveis, para que seja um diálogo fluido

### Como personalizar uma mensagem de erro no tópico 

#### Usamos as mensagens de erro quando:

- O usuário nos dá uma entrada invalida;
- O fluxo não encontra um caminho válido que ele possa seguir;
- Há um erro ao chamar um fluxo externo.
  
#### Como personalizar: 
- Entrada inválida:<br>

1- No passo onde há a pergunta ao usuário, clique no nó da pergunta.<br> 
2- Habilite a opção "Validar resposta".<br>
3- Escolha uma expressão (ex: tipo de dado, regex).<br>
4- Escreva a mensagem personalizada de erro (ex: "Essa especialidade não se encontra no nosso sistema. Tente novamente.").<br>

- Fluxo não encontra caminho: <br>
Sempre termine caminhos com uma mensagem final personalizada, como:
- "Não entendi sua resposta, poderia reformular?"
- "Parece que tivemos um problema técnico. Você pode tentar novamente?"

## Dicas para aumentar a qualidade da resposta com GenAI:
- Seja Claro e Específico no Prompt;
- Defina o papel do seu agente e o tom da resposta que ele deve dar; 
- Use exemplos de entrada e saída;
- Use restrições claras;
- Personalize com variáveis dinâmicas;
- Combine com regras de negócio





    




