# Modulo_Ponderada_Semana_8

# Relatório Técnico sobre Ataques MQTT

## Introdução
Este relatório descreve os resultados dos experimentos realizados para testar a segurança do protocolo MQTT, focando em confidencialidade, integridade e disponibilidade. Os testes foram realizados pelo Colab, onde um arquivo eh o usuário e outro simulando um atacante. 

## Configuração
- Cliente MQTT: HiveMQ Websocket Client
- Broker: broker.hivemq.com, Porta: 8000
- Tópico: test/topic12345

## Possíveis Experimentos e Resultados Esperados

### Confidencialidade
**Descrição**: Poderiamos realizar um teste de interceptação de mensagens usando Wireshark.
**Resultado Esperado**: Mensagens foram capturadas em texto claro, expondo dados sensíveis.

### Integridade
**Descrição**: Modificação de mensagens em trânsito.
**Resultado**: Mensagem original `Hello MQTT` foi alterada para `Hello Hacked`, mostrando a vulnerabilidade de integridade.

### Disponibilidade
**Descrição**: Ataque DoS enviando 1000 mensagens rapidamente.
**Resultado**: Broker sobrecarregado, causando desconexões e latência.

## Conclusão
Os experimentos mostraram vulnerabilidades significativas no protocolo MQTT. Recomenda-se a adoção de medidas de segurança, como criptografia TLS, verificações de integridade e limitações de taxa de mensagens para mitigar esses riscos.
Infelizmente não retirei print do terminal antes do ataque e apenas depois, mas o ataque causou indisponibilidade no serviço.
