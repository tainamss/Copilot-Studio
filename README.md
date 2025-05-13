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
    




