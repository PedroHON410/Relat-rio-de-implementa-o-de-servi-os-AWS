# RELATÓRIO DE IMPLEMENTAÇÃO DE SERVIÇOS AWS

Data: 08/05/2026  
Empresa: Abstergo Industries  
Responsável: Pedro Henrique Oliveira Nascimento

## Introdução
Este relatório apresenta o processo de implementação de ferramentas na empresa Abstergo Industries, realizado por Pedro Henrique Oliveira Nascimento. O objetivo do projeto foi elencar 3 serviços AWS, com a finalidade de realizar diminuição de custos imediatos.

## Descrição do Projeto
O projeto de implementação de ferramentas foi dividido em 3 etapas, cada uma com seus objetivos específicos. A seguir, serão descritas as etapas do projeto:

Etapa 1: 
- **SQS** e **SNS** (Fan-out)
- Permitem comunicação assíncrona e desacoplamento de microsserviços e aplicações, aumentando a resiliência e escalabilidade com alta disponibilidade. Neste modelo, você envia uma mensagem para um tópico **SNS**, que então a replica e distribui para várias filas **SQS** inscritas nesse tópico.
- No sistema, quando um cliente finalizar uma compra, o sistema publica um evento no SNS. Esse evento é enviado para uma fila de Logística (para separar o produto), uma fila de Faturamento (para gerar a nota fiscal) e uma fila de E-mail (para avisar o cliente).

Etapa 2: 
- **EC2** (Comput Cloud) Autoscaling
- Capacidade computacional e redimensionável. Adiciona ou remove automaticamente instâncias, contêineres ou nós do **EC2** com base na demanda, melhorando a disponibilidade e o desempenho do aplicativo. Ele lida com o aumento de tráfego distribuindo a carga entre vários servidores menores.
- Em tempos de alta demanda, evita congestionamente e sobrecarga de máquinas. Também evita compras de máquinas para determinados períodos, tornado elas ociosas em vários períodos.

Etapa 3: 
- **S3** (Simple Storage Service)
-  Armazena de 'objetos' em nuvem da AWS, oferecendo escalabilidade, alta disponibilidade, segurança e desempenho. Projetado para armazenar qualquer tipo de dado (fotos, vídeos, backups). Ajusta automaticamente a capacidade conforme a necessidade, suportando de megabytes a petabytes de dados. Proteção com criptografia em trânsito e em repouso, gerenciamento de acesso e armazenamento em múltiplas zonas de disponibilidade.
- Em caso de queda de sistema ou banco de dados, irá salvar os backups. Também fornece Hospedagem de sites estáticos, armazenamento de dados para aplicativos móveis, IoT, e Data Lakes para análise, tornando viável novas funcionalidades na empresa. 



## Conclusão
A implementação de ferramentas na empresa  Abstergo Industries  tem como esperado diminuição de custos, antecipação de eventuais problemas com dados, possibildade de escalabilidade, o que aumentarão a eficiência e a produtividade da empresa. Recomenda-se a continuidade da utilização das ferramentas implementadas e a busca por novas tecnologias que possam melhorar ainda mais os processos da empresa.

## Anexos
  
- SNS: https://aws.amazon.com/pt/sns/  
- SQS: http://aws.amazon.com/pt/sqs/  
- EC2: https://aws.amazon.com/pt/ec2/autoscaling/  
- S3: https://aws.amazon.com/pt/s3/  

## Assinatura do Responsável pelo Projeto:

Pedro Henrique Oliveira Nascimento
