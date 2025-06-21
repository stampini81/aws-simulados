

### Perguntas e Respostas Detalhadas sobre AWS para Estudo

---

1.  Uma empresa deu início a um processo de migração para a AWS, exigindo que todos os departamentos de sistemas implementem suas aplicações utilizando modelos de infraestrutura pré-definidos pelo time de arquitetos e especialistas, aplicando a técnica de Infraestrutura como Código (IAC). Qual serviço é o mais adequado para ser utilizado neste processo?
    * **AWS CloudFormation**
    * AWS Config
    * Cloud Templates
    * Cloud Stacks

    **Explicação:** O **AWS CloudFormation** permite que você defina a infraestrutura da sua AWS em código (JSON ou YAML). Esses "templates" pré-definidos são ideais para implementar a Infraestrutura como Código (IaC), garantindo consistência e automação no provisionamento de recursos.

---

2.  Para facilitar a localização de informações importantes armazenadas na grande quantidade de conteúdo distribuído na sua empresa, você gostaria que os desenvolvedores adicionassem recursos de pesquisa diretamente em suas aplicações. Qual serviço pode ser utilizado para essa finalidade?
    * Amazon Polly
    * Amazon Comprehend
    * **Amazon Kendra**
    * Amazon Lex

    **Explicação:** O **Amazon Kendra** é um serviço de pesquisa empresarial inteligente que usa machine learning para fornecer resultados de pesquisa altamente precisos em vários repositórios de conteúdo, sendo perfeito para adicionar recursos de pesquisa diretamente em aplicações.

---

3.  Ao usar a AWS, é possível obter descontos proporcionais ao volume, resultando em economias significativas conforme o uso aumenta. Em qual serviço a definição de preço é estruturada em camadas, oferecendo redução no custo por GB à medida que o uso aumenta?
    * Elastic Kubernetes Service (EKS)
    * Elastic Container Service (ECS)
    * Lambda
    * **Simple Storage Service (S3)**

    **Explicação:** O **Amazon S3** é conhecido por sua precificação em camadas, onde o custo por gigabyte armazenado diminui à medida que o volume de dados aumenta, caracterizando um desconto por volume.

---

4.  Qual é o modelo de utilização de nuvem em que não é necessário se preocupar com o gerenciamento dos recursos de infraestrutura tecnológica, permitindo que o foco do cliente esteja principalmente no desenvolvimento das aplicações que serão executadas sobre esses recursos?
    * **PaaS**
    * IaaS
    * SaaS
    * BaaS

    **Explicação:** O **PaaS (Platform as a Service)** fornece um ambiente completo para desenvolvimento e execução de aplicações, abstraindo a infraestrutura subjacente (servidores, sistemas operacionais, rede), permitindo que o cliente foque apenas no código.

---

5.  Qual serviço da AWS permite a execução de contêineres de forma serverless, abstraindo totalmente o gerenciamento da infraestrutura subjacente, incluindo provisionamento, escalabilidade e manutenção de servidores, para que os desenvolvedores possam focar apenas no código e lógica de aplicação?
    * AWS Lambda
    * **AWS Fargate**
    * Amazon Elastic Kubernetes Services (EKS)
    * Amazon Elastic Container Service (ECS)

    **Explicação:** O **AWS Fargate** é um motor de computação serverless que permite executar contêineres Docker sem precisar provisionar ou gerenciar servidores, simplificando drasticamente a operação de cargas de trabalho conteinerizadas.

---

6.  Ao definir um orçamento no AWS Budgets, qual serviço da AWS é encarregado de monitorar os gastos e disparar alarmes para alertar sobre o cumprimento dos limites estabelecidos?
    * AWS Trusted Advisor
    * Amazon EventBridge
    * Amazon CloudTrail
    * **Amazon CloudWatch**

    **Explicação:** O **Amazon CloudWatch** é o serviço de monitoramento da AWS que coleta métricas e logs, e é o responsável por monitorar os gastos definidos no AWS Budgets e disparar os alarmes quando os limites são atingidos.

---

7.  Qual é o serviço de mensagens desenvolvido para Apache ActiveMQ e RabbitMQ que torna as integrações com sistemas legados desacoplados mais fáceis e que permite o uso de arquiteturas híbridas?
    * Amazon SQS
    * Amazon MSK
    * Amazon SNS
    * **Amazon MQ**

    **Explicação:** O **Amazon MQ** é um serviço de broker de mensagens gerenciado compatível com Apache ActiveMQ e RabbitMQ. Ele é ideal para migrar aplicações existentes que usam esses brokers, facilitando integrações com sistemas legados e arquiteturas híbridas sem reescrita de código.

---

8.  Uma organização almeja estabelecer governança nos serviços de TI homologados e aprovados para utilização na AWS, monitorando custos, desempenho, segurança e status operacional desses serviços. Qual é o serviço destinado à criação de catálogos de serviços de TI para atender a esse propósito?
    * AWS Marketplace
    * AWS License Manager
    * AWS Console Manager
    * **AWS Service Catalog**

    **Explicação:** O **AWS Service Catalog** permite que as organizações criem e gerenciem catálogos de serviços de TI aprovados para uso, garantindo que os recursos sejam implantados de forma consistente e em conformidade com as políticas da empresa.

---

9.  Uma empresa foi autuada após uma auditoria que identificou a exposição de arquivos contendo dados sensíveis de clientes em buckets do S3, levantando preocupações sobre vazamento de informações. Qual serviço da AWS pode ser utilizado para monitorar e proteger esses dados, prevenindo futuras exposições e garantindo a conformidade com normas de segurança?
    * AWS GuardDuty
    * **AWS Macie**
    * AWS Sensitive
    * AWS Keys Management Service (KMS)

    **Explicação:** O **Amazon Macie** é um serviço de segurança de dados que usa machine learning para descobrir, classificar e proteger dados sensíveis na AWS, especialmente em buckets do Amazon S3, alertando sobre possíveis exposições.

---

10. Qual dos seguintes itens é de responsabilidade exclusiva da AWS no modelo de responsabilidade compartilhada (shared responsibility model)?
    * Gerenciar imagens customizadas das instâncias do AMI
    * Atualizar patch de segurança em instâncias do clientes
    * **Proteger a infraestrutura global.**
    * Proteger os dados das aplicações dos usuários

    **Explicação:** No modelo de responsabilidade compartilhada, a AWS é responsável pela "segurança da nuvem", o que inclui a **proteção da infraestrutura global** (hardware, software, rede e instalações que executam os serviços). A segurança "na nuvem" (dados do cliente, configurações de OS) é responsabilidade do cliente.

---

11. Quais são os 6 pilares do Well-Architected Framework?
    * **Excelência Operacional, Segurança, Confiabilidade, Desempenho Eficiente, Otimização de Custos, Sustentabilidade**
    * Excelência Operacional, Segurança, Escalabilidade, Desempenho Eficiente, Otimização de Custos, Sustentabilidade
    * Excelência Operacional, Confiabilidade, Escalabilidade, Desempenho Eficiente, Otimização de Custos, Disciplina
    * Excelência Operacional, Segurança, Confiabilidade, Desempenho Eficiente, Escalabilidade, Disciplina

    **Explicação:** Os seis pilares do AWS Well-Architected Framework são: Excelência Operacional, Segurança, Confiabilidade, Eficiência de Performance, Otimização de Custos e Sustentabilidade.

---

12. Clientes na Europa e Austrália enfrentam lentidão no carregamento de imagens em um site cuja infraestrutura está na Região de São Paulo. Qual solução imediata poderia ser implementada para melhorar a performance global, considerando a necessidade de reduzir a latência e otimizar a experiência do usuário?
    * criar uma conta nessas regiões e duplicar a infraestrutura
    * habilitar o Intelligent-Tiering das classes do S3
    * deixar as imagens numa resolução bem baixa
    * **habilitar o CloudFront**

    **Explicação:** O **Amazon CloudFront** é uma Rede de Entrega de Conteúdo (CDN) que armazena cópias de conteúdo (como imagens) em locais de borda próximos aos usuários globais, reduzindo a latência e melhorando a velocidade de carregamento.

---

13. No contexto do modelo de responsabilidade compartilhada, a AWS é responsável pela segurança da infraestrutura global onde os dados são armazenados. O que pode ser afirmado sobre a criptografia utilizada nesse processo?
    * **A AWS criptografa automaticamente os dados na camada física ao armazená-los.**
    * A AWS não criptografa os dados, entretanto fornece o KMS para o cliente fazê-la.
    * A AWS não criptografa os dados, entretanto fornece o ACM para o cliente fazê-la.
    * A AWS criptografa automaticamente somente os dados em trânsito, enquanto os clientes criptografam os dados em repouso.

    **Explicação:** A AWS implementa criptografia na camada física de armazenamento como parte de sua responsabilidade de segurança "da nuvem", protegendo os dados em repouso na infraestrutura subjacente.

---

14. Uma empresa enfrenta problemas em produção com suas aplicações críticas, e a falta de registros detalhados dos componentes está dificultando a equipe de suporte na resolução dos problemas e na restauração das aplicações. Qual serviço da AWS é recomendado para monitorar o ambiente, coletar logs e fornecer informações detalhadas para auxiliar na solução de problemas e no gerenciamento contínuo da infraestrutura?
    * AWS Log
    * AWS Monitor
    * **AWS CloudWatch**
    * AWS CloudTrail

    **Explicação:** O **Amazon CloudWatch** é o serviço principal da AWS para monitoramento e observabilidade, permitindo coletar métricas, logs (via CloudWatch Logs) e configurar alarmes para diagnóstico e solução de problemas.

---

15. Uma das principais vantagens ao optar pela AWS reside nas opções flexíveis de pagamento oferecidas por seus serviços. Qual é o método de pagamento padrão amplamente utilizado na maioria dos serviços da AWS?
    * Pagamento conforme o licenciamento
    * Pagamento conforme a compra
    * Pagamento conforme o contrato
    * **Pagamento conforme o uso**

    **Explicação:** O modelo de "Pagamento conforme o uso" (Pay-as-you-go) é o padrão na AWS, onde você paga apenas pelos recursos que realmente consome, sem compromissos de longo prazo ou pagamentos antecipados.

---

16. Para garantir que os nomes de buckets no Amazon S3 sejam únicos e atendam aos requisitos do serviço, quais são as regras específicas que devem ser seguidas na criação desses nomes? (Selecione 3 alternativas)
    * Devem começar exclusivamente com uma letra
    * **Devem consistir apenas em letras minúsculas, números, pontos (.) e hífens**
    * **Devem começar e terminar com uma letra ou número**
    * **Devem possuir de 3 a 63 caracteres**
    * Devem ser formatados como um endereço IP sempre que possível

    **Explicação:** Os nomes de buckets S3 devem ser globalmente únicos, ter de 3 a 63 caracteres, consistir apenas em letras minúsculas, números, pontos e hífens, e devem começar e terminar com uma letra ou número.

---

17. Qual serviço da AWS pode ser utilizado para mitigar problemas de tráfego de dados dinâmicos causados por congestionamento na Internet, aproveitando a infraestrutura global da AWS?
    * **AWS Global Accelerator**
    * AWS DataSync
    * AWS CloudFront
    * AWS Snowball

    **Explicação:** O **AWS Global Accelerator** melhora a performance e a disponibilidade de aplicações para usuários globais, direcionando o tráfego dinâmico para os pontos de borda da AWS e roteando-o pela rede global da AWS, contornando o congestionamento da Internet pública.

---

18. Uma empresa precisa configurar uma rede virtual isolada para hospedar seus servidores virtuais, separando a camada de dados da camada de servidores de aplicação em sub-redes distintas. Qual serviço da AWS é mais adequado para criar e gerenciar essa infraestrutura, garantindo a segregação apropriada dos recursos em diferentes sub-redes?
    * Elastic Load Balancer (ELB)
    * **Virtual Private Cloud (VPC)**
    * AWS Budget
    * AWS Organizations

    **Explicação:** O **Amazon VPC** permite que você provisione uma seção isolada e logicamente isolada da Nuvem AWS, onde você pode lançar recursos e definir suas próprias sub-redes, tabelas de rotas e segurança de rede.

---

19. Quais são as melhores práticas para implementar o princípio de "projetar para a falha" e assegurar a continuidade e resiliência do sistema mesmo em caso de falhas?
    * Utilizar CloudFront para fazer o cache do conteúdo do sistema
    * Monitorar constantemente o ambiente e enviar alertas de falhar pelo CloudWatch
    * **Implantar o sistema em múltiplas zonas de disponibilidade**
    * Implantar o sistema exclusivamente com o CodeDeploy

    **Explicação:** Implantar o sistema em **múltiplas Zonas de Disponibilidade (AZs)** garante que, se uma AZ falhar, as outras podem assumir a carga, mantendo o sistema disponível e resiliente, o que é fundamental para "projetar para a falha".

---

20. Um administrador de redes atua em um escritório jurídico que lida com uma grande quantidade de contratos de clientes. Estes documentos passam alterações frequentes e demandam um eficiente processo de gerenciamento de versões. Qual serviço da AWS recomenda-se para armazenar esses documentos e atender a esse requisito específico?
    * Amazon EBS
    * **Amazon S3**
    * AWS CodeCommit
    * Git

    **Explicação:** O **Amazon S3** oferece um recurso de **Versionamento** que permite manter várias versões de um objeto (documento), ideal para contratos que sofrem alterações frequentes e exigem histórico e recuperação de versões.

---

21. Uma empresa adquiriu um contrato para obter um pacote com 50 licenças do Microsoft SQL Server, planejando instalar esses softwares em novos servidores conforme expande seus negócios globalmente. Devido às auditorias frequentes, a empresa precisa assegurar que apenas softwares licenciados estejam presentes em sua rede. Qual serviço da AWS simplifica o processo de conformidade nesse cenário?
    * Config
    * Certificate Manager
    * **License Manager**
    * CloudFormation

    **Explicação:** O **AWS License Manager** facilita o gerenciamento de suas licenças de software de fornecedores de terceiros, ajudando a aplicar regras de licença e rastrear o uso para garantir a conformidade.

---

22. Uma organização precisa realizar uma grande quantidade de processos em lote para atualizar informações de clientes, mas não tem uma estimativa clara dos recursos computacionais necessários. Qual serviço da AWS é recomendado para lidar com esse cenário, oferecendo escalabilidade automática e flexibilidade de recursos, sem a necessidade de provisionamento antecipado de infraestrutura?
    * **AWS Batch**
    * AWS Step Functions
    * AWS OnDemand
    * AWS EC2 Reserved

    **Explicação:** O **AWS Batch** é um serviço totalmente gerenciado que permite executar trabalhos de computação em lote em escala. Ele lida com o provisionamento e o gerenciamento dos recursos de computação de forma automática e flexível, sem a necessidade de provisionamento antecipado.

---

23. Uma corretora de investimentos busca estabelecer uma integração eficiente e segura entre seus escritórios em São Paulo, Londres e 2 mil funcionários distribuídos globalmente. Qual serviço da AWS é recomendado para facilitar essa integração de maneira rápida e escalável?
    * AWS Link
    * **AWS VPN**
    * AWS VPC
    * AWS DataSync

    **Explicação:** O **AWS VPN** (Site-to-Site VPN para escritórios e Client VPN para usuários) permite criar conexões seguras e criptografadas entre redes on-premises e a AWS, além de permitir acesso seguro para usuários remotos de forma escalável.

---

24. Qual é o banco de dados sem servidor da AWS que oferece escalabilidade automática, suporte a esquemas flexíveis e é ideal para cargas de trabalho que requerem baixa latência, como jogos e IoT?
    * Aurora
    * **DynamoDB**
    * MariaDB
    * MySQL

    **Explicação:** O **Amazon DynamoDB** é um banco de dados NoSQL totalmente gerenciado e sem servidor, projetado para alta performance, escalabilidade automática e baixa latência, ideal para aplicações com esquemas flexíveis como jogos e IoT.

---

25. Sua empresa faz uso do Apache Kafka no ambiente on-premises para ingestão de logs e processamento de eventos em tempo real. Numa migração da infraestrutura para a AWS, qual serviço pode ser utilizado para manter o uso desta tecnologia de maneira totalmente gerenciada?
    * Amazon KMS
    * Amazon SQS
    * **Amazon MSK**
    * Amazon EKS

    **Explicação:** O **Amazon MSK (Managed Streaming for Apache Kafka)** é um serviço totalmente gerenciado para Apache Kafka, que permite operar clusters Kafka na AWS sem se preocupar com a infraestrutura subjacente, mantendo a compatibilidade com sua tecnologia existente.

---

26. Uma equipe de desenvolvimento de software está encarregada de criar uma pipeline de CI/CD para uma nova aplicação na AWS. Qual serviço específico da AWS deve ser integrado no final da pipeline para automatizar o processo de implantação nos servidores, garantindo uma entrega contínua e segura?
    * **AWS CodeDeploy**
    * AWS Git
    * AWS Deploy
    * AWS CodeCommit

    **Explicação:** O **AWS CodeDeploy** é um serviço de implantação que automatiza a entrega de código para instâncias EC2, servidores on-premises ou funções serverless, sendo o componente de deployment no final de uma pipeline de CI/CD.

---

27. Qual serviço da AWS que além de ajudar na visualização dos cinco serviços que mais oneram os custos de uma conta, também disponibiliza um detalhamento minucioso sobre todos os serviços e custos da conta?
    * AWS Pricing Calculator
    * **AWS Cost Explorer**
    * AWS Trusted Advisor
    * AWS Budget

    **Explicação:** O **AWS Cost Explorer** é a ferramenta para visualizar, entender e gerenciar seus custos e uso da AWS ao longo do tempo, permitindo analisar detalhadamente os gastos por serviço e identificar os maiores contribuidores.

---

28. Uma pequena empresa deseja implementar um site dinâmico em WordPress com despesas mínimas. Qual serviço fornece um servidor privado virtual simples (VPS) de baixo custo que pode satisfazer essa demanda?
    * **Amazon LightSail**
    * Amazon EC2
    * Amazon S3
    * Amazon ECS

    **Explicação:** O **Amazon Lightsail** oferece uma experiência simplificada de servidor privado virtual (VPS) com preços fixos e baixos, incluindo blueprints pré-configurados para aplicações como WordPress, ideal para despesas mínimas.

---

29. Quais dos itens não fazem parte dos pilares do Well-Architected Framework? (Selecione 2 alternativas)
    * Segurança
    * **Elasticidade**
    * Excelência Operacional
    * Sustentabilidade
    * **Desacoplamento**

    **Explicação:** Os 6 pilares são: Excelência Operacional, Segurança, Confiabilidade, Eficiência de Performance, Otimização de Custos e Sustentabilidade. Elasticidade e Desacoplamento são princípios de design importantes, mas não pilares *diretos* do Framework.

---

30. Qual é a maior diferença entre os serviços Amazon RDS e Amazon DynamoDB?
    * RDS é chave e valor, DynamoDB é relacional.
    * RDS é NoSQL, DynamoDB é SQL.
    * **RDS é SQL, DynamoDB é NoSQL.**
    * RDS é gerenciado, DynamoDB não é gerenciado.

    **Explicação:** O **Amazon RDS** é um serviço para bancos de dados **relacionais (SQL)**, enquanto o **Amazon DynamoDB** é um serviço para bancos de dados **NoSQL** (chave-valor e documento). Ambos são gerenciados.

---

31. Qual é o banco de dados NoSQL do tipo chave-valor, totalmente gerenciado pela AWS, que oferece escalabilidade automática e é ideal para aplicações com alta demanda de leitura e escrita?
    * RDS MySQL
    * **DynamoDB**
    * Amazon KeySpaces
    * Aurora

    **Explicação:** O **Amazon DynamoDB** é um banco de dados NoSQL (chave-valor e documento) totalmente gerenciado, conhecido por sua escalabilidade automática e desempenho de milissegundos de dígito único para cargas de trabalho de alta demanda.

---

32. Qual é o plano de suporte recomendado se você é um desenvolvedor e está experimentando ou testando na AWS?
    * **Developer**
    * Enterprise
    * Business
    * Basic

    **Explicação:** O plano **Developer** é o mais adequado para desenvolvedores que estão experimentando e testando na AWS, oferecendo suporte técnico por e-mail durante o horário comercial.

---

33. Você trabalha numa grande organização que utiliza o AWS Control Tower. Qual é a principal função deste serviço?
    * Realizar análise de big data em tempo real na AWS.
    * **Fornecer recursos de gerenciamento centralizado e governança para contas na AWS.**
    * Gerenciar a segurança de dispositivos IoT na AWS.
    * Hospedar sites da web na AWS.

    **Explicação:** O **AWS Control Tower** facilita a configuração e o gerenciamento de um ambiente AWS multi-contas seguro e compatível, estabelecendo uma "landing zone" com governança e gestão centralizada.

---

34. Uma startup brasileira precisa garantir alta disponibilidade, resiliência e performance para uma aplicação crítica usando o Amazon RDS. Quais configurações devem ser implementadas para assegurar a implementação destes requisitos?
    * **Multi AZ (Distribuir os bancos de dados em mais de uma zona de disponibilidade na mesma região)**
    * **Read Replicas (Utilizar cópias de leitura dos bancos de dados)**
    * Multi Regions (Distribuir os bancos de dados em mais de uma região)
    * Criar um Security Group para isolar apenas os bancos de dados da aplicação.

    **Explicação:** **Multi-AZ** garante alta disponibilidade e resiliência (failover automático em caso de falha de AZ), enquanto **Read Replicas** melhoram a performance ao descarregar as operações de leitura da instância principal, permitindo escalabilidade de leitura.

---

35. Uma equipe de desenvolvimento backend iniciou o uso do API Gateway para a implementação de novas APIs para um projeto na AWS. Considerando as funcionalidades e os recursos avançados oferecidos pelo API Gateway, quais das seguintes opções destacam suas principais finalidades? (Selecione 2 alternativas)
    * Balanceamento de carga.
    * **Criação de APIs RESTful e WebSocket.**
    * Criação e Contenirização de microsserviços.
    * **Publicação, manutenção e monitoramento de APIs.**
    * Criação e execução de funções sem servidores.

    **Explicação:** O **Amazon API Gateway** é usado para criar e gerenciar APIs (RESTful e WebSocket), incluindo sua publicação, manutenção de versões e monitoramento de desempenho e uso.

---

36. Uma equipe de desenvolvimento precisa redesenhar um sistema para modernizá-lo na AWS. Um dos requisitos não funcionais é reduzir a interdependência entre os microsserviços para minimizar o impacto de possíveis falhas. Qual dos seguintes conceitos deve ser aplicado para alcançar esse objetivo?
    * Segregação
    * Agregação
    * Escalabilidade
    * **Desacoplamento**

    **Explicação:** O **Desacoplamento** é um princípio de design fundamental para microsserviços, que visa reduzir as dependências diretas entre os componentes, isolando falhas e aumentando a resiliência do sistema.

---

37. Qual é o serviço da AWS que permite a migração eficiente e segura de dados entre bancos de dados, suportando uma ampla gama de tipos de bancos de dados, tanto relacionais quanto não relacionais, e que também oferece a capacidade de realizar migrações contínuas com mínima interrupção do serviço?
    * AWS Snow
    * AWS Connect
    * AWS Glue
    * **AWS Data Migration Service (DMS)**

    **Explicação:** O **AWS Data Migration Service (DMS)** é um serviço especializado para migrar dados entre diversos tipos de bancos de dados (homogêneos e heterogêneos), suportando migrações contínuas com replicação de dados (CDC) para minimizar o tempo de inatividade.

---

38. Quais fatores são considerados para calcular o Total Cost of Ownership (TCO) numa migração para a AWS?
    * custos de infraestrutura de hardware, manutenção e suporte, consumo de energia, custos de treinamentos e administração de sistemas.
    * custos de infraestrutura de hardware, manutenção e suporte, consumo de energia, custos operacionais como mão de obra e linguagens de programação.
    * **custos de infraestrutura de hardware, manutenção e suporte, consumo de energia, custos operacionais como mão de obra e administração de sistemas.**
    * custos de infraestrutura de hardware, manutenção e suporte, consumo de energia, custos operacionais como mão de obra e satisfação dos usuários finais.

    **Explicação:** O TCO abrange os custos diretos (hardware, energia, manutenção) e indiretos (mão de obra, administração de sistemas, treinamento) associados à infraestrutura e sua gestão.

---

39. Um desenvolvedor pretende criar uma aplicação utilizando Java ou C# e busca integrar suas funcionalidades com serviços da AWS. Qual conjunto de ferramentas e bibliotecas da AWS ele deve utilizar para facilitar essa integração, permitindo o uso de APIs e serviços da nuvem de forma otimizada para essas linguagens de programação?
    * AWS CLI
    * **AWS SDK**
    * AWS CodeDeveloper
    * AWS Console

    **Explicação:** O **AWS SDK (Software Development Kit)** fornece bibliotecas e ferramentas específicas para diversas linguagens de programação (incluindo Java e C#) que facilitam a interação programática com os serviços da AWS.

---

40. Qual banco de dados SQL da AWS é projetado para garantir uma disponibilidade de 99,99% ou superior, realizando replicação automática de seis cópias dos dados em três zonas de disponibilidade distintas, e utilizando o Amazon S3 para backups contínuos e duráveis?
    * DynamoDB
    * **Aurora**
    * MariaDB
    * MySQL

    **Explicação:** O **Amazon Aurora** é um banco de dados relacional (SQL) com uma arquitetura de armazenamento que replica automaticamente seis cópias dos dados em três zonas de disponibilidade e usa o S3 para backups contínuos, garantindo alta durabilidade e disponibilidade.

---

41. Ao definir uma estratégia de backup robusta para bancos de dados utilizando o Amazon RDS, é crucial considerar o limite imposto pela AWS para snapshots manuais por região. Além de gerenciar a retenção de dados e otimização de custos de armazenamento, qual é o número máximo de snapshots manuais permitidos por região?
    * **100 snapshots por região**
    * o número de cópia é virtualmente ilimitado
    * 128 snapshots por região
    * 256 snapshots por região

    **Explicação:** O limite de snapshots manuais no Amazon RDS é de **100 por região**, o que deve ser considerado no planejamento de backups e retenção de dados.

---

42. Um banco está desenvolvendo um microsserviço para realizar análises de crédito solicitadas por clientes. Os resultados dessas análises precisam ser enviados para sistemas de vendas, de empréstimos e para um serviço de log interno. Qual serviço da AWS é mais adequado para facilitar essas integrações de forma rápida e eficiente, permitindo futuras expansões?
    * AWS SES
    * **AWS SNS**
    * AWS ECS
    * AWS Lambda

    **Explicação:** O **Amazon SNS (Simple Notification Service)** é um serviço de publicação/assinatura (pub/sub) que permite enviar mensagens para múltiplos "assinantes" (sistemas de vendas, empréstimos, log) de forma desacoplada e escalável, ideal para integração e futuras expansões.

---

43. Por que é necessário associar um Elastic Block Store (EBS) a uma instância EC2?
    * **Para fornecer armazenamento persistente e escalável para a instância.**
    * Para permitir redundância computacional da instância.
    * Para que os dados sejam criptografados na instância.
    * Para deixar o fluxo de transmissão de dados mais rápido na instância.

    **Explicação:** O **Amazon EBS** fornece volumes de armazenamento persistentes em nível de bloco que podem ser anexados a instâncias EC2, garantindo que os dados não sejam perdidos quando a instância é interrompida ou encerrada, além de ser escalável em tamanho e desempenho.

---

44. Sua empresa começou a utilizar a AWS e precisa conceder acessos a 100 funcionários. Considerando que o time é composto por desenvolvedores, DBAs e arquitetos, e que cada grupo precisa de permissões específicas para diferentes recursos, qual serviço da AWS você escolheria para gerenciar esses acessos de forma eficiente?
    * IAM Roles
    * **IAM Grupos**
    * AWS Organizations
    * Amazon Cognito

    **Explicação:** Os **IAM Grupos** permitem organizar usuários com funções semelhantes e anexar políticas de permissão aos grupos, simplificando o gerenciamento de acesso para um grande número de funcionários com permissões específicas por função.

---

45. Uma empresa está desenvolvendo uma nova plataforma para a distribuição global de vídeos. Qual serviço pode reduzir a latência entre a solicitação e a entrega do serviço para essa solução?
    * Amazon Kinesis
    * Amazon ElasticCache
    * Amazon S3
    * **Amazon CloudFront**

    **Explicação:** O **Amazon CloudFront** é uma CDN que usa uma rede global de *edge locations* para armazenar em cache e entregar conteúdo (como vídeos) aos usuários a partir do local mais próximo, reduzindo significativamente a latência.

---

46. Uma empresa desenvolveu uma aplicação hospedada no Amazon EC2 que precisa se conectar de forma segura e eficiente a um banco de dados no Amazon RDS. Para garantir uma comunicação segura e a configuração adequada de acesso entre a aplicação e o banco de dados, qual serviço da AWS deve ser implementado?
    * IAM Groups
    * **IAM Roles**
    * IAM Users
    * IAM Grant

    **Explicação:** **IAM Roles** são a maneira mais segura e recomendada para conceder permissões a instâncias EC2, permitindo que elas acessem outros serviços da AWS (como RDS) usando credenciais temporárias, sem a necessidade de armazenar credenciais de longo prazo na instância.

---

47. Qual é a plataforma da AWS para Big Data em Cloud que permite integração com várias ferramentas de código livre como Apache Spark, Apache Hive, Apache HBase, Apache Flink, Apache Hudi?
    * **Amazon EMR**
    * Amazon Hadoop
    * Amazon Redshift
    * Amazon Kinesis

    **Explicação:** O **Amazon EMR (Elastic MapReduce)** é um serviço de cluster gerenciado que facilita a execução de frameworks de big data de código aberto como Apache Spark, Hive, HBase, Flink e Hudi em escala na AWS.

---

48. Em cenários de migração para a AWS, como as empresas podem aplicar o AWS Application Discovery Service para auxiliá-las?
    * Para armazenar backups de dados.
    * Para criar aplicativos móveis para clientes.
    * **Para identificar e avaliar as dependências de aplicativos e servidores locais.**
    * Para gerar relatórios de custos.

    **Explicação:** O **AWS Application Discovery Service** coleta dados sobre servidores e aplicações on-premises, incluindo suas dependências, para ajudar no planejamento e na execução de migrações para a AWS.

---

49. Uma empresa containerizou dois microsserviços com padrões de carga variáveis: um tem picos de acesso pela manhã e o outro à tarde. Para garantir escalabilidade automatizada e uso eficiente dos recursos, quais serviços da AWS podem orquestrar e ajustar dinamicamente os recursos conforme as variações de carga?
    * Elastic Compute Cloud (EC2) ou Elastic Kubernetes Service (EKS)
    * Elastic Container Register (ECR) ou Elastic Container Service (ECS)
    * Lambda ou Elastic Kubernetes Service (EKS)
    * **Elastic Kubernetes Service (EKS) ou Elastic Container Service (ECS)**

    **Explicação:** Tanto o **Amazon EKS** quanto o **Amazon ECS** são orquestradores de contêineres que fornecem capacidades de escalabilidade automática para gerenciar e ajustar dinamicamente os recursos de microsserviços conteinerizados com base na demanda.

---

50. Você precisa criar pequenos scripts para automatizar a administração de uma aplicação em servidores Linux na AWS. Qual serviço pode ser utilizado para essa finalidade através de um navegador?
    * AWS IQ
    * **AWS CloudShell**
    * AWS Cloud9
    * AWS Device Farm

    **Explicação:** O **AWS CloudShell** é um shell baseado em navegador que oferece um ambiente Linux pré-autenticado com ferramentas AWS (como AWS CLI) para gerenciar recursos e executar scripts, ideal para administração rápida via navegador.

---

51. Uma empresa encontra-se atualmente em processo de avaliação do uso do banco de dados DynamoDB, buscando compreender as diversas oportunidades relacionadas ao seu uso. Qual das seguintes opções NÃO representa uma característica deste serviço?
    * é um banco de dados de chave-valor e documentos
    * **É um banco de dados cobrado por MB na solicitação de gravação e leitura**
    * É um banco de dados totalmente gerenciado
    * É um banco de dados sem servidor

    **Explicação:** O DynamoDB é cobrado principalmente por **Unidades de Capacidade de Leitura (RCUs)** e **Unidades de Capacidade de Gravação (WCUs)**, além do armazenamento, e não diretamente por MB na solicitação de gravação e leitura.

---

52. Quais opções representam recursos fundamentais do AWS Cloud Adoption Framework (AWS CAF) para a perspectiva de segurança? (Selecione 3)
    * **Proteção de dados com criptografia em repouso e em trânsito.**
    * **Monitoramento de atividades e auditoria de logs de segurança.**
    * Automação de respostas a eventos de segurança.
    * **Implementação de controles de acesso baseados em identidade.**
    * Planejamento de capacidade e desempenho.

    **Explicação:** As perspectivas de segurança do AWS CAF incluem proteção de dados (com criptografia), monitoramento e auditoria de logs, e gerenciamento de acesso baseado em identidade.

---

53. Quais são as possíveis utilizações do AWS CLI (Command Line Interface) após o correto download, instalação e configuração deste serviço em seu computador? (Selecione 2 alternativas)
    * **Automatizar serviços da AWS**
    * Visualização de Dashboards Personalizados
    * **Controlar múltiplos serviços da AWS**
    * Criação de Grupos de Recursos Personalizados no Console do AWS Management
    * Visualizar gráficos de Custo de serviços da AWS

    **Explicação:** O AWS CLI permite controlar e automatizar a interação com múltiplos serviços da AWS através de comandos de linha e scripts.

---

54. Qual medida de segurança avançada você implementaria para fortalecer a proteção da sua conta AWS contra acessos não autorizados e garantir a integridade dos recursos críticos?
    * Habilitar o AWS Key Management Service (KMS)
    * Habilitar o AWS Secrets Manager
    * **Habilitar a Autenticação Multifator - Multi-Factor Authentication (MFA)**
    * Habilitar o AWS Certificate Manager

    **Explicação:** A **Autenticação Multifator (MFA)** adiciona uma camada essencial de segurança ao exigir um segundo fator de verificação para o login, protegendo contra acessos não autorizados mesmo que a senha seja comprometida.

---

55. Quais são as principais funções do AWS Glue? (Selecione 3 alternativas)
    * Criptografar dados
    * **Transformar dados**
    * Arquivar dados
    * **Extrair dados**
    * **Carregar dados**

    **Explicação:** O AWS Glue é um serviço de ETL (Extract, Transform, Load) totalmente gerenciado, cujas funções primárias são Extrair, Transformar e Carregar dados para análise.

---

56. Quais planos de suporte da AWS incluem acesso completo ao AWS Trusted Advisor, que oferece recomendações para otimizar o uso de recursos e seguir as melhores práticas de segurança e eficiência?
    * Basic, Developer, Business, Enterprise OnRamp e Enterprise
    * Enterprise OnRamp e Enterprise
    * Developer, Business, Enterprise OnRamp e Enterprise
    * **Business, Enterprise OnRamp e Enterprise**

    **Explicação:** O acesso completo a todas as verificações do AWS Trusted Advisor está disponível a partir do plano **Business**, incluindo também os planos Enterprise OnRamp e Enterprise.

---

57. Para desenvolver uma solução que permita a uma aplicação escalonar automaticamente conforme a demanda, quais serviços da AWS são essenciais? (Selecione 2 alternativas)
    * **Auto Scaling Group (ASG)**
    * **Elastic Load Balancer (ELB)**
    * CloudFormation
    * Route 53
    * CloudFront

    **Explicação:** O **Auto Scaling Group (ASG)** é responsável por adicionar ou remover instâncias automaticamente com base na demanda, e o **Elastic Load Balancer (ELB)** distribui o tráfego de entrada entre essas instâncias escaláveis, garantindo alta disponibilidade e eficiência.

---

58. Se você deseja realizar um gerenciamento total do seu banco de dados, qual é o serviço mais indicado para implementá-lo?
    * **EC2**
    * RDS
    * DynamoDB
    * DocumentDB

    **Explicação:** A execução de um banco de dados em uma instância **Amazon EC2** oferece o controle mais granular sobre o sistema operacional, software de banco de dados, patching, backups e escalabilidade, ou seja, um gerenciamento total pelo cliente.

---

59. No modelo de Responsabilidade Compartilhada, a AWS e o cliente têm responsabilidades distintas para a segurança da infraestrutura e dos dados. Qual é a função específica desempenhada pela AWS nesse modelo? (Selecione 2 alternativas)
    * Proteger o acesso aos dados das aplicações dos usuários
    * **Realizar a manutenção dos hardwares**
    * Atualizar o Sistema Operacional das Instâncias EC2
    * **Proteger os data centers**

    **Explicação:** A AWS é responsável pela "segurança da nuvem", que inclui a manutenção da infraestrutura física (hardwares) e a proteção das instalações (data centers).

---

60. A Amazon oferece várias classes de armazenamento no S3 específicas para cada tipo de uso. Qual das opções abaixo são classes existentes no serviço? (Selecione 3)
    * S3 Business
    * S3 Enterprise
    * **S3 Standard**
    * **S3 Intelligent-Tiering**
    * **S3 Standard Infrequent Access**

    **Explicação:** As classes de armazenamento do Amazon S3 incluem S3 Standard, S3 Intelligent-Tiering, S3 Standard-IA (Standard Infrequent Access), S3 One Zone-IA, S3 Glacier Instant Retrieval, S3 Glacier Flexible Retrieval e S3 Glacier Deep Archive.

---

61. Selecione as afirmações verdadeiras sobre o AWS Identity and Access Management (IAM), o serviço que permite gerenciar o acesso aos recursos da AWS de forma segura. (Selecione 3 alternativas)
    * **Oferece autenticação multifator (MFA) para aumentar a segurança das contas.**
    * Necessita de uma conta root para criar novos usuários e grupos.
    * **Suporta a integração com provedores de identidade externos para autenticação federada.**
    * **Permite a criação de políticas (policies) de controle de acesso detalhadas para usuários e grupos.**
    * Não permite a delegação de permissões específicas para serviços da AWS.

    **Explicação:** O IAM oferece MFA, suporta federação de identidade e permite a criação de políticas de acesso detalhadas. Não é necessário a conta root para criar usuários/grupos (se o usuário IAM tiver permissão), e ele permite delegação de permissões via Roles.

---

62. Qual é a diferença entre o AWS Web Application Firewall (WAF) e o AWS Firewall Manager em termos de funcionalidade e finalidade?
    * O WAF é usado para gerenciar políticas de segurança de firewall em várias contas, enquanto o Firewall Manager é usado para proteger aplicativos web.
    * **O WAF é um serviço para bloquear ataques de aplicativos web, enquanto o Firewall Manager é uma solução para gerenciar regras de firewall em várias contas.**
    * O WAF é uma solução centralizada para gerenciar regras de firewall em várias contas, enquanto o Firewall Manager é focado em proteger aplicativos web contra ataques.
    * Não há diferença significativa entre o WAF e o Firewall Manager em termos de funcionalidade e finalidade.

    **Explicação:** O **AWS WAF** protege aplicações web contra ataques comuns (Camada 7), enquanto o **AWS Firewall Manager** centraliza o gerenciamento e a aplicação de políticas de firewall (incluindo WAF) em várias contas da AWS.

---

63. O que pode-se afirmar sobre o AWS Budgets? (Selecione 3 alternativas)
    * **Pode ser utilizado para criar e gerenciar orçamentos.**
    * Pode enviar notificações para até 5 destinatários de e-mail no máximo.
    * Pode calcular e estimar os custos dos serviços da AWS.
    * **Pode ser utilizados para refinar e filtrar orçamentos.**
    * **Pode ser utilizado para enviar alertas para te ajudar no controle do uso dos serviços da sua conta.**

    **Explicação:** O AWS Budgets permite criar, gerenciar, filtrar orçamentos e enviar alertas sobre seus custos e uso, mas não calcula ou estima custos para serviços *antes* do uso (isso é feito pelo Pricing Calculator).

---

64. Qual é o modelo de planos flexíveis que oferece preços mais vantajosos em comparação com outros modelos de tarifação, exigindo um compromisso de uso específico em dólares por hora por um período de um ou três anos, independentemente da região, tipo de instância ou serviço AWS, como EC2, Fargate e Lambda?
    * Spot
    * Sob Demanda (On-Demand)
    * Reservada (Reserved)
    * **Savings Plans**

    **Explicação:** Os **Savings Plans** oferecem descontos significativos em troca de um compromisso de gasto por hora (em USD) por 1 ou 3 anos, com flexibilidade entre regiões, tipos de instância e serviços como EC2, Fargate e Lambda.

---

65. Uma corporação global com clientes distribuídos em praticamente todos os países pretende adotar a AWS como sua nova provedora de serviços de computação em nuvem. Qual é o principal benefício imediato para os clientes dessa empresa ao utilizar a AWS?
    * Suporte ao usuário final
    * Suporte em mais de 50 idiomas
    * **Presença Global**
    * Documentações bem traduzidas em 50 idiomas

    **Explicação:** A **Presença Global** da AWS (suas regiões e *edge locations* distribuídas mundialmente) permite que a corporação hospede seus serviços mais próximos de seus clientes finais, resultando em menor latência e uma melhor experiência de usuário.

---
