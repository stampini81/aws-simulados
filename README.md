
### Pergunta 1
Qual das classes a seguir pode resultar em custos mais elevados no uso do S3?
Glacier
Glacier Deep Arquive
Standard Infrequent Access
Standard

[cite_start]**Resposta:** Glacier e Glacier Deep Archive [cite: 2]

**Explicação:** Glacier e Glacier Deep Archive são classes de armazenamento do S3 que **podem resultar em custos mais elevados** se você precisar acessar os dados frequentemente ou rapidamente. [cite_start]Embora o custo por GB armazenado seja muito baixo, as taxas de recuperação de dados são significativas e podem se acumular rapidamente[cite: 3].

* [cite_start]**Glacier**: Esta classe é otimizada para arquivamento de dados de longo prazo que são acessados raramente[cite: 4]. [cite_start]Os custos de armazenamento são baixos, mas os custos de recuperação são mais altos e o tempo de recuperação pode variar de minutos a horas[cite: 5].
* [cite_start]**Glacier Deep Archive**: A classe mais barata para armazenamento de longo prazo, projetada para dados que podem ser acessados apenas uma ou duas vezes por ano[cite: 6]. [cite_start]Os custos de armazenamento são mínimos, mas os custos e tempos de recuperação são os mais altos[cite: 7].
* [cite_start]**Standard Infrequent Access (S3 IA)**: Ideal para dados que são acessados com menos frequência, mas que exigem acesso rápido quando necessário[cite: 8]. [cite_start]Os custos de armazenamento são menores que o S3 Standard, mas há uma taxa de recuperação por GB[cite: 9].
* [cite_start]**Standard (S3 Standard)**: Esta é a classe de uso geral, ideal para dados acessados com frequência[cite: 10]. [cite_start]Oferece alta durabilidade, disponibilidade e desempenho, mas tem o custo de armazenamento mais alto por GB em comparação com as outras classes[cite: 11].

[cite_start]Em resumo, a escolha da classe S3 que pode resultar em custos mais elevados depende do seu padrão de acesso aos dados: Se você acessa os dados frequentemente, o Glacier e o Glacier Deep Archive resultarão em custos muito mais altos devido às taxas de recuperação[cite: 12]. [cite_start]As classes Glacier e Glacier Deep Archive têm o maior potencial para custos elevados inesperados devido às taxas de recuperação significativas se os dados forem acessados com mais frequência do que o pretendido para essas classes[cite: 15].
```

```markdown
### Pergunta 2
Um time de desenvolvimento detectou baixo desempenho em um banco de dados relacional. A concorrência entre um alto volume de consultas e outras operações no banco de dados tem elevado a latência no tráfego de dados.
Qual é a abordagem mais eficiente e econômica para solucionar esse problema?
Atualizar a role de acesso ao banco de dados.
Utilizar Read Replicas
Criar novas instâncias do RDS em outra zona de disponibilidade.
Substituir o RDS pelo Dynamo.

[cite_start]**Resposta:** Utilizar Read Replicas [cite: 20]

[cite_start]**Explicação:** A abordagem mais **eficiente e econômica** para resolver o problema de baixo desempenho devido à alta concorrência em um banco de dados relacional é **Utilizar Read Replicas**[cite: 20].

* [cite_start]**Eficiência na Distribuição de Carga:** Read Replicas (ou Réplicas de Leitura) criam cópias somente leitura do seu banco de dados principal[cite: 21]. [cite_start]Isso permite que as consultas de leitura, que geralmente representam a maior parte do tráfego em muitas aplicações, sejam direcionadas para essas réplicas[cite: 22]. [cite_start]Dessa forma, o banco de dados principal fica mais livre para lidar com operações de escrita e outras operações que exigem mais recursos, reduzindo a concorrência e a latência[cite: 23].
* [cite_start]**Economia:** Em comparação com as outras opções, implementar Read Replicas geralmente é mais econômico[cite: 24]. [cite_start]Você não precisa provisionar um banco de dados completamente novo e as réplicas são otimizadas para leitura, o que pode resultar em custos de instância menores do que um banco de dados principal[cite: 25].
* [cite_start]**Escalabilidade:** As Read Replicas permitem que você escale horizontalmente a capacidade de leitura do seu banco de dados, adicionando mais réplicas conforme a demanda aumenta[cite: 26].

**Por que as outras opções não são as ideais?**
* [cite_start]**Atualizar a role de acesso ao banco de dados:** Alterar as permissões de acesso não resolverá um problema de desempenho causado por alta concorrência de consultas[cite: 27]. [cite_start]Isso está relacionado à segurança e controle de quem pode acessar o banco de dados, não à sua capacidade de processamento[cite: 28].
* [cite_start]**Criar novas instâncias do RDS em outra zona de disponibilidade:** Embora isso aumente a disponibilidade e a resiliência a falhas, não resolve diretamente o problema de concorrência e latência para operações de leitura[cite: 29]. [cite_start]As operações de escrita ainda seriam direcionadas para a instância principal, e as leituras, se não forem distribuídas, ainda poderiam sobrecarregá-la[cite: 30]. [cite_start]Além disso, ter uma nova instância completa é geralmente mais caro do que uma Read Replica[cite: 31].
* [cite_start]**Substituir o RDS pelo DynamoDB:** O DynamoDB é um banco de dados NoSQL e a migração de um banco de dados relacional para NoSQL é uma mudança arquitetural significativa[cite: 32]. [cite_start]Ela exigiria uma reengenharia da aplicação, o que é um processo **caro, demorado e complexo**, e nem sempre a abordagem NoSQL é a mais adequada para todos os tipos de dados e consultas relacionais[cite: 33]. [cite_start]Portanto, não é uma solução eficiente nem econômica para o problema imediato de desempenho em um banco de dados relacional existente[cite: 34].
```

```markdown
### Pergunta 3
Autenticação Multi Fator)?
Um serviço que permite a conexão entre a máquina do cliente e um servidor na AWS através de um arquivo contendo key pairs (par de chaves).
Um serviço que inclui uma etapa a mais no processo de autenticação de acesso a conta da AWS através do Console Web.
Um serviço para permitir que instâncias EC2 acessem banco de dados DynamoDb.
Um serviço que utiliza key pairs (par de chaves) na autenticação do usuário através da CLI (Linha de Comando)

[cite_start]**Resposta:** Um serviço que inclui uma etapa a mais no processo de autenticação de acesso a conta da AWS através do Console Web [cite: 39]

[cite_start]**Explicação:** A **Autenticação Multifator (MFA)** é um serviço que **inclui uma etapa a mais no processo de autenticação de acesso à conta da AWS através do Console Web**[cite: 39].

* [cite_start]**Entendendo a Autenticação Multifator (MFA):** A MFA é uma medida de segurança que exige que os usuários forneçam duas ou mais evidências (fatores) para verificar sua identidade antes de conceder acesso[cite: 40]. [cite_start]Na AWS, isso geralmente significa "Algo que você sabe" (Sua senha) [cite: 41] [cite_start]e "Algo que você tem" (Um dispositivo MFA como token ou aplicativo)[cite: 42]. [cite_start]Ao exigir essa segunda etapa, a MFA aumenta significativamente a segurança da sua conta, mesmo que sua senha seja comprometida[cite: 43].

**Por que as outras opções estão incorretas?**
* "Um serviço que permite a conexão entre a máquina do cliente e um servidor na AWS através de um arquivo contendo key pairs (par de chaves)." [cite_start]Esta descrição se refere principalmente ao uso de pares de chaves SSH para acessar instâncias EC2, não à autenticação da conta da AWS[cite: 45].
* "Um serviço para permitir que instâncias EC2 acessem banco de dados DynamoDB." [cite_start]Isso é geralmente configurado usando **perfis de instância (Instance Profiles)** e **funções do IAM (IAM Roles)**, que concedem permissões às instâncias EC2 para acessar outros serviços da AWS[cite: 47]. [cite_start]Não tem relação direta com a autenticação de login do usuário na conta[cite: 48].
* "Um serviço que utiliza key pairs (par de chaves) na autenticação do usuário através da CLI (Linha de Comando)." [cite_start]Embora as chaves de acesso (access keys) sejam usadas para autenticar usuários e aplicativos na AWS CLI e via SDKs, essa descrição não aborda a "segunda etapa" da autenticação que a MFA oferece[cite: 50].
```

```markdown
### Pergunta 4
Qual usuário possui acesso a todos os recursos da conta, que é utilizado para acessar o AWS Console pela primeira vez, mas que não é recomendado para uso no dia a dia?

[cite_start]**Resposta:** O usuário root da conta AWS (AWS account root user) [cite: 54]

[cite_start]**Explicação:** O usuário que possui acesso a todos os recursos da conta e é utilizado para acessar o AWS Console pela primeira vez, mas que **não é recomendado para uso no dia a dia**, é o **usuário root da conta AWS (AWS account root user)**[cite: 54].

**Por que o usuário root não é recomendado para uso diário?**
* [cite_start]**Acesso Irrestrito:** O usuário root tem permissões ilimitadas sobre todos os recursos da sua conta AWS, incluindo informações de faturamento e a capacidade de encerrar a conta[cite: 56]. [cite_start]Qualquer erro ou comprometimento desse usuário pode ter consequências catastróficas[cite: 57].
* [cite_start]**Princípio do Privilégio Mínimo:** A AWS e as melhores práticas de segurança recomendam sempre operar com o princípio do privilégio mínimo[cite: 58]. [cite_start]O usuário root viola esse princípio ao ter acesso total o tempo todo[cite: 60].
* [cite_start]**Risco de Segurança:** Usar o usuário root para tarefas diárias aumenta a superfície de ataque da sua conta[cite: 61]. [cite_start]Se as credenciais do usuário root forem comprometidas, um atacante teria controle total sobre sua infraestrutura e dados na AWS[cite: 62].

**Boas Práticas de Segurança com o Usuário Root:**
* [cite_start]**Proteja as Credenciais:** Use uma senha forte e única para o usuário root[cite: 63].
* [cite_start]**Ative o MFA (Multi-Factor Authentication):** **Sempre** ative a Autenticação Multifator (MFA) para o usuário root[cite: 64]. [cite_start]Isso adiciona uma camada extra de segurança[cite: 65].
* [cite_start]**Armazene as Credenciais com Segurança:** Armazene as credenciais do usuário root em um local extremamente seguro e acessível apenas em situações de emergência[cite: 66].
* [cite_start]**Crie Usuários IAM (IAM Users) para o Dia a Dia:** Após a criação da conta, crie usuários IAM com permissões específicas para as tarefas diárias[cite: 67].
* [cite_start]**Evite Chaves de Acesso Programáticas:** Não crie chaves de acesso para o usuário root[cite: 69]. [cite_start]Se precisar de acesso programático, use usuários IAM ou roles do IAM[cite: 70].
* [cite_start]**Use Apenas para Tarefas Específicas e Raras:** O usuário root deve ser usado apenas para tarefas que exigem acesso irrestrito e que não podem ser realizadas por um usuário IAM[cite: 71].
```

```markdown
### Pergunta 5
Qual é o banco de dados relacional totalmente gerenciado pela AWS e que pode ser 5 x mais rápido que o MySQL?
MariaDb
Aurora
DynamoDb
Neptune

[cite_start]**Resposta:** Amazon Aurora [cite: 74]

[cite_start]**Explicação:** O banco de dados relacional totalmente gerenciado pela AWS que pode ser **5 vezes mais rápido que o MySQL** é o **Amazon Aurora**[cite: 74].

* [cite_start]**Por que Amazon Aurora?** O Amazon Aurora é um serviço de banco de dados relacional construído para a nuvem, combinando a velocidade e a disponibilidade de bancos de dados comerciais de ponta com a simplicidade e a economia de bancos de dados de código aberto[cite: 75]. [cite_start]Ele é compatível com MySQL e PostgreSQL[cite: 76]. [cite_start]A AWS projeta o Aurora para ser **até 5 vezes mais rápido que o MySQL padrão** e 3 vezes mais rápido que o PostgreSQL padrão em cargas de trabalho típicas[cite: 77].

**Por que as outras opções não se encaixam?**
* [cite_start]**MariaDB:** O Amazon RDS suporta o MariaDB, mas ele não é a opção da AWS que promete ser 5x mais rápida que o MySQL[cite: 78].
* [cite_start]**DynamoDB:** O Amazon DynamoDB é um serviço de banco de dados **NoSQL**, não relacional[cite: 80]. [cite_start]Ele é totalmente gerenciado e oferece alta performance, mas não é comparável diretamente ao MySQL[cite: 81].
* [cite_start]**Neptune:** O Amazon Neptune é um serviço de banco de dados de **grafos**, também não relacional[cite: 82].
```

```markdown
### Pergunta 6
AWS Trusted Advisor é um serviço de monitoramento e recomendação que auxilia o cliente a utilizar os recursos de sua conta de maneira alinhada com as melhores práticas para trazer muitos benefícios.
Quais itens abaixo representam tais benefícios? (Selecione 3 alternativas)
Segurança
Performance
Otimização de Custos
Proteção de Hardware

**Resposta:**
* [cite_start]Segurança [cite: 88]
* [cite_start]Performance [cite: 90]
* [cite_start]Otimização de Custos [cite: 92]

[cite_start]**Explicação:** O **AWS Trusted Advisor** é uma ferramenta que fornece insights e recomendações para otimizar o ambiente AWS, alinhado com as melhores práticas da AWS[cite: 86, 87].

* [cite_start]**Segurança**: O Trusted Advisor monitora sua conta AWS para identificar possíveis vulnerabilidades de segurança e oferece recomendações para fortalecer a postura de segurança[cite: 88].
* [cite_start]**Performance**: Este serviço avalia o desempenho dos seus recursos AWS, identificando áreas onde melhorias podem ser feitas[cite: 90].
* [cite_start]**Otimização de Custos**: Um dos benefícios mais procurados do Trusted Advisor é a capacidade de identificar oportunidades para reduzir seus gastos na AWS[cite: 92].
* [cite_start]**Proteção de Hardware** não é um benefício direto do AWS Trusted Advisor[cite: 94]. [cite_start]O Trusted Advisor foca nas suas configurações e uso dos serviços, não na proteção física do hardware em si[cite: 95].
```

```markdown
### Pergunta 7
Uma empresa está migrando parte de sua aplicação para a AWS e precisa de uma solução para armazenar arquivos que utilizam sistemas de arquivos.
Qual serviço da AWS seria o mais adequado para atender a essa necessidade?
AWS Config
Elastic Compute Cloud (EC2)
Key Management Service (AWS KMS)
Elastic File System (EFS)

[cite_start]**Resposta:** Elastic File System (EFS) [cite: 98]

[cite_start]**Explicação:** Para uma empresa que está migrando parte de sua aplicação para a AWS e precisa de uma solução para armazenar arquivos que utilizam **sistemas de arquivos**, o serviço mais adequado seria o **Elastic File System (EFS)**[cite: 98].

* [cite_start]**Por que o Elastic File System (EFS) é o mais adequado?** O **Amazon Elastic File System (EFS)** é um serviço de armazenamento de arquivos totalmente gerenciado para instâncias do Amazon EC2 e servidores on-premises[cite: 100]. [cite_start]Ele é projetado para ser **altamente escalável, elástico e disponível**, e fornece uma interface de **sistema de arquivos de rede (NFS)** padrão[cite: 101]. [cite_start]Isso significa que as aplicações podem acessá-lo como um sistema de arquivos tradicional, tornando a migração de aplicações baseadas em arquivos mais simples e sem a necessidade de reescrever o código[cite: 102].

**Por que as outras opções não são as mais adequadas?**
* [cite_start]**AWS Config**: É um serviço que permite avaliar, auditar e avaliar as configurações dos seus recursos da AWS[cite: 104]. [cite_start]Ele não é um serviço de armazenamento de arquivos[cite: 105].
* [cite_start]**Elastic Compute Cloud (EC2)**: O EC2 em si é um serviço de computação (servidores virtuais), e não um serviço de armazenamento de arquivos compartilhado e escalável para sistemas de arquivos[cite: 106].
* [cite_start]**Key Management Service (AWS KMS)**: É um serviço que facilita a criação e o controle de chaves de criptografia[cite: 108]. [cite_start]Ele é crucial para a segurança dos dados, mas não é um serviço de armazenamento de arquivos em si[cite: 109].
```

```markdown
### Pergunta 8
Quais são os componentes principais do Amazon S3 utilizados para organizar e armazenar dados?
(Selecione 2 alternativas)
Buckets
Lambdas
Objetos
Funções (Roles)

**Resposta:**
* [cite_start]Buckets [cite: 112]
* [cite_start]Objetos [cite: 112]

[cite_start]**Explicação:** Os componentes principais do Amazon S3 utilizados para organizar e armazenar dados são: **Buckets** e **Objetos**[cite: 112].

* [cite_start]**Buckets (Baldes):** São contêineres lógicos para seus dados[cite: 114]. [cite_start]Cada objeto armazenado no S3 deve estar dentro de um bucket[cite: 115].
* [cite_start]**Objetos:** São os itens fundamentais armazenados no S3[cite: 117]. [cite_start]Um objeto consiste nos dados em si e metadados que descrevem esse objeto[cite: 118].

**Por que as outras opções não se encaixam?**
* **Lambdas:** AWS Lambda é um serviço de computação serverless. [cite_start]Embora possa interagir com o S3, não é um componente de armazenamento ou organização de dados *dentro* do S3[cite: 120, 121].
* [cite_start]**Funções (Roles):** As Funções (IAM Roles) concedem permissões temporárias para entidades acessarem recursos da AWS[cite: 122]. [cite_start]Elas são essenciais para o controle de acesso ao S3, mas não armazenam ou organizam os dados *no* S3[cite: 123].
```

```markdown
### Pergunta 9
Quais dos seguintes são princípios do pilar de confiabilidade no AWS Well-Architected Framework?
Implementar recuperação automática para falhas.
Utilizar automação para gerenciar infraestrutura.
Planejar limites de capacidade e testar frequentemente.
Proteger dados em trânsito e em repouso.
Monitorar continuamente o uso de recursos e métricas de desempenho.

**Resposta:**
* [cite_start]Implementar recuperação automática para falhas. [cite: 129]
* [cite_start]Planejar limites de capacidade e testar frequentemente. [cite: 131]
* [cite_start]Monitorar continuamente o uso de recursos e métricas de desempenho. [cite: 133]

[cite_start]**Explicação:** No **AWS Well-Architected Framework**, o pilar de **Confiabilidade** foca em como um sistema consegue se recuperar de falhas, adquirir e recuperar recursos de computação para atender à demanda e mitigar interrupções[cite: 128].

* [cite_start]**Implementar recuperação automática para falhas:** Este é um princípio chave da confiabilidade, garantindo que seu sistema possa detectar falhas e se recuperar delas automaticamente[cite: 129, 130].
* [cite_start]**Planejar limites de capacidade e testar frequentemente:** Garante que o sistema seja capaz de lidar com a demanda e possa manter seu desempenho sob diferentes cargas[cite: 131, 132].
* [cite_start]**Monitorar continuamente o uso de recursos e métricas de desempenho:** Essencial para detectar problemas antes que se tornem interrupções e reagir rapidamente a anomalias[cite: 133, 134].

**Por que os outros não se encaixam tão diretamente no pilar de Confiabilidade?**
* [cite_start]**Utilizar automação para gerenciar infraestrutura:** Alinha-se mais fortemente com o pilar de **Excelência Operacional**, que foca em executar e monitorar sistemas e melhorar continuamente os processos[cite: 136].
* [cite_start]**Proteger dados em trânsito e em repouso:** Esta é uma prática essencial de **Segurança**, um pilar distinto no Well-Architected Framework[cite: 137].
```

```markdown
### Pergunta 10
Qual serviço da AWS é recomendado para estimar de forma detalhada e precisa os custos de implementação e operação dos diversos serviços AWS para uma empresa, considerando diferentes cenários de uso, variáveis de configuração e previsões de crescimento?
AWS Pricing Calculator
AWS Billing
AWS Cost Explorer
AWS Organizations

[cite_start]**Resposta:** AWS Pricing Calculator [cite: 141]

[cite_start]**Explicação:** Para estimar de forma detalhada e precisa os custos de implementação e operação dos diversos serviços AWS, considerando diferentes cenários de uso, variáveis de configuração e previsões de crescimento, o serviço recomendado é o **AWS Pricing Calculator**[cite: 141].

* [cite_start]**Por que o AWS Pricing Calculator é o ideal?** É uma ferramenta baseada na web que permite modelar soluções e fornecer estimativas de custo[cite: 142]. [cite_start]Ele permite adicionar e configurar múltiplos serviços com especificações (detalhamento) [cite: 143][cite_start], fornece estimativas com base nas configurações (precisão) [cite: 144][cite_start], permite criar e salvar diferentes cenários para comparação [cite: 145][cite_start], e pode auxiliar no planejamento de crescimento futuro[cite: 146].

**Por que as outras opções não são as mais adequadas para *estimativa detalhada*?**
* [cite_start]**AWS Billing:** Usado para visualizar faturas *atuais e passadas*[cite: 148].
* [cite_start]**AWS Cost Explorer:** Ferramenta poderosa para analisar custos e uso *existentes* e prever custos com base no uso *histórico*[cite: 150, 151]. [cite_start]Não serve para estimar custos de novos projetos do zero com a mesma granularidade[cite: 152].
* [cite_start]**AWS Organizations:** Serviço de gerenciamento de contas que ajuda a centralizar e consolidar contas, mas não é uma ferramenta para estimativa de custos de serviços[cite: 153, 154].
```

```markdown
### Pergunta 11
Uma empresa busca assegurar a segurança das instâncias de uma aplicação que está prestes a ser lançada.
Qual é o serviço que auxilia na identificação de vulnerabilidades de segurança e riscos de exposição, seguindo as melhores práticas e conformidade com regulamentações?
AWS GuardDuty
AWS Macie
AWS Inspector
AWS KMS

[cite_start]**Resposta:** AWS Inspector [cite: 158]

[cite_start]**Explicação:** Para uma empresa que busca assegurar a segurança das instâncias de uma aplicação e precisa identificar vulnerabilidades de segurança e riscos de exposição, seguindo as melhores práticas e conformidade, o serviço mais adequado é o **Amazon Inspector**[cite: 158].

* [cite_start]**Por que o Amazon Inspector é o mais adequado?** É um serviço de avaliação de segurança automatizado que melhora a segurança e a conformidade de aplicações implantadas na AWS[cite: 159]. [cite_start]Ele avalia automaticamente o comportamento e as configurações de instâncias EC2, volumes EBS e imagens de container em busca de vulnerabilidades e desvios[cite: 160]. [cite_start]Suas funcionalidades incluem identificação de vulnerabilidades [cite: 161][cite_start], análise de rede [cite: 162][cite_start], conformidade com padrões [cite: 163] [cite_start]e relatórios detalhados[cite: 164].

**Por que as outras opções não se encaixam?**
* [cite_start]**AWS GuardDuty:** Serviço de detecção de ameaças que monitora atividades maliciosas em tempo real, mas não para avaliação proativa de vulnerabilidades nas instâncias[cite: 165, 166].
* [cite_start]**AWS Macie:** Serviço de segurança de dados focado em descobrir, classificar e proteger dados sensíveis no Amazon S3[cite: 167]. [cite_start]Não avalia vulnerabilidades nas instâncias de computação[cite: 168].
* [cite_start]**AWS KMS (Key Management Service):** Serviço para criação e controle de chaves de criptografia[cite: 169]. [cite_start]Não é um serviço de identificação de vulnerabilidades[cite: 170].
```

```markdown
### Pergunta 12
Durante a migração de sistemas, observou-se que há dados em uma aplicação que raramente são acessados e poderiam ser preservados em arquivos apenas para fins de auditoria.
Qual serviço pode ser empregado para alcançar esse objetivo com o menor custo possível?

[cite_start]**Resposta:** Amazon S3 Glacier Deep Archive [cite: 174]

[cite_start]**Explicação:** Para armazenar dados que são **raramente acessados** e precisam ser preservados em arquivos apenas para fins de auditoria, com o **menor custo possível** na AWS, o serviço mais indicado é o **Amazon S3 Glacier Deep Archive**[cite: 174].

* [cite_start]**Por que o Amazon S3 Glacier Deep Archive?** É a classe de armazenamento de objetos de custo mais baixo na AWS, projetada para arquivamento de longo prazo de dados que podem ser acessados uma ou duas vezes por ano[cite: 175]. [cite_start]Oferece custos de armazenamento por GB extremamente baixos [cite: 176][cite_start], alta durabilidade e confiabilidade [cite: 177][cite_start], e recuperação sob demanda (com tempos de recuperação de horas)[cite: 178].

**Considerações Importantes:**
* [cite_start]**Frequência de Acesso:** O principal fator para escolher essa classe é a **raridade do acesso**[cite: 179].
* [cite_start]**Tempo de Recuperação:** Esteja ciente dos tempos de recuperação, que podem variar de horas a até 12 horas[cite: 178, 181].
```

```markdown
### Pergunta 13
Qual é o serviço de banco de dados em grafo gerenciado pela AWS que possibilita diversos tipos de relacionamentos entre seus nós e pode ser aplicado em diversos contextos, representando conexões presentes em situações cotidianas, como em redes sociais, cadeias logísticas, ambientes empresariais, entre outros?
Amazon Graph
Amazon Neptune
Amazon JanusGraph
Amazon Neo4j

[cite_start]**Resposta:** Amazon Neptune [cite: 186]

[cite_start]**Explicação:** O serviço de banco de dados em grafo **gerenciado pela AWS** que possibilita diversos tipos de relacionamentos entre seus nós e pode ser aplicado em diversos contextos, representando conexões em situações cotidianas, é o **Amazon Neptune**[cite: 186].

* [cite_start]**Por que Amazon Neptune?** É um serviço de banco de dados de grafo totalmente gerenciado, construído para armazenar e navegar por bilhões de relacionamentos com baixa latência[cite: 187]. [cite_start]Suporta modelos de grafo como Property Graph (Gremlin, OpenCypher) e RDF (SPARQL)[cite: 188]. [cite_start]Suas aplicações incluem redes sociais [cite: 189][cite_start], mecanismos de recomendação [cite: 190][cite_start], detecção de fraudes [cite: 191][cite_start], cadeias logísticas [cite: 192] [cite_start]e grafos de conhecimento[cite: 193].

**Por que as outras opções não são as corretas?**
* [cite_start]**Amazon Graph:** Não existe um serviço da AWS com esse nome[cite: 194].
* [cite_start]**Amazon JanusGraph:** É um banco de dados de grafo de código aberto, não um serviço gerenciado pela AWS[cite: 195, 196].
* [cite_start]**Amazon Neo4j:** Neo4j é um banco de dados de grafo popular, mas não é um serviço gerenciado nativamente pela AWS[cite: 197, 198].
```

```markdown
### Pergunta 14
Um sistema externo gera arquivos em um formato incompatível com o seu sistema.
Qual serviço da AWS pode ser utilizado para realizar a transformação desses arquivos e integrá-los ao seu ambiente de forma eficiente?
AWS DataSync
AWS DTS
AWS Glue
AWS DMS

[cite_start]**Resposta:** AWS Glue [cite: 202]

[cite_start]**Explicação:** Para transformar arquivos gerados por um sistema externo em um formato compatível com o seu sistema e integrá-los ao seu ambiente AWS de forma eficiente, o serviço mais adequado é o **AWS Glue**[cite: 202].

* [cite_start]**Por que o AWS Glue é o mais adequado?** É um serviço de ETL (Extract, Transform, Load) serverless que facilita a preparação e movimentação de dados para análise[cite: 203].
    * [cite_start]**Extração (Extract):** Pode se conectar a diversas fontes de dados, incluindo S3[cite: 204].
    * [cite_start]**Transformação (Transform):** Permite definir e executar trabalhos de ETL para limpar, normalizar e transformar dados, incluindo a mudança de formatos[cite: 205, 206].
    * [cite_start]**Carregamento (Load):** Carrega os dados transformados em diversos destinos[cite: 208].
    * [cite_start]**Serverless:** Não exige provisionamento ou gerenciamento de servidores[cite: 209].

**Por que as outras opções não se encaixam tão bem?**
* [cite_start]**AWS DataSync:** É para transferência de dados, mas **não realiza a transformação** do formato do arquivo[cite: 211, 212].
* [cite_start]**AWS DMS (Database Migration Service):** Focado na migração de bancos de dados[cite: 213, 214].
```

```markdown
### Pergunta 15
Qual serviço da AWS possui um catálogo onde os clientes podem encontrar aplicações desenvolvidas por terceiros, prontas para serem instaladas e executadas para atender as mais diversas necessidades de negócio?
AWS Marketplace
AWS AMI
AWS MFA
AWS OpsWorks

[cite_start]**Resposta:** AWS Marketplace [cite: 219]

[cite_start]**Explicação:** O serviço da AWS que possui um catálogo onde os clientes podem encontrar aplicações desenvolvidas por terceiros, prontas para serem instaladas e executadas para atender as mais diversas necessidades de negócio, é o **AWS Marketplace**[cite: 219].

* [cite_start]**Por que o AWS Marketplace?** É um catálogo digital curado onde os clientes da AWS podem encontrar, comprar e implantar softwares, dados e serviços de terceiros[cite: 220]. [cite_start]Oferece um catálogo curado [cite: 222][cite_start], implantação simplificada [cite: 223][cite_start], faturamento consolidado [cite: 224] [cite_start]e opções de preços flexíveis[cite: 225].

**Por que as outras opções não se encaixam?**
* [cite_start]**AWS AMI (Amazon Machine Image):** É um template para iniciar instâncias EC2, não o catálogo[cite: 226, 227].
* [cite_start]**AWS MFA (Multi-Factor Authentication):** É um recurso de segurança para login, não um catálogo de aplicações[cite: 228].
* [cite_start]**AWS OpsWorks:** Serviço de gerenciamento de configuração para automação de servidores e aplicações, mas não um catálogo de software de terceiros[cite: 229, 230].
```

```markdown
### Pergunta 16
Uma organização almeja padronizar o processo de criação e configuração de todos os bancos de dados em sua infraestrutura por meio de código, permitindo a implementação automática através de pipelines de CI/CD.
Qual serviço seria a recomendação para atender a esse propósito?
AWS IAC
AWS RDS
AWS CodePipeline
AWS CloudFormation

[cite_start]**Resposta:** AWS CloudFormation [cite: 234]

[cite_start]**Explicação:** Para uma organização que busca padronizar a criação e configuração de bancos de dados por meio de código, permitindo a implementação automática via pipelines de CI/CD, o serviço recomendado é o **AWS CloudFormation**[cite: 234].

* [cite_start]**Por que AWS CloudFormation?** É um serviço de Infrastructure as Code (IaC) que permite modelar e provisionar recursos da AWS de forma declarativa[cite: 235]. [cite_start]Você descreve a infraestrutura (incluindo bancos de dados RDS) em um template[cite: 236]. [cite_start]Ele garante padronização por código [cite: 237][cite_start], implementação automática via CI/CD [cite: 238, 239][cite_start], gerenciamento do ciclo de vida [cite: 240] [cite_start]e controle de versão[cite: 241].

**Por que as outras opções não são as mais adequadas?**
* [cite_start]**AWS IAC (Infrastructure as Code):** É um conceito, não um serviço específico da AWS[cite: 243, 244].
* [cite_start]**AWS RDS (Relational Database Service):** É o serviço que *provisiona e gerencia* os bancos de dados, mas não a ferramenta para *automatizar a criação e configuração* por meio de código[cite: 245, 246].
* [cite_start]**AWS CodePipeline:** Orquestra o pipeline de CI/CD, mas **não define a infraestrutura como código**[cite: 247, 248]. [cite_start]Ele seria usado *em conjunto* com o CloudFormation[cite: 249].
```

```markdown
### Pergunta 17
Quais das seguintes opções são métodos de pagamento disponíveis para instâncias EC2?
(Selecione 3 alternativas)
On-premises (Próprio)
Reserved (Reservado).
Tailor Made (Sob medida).
On-demand (Sob demanda).
Spot

**Resposta:**
* [cite_start]Reserved (Reservado) [cite: 253]
* [cite_start]On-demand (Sob demanda) [cite: 253]
* [cite_start]Spot [cite: 253]

[cite_start]**Explicação:** A Amazon EC2 oferece diferentes modelos de precificação para otimizar os custos com base nas necessidades da carga de trabalho[cite: 253].

* [cite_start]**On-demand (Sob demanda):** Modelo mais flexível, paga por hora ou segundo sem compromissos[cite: 254]. [cite_start]Ideal para cargas de trabalho irregulares[cite: 255].
* **Reserved (Reservado):** Compromisso de 1 ou 3 anos com desconto significativo. [cite_start]Ideal para cargas de trabalho estáveis e previsíveis[cite: 256, 257].
* [cite_start]**Spot:** Capacidade EC2 não utilizada com até 90% de desconto, mas pode ser interrompida[cite: 257, 258]. [cite_start]Ideal para cargas de trabalho flexíveis e tolerantes a falhas[cite: 259].

**Por que as outras opções não são métodos de pagamento do EC2?**
* [cite_start]**On-premises (Próprio):** Refere-se à infraestrutura física fora da nuvem da AWS[cite: 261].
* [cite_start]**Tailor Made (Sob medida):** Não é uma categoria de pagamento oficial[cite: 262].
```

```markdown
### Pergunta 18
Ao utilizar os serviços da AWS, qual é a sequência típica esperada em uma pipeline de CI/CD?
CodeCommit, CodeBuild, CodeDeploy.
CodeCommit, CodeDeploy, CodeBuild.
CodeBuild, CodeDeploy, CodeCommit.
CodeBuild, CodeCommit, CodeDeploy.

[cite_start]**Resposta:** CodeCommit, CodeBuild, CodeDeploy. [cite: 266]

[cite_start]**Explicação:** A sequência típica e esperada em uma pipeline de CI/CD (Integração Contínua/Entrega Contínua) ao utilizar os serviços da AWS é: **CodeCommit, CodeBuild, CodeDeploy**[cite: 266].

1.  **AWS CodeCommit (Repositório de Código-Fonte):** É o ponto de partida onde os desenvolvedores enviam seu código-fonte. [cite_start]Alterações no código acionam a pipeline[cite: 267, 268, 269, 270].
2.  [cite_start]**AWS CodeBuild (Construção e Teste):** Pega o código do CodeCommit, compila, executa testes e produz pacotes de software prontos para implantação[cite: 271, 272, 273].
3.  [cite_start]**AWS CodeDeploy (Implantação):** Responsável pela implantação dos artefatos construídos nos ambientes de destino[cite: 274, 275, 276].
```

```markdown
### Pergunta 19
Para garantir elasticidade e economia no uso do EC2, mantendo os arquivos de programas e sistemas em um armazenamento persistente e escalável, que pode ser anexado e desanexado de instâncias conforme necessário, qual serviço da AWS deve ser utilizado?
S3
Git
CodeCommit
EBS

[cite_start]**Resposta:** Amazon Elastic Block Storage (EBS) [cite: 279]

[cite_start]**Explicação:** Para garantir **elasticidade e economia** no uso do EC2, mantendo os **arquivos de programas e sistemas em um armazenamento persistente e escalável** que pode ser anexado e desanexado de instâncias conforme necessário, o serviço da AWS que deve ser utilizado é o **Amazon EBS (Elastic Block Store)**[cite: 279].

* [cite_start]**Por que Amazon EBS é a escolha ideal?** Fornece volumes de armazenamento em bloco persistentes para uso com instâncias Amazon EC2[cite: 280]. [cite_start]Oferece persistência (dados permanecem após o término da instância) [cite: 282, 283][cite_start], facilidade de anexar e desanexar volumes [cite: 284][cite_start], elasticidade e escalabilidade [cite: 285][cite_start], e otimização de custos através da escolha de tipos de volumes[cite: 286]. [cite_start]É usado para sistemas operacionais, logs, bancos de dados[cite: 287].

**Por que as outras opções não se encaixam?**
* [cite_start]**S3 (Simple Storage Service):** Armazenamento de objetos, não em bloco[cite: 288, 289].
* [cite_start]**Git:** Sistema de controle de versão[cite: 290, 291].
* [cite_start]**CodeCommit:** Serviço de repositório Git gerenciado[cite: 292, 293].
```

```markdown
### Pergunta 20
Uma empresa deseja empregar o AWS IQ para agilizar a entrega de um projeto na nuvem.
De que maneira esse serviço pode ser utilizado para atender às necessidades da empresa e acelerar o processo de implementação do projeto?
Conectando especialistas da AWS para projetos de curto prazo.
Facilitando o desenvolvimento, a construção e a implantação de aplicações na AWS, oferecendo um conjunto integrado de ferramentas DevOps.
Facilita o gerenciamento e automação de operações em recursos da AWS e on-premises.
Versionando e automatizando a implementação de infraestrutura na nuvem.

[cite_start]**Resposta:** Conectando especialistas da AWS para projetos de curto prazo. [cite: 299]

[cite_start]**Explicação:** O **AWS IQ** pode ser utilizado para atender às necessidades da empresa e acelerar o processo de implementação do projeto **conectando especialistas da AWS para projetos de curto prazo**[cite: 299].

* [cite_start]**Como o AWS IQ Acelera Projetos:** Permite encontrar e contratar especialistas independentes certificados pela AWS para projetos específicos[cite: 300]. [cite_start]Oferece acesso rápido a expertise [cite: 301][cite_start], é ideal para projetos de curto prazo e escopo definido [cite: 302, 303][cite_start], proporciona orçamentos e entregas claros [cite: 304, 305][cite_start], e foca em soluções que seguem as melhores práticas da nuvem[cite: 305].

**Por que as outras opções não são o AWS IQ?**
* [cite_start]**"Facilitando o desenvolvimento, a construção e a implantação de aplicações na AWS, oferecendo um conjunto integrado de ferramentas DevOps."** Refere-se a serviços DevOps como CodePipeline, CodeBuild, CodeDeploy[cite: 307, 308].
* [cite_start]**"Facilita o gerenciamento e automação de operações em recursos da AWS e on-premises."** Alinha-se com o AWS Systems Manager[cite: 309, 310].
* [cite_start]**"Versionando e automatizando a implementação de infraestrutura na nuvem."** Ligado a Infrastructure as Code (IaC) e serviços como AWS CloudFormation e CodePipeline[cite: 311].
```

```markdown
### Pergunta 21
Após concluir os testes, homologações e implantação de uma aplicação, usuários relataram a impossibilidade de acessá-la em ambiente de produção. Na log do CloudWatch, uma mensagem de erro indica que a função Lambda enfrentou negação de acesso ao DynamoDB.
Qual serviço precisa ser configurado para resolver este problema em produção?
AWS IAM Roles
AWS CloudWatch
AWS Config
AWS Cognito

[cite_start]**Resposta:** AWS IAM Roles [cite: 316]

[cite_start]**Explicação:** Para resolver o problema de negação de acesso da função Lambda ao DynamoDB, o serviço que precisa ser configurado é o **AWS IAM Roles**[cite: 316].

* [cite_start]**Por que AWS IAM Roles?** O erro "negação de acesso" indica um problema de permissões[cite: 317]. [cite_start]As **AWS IAM Roles (Funções do IAM)** são a forma padrão e segura de conceder permissões a serviços AWS (como Lambda) para acessar outros serviços (como DynamoDB)[cite: 318]. [cite_start]Uma função Lambda precisa de uma função IAM com as políticas de permissão apropriadas (ex: `dynamodb:GetItem`) para interagir com o DynamoDB[cite: 319, 320]. [cite_start]A função Lambda assume a Role e herda suas permissões[cite: 321].

**Por que as outras opções não são a solução direta?**
* [cite_start]**AWS CloudWatch:** Usado para *identificar* o problema na log, não para *resolver* permissões[cite: 323, 324].
* [cite_start]**AWS Config:** Ajuda na governança e conformidade, rastreando configurações, mas não concede permissões de acesso entre serviços[cite: 325, 326].
* [cite_start]**AWS Cognito:** Gerencia identidades de usuários finais para aplicações web/móveis, não permissões de serviço para serviço[cite: 327, 328].
```

```markdown
### Pergunta 22
Quais dos seguintes planos de suporte oferecem acesso ao atendimento ao cliente, whitepapers, documentações e fóruns de suporte 24x7?
(Selecione 2)
Basic
Developer
Enterprise
Reserved

**Resposta:**
* [cite_start]Basic [cite: 348]
* [cite_start]Enterprise [cite: 348]

[cite_start]**Explicação:** Todos os planos de suporte da AWS (Basic, Developer, Business, Enterprise On-Ramp e Enterprise) oferecem acesso 24x7 à documentação, whitepapers e fóruns de suporte (AWS re:Post), e suporte 24x7 para questões de conta e faturamento[cite: 347, 350]. No entanto, ao selecionar dois que oferecem atendimento ao cliente (incluindo suporte técnico abrangente) 24x7:

* [cite_start]**Basic Support:** Inclui acesso 24x7 a atendimento ao cliente para questões de conta e faturamento, além de acesso total a documentação, whitepapers e fóruns públicos[cite: 350, 351].
* [cite_start]**Enterprise Support:** É o nível mais alto de suporte, fornecendo acesso 24x7 a todas as formas de atendimento ao cliente, incluindo engenheiros de Cloud Support dedicados via telefone, chat e e-mail para problemas técnicos, além de todos os recursos de documentação e fóruns[cite: 352, 353].

[cite_start]O plano Developer oferece suporte técnico por e-mail em horário comercial, não 24x7 para todos os problemas[cite: 355]. [cite_start]"Reserved" é um modelo de precificação para instâncias EC2, não um plano de suporte[cite: 356].
```

```markdown
### Pergunta 23
Um banco precisa executar milhares de tarefas de computação em lote com eficiência.
Qual é o serviço mais indicado para essa necessidade?

[cite_start]**Resposta:** AWS Batch [cite: 358]

[cite_start]**Explicação:** Para um banco que precisa executar **milhares de tarefas de computação em lote com eficiência**, o serviço mais indicado na AWS é o **AWS Batch**[cite: 358].

* [cite_start]**Por que AWS Batch?** É um serviço totalmente gerenciado que permite executar centenas de milhares de tarefas de computação em lote, eliminando a necessidade de gerenciar softwares ou clusters[cite: 359, 360]. [cite_start]Oferece gerenciamento total (provisionamento, planejamento, agendamento) [cite: 361, 362][cite_start], escalabilidade automática de recursos [cite: 363, 364][cite_start], otimização de custos (integrando com Spot Instances) [cite: 365][cite_start], suporte a contêineres Docker [cite: 366][cite_start], e permite definir priorização e dependências[cite: 368].
```

```markdown
### Pergunta 24
Uma aplicação disponibiliza dados por meio de APIs REST para várias aplicações externas. Considerando possíveis cenários de manutenção e evolução futuras, qual serviço pode auxiliar na gestão de múltiplas versões de uma API, garantindo a compatibilidade contínua com todos os seus consumidores?
AWS Zuul
AWS Route53
AWS EventBridge
API Gateway

[cite_start]**Resposta:** Amazon API Gateway [cite: 372]

[cite_start]**Explicação:** Para uma aplicação que disponibiliza dados por meio de APIs REST para várias aplicações externas e precisa gerenciar múltiplas versões de uma API, garantindo compatibilidade contínua com todos os seus consumidores, o serviço mais indicado é o **Amazon API Gateway**[cite: 372].

* [cite_start]**Por que o Amazon API Gateway?** É um serviço totalmente gerenciado para criar, publicar, manter, monitorar e proteger APIs[cite: 373]. [cite_start]Ele permite gerenciar múltiplas versões da API (ex: v1, v2, v3) [cite: 374][cite_start], configurar mapeamentos de domínios [cite: 377][cite_start], oferece controle de acesso e segurança (autenticação, throttling) [cite: 378] [cite_start]e se integra com CloudWatch para monitoramento[cite: 379].

**Por que as outras opções não são as ideais?**
* [cite_start]**AWS Zuul:** Um gateway de API de código aberto, não um serviço AWS gerenciado[cite: 380, 381].
* [cite_start]**AWS Route 53:** Serviço de DNS, usado para rotear tráfego, mas não gerencia versões de API[cite: 382, 383].
* [cite_start]**AWS EventBridge:** Barramento de eventos serverless para arquiteturas orientadas a eventos, não para gerenciar APIs REST diretamente[cite: 384, 385].
```

```markdown
### Pergunta 25
Uma agência de publicidade pretende lançar um site com conteúdo estático para realizar a primeira divulgação de um produto.
Qual serviço seria mais apropriado e econômico para esse cenário?
Elastic File System (EFS)
Docker
Simple Storage Service (S3)
Elastic Compute Cloud (EC2)

[cite_start]**Resposta:** Simple Storage Service (S3) [cite: 389]

[cite_start]**Explicação:** Para uma agência de publicidade que pretende lançar um site com conteúdo **estático** para a primeira divulgação de um produto, o serviço mais apropriado e econômico é o **Simple Storage Service (S3)**[cite: 389].

* [cite_start]**Por que o Amazon S3 é o mais adequado?** É um serviço de armazenamento de objetos altamente escalável, durável e disponível[cite: 390]. [cite_start]É perfeito para conteúdo estático (HTML, CSS, imagens) [cite: 391][cite_start], é extremamente econômico pois você paga apenas pelo uso [cite: 393, 394][cite_start], fácil de configurar [cite: 395, 396][cite_start], oferece alta disponibilidade e escalabilidade [cite: 397, 398][cite_start], e pode ser integrado com CloudFront[cite: 399].

**Por que as outras opções não são as ideais?**
* [cite_start]**Elastic File System (EFS):** Mais caro e complexo, focado em compartilhamento de arquivos para aplicações dinâmicas[cite: 400, 401].
* [cite_start]**Docker:** Plataforma de contêineres que exigiria infraestrutura de computação subjacente, adicionando custo e complexidade[cite: 402, 403].
* [cite_start]**Elastic Compute Cloud (EC2):** Servidores virtuais que seriam superdimensionados e mais caros para um site estático, exigindo gerenciamento de SO e servidor web[cite: 404, 405, 406].
```

```markdown
### Pergunta 26
Utilização de recursos de rede, computadores virtuais e armazenamento de dados com alto nível de flexibilidade, gerenciamento e controle sobre os recurso de TI são características de qual tipo de uso de cloud?
SaaS
PaaS
BaaS
IaaS

[cite_start]**Resposta:** IaaS [cite: 409]

[cite_start]**Explicação:** A utilização de recursos de rede, computadores virtuais (instâncias) e armazenamento de dados com alto nível de flexibilidade, gerenciamento e controle sobre os recursos de TI são características do **IaaS (Infrastructure as a Service)**[cite: 409].

* [cite_start]**Entendendo o IaaS:** IaaS fornece recursos de infraestrutura virtualizados como rede, computadores virtuais (ex: Amazon EC2) e armazenamento de dados (EBS, S3, EFS)[cite: 410, 411, 412]. [cite_start]O provedor gerencia a infraestrutura física, mas o cliente tem controle significativo sobre o sistema operacional, aplicações e rede[cite: 413, 414].

**Por que as outras opções não se encaixam?**
* [cite_start]**SaaS (Software as a Service):** Consome uma aplicação pronta, mínimo controle sobre infraestrutura[cite: 415, 416, 417].
* [cite_start]**PaaS (Platform as a Service):** Oferece uma plataforma para desenvolver e gerenciar aplicações, com o provedor gerenciando o SO e servidores[cite: 418, 419].
* [cite_start]**BaaS (Backend as a Service):** Focado em serviços de backend para desenvolvimento de aplicações, não sobre a infraestrutura subjacente[cite: 420].
```

```markdown
### Pergunta 27
Uma organização busca implementar uma estratégia de Recuperação de Desastres (DR) para suas aplicações.
Qual é a recomendação mais adequada para a utilização do AWS RDS?
Implementar as Read Replicas do RDS (Fazer cópias de leitura)
Implementar o RDS - Multi A-Z (Distribuir em zonas de disponibilidade diferentes)
Implementar o RDS - Multi Regions (Distribuir em regiões diferentes)
Implementar uma cópia do banco numa instância EC2

[cite_start]**Resposta:** Implementar o RDS - Multi Regions (Distribuir em regiões diferentes) [cite: 424]

[cite_start]**Explicação:** Para implementar uma estratégia de Recuperação de Desastres (DR) para aplicações que usam o AWS RDS, a recomendação mais adequada é **Implementar o RDS - Multi Regions (Distribuir em regiões diferentes)**[cite: 424].

* [cite_start]**Por que Multi-Region RDS para DR?** Uma estratégia de DR visa garantir a recuperação de falhas graves, incluindo aquelas que afetam uma **região inteira** da AWS[cite: 425]. [cite_start]O RDS Multi-Region cria uma réplica do banco de dados em uma **região geográfica diferente**, permitindo um *failover* em caso de desastre regional, oferecendo o nível mais alto de resiliência[cite: 426, 427, 428].

**Por que as outras opções não são as mais adequadas para DR abrangente?**
* [cite_start]**Implementar as Read Replicas do RDS:** Ótimas para escalabilidade de leitura e resiliência *dentro da mesma região*, mas não protegem contra desastres regionais[cite: 430, 431].
* [cite_start]**Implementar o RDS - Multi A-Z:** Configura réplicas em AZs distintas *dentro da mesma região*, oferecendo alta disponibilidade, mas **não protege contra um desastre regional**[cite: 432, 433, 434, 435].
* [cite_start]**Implementar uma cópia do banco numa instância EC2:** Aumenta a complexidade operacional e não é a recomendação mais eficiente para DR em um ambiente gerenciado como o RDS[cite: 436, 437, 438].
```

```markdown
### Pergunta 28
Qual das seguintes opções oferece a descrição mais precisa e abrangente do conceito de tolerância a falhas?
A habilidade de um sistema gravar as logs de execução.
A habilidade de um sistema nunca falhar
A habilidade de um sistema crescer e provisionar novos recursos para continuar executando suas cargas de trabalho sem interrupção
A habilidade de um sistema permanecer em funcionamento mesmo se um dos seus componentes falhar.

[cite_start]**Resposta:** A habilidade de um sistema permanecer em funcionamento mesmo se um dos seus componentes falhar. [cite: 443]

[cite_start]**Explicação:** A descrição mais precisa e abrangente do conceito de **tolerância a falhas** é: **A habilidade de um sistema permanecer em funcionamento mesmo se um dos seus componentes falhar.** [cite: 443]

* [cite_start]**Entendendo a Tolerância a Falhas:** Refere-se à capacidade de um sistema de continuar operando, mesmo com desempenho degradado, quando um ou mais de seus componentes apresentam falha[cite: 444, 445]. [cite_start]O objetivo é evitar interrupções completas[cite: 446].

**Análise das opções:**
* [cite_start]"A habilidade de um sistema gravar as logs de execução": Importante para depuração, mas não define tolerância a falhas[cite: 447, 448].
* [cite_start]"A habilidade de um sistema nunca falhar": Inatingível no mundo real[cite: 449, 450, 451].
* [cite_start]"A habilidade de um sistema crescer e provisionar novos recursos para continuar executando suas cargas de trabalho sem interrupção": Esta é a definição de **escalabilidade (elasticidade)**[cite: 452].
```

```markdown
### Pergunta 29
Uma empresa deseja migrar suas licenças de software existentes para a AWS, mas o modelo de licenciamento exige que sejam vinculadas a hardware físico exclusivo, com controle sobre os núcleos físicos e conformidade com as regras do fornecedor.
Qual estratégia a empresa deve adotar para atender a esse requisito?
Configurar um host dedicado no Amazon EC2 para garantir exclusividade de hardware físico e usar o AWS License Manager para rastrear e validar as licenças.
Criar uma reserva de capacidade em uma zona de disponibilidade específica e usar o AWS License Manager para controle de licenças.
Usar o AWS License Manager para gerenciar licenças e executar as instâncias do Amazon EC2 com tenancy padrão.
Utilizar instâncias reservadas combinadas com o AWS License Manager para economizar custos e garantir conformidade.
Beta

[cite_start]**Resposta:** Configurar um host dedicado no Amazon EC2 para garantir exclusividade de hardware físico e usar o AWS License Manager para rastrear e validar as licenças. [cite: 462]

[cite_start]**Explicação:** Para uma empresa que precisa migrar licenças de software existentes para a AWS, onde o modelo de licenciamento exige **vinculação a hardware físico exclusivo**, com **controle sobre os núcleos físicos** e **conformidade com as regras do fornecedor**, a estratégia mais adequada é: **Configurar um host dedicado no Amazon EC2 para garantir exclusividade de hardware físico e usar o AWS License Manager para rastrear e validar as licenças**[cite: 462].

* **Por que esta é a estratégia correta?**
    * [cite_start]**Host Dedicado (Dedicated Host) no Amazon EC2:** É um servidor físico dedicado para seu uso exclusivo, garantindo hardware físico exclusivo e controle sobre núcleos físicos, essencial para conformidade com licenças "bind-to-hardware"[cite: 463, 464, 466, 467].
    * [cite_start]**AWS License Manager:** Facilita o gerenciamento de licenças, permitindo definir regras e rastrear a conformidade[cite: 468, 469, 470].

**Por que as outras opções não são adequadas?**
* [cite_start]**Reserva de capacidade...:** Não garante hardware físico exclusivo; instâncias podem ser executadas em hardware compartilhado[cite: 471, 472].
* [cite_start]**Tenancy padrão:** Significa hardware compartilhado, violando o requisito de exclusividade[cite: 473, 474].
* [cite_start]**Instâncias reservadas...:** Oferecem desconto, mas por si só não garantem exclusividade de hardware físico (a menos que associadas a Hosts Dedicados)[cite: 475, 476].
```

```markdown
### Pergunta 30
Uma empresa tem o interesse de acompanhar o percentual de utilização de processamento e memória em seus servidores durante um período específico do dia.
Qual serviço da AWS seria adequado para atender a essa necessidade?
AWS CloudTrail
AWS Cost Explorer
AWS DataSync
AWS CloudWatch

[cite_start]**Resposta:** AWS CloudWatch [cite: 480]

[cite_start]**Explicação:** Para uma empresa que deseja acompanhar o percentual de utilização de processamento (CPU) e memória em seus servidores durante um período específico do dia, o serviço da AWS adequado é o **Amazon CloudWatch**[cite: 480].

* [cite_start]**Por que o Amazon CloudWatch?** É um serviço de monitoramento e observabilidade que fornece dados e insights acionáveis[cite: 481]. [cite_start]Ele coleta e rastreia métricas de desempenho (CPU e memória) [cite: 482][cite_start], permite monitoramento em tempo real e histórico [cite: 483][cite_start], criação de dashboards personalizados [cite: 484] [cite_start]e configuração de alarmes[cite: 485].

**Por que as outras opções não são adequadas?**
* [cite_start]**AWS CloudTrail:** Registra chamadas de API para auditoria, não métricas de desempenho[cite: 486, 487].
* [cite_start]**AWS Cost Explorer:** Analisa e visualiza custos e uso da AWS, não métricas operacionais[cite: 488, 489].
* [cite_start]**AWS DataSync:** Serviço de transferência de dados, não de monitoramento de desempenho[cite: 490, 491].
```

```markdown
### Pergunta 31
Com base nos princípios de excelência operacional, segurança, confiabilidade, desempenho eficiente, sustentabilidade e otimização de custos, qual é o framework que auxilia os arquitetos de nuvem na construção de aplicações seguras, altamente eficientes, resilientes e otimizadas?
Framework .Net
AWS CloudFormation
AWS Well-Architected
AWS Pillar

[cite_start]**Resposta:** AWS Well-Architected [cite: 494]

[cite_start]**Explicação:** O framework que auxilia os arquitetos de nuvem na construção de aplicações seguras, altamente eficientes, resilientes e otimizadas, com base nos princípios de excelência operacional, segurança, confiabilidade, desempenho eficiente, sustentabilidade e otimização de custos, é o **AWS Well-Architected Framework**[cite: 494].

* [cite_start]**Por que o AWS Well-Architected Framework?** É um guia para construir infraestrutura segura, de alto desempenho, resiliente e eficiente na AWS[cite: 495]. [cite_start]É baseado em seis pilares: Excelência Operacional [cite: 496][cite_start], Segurança [cite: 497][cite_start], Confiabilidade [cite: 498][cite_start], Eficiência de Performance [cite: 499][cite_start], Otimização de Custos [cite: 500] [cite_start]e Sustentabilidade[cite: 500].

**Por que as outras opções não se encaixam?**
* [cite_start]**Framework .NET:** Plataforma de desenvolvimento de software, não um framework de arquitetura de nuvem[cite: 502, 503].
* [cite_start]**AWS CloudFormation:** Serviço de Infrastructure as Code (IaC) para provisionar recursos, não o framework de princípios[cite: 504, 505].
* [cite_start]**AWS Pillar:** Termo usado *dentro* do Framework para suas áreas de foco, não um framework independente[cite: 506, 507].
```

```markdown
### Pergunta 32
Quais dos seguintes itens fazem parte dos pilares do Well-Architected Framework?
(Selecione 2 alternativas)
Segurança
Excelência Operacional
Monitoramento
Escalabilidade
Desacoplamento

**Resposta:**
* [cite_start]Segurança [cite: 509]
* [cite_start]Excelência Operacional [cite: 509]

[cite_start]**Explicação:** O AWS Well-Architected Framework é estruturado em seis pilares principais[cite: 510]:
1.  [cite_start]**Excelência Operacional:** Foca em executar e monitorar sistemas e melhorar processos[cite: 511].
2.  [cite_start]**Segurança:** Garante a proteção de dados e ativos[cite: 511].
3.  [cite_start]Confiabilidade [cite: 512]
4.  [cite_start]Eficiência de Performance [cite: 513]
5.  [cite_start]Otimização de Custos [cite: 514]
6.  [cite_start]Sustentabilidade [cite: 514]

**Por que as outras opções não são pilares diretos?**
* [cite_start]**Monitoramento:** Prática fundamental dentro de Excelência Operacional e Confiabilidade, mas não um pilar independente[cite: 515].
* [cite_start]**Escalabilidade:** Característica importante de Desempenho Eficiente e Confiabilidade, mas não um pilar por si só[cite: 516].
* [cite_start]**Desacoplamento:** Princípio de design que contribui para Confiabilidade e Excelência Operacional, mas não um pilar direto[cite: 517].
```

```markdown
### Pergunta 33
Qual dos seguintes serviços de bancos de dados oferecidos pela AWS proporciona, por padrão, gerenciamento completo, incluindo automação de tarefas como backup, aplicação de patches, monitoramento e escalabilidade, minimizando a intervenção administrativa do usuário?

[cite_start]**Resposta:** Amazon Relational Database Service (RDS) e Amazon Aurora [cite: 520]

[cite_start]**Explicação:** O serviço de banco de dados da AWS que proporciona, por padrão, gerenciamento completo, incluindo automação de tarefas como backup, aplicação de patches, monitoramento e escalabilidade, minimizando a intervenção administrativa do usuário, é o **Amazon Relational Database Service (RDS)** e seus motores compatíveis, como o **Amazon Aurora**[cite: 520].

* [cite_start]**Amazon RDS e Amazon Aurora: Gerenciamento Completo:** O Amazon RDS é um serviço de banco de dados relacional totalmente gerenciado[cite: 521]. [cite_start]O Amazon Aurora é um banco de dados relacional construído para a nuvem pela AWS e também é totalmente gerenciado[cite: 523, 524]. [cite_start]Ambos minimizam a intervenção administrativa ao automatizar: provisionamento de hardware [cite: 524][cite_start], backups automatizados [cite: 525][cite_start], aplicação de patches [cite: 526][cite_start], monitoramento [cite: 527][cite_start], escalabilidade [cite: 528] [cite_start]e alta disponibilidade (Multi-AZ)[cite: 529].
```

```markdown
### Pergunta 34
Qual dos seguintes serviços de bancos de dados oferecidos pela AWS proporciona, por padrão, gerenciamento completo, incluindo automação de tarefas como backup, aplicação de patches, monitoramento e escalabilidade, minimizando a intervenção administrativa do usuário?
MySql
MariaDB
DynamoDB
SQL Server

[cite_start]**Resposta:** DynamoDB [cite: 532]

[cite_start]**Explicação:** O serviço de banco de dados que proporciona, por padrão, **gerenciamento completo**, incluindo automação de tarefas como backup, aplicação de patches, monitoramento e escalabilidade, minimizando a intervenção administrativa do usuário, é o **Amazon DynamoDB**[cite: 532].

* [cite_start]**Por que o Amazon DynamoDB?** É um serviço de banco de dados **NoSQL** totalmente gerenciado e serverless[cite: 533]. [cite_start]A AWS cuida de todas as tarefas operacionais como provisionamento de hardware [cite: 535][cite_start], backups [cite: 536][cite_start], replicação [cite: 537][cite_start], aplicação de patches [cite: 537][cite_start], monitoramento [cite: 538][cite_start], escalabilidade automática [cite: 539] [cite_start]e alta disponibilidade[cite: 540].

**Por que os outros não se encaixam tão perfeitamente?**
* MySQL, MariaDB, SQL Server são **motores de bancos de dados relacionais**. [cite_start]Embora gerenciados via Amazon RDS, o RDS ainda exige alguma intervenção administrativa do usuário (escolha de instância, dimensionamento, segurança)[cite: 542, 543, 544, 545]. [cite_start]O DynamoDB, sendo serverless, abstrai ainda mais a infraestrutura[cite: 546].
```

```markdown
### Pergunta 35
O que é o AWS Free Tier (Nível Gratuito) e quais são as suas categorias de serviços disponíveis?
É um modelo de uso onde você não é cobrado na AWS. Suas categorias são 12 meses de gratuidade, sempre gratuito e spot.
É um modelo de uso onde você não é cobrado na AWS. Suas categorias são 12 meses de gratuidade, sempre gratuito e sob demanda.
É um modelo de uso onde você não é cobrado na AWS. Suas categorias são 12 meses de gratuidade, sempre gratuito e experimentação.
É um modelo de uso onde você não é cobrado na AWS. Suas categorias são 12 meses de gratuidade, sempre gratuito e reservado.

**Resposta:** É um modelo de uso onde você não é cobrado na AWS. [cite_start]Suas categorias são 12 meses de gratuidade, sempre gratuito e experimentação. [cite: 557]

[cite_start]**Explicação:** O **AWS Free Tier (Nível Gratuito da AWS)** é um programa que permite aos novos clientes da AWS explorar e experimentar serviços sem custo, até certos limites de uso[cite: 558]. As três categorias principais são:

1.  [cite_start]**12 Meses de Gratuidade (12 months Free Tier):** Uso gratuito por 12 meses a partir da criação da conta[cite: 560]. [cite_start]Ex: horas de EC2, GB de S3[cite: 561].
2.  [cite_start]**Sempre Gratuito (Always Free):** Uso gratuito de certos serviços que **não expiram** após 12 meses[cite: 562]. [cite_start]Ex: requisições Lambda, armazenamento DynamoDB[cite: 564].
3.  [cite_start]**Experimentação (Free Trials):** Acesso gratuito a serviços por um **período de tempo limitado** ou até um limite de uso específico[cite: 565].
```

```markdown
### Pergunta 36
Uma empresa tem a intenção de desenvolver uma aplicação sem servidor, fazendo uso de Lambda, SQS e SNS. Nesse contexto, é necessário escolher um serviço que possa orquestrar e integrar esses recursos para criar fluxos de negócio.
Qual serviço seria mais adequado para essa finalidade?
AWS Service Mesh
AWS EventBridge
AWS Workflow
AWS Step Functions

[cite_start]**Resposta:** AWS Step Functions [cite: 571]

[cite_start]**Explicação:** Para uma empresa que desenvolve uma aplicação serverless com Lambda, SQS e SNS e precisa orquestrar e integrar esses recursos para criar **fluxos de negócio**, o serviço mais adequado é o **AWS Step Functions**[cite: 571].

* [cite_start]**Por que o AWS Step Functions?** É um serviço de fluxo de trabalho serverless que facilita a coordenação de componentes distribuídos usando fluxos de trabalho visuais[cite: 572]. [cite_start]Ele é ideal para orquestrar Lambda, SQS e SNS em fluxos complexos [cite: 573][cite_start], oferece tratamento de erros e retentativas [cite: 575][cite_start], mantém o estado da execução [cite: 576, 577][cite_start], possui monitoramento visual [cite: 578] [cite_start]e integração nativa com Lambda, SQS e SNS[cite: 579].

**Por que as outras opções não são as mais adequadas?**
* [cite_start]**AWS Service Mesh:** Fornece comunicação em nível de rede para microsserviços, não orquestra fluxos de negócio[cite: 581, 582].
* [cite_start]**AWS EventBridge:** É um barramento de eventos para rotear eventos, mas não para orquestrar fluxos de trabalho com múltiplos passos e estado como o Step Functions[cite: 583, 584, 585].
* **AWS Workflow:** Não existe um serviço da AWS com esse nome. [cite_start]Step Functions é o principal serviço de orquestração[cite: 586, 587].
```

```markdown
### Pergunta 37
O desenvolvedor de uma empresa implementou um sistema baseado em arquitetura de microsserviços e necessita realizar a depuração de cada um desses microsserviços a partir de uma requisição do usuário, visando compreender a performance e identificar possíveis oportunidades de aprimoramento.
Qual serviço é mais apropriado para essa finalidade, tanto em ambientes de desenvolvimento quanto em ambientes de produção?
AWS OpenSearch
AWS CloudSearch
AWS CloudWatch
AWS X-Ray

[cite_start]**Resposta:** AWS X-Ray [cite: 591]

[cite_start]**Explicação:** Para um desenvolvedor que precisa depurar microsserviços a partir de uma requisição do usuário, compreender a performance e identificar oportunidades de aprimoramento, tanto em ambientes de desenvolvimento quanto de produção, o serviço mais apropriado é o **AWS X-Ray**[cite: 591].

* [cite_start]**Por que o AWS X-Ray é o mais adequado?** É um serviço que ajuda desenvolvedores a analisar e depurar aplicações distribuídas[cite: 592]. [cite_start]Oferece rastreamento distribuído (rastreia requisições em microsserviços) [cite: 594, 595][cite_start], gera um mapa de serviço visual para identificar gargalos [cite: 596, 597][cite_start], permite análise de performance detalhada [cite: 598][cite_start], facilita a identificação de erros [cite: 599] [cite_start]e pode ser usado em ambientes de desenvolvimento e produção[cite: 600].

**Por que as outras opções não são as ideais?**
* [cite_start]**AWS OpenSearch:** Serviço para pesquisa e análise de logs, não oferece rastreamento distribuído[cite: 601, 602].
* [cite_start]**AWS CloudSearch:** Serviço de pesquisa para sites, sem relação com depuração de microsserviços[cite: 603, 604].
* [cite_start]**AWS CloudWatch:** Serviço de monitoramento geral, mas não oferece o nível de rastreamento distribuído por requisição que o X-Ray fornece para depuração detalhada[cite: 605, 606, 607].
```

```markdown
### Pergunta 38
Qual é o serviço da AWS que permite que aplicações acessem de forma segura e controlada recursos restritos de outros serviços dentro da AWS, utilizando políticas de permissões granulares e autenticação robusta?
IAM Users (usuários)
IAM Função/Papeis (Roles)
IAM Groups (grupos)
IAM policies (políticas)

[cite_start]**Resposta:** IAM Função/Papeis (Roles) [cite: 609]

[cite_start]**Explicação:** O serviço da AWS que permite que aplicações acessem de forma segura e controlada recursos restritos de outros serviços dentro da AWS, utilizando políticas de permissões granulares e autenticação robusta, é **IAM Função/Papeis (Roles)**[cite: 609].

* [cite_start]**Por que IAM Função/Papeis (Roles)?** São a maneira mais segura e recomendada de conceder permissões a serviços AWS[cite: 610]. [cite_start]Fornecem **credenciais de segurança temporárias**, evitando o armazenamento de credenciais de longo prazo[cite: 611, 612]. [cite_start]Permitem acesso controlado para serviços, que assumem a Role para herdar permissões[cite: 613]. [cite_start]Adere ao princípio do privilégio mínimo com políticas granulares [cite: 614, 615][cite_start], e o processo é seguro com autenticação robusta[cite: 616].

**Por que as outras opções não são as mais adequadas para aplicações?**
* [cite_start]**IAM Users (usuários):** Ideais para pessoas, mas não recomendadas para uso direto em aplicações devido ao risco de segurança das credenciais de longo prazo[cite: 618, 619].
* [cite_start]**IAM Groups (grupos):** Coleções de usuários para aplicar permissões, mas não uma identidade que uma aplicação possa assumir[cite: 620, 621].
* **IAM policies (políticas):** Documentos JSON que *definem* as permissões, mas não o mecanismo pelo qual as aplicações as assumem. [cite_start]As políticas são anexadas a Roles[cite: 622, 623, 624].
```

```markdown
### Pergunta 39
Uma startup SaaS que utiliza diversos serviços da AWS está crescendo rapidamente e enfrenta desafios técnicos e operacionais. A gerente de engenharia precisa avaliar os planos de suporte disponíveis.
Quais são os cinco tipos de suporte ofertados pela AWS?
Standard, Developer, Business, Enterprise, Enterprise On-Ramp
Basic, Developer, Business, Advanced, Enterprise On-Ramp
Basic, Developer, Business, Enterprise On-Ramp, Enterprise
Bronze, Silver, Gold, Diamond, Ruby

[cite_start]**Resposta:** Basic, Developer, Business, Enterprise On-Ramp, Enterprise [cite: 630]

[cite_start]**Explicação:** Os cinco tipos de suporte ofertados pela AWS são: **Basic, Developer, Business, Enterprise On-Ramp, Enterprise**[cite: 630].

* [cite_start]**Basic Support:** Gratuito, oferece acesso 24x7 a documentação, whitepapers, fóruns e suporte para conta/faturamento[cite: 632, 633].
* [cite_start]**Developer Support:** Para desenvolvedores, oferece suporte técnico por e-mail em horário comercial[cite: 634, 635].
* [cite_start]**Business Support:** Para cargas de trabalho de produção, inclui acesso 24x7 a engenheiros de Cloud Support por telefone, chat e e-mail[cite: 636, 637].
* [cite_start]**Enterprise On-Ramp:** Ponte entre Business e Enterprise, com benefícios de nível empresarial e engajamento de TAM mais leve[cite: 638, 639].
* [cite_start]**Enterprise Support:** O plano mais abrangente, para cargas de trabalho críticas, com TAM dedicado, revisões proativas e suporte 24x7 com tempos de resposta rápidos[cite: 640, 641].
```

```markdown
### Pergunta 40
Qual é o serviço de alta performance desenvolvido para fornecer block-storage para instâncias EC2?
Amazon Elastic Block Storage (EBS)
AWS Key Management Service (KMS)
Amazon S3
Elastic Load Balancing (ELB)

[cite_start]**Resposta:** Amazon Elastic Block Storage (EBS) [cite: 644]

[cite_start]**Explicação:** O serviço de alta performance desenvolvido para fornecer **block-storage para instâncias EC2** é o **Amazon Elastic Block Storage (EBS)**[cite: 644].

* [cite_start]**Por que o Amazon EBS?** Oferece volumes de armazenamento em bloco persistentes para instâncias EC2[cite: 645]. [cite_start]É projetado para alto desempenho com vários tipos de volumes [cite: 647][cite_start], fornece block-storage (como um disco rígido virtual) ideal para sistemas operacionais e bancos de dados [cite: 648, 649][cite_start], garante persistência de dados independentemente da instância [cite: 650, 651][cite_start], e oferece flexibilidade (anexar/desanexar)[cite: 652].

**Por que as outras opções não se encaixam?**
* [cite_start]**AWS Key Management Service (KMS):** Serviço para chaves de criptografia, não armazenamento[cite: 653, 654].
* [cite_start]**Amazon S3:** Serviço de armazenamento de **objetos**, não em bloco[cite: 654, 655].
* [cite_start]**Elastic Load Balancing (ELB):** Serviço de rede para distribuir tráfego, não armazenamento[cite: 656, 657].
```

```markdown
### Pergunta 41
Um desenvolvedor precisa modificar determinadas partes do código de uma aplicação, mas no momento, não possui acesso ao seu computador e nem à sua IDE preferida.
Como esse cenário pode ser contornado utilizando os serviços da AWS, permitindo que ele edite, compile e implemente o código remotamente de maneira eficiente?
Utilizando o Athena através de um navegador de internet
Utilizando o CodePipeline através de um navegador de internet
Utilizando o Cloud9 através de um navegador de internet
Utilizando o CodeBuild através de um navegador de internet

[cite_start]**Resposta:** Utilizando o Cloud9 através de um navegador de internet [cite: 661]

[cite_start]**Explicação:** Para um desenvolvedor que precisa modificar, compilar e implementar código remotamente sem acesso ao seu computador ou IDE local, utilizando apenas um navegador de internet, a solução ideal na AWS é o **AWS Cloud9**[cite: 661].

* [cite_start]**Por que o AWS Cloud9 é a solução?** É um **Ambiente de Desenvolvimento Integrado (IDE) baseado em nuvem** acessível via navegador[cite: 662, 663]. [cite_start]Vem pré-configurado com ferramentas essenciais [cite: 664][cite_start], permite edição, compilação e implementação direta [cite: 665][cite_start], facilita a colaboração [cite: 666] [cite_start]e oferece integração com outros serviços AWS[cite: 667].

**Por que as outras opções não são adequadas?**
* [cite_start]**Athena:** Serviço de consulta SQL em S3, não um ambiente de desenvolvimento[cite: 668, 669].
* [cite_start]**CodePipeline:** Serviço de entrega contínua que orquestra o pipeline, mas não é uma IDE para escrita de código[cite: 670, 671].
* [cite_start]**CodeBuild:** Serviço de integração contínua para compilar e testar código, mas não uma IDE para codificação manual[cite: 672, 673].
```

```markdown
### Pergunta 42
Qual é a opção de armazenamento padrão (default) do serviço S3?
Standard
Glacier
Frequent Access
Infrequent Access

[cite_start]**Resposta:** Standard [cite: 676]

[cite_start]**Explicação:** A opção de armazenamento padrão (default) do serviço S3 é o **Standard**[cite: 676].

* [cite_start]**Por que o S3 Standard é o padrão?** Quando você faz upload de um objeto para um bucket do Amazon S3 e não especifica uma classe de armazenamento, o S3 o armazena automaticamente na classe **S3 Standard**[cite: 677]. [cite_start]É a classe de uso geral, otimizada para dados acessados frequentemente, com baixa latência e alto throughput [cite: 678][cite_start], e alta durabilidade e disponibilidade[cite: 679].
```

```markdown
### Pergunta 43
Uma startup está em busca de um serviço capaz de identificar os sentimentos expressos em textos digitados durante conversas entre clientes e atendentes em um chat de um e-commerce.
Qual serviço da AWS pode ser utilizado para analisar esses textos e determinar os sentimentos expressos, ajudando a melhorar a experiência do cliente e a eficiência do atendimento?
Amazon Polly
Amazon Translate
Amazon Comprehend
Amazon Kendra

[cite_start]**Resposta:** Amazon Comprehend [cite: 683]

[cite_start]**Explicação:** Para uma startup que precisa identificar os sentimentos expressos em textos de conversas entre clientes e atendentes em um chat de e-commerce, o serviço da AWS mais adequado é o **Amazon Comprehend**[cite: 683].

* [cite_start]**Por que o Amazon Comprehend?** É um serviço de Processamento de Linguagem Natural (NLP) que usa aprendizado de máquina para encontrar insights em texto[cite: 684]. [cite_start]Oferece análise de sentimentos (positivo, negativo, neutro, misto) [cite: 685, 686][cite_start], detecção de entidades [cite: 688][cite_start], detecção de frases-chave [cite: 689] [cite_start]e detecção de idioma[cite: 690].

**Por que as outras opções não são adequadas?**
* [cite_start]**Amazon Polly:** Transforma texto em fala (Text-to-Speech)[cite: 692, 693].
* [cite_start]**Amazon Translate:** Serviço de tradução automática[cite: 694, 695].
* [cite_start]**Amazon Kendra:** Serviço de pesquisa inteligente para encontrar respostas, mas não para análise de sentimento em conversas[cite: 696, 697].
```

```markdown
### Pergunta 44
Uma agência está buscando incorporar ao seu site uma funcionalidade que permita realizar pesquisas em todas as páginas e arquivos, visando aprimorar a navegação e a experiência dos usuários.
Qual serviço SaaS disponível na AWS oferece ferramentas robustas para atender a esse propósito e pode ser facilmente integrado à sua aplicação?
Amazon OpenSearch
Amazon Athena
Amazon CloudWatch
Amazon CloudSearch

[cite_start]**Resposta:** Amazon CloudSearch [cite: 701]

[cite_start]**Explicação:** Para uma agência que busca incorporar ao seu site uma funcionalidade de pesquisa robusta em todas as páginas e arquivos, o serviço SaaS da AWS mais adequado e facilmente integrável é o **Amazon CloudSearch**[cite: 701].

* [cite_start]**Por que o Amazon CloudSearch é o mais adequado?** É um serviço totalmente gerenciado e baseado em nuvem para configurar, gerenciar e dimensionar uma solução de pesquisa[cite: 702]. [cite_start]É focado em pesquisa de sites [cite: 703, 704][cite_start], é totalmente gerenciado (SaaS), eliminando a necessidade de gerenciar servidores de busca [cite: 705, 706, 707][cite_start], oferece fácil integração via APIs/SDKs [cite: 708][cite_start], inclui recursos robustos (autocompletar, facetas) [cite: 709] [cite_start]e otimização de custos (paga pelo uso)[cite: 710].

**Por que as outras opções não são as ideais?**
* [cite_start]**Amazon OpenSearch:** Mais complexo de gerenciar para uma pesquisa de site simples, embora poderoso[cite: 711, 712, 713].
* [cite_start]**Amazon Athena:** Serviço de consulta SQL em S3, não um serviço de pesquisa para um site[cite: 714, 715].
* [cite_start]**Amazon CloudWatch:** Serviço de monitoramento, não de pesquisa de conteúdo de site[cite: 716, 717].
```

```markdown
### Pergunta 45
Qual é o serviço serverless (sem servidor) da AWS que permite a execução de consultas utilizando o padrão SQL para analisar e processar grandes volumes de dados armazenados no Amazon S3, oferecendo escalabilidade automática e integração com outras ferramentas de análise de dados?
Amazon Query Analyzer
Athena
Amazon Elastic MapReduce (EMR)
Amazon Elastic Search

[cite_start]**Resposta:** Athena [cite: 720]

[cite_start]**Explicação:** O serviço serverless (sem servidor) da AWS que permite a execução de consultas utilizando o padrão SQL para analisar e processar grandes volumes de dados armazenados no Amazon S3, oferecendo escalabilidade automática e integração com outras ferramentas de análise de dados, é o **Amazon Athena**[cite: 720].

* [cite_start]**Por que o Amazon Athena é o serviço ideal?** É um serviço de consulta interativa serverless que facilita a análise de dados diretamente no Amazon S3 usando SQL padrão[cite: 721, 722]. [cite_start]Oferece escalabilidade automática [cite: 727][cite_start], integração com outras ferramentas (QuickSight, Glue) [cite: 728][cite_start], e custo-benefício (paga por consulta)[cite: 729, 730].

**Por que as outras opções não são as mais adequadas?**
* [cite_start]**Amazon Query Analyzer:** Não existe um serviço da AWS com esse nome[cite: 731].
* [cite_start]**Amazon Elastic MapReduce (EMR):** Plataforma de big data gerenciada, mas **não é serverless**[cite: 732, 733, 734].
* [cite_start]**Amazon Elastic Search (OpenSearch Service):** Serviço gerenciado para pesquisa e análise de logs, não consultas SQL diretas sobre dados em S3[cite: 734, 735, 736].
```

```markdown
### Pergunta 46
Uma empresa pretende manter suas cargas de trabalho no ambiente on-premises e armazenar parte de seus arquivos na AWS, adotando uma arquitetura de nuvem híbrida.
Qual serviço proporciona uma variedade de recursos para a implementação dessa integração de armazenamento?
Amazon Virtual Private Cloud (VPC)
AWS Organizations
AWS Database Migration Service
AWS Storage Gateway

[cite_start]**Resposta:** AWS Storage Gateway [cite: 740]

[cite_start]**Explicação:** Para uma empresa que pretende manter cargas de trabalho no ambiente on-premises e armazenar parte de seus arquivos na AWS, adotando uma arquitetura de nuvem híbrida, o serviço que proporciona uma variedade de recursos para a implementação dessa integração de armazenamento é o **AWS Storage Gateway**[cite: 740].

* [cite_start]**Por que o AWS Storage Gateway?** É um serviço híbrido que conecta um ambiente on-premises ao armazenamento na AWS[cite: 741]. [cite_start]Atua como uma ponte para mover dados com segurança[cite: 743]. [cite_start]Oferece variedade de recursos (tipos de Gateway como File Gateway para arquivos) [cite: 744, 745][cite_start], sincronização e caching [cite: 748][cite_start], e otimização de largura de banda[cite: 749].

**Por que as outras opções não são adequadas?**
* [cite_start]**Amazon Virtual Private Cloud (VPC):** Para provisionar redes isoladas na AWS, mas não é um serviço de integração de armazenamento[cite: 750, 751].
* [cite_start]**AWS Organizations:** Serviço de gerenciamento de contas, não relacionado à integração de armazenamento híbrido[cite: 752, 753].
* [cite_start]**AWS Database Migration Service (DMS):** Focado na migração de bancos de dados, não em armazenamento de arquivos[cite: 753, 754].
```

```markdown
### Pergunta 47
Em relação ao framework de melhores práticas arquitetônicas da AWS, qual pilar se dedica a assegurar que uma carga de trabalho execute sua função prevista de forma correta e consistente, e que essa carga de trabalho seja resiliente, recuperando-se prontamente de falhas para atender às demandas do negócio e do cliente?
Excelência Operacional
Confiabilidade
Performance Eficiente
Segurança

[cite_start]**Resposta:** Confiabilidade [cite: 757]

[cite_start]**Explicação:** O pilar do framework de melhores práticas arquitetônicas da AWS que se dedica a assegurar que uma carga de trabalho execute sua função prevista de forma correta e consistente, e que seja resiliente, recuperando-se prontamente de falhas para atender às demandas do negócio e do cliente, é a **Confiabilidade**[cite: 757].

* [cite_start]**Entendendo o Pilar da Confiabilidade:** Foca na capacidade de um sistema de se recuperar de falhas e de se dimensionar para atender à demanda[cite: 758]. [cite_start]Aborda fundamentos [cite: 760][cite_start], recuperação de falhas (redundância, replicação, failovers) [cite: 761, 762][cite_start], gerenciamento de mudanças [cite: 763] [cite_start]e dimensionamento para lidar com demandas variáveis[cite: 764].
```

```markdown
### Pergunta 48
Um E-Commerce precisa armazenar catálogos de produtos, onde cada item possui diferentes atributos, como descrição, preço, imagens e avaliações de clientes.
Qual serviço de banco de dados é o mais adequado para essa finalidade?
Amazon RedShift
Amazon EMR
Amazon Aurora
Amazon DynamoDB

[cite_start]**Resposta:** Amazon DynamoDB [cite: 768]

[cite_start]**Explicação:** Para um E-Commerce que precisa armazenar catálogos de produtos, onde cada item possui diferentes atributos (descrição, preço, imagens, avaliações de clientes), o serviço de banco de dados mais adequado é o **Amazon DynamoDB**[cite: 768].

* [cite_start]**Por que o Amazon DynamoDB é a melhor escolha?** É um serviço de banco de dados NoSQL totalmente gerenciado e serverless, oferecendo desempenho de escala única de dígito de milissegundo[cite: 769]. [cite_start]É ideal por sua flexibilidade de esquema (não exige esquema fixo para atributos variados) [cite: 770, 772, 773][cite_start], escalabilidade e performance em grande escala para picos de tráfego [cite: 774, 775][cite_start], gerenciamento reduzido (AWS cuida da infraestrutura) [cite: 776, 777][cite_start], e durabilidade/alta disponibilidade[cite: 778].

**Por que as outras opções não são tão adequadas?**
* [cite_start]**Amazon Redshift:** Data warehouse para análise de grandes volumes, não otimizado para catálogo de produtos transacional[cite: 779, 780].
* [cite_start]**Amazon EMR:** Plataforma de big data para processamento e análise em larga escala, não um banco de dados para servir dados de catálogo diretamente[cite: 781, 782].
* **Amazon Aurora:** Banco de dados relacional. [cite_start]Embora performático, o modelo relacional pode ser menos flexível para esquemas muito variados do que um NoSQL para catálogos[cite: 783, 784].
```

```markdown
### Pergunta 49
Uma empresa deseja lançar um novo produto e precisa criar um novo domínio público para associá-lo ao seu novo site. Considerando a necessidade de rapidez e eficiência no processo de registro e configuração do domínio, qual é a maneira mais rápida e eficaz de realizar essa tarefa utilizando os serviços da AWS?
Criar um novo domínio no Amazon Route 53.
Criar um servidor de domínio numa instância AWS EC2 e incluir o novo domínio.
Desenvolver o novo site no AWS BeanStalk, que provisiona toda a infra para o desenvolvedor apenas programar.
Criar um novo domínio no Registro.br

[cite_start]**Resposta:** Criar um novo domínio no Amazon Route 53. [cite: 790]

[cite_start]**Explicação:** Para registrar e configurar um novo domínio público de forma rápida e eficaz para um site usando os serviços da AWS, a maneira mais eficiente é **Criar um novo domínio no Amazon Route 53**[cite: 790].

* [cite_start]**Por que o Amazon Route 53?** É um serviço web de DNS altamente disponível e escalável[cite: 791]. [cite_start]Ele permite registro de domínio (comprar novos domínios) [cite: 792, 793][cite_start], gerenciamento de DNS (configurar registros para recursos AWS) [cite: 794, 795][cite_start], oferece rapidez e integração dentro do ecossistema AWS [cite: 796][cite_start], e é construído para confiabilidade e escalabilidade[cite: 797].

**Por que as outras opções não são as mais rápidas/eficazes?**
* [cite_start]**Criar um servidor de domínio numa instância AWS EC2:** Extremamente complexo, demorado e não gerenciado[cite: 799, 800].
* [cite_start]**Desenvolver o novo site no AWS Elastic Beanstalk:** Excelente para implantar aplicações web, mas **não é um registrador de domínio**[cite: 801, 802, 803].
* [cite_start]**Criar um novo domínio no Registro.br:** Válido para domínios .br, mas Route 53 integra registro e configuração DNS na mesma plataforma, simplificando[cite: 804, 805].
```

```markdown
### Pergunta 50
Uma agência de viagens online tem a necessidade de armazenar, analisar e correlacionar dados de logs de seus aplicativos. Isso é essencial para identificar e resolver gargalos de desempenho, bem como lidar com problemas de disponibilidade, a fim de garantir uma experiência de reserva otimizada para seus clientes.
Qual serviço da AWS é mais indicado para atender a essa demanda?
Amazon OpenSearch
Amazon Athena
Amazon CloudSearch
Amazon EMR

[cite_start]**Resposta:** Amazon OpenSearch [cite: 811]

[cite_start]**Explicação:** Para uma agência de viagens online que precisa armazenar, analisar e correlacionar **dados de logs** de seus aplicativos para identificar gargalos de desempenho e problemas de disponibilidade, o serviço da AWS mais indicado é o **Amazon OpenSearch Service**[cite: 811].

* [cite_start]**Por que o Amazon OpenSearch Service?** É um serviço totalmente gerenciado para clusters OpenSearch[cite: 812]. [cite_start]É otimizado para análise de logs em tempo real [cite: 813, 814][cite_start], oferece armazenamento e indexação escaláveis [cite: 815][cite_start], pesquisa poderosa e correlacionada para logs [cite: 816][cite_start], visualização e dashboards (OpenSearch Dashboards/Kibana) [cite: 817, 818][cite_start], e facilidade de gerenciamento[cite: 819].

**Por que as outras opções não são as mais adequadas?**
* [cite_start]**Amazon Athena:** Para consulta SQL em S3, mas não otimizado para ingestão e visualização de logs em tempo real[cite: 821, 822].
* [cite_start]**Amazon CloudSearch:** Para funcionalidade de pesquisa em sites, não para análise de logs para monitoramento de infraestrutura[cite: 823, 824].
* [cite_start]**Amazon EMR:** Plataforma de big data para processamento em lote, não a ferramenta de primeira linha para análise de logs em tempo real[cite: 825, 826].
```

```markdown
### Pergunta 51
Qual é a quantidade máxima de dados que pode ser armazenada no Amazon S3?
5 TB
10 MB
100 MB
A capacidade é virtualmente ilimitada

[cite_start]**Resposta:** A capacidade é virtualmente ilimitada [cite: 829]

[cite_start]**Explicação:** A quantidade máxima de dados que pode ser armazenada no Amazon S3 é **virtualmente ilimitada**[cite: 829]. [cite_start]O Amazon S3 é projetado para oferecer escalabilidade massiva, o que significa que não há limite total para a quantidade de dados ou o número de objetos que você pode armazenar[cite: 830].

* [cite_start]**Tamanho Máximo de Objeto Individual:** Cada objeto individual armazenado no S3 pode ter um tamanho máximo de **5 TB**[cite: 831].
* **Upload em uma Única Requisição:** O maior objeto que pode ser carregado em uma única operação PUT é de 5 GB. [cite_start]Para objetos maiores, a AWS recomenda o uso do upload multipartado[cite: 833, 834].
```

```markdown
### Pergunta 52
Como é possível manter a exposição constante de serviços em um mesmo endereço IP e facilitar a substituição simples dos hosts associados a esse endereço em sua infraestrutura?
Utilizando um IP Elástico
Utilizando um IPV6
Utilizando o Route 53
Utilizando HTTPS

[cite_start]**Resposta:** Utilizando um IP Elástico [cite: 837]

[cite_start]**Explicação:** Para manter a exposição constante de serviços em um mesmo endereço IP e facilitar a substituição simples dos hosts associados a esse endereço em sua infraestrutura, a solução é **Utilizando um IP Elástico (Elastic IP - EIP)**[cite: 837].

* [cite_start]**Por que um IP Elástico?** Um EIP é um endereço IP público estático que você pode alocar e associar a um recurso AWS[cite: 838]. [cite_start]Ele oferece um endereço IP constante que não muda, mesmo se a instância EC2 for substituída[cite: 840, 841]. [cite_start]Permite a substituição simples de hosts, minimizando o tempo de inatividade [cite: 843, 844][cite_start], e facilita a construção de arquiteturas tolerantes a falhas[cite: 845].

**Por que as outras opções não são adequadas para este propósito específico?**
* [cite_start]**Utilizando um IPv6:** Protocolo de rede, mas não resolve o remapeamento de um endereço estático[cite: 847, 848, 849].
* [cite_start]**Utilizando o Route 53:** Serviço de DNS que opera no nível do nome de domínio; não oferece a mesma agilidade de remapeamento de um IP estático diretamente[cite: 850, 851, 852, 853].
* [cite_start]**Utilizando HTTPS:** Protocolo de comunicação seguro para a web, sem relação com a manutenção ou remapeamento de um endereço IP[cite: 854, 855, 856].
```

```markdown
### Pergunta 53
Um equipe de desenvolvimento lançou o piloto de uma aplicação. Para obter a aprovação do rollout, o CTO solicitou uma análise dos custos de infraestrutura na AWS durante o período deste piloto.
Qual é o serviço que fornece essas informações?
AWS Trusted Advisor
AWS Budgets
AWS CostExplorer
AWS Inspector

[cite_start]**Resposta:** AWS CostExplorer [cite: 860]

[cite_start]**Explicação:** Para uma equipe de desenvolvimento que precisa analisar os custos de infraestrutura na AWS durante o período de um piloto, o serviço que fornece essas informações é o **AWS Cost Explorer**[cite: 860].

* [cite_start]**Por que o AWS Cost Explorer?** É uma ferramenta poderosa para visualizar e analisar custos e uso da AWS[cite: 861]. [cite_start]Permite análise detalhada de custos por período, serviço, recurso [cite: 862, 863][cite_start], identifica tendências de custo [cite: 864][cite_start], oferece relatórios personalizáveis [cite: 865] [cite_start]e pode fornecer previsões de custo futuras com base no histórico[cite: 866].

**Por que as outras opções não são as mais adequadas?**
* [cite_start]**AWS Trusted Advisor:** Sugere otimizações de custo, mas não é a ferramenta principal para analisar custos *reais* históricos[cite: 868, 869].
* [cite_start]**AWS Budgets:** Para definir orçamentos e alertas de custos *futuros*, não para análise de custos passados[cite: 870, 871].
* [cite_start]**AWS Inspector:** Serviço de avaliação de segurança, não fornece informações sobre custos[cite: 872, 873].
```

```markdown
### Pergunta 54
Uma empresa de e-commerce enfrenta picos de tráfego durante promoções e precisa ajustar sua infraestrutura para garantir alta disponibilidade e bom desempenho, mesmo em momentos de alta demanda.
Qual princípio de design de arquitetura é mais adequado para atender a essa necessidade?
Implementar automação para provisionar e desprovisionar recursos conforme necessário.
Garantir o monitoramento contínuo.
Escalar horizontalmente.
Projetar para falhas e implementar recuperação automática.

[cite_start]**Resposta:** Escalar horizontalmente. [cite: 878]

[cite_start]**Explicação:** Para uma empresa de e-commerce que enfrenta picos de tráfego e precisa ajustar sua infraestrutura para garantir alta disponibilidade e bom desempenho, o princípio de design de arquitetura mais adequado é **escalar horizontalmente**[cite: 878].

* [cite_start]**Por que Escalar Horizontalmente?** Significa adicionar mais instâncias ou nós para distribuir a carga[cite: 879]. [cite_start]Lida com picos de demanda ao distribuir requisições entre múltiplos servidores [cite: 880][cite_start], aumenta a alta disponibilidade e resiliência [cite: 881][cite_start], e permite elasticidade e otimização de custos ao adicionar/remover recursos automaticamente[cite: 882, 883].

**Por que as outras opções não são as mais adequadas como princípio primário?**
* [cite_start]**Implementar automação...:** É um **meio** para alcançar a escalabilidade horizontal[cite: 886, 887].
* [cite_start]**Garantir o monitoramento contínuo:** Essencial para **identificar** quando escalar, mas não o princípio de design que diretamente resolve o problema de picos de tráfego[cite: 889, 890].
* [cite_start]**Projetar para falhas e implementar recuperação automática:** Princípio da **Confiabilidade**, focado em recuperar de interrupções, não primariamente em adaptação a picos de demanda[cite: 891, 892, 893].
```

```markdown
### Pergunta 55
Uma empresa busca aprimorar a eficiência dos custos ao utilizar o serviço S3. Neste contexto identificou a presença de numerosos registros armazenados que poderiam ser removidos após decorridos 30 dias desde sua criação.
Como seria possível otimizar essa situação?
Configurando o CloudWatch para monitorar o S3 e enviar um email solicitando a exclusão dos arquivos.
Criando uma cópia destes objetos em outra zona de disponibilidade.
Criando uma cópia destes objetos em outra região.
Configurando o S3 Lifecycle (Ciclo de Vida) para que os objetos expirem em 30 dias para serem automaticamente excluídos.

[cite_start]**Resposta:** Configurando o S3 Lifecycle (Ciclo de Vida) para que os objetos expirem em 30 dias para serem automaticamente excluídos. [cite: 900]

[cite_start]**Explicação:** Para otimizar os custos no Amazon S3, removendo automaticamente registros após 30 dias desde sua criação, a melhor forma é **Configurar o S3 Lifecycle (Ciclo de Vida) para que os objetos expirem em 30 dias para serem automaticamente excluídos**[cite: 900].

* [cite_start]**Por que usar o S3 Lifecycle?** É um conjunto de regras para gerenciar o ciclo de vida dos objetos, incluindo a automação de exclusões[cite: 901, 902]. [cite_start]Permite exclusão automática de objetos após 30 dias [cite: 903, 904][cite_start], otimiza custos ao parar de pagar por armazenamento desnecessário [cite: 905][cite_start], e oferece eficiência operacional pela automação[cite: 906].

**Por que as outras opções não são adequadas?**
* [cite_start]**Configurando o CloudWatch para monitorar o S3 e enviar um email:** Apenas alerta, não executa a exclusão automaticamente[cite: 907, 908, 909].
* [cite_start]**Criando uma cópia destes objetos em outra zona de disponibilidade/região:** Aumenta durabilidade/resiliência, mas **não reduz custos** nem exclui arquivos automaticamente, podendo até aumentar custos[cite: 910, 911, 912, 913].
```

```markdown
### Pergunta 56
Qual das seguintes opções é um princípio essencial do AWS Cloud Adoption Framework (AWS CAF) relacionado à perspectiva de governança?
Gerenciamento de desempenho e capacidade.
Automação do ciclo de vida de produtos e serviços.
Definição de políticas e monitoramento de conformidade.
Provisionamento de identidades e controle de acesso.

[cite_start]**Resposta:** Definição de políticas e monitoramento de conformidade. [cite: 936]

[cite_start]**Explicação:** O AWS Cloud Adoption Framework (AWS CAF) é um guia para adoção da nuvem, dividido em perspectivas, incluindo a de **Governança**[cite: 934, 935].

* [cite_start]Dentro da perspectiva de Governança, o princípio essencial é: **Definição de políticas e monitoramento de conformidade**[cite: 936].
    * [cite_start]**Definir Políticas:** Estabelecer regras claras sobre o uso de recursos da nuvem[cite: 938].
    * [cite_start]**Monitorar Conformidade:** Acompanhar continuamente para garantir que as políticas sejam seguidas e que a organização esteja em conformidade[cite: 939].

**Por que as outras opções não são o princípio principal da Governança?**
* [cite_start]**Gerenciamento de desempenho e capacidade:** Alinha-se mais com a perspectiva de Plataforma ou Operações[cite: 942].
* [cite_start]**Automação do ciclo de vida de produtos e serviços:** Aspecto chave das perspectivas de Operações e Plataforma[cite: 943].
* [cite_start]**Provisionamento de identidades e controle de acesso:** Princípio central da perspectiva de **Segurança**[cite: 944, 945].
```

```markdown
### Pergunta 57
Como o AWS Compute Optimizer emprega informações específicas para identificar configurações ideais de recursos na infraestrutura da AWS?
Utilizando Machine learning.
Utilizando IA Generativa.
Utilizando Mineração de dados.
Utilizando APIs de processamento de linguagem natural (NLP).

[cite_start]**Resposta:** Utilizando Machine learning. [cite: 949]

[cite_start]**Explicação:** O AWS Compute Optimizer emprega informações específicas para identificar configurações ideais de recursos na infraestrutura da AWS **utilizando Machine Learning (Aprendizado de Máquina)**[cite: 949].

* [cite_start]**Como o AWS Compute Optimizer usa Machine Learning:** Ele coleta dados de utilização de recursos (CPU, memória, etc.) de serviços como CloudWatch[cite: 951]. [cite_start]Com base nesses dados históricos, ele usa **algoritmos de machine learning** para analisar padrões de uso e prever desempenho[cite: 953, 954]. [cite_start]A partir dessa análise, gera recomendações para redimensionamento, otimização de custos e melhora de performance[cite: 955, 956, 957].

**Por que as outras opções não são a resposta principal?**
* [cite_start]**IA Generativa:** Foca na criação de conteúdo, não na análise de dados para recomendação de otimização de recursos[cite: 960, 961].
* [cite_start]**Mineração de Dados:** Termo mais genérico, onde Machine Learning é uma técnica usada[cite: 962, 963, 964].
* [cite_start]**APIs de processamento de linguagem natural (NLP):** Usadas para entender linguagem humana, não métricas de infraestrutura[cite: 965, 966].
```

```markdown
### Pergunta 58
Qual das seguintes afirmações NÃO está relacionada ao AWS Lambda?
Pode ser acionado diretamente pelo AWS S3.
Processa dados sem servidor.
Pode ser acionado diretamente pelo AWS SNS
Permite o gerenciamento total dos recursos de infraestrutura.

[cite_start]**Resposta:** Permite o gerenciamento total dos recursos de infraestrutura. [cite: 969]

[cite_start]**Explicação:** A afirmação que **NÃO** está relacionada ao AWS Lambda é: **Permite o gerenciamento total dos recursos de infraestrutura.** [cite: 969]

* [cite_start]**Entendendo o AWS Lambda:** O AWS Lambda é um serviço de computação **serverless** (sem servidor)[cite: 970]. [cite_start]Isso significa que a AWS gerencia totalmente a infraestrutura subjacente (servidores, SO, escalabilidade, patches) para você[cite: 971]. [cite_start]Você se preocupa apenas com o código[cite: 972].

**Análise das afirmações:**
* [cite_start]"Pode ser acionado diretamente pelo AWS S3": **Verdadeiro.** É comum ser acionado por eventos do S3[cite: 973, 974, 975].
* [cite_start]"Processa dados sem servidor": **Verdadeiro.** É a principal característica do Lambda[cite: 976, 977].
* [cite_start]"Pode ser acionado diretamente pelo AWS SNS": **Verdadeiro.** SNS pode acionar funções Lambda[cite: 978, 979, 980].
* [cite_start]"Permite o gerenciamento total dos recursos de infraestrutura": **Falso.** O Lambda **abstrai o gerenciamento da infraestrutura** do usuário[cite: 981, 982, 983, 984].
```

```markdown
### Pergunta 59
Uma equipe limitada em infraestrutura está interessada em adotar uma arquitetura de microsserviços em containers sem servidor.
Qual serviço poderia ajudá-los, uma vez que não exige conhecimento especializado em containers e pode ser implementado com facilidade?
Amazon Elastic Container Service (ECS)
AWS Fargate
Amazon Elastic Container Registry (ECR)
Amazon Elastic Kubernetes Service (EKS)

[cite_start]**Resposta:** AWS Fargate [cite: 988]

[cite_start]**Explicação:** Para uma equipe limitada em infraestrutura que busca adotar uma arquitetura de microsserviços em containers **sem servidor** e que **não exige conhecimento especializado em containers**, o serviço ideal é o **AWS Fargate**[cite: 988].

* [cite_start]**Por que o AWS Fargate é a melhor escolha?** É um motor de computação serverless para ECS e EKS, permitindo executar contêineres sem provisionar ou gerenciar servidores[cite: 989]. [cite_start]É serverless para contêineres (AWS gerencia infraestrutura) [cite: 990, 991, 992][cite_start], minimiza conhecimento especializado em contêineres [cite: 993, 994][cite_start], oferece facilidade de implementação [cite: 995, 996] [cite_start]e otimização de custos[cite: 997].

**Por que as outras opções não são as ideais para este cenário?**
* [cite_start]**Amazon Elastic Container Service (ECS):** É um orquestrador, mas pode exigir gerenciamento de instâncias EC2, a menos que usado com Fargate[cite: 999, 1000, 1001].
* [cite_start]**Amazon Elastic Container Registry (ECR):** É um registro de imagens de contêineres, não executa ou gerencia a infraestrutura[cite: 1002, 1003].
* [cite_start]**Amazon Elastic Kubernetes Service (EKS):** Serviço gerenciado de Kubernetes, que exige conhecimento especializado e gerenciamento de nós de trabalho[cite: 1004, 1005, 1006].
```

```markdown
### Pergunta 60
Uma empresa precisa auditar sua infraestrutura na AWS para identificar ações manuais e não planejadas de desligamento de recursos.
Qual serviço pode ser útil para auxiliar nessa atividade?
AWS Cloud ElasticSearch
AWS CloudSearch
AWS Audit
AWS CloudTrail

[cite_start]**Resposta:** AWS CloudTrail [cite: 1009]

[cite_start]**Explicação:** Para auditar a infraestrutura na AWS e identificar ações manuais e não planejadas de desligamento de recursos, o serviço que pode ser útil é o **AWS CloudTrail**[cite: 1009].

* [cite_start]**Por que o AWS CloudTrail?** Registra as chamadas de API da AWS e os eventos relacionados à atividade do usuário e do serviço na sua conta[cite: 1010, 1011]. [cite_start]Isso inclui ações de desligamento (`TerminateInstances`, `StopInstances`), quem as executou e quando, permitindo identificar atividades não planejadas[cite: 1014, 1015]. [cite_start]É crucial para auditoria, segurança e conformidade [cite: 1016][cite_start], e integra-se com CloudWatch e S3[cite: 1017].

**Por que as outras opções não são adequadas?**
* [cite_start]**AWS Cloud ElasticSearch (Amazon OpenSearch Service):** Usado para pesquisa e análise de logs, mas não gera os logs de auditoria[cite: 1018, 1019].
* [cite_start]**AWS CloudSearch:** Serviço para funcionalidades de pesquisa em sites, sem relação com auditoria[cite: 1020, 1021].
* **AWS Audit:** Não existe um serviço da AWS com esse nome. [cite_start]A auditoria é feita com CloudTrail[cite: 1021, 1022].
```

```markdown
### Pergunta 61
Chief Technology Officer (CTO) de uma rede hospitalar almeja incorporar o AWS Data Exchange em suas plataformas.
Para que finalidade esse serviço pode ser utilizado nesse contexto?
Para gerar relatórios financeiros dos custos de infraestrutura de hospitais.
Para compartilhar dados de pacientes com outras organizações de saúde.
Para criar websites de informações médicas.
Para integrar as redes computacionais dos hospitais.

[cite_start]**Resposta:** Para compartilhar dados de pacientes com outras organizações de saúde. [cite: 1027]

[cite_start]**Explicação:** O AWS Data Exchange pode ser utilizado por uma rede hospitalar para **compartilhar dados de pacientes com outras organizações de saúde**[cite: 1027].

* [cite_start]**Entendendo o AWS Data Exchange no Contexto Hospitalar:** É um serviço que facilita encontrar, assinar e usar dados de terceiros, e também empacotar e monetizar seus próprios dados[cite: 1028, 1029]. [cite_start]No contexto hospitalar, permite o compartilhamento seguro de dados (anonimizados e conformes) com instituições de pesquisa ou parceiros[cite: 1030, 1031]. [cite_start]Também possibilita monetização de dados de pesquisa [cite: 1032] [cite_start]ou consumo de dados externos para melhoria de diagnóstico/tratamento[cite: 1033].

**Por que as outras opções não se encaixam?**
* [cite_start]**Gerar relatórios financeiros de custos de infraestrutura:** Usaria Cost Explorer, Budgets, Billing[cite: 1035].
* [cite_start]**Criar websites de informações médicas:** Usaria S3, Amplify, Beanstalk, EC2[cite: 1036, 1037].
* [cite_start]**Integrar redes computacionais:** Usaria Direct Connect, VPN, VPC[cite: 1038, 1039].
```

```markdown
### Pergunta 62
A equipe de Arquitetura de Soluções de uma empresa recomendou o uso do AWS Wavelength para melhorar o desempenho de suas aplicações.
Qual é a melhor definição para o AWS Wavelength, considerando seu papel para os serviços de computação e armazenamento da AWS?
Uma tecnologia de monitoramento de tráfego de rede na AWS.
Uma região geográfica da AWS especialmente projetada para cargas de trabalho de baixa latência.
Uma ferramenta de gerenciamento e implementação de serviços de computação e banco de dados na AWS.
Um serviço de monitoramento do uso e performance de serviços de computação e armazenamento.

[cite_start]**Resposta:** Uma região geográfica da AWS especialmente projetada para cargas de trabalho de baixa latência. [cite: 1065]

[cite_start]**Explicação:** A melhor definição para o **AWS Wavelength**, considerando seu papel para os serviços de computação e armazenamento da AWS, é: **Uma região geográfica da AWS especialmente projetada para cargas de trabalho de baixa latência**[cite: 1065].

* [cite_start]**Entendendo o AWS Wavelength:** Ele estende a infraestrutura e os serviços da AWS para as redes 5G das operadoras[cite: 1066]. [cite_start]Seu objetivo principal é atender a cargas de trabalho que exigem latência extremamente baixa, implantando aplicações mais próximas dos usuários no "edge" da rede 5G[cite: 1067, 1069]. [cite_start]Permite implantar recursos como instâncias EC2 e volumes EBS em Wavelength Zones[cite: 1070].

**Por que as outras opções estão incorretas?**
* [cite_start]**Tecnologia de monitoramento de tráfego de rede:** Funções de CloudWatch, Network Monitor[cite: 1071].
* [cite_start]**Ferramenta de gerenciamento e implementação:** Descrição muito ampla (ex: Console, CloudFormation)[cite: 1072].
* [cite_start]**Serviço de monitoramento de uso e performance:** Função de CloudWatch[cite: 1073].
```

```markdown
### Pergunta 63
Quais são as principais funcionalidades do Amazon QuickSight?
Capturar dados de diversos dispositivos através de streaming de dados de forma quase online.
Executar Map reduce em dados distribuídos.
Realizar consultas em objetos armazenados no S3
Criar DashBoards de BI com uso de Aprendizado de Máquina (Machine Learning)

[cite_start]**Resposta:** Criar DashBoards de BI com uso de Aprendizado de Máquina (Machine Learning) [cite: 1076]

[cite_start]**Explicação:** A principal funcionalidade do Amazon QuickSight é **Criar Dashboards de BI com uso de Aprendizado de Máquina (Machine Learning)**[cite: 1076].

* [cite_start]**Entendendo as Funcionalidades do Amazon QuickSight:** É um serviço de inteligência de negócios (BI) escalável e serverless[cite: 1077]. Suas capacidades incluem:
    * [cite_start]**Dashboards de BI Interativos:** Permite a criação de dashboards ricos e interativos[cite: 1079].
    * [cite_start]**Insights de Machine Learning:** Integra recursos de ML para descoberta de insights, incluindo SPICE (motor de cálculo em memória) [cite: 1080, 1081][cite_start], ML-Powered Insights (anomalias, previsões) [cite: 1082] [cite_start]e perguntas em linguagem natural[cite: 1083].
    * [cite_start]Conectividade a diversas fontes de dados[cite: 1084].

**Por que as outras opções estão incorretas?**
* [cite_start]**Capturar dados de streaming:** Associado a Amazon Kinesis[cite: 1085].
* [cite_start]**Executar Map Reduce:** Função de plataformas como Amazon EMR[cite: 1086].
* [cite_start]**Realizar consultas em objetos armazenados no S3:** Principalmente função do Amazon Athena[cite: 1087].
```

```markdown
### Pergunta 64
Uma empresa deu início a um processo de transformação digital em todas as suas plataformas e optou por empregar uma arquitetura de sistemas orientada a eventos.
Qual dos serviços a seguir pode ser utilizado como um barramento escalável de eventos para facilitar a implementação dessa arquitetura?
Amazon EventBridge
Amazon SQS
Amazon EventSync
Amazon Lambda

[cite_start]**Resposta:** Amazon EventBridge [cite: 1091]

[cite_start]**Explicação:** Para uma empresa que está implementando uma arquitetura de sistemas orientada a eventos e precisa de um **barramento escalável de eventos**, o serviço da AWS mais adequado é o **Amazon EventBridge**[cite: 1091].

* [cite_start]**Por que o Amazon EventBridge?** É um serviço de barramento de eventos serverless que facilita a conexão de aplicações usando dados de eventos[cite: 1092]. [cite_start]Permite construir aplicações escaláveis e desacopladas, roteando eventos de diversas fontes (serviços AWS, SaaS, eventos personalizados) para múltiplos destinos[cite: 1093, 1095, 1096, 1097, 1099]. [cite_start]Oferece roteamento e filtragem de eventos [cite: 1097, 1098] [cite_start]e transformação de eventos[cite: 1100].

**Por que as outras opções não são as mais adequadas?**
* [cite_start]**Amazon SQS (Simple Queue Service):** Serviço de filas de mensagens (ponto a ponto), não um barramento de eventos com roteamento e múltiplas fontes/destinos[cite: 1102, 1103].
* [cite_start]**Amazon EventSync:** Não existe um serviço da AWS com esse nome[cite: 1104].
* [cite_start]**Amazon Lambda:** Serviço de computação serverless que executa código em resposta a eventos, sendo um destino comum para eventos, mas não o barramento em si[cite: 1105, 1106].
```
