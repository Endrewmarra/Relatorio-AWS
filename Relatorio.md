# RELATÓRIO DE IMPLEMENTAÇÃO DE SERVIÇOS AWS

**Data:** 19/01/2026  
**Empresa:** Abstergo Industries  
**Responsável:** Endrew Marra Pedrosa

---

## Introdução

Este relatório apresenta o processo de implementação de serviços em nuvem na empresa **Abstergo Industries**, uma empresa do setor farmacêutico que atua como **hub de comunicação entre redes de farmácias, lojas independentes e outros clientes corporativos**.

O objetivo do projeto foi selecionar e implementar **3 serviços da Amazon Web Services (AWS)** capazes de **otimizar a comunicação, aumentar a confiabilidade das integrações e reduzir custos operacionais**, garantindo escalabilidade e segurança para o crescimento da plataforma.

---

## Descrição do Projeto

O projeto de implementação foi dividido em **3 etapas**, cada uma focada em um pilar essencial da operação: **mensageria, processamento e armazenamento de dados**.

### Etapa 1 – Comunicação e Mensageria Assíncrona

- **Nome da ferramenta:** Amazon Simple Notification Service (SNS)
- **Foco da ferramenta:** Distribuição de mensagens em tempo real
- **Descrição do caso de uso:**  

O Amazon SNS foi utilizado como serviço central de **envio e distribuição de notificações** entre o hub farmacêutico, as farmácias parceiras e outros clientes integrados.

Por meio de tópicos, o sistema consegue enviar mensagens como:
- Atualizações de estoque
- Avisos de pedidos
- Notificações de integração entre sistemas
- Alertas operacionais

O uso do SNS melhora a comunicação ao permitir **mensagens desacopladas**, reduzindo falhas entre sistemas e eliminando a necessidade de conexões diretas entre todas as partes. Além disso, o modelo de pagamento por uso contribui para a **redução de custos**, já que não há necessidade de servidores dedicados para mensageria.

---

### Etapa 2 – Processamento e Integração de Eventos

- **Nome da ferramenta:** AWS Lambda
- **Foco da ferramenta:** Processamento serverless de eventos
- **Descrição do caso de uso:**  

O AWS Lambda foi adotado para processar os eventos recebidos pelo hub de comunicação, como mensagens vindas do SNS ou requisições de APIs externas.

Cada evento (por exemplo, uma atualização de pedido ou confirmação de recebimento) é tratado por funções Lambda específicas, que executam apenas quando necessário. Isso elimina a necessidade de servidores em execução contínua.

Esse modelo melhora a operação ao:
- Reduzir custos com infraestrutura
- Aumentar a escalabilidade automática
- Diminuir o tempo de resposta para integrações
- Facilitar a manutenção do código

O uso de arquitetura serverless é especialmente vantajoso para o setor farmacêutico, onde a demanda pode variar conforme campanhas, períodos sazonais ou volume de pedidos.

---

### Etapa 3 – Armazenamento Seguro e Escalável de Dados

- **Nome da ferramenta:** Amazon DynamoDB
- **Foco da ferramenta:** Banco de dados NoSQL altamente disponível
- **Descrição do caso de uso:**  

O Amazon DynamoDB foi utilizado para armazenar dados operacionais do hub, como:
- Registros de mensagens enviadas
- Status de integrações com farmácias
- Metadados de pedidos e comunicações
- Logs de eventos processados

Por ser um banco de dados totalmente gerenciado, o DynamoDB garante **alta disponibilidade, baixa latência e escalabilidade automática**, sem necessidade de administração manual.

Além disso, o modelo de cobrança baseado em demanda permite que a empresa pague apenas pelo volume de leitura e escrita utilizado, o que gera **economia significativa**, especialmente em ambientes com picos de uso.

---

## Conclusão

A implementação dos serviços **Amazon SNS, AWS Lambda e Amazon DynamoDB** proporciona à **Abstergo Industries** uma arquitetura moderna, escalável e orientada a eventos, ideal para atuar como hub de comunicação no setor farmacêutico.

Os principais benefícios esperados são:
- Melhoria na comunicação entre sistemas
- Redução de custos operacionais
- Alta disponibilidade e escalabilidade
- Facilidade de manutenção e evolução da plataforma

Recomenda-se a continuidade do uso desses serviços, bem como a avaliação de novas soluções AWS que possam fortalecer ainda mais a segurança, a observabilidade e a performance do sistema.

---

## Anexos

- Documentação dos serviços AWS utilizados  
- Diagramas da arquitetura do sistema  
- Políticas de segurança e acesso  

---

**Assinatura do Responsável pelo Projeto:**  

Endrew Marra Pedrosa
