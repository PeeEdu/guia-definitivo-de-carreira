# Do Código à Arquitetura

## Engenharia de Software com Java, Sistemas Distribuídos e Inteligência Artificial — da base júnior ao arquiteto de software

**Autor:** Pedro Santos
**Documento:** Estrutura editorial completa — versão 1.1 (ordem alinhada ao `roadmap.sh/java` e módulo dedicado ao Spring), para aprovação
**Base:** *Plano Mestre Granular: De Desenvolvedor Java Júnior a Arquiteto de Software & Engenheiro de IA*

---

## 0. Proposta editorial

### 0.1 Título

- **Título:** *Do Código à Arquitetura*
- **Subtítulo:** *Engenharia de Software com Java, Sistemas Distribuídos e Inteligência Artificial — da base júnior ao arquiteto de software*
- **Alternativas consideradas:** *A Jornada do Arquiteto: Java, Sistemas Distribuídos e IA na Prática*; *Engenharia de Software de Ponta a Ponta: do Desenvolvedor Java ao Arquiteto de Software*.

O título escolhido expressa a progressão central da obra: começar pela linha de código bem escrita e terminar nas decisões que moldam ecossistemas inteiros, sem pular os degraus intermediários.

### 0.2 Público, pré-requisitos e versões-alvo

O livro atende dois leitores ao mesmo tempo. O primeiro está começando a carreira e precisa de fundamentos explicados sem atalhos. O segundo já trabalha com desenvolvimento e quer entender o *porquê* das decisões, os mecanismos internos e os trade-offs. Para servir aos dois, cada capítulo parte do problema concreto, explica o fundamento e só então avança para os aspectos internos e avançados.

- **Pré-requisitos:** nenhum conhecimento prévio de Java. Noções de lógica de programação ajudam, mas os Capítulos 5 a 7 constroem a base da linguagem desde o início.
- **Versões-alvo propostas:** Java 21 LTS como base dos exemplos, com recursos do Java 25 LTS sinalizados quando relevantes; Spring Boot 4.x (GA em novembro de 2025, sobre Spring Framework 7) como base, com notas de compatibilidade para Spring Boot 3.x. O Apêndice E cobre a migração de Java 17 / Spring Boot 2.7.
- **Verificação de versões:** detalhes que mudam com o tempo (versões, status de *preview*, preços de provedores de IA, licenças) serão conferidos na documentação oficial no momento da escrita de cada capítulo.

### 0.3 Padrão interno de cada capítulo

Todos os capítulos seguem o mesmo esqueleto, adaptado ao assunto (nem todo capítulo terá todos os blocos, mas nenhum bloco relevante será omitido):

1. **Abertura:** cenário-problema real e objetivos de aprendizagem.
2. **Fundamentos:** o que é, que problema resolve, por que surgiu, contexto histórico.
3. **Como funciona por dentro:** componentes, mecanismos internos, diagramas explicados.
4. **Implementação:** versão ingênua → versão robusta; exemplos *incorreto × correto*; código comentado e explicado trecho a trecho.
5. **Comparações e alternativas:** tabela comparativa seguida de análise em texto corrido.
6. **Quando usar e quando NÃO usar.**
7. **Problemas comuns, anti-patterns e armadilhas de produção** (desempenho, escalabilidade, manutenção, segurança, concorrência).
8. **Aplicações reais:** como o conceito aparece em sistemas bancários, pagamentos, e-commerce, alta disponibilidade, tempo real, monólitos e microsserviços.
9. **Pare e Pense:** situação-problema apresentada antes da análise; a resposta comentada vem depois, com os trade-offs de cada caminho.
10. **Break-It Lab:** falha provocada de propósito e roteiro de diagnóstico.
11. **Projeto do capítulo** (quando houver): escopo, requisitos, C4, ADRs e Definição de Pronto.
12. **Exercícios e desafios** graduados.
13. **Conclusão** e ponte para os capítulos seguintes.
14. **Para aprofundar:** documentação oficial, RFCs, livros e artigos de referência.

### 0.4 Quadros e convenções

- **Conceito-chave:** definição precisa com significado, finalidade e importância.
- **Atenção:** armadilha frequente ou consequência de produção.
- **Na prática:** como o assunto aparece em times e sistemas reais.
- **Pare e Pense:** pergunta para reflexão antes da análise.
- **Break-It Lab:** experimento de falha controlada.
- **Correção do material original:** quando o Plano Mestre contém imprecisão, a correção é explicada.
- **Fato × Recomendação:** separa fatos técnicos verificáveis de opiniões e recomendações do autor.
- **Código:** Java e Spring Boot quando pertinentes; SQL, Bash, YAML, HCL, Lua, Protobuf, PromQL e outras linguagens quando forem a ferramenta certa para o conceito.
- **Diagramas:** Mermaid como padrão (classes, sequência, estados, atividades, ER, fluxos, C4); PlantUML e Structurizr DSL nos capítulos que ensinam essas ferramentas. Todo diagrama é acompanhado de explicação e mantém consistência com o código do capítulo.
- **Empresas fictícias recorrentes:** *Banco Aurora* (banco digital e pagamentos) e *Marketplace Vértice* (e-commerce e marketplace) atravessam o livro como fio condutor, permitindo que o leitor veja o mesmo sistema evoluir de monólito simples a plataforma distribuída.

### 0.5 Ordem da obra: progressão alinhada ao `roadmap.sh/java`

A ordem dos capítulos segue a progressão do roadmap Java do `roadmap.sh`: fundamentos da linguagem, aprofundamento (estruturas de dados, generics, streams, serialização, redes, JVM, memória e threads), ferramentas de build, frameworks web (Spring), ORM, logging, acesso a banco de dados e testes. Ao terminar o trecho Java, o próprio roadmap encaminha para o `roadmap.sh/backend`; o livro faz o mesmo e termina no `roadmap.sh/software-architect`, que o Plano Mestre já usava como referência.

> **Nota sobre a fonte:** a página `roadmap.sh/java` é um gráfico interativo. A correspondência abaixo usa a sequência de blocos da versão publicada do roadmap. Os nomes de tópicos individuais variam um pouco entre versões, mas a ordem dos grandes blocos é a mesma.

| Bloco do `roadmap.sh/java` | Onde está no livro |
| :--- | :--- |
| Fundamentos: sintaxe, tipos e variáveis, condicionais, laços, funções | Parte II — Capítulos 5 a 8 |
| Fundamentos: POO, interfaces, classes, pacotes | Parte II — Capítulos 9 a 15 |
| Aprofundamento: tratamento de exceções | Parte II — Capítulo 16 |
| Fundamentos/aprofundamento: estruturas de dados, Collection Framework, generics | Parte III — Capítulos 17 a 19 |
| Aprofundamento: programação funcional e streams | Parte III — Capítulos 20 a 22 |
| Fundamentos/aprofundamento: arquivos e APIs, serialização, redes e sockets | Parte III — Capítulos 23 a 26 |
| Aprofundamento: como a JVM funciona, gerenciamento de memória, garbage collection | Parte IV — Capítulos 27 a 31 |
| Aprofundamento: threads e concorrência | Parte V — Capítulos 32 a 36 |
| Build Tools (Maven, Gradle, Ant) | Parte VI — Capítulo 37 |
| Logging Frameworks (Logback, Log4j2, TinyLog e a fachada SLF4J) | Parte VI — Capítulo 38 |
| Testes: unitários (JUnit, TestNG) e mocking (Mockito) | Parte VI — Capítulo 39 |
| Database Access (JDBC, JDBI3, JdbcTemplate) | Parte VII — Capítulo 42 (JdbcTemplate no Capítulo 57) |
| Web Frameworks (Spring, Spring Boot; Play e outros como alternativas) | Parte VIII — módulo Spring, Capítulos 45 a 65 |
| ORM (JPA, Hibernate, Spring Data JPA, EBean) | Parte VIII — Capítulos 55 a 58 |
| Testes de integração e comportamento (REST Assured, JMeter, Cucumber-JVM, JBehave) | Capítulo 64 e Parte XVIII |
| Continuação: `roadmap.sh/backend` | Partes IX a XXII |
| Continuação: `roadmap.sh/software-architect` | Partes XXIII a XXV |

**Onde o livro se afasta do roadmap, e por quê:**

- **Banco de dados e JDBC antes do Spring.** No roadmap, *Database Access* vem depois de *Web Frameworks* e *ORM*. Aqui, modelagem, SQL, JDBC e transações vêm antes, porque o ORM é construído sobre JDBC e SQL: entender a camada de baixo evita que o Hibernate pareça mágica.
- **Logging e testes unitários antes do Spring.** No roadmap eles aparecem no fim do bloco Java. Antecipá-los faz com que todo código escrito a partir daí já nasça testado e observável. Os testes específicos do Spring continuam no fim do módulo Spring, como no roadmap.
- **Git, Linux e redes.** O roadmap Java não os cobre; eles pertencem ao roadmap backend. O Capítulo 4 ensina o essencial para começar (Git e Docker básicos) e a Parte IX aprofunda, logo depois do bloco Java.
- **Depois do bloco Java,** a ordem segue o roadmap backend sempre que isso não quebra pré-requisitos. Exemplos: mensageria vem antes de Saga e Outbox, e testes e containers vêm antes de CI/CD.

### 0.6 O módulo dedicado ao Spring (Parte VIII)

O Spring ganhou um módulo próprio e contínuo, com 21 capítulos, organizado conforme a progressão do `roadmap.sh/spring-boot`: Spring Core, Spring Boot, Spring MVC, Hibernate, Spring Data, Spring Security, Spring Cloud e testes. Ao longo do módulo, o leitor constrói um **projeto progressivo**: a API de Pedidos do Marketplace Vértice, que ganha uma camada nova a cada capítulo.

| Seção do `roadmap.sh/spring-boot` | Capítulos |
| :--- | :--- |
| Spring Core: introdução, terminologia, arquitetura, por que Spring | 45 |
| Spring Core: injeção de dependência e IoC | 46 |
| Spring Core: configuração e anotações | 47 |
| Spring Core: escopos de beans | 48 |
| Spring Core: Spring AOP | 49 |
| Spring Boot: starters, autoconfiguração, servidor embutido | 50 |
| Spring MVC: Servlet, arquivos JSP, arquitetura, componentes | 51 e 52 |
| Complemento: clientes HTTP e Spring WebFlux | 53 e 54 |
| Hibernate: ciclo de vida de entidades, relacionamentos, transações | 55 e 56 |
| Spring Data: JPA, JDBC, MongoDB | 57 e 58 |
| Spring Security: autenticação, autorização, OAuth2, JWT | 59 e 60 |
| Complemento: `@Async`, `@Scheduled`, Quartz e Spring Batch | 61 |
| Microservices — Spring Cloud: Gateway, Config, Circuit Breaker, OpenFeign, Eureka, Sleuth/Hystrix | 62 e 63 |
| Testing: `@SpringBootTest`, `@MockBean`, MockMvc, testes JPA | 64 |
| Spring Boot: Actuator e operação em produção | 65 |

**Diferenças em relação ao roadmap Spring Boot:**

- **Spring Security vem depois do Spring Data.** No roadmap, Security fica dentro de Spring Core. Aqui, os exemplos de autenticação usam usuários persistidos, então precisam de uma API com banco já funcionando.
- **Projetos que dependem de outros fundamentos continuam onde os pré-requisitos estão,** com remissões a partir do Capítulo 45:
  - Spring Modulith: Capítulo 97, porque depende de DDD.
  - Spring AMQP, Spring Kafka e Spring Cloud Stream: Parte XV, porque dependem de mensageria.
  - Spring Cloud AWS: Capítulo 108.
  - Spring AI: Parte XXI.

### 0.7 Lacunas do material original que serão preenchidas

- **Fundamentos para iniciantes:**
  - Ambiente de desenvolvimento.
  - Ciclo de vida de um programa Java.
  - Sintaxe, tipos, operadores e conversões.
  - Controle de fluxo, métodos e arrays.
  - Classes e objetos.
  - Pacotes e módulos.
  - Anotações e reflexão (base para entender o Spring).
- **Java intermediário:**
  - Programação funcional.
  - Arquivos e I/O.
  - Serialização.
  - Redes e sockets em Java.
  - Unicode e codificação.
  - Medição de desempenho: percentis, Lei de Little, Lei de Amdahl e JMH.
- **Ferramentas e dados:**
  - Frameworks de logging.
  - TDD.
  - JDBC e JDBI.
  - Modelagem de dados (DER e normalização).
  - SQL avançado.
  - Comparação entre bancos relacionais (incluindo SQL Server) e famílias NoSQL.
- **Spring:** o módulo Spring completo, incluindo clientes HTTP, WebFlux, gerenciamento de transações, Spring Data JDBC/MongoDB, agendamento e Spring Batch, Spring Cloud e Spring Boot em produção.
- **Arquitetura e plataforma:**
  - Estratégias de multi-tenancy.
  - Clean Code e refatoração.
  - Fundamentos de arquitetura e estilos arquiteturais (incluindo microsserviços).
  - GraphQL.
  - Fundamentos de caching.
  - Comunicação síncrona × assíncrona.
  - Capítulo comparativo de mensageria.
  - Modelos de consistência.
  - Fundamentos de tolerância a falhas.
  - Estratégias de deploy e métricas DORA.
  - GitLab CI.
  - Helm e GitOps.
  - Fundamentos de observabilidade.
- **IA, arquitetura e System Design:**
  - RAG × fine-tuning × contexto longo.
  - Padrões de workflows para agentes.
  - Dívida técnica.
  - Anti-patterns arquiteturais.
  - Replicação de dados.
  - CDN e borda global.
  - Estudos de caso de System Design.
  - Migração de Spring Boot 2.7 para 3/4.

### 0.8 Correções técnicas previstas

Correções ao Plano Mestre original:

| # | Trecho do original | Correção ou contextualização |
| :-: | :--- | :--- |
| 1 | `HashMap` faz *treeification* quando o bucket ≥ 8 | Também exige capacidade da tabela ≥ 64 (`MIN_TREEIFY_CAPACITY`); abaixo disso, o mapa redimensiona. A árvore volta a lista com 6 elementos. |
| 2 | RFC 7807 `ProblemDetail` | A RFC 7807 foi substituída pela RFC 9457 (2023), que é compatível e mantém o mesmo modelo. |
| 3 | *Thread pinning* em Virtual Threads | Desde o JDK 24 (JEP 491), `synchronized` não fixa mais a virtual thread na carrier thread; o pinning persiste em frames nativos/JNI. O capítulo explica o antes e o depois. |
| 4 | `StructuredTaskScope` e `ScopedValue` | No Java 25, `ScopedValue` é final (JEP 506) e Structured Concurrency segue em *preview* (JEP 505), com API diferente da do Java 21. |
| 5 | "Stack LGTM: Prometheus, Loki, Tempo, Grafana" | LGTM significa Loki, Grafana, Tempo e Mimir. Prometheus é o modelo e o ecossistema de métricas com o qual o Mimir é compatível. |
| 6 | "6 Rs de migração" | A AWS passou a usar 7 Rs (inclui *Relocate*). Ambos os modelos serão apresentados. |
| 7 | ACID e BASE contados como "padrões" | São modelos/propriedades de consistência, não design patterns. Serão tratados como modelos; os projetos 10.01 e 10.02 são mantidos. |
| 8 | Semântica *exactly-once* | Entrega exatamente-uma-vez de ponta a ponta não é garantível em geral; o que se obtém é processamento *efetivamente uma vez* (idempotência + transações). O EOS do Kafka vale para o ciclo ler-processar-escrever dentro do Kafka. |
| 9 | "Redis *single-threaded*" | A execução de comandos é single-threaded; desde o Redis 6 há *I/O threads* opcionais, e persistência usa processos/threads em segundo plano. |
| 10 | Fórmula do HikariCP | É um ponto de partida difundido pela comunidade PostgreSQL e pela documentação do HikariCP, não uma lei; deve ser validada com testes de carga. O conceito de *spindle* perde sentido em SSDs e será discutido. |
| 11 | IcePanel como *diagrams-as-code* | IcePanel é uma ferramenta visual e colaborativa de modelagem C4, não *diagrams-as-code*. |
| 12 | "90% das vagas de Arquiteto exigem Brownfield" | Estatística sem fonte; será reescrita de forma qualitativa. |
| 13 | Metas numéricas dos projetos e de FinOps de IA (ex.: < 300 ms, < 5 ms, 60–85% de economia de tokens, 50–90% de desconto em *prompt caching*) | Tratadas como requisitos de projeto a medir, não como fatos. Descontos e preços dependem do provedor e serão conferidos na documentação oficial. |
| 14 | ISO/IEC 25010 | A revisão de 2023 tem nove características (inclui *Safety*; *Usability* virou *Interaction Capability*; *Portability* virou *Flexibility*). |
| 15 | "OWASP Top 10 API" | São duas listas distintas: OWASP Top 10 (aplicações web, edição 2025) e OWASP API Security Top 10 (2023). Ambas serão cobertas. |
| 16 | Concatenação de `String` com `+` | Desde o Java 9 a concatenação em uma expressão é compilada via `invokedynamic` (`StringConcatFactory`); o problema real é a concatenação dentro de laços. |
| 17 | Cache de `Integer` (−128 a 127) | É o padrão; o limite superior é configurável (`-XX:AutoBoxCacheMax`), por isso nunca se deve depender de `==` entre wrappers. |
| 18 | *Semantic cache* com similaridade ≥ 0,95 | O limiar precisa ser calibrado por domínio; valores altos ou baixos demais trazem falsos positivos ou cache inútil. |
| 19 | Java "17 a 21+" e Spring Security 6 | Atualizado para incluir Java 25 LTS e Spring Security 7 (Spring Boot 4), com notas para as versões anteriores. |

Correções ao `roadmap.sh/spring-boot` (tópicos que o roadmap ainda lista, mas que mudaram):

| # | Item do roadmap | Correção ou contextualização |
| :-: | :--- | :--- |
| 20 | Hystrix | Em modo de manutenção desde 2018 e removido do Spring Cloud. O substituto é o Spring Cloud Circuit Breaker com Resilience4j. Hystrix é apresentado apenas como contexto histórico. |
| 21 | Spring Cloud Sleuth | Não acompanha o Spring Boot 3+. O rastreamento passou para o Micrometer Tracing, com exportação via OpenTelemetry. |
| 22 | `@MockBean` | Depreciado no Spring Boot 3.4 em favor de `@MockitoBean` e `@MockitoSpyBean` (Spring Framework 6.2+). |
| 23 | Arquivos JSP | Têm limitações conhecidas com servidores embutidos e JAR executável no Spring Boot. São tratados como legado; Thymeleaf é a alternativa apresentada. |
| 24 | Eureka como descoberta de serviços padrão | Continua válido, mas em Kubernetes o DNS e os Services nativos costumam tornar o Eureka desnecessário. Ambos são comparados. |

### 0.9 Escala da obra e organização em volumes

A estrutura tem **25 partes e 183 capítulos**. Proponho organizá-la como uma coleção em seis volumes, com numeração contínua de capítulos:

| Volume | Partes | Capítulos | Tema |
| :-: | :-: | :-: | :--- |
| 1 | I–V | 1–36 | A linguagem Java: da base à JVM e à concorrência |
| 2 | VI–VIII | 37–65 | Ferramentas, bancos de dados e o ecossistema Spring |
| 3 | IX–XIII | 66–100 | Infraestrutura, dados avançados, segurança, design e arquitetura de aplicações |
| 4 | XIV–XVIII | 101–134 | Sistemas distribuídos: cache, mensageria, consistência, resiliência e qualidade |
| 5 | XIX–XXII | 135–159 | Plataforma, observabilidade e engenharia de IA |
| 6 | XXIII–XXV | 160–183 | Arquitetura corporativa, System Design e projeto integrador |

### 0.10 Plano de produção

- Escrita na ordem dos capítulos, um capítulo por entrega (dois quando forem curtos e interdependentes), cada um em arquivo próprio.
- Glossário, referências e índice remissivo alimentados incrementalmente a cada capítulo.
- Prefácio e Introdução escritos primeiro (definem tom e convenções); Conclusão e revisão final da obra ao término.
- Ao fim de cada Parte: revisão de lacunas, contradições e repetições, e compilação da Parte/Volume em PDF com diagramas renderizados.

---

## Elementos pré-textuais

- **Capa:** título, subtítulo e autor.
- **Folha de rosto e página de apresentação:** o que é a obra, a quem se destina, como foi construída a partir do Plano Mestre e o que o leitor será capaz de fazer ao final.
- **Prefácio:** a motivação da obra, a diferença entre usar ferramentas e pensar como engenheiro, e o compromisso com profundidade e honestidade técnica.
- **Sumário.**
- **Introdução — Como usar este livro:** organização em partes e volumes; padrão dos capítulos e quadros; trilhas de leitura por nível (Júnior, Pleno, Sênior, Staff, Arquiteto); ambiente de laboratório; organização dos repositórios de projetos (incluindo o multi-módulo `java-design-patterns-realworld`); correspondência com `roadmap.sh/java`, `roadmap.sh/backend` e `roadmap.sh/software-architect`.

---

# VOLUME 1 — A LINGUAGEM JAVA: DA BASE À CONCORRÊNCIA

## PARTE I — A JORNADA E O MÉTODO

### Capítulo 1 — A carreira em engenharia de software: de Júnior a Arquiteto
*O que o mercado realmente avalia em cada nível e quais competências técnicas e comportamentais marcam cada transição. Serve de mapa para todo o livro.*
1. O que define senioridade: autonomia, complexidade resolvida, comunicação e impacto no negócio
2. Júnior → Pleno: autonomia tática e requisitos técnicos obrigatórios
3. Pleno → Sênior: *ownership* em produção, sistemas distribuídos e mentoria
4. Sênior → Especialista/Staff: multiplicação técnica, padrões corporativos, modernização e FinOps
5. Especialista → Arquiteto: as esferas *Application*, *Solution* e *Enterprise*
6. Trilhas paralelas: carreira técnica (IC) × carreira de gestão
7. Benchmark `roadmap.sh` e mapa de competências × capítulos
8. Horizonte realista de 4 a 5,5 anos e por que prazos são estimativas, não promessas

**Destaques práticos:** diagrama da progressão de carreira; matriz de competências por nível; checklist de autoavaliação.

### Capítulo 2 — Aprender a aprender engenharia: o método de alta retenção
*Como estudar uma trilha de vários anos sem cair no Tutorial Hell, com técnicas de aprendizagem baseadas em evidência e prática deliberada.*
1. Tutorial Hell e a ilusão de competência
2. A regra 20/60/20 (teoria na fonte, prática deliberada, consolidação)
3. O ciclo de 4 passos: mapa mental + C4, Break-It Lab, projeto com escopo fechado, ADR
4. Método Feynman, recuperação ativa e repetição espaçada
5. Rotina semanal sustentável e modo manutenção para semanas caóticas
6. IA como revisora técnica (Staff Engineer / Architecture Review Board), não como muleta — prompts recomendados e proibidos
7. Definição de Pronto (DoD) para avançar de capítulo
8. Portfólio profissional: organização de repositórios, README executivo e evidências de aprendizado

**Destaques práticos:** fluxograma do ciclo de estudo; template de ADR de estudo; modelo de README de projeto.

### Capítulo 3 — A linguagem visual do engenheiro: UML essencial e introdução ao C4
*Ensina a ler e desenhar os diagramas usados em todo o livro, para que nenhum diagrama posterior seja um obstáculo.*
1. Por que diagramar: comunicação, raciocínio e documentação
2. Diagrama de classes: associação, agregação, composição, herança, realização e multiplicidade
3. Diagrama de sequência: mensagens síncronas, assíncronas, retornos e fragmentos (`alt`, `loop`, `opt`)
4. Diagrama de atividades e diagrama de estados
5. Diagramas de componentes e de implantação
6. Diagrama Entidade-Relacionamento: notação pé-de-galinha (*crow's foot*) × Chen
7. Introdução ao C4 Model: níveis 1 (Contexto) e 2 (Containers)
8. Diagrams-as-code com Mermaid e PlantUML: convenções adotadas no livro

**Destaques práticos:** o mesmo domínio (pedido de e-commerce do Marketplace Vértice) desenhado em cada tipo de diagrama, mostrando o que cada visão revela e esconde.

### Capítulo 4 — Preparando o ambiente de desenvolvimento
*O mínimo necessário para começar a programar e versionar desde o primeiro capítulo técnico.*
1. Instalando o JDK: distribuições, gerenciadores de versão e `JAVA_HOME`
2. IDEs: IntelliJ IDEA × Eclipse × VS Code; uso do depurador
3. Terminal essencial (Bash e PowerShell)
4. Git essencial: `init`, `clone`, `add`, `commit`, `branch`, `push` e `pull` (aprofundado na Parte IX)
5. Docker essencial: subir um PostgreSQL com Docker Compose (aprofundado na Parte IX)
6. Organização dos repositórios de estudo

**Destaques práticos:** checklist de ambiente; primeiro repositório versionado com um "Olá, mundo" depurado passo a passo.

---

## PARTE II — FUNDAMENTOS DA LINGUAGEM JAVA

*Correspondência no `roadmap.sh/java`: Learn the Fundamentals (sintaxe, tipos e variáveis, condicionais, laços, funções, POO, interfaces, classes e pacotes) e tratamento de exceções.*

### Capítulo 5 — A plataforma Java e o ciclo de vida de um programa
*O que acontece entre escrever o código-fonte e vê-lo executando.*
1. JDK, JRE e JVM; distribuições do OpenJDK
2. Ciclo de vida de um programa: código-fonte → `javac` → bytecode → carregamento → interpretação/JIT → execução → término
3. O método `main`, argumentos de linha de comando e código de saída; execução direta de arquivo-fonte
4. Classpath e arquivos JAR
5. Ferramentas do JDK: `javac`, `java`, `jshell`, `jar`, `javadoc` e `jcmd`

**Destaques práticos:** diagrama de atividades do ciclo de vida de um programa; primeiros experimentos no `jshell`.

### Capítulo 6 — Sintaxe básica, tipos de dados, variáveis e operadores
*Os blocos elementares da linguagem, com atenção às armadilhas que acompanham o programador por toda a carreira.*
1. Estrutura de um programa, comentários e convenções de nomenclatura
2. Tipos primitivos: tamanhos, faixas e valores padrão
3. Variáveis e escopo (bloco, método, classe); `var` e inferência de tipo local
4. Literais e constantes
5. Operadores aritméticos, relacionais, lógicos e bit a bit; precedência e curto-circuito
6. Conversão de tipos: promoção automática, *casting* explícito, perda de precisão e *overflow* silencioso
7. A classe `Math` e operações matemáticas (`floorDiv`, `floorMod`, métodos `*Exact`)

**Destaques práticos:** tabela de tipos primitivos; exemplos de conversões que perdem dados sem aviso.

### Capítulo 7 — Controle de fluxo, métodos e arrays
*Decisões, repetições e a organização do código em métodos.*
1. Condicionais: `if/else`, operador ternário, `switch` clássico × *switch expressions*
2. Laços: `for`, *for-each*, `while`, `do-while`; `break`, `continue` e rótulos
3. Métodos: parâmetros, retorno, *varargs* e recursão (e o `StackOverflowError`)
4. Arrays: declaração, inicialização, arrays multidimensionais e a classe utilitária `Arrays`
5. Entrada e saída no console
6. Lógica aplicada: calculadora de parcelas e validador de CPF

**Destaques práticos:** fluxogramas de decisão; diagrama da pilha de chamadas em uma recursão.

### Capítulo 8 — Strings, texto e codificação
*Texto parece simples até aparecerem acentos, regex lentas e concatenação em laços.*
1. Imutabilidade, String Pool e `intern()`
2. Concatenação: `+` × `StringBuilder` e o que o compilador faz desde o Java 9
3. Text blocks (`"""`)
4. Expressões regulares: `Pattern.compile` pré-compilado e ReDoS (negação de serviço por regex)
5. Unicode, UTF-8, `Charset` e normalização (acentuação em português)
6. Formatação e `Locale` (pt-BR)

**Destaques práticos:** benchmark comentado de concatenação em laço; regex vulnerável × segura.

### Capítulo 9 — Classes e objetos
*Do primeiro `new` ao entendimento de onde os objetos vivem e como são passados entre métodos.*
1. Classe × objeto; atributos, métodos, construtores e `this`
2. Modificadores de acesso: `public`, `protected`, *package-private* e `private`
3. `static`: membros de classe × membros de instância
4. `final` em variáveis, métodos e classes
5. Blocos de inicialização e ordem de inicialização
6. Classes aninhadas: *static nested*, *inner*, locais e anônimas
7. Ciclo de vida do objeto: criação, alcançabilidade e coleta
8. Stack × Heap; Java é sempre *pass-by-value* (cópia do valor da referência)
9. Encadeamento de métodos (*method chaining*) e interfaces fluentes

**Destaques práticos:** diagramas de Stack e Heap durante a passagem de parâmetros; diagrama da ordem de inicialização de uma classe.

### Capítulo 10 — Os pilares da orientação a objetos
*POO como ferramenta para proteger regras de negócio, não como cerimônia.*
1. Encapsulamento forte: invariantes validadas no construtor; objetos sempre válidos × dezenas de setters soltos
2. Herança: `extends`, `super`, construtores e sobrescrita
3. Herança × composição: "é-um" genuíno × "tem-um"; o problema da classe base frágil
4. Polimorfismo: sobrecarga (*overloading*, ligação estática em compilação) × sobrescrita (*overriding*, ligação dinâmica em runtime)
5. Abstração: classes abstratas × interfaces modernas (`default`, `static`, `private`) e `@FunctionalInterface`
6. Imutabilidade como estratégia de design

**Destaques práticos:** diagramas de classes comparando herança e composição; refatoração de uma `ContaBancaria` anêmica para uma classe com invariantes.

### Capítulo 11 — Enums, records e wrapper classes
*Tipos especiais que eliminam classes inteiras de bugs quando bem usados.*
1. Enums com atributos, construtores privados e comportamento por constante; `EnumMap` e `EnumSet`
2. Enums como máquinas de estado simples
3. Records: dados imutáveis concisos, construtor compacto com validação e limites do recurso
4. Wrapper classes: por que existem
5. Autoboxing e unboxing: `NullPointerException` silencioso, cache de `Integer` e `==` × `equals`

**Destaques práticos:** enum de categorias financeiras com regras por constante; diagrama de estados de um enum de status; record com validação.

### Capítulo 12 — Precisão numérica e dinheiro
*Os detalhes que mais causam bugs graves em sistemas financeiros.*
1. Ponto flutuante IEEE 754: por que `0.1 + 0.2 != 0.3`
2. `BigDecimal`: `new BigDecimal(String)` × `valueOf` × `new BigDecimal(double)`, `scale`, `precision`, `RoundingMode` (incluindo `HALF_EVEN`) e a armadilha `equals` × `compareTo`
3. Dinheiro em Java: `long` em centavos × `BigDecimal` × Money API (JSR 354) — comparação
4. *Overflow* de inteiros e `Math.addExact`
5. Arredondamento em parcelamentos e rateio de centavos

**Destaques práticos:** parcelamento com dízimas implementado de forma incorreta e correta.

### Capítulo 13 — O contrato de `java.lang.Object` e a ordenação de objetos
*Por que objetos "somem" de coleções e como implementar igualdade e ordenação corretamente.*
1. `equals`: reflexividade, simetria, transitividade, consistência e não-nulidade
2. `hashCode` e o contrato com `equals`
3. Objetos mutáveis como chave de `HashMap` e `HashSet`
4. `equals`/`hashCode` em entidades JPA (prévia do Capítulo 55)
5. `toString` e por que evitar `clone`
6. `Comparable` × `Comparator`; consistência com `equals`; `Comparator.comparing` encadeado
7. Break-It Lab: quebrar o contrato `hashCode` e ver o objeto "sumir" do `HashMap`

**Destaques práticos:** diagrama de buckets do `HashMap` mostrando a busca falhando.

### Capítulo 14 — Pacotes, módulos e organização de código
*Como organizar código para que as fronteiras do sistema sejam respeitadas pelo compilador.*
1. Pacotes, `import` e convenções de nomenclatura
2. *Package-private* como fronteira de módulo
3. JARs, classpath e conflitos de versão (prévia do Capítulo 37)
4. JPMS: `module-info.java`, `exports`, `requires` e encapsulamento forte
5. Quando o JPMS vale a pena (e por que muitos projetos Spring não o adotam)

**Destaques práticos:** diagrama de dependências entre pacotes e módulos; módulo que esconde sua implementação.

### Capítulo 15 — Anotações e reflexão
*Os mecanismos que frameworks como Spring, Hibernate e JUnit usam por baixo dos panos.*
1. O que são anotações; anotações do JDK (`@Override`, `@Deprecated`, `@FunctionalInterface`, `@SuppressWarnings`)
2. Meta-anotações: `@Retention`, `@Target`, `@Inherited` e `@Repeatable`
3. Criando anotações próprias
4. Reflection API: `Class`, `Method`, `Field` e `Constructor`; custos e riscos
5. Processamento de anotações em tempo de compilação (Lombok, MapStruct)
6. Proxies dinâmicos (`java.lang.reflect.Proxy`): a base do Spring AOP

**Destaques práticos:** mini-framework de validação com anotações próprias e reflexão; diagrama de sequência de uma chamada via proxy dinâmico.

### Capítulo 16 — Tratamento profissional de exceções
*Como erros devem fluir por uma aplicação sem esconder problemas nem poluir o código.*
1. Hierarquia `Throwable`: `Error` × `Exception`; *checked* × *unchecked* (`RuntimeException`) e o debate em torno delas
2. `try-with-resources`, `AutoCloseable` e exceções suprimidas
3. Hierarquia limpa de exceções de domínio
4. Anti-patterns: engolir exceções, *log-and-throw*, exceção como controle de fluxo, capturar `Exception`
5. Exceções × tipos de resultado (`Result`/`Either`) — alternativas e trade-offs
6. Tradução de exceções entre camadas

**Destaques práticos:** diagrama da hierarquia `Throwable`; hierarquia de exceções do Banco Aurora.

---

## PARTE III — JAVA INTERMEDIÁRIO: ESTRUTURAS DE DADOS, PROGRAMAÇÃO FUNCIONAL E I/O

*Correspondência no `roadmap.sh/java`: Data Structures, Collection Framework, Generics, Streams, Working with Files and APIs, Serialization e Networking & Sockets.*

### Capítulo 17 — Complexidade algorítmica e Big-O
*A linguagem para raciocinar sobre o custo de algoritmos e estruturas antes de medir.*
1. Por que medir complexidade; notações O, Θ e Ω; melhor, pior e caso médio
2. Classes de complexidade: O(1), O(log n), O(n), O(n log n), O(n²) e exponencial
3. Complexidade de espaço e custo amortizado
4. Algoritmos fundamentais: busca binária e ordenação (TimSort e *dual-pivot quicksort* no JDK)
5. Big-O × realidade: constantes, cache de CPU e localidade de memória

**Destaques práticos:** gráfico de crescimento das classes; implementações comentadas de busca binária.

### Capítulo 18 — Estruturas de dados e o Collections Framework
*Como cada coleção do JDK funciona internamente e como escolher a certa.*
1. Array × `ArrayList`
2. Hierarquia: `Collection`, `List`, `Set`, `Queue`, `Deque` e `Map`
3. `ArrayList` × `LinkedList` (e por que a `LinkedList` raramente vence)
4. Pilhas e filas: `Stack` (legado) × `ArrayDeque`; `PriorityQueue` (heap binário)
5. `Iterator`, `ListIterator`, comportamento *fail-fast* e `ConcurrentModificationException`
6. Anatomia do `HashMap`: buckets, espalhamento do hash, *load factor* 0,75, redimensionamento, colisões e *treeification*
7. `LinkedHashMap` (base de caches LRU), `TreeMap` (árvore rubro-negra), `EnumMap`, `HashSet` e `TreeSet`
8. Coleções imutáveis (`List.of`) × não modificáveis; *Sequenced Collections* (Java 21)
9. Guia de decisão: qual coleção usar em cada cenário

**Destaques práticos:** diagramas internos de `ArrayList`, `HashMap` e `TreeMap`; tabela de complexidades por operação; cache LRU com `LinkedHashMap`.

### Capítulo 19 — Generics a fundo
*Segurança de tipos em tempo de compilação e os limites impostos pelo type erasure.*
1. Por que generics existem; *type erasure*
2. Tipos limitados (*bounded types*) e wildcards
3. PECS: *Producer Extends, Consumer Super*
4. Métodos genéricos e inferência de tipos
5. Limitações: arrays genéricos, `instanceof`, *heap pollution* e `@SafeVarargs`

**Destaques práticos:** API genérica de repositório; exemplos incorreto × correto de wildcards.

### Capítulo 20 — Programação funcional: lambdas, interfaces funcionais e `Optional`
*Funções como valores e a eliminação de `null` como retorno.*
1. Lambdas e *method references*
2. Interfaces funcionais do JDK: `Function`, `Predicate`, `Supplier`, `Consumer`, `BiFunction` e variantes primitivas
3. Funções de alta ordem e composição (`andThen`, `compose`, `Predicate.and`)
4. Captura de variáveis (*effectively final*) e closures
5. `Optional`: propósito (retorno de métodos), `map`, `flatMap`, `filter`, `orElse` × `orElseGet` × `orElseThrow`
6. Anti-patterns de `Optional`: parâmetros, atributos e campos JPA, `Optional.get()` sem verificação

**Destaques práticos:** motor de regras de desconto construído por composição de funções.

### Capítulo 21 — Stream API
*Expressar transformações de dados de forma declarativa sem cair em armadilhas de desempenho.*
1. Pipeline, avaliação preguiçosa, operações intermediárias e terminais
2. Operações essenciais: `map`, `filter`, `flatMap`, `reduce`, `sorted` e `distinct`
3. Collectors: `groupingBy`, `partitioningBy`, `toMap`, `joining`, `teeing` e collectors customizados (`Collector.of`)
4. Streams primitivos (`IntStream`, `LongStream`) e o custo do boxing
5. Stream Gatherers (operações intermediárias customizadas)
6. Parallel streams: quando ajudam, quando atrapalham e o `ForkJoinPool` comum
7. Anti-patterns: efeitos colaterais e "stream para tudo"

**Destaques práticos:** relatório financeiro com collectors customizados; diagrama do pipeline de um stream.

### Capítulo 22 — Java moderno: da versão 17 à 25
*Os recursos que mudaram a forma de modelar dados em Java.*
1. Cadência de releases e versões LTS (17, 21, 25)
2. Records
3. Sealed classes e interfaces
4. Pattern matching para `instanceof` e `switch`, *record patterns* e verificação de exaustividade
5. Programação orientada a dados (*Data-Oriented Programming*) com records + sealed
6. Demais recursos relevantes até o Java 25 (conferidos na documentação oficial no momento da escrita)

**Destaques práticos:** modelagem de meios de pagamento com sealed + records + switch exaustivo; comparação com a modelagem clássica por herança.

### Capítulo 23 — Datas e horas com `java.time`
*Tempo é uma das fontes mais traiçoeiras de bugs em produção.*
1. Por que `java.util.Date` e `Calendar` falharam
2. `LocalDate`, `LocalTime`, `LocalDateTime`, `Instant`, `ZonedDateTime` e `OffsetDateTime`
3. Fusos horários: `America/Sao_Paulo`, o histórico de horário de verão e a base de dados de fusos
4. `Duration` × `Period`; `DateTimeFormatter` e *parsing*
5. `Clock` injetável e testabilidade
6. Persistência e transmissão de datas (UTC e ISO-8601) e armadilhas comuns

**Destaques práticos:** linha do tempo dos tipos de data; cálculo de vencimento em dia útil.

### Capítulo 24 — Arquivos e I/O essencial
*Ler e escrever dados de forma correta, segura e eficiente.*
1. `java.io`: streams de bytes × de caracteres, `Reader`/`Writer` e *buffering*
2. `try-with-resources` aplicado a I/O
3. `java.nio.file`: `Path`, `Files`, percorrendo diretórios e leitura em streaming
4. Codificação de arquivos (UTF-8, BOM) e erros clássicos
5. Leitura e escrita robusta de CSV
6. Tratamento de erros de I/O

**Destaques práticos:** importador de extrato bancário em CSV processado em streaming.

### Capítulo 25 — Serialização: Java nativo, JSON e formatos de dados
*Como objetos viram bytes e texto, e por que a serialização nativa do Java é perigosa.*
1. O que é serialização; formatos textuais × binários
2. Serialização nativa (`Serializable`): funcionamento, `serialVersionUID` e os riscos de desserialização insegura
3. JSON com Jackson: `ObjectMapper`, módulos (`JavaTimeModule`), records, anotações e configuração segura
4. Jackson × Gson × JSON-B
5. Formatos binários (Protobuf, Avro): prévia dos Capítulos 99 e 113
6. **Projeto: `FinTrack Core`** — motor de finanças pessoais e parcelamento em Java puro: faturas, parcelas com `BigDecimal`, fusos com `ZonedDateTime`, enums ricos, deduplicação via `equals/hashCode` e importação/exportação CSV e JSON com `try-with-resources`

**Destaques práticos:** comparação do mesmo objeto em três formatos; diagrama de classes do FinTrack Core.

### Capítulo 26 — Redes em Java: sockets e clientes HTTP
*Como programas Java conversam pela rede.*
1. Sockets TCP: `ServerSocket` e `Socket`; um servidor de eco
2. UDP com `DatagramSocket`
3. `URI` e `java.net.http.HttpClient`: chamadas síncronas, assíncronas e HTTP/2
4. Timeouts de conexão e de leitura: o erro mais comum em integrações
5. Um servidor HTTP mínimo com o JDK
6. Os fundamentos de rede por trás do código (prévia dos Capítulos 69 a 71)

**Destaques práticos:** diagrama de sequência cliente-servidor via socket; cliente HTTP com timeouts corretos.

---

## PARTE IV — A JVM E O DESEMPENHO

*Correspondência no `roadmap.sh/java`: How JVM works?, Memory Management e Garbage Collection.*

### Capítulo 27 — Medindo desempenho: latência, throughput e microbenchmarks
*Antes de otimizar, é preciso medir corretamente — e a média quase sempre engana.*
1. Latência × throughput; percentis (p50, p95, p99) e caudas de latência
2. Lei de Little e Lei de Amdahl (base para dimensionar pools e prever ganhos de paralelismo)
3. JMH: microbenchmarks corretos, *warmup*, eliminação de código morto e *constant folding*
4. *Coordinated omission* (prévia do Capítulo 132)

**Destaques práticos:** benchmark JMH completo; cálculo de dimensionamento de pool pela Lei de Little.

### Capítulo 28 — A JVM por dentro: carregamento, bytecode e compilação
*Do `.class` ao código de máquina otimizado.*
1. Arquitetura da JVM
2. ClassLoaders: hierarquia, delegação, isolamento; `ClassNotFoundException` × `NoClassDefFoundError`
3. Lendo bytecode com `javap -c`
4. Interpretador, JIT C1/C2, compilação em camadas, *inlining*, *escape analysis* e desotimização
5. AOT com GraalVM Native Image (mundo fechado, configuração de reflexão) e Spring AOT
6. JIT × AOT × CDS/AppCDS e Project Leyden: *startup*, desempenho de pico e memória

**Destaques práticos:** diagrama da arquitetura da JVM; tabela comparativa JIT × AOT; mesmo serviço medido nos dois modos.

### Capítulo 29 — Memória e Garbage Collection
*Onde os objetos vivem, como morrem e como escolher e ajustar o coletor.*
1. Áreas de memória: Heap (Eden, Survivor, Old), Metaspace, Thread Stacks, Code Cache e Off-Heap
2. Fundamentos de GC: alcançabilidade, hipótese geracional, *mark-sweep-compact* e *stop-the-world*
3. Coletores: Serial, Parallel, G1, ZGC geracional e Shenandoah — comparação
4. Ajuste fino: throughput × latência × footprint, flags essenciais e leitura de GC logs
5. Causas típicas de *memory leak* em Java

**Destaques práticos:** diagrama das regiões do heap e do ciclo de promoção; análise de GC log comentada.

### Capítulo 30 — I/O de alto desempenho com NIO.2
*Processar arquivos de gigabytes com memória constante.*
1. De `java.io` a `java.nio`: channels e buffers (retomando o Capítulo 24)
2. `ByteBuffer` (heap × direct), `Channel` e `FileChannel`
3. *Memory-mapped files* e a Foreign Function & Memory API como alternativa moderna
4. Processamento de arquivos gigantes com memória constante
5. I/O assíncrono e `WatchService`

**Destaques práticos:** leitor de CSV de 10 GB em streaming; diagrama de fluxo de buffers.

### Capítulo 31 — Diagnóstico e profiling da JVM
*O kit do engenheiro sênior para incidentes de CPU, memória e travamentos.*
1. Metodologia de diagnóstico
2. Thread dumps (`jstack`, `jcmd`): deadlocks e threads bloqueadas
3. Heap dumps e Eclipse MAT: *dominator tree* e *retained size*
4. JDK Flight Recorder e JDK Mission Control
5. async-profiler e *flame graphs* (CPU, alocação, *wall-clock*)
6. Break-It Lab: `OutOfMemoryError` proposital e análise do heap dump
7. **Projeto: `SwiftRecon`** — conciliador B2B de arquivos CSV/EDI de 10 GB+ com NIO.2, heap abaixo de 256 MB e binário nativo GraalVM

**Destaques práticos:** leitura guiada de um flame graph; diagrama C4 e pipeline do SwiftRecon.

---

## PARTE V — CONCORRÊNCIA E PARALELISMO

*Correspondência no `roadmap.sh/java`: Basics of Threads e concorrência.*

### Capítulo 32 — Fundamentos de concorrência
*Os problemas que surgem quando mais de uma coisa acontece ao mesmo tempo.*
1. Concorrência × paralelismo; processos × threads; troca de contexto
2. Threads em Java: ciclo de vida, `Runnable` e `Callable`
3. Condições de corrida: *check-then-act* e *read-modify-write*
4. Deadlock, livelock e starvation; condições de Coffman
5. Tarefas *CPU-bound* × *I/O-bound*

**Destaques práticos:** diagrama de estados de uma thread; contador concorrente incorreto × correto; deadlock reproduzido.

### Capítulo 33 — Java Memory Model
*Por que um valor escrito por uma thread pode não ser visto por outra.*
1. Caches de CPU, reordenação de instruções e visibilidade
2. A relação *happens-before*
3. `volatile`: o que garante e o que não garante
4. `synchronized`: exclusão mútua e visibilidade
5. Imutabilidade, publicação segura e semântica de campos `final`
6. *Double-checked locking*: versão quebrada × versão correta

**Destaques práticos:** diagramas de caches por núcleo e de arestas happens-before.

### Capítulo 34 — Primitivas de sincronização e estruturas concorrentes
*As ferramentas do `java.util.concurrent` e quando cada uma é a escolha certa.*
1. CAS, classes `Atomic*`, `AtomicReference` e `LongAdder` sob contenção
2. `ReentrantLock` (justiça, `tryLock`), `ReadWriteLock` e `StampedLock` (leitura otimista)
3. `Semaphore`, `CountDownLatch`, `CyclicBarrier` e `Phaser`
4. `ConcurrentHashMap`, `CopyOnWriteArrayList` e `BlockingQueue` (produtor-consumidor)
5. `ThreadLocal` e seus perigos (vazamentos em pools)

**Destaques práticos:** tabela de decisão de primitivas; produtor-consumidor com `BlockingQueue`.

### Capítulo 35 — Executores, pools e programação assíncrona
*Como organizar trabalho concorrente sem criar threads à mão.*
1. `ThreadPoolExecutor`: core/max, filas, políticas de rejeição; dimensionamento CPU-bound × I/O-bound
2. `ForkJoinPool` e *work-stealing*
3. `CompletableFuture`: composição, tratamento de erros, timeouts e escolha de executor
4. Programação reativa: conceitos, *backpressure* e quando faz sentido (Spring WebFlux no Capítulo 54)

**Destaques práticos:** agregador de cotações com `CompletableFuture`; diagrama do ThreadPoolExecutor.

### Capítulo 36 — Virtual Threads e Project Loom
*O modelo que devolveu ao Java a simplicidade do código bloqueante com escalabilidade de I/O.*
1. O limite do modelo *thread-per-request*; o modelo M:N e *continuations*
2. Criando e usando virtual threads (uso no Spring retomado nos Capítulos 50 e 65)
3. *Pinning*: o que era, o que mudou no JDK 24 e o que ainda causa pinning
4. Por que nunca fazer pool de virtual threads; limitando concorrência com `Semaphore`
5. Structured Concurrency (`StructuredTaskScope`) e seu status de preview
6. `ScopedValue` × `ThreadLocal`
7. Platform threads × reativo × virtual threads — comparação
8. **Projeto: `FarePulse`** — agregador que dispara 150+ chamadas externas em paralelo com virtual threads e structured concurrency, timeouts rigorosos e consolidação com meta de < 300 ms

**Destaques práticos:** diagrama de mounting/unmounting em carrier threads; diagrama de sequência do FarePulse.

---

# VOLUME 2 — FERRAMENTAS, BANCOS DE DADOS E O ECOSSISTEMA SPRING

## PARTE VI — FERRAMENTAS DO ECOSSISTEMA JAVA: BUILD, LOGGING E TESTES

*Correspondência no `roadmap.sh/java`: Build Tools, Logging Frameworks e Testing your Apps (testes unitários e mocking).*

### Capítulo 37 — Build de projetos Java: Maven e Gradle
*Como dependências, plugins e módulos são resolvidos, e como evitar o inferno de versões.*
1. Para que servem ferramentas de build; repositórios e resolução de dependências
2. Maven: ciclo de vida, fases, plugins, `dependencyManagement`, BOM, `dependency:tree`, conflitos (*nearest wins*) e Enforcer Plugin
3. `surefire` × `failsafe`: testes unitários e de integração no build
4. Projetos multi-módulo
5. Gradle: grafo de tarefas, *build cache*, Kotlin DSL e *version catalogs*
6. Maven × Gradle: comparação e critérios de escolha
7. Ant e Bazel: contexto histórico e onde ainda aparecem

**Destaques práticos:** criação de um BOM corporativo; projeto multi-módulo de exemplo.

### Capítulo 38 — Logging em Java
*Logs bem feitos encurtam incidentes; logs mal feitos vazam dados e derrubam desempenho.*
1. Para que logar e o que logar; níveis de log
2. SLF4J como fachada; Logback, Log4j2, `java.util.logging` e TinyLog
3. Configuração: *appenders*, *layouts* e níveis por pacote
4. Logs estruturados (JSON) e MDC para correlação
5. Desempenho: logging assíncrono e custo de construção de mensagens
6. Segurança: Log4Shell (CVE-2021-44228), *log injection* e dados pessoais em logs

**Destaques práticos:** configuração Logback comentada; diagrama fachada → implementação.

### Capítulo 39 — Fundamentos de testes automatizados
*O que torna um teste valioso e como escrever testes unitários que protegem de verdade.*
1. Por que testar; os quatro pilares de um bom teste (Khorikov)
2. Pirâmide de testes × *Testing Trophy* × *Honeycomb*
3. *Test doubles*: Dummy, Stub, Spy, Mock e Fake
4. Escola clássica (Detroit) × escola de Londres (mockista)
5. Testes unitários com JUnit 5 (e TestNG como alternativa), AssertJ e Mockito (*strict stubs*); `Clock` fixo; testes parametrizados
6. TDD: ciclo red-green-refactor e quando ajuda
7. *Shift-left* × *shift-right* (prévia da Parte XVIII)

**Destaques práticos:** suíte unitária do FinTrack Core; comparação lado a lado de testes no estilo clássico e mockista.

---

## PARTE VII — BANCOS DE DADOS RELACIONAIS E ACESSO A DADOS

*Correspondência no `roadmap.sh/java`: Database Access (JDBC, JDBI3). Modelagem, SQL e transações vêm antes do ORM porque ele é construído sobre eles.*

### Capítulo 40 — Modelagem de dados relacional
*Do problema de negócio ao esquema físico, com decisões justificadas.*
1. Modelos conceitual, lógico e físico
2. Entidades, atributos, relacionamentos e cardinalidades — DER de Cliente, Pedido, ItemPedido e Produto
3. Normalização (1FN, 2FN, 3FN, FNBC) com exemplos de anomalias
4. Desnormalização consciente
5. Chaves naturais × substitutas; sequência × UUID (v4 × v7) — comparação
6. Integridade: constraints, chaves estrangeiras e `CHECK`; modelagem de dinheiro e datas
7. Padrões de modelagem: herança em tabelas (*single table*, *joined*, *table per class*), *soft delete*, auditoria e multi-tenancy (prévia)

**Destaques práticos:** DERs completos com cardinalidades; comparação visual de três modelagens de herança.

### Capítulo 41 — SQL além do CRUD
*As consultas que resolvem no banco o que muitos tentam resolver em laços Java.*
1. Joins e álgebra relacional
2. Agregações, `GROUP BY` e `HAVING`
3. Subqueries e CTEs (incluindo recursivas)
4. Window functions: ranking, totais acumulados e comparação entre linhas
5. *Upsert* (`ON CONFLICT` / `MERGE`) e consultas em `JSONB`

**Destaques práticos:** relatórios do Marketplace Vértice resolvidos em SQL; diagramas de conjuntos dos joins.

### Capítulo 42 — Acesso a dados em Java: JDBC, pool de conexões e JDBI
*A camada sobre a qual todo ORM é construído.*
1. Arquitetura JDBC: `Driver`, `Connection`, `Statement` e `ResultSet`
2. `PreparedStatement` e prevenção de SQL injection
3. Transações em JDBC: `autoCommit`, `commit` e `rollback`
4. Pool de conexões: por que existe; HikariCP em seu uso básico
5. Mapeamento manual de linhas para objetos
6. JDBI3 como camada leve; comparação com JDBC puro (prévia de `JdbcClient` no Capítulo 57 e de JPA no Capítulo 55)

**Destaques práticos:** repositório JDBC completo; diagrama de sequência da obtenção de conexão no pool.

### Capítulo 43 — Transações e ACID em profundidade
*O que uma transação garante, onde as garantias terminam e como bancos diferentes as implementam.*
1. O que é uma transação e as quatro propriedades ACID
2. Anomalias: *dirty read*, *non-repeatable read*, *phantom read*, *lost update* e *write skew*
3. Níveis de isolamento (`READ UNCOMMITTED`, `READ COMMITTED`, `REPEATABLE READ`, `SERIALIZABLE`): o padrão SQL × a implementação real
4. MVCC × bloqueio em duas fases; PostgreSQL × SQL Server (RCSI e Snapshot Isolation)
5. **Projeto 10.01: `AcidVaultTransfer`** — motor bancário que prova as quatro propriedades sob concorrência pesada e falha simulada entre débito e crédito

**Destaques práticos:** diagramas de linha do tempo de cada anomalia; matriz isolamento × anomalia.

### Capítulo 44 — Migrações versionadas com Flyway e Liquibase
*O schema do banco também é código e precisa de versionamento.*
1. Por que versionar o schema
2. Flyway: convenções, migrações versionadas × repetíveis, *checksum* e *baseline*
3. Liquibase: *changelogs* e *changesets*
4. Flyway × Liquibase — comparação
5. Migrações em pipelines e ambientes (evolução sem downtime no Capítulo 76)

**Destaques práticos:** série de migrations do domínio de pedidos.

---

## PARTE VIII — O ECOSSISTEMA SPRING (MÓDULO DEDICADO)

*Correspondência no `roadmap.sh/java`: Web Frameworks (Spring, Spring Boot) e ORM (JPA, Hibernate, Spring Data JPA). A ordem interna segue o `roadmap.sh/spring-boot`. Projeto progressivo do módulo: a API de Pedidos do Marketplace Vértice, que ganha uma camada nova a cada capítulo.*

> **Seção A — Spring Core** (Capítulos 45 a 49)

### Capítulo 45 — Introdução ao Spring: terminologia, arquitetura e por que Spring
*A abertura do módulo: que problema o Spring resolveu, como ele está organizado e como o restante do módulo será percorrido.*
1. O problema que o Spring resolveu: J2EE/EJB, acoplamento e baixa testabilidade
2. Terminologia: bean, container, contexto, injeção, aspecto, starter e autoconfiguração
3. Arquitetura do Spring Framework: Core Container, AOP, acesso a dados, Web (MVC e WebFlux) e Test
4. O portfólio Spring (Boot, Data, Security, Cloud, Batch, Modulith, AI, Integration) e onde cada projeto aparece no livro
5. Por que Spring? Spring × Jakarta EE × Quarkus × Micronaut × Play × Javalin — comparação
6. Gerações: Spring 5 / Boot 2 (`javax`) → Spring 6 / Boot 3 (Jakarta, Java 17) → Spring 7 / Boot 4
7. Apresentação do projeto progressivo do módulo: a API de Pedidos do Marketplace Vértice

**Destaques práticos:** diagrama dos módulos do framework; mapa do portfólio Spring com remissões aos capítulos.

### Capítulo 46 — Inversão de Controle e Injeção de Dependência
*O princípio que sustenta todo o ecossistema Spring.*
1. O problema do acoplamento: `new` espalhado pelo código e testabilidade comprometida
2. Inversão de Controle: o container assume o ciclo de vida dos objetos
3. Injeção por construtor × setter × campo, e por que preferir o construtor
4. `BeanFactory` × `ApplicationContext`
5. Resolução de dependências: por tipo, `@Qualifier`, `@Primary`, coleções e `Map` de beans
6. Dependências circulares como sintoma de problema de design
7. Um mini-container de DI escrito à mão com reflexão (retomando o Capítulo 15)

**Destaques práticos:** diagramas de classes antes e depois da DI; diagrama de sequência da inicialização do contexto.

### Capítulo 47 — Configuração do container: Java Config, anotações e `Environment`
*As formas de dizer ao Spring o que criar e como.*
1. Evolução: XML → anotações → Java Config
2. `@Configuration`, `@Bean` e o proxy de configuração (`proxyBeanMethods`)
3. *Component scanning* e estereótipos (`@Component`, `@Service`, `@Repository`, `@Controller`)
4. Catálogo das anotações essenciais do Spring
5. `Environment`, *property sources*, `@Value` × `@ConfigurationProperties`
6. Profiles e `@Conditional`
7. SpEL (Spring Expression Language) e quando usá-la

**Destaques práticos:** a mesma configuração escrita em XML, anotações e Java Config.

### Capítulo 48 — Beans: ciclo de vida, escopos e eventos
*O que acontece com um bean do nascimento à destruição.*
1. Ciclo de vida: instanciação, injeção, interfaces `Aware`, `BeanPostProcessor`, `@PostConstruct` e `@PreDestroy`
2. `BeanFactoryPostProcessor` e `BeanDefinition`
3. Escopos: `singleton`, `prototype`, `request`, `session` e `application`; injetar um prototype em um singleton (`ObjectProvider` e *scoped proxies*)
4. Beans singleton e *thread-safety* (retomando a Parte V)
5. Inicialização preguiçosa (*lazy*)
6. Eventos de aplicação: `ApplicationEvent`, `@EventListener`, eventos assíncronos e prévia do `@TransactionalEventListener`

**Destaques práticos:** diagrama de atividades do ciclo de vida completo de um bean.

### Capítulo 49 — Spring AOP e proxies
*Como o Spring adiciona comportamento a métodos sem que o código perceba.*
1. Interesses transversais (*cross-cutting concerns*)
2. Conceitos: *aspect*, *advice*, *join point*, *pointcut* e *weaving*
3. JDK Dynamic Proxy × CGLIB (retomando o Capítulo 15)
4. Escrevendo aspectos com `@Aspect`: `@Before`, `@After` e `@Around`
5. A armadilha da autoinvocação e das chamadas internas
6. Onde o Spring usa AOP: `@Transactional`, `@Cacheable`, `@Async`, `@PreAuthorize` e `@Retryable`
7. Spring AOP × AspectJ completo

**Destaques práticos:** diagramas de sequência de uma chamada via proxy × autoinvocação; aspecto de auditoria completo.

> **Seção B — Spring Boot** (Capítulo 50)

### Capítulo 50 — Spring Boot por dentro: starters, autoconfiguração e servidor embutido
*Como o Boot transforma convenções em aplicações prontas para rodar.*
1. O que o Spring Boot acrescenta ao Spring Framework
2. Starters e gestão de dependências pelo BOM do Spring Boot (retomando o Capítulo 37)
3. Autoconfiguração: `@EnableAutoConfiguration`, condições `@Conditional*` e o relatório de condições
4. Configuração externalizada: ordem de precedência, `application.yml`, profiles e `@ConfigurationProperties` validado
5. Servidor embutido: Tomcat × Jetty × Undertow; threads do servidor e virtual threads
6. Empacotamento: JAR executável e *layered JARs*
7. Criando um starter próprio

**Destaques práticos:** diagrama de sequência do `SpringApplication.run`; starter corporativo de auditoria.

> **Seção C — Web: Spring MVC, clientes HTTP e WebFlux** (Capítulos 51 a 54)

### Capítulo 51 — Spring MVC por dentro: Servlet, arquitetura e componentes
*O caminho de uma requisição HTTP até o seu método e de volta.*
1. A Servlet API: `Servlet`, `Filter`, ciclo de vida e o container (Tomcat)
2. Arquitetura do Spring MVC: o padrão *Front Controller* e o `DispatcherServlet`
3. Componentes: `HandlerMapping`, `HandlerAdapter`, `HandlerMethodArgumentResolver`, `HttpMessageConverter`, `ViewResolver` e `HandlerExceptionResolver`
4. Filtros × interceptors × aspectos: onde colocar cada lógica
5. Renderização no servidor: JSP (legado, com limitações no JAR executável) × Thymeleaf
6. Modelo de threads: *thread-per-request* e virtual threads

**Destaques práticos:** diagrama de sequência completo de uma requisição; diagrama de componentes do Spring MVC.

### Capítulo 52 — APIs REST com Spring MVC
*Projetar e implementar APIs previsíveis, evolutivas e seguras para retentativas.*
1. Princípios REST, recursos, representações e modelo de maturidade de Richardson, com o essencial de HTTP (métodos, status e cabeçalhos; aprofundado no Capítulo 71)
2. `@RestController`, mapeamentos, `ResponseEntity` e negociação de conteúdo
3. Bean Validation e validação de regras de domínio
4. Erros padronizados com `ProblemDetail` (RFC 9457) e `@ControllerAdvice`
5. Paginação *offset* × cursor/*keyset* e seus custos
6. `Idempotency-Key`, `ETag`/`If-Match` (concorrência otimista na API) e cache
7. Versionamento; OpenAPI com springdoc; *contract-first* × *code-first*
8. DTOs × entidades na API e mapeamento (MapStruct)

**Destaques práticos:** API de Pedidos do projeto progressivo; diagrama de sequência de uma retentativa com `Idempotency-Key`.

### Capítulo 53 — Consumindo APIs: clientes HTTP no Spring
*Integrar com outros sistemas sem herdar a instabilidade deles.*
1. `RestTemplate` (em modo de manutenção) e por que ainda aparece em legados
2. `WebClient` (reativo)
3. `RestClient`: API fluente e síncrona moderna
4. HTTP Interfaces declarativas (`@HttpExchange`)
5. Spring Cloud OpenFeign
6. Timeouts, pool de conexões, tratamento de erros e observabilidade em clientes
7. Comparação e critérios de escolha

**Destaques práticos:** o mesmo cliente implementado nas cinco abordagens; testes com WireMock.

### Capítulo 54 — Spring WebFlux e programação reativa
*O modelo não bloqueante, seus ganhos e seus custos.*
1. O modelo reativo: Reactive Streams, `Publisher`/`Subscriber` e *backpressure*
2. Project Reactor: `Mono` e `Flux`, operadores e *schedulers*
3. WebFlux: controllers anotados × rotas funcionais; Netty
4. Acesso a dados reativo (R2DBC) e seus limites
5. Depuração e testes (`StepVerifier`)
6. Spring MVC com virtual threads × WebFlux — comparação e critérios

**Destaques práticos:** diagrama de *event loop*; o mesmo endpoint implementado em MVC e em WebFlux.

> **Seção D — Persistência: Hibernate e Spring Data** (Capítulos 55 a 58)

### Capítulo 55 — JPA e Hibernate: entidades, relacionamentos e ciclo de vida
*O que o ORM faz com suas entidades e por que ele surpreende.*
1. *Impedance mismatch*; JPA × Hibernate × Spring Data JPA
2. Mapeamento de entidades: `@Entity`, `@Id`, estratégias de geração de chave (e o impacto de `IDENTITY`), tipos e conversores
3. Relacionamentos: `@OneToMany`, `@ManyToOne`, `@ManyToMany` e `@OneToOne`; lado dono e bidirecionalidade
4. `LAZY` × `EAGER`, `cascade` e `orphanRemoval`
5. *Persistence context* e ciclo de vida da entidade (*transient*, *managed*, *detached*, *removed*); *dirty checking* e *flush*
6. Herança no JPA (retomando o Capítulo 40)
7. `equals`/`hashCode` em entidades (retomando o Capítulo 13)

**Destaques práticos:** diagrama de estados da entidade; DER × diagrama de classes do domínio de pedidos.

### Capítulo 56 — Gerenciamento de transações no Spring
*O `@Transactional` explicado de ponta a ponta, incluindo as armadilhas.*
1. `PlatformTransactionManager` e a abstração de transações
2. `@Transactional` via proxy: o que acontece em cada chamada
3. Propagação (`REQUIRED`, `REQUIRES_NEW`, `NESTED` e demais) e isolamento
4. Regras de rollback (exceções *checked* × *unchecked*)
5. `readOnly`, timeouts e autoinvocação
6. Transações programáticas com `TransactionTemplate`
7. `open-in-view`: por que desligar
8. `@TransactionalEventListener` e efeitos colaterais após o commit

**Destaques práticos:** diagramas de sequência de cada tipo de propagação; armadilhas implementadas de forma incorreta e correta.

### Capítulo 57 — Spring Data: JPA, JDBC e MongoDB
*Repositórios declarativos e a escolha do modelo de persistência certo.*
1. A abstração de repositórios: `Repository`, `CrudRepository`, `ListCrudRepository` e `JpaRepository`
2. Consultas derivadas, `@Query` (JPQL e nativa), paginação e ordenação
3. Projeções (interfaces, DTOs e records) e prévia de Specifications (Capítulo 94)
4. Auditoria (`@CreatedDate`, `@LastModifiedBy`)
5. Spring JDBC: `JdbcTemplate` e `JdbcClient`
6. Spring Data JDBC: modelo orientado a aggregates, sem *lazy loading*
7. Spring Data MongoDB: documentos, mapeamento e consultas
8. Quando usar cada um

**Destaques práticos:** o mesmo repositório implementado em JPA, JDBC e MongoDB.

### Capítulo 58 — Desempenho em persistência com Spring
*Eliminar N+1, dimensionar conexões e saber quando sair do ORM.*
1. O problema N+1: detecção por logs, estatísticas do Hibernate e testes
2. `JOIN FETCH`, `@EntityGraph` e *batch fetching*
3. Projeções para leitura
4. *Batch inserts* e *updates* (e por que `IDENTITY` impede batching)
5. HikariCP: dimensionamento (a fórmula como ponto de partida) e métricas do pool
6. Cache de segundo nível do Hibernate: quando ajuda e quando atrapalha
7. Alternativas: jOOQ, MyBatis e EBean — comparação

**Destaques práticos:** a mesma consulta em várias abordagens com o SQL gerado comparado.

> **Seção E — Spring Security** (Capítulos 59 e 60)

### Capítulo 59 — Spring Security I: arquitetura, autenticação e autorização
*A cadeia de filtros e como configurá-la sem copiar e colar.*
1. Autenticação × autorização
2. Arquitetura: `DelegatingFilterProxy`, `FilterChainProxy` e `SecurityFilterChain`
3. `AuthenticationManager`, `AuthenticationProvider`, `UserDetailsService` e `PasswordEncoder`
4. Autenticação por formulário, HTTP Basic e sessão; o `SecurityContext`
5. Autorização por URL e por método (`@PreAuthorize`)
6. CSRF, CORS e cabeçalhos de segurança
7. Testes com Spring Security Test

**Destaques práticos:** diagrama da cadeia de filtros; configuração completa comentada.

### Capítulo 60 — Spring Security II: JWT, OAuth 2.0 e OpenID Connect
*Autenticação sem estado, delegação de acesso e identidade federada.*
1. Sessão com estado × token sem estado; tokens opacos × JWT
2. Anatomia do JWT (JWS e JWE), validação correta e armadilhas (`alg: none`, chave fraca, ausência de expiração, armazenamento no navegador)
3. OAuth 2.0: papéis e fluxos (*Authorization Code* + PKCE, *Client Credentials*, *Device Flow*), *refresh token rotation*, revogação de tokens e OAuth 2.1
4. OpenID Connect: ID Token, *userinfo*, *discovery* e JWKS
5. Spring como Resource Server, OAuth2 Client/Login e Spring Authorization Server
6. Integração com Keycloak; Keycloak × Auth0 × Okta × Cognito

**Destaques práticos:** diagramas de sequência de cada fluxo; Keycloak via Docker Compose protegendo a API de Pedidos.

> **Seção F — Tarefas assíncronas e processamento em lote** (Capítulo 61)

### Capítulo 61 — Execução assíncrona, agendamento e processamento em lote
*Tarefas que não cabem no ciclo de uma requisição.*
1. `@Async` e configuração de executores (incluindo virtual threads)
2. `@Scheduled`: cron, `fixedRate` × `fixedDelay` e o problema de múltiplas réplicas (prévia do ShedLock no Capítulo 105)
3. Quartz: jobs persistentes e execução em cluster
4. Spring Batch: `Job`, `Step`, processamento em *chunks*, `ItemReader`/`ItemProcessor`/`ItemWriter`, *restart* e *skip*
5. Alternativas: JobRunr e `CronJob` do Kubernetes
6. Comparação e critérios de escolha

**Destaques práticos:** job Spring Batch de importação de arquivo; diagrama de atividades do processamento em chunks.

> **Seção G — Microsserviços com Spring Cloud** (Capítulos 62 e 63)

### Capítulo 62 — Microsserviços com Spring Cloud I: configuração, descoberta e gateway
*As peças de infraestrutura que o Spring Cloud oferece para sistemas distribuídos.*
1. Visão rápida de microsserviços e quando o Spring Cloud entra em cena (estilos arquiteturais aprofundados na Parte XIII)
2. Spring Cloud Config: configuração centralizada e atualização em tempo de execução
3. Descoberta de serviços: Eureka × DNS do Kubernetes × Consul
4. Spring Cloud LoadBalancer (balanceamento no cliente)
5. Spring Cloud Gateway: rotas, predicados e filtros
6. O que o Kubernetes já resolve e torna dispensável

**Destaques práticos:** diagrama de containers de um sistema com Config, Discovery e Gateway.

### Capítulo 63 — Microsserviços com Spring Cloud II: comunicação, resiliência e rastreamento
*Fazer serviços conversarem sem que a falha de um derrube todos.*
1. OpenFeign na comunicação entre serviços
2. Spring Cloud Circuit Breaker com Resilience4j (e por que o Hystrix ficou para trás)
3. Rastreamento distribuído: Sleuth (legado) → Micrometer Tracing + OpenTelemetry
4. Spring Cloud Stream: abstração de mensageria (prévia da Parte XV)
5. Riscos: chamadas em cascata e o monólito distribuído

**Destaques práticos:** diagrama de sequência com circuit breaker; trace propagado entre dois serviços.

> **Seção H — Testes e produção** (Capítulos 64 e 65)

### Capítulo 64 — Testes no Spring
*Testar com o container e dependências reais sem tornar a suíte lenta e frágil.*
1. Spring TestContext Framework e cache de contexto
2. `@SpringBootTest` e seus modos de `webEnvironment`
3. Slice tests: `@WebMvcTest` com MockMvc, `@DataJpaTest`, `@JsonTest` e `@RestClientTest`
4. `@MockitoBean` e `@MockitoSpyBean` (substitutos de `@MockBean` e `@SpyBean`)
5. Testcontainers e `@ServiceConnection`; por que H2 engana
6. WireMock, Awaitility e REST Assured
7. Organização no build: `surefire` × `failsafe`

**Destaques práticos:** pirâmide de testes aplicada à API de Pedidos; diagrama do ambiente de teste.

### Capítulo 65 — Spring Boot em produção
*O que muda quando a aplicação sai do notebook.*
1. Actuator: endpoints, *health groups* e proteção dos endpoints
2. Métricas com Micrometer (prévia da Parte XX)
3. *Graceful shutdown* e ciclo de vida em containers
4. Virtual threads no Spring Boot
5. Spring AOT, GraalVM Native Image e CDS: *startup* × throughput
6. Empacotamento com Buildpacks e imagens OCI (prévia do Capítulo 138)
7. Estratégia de atualização de versões e OpenRewrite (detalhes no Apêndice E)

**Destaques práticos:** comparação de startup e memória entre JVM e binário nativo da API de Pedidos.

---

# VOLUME 3 — INFRAESTRUTURA, DADOS AVANÇADOS, SEGURANÇA, DESIGN E ARQUITETURA DE APLICAÇÕES

## PARTE IX — ENGENHARIA COLABORATIVA E FUNDAMENTOS DE INFRAESTRUTURA

*Início da continuação pelo `roadmap.sh/backend`: controle de versão, sistema operacional, redes, protocolos web e containers.*

### Capítulo 66 — Git por dentro
*Como o Git armazena e relaciona informações, e como isso explica o comportamento de cada comando.*
1. Controle de versão centralizado × distribuído
2. O modelo de objetos: *blobs*, *trees*, *commits* e *tags* endereçados por hash; o DAG de commits
3. Refs, `HEAD`, branches como ponteiros e a *staging area*
4. `merge` *fast-forward* × *three-way* × `rebase`; a regra de ouro do rebase em branches compartilhadas
5. Comandos cirúrgicos: `rebase -i` (*squash, fixup, reword, drop*), `cherry-pick`, `revert` × `reset`, `stash`, `reflog`, `bisect` (busca binária em O(log n)) e `worktree`
6. Break-It Lab: "perder" commits com `reset --hard` e recuperá-los com `reflog`

**Destaques práticos:** diagramas do grafo de objetos antes e depois de merge e rebase; exploração da pasta `.git` com `git cat-file`.

### Capítulo 67 — Git em equipe: fluxos, governança e code review
*Como times de alta performance organizam branches, versões e revisões de código.*
1. Trunk-Based Development + *Feature Flags* × GitHub Flow × GitFlow — comparação por tamanho de time, cadência de release e risco
2. Conventional Commits e Semantic Versioning (`MAJOR.MINOR.PATCH`)
3. Git Hooks, `CODEOWNERS` e *Branch Protection Rulesets*
4. Pull Requests coesos e code review técnico e construtivo
5. Métricas de fluxo: *lead time*, tamanho de PR e métricas DORA
6. **Projeto: `RepoGuard CLI`** — auditoria de repositórios via GitHub API, validação de Conventional Commits, métricas de PR, `CHANGELOG.md` SemVer automático e instalação padronizada de hooks

**Destaques práticos:** fluxogramas comparativos das três estratégias de branching; código Java do CLI.

### Capítulo 68 — Linux para desenvolvedores back-end
*O sistema operacional onde quase todo back-end roda, do ponto de vista de quem precisa diagnosticá-lo em produção.*
1. Kernel, *user space* e chamadas de sistema
2. Processos, threads e sinais (`SIGTERM` × `SIGKILL`) e sua relação com *graceful shutdown*
3. Usuários, grupos e permissões POSIX
4. *File descriptors* e `ulimit` ("Too many open files")
5. Memória virtual, RSS, *page cache*, swap e OOM Killer
6. Caixa de ferramentas de diagnóstico: `ps`, `htop`, `lsof`, `ss`, `dig`, `curl -v`, `jq`, `journalctl`, `vmstat`, `iostat`, `strace`
7. Break-It Lab: esgotar file descriptors de uma aplicação Java e diagnosticar

**Destaques práticos:** diagrama de ciclo de vida de processo e sinais; roteiro de investigação de incidente.

### Capítulo 69 — Redes de computadores para quem escreve software
*Os conceitos de rede que explicam latências, timeouts e falhas de conexão em sistemas reais.*
1. Modelo OSI × modelo TCP/IP
2. Endereçamento IP, portas, NAT e sub-redes (CIDR) — base para entender VPCs
3. TCP: *3-way handshake*, controle de fluxo e de congestionamento, `TIME_WAIT`, *keep-alive*; UDP e quando usá-lo
4. DNS: resolução recursiva, registros A, AAAA, CNAME, TXT, SRV e MX, TTL, cache e propagação
5. Ordens de grandeza de latência que todo engenheiro deve conhecer

**Destaques práticos:** diagramas de sequência do handshake TCP e da resolução DNS; laboratório com `dig` e `ss`.

### Capítulo 70 — Segurança de transporte: TLS 1.3, certificados e mTLS
*Como a comunicação é protegida em trânsito e por que certificados vencidos derrubam sistemas inteiros.*
1. O que TLS garante: confidencialidade, integridade e autenticidade
2. Handshake TLS 1.3 × TLS 1.2
3. Certificados X.509, cadeias de confiança, CAs, revogação (OCSP/CRL) e ACME/Let's Encrypt
4. mTLS: autenticação mútua entre serviços
5. TLS em Java: *keystores*, *truststores* e erros clássicos (`PKIX path building failed`)

**Destaques práticos:** diagrama de sequência do handshake; configuração de mTLS entre dois serviços Spring Boot.

### Capítulo 71 — Protocolos HTTP e a borda da aplicação
*A evolução do HTTP e os componentes que ficam entre o cliente e sua aplicação.*
1. Semântica HTTP: métodos, status, cabeçalhos e cache HTTP
2. HTTP/1.1 e o *head-of-line blocking*
3. HTTP/2: multiplexação binária, *streams* e HPACK
4. HTTP/3 e QUIC sobre UDP
5. Comparação HTTP/1.1 × HTTP/2 × HTTP/3
6. Proxy reverso (NGINX × Envoy × HAProxy) e balanceamento L4 × L7; algoritmos de balanceamento
7. CORS e requisições *preflight*
8. **Projeto: `CertWatch & NetProbe`** — Micro-SaaS que audita validade de certificados, propagação DNS, suporte a HTTP/2 e latência TCP, com alertas preventivos

**Destaques práticos:** diagrama de multiplexação HTTP/2 × conexões HTTP/1.1; diagrama C4 do projeto.

### Capítulo 72 — Containers com Docker: fundamentos
*O que é um container de verdade e como usá-lo para ambientes locais reproduzíveis.*
1. Máquinas virtuais × containers; *namespaces* e *cgroups*
2. Imagens, camadas, registries e o padrão OCI
3. Dockerfile: instruções e cache de camadas
4. Redes e volumes
5. Docker Compose para ambientes locais (PostgreSQL, Redis, RabbitMQ, Kafka)
6. Alternativas: Podman, containerd e Buildah

**Destaques práticos:** `docker-compose.yml` base do laboratório do livro; diagrama de camadas de imagem.

---

## PARTE X — BANCOS DE DADOS EM PROFUNDIDADE

### Capítulo 73 — PostgreSQL por dentro
*Como o PostgreSQL armazena, versiona e recupera dados.*
1. Arquitetura de processos e *shared buffers*
2. Armazenamento: páginas de 8 KB, tuplas e TOAST
3. WAL, checkpoints, durabilidade e replicação baseada em WAL
4. MVCC (`xmin`/`xmax`), *dead tuples*, `VACUUM`, `AUTOVACUUM`, *bloat* e *wraparound*
5. Configurações essenciais

**Destaques práticos:** diagrama de layout de página; laboratório observando versões de tuplas.

### Capítulo 74 — Índices e planos de execução
*Por que uma consulta leva 2 ms ou 20 segundos.*
1. Como índices funcionam; B-Tree
2. Hash, GIN (`JSONB` e busca textual), GiST e BRIN — comparação
3. Índices compostos (ordem das colunas), parciais, *covering* (`INCLUDE`) e de expressão
4. `EXPLAIN (ANALYZE, BUFFERS)`: *seq scan*, *index scan*, *bitmap scan*; *nested loop*, *hash join* e *merge join*
5. Estatísticas e o *planner*
6. Particionamento de tabelas (range, list, hash)
7. Anti-patterns: índices demais, função sobre coluna indexada, `LIKE '%termo'`

**Destaques práticos:** diagrama de árvore B-Tree; leitura comentada de planos antes e depois de indexar.

### Capítulo 75 — Concorrência no banco de dados
*Impedir saques duplicados e atualizações perdidas.*
1. *Lost update* em aplicações web
2. *Optimistic locking* com `@Version`
3. *Pessimistic locking*: `SELECT ... FOR UPDATE`, `NOWAIT` e `SKIP LOCKED` (filas no banco)
4. Otimista × pessimista: critérios de escolha
5. *Advisory locks* e constraints como última linha de defesa
6. **Projeto: `SplitPay Ledger`** — carteira digital e split de pagamentos com partidas dobradas, Flyway e proteção contra saques concorrentes

**Destaques práticos:** diagramas de sequência de duas transações concorrentes em cada estratégia; DER do ledger.

### Capítulo 76 — Evolução de schema sem downtime
*Mudar o banco com a aplicação no ar.*
1. Por que migrations quebram sistemas em produção
2. O padrão *Expand & Contract*
3. Operações perigosas: locks em `ALTER TABLE`, `CREATE INDEX CONCURRENTLY` e *backfill* em lotes
4. Compatibilidade entre código V1 e banco V2 durante deploys graduais
5. Estratégias de rollback de schema

**Destaques práticos:** fluxograma das fases do Expand & Contract; renomeação de coluna sem downtime passo a passo.

### Capítulo 77 — Panorama de bancos de dados: relacionais e NoSQL
*Escolher armazenamento pelo padrão de acesso, não pela moda.*
1. PostgreSQL × SQL Server × MySQL × Oracle
2. Famílias NoSQL: documento (MongoDB), chave-valor (DynamoDB, Redis), colunar larga (Cassandra), grafos (Neo4j) e séries temporais
3. Persistência poliglota
4. Critérios de decisão e erros comuns

**Destaques práticos:** o mesmo domínio modelado em relacional, documento e chave-valor; matriz de decisão.

---

## PARTE XI — SEGURANÇA DE APLICAÇÕES

*Autenticação, JWT, OAuth 2.0 e OpenID Connect foram tratados com o Spring Security nos Capítulos 59 e 60; esta Parte cobre criptografia, vulnerabilidades e autorização avançada.*

### Capítulo 78 — Criptografia prática para desenvolvedores
*Usar criptografia corretamente sem precisar inventá-la.*
1. Hash criptográfico × hash de senha: Argon2id, BCrypt, scrypt e PBKDF2
2. Integridade e autenticidade com HMAC-SHA256
3. Criptografia simétrica: AES-256-GCM, nonces e modos de operação
4. Criptografia assimétrica e assinaturas: RSA × curvas elípticas (Ed25519)
5. Gestão de chaves: KMS, *envelope encryption* e rotação
6. Erros clássicos: ECB, IV reutilizado, chaves no código

**Destaques práticos:** diagrama de envelope encryption; implementações incorreta × correta em Java.

### Capítulo 79 — OWASP: vulnerabilidades de aplicações web e de APIs
*As falhas que mais causam incidentes e como preveni-las no código.*
1. OWASP Top 10 (edição 2025) e OWASP API Security Top 10 (2023): diferenças e sobreposições
2. BOLA/IDOR e autorização em nível de objeto
3. *Mass assignment*
4. SSRF
5. Injeção (SQL, comandos, LDAP) e *path traversal*
6. Configuração insegura, componentes vulneráveis e falhas de log

**Destaques práticos:** ataque e correção de cada vulnerabilidade em uma API Spring; diagrama de fluxo de um SSRF.

### Capítulo 80 — Autorização, multi-tenancy e privacidade (LGPD)
*Quem pode fazer o quê, em qual tenant, com quais dados pessoais.*
1. RBAC × ABAC × ReBAC — comparação
2. Estratégias de multi-tenancy: banco por tenant, schema por tenant e linha por tenant (incluindo Row-Level Security)
3. API Keys: geração, armazenamento com hash SHA-256 e escopos
4. LGPD para engenheiros: dados pessoais, minimização, *field-level encryption* e direito de eliminação
5. Trilha de auditoria imutável
6. **Projeto: `TenantVault IAM`** — organizações multi-tenant, convites, RBAC/ABAC, API keys com escopo, SSO via Keycloak e auditoria LGPD

**Destaques práticos:** comparação visual das três estratégias de tenancy; DER do TenantVault.

---

## PARTE XII — DESIGN DE CÓDIGO: CLEAN CODE, PRINCÍPIOS E PADRÕES GoF

### Capítulo 81 — Clean Code e refatoração
*Código é lido muito mais vezes do que é escrito.*
1. Nomes, funções e níveis de abstração
2. Comentários úteis × comentários que mentem
3. Tratamento de erros limpo
4. *Code smells* (catálogo de Fowler)
5. Refatoração segura com testes: técnicas fundamentais
6. Code review orientado a design

**Destaques práticos:** refatoração passo a passo de um serviço legado de 300 linhas.

### Capítulo 82 — SOLID em profundidade
*Cada princípio com o problema que resolve, a violação típica e a correção.*
1. SRP — Responsabilidade Única
2. OCP — Aberto/Fechado
3. LSP — Substituição de Liskov
4. ISP — Segregação de Interfaces
5. DIP — Inversão de Dependência
6. Quando aplicar SOLID vira *overengineering*

**Destaques práticos:** diagramas de classes antes/depois para cada princípio.

### Capítulo 83 — Princípios complementares de design
*O vocabulário que orienta decisões de design no dia a dia.*
1. GRASP (Information Expert, Creator, Controller, Low Coupling, High Cohesion, Polymorphism, Pure Fabrication, Indirection, Protected Variations)
2. DRY, KISS e YAGNI — e seus limites
3. Tell, Don't Ask e Lei de Demeter
4. Composição sobre herança
5. Coesão e acoplamento; métricas de acoplamento aferente e eferente e instabilidade

**Destaques práticos:** exemplos de violação e correção; diagrama de dependências com métricas.

### Capítulo 84 — Introdução aos Design Patterns
*O que é um padrão, como ler um catálogo e quando não usar.*
1. Origem: Christopher Alexander e o GoF
2. Anatomia de um padrão: intenção, problema, estrutura, participantes e consequências
3. Classificação: criacionais, estruturais e comportamentais
4. Padrões em Java moderno: lambdas, records e sealed como substitutos parciais
5. Padrões no Spring: onde eles já estão
6. Organização do repositório `java-design-patterns-realworld` (um módulo testado por padrão)

**Destaques práticos:** mapa visual dos 23 padrões e suas relações.

> **Estrutura de cada padrão nos Capítulos 85 a 88:** intenção; problema motivador; diagrama UML da estrutura; implementação ingênua sem o padrão; implementação com o padrão; variação idiomática em Java 21+/Spring; testes; quando NÃO usar; padrões relacionados; mini-projeto exclusivo.

### Capítulo 85 — Padrões criacionais
1. **Singleton** — instância única *thread-safe* (e por que o container do Spring geralmente substitui o padrão). **Projeto 09.01: `FeatureToggleRegistry`** — feature flags com recarga atômica sem reiniciar a API
2. **Factory Method** — criação delegada a subclasses ou métodos fábrica. **Projeto 09.02: `MultiBankSlipGenerator`** — boletos e QR Codes Pix por código FEBRABAN
3. **Abstract Factory** — famílias de objetos compatíveis. **Projeto 09.03: `GlobalInvoiceSuite`** — faturamento por país (BR: CPF/CNPJ, ICMS/ISS, NF-e; US: EIN, Sales Tax, Invoice PDF)
4. **Builder** — construção passo a passo de objetos imutáveis (*Staged Builder* + `record`). **Projeto 09.04: `LoanContractBuilder`** — contratos de crédito com avalistas, garantias, carência e indexadores
5. **Prototype** — clonagem profunda de objetos custosos. **Projeto 09.05: `InsurancePolicyCloner`** — cotações de seguro a partir de matrizes de cobertura

### Capítulo 86 — Padrões estruturais
1. **Adapter** — **Projeto 09.06: `LegacyBiometricsAdapter`** — domínio REST/JSON conectado a biometria legada SOAP/XML
2. **Bridge** — M + N classes em vez de M × N. **Projeto 09.07: `OmniReportBridge`** — tipos de relatório × motores de renderização (PDF, XLSX, HTML, CSV)
3. **Composite** — **Projeto 09.08: `KitAndComboPricingTree`** — produtos simples e kits aninhados sob o mesmo contrato
4. **Decorator** — **Projeto 09.09: `DynamicTariffDecorator`** — valor base → spread → IOF → seguro → desconto VIP
5. **Facade** — **Projeto 09.10: `DigitalOnboardingFacade`** — credenciamento de lojista em um único endpoint
6. **Flyweight** — **Projeto 09.11: `SkuTaxFlyweightEngine`** — 2 milhões de itens compartilhando regras NCM/CEST imutáveis
7. **Proxy** — base do Spring AOP. **Projeto 09.12: `CreditScoreSmartProxy`** — controle de permissão, mascaramento LGPD e cache para consultas pagas ao bureau

### Capítulo 87 — Padrões comportamentais I
1. **Chain of Responsibility** — **Projeto 09.13: `CardAntifraudChain`** — saldo → horário → distância → frequência
2. **Command** — **Projeto 09.14: `AuditedBankCommandBus`** — `AgendarPix`, `BloquearCartao`, `AlterarLimite` com auditoria e reversão
3. **Interpreter** — **Projeto 09.15: `EligibilityRuleDSL`** — `(RENDA > 5000 AND SCORE >= 700) OR CLIENTE_VIP` avaliado sem deploy (inclui noções de gramática, *tokenizer* e AST)
4. **Iterator** — **Projeto 09.16: `CloudStatementLazyIterator`** — milhões de linhas paginadas sob demanda
5. **Mediator** — **Projeto 09.17: `ControlTowerChatMediator`** — bot, atendente, supervisor e auditoria coordenados
6. **Memento** — **Projeto 09.18: `ContractDraftTimeMachine`** — snapshots imutáveis de minutas e *rollback*

### Capítulo 88 — Padrões comportamentais II
1. **Observer** — **Projeto 09.19: `InvoicePaidEventHub`** — `@TransactionalEventListener` liberando licença, comissão e recibo
2. **State** — **Projeto 09.20: `ClaimLifecycleStateMachine`** — sinistro `ABERTO → EM_VISTORIA → APROVADO → INDENIZADO / NEGADO` com transições ilegais impossíveis
3. **Strategy** — **Projeto 09.21: `SmartCommissionStrategy`** — estratégias injetadas via `Map<String, Strategy>`
4. **Template Method** — **Projeto 09.22: `UniversalBankReconciler`** — esqueleto comum para OFX, CNAB 240 e CSV
5. **Visitor** — com `sealed interface` + pattern matching. **Projeto 09.23: `RegulatoryTaxVisitor`** — IR e relatório regulatório sobre carteira heterogênea (`RendaFixa`, `Acao`, `FundoImobiliario`, `Cripto`) com exaustividade verificada pelo compilador

### Capítulo 89 — Padrões em perspectiva: comparações, combinações e anti-patterns
*Os padrões se parecem; as intenções não.*
1. Strategy × State × Template Method
2. Decorator × Proxy × Adapter × Facade
3. Factory Method × Abstract Factory × Builder
4. Observer × Mediator; Command × Strategy
5. Combinações frequentes em sistemas reais
6. Anti-patterns: *pattern fever*, Singleton como variável global, *God Object*, *Service Locator*

**Destaques práticos:** diagramas lado a lado das estruturas semelhantes; tabela intenção × estrutura.

---

## PARTE XIII — ARQUITETURA DE APLICAÇÕES E DOMÍNIO

### Capítulo 90 — Fundamentos de arquitetura de software
*O que é arquitetura, quais decisões ela envolve e como raciocinar sobre trade-offs.*
1. Definições de arquitetura e decisões "difíceis de mudar"
2. Atributos de qualidade (características arquiteturais)
3. Trade-offs: não existe melhor arquitetura, existe a menos pior para o contexto
4. Acoplamento estático e dinâmico; *quanta* arquiteturais
5. Arquitetura evolutiva e *fitness functions*

**Destaques práticos:** exercício de identificação de características arquiteturais a partir de requisitos do Banco Aurora.

### Capítulo 91 — Estilos arquiteturais comparados
*Monólito, microsserviços e o espectro entre eles.*
1. Arquitetura em camadas
2. Monólito tradicional e monólito modular
3. SOA e microsserviços: princípios, benefícios e custos reais
4. Arquitetura orientada a eventos
5. Serverless
6. Comparação por escalabilidade, implantação, consistência, custo operacional e maturidade do time
7. O monólito distribuído e outros anti-patterns de decomposição

**Destaques práticos:** o mesmo sistema desenhado em cada estilo (diagramas C4 de containers); matriz comparativa.

### Capítulo 92 — DDD estratégico
*Dividir sistemas complexos pelas fronteiras do negócio.*
1. Domínio, subdomínios (*Core*, *Supporting*, *Generic*) e onde investir
2. Linguagem ubíqua
3. *Bounded Contexts*
4. *Context Mapping*: Shared Kernel, Customer-Supplier, Conformist, Anti-Corruption Layer, Open Host Service e Published Language
5. **Anti-Corruption Layer — Projeto 10.11: `LegacyErpShieldACL`** — logística moderna protegida de um ERP legado com tabelas `TB_CLI_99` e códigos mágicos

**Destaques práticos:** mapa de contextos do Marketplace Vértice; diagrama de tradução da ACL.

### Capítulo 93 — Descoberta colaborativa de domínio: Event Storming e Domain Storytelling
*Técnicas para extrair o conhecimento do negócio antes de escrever código.*
1. Event Storming *Big Picture*
2. Event Storming *Process Level*
3. Event Storming *Design Level* (do post-it ao aggregate)
4. Domain Storytelling
5. Facilitação: preparação, condução e armadilhas

**Destaques práticos:** sessão de Event Storming completa do checkout do Marketplace Vértice reproduzida em diagramas.

### Capítulo 94 — DDD tático
*Os blocos de construção de um modelo de domínio rico.*
1. Entidades e identidade
2. Value Objects
3. Aggregates: regras de design, invariantes e fronteiras transacionais
4. Domain Services e Application Services
5. Domain Events
6. Factories
7. **Repository, Unit of Work e Specification — Projeto 10.09: `RealEstateSpecSearch`** — busca de imóveis com dezenas de filtros opcionais via Specifications tipadas
8. Modelo anêmico × modelo rico

**Destaques práticos:** diagramas de classes de aggregates; aggregate grande demais × bem delimitado.

### Capítulo 95 — Arquitetura Hexagonal (Ports & Adapters)
*Isolar o domínio de frameworks, bancos e protocolos.*
1. Origem e motivação (Alistair Cockburn)
2. Portas de entrada e de saída; adaptadores primários e secundários
3. Organização de pacotes e módulos em Java
4. Testabilidade: testando o núcleo sem infraestrutura
5. Custos e quando é exagero

**Destaques práticos:** diagrama hexagonal com código correspondente; regras ArchUnit protegendo as dependências.

### Capítulo 96 — Clean Architecture
*A regra de dependência e suas variações.*
1. Círculos concêntricos e a regra de dependência
2. *Entities*, *Use Cases*, *Interface Adapters* e *Frameworks & Drivers*
3. Clean pragmática em Spring Boot
4. Camadas × Onion × Hexagonal × Clean — comparação
5. Armadilhas: mapeamentos excessivos e cerimônia sem valor

**Destaques práticos:** diagrama comparativo das quatro abordagens; mesmo caso de uso implementado em camadas e em Clean.

### Capítulo 97 — Monólito modular com Spring Modulith
*A modularidade dos microsserviços sem o custo da distribuição.*
1. Por que monólitos modulares; fronteiras de módulo
2. Spring Modulith: módulos, verificação de dependências e eventos entre módulos
3. *Event Publication Registry* e consistência entre módulos
4. Documentação gerada e testes de módulo
5. Evolução para microsserviços quando (e se) necessário

**Destaques práticos:** diagrama de componentes dos módulos; verificação automática de violações.

### Capítulo 98 — Comunicação entre serviços: síncrona × assíncrona
*A escolha que define acoplamento, latência e consistência de um sistema distribuído.*
1. Acoplamento temporal, espacial e de formato
2. Comunicação síncrona: simplicidade, latência acumulada e falhas em cascata
3. Comunicação assíncrona: desacoplamento, consistência eventual e complexidade operacional
4. Orquestração × coreografia (prévia da Parte XVI)
5. Critérios de decisão com cenários de pagamentos, e-commerce e notificações

**Destaques práticos:** diagramas de sequência do mesmo fluxo nos dois modelos; tabela de trade-offs.

### Capítulo 99 — Protocolos de API além do REST: gRPC, GraphQL, SSE e WebSockets
*Escolher o protocolo pelo padrão de comunicação.*
1. gRPC e Protocol Buffers sobre HTTP/2: unary, server streaming, client streaming e bidirecional
2. GraphQL: esquema, resolvers, problema N+1 e quando usar
3. Tempo real: *polling* × *long polling* × SSE × WebSockets
4. Comparação REST × gRPC × GraphQL
5. **Projeto: `MedCore Modulith`** — SaaS clínico em DDD + Hexagonal + Spring Modulith, REST com paginação por cursor, painel em tempo real via SSE/WebSockets e motor de autorização de exames via gRPC

**Destaques práticos:** arquivo `.proto` completo; diagramas de sequência de SSE e WebSocket; C4 do MedCore.

### Capítulo 100 — API Gateway e Backend for Frontend
*A borda da arquitetura sob medida para cada cliente.*
1. API Gateway: roteamento, autenticação, rate limiting e agregação
2. BFF: por que clientes diferentes precisam de APIs diferentes
3. Gateway × BFF × Service Mesh — responsabilidades
4. Spring Cloud Gateway × Kong × soluções gerenciadas
5. **Projeto 10.10: `DualChannelBankingBFF`** — BFFs Mobile e Web agregando conta, cartão e investimentos

**Destaques práticos:** diagrama de containers com os dois BFFs; agregação paralela com virtual threads.

---

# VOLUME 4 — SISTEMAS DISTRIBUÍDOS

## PARTE XIV — CACHE E REDIS

### Capítulo 101 — Fundamentos de caching
*Cache é uma das ferramentas de desempenho mais poderosas — e uma das maiores fontes de inconsistência.*
1. Localidade, *hit ratio* e o custo de um *miss*
2. Estratégias: *cache-aside*, *read-through*, *write-through*, *write-behind* e *refresh-ahead*
3. Invalidação, TTL e consistência
4. Cache local × distribuído; Caffeine como L1
5. Redis × Memcached × Hazelcast × Caffeine — comparação

**Destaques práticos:** diagramas de sequência de cada estratégia; Spring Cache com Caffeine.

### Capítulo 102 — Redis por dentro
*Por que o Redis é tão rápido e como mantê-lo disponível.*
1. Modelo de execução: *event loop*, execução de comandos em thread única e *I/O threads*
2. Persistência: RDB × AOF × híbrido
3. Políticas de *eviction*
4. Replicação, Redis Sentinel × Redis Cluster (16.384 *hash slots*)
5. Licenciamento e ecossistema: Redis × Valkey

**Destaques práticos:** diagrama da topologia Sentinel × Cluster; distribuição de *hash slots*.

### Capítulo 103 — Estruturas de dados do Redis e seus casos de uso
*Cada estrutura resolve um problema específico com eficiência.*
1. Strings, Hashes, Lists e Sets
2. Sorted Sets (ZSET): rankings e filas agendadas
3. Bitmaps
4. HyperLogLog: contagem de únicos em até 12 KB com erro estatístico conhecido
5. Geo
6. Redis Streams (e como se comparam ao Kafka)

**Destaques práticos:** um caso de uso implementado para cada estrutura com Spring Data Redis.

### Capítulo 104 — Cache de alta escala: L1 + L2 e falhas clássicas
*Quando o cache vira o ponto crítico do sistema.*
1. Cache híbrido L1 (Caffeine) + L2 (Redis) e invalidação entre instâncias
2. *Cache stampede*: locks, *request coalescing* e expiração probabilística
3. *Cache penetration* e Bloom Filters
4. *Cache avalanche* e TTL com *jitter*
5. *Hot keys* e *big keys*

**Destaques práticos:** diagramas de cada falha e de sua mitigação; implementação do cache híbrido.

### Capítulo 105 — Coordenação distribuída: locks, rate limiting e eleição de líder
*Exclusão mútua e controle de taxa quando há dezenas de réplicas.*
1. Locks distribuídos com Redisson e *watchdog*
2. A controvérsia do Redlock e *fencing tokens*
3. Algoritmos de rate limiting: *token bucket*, *leaky bucket*, janela fixa e janela deslizante
4. Rate limiting atômico com Lua scripts
5. **Distributed Lock & Leader Election — Projeto 10.18: `ClusterBillingLeader`** — fechamento mensal com 4 réplicas e um único líder, com *failover*
6. Eleição de líder com Redis × ZooKeeper/etcd × banco de dados (ShedLock) × Kubernetes Lease — comparação
7. **Projeto: `FlashDrop & ShieldGate`** — vendas relâmpago com fila justa em ZSET, bloqueio de bots via Bloom Filter + rate limit em Lua e reserva atômica de estoque sem *overselling*

**Destaques práticos:** diagrama de sequência mostrando um lock expirado sem fencing token; script Lua comentado; C4 do FlashDrop.

---

## PARTE XV — MENSAGERIA E STREAMING DE EVENTOS

### Capítulo 106 — Fundamentos de mensageria
*Os conceitos universais que valem para qualquer broker.*
1. Por que filas: desacoplamento temporal e *peak shaving*
2. Ponto a ponto (*competing consumers*) × *publish-subscribe* (*fan-out*)
3. *Request-reply* assíncrono e *correlation id*
4. *Push* × *pull* e *backpressure*
5. Garantias de entrega: *at-most-once*, *at-least-once* e o que "exactly-once" realmente significa
6. *Idempotent consumer* e deduplicação
7. Ordenação de mensagens
8. *Poison pills* e DLQ

**Destaques práticos:** diagramas de cada topologia; consumidor idempotente com tabela de deduplicação.

### Capítulo 107 — RabbitMQ por dentro
*Roteamento flexível com AMQP.*
1. Modelo AMQP 0-9-1: `Connection` × `Channel`, *virtual hosts*, exchanges, filas e bindings
2. Os quatro tipos de exchange: Direct, Fanout, Topic e Headers
3. *Publisher confirms* e `ACK`/`NACK` do consumidor
4. *Prefetch count* (`basic.qos`) e distribuição de carga
5. DLX, TTL, filas de atraso e *priority queues*
6. Filas clássicas × *Quorum Queues* (Raft) × *Streams*
7. Spring AMQP na prática

**Destaques práticos:** diagrama de roteamento para cada tipo de exchange; configuração completa com DLX.

### Capítulo 108 — AWS SQS e SNS
*Mensageria gerenciada e serverless na nuvem.*
1. SQS Standard × FIFO (`MessageGroupId` e `MessageDeduplicationId`)
2. *Long polling* e *batching*
3. *Visibility timeout* e renovação dinâmica via *heartbeat*
4. DLQ e *redrive*
5. SNS e *fan-out* (1 SNS → N SQS) com *filter policies*
6. SNS/SQS × EventBridge — quando cada um
7. Spring Cloud AWS e LocalStack para desenvolvimento local
8. **Projeto: `HookDispatch & OmniNotify`** — hub de notificações e webhooks B2B assinados com HMAC, RabbitMQ com prioridade (2FA antes de relatórios), SNS + SQS para retentativas e portal de reprocessamento de DLQ

**Destaques práticos:** diagrama de sequência do visibility timeout expirando; C4 do HookDispatch.

### Capítulo 109 — Claim Check: mensagens leves para payloads pesados
*Brokers não foram feitos para transportar arquivos de 200 MB.*
1. O problema dos payloads grandes em brokers
2. O padrão Claim Check
3. Object storage (S3/MinIO), URLs pré-assinadas e criptografia
4. Ciclo de vida e limpeza de objetos órfãos
5. **Projeto 10.16: `LargeMedicalExamPipeline`** — laudos e tomografias armazenados criptografados no MinIO/S3, com metadado de ~1 KB na fila

**Destaques práticos:** diagrama de sequência do Claim Check com falhas parciais.

### Capítulo 110 — Apache Kafka por dentro: o log distribuído
*Por que o Kafka não é "uma fila mais rápida".*
1. O log *append-only* como abstração central
2. Segmentos, índices e retenção
3. I/O sequencial, *page cache* do sistema operacional e *zero-copy*
4. Brokers, controladores e KRaft (o fim do ZooKeeper)

**Destaques práticos:** diagrama da estrutura de um log em disco; comparação visual fila × log.

### Capítulo 111 — Kafka: partições, replicação e durabilidade
*Paralelismo, ordenação e garantia de não perder dados.*
1. Tópicos e partições; *partition key* e ordenação por chave
2. Offsets
3. Réplicas líder e seguidoras; ISR
4. Configuração de perda zero: `acks=all`, `min.insync.replicas=2`, `enable.idempotence=true`
5. *Log compaction*
6. Internals do produtor: batching, `linger.ms` e compressão

**Destaques práticos:** diagrama de partições replicadas entre brokers; simulação de queda de líder.

### Capítulo 112 — Consumidores Kafka e tratamento de erros
*Consumir em paralelo, com rebalanceamento e falhas.*
1. *Consumer groups* e o limite consumidores ≤ partições
2. Rebalanceamento: *eager* × *cooperative sticky* (`CooperativeStickyAssignor`) e o novo protocolo de grupos
3. Commit de offsets e semânticas resultantes
4. *Consumer lag*: medição e alertas
5. Spring Kafka e Spring Cloud Stream: *listeners*, concorrência e *error handlers*
6. *Non-blocking retries* (`@RetryableTopic`) e DLT
7. Transações e *exactly-once semantics* no Kafka
8. *Share groups* (filas no Kafka): o que são e o status atual

**Destaques práticos:** diagrama de atribuição de partições antes e depois de um rebalance; topologia de retry topics.

### Capítulo 113 — Contratos de eventos: Schema Registry, Avro e Protobuf
*Eventos são APIs; mudá-los sem cuidado quebra consumidores.*
1. Design de eventos: *event notification*, *event-carried state transfer* e *domain events*
2. Schema Registry
3. Avro × Protobuf × JSON Schema
4. Modos de compatibilidade: *backward*, *forward* e *full*
5. Evolução de schemas na prática

**Destaques práticos:** schema Avro versionado com mudança compatível e incompatível.

### Capítulo 114 — Processamento de streams com Kafka Streams
*Calcular sobre dados em movimento.*
1. Stream processing × batch
2. `KStream`, `KTable` e dualidade stream-tabela
3. Janelas: *tumbling*, *hopping*, *sliding* e *session*
4. *State stores* e tolerância a falhas
5. Kafka Streams × Apache Flink × Spark Structured Streaming

**Destaques práticos:** topologia desenhada e implementada para velocidade de gasto por cartão.

### Capítulo 115 — Change Data Capture com Debezium
*Transformar o log de transações do banco em eventos.*
1. CDC por consulta periódica × CDC baseado em log
2. Debezium e Kafka Connect
3. *Snapshots*, ordenação e garantias
4. Outbox Event Router (prévia do Capítulo 119)
5. **Projeto: `FraudStream Kafka Engine`** — Java 21 + Kafka KRaft + Avro + Debezium + Kafka Streams analisando PIX/cartão em janelas de segundos e bloqueando anomalias

**Destaques práticos:** diagrama de fluxo de dados WAL → Debezium → Kafka; C4 do FraudStream.

### Capítulo 116 — Escolhendo a mensageria: RabbitMQ × Kafka × SQS/SNS e além
*O capítulo de decisão: nenhuma opção é universalmente superior.*
1. Mensageria tradicional × *event streaming*
2. RabbitMQ × Kafka
3. SQS × RabbitMQ
4. Kafka × SQS
5. Outras opções: Apache Pulsar, NATS, Redis Streams e Google Pub/Sub
6. Critérios: volume, ordenação, persistência e *replay*, modelo de consumo, latência, custo operacional, escalabilidade e complexidade
7. Cenários: pagamentos, e-commerce, notificações, IoT, analytics e integração legada
8. Pare e Pense: sistema de pagamentos com milhares de transações — RabbitMQ, Kafka ou SQS?
9. Escolhas que parecem boas e se tornam problemas

**Destaques práticos:** matriz de decisão ponderada; diagramas da mesma solução nos três brokers.

---

## PARTE XVI — CONSISTÊNCIA E TRANSAÇÕES DISTRIBUÍDAS

### Capítulo 117 — Consistência em sistemas distribuídos
*O que acontece com as garantias ACID quando os dados se espalham por vários serviços.*
1. ACID × BASE como modelos de consistência
2. Modelos de consistência: linearizabilidade, sequencial, causal, *read-your-writes* e eventual
3. Teorema CAP: enunciado, interpretações erradas e uso correto
4. PACELC: latência × consistência em operação normal
5. **Modelo BASE — Projeto 10.02: `BaseSocialEngagement`** — curtidas, visualizações e carrinho altamente disponíveis com reconciliação em segundos

**Destaques práticos:** diagramas de partição de rede; linha do tempo de leituras sob cada modelo.

### Capítulo 118 — Two-Phase Commit e XA
*A tentativa clássica de atomicidade distribuída e seus custos.*
1. O protocolo 2PC: *prepare* e *commit*
2. Falha do coordenador e bloqueio
3. JTA/XA em Java
4. Por que 2PC raramente cabe em microsserviços; consenso (Raft/Paxos) como contraste
5. **Projeto 10.03: `XaTwoPhaseLab`** — coordenador JTA/XA entre dois PostgreSQL com benchmark de vazão

**Destaques práticos:** diagramas de sequência do caso feliz e da falha no meio do protocolo.

### Capítulo 119 — Dual write, Transactional Outbox e Idempotent Inbox
*O bug que perde ou duplica eventos e como eliminá-lo.*
1. O problema do *dual write*
2. Transactional Outbox: tabela `outbox` na mesma transação
3. Publicação por *polling publisher* × CDC (Debezium Outbox Router)
4. Idempotent Inbox: consumo único
5. **Projeto 10.06: `ZeroLossOutboxRelay`** — pagamentos que não perdem nem duplicam eventos mesmo com o broker derrubado no momento da confirmação

**Destaques práticos:** diagramas de sequência do dual write falhando e do outbox resolvendo.

### Capítulo 120 — Saga coreografada
*Transações de negócio longas coordenadas por eventos.*
1. O que é uma saga; transações compensatórias
2. Coreografia por eventos de domínio
3. Falta de isolamento e contramedidas (*semantic lock*, versão, releitura)
4. Rastreabilidade de sagas coreografadas
5. **Projeto 10.04: `ChoreoTravelBooking`** — `VooService`, `HotelService` e `PagamentoService` com estorno automático quando o hotel falha

**Destaques práticos:** diagrama de sequência com caminho feliz e compensações.

### Capítulo 121 — Saga orquestrada
*Um orquestrador com estado persistido no comando.*
1. Orquestrador como máquina de estados persistida
2. Compensações em ordem inversa e determinismo
3. Timeouts, retentativas e passos não compensáveis (*pivot transactions*)
4. Ferramentas: implementação própria × Temporal × Camunda
5. Coreografia × orquestração — comparação
6. **Projeto 10.05: `OrchestratedLoanSaga`** — consignado: averbar margem → biometria → emitir CCB → PIX, com compensação e painel de estado

**Destaques práticos:** diagrama de estados do orquestrador; Break-It Lab derrubando um serviço no meio da saga.

### Capítulo 122 — CQRS
*Modelos diferentes para escrever e para ler.*
1. Separação entre *commands* e *queries*
2. Projeções e modelos de leitura desnormalizados
3. Sincronização e consistência eventual da leitura
4. CQRS com e sem Event Sourcing; quando é exagero
5. **Projeto 10.07: `TicketArenaCQRS`** — compra de ingressos validada no PostgreSQL e mapa de assentos servido por projeção otimizada

**Destaques práticos:** diagrama de containers command/query; diagrama de sequência da atualização da projeção.

### Capítulo 123 — Event Sourcing
*O estado como consequência de uma sequência de fatos.*
1. Eventos como fonte da verdade; *event store*
2. Reconstrução de estado, *snapshots* e projeções
3. Versionamento e *upcasting* de eventos
4. Consultas temporais e auditoria
5. Event Sourcing × CDC × Outbox — diferenças
6. Quando NÃO usar
7. **Projeto 10.08: `TimeTravelWalletES`** — conta digital com saldo consultável em qualquer instante do passado

**Destaques práticos:** diagrama de stream de eventos e projeções; esquema da tabela de eventos.

---

## PARTE XVII — RESILIÊNCIA E TOLERÂNCIA A FALHAS

### Capítulo 124 — Fundamentos de tolerância a falhas
*Em sistemas distribuídos, falha parcial é o estado normal.*
1. As falácias da computação distribuída
2. Falhas parciais, falhas em cascata e *retry storms*
3. Timeouts: o padrão de resiliência mais importante e o mais negligenciado
4. Degradação graciosa
5. Resilience4j: visão geral

**Destaques práticos:** diagrama de falha em cascata; configuração de timeouts em cada camada.

### Capítulo 125 — Retry com exponential backoff e jitter
*Tentar de novo sem derrubar quem já está caído.*
1. Falhas transitórias × permanentes
2. Backoff exponencial, *jitter* e *thundering herd*
3. Retry × idempotência
4. Orçamento de retentativas e retentativas em camadas
5. **Projeto 10.15: `JitterRetryWebhookClient`** — cliente resiliente para APIs governamentais instáveis

**Destaques práticos:** gráfico de distribuição de retentativas com e sem jitter; implementação comparada.

### Capítulo 126 — Circuit Breaker e fallback
*Falhar rápido para não arrastar o sistema inteiro.*
1. Estados *closed*, *open* e *half-open*
2. Janelas por contagem × por tempo; limiares
3. Estratégias de fallback e seus riscos
4. Circuit breaker × retry × timeout: combinação correta
5. **Projeto 10.13: `MultiGatewayCircuitGuard`** — degradação da adquirente A detectada e vendas chaveadas para a adquirente B

**Destaques práticos:** diagrama de estados do circuit breaker; diagrama de sequência do chaveamento.

### Capítulo 127 — Bulkhead, rate limiting e load shedding
*Compartimentos estanques para que uma rota lenta não afunde o sistema.*
1. Bulkhead por semáforo × por pool de threads
2. Isolamento de pools de conexões
3. Rate limiting na aplicação × na borda
4. *Load shedding* e priorização
5. **Projeto 10.14: `BulkheadApiProtector`** — exportação de PDFs confinada enquanto o endpoint de vendas mantém baixa latência

**Destaques práticos:** diagrama de compartimentos; teste de carga comparando com e sem bulkhead.

---

## PARTE XVIII — QUALIDADE TOTAL: TESTES AVANÇADOS

### Capítulo 128 — Testando os testes: mutação, propriedades e fuzzing
1. Cobertura de linhas × eficácia real das asserções
2. Testes de mutação com PITest
3. Testes baseados em propriedades com jqwik
4. Fuzzing (Jazzer e alternativas, conforme status atual)

**Destaques práticos:** suíte com 100% de cobertura e mutantes sobreviventes; propriedades para o cálculo de parcelas.

### Capítulo 129 — Testes de componente e de contrato
1. Testes de componente (*subcutaneous*): o serviço inteiro em caixa-preta
2. Contratos orientados ao consumidor
3. Pact × Spring Cloud Contract
4. Validação de OpenAPI e de schemas no Schema Registry

**Destaques práticos:** diagrama do fluxo de contrato entre consumidor, broker de contratos e provedor.

### Capítulo 130 — Testes E2E, aceitação, regressão e smoke
1. E2E com Playwright e REST Assured nas jornadas vitais
2. Aceitação e BDD com Cucumber/Gherkin
3. Regressão, snapshot e *Golden Master* para refatorar legados
4. Smoke e sanity tests pós-deploy

**Destaques práticos:** cenário Gherkin completo; Golden Master aplicado a um cálculo legado.

### Capítulo 131 — Testes de arquitetura e fitness functions
1. Fitness functions como guardiãs da arquitetura
2. ArchUnit: camadas, dependências, nomenclatura e ciclos
3. Integração com Spring Modulith e com o build

**Destaques práticos:** regras ArchUnit para a arquitetura hexagonal do MedCore.

### Capítulo 132 — Testes de desempenho
1. Carga (*load*): validar p95/p99 no tráfego nominal e de pico
2. Estresse: encontrar o ponto de ruptura e a recuperação
3. Pico súbito (*spike*): filas e rate limit
4. Resistência (*soak*): vazamentos lentos
5. Escalabilidade: ganho ao adicionar réplicas
6. k6 × Gatling × JMeter
7. *Coordinated omission* e interpretação correta de resultados

**Destaques práticos:** gráficos de perfil de carga de cada tipo; scripts k6 comentados.

### Capítulo 133 — Engenharia do caos e testes de recuperação
1. Princípios da engenharia do caos e hipótese de estado estável
2. Toxiproxy (latência, perda, corte de conexão) e Chaos Mesh
3. Compatibilidade de migration: código V1 sobre banco V2
4. *DR drills*: restauração cronometrada de backup

**Destaques práticos:** experimento de caos com Toxiproxy em teste de integração.

### Capítulo 134 — Segurança automatizada e testes em produção
1. SAST, SCA e DAST (OWASP ZAP)
2. Suítes automatizadas anti-BOLA/IDOR
3. *Shift-right*: *synthetic monitoring*, *canary release* e *shadow traffic*
4. Testes de sistemas de IA (remissão ao Capítulo 154)
5. **Projeto: `CertiPulse`** — *harness* que submete uma API financeira aos 22 tipos de testes e emite laudo executivo de aprovação

**Destaques práticos:** mapa dos 22 tipos de testes × capítulos; C4 do CertiPulse.

---

# VOLUME 5 — PLATAFORMA, OBSERVABILIDADE E ENGENHARIA DE IA

## PARTE XIX — ENTREGA CONTÍNUA, CONTAINERS E PLATAFORMA

### Capítulo 135 — CI/CD: integração, entrega e implantação contínuas
*Do commit à produção com segurança e frequência.*
1. Continuous Integration × Continuous Delivery × Continuous Deployment
2. Anatomia de uma pipeline e artefatos imutáveis
3. Estratégias de deploy: *rolling*, *blue/green*, *canary* e *feature flags*
4. Métricas DORA
5. Rollback × *roll-forward*

**Destaques práticos:** diagrama de atividades de uma pipeline completa; comparação visual das estratégias de deploy.

### Capítulo 136 — GitHub Actions em profundidade
1. Gatilhos: `push`, `pull_request`, `workflow_dispatch` e `schedule`
2. `concurrency` e `strategy.matrix`
3. Cache avançado (Maven/Gradle e camadas Docker com Buildx)
4. Runners hospedados × *self-hosted* com Actions Runner Controller (ARC)
5. *Reusable workflows* (`workflow_call`) e *composite actions*
6. Ambientes com aprovação
7. GitHub Actions × GitLab CI × Jenkins — comparação

**Destaques práticos:** workflow completo de build multi-módulo comentado; equivalente em GitLab CI.

### Capítulo 137 — DevSecOps e segurança da cadeia de suprimentos
1. Federação OIDC sem segredos fixos (AWS, GCP, Azure)
2. SAST com CodeQL × Semgrep
3. SCA e SBOM: Dependabot, CycloneDX × SPDX
4. Varredura de imagens com Trivy
5. Detecção de segredos com Gitleaks
6. Assinatura de imagens com Cosign/Sigstore e níveis SLSA
7. **Projeto: `PipeShield DevSecOps Kit`** — esteiras reutilizáveis com build em cache, Testcontainers, CodeQL, Gitleaks, Trivy, Cosign, OIDC e deploy com rollback

**Destaques práticos:** diagrama de sequência da federação OIDC; C4 do PipeShield.

### Capítulo 138 — Containers Java para produção
1. Dockerfiles *multi-stage*
2. Spring Boot *layered JARs*; Buildpacks × Jib × Dockerfile — comparação
3. Imagens *distroless* e usuário *non-root*
4. *Graceful shutdown* em containers
5. Startup: CDS, Native Image e trade-offs

**Destaques práticos:** evolução de um Dockerfile ingênuo até a versão de produção, com tamanho e superfície de ataque comparados.

### Capítulo 139 — Kubernetes: arquitetura e objetos fundamentais
1. *Control plane* (API server, etcd, scheduler, controllers) e *worker nodes* (kubelet, kube-proxy, runtime)
2. O modelo declarativo e os *reconciliation loops*
3. `Pod`, `Deployment`, `ReplicaSet`, `StatefulSet`, `Job` e `CronJob`
4. `Service`, `ConfigMap` e `Secret`
5. Distribuições: Kubernetes puro, EKS/GKE/AKS e OpenShift/OKD

**Destaques práticos:** diagrama de arquitetura do cluster; manifestos comentados.

### Capítulo 140 — Kubernetes em produção: rede, probes, recursos e a JVM
1. Rede: tipos de Service, Ingress × Gateway API
2. `PodDisruptionBudget` (PDB) e `NetworkPolicy` (*zero-trust*)
3. `startupProbe`, `readinessProbe` e `livenessProbe`: responsabilidades distintas
4. `requests` e `limits`; *CPU throttling*
5. JVM em containers: `MaxRAMPercentage`, `OOMKilled` (código 137) e dimensionamento de memória não-heap

**Destaques práticos:** diagrama de sequência do ciclo de probes; Break-It Lab provocando OOMKilled.

### Capítulo 141 — Escalabilidade automática: HPA, VPA e KEDA
1. HPA por CPU, memória e métricas customizadas
2. VPA e *Cluster Autoscaler*
3. KEDA: escalar pelo lag do Kafka ou tamanho de fila (SQS/RabbitMQ), inclusive até zero
4. Armadilhas: oscilação, *cold start* da JVM e limites de partições

**Destaques práticos:** diagrama de fluxo KEDA → HPA → pods; ScaledObject comentado.

### Capítulo 142 — Helm e GitOps
1. Helm: charts, templates, values e releases
2. GitOps: o Git como fonte da verdade
3. Argo CD × Flux — comparação
4. Promoção entre ambientes

**Destaques práticos:** chart completo de um microsserviço Java; diagrama do fluxo GitOps.

### Capítulo 143 — Infraestrutura como código com Terraform
1. IaC declarativa: *providers*, *resources* e *state*
2. `plan`/`apply`, módulos e ambientes
3. State remoto, locking e *drift*
4. Terraform × OpenTofu × Pulumi × CloudFormation
5. **Projeto: `KubeElastic Cloud Blueprint`** — Terraform + Helm subindo cluster com microsserviços Java ajustados, probes, NetworkPolicies e KEDA escalando *workers* de 1 a 20 réplicas

**Destaques práticos:** diagrama de deployment C4 do KubeElastic; módulos Terraform comentados.

### Capítulo 144 — Sidecar, Ambassador e Service Mesh
1. O padrão Sidecar e o padrão Ambassador
2. Service Mesh: mTLS automático, *traffic shifting* e observabilidade
3. Istio × Linkerd; *sidecar* × *ambient mode*
4. Quando um mesh é exagero
5. **Projeto 10.17: `SecretInjectorSidecarLab`** — sidecar que renova credenciais temporárias e coleta métricas de rede para uma API Spring Boot

**Destaques práticos:** diagrama de pod com sidecar; comparação visual com e sem mesh.

---

## PARTE XX — OBSERVABILIDADE, SRE E FINOPS

### Capítulo 145 — Fundamentos de observabilidade
1. Monitoramento × observabilidade
2. Os sinais: métricas, logs, traces e perfis
3. Cardinalidade e custo
4. Métodos RED e USE e os *Golden Signals*
5. Logs estruturados em JSON e correlação

**Destaques práticos:** diagrama de como os três sinais se conectam por `traceId`.

### Capítulo 146 — OpenTelemetry
1. Arquitetura: API, SDK, Collector e OTLP
2. Instrumentação automática (Java agent) × manual × Micrometer
3. Propagação de contexto W3C `traceparent` via HTTP, gRPC, Kafka, RabbitMQ e JDBC
4. Métricas customizadas
5. Amostragem (*head* × *tail sampling*)

**Destaques práticos:** diagrama de sequência da propagação de contexto por um fluxo assíncrono; Collector configurado.

### Capítulo 147 — A stack de observabilidade: Prometheus, Grafana, Loki, Tempo e Mimir
1. Prometheus: modelo *pull*, tipos de métricas e histogramas
2. PromQL e cálculo de percentis
3. Grafana Loki para logs correlacionados por `traceId`
4. Grafana Tempo × Jaeger para tracing distribuído
5. Mimir e o significado de LGTM
6. Alternativas comerciais (Datadog, New Relic, Elastic) — critérios

**Destaques práticos:** dashboards e consultas PromQL comentadas; diagrama de containers da stack.

### Capítulo 148 — SRE: SLI, SLO, SLA e error budgets
1. SLI, SLO e SLA: diferenças e escolha de indicadores
2. Error budget: cálculo e política de uso
3. Alertas por *burn rate* em múltiplas janelas
4. Gestão de incidentes e *blameless post-mortem*
5. *Toil* e automação

**Destaques práticos:** cálculo de error budget passo a passo; regras de alerta comentadas.

### Capítulo 149 — Cloud FinOps e unit economics
1. O ciclo FinOps: informar, otimizar e operar
2. Custo por cliente, tenant e transação
3. *Rightsizing*, reservas, instâncias spot e *autoscaling* como alavancas de custo
4. *Tagging* e alocação de custos compartilhados
5. **Projeto: `PulseRadar SRE & FinOps Suite`** — telemetria e governança financeira com queima de SLO em tempo real, tracing ponta a ponta e margem por tenant

**Destaques práticos:** modelo de cálculo de custo unitário; C4 do PulseRadar.

---

## PARTE XXI — ENGENHARIA DE IA EM JAVA

### Capítulo 150 — Fundamentos de LLMs para engenheiros
*O suficiente de teoria para tomar boas decisões de engenharia.*
1. Como um LLM gera texto: transformers em alto nível e predição de tokens
2. Tokenização e janela de contexto
3. Custo assimétrico de *input* × *output*
4. Parâmetros de amostragem: `temperature` e *top-p*
5. *System prompts* e engenharia de prompts
6. Alucinação e limitações

**Destaques práticos:** diagrama do ciclo requisição → tokens → resposta; estimativa de custo de uma funcionalidade.

### Capítulo 151 — Integrando LLMs em Java: Spring AI e LangChain4j
1. Spring AI × LangChain4j — comparação
2. Provedores: OpenAI, Anthropic, Google Gemini e modelos locais via Ollama
3. *Structured Outputs*: resposta convertida em `record` via JSON Schema
4. Streaming de respostas via SSE
5. Timeouts, retentativas e tratamento de erros de provedores

**Destaques práticos:** o mesmo caso de uso implementado nos dois frameworks.

### Capítulo 152 — Embeddings e bancos vetoriais
1. Embeddings e o espaço vetorial
2. Similaridade: cosseno, produto interno e distância euclidiana
3. Busca aproximada (ANN): HNSW × IVFFlat
4. `pgvector` no PostgreSQL e busca vetorial no Redis (Redis Vector)
5. `pgvector` × bancos vetoriais dedicados (Qdrant, Milvus, Pinecone) × OpenSearch — comparação

**Destaques práticos:** diagrama de grafo HNSW; índice e consulta `pgvector` comentados.

### Capítulo 153 — RAG de produção
1. Por que RAG; RAG × fine-tuning × contexto longo
2. Ingestão e parsing de PDFs complexos
3. Estratégias de *chunking* (fixo, recursivo, semântico)
4. *Hybrid search*: vetorial + BM25 fundidos por RRF
5. Re-ranking com *cross-encoders*
6. Citação obrigatória de fontes
7. Isolamento multi-tenant
8. **Projeto: `LexVault Hybrid RAG`** — copiloto documental multi-tenant com respostas citando página e cláusula originais

**Destaques práticos:** diagrama do pipeline de ingestão e de consulta; C4 do LexVault.

### Capítulo 154 — Avaliação de sistemas de IA (AI Evals)
1. Por que testes tradicionais não bastam
2. *Golden datasets*
3. *LLM-as-a-Judge*: vieses e calibração
4. Métricas RAGAS (fidelidade, relevância, precisão e revocação de contexto)
5. Evals contínuos no CI a cada mudança de prompt

**Destaques práticos:** suíte de evals integrada ao pipeline do LexVault.

---

## PARTE XXII — AGENTES DE IA

### Capítulo 155 — Workflows e agentes: padrões de design
1. Workflow determinístico × agente autônomo: a decisão mais importante
2. Padrões: *prompt chaining*, *routing*, paralelização, *orchestrator-workers* e *evaluator-optimizer*
3. Multi-agente: *Router* / *Supervisor* com sub-agentes (Extrator, Auditor, Executor)
4. Quando NÃO usar agentes

**Destaques práticos:** diagramas de cada padrão; mesmo problema resolvido como workflow e como agente.

### Capítulo 156 — Ferramentas, function calling e MCP
1. *Function calling* e `@Tool` em Java
2. Model Context Protocol: hosts, clientes, servidores e transportes
3. Construindo servidores MCP em Java
4. Segurança de ferramentas: `tenantId`/`userId` vindos do `SecurityContext`, nunca do prompt
5. Validação de argumentos e princípio do menor privilégio

**Destaques práticos:** diagrama de sequência de uma chamada de ferramenta via MCP; ferramenta insegura × segura.

### Capítulo 157 — Memória e estado em agentes
1. Memória de curto prazo no Redis com TTL
2. Memória de longo prazo semântica no `pgvector`
3. Janela deslizante e sumarização assíncrona
4. Privacidade e retenção de memória

**Destaques práticos:** diagrama de containers da memória dupla.

### Capítulo 158 — Segurança, guardrails e controle de agentes
1. Limites de execução: `maxIterations` e orçamento de tokens
2. Circuit breaker multi-provedor
3. *Human-in-the-loop* em decisões críticas
4. *Prompt injection* direta e indireta
5. *PII masking* (CPF, nomes) antes do provedor externo e reversão local — LGPD
6. OWASP Top 10 para aplicações com LLM

**Destaques práticos:** diagrama de sequência com pausa para aprovação humana; pipeline de mascaramento.

### Capítulo 159 — FinOps de IA: reduzindo o custo de tokens
1. Filtro determinístico em Java antes da IA
2. *Semantic cache* no Redis e calibração do limiar
3. *Model routing* em cascata (modelos menores e locais primeiro)
4. Estruturação de prompts para *prompt caching*
5. Compressão de payload (tabelas enxutas × JSON verboso) e controle de `maxTokens`
6. Janela deslizante + sumarização
7. Processamento em lote: Kafka + Batch API
8. Medindo a economia real: *token ledger* e tarifação por cliente
9. **Projeto: `DocuAudit AI`** — auditoria multi-agente de dossiês com máscara LGPD, semantic cache, model routing e billing de tokens por cliente

**Destaques práticos:** fluxograma de decisão de roteamento; C4 do DocuAudit.

---

# VOLUME 6 — ARQUITETURA CORPORATIVA E SYSTEM DESIGN

## PARTE XXIII — ARQUITETURA COMO DISCIPLINA: MODELAGEM, DOCUMENTAÇÃO E DECISÃO

*Continuação pelo `roadmap.sh/software-architect`.*

### Capítulo 160 — O arquiteto de software: papéis, esferas e influência
1. *Application*, *Solution* e *Enterprise Architect*: escopos e entregáveis
2. Habilidades técnicas, de comunicação e de negociação
3. Influência sem autoridade
4. *Architecture Advice Process* × torre de marfim
5. *Greenfield* × *Brownfield*

**Destaques práticos:** mapa de responsabilidades por esfera; estudo de caso de uma decisão conduzida por advice process.

### Capítulo 161 — C4 Model completo
1. Nível 1 — *System Context* e seu público
2. Nível 2 — *Containers* (unidades implantáveis, não necessariamente Docker) e protocolos
3. Nível 3 — *Components*: quando vale a pena
4. Nível 4 — *Code*: geração sob demanda
5. Diagramas suplementares: *System Landscape*, *Dynamic* e *Deployment*
6. Erros comuns de notação e de nível de abstração

**Destaques práticos:** conjunto C4 completo do Banco Aurora em todos os níveis e visões.

### Capítulo 162 — Diagrams-as-code
1. Por que versionar arquitetura no Git
2. Structurizr DSL: um modelo, várias visões
3. Mermaid × PlantUML × Structurizr — comparação
4. Ferramentas visuais colaborativas (IcePanel) e seu lugar
5. Renderização no CI/CD

**Destaques práticos:** workspace Structurizr DSL completo gerando as visões do Capítulo 161.

### Capítulo 163 — arc42 e documentação viva
1. As 12 seções do arc42
2. Quanto documentar: documentação suficiente
3. *Docs-as-code*: MkDocs × Docusaurus
4. Mantendo a documentação viva

**Destaques práticos:** arc42 preenchido para o MedCore.

### Capítulo 164 — RFCs e ADRs
1. RFC: proposta colaborativa antes da decisão (motivação, desenho, impacto, segurança, custo, alternativas)
2. ADR: registro conciso e imutável após o consenso (Nygard e MADR)
3. Ciclo de vida: *Proposed*, *Accepted*, *Deprecated*, *Superseded*
4. Cultura de escrita técnica

**Destaques práticos:** uma RFC e três ADRs completos de exemplo.

### Capítulo 165 — Atributos de qualidade e avaliação de arquitetura
1. ISO/IEC 25010 (revisão 2023)
2. Cenários de atributos de qualidade: fonte, estímulo, artefato, ambiente, resposta e medida
3. Matriz de Pugh e matrizes ponderadas
4. ATAM: *sensitivity points*, *trade-off points*, riscos e não-riscos
5. Da avaliação às fitness functions

**Destaques práticos:** árvore de utilidade (*utility tree*) do Banco Aurora; ATAM simplificado conduzido passo a passo.

### Capítulo 166 — Modelagem de ameaças e riscos: STRIDE e Risk Storming
1. STRIDE: *Spoofing*, *Tampering*, *Repudiation*, *Information Disclosure*, *Denial of Service* e *Elevation of Privilege*
2. Aplicando STRIDE sobre o diagrama C4 de containers e fronteiras de confiança
3. Risk Storming colaborativo
4. Priorização e mitigação

**Destaques práticos:** diagrama de containers anotado com ameaças e mitigações.

### Capítulo 167 — Estratégia tecnológica: Wardley Mapping, Buy × Build e TCO
1. Wardley Maps: cadeia de valor e evolução (*Genesis → Custom Built → Product → Commodity*)
2. Onde construir diferencial e onde comprar
3. TCO: custos visíveis e ocultos
4. Matriz Buy × Build

**Destaques práticos:** Wardley Map do Banco Aurora; planilha de TCO comentada.

### Capítulo 168 — Governança: TOGAF, ArchiMate e portfólio
1. TOGAF ADM pragmático: fases e os quatro domínios (negócio, dados, aplicação e tecnologia)
2. ArchiMate em visão geral
3. Racionalização de portfólio: matriz TIME (*Tolerate, Invest, Migrate, Eliminate*)
4. Estratégias de migração para nuvem: 6 Rs (*Rehost, Replatform, Refactor/Re-architect, Repurchase, Retire, Retain*) e 7 Rs (+ *Relocate*)
5. Governança leve sem burocracia paralisante

**Destaques práticos:** classificação TIME de um portfólio fictício.

### Capítulo 169 — Modernização de legados I: AS-IS, TO-BE e Gap Analysis
1. Arqueologia de software: traces, logs de gateway, bancos compartilhados, jobs ocultos e entrevistas
2. SPOFs, acoplamento aferente/eferente, gargalos, riscos e TCO de base
3. TO-BE ligado a metas de negócio mensuráveis, sem *Hype Driven Development*
4. Gap Analysis nas quatro dimensões

**Destaques práticos:** C4 AS-IS e TO-BE de um monólito bancário; matriz de lacunas.

### Capítulo 170 — Modernização de legados II: arquiteturas de transição e Strangler Fig
1. Por que reescritas *Big Bang* fracassam
2. Arquiteturas de transição (T1, T2, T3) seguras e autossustentáveis
3. Onda T1: API Gateway + observabilidade + ACL
4. Onda T2: leitura crítica extraída via CDC para réplica (CQRS)
5. **Strangler Fig — Projeto 10.12: `MonolithStranglerProxy`** — roteamento gradual na borda, *shadow mode* e rollback instantâneo
6. Onda T3: *parallel run*, feature flag e descomissionamento
7. **Projeto: `Legacy2Cloud Modernization Portal & PoC`** — dossiê completo com AS-IS, TIME/6R/7R, Gap Analysis, C4 completo, STRIDE, Wardley Map, três transições, RFC, 10 ADRs e PoC da onda T1

**Destaques práticos:** sequência de diagramas mostrando a arquitetura em cada onda.

### Capítulo 171 — Dívida técnica
1. O que é (e o que não é) dívida técnica
2. O quadrante de Fowler: deliberada × inadvertida, prudente × imprudente
3. Identificação e medição
4. Comunicação com o negócio e priorização
5. Estratégias de pagamento contínuo

**Destaques práticos:** registro de dívida técnica e exemplo de negociação com produto.

### Capítulo 172 — Anti-patterns arquiteturais: os erros mais caros
1. *Overengineering*: complexidade sem requisito
2. *Underengineering*: atalhos que viram gargalos
3. Monólito distribuído, banco compartilhado entre serviços e serviços "tagarelas"
4. *Golden Hammer*, *Resume-Driven Development* e *Hype-Driven Development*
5. *Big Ball of Mud* e arquitetura acidental
6. Estudos de caso: decisões aparentemente boas que se tornaram problemas

**Destaques práticos:** diagramas "antes e depois" de cada anti-pattern.

---

## PARTE XXIV — SYSTEM DESIGN EM LARGA ESCALA

### Capítulo 173 — Metodologia de System Design e estimativas
1. Roteiro: requisitos funcionais e não funcionais, estimativas, desenho de alto nível, aprofundamento e trade-offs
2. *Back-of-the-envelope*: QPS de leitura e escrita, banda, armazenamento em 5 anos e RAM de cache
3. Ordens de grandeza e arredondamentos úteis

**Destaques práticos:** estimativa completa calculada passo a passo para um sistema de pagamentos.

### Capítulo 174 — Escalando dados: replicação, particionamento e sharding
1. Replicação líder-seguidor, multi-líder e sem líder
2. *Read replicas* e atraso de replicação
3. Particionamento e sharding: por faixa, por hash e por diretório
4. *Consistent hashing*
5. Rebalanceamento e *hot spots*

**Destaques práticos:** diagrama do anel de consistent hashing; simulação de redistribuição de chaves.

### Capítulo 175 — A borda global: CDN, edge computing e balanceamento global
1. CDNs: cache de borda e invalidação
2. Edge computing
3. Balanceamento global: DNS (GSLB) e anycast

**Destaques práticos:** diagrama de deployment global com CDN e regiões.

### Capítulo 176 — OLTP × OLAP e arquitetura de dados corporativa
1. OLTP × OLAP; armazenamento por linha × colunar
2. Data warehouse × data lake × lakehouse
3. ClickHouse × BigQuery × Snowflake
4. ETL × ELT e pipelines em tempo real com Debezium + Kafka
5. Data Mesh e *data as a product*

**Destaques práticos:** diagrama de fluxo de dados do OLTP ao OLAP.

### Capítulo 177 — Busca textual com OpenSearch e Elasticsearch
1. Índice invertido, análise de texto e BM25
2. Elasticsearch × OpenSearch (história da bifurcação e critérios)
3. Sincronização com o banco via CDC
4. Relevância, facetas e paginação profunda

**Destaques práticos:** busca de produtos do Marketplace Vértice com mapeamento e consultas comentadas.

### Capítulo 178 — Alta disponibilidade, disaster recovery e multi-região
1. Disponibilidade: os "noves" e o cálculo de disponibilidade composta
2. Redundância e eliminação de SPOFs
3. RPO e RTO
4. Estratégias de DR: *Backup & Restore*, *Pilot Light*, *Warm Standby* e *Multi-Site Active-Active*
5. Ativo-ativo e conflitos de escrita
6. Testes de failover
7. **Projeto: `GlobalScale OLAP & Disaster Recovery Engine`** — pipeline OLTP → Debezium → Kafka → ClickHouse + OpenSearch com dashboards sub-segundo e simulação cronometrada de failover regional

**Destaques práticos:** diagramas de deployment de cada estratégia de DR; tabela custo × RPO × RTO.

### Capítulo 179 — Design organizacional: Lei de Conway e Team Topologies
1. Lei de Conway e *Inverse Conway Maneuver*
2. Team Topologies: *Stream-aligned*, *Platform*, *Enabling* e *Complicated-Subsystem*
3. Modos de interação e carga cognitiva
4. Plataformas internas e *Golden Paths*

**Destaques práticos:** mapa de times e de sistemas do Banco Aurora antes e depois de uma reorganização.

### Capítulo 180 — Estudos de caso de System Design
*Problemas completos resolvidos do requisito ao trade-off, com perguntas para o leitor antes de cada análise.*
1. Sistema de pagamentos instantâneos (PIX)
2. Checkout de e-commerce com venda relâmpago
3. Ledger bancário de alta consistência
4. Sistema de notificações em larga escala
5. Feed de atividades com milhões de usuários
6. Rate limiter distribuído

**Destaques práticos:** para cada caso — requisitos, estimativas, C4, sequência, gargalos e alternativas descartadas.

---

## PARTE XXV — PROJETO INTEGRADOR: VeriTrust Cloud AI

### Capítulo 181 — VeriTrust Cloud AI: visão de produto, requisitos e cenários de qualidade
1. A tese de produto: onboarding digital, risco/antifraude, orquestração de eventos e auditoria por IA para fintechs, seguradoras, saúde e marketplaces
2. Personas e jornadas
3. Requisitos funcionais e não funcionais
4. Cenários de atributos de qualidade e árvore de utilidade

### Capítulo 182 — VeriTrust Cloud AI: arquitetura da solução
1. C4 completo (Landscape, Contexto, Containers, Componentes, Dinâmico e Deployment)
2. Buy × Build e STRIDE
3. Evolução MVP → Scale-Up (T1/T2) → Enterprise multirregião (TO-BE)
4. RFCs e caderno de ADRs
5. Integração dos módulos: Git/DevSecOps, Core Java, IAM, padrões, testes, Redis, Kafka, RabbitMQ, SQS/SNS, Kubernetes, observabilidade, IA multi-agente e analytics

### Capítulo 183 — VeriTrust Cloud AI: roteiro de implementação
1. Plano de construção em marcos
2. Definição de Pronto por marco
3. Riscos e estratégias de mitigação
4. Como apresentar o projeto em entrevistas e revisões de arquitetura

**Destaques práticos:** roadmap visual; matriz capítulo × componente do VeriTrust.

---

## Elementos pós-textuais

- **Conclusão:** a síntese da jornada, o que distingue engenharia de uso de ferramentas e como continuar evoluindo depois do livro.
- **Apêndice A — Mapa de correspondência:** Plano Mestre original, `roadmap.sh/java` e `roadmap.sh/spring-boot` × capítulos do livro (incluindo os 41 padrões e os 22 tipos de testes).
- **Apêndice B — Catálogo consolidado de projetos:** todos os projetos com escopo, pré-requisitos, capítulos e Definição de Pronto.
- **Apêndice C — Checklists de carreira:** requisitos de cada transição de nível × capítulos.
- **Apêndice D — Ambiente de laboratório:** JDK, IDE, Docker Compose base, Testcontainers, LocalStack e Keycloak.
- **Apêndice E — Migração de Java 17 e Spring Boot 2.7 para Java 21/25 e Spring Boot 3/4:** `javax` → `jakarta`, Spring Security, Hibernate 6+, observabilidade e roteiro incremental.
- **Glossário técnico:** termos, siglas e expressões em ordem alfabética, construído incrementalmente.
- **Referências bibliográficas e fontes de consulta:** livros, documentação oficial, RFCs e especificações (lista inicial abaixo, ampliada a cada capítulo).
- **Índice remissivo:** gerado na compilação de cada volume.

### Referências iniciais (do Plano Mestre, a ampliar)

Joshua Bloch, *Effective Java*; Brian Goetz et al., *Java Concurrency in Practice*; Gamma, Helm, Johnson e Vlissides, *Design Patterns*; Martin Fowler, *Patterns of Enterprise Application Architecture* e *Refactoring*; Chris Richardson, *Microservices Patterns*; Vaughn Vernon, *Implementing Domain-Driven Design*; Eric Evans, *Domain-Driven Design*; Robert C. Martin, *Clean Code* e *Clean Architecture*; Vladimir Khorikov, *Unit Testing Principles, Practices, and Patterns*; Simon Brown, *Software Architecture for Developers*; Jacqui Read, *Communication Patterns*; Mark Richards e Neal Ford, *Fundamentals of Software Architecture* e *Software Architecture: The Hard Parts* (com Pramod Sadalage e Zhamak Dehghani); Martin Kleppmann, *Designing Data-Intensive Applications*; Chip Huyen, *AI Engineering*; Gregor Hohpe e Bobby Woolf, *Enterprise Integration Patterns*; Betsy Beyer et al., *Site Reliability Engineering*; Matthew Skelton e Manuel Pais, *Team Topologies*. Documentação oficial: OpenJDK/JEPs, Spring, PostgreSQL, Apache Kafka, RabbitMQ, AWS, Kubernetes, OpenTelemetry, OWASP, C4 Model, arc42 e `roadmap.sh`.

---

## Apêndice A deste documento — Mapa de correspondência com o Plano Mestre

### Partes introdutórias e módulos

| Origem no Plano Mestre | Capítulos do livro |
| :--- | :--- |
| Benchmark `roadmap.sh` | Introdução, 1, seções 0.5 e 0.6 |
| Parte 1 — Progressão profissional | 1, Apêndice C |
| Parte 2 — Método de estudos e bibliografia | 2, 3, 4, Referências |
| Módulo 01 — Git | 4 (essencial), 66, 67 |
| Módulo 02 — Linux, redes, HTTP, build | 37, 68, 69, 70, 71 |
| Módulo 03 — CI/CD e DevSecOps | 135, 136, 137 |
| Módulo 04 — Fundamentos Java | 5–16, 20, 23–25 (6, 7, 14, 15, 24 e 26 acrescentados) |
| Módulo 05 — Java moderno, estruturas de dados e JVM | 17–19, 21, 22, 27–31 |
| Módulo 06 — Concorrência e Virtual Threads | 32–36 |
| Módulo 07 — PostgreSQL e JPA | 43, 44, 55–58, 73–76 (40–42 e 77 acrescentados) |
| Módulo 08 — Segurança | 59, 60, 78, 79, 80 |
| Módulo 09 — GoF e princípios | 82–89 (81 acrescentado) |
| Módulo 10 — 18 padrões transacionais e distribuídos | ver tabela abaixo |
| Módulo 11 — 22 tipos de testes | 39, 64, 128–134, 154 |
| Módulo 12 — DDD, Hexagonal, Clean, APIs | 52, 90–100 |
| Módulo 13 — Redis | 101–105 |
| Módulo 14 — Mensageria, RabbitMQ, SQS/SNS | 106–109 |
| Módulo 15 — Kafka, Schema Registry, CDC | 110–116 |
| Módulo 16 — Containers, Kubernetes, Terraform | 72, 138–144 |
| Módulo 17 — Observabilidade, SRE, FinOps | 145–149 |
| Módulo 18 — IA em Java e RAG | 150–154 |
| Módulo 19 — Agentes, MCP, guardrails, FinOps de tokens | 155–159 |
| Módulo 20 — C4, AS-IS/TO-BE, arc42, RFC/ADR, governança | 3, 92, 93, 160–172 |
| Módulo 21 — System Design, OLTP/OLAP, DR, Conway | 117, 173–180 |
| Parte 4 — VeriTrust Cloud AI | 181–183 |
| Parte 5 — Mapa consolidado | Apêndice B |
| *(novo)* Módulo dedicado ao Spring | 45–65 |

### Os 18 padrões do Módulo 10

| # | Padrão | Projeto | Capítulo |
| :-: | :--- | :--- | :-: |
| 10.01 | ACID (modelo) | `AcidVaultTransfer` | 43 |
| 10.02 | BASE (modelo) | `BaseSocialEngagement` | 117 |
| 10.03 | Two-Phase Commit / XA | `XaTwoPhaseLab` | 118 |
| 10.04 | Saga coreografada | `ChoreoTravelBooking` | 120 |
| 10.05 | Saga orquestrada | `OrchestratedLoanSaga` | 121 |
| 10.06 | Transactional Outbox & Idempotent Inbox | `ZeroLossOutboxRelay` | 119 |
| 10.07 | CQRS | `TicketArenaCQRS` | 122 |
| 10.08 | Event Sourcing | `TimeTravelWalletES` | 123 |
| 10.09 | Repository, Unit of Work & Specification | `RealEstateSpecSearch` | 94 |
| 10.10 | API Gateway & BFF | `DualChannelBankingBFF` | 100 |
| 10.11 | Anti-Corruption Layer | `LegacyErpShieldACL` | 92 |
| 10.12 | Strangler Fig | `MonolithStranglerProxy` | 170 |
| 10.13 | Circuit Breaker & Fallback | `MultiGatewayCircuitGuard` | 126 |
| 10.14 | Bulkhead | `BulkheadApiProtector` | 127 |
| 10.15 | Retry com Backoff + Jitter | `JitterRetryWebhookClient` | 125 |
| 10.16 | Claim Check | `LargeMedicalExamPipeline` | 109 |
| 10.17 | Sidecar | `SecretInjectorSidecarLab` | 144 |
| 10.18 | Distributed Lock & Leader Election | `ClusterBillingLeader` | 105 |

### Os 23 padrões GoF do Módulo 09

Projetos 09.01–09.05 no Capítulo 85; 09.06–09.12 no Capítulo 86; 09.13–09.18 no Capítulo 87; 09.19–09.23 no Capítulo 88.

### Os 22 tipos de testes do Módulo 11

| # | Tipo | Capítulo |
| :-: | :--- | :-: |
| 1 | Unitários | 39 |
| 2 | Mutação | 128 |
| 3 | Propriedades e fuzzing | 128 |
| 4 | Slice tests | 64 |
| 5 | Integração | 64 |
| 6 | Componente | 129 |
| 7 | Contrato | 129 |
| 8 | End-to-End | 130 |
| 9 | Aceitação / BDD | 130 |
| 10 | Regressão, snapshot e Golden Master | 130 |
| 11 | Smoke e sanity | 130 |
| 12 | Arquitetura (fitness functions) | 131 |
| 13 | Carga | 132 |
| 14 | Estresse | 132 |
| 15 | Pico súbito | 132 |
| 16 | Resistência (soak) | 132 |
| 17 | Escalabilidade | 132 |
| 18 | Engenharia do caos | 133 |
| 19 | Segurança automatizada | 134 |
| 20 | Compatibilidade de migration e DR drills | 133 |
| 21 | Shift-right em produção | 134 |
| 22 | Testes de IA (AI/LLM Evals) | 154 |

### Projetos principais

| Projeto | Capítulo |
| :--- | :-: |
| `FinTrack Core` | 25 |
| `SwiftRecon` | 31 |
| `FarePulse` | 36 |
| API de Pedidos do Marketplace Vértice (projeto progressivo do módulo Spring) | 45–65 |
| `RepoGuard CLI` | 67 |
| `CertWatch & NetProbe` | 71 |
| `SplitPay Ledger` | 75 |
| `TenantVault IAM` | 80 |
| `MedCore Modulith` | 99 |
| `FlashDrop & ShieldGate` | 105 |
| `HookDispatch & OmniNotify` | 108 |
| `FraudStream Kafka Engine` | 115 |
| `CertiPulse` | 134 |
| `PipeShield DevSecOps Kit` | 137 |
| `KubeElastic Cloud Blueprint` | 143 |
| `PulseRadar SRE & FinOps Suite` | 149 |
| `LexVault Hybrid RAG` | 153 |
| `DocuAudit AI` | 159 |
| `Legacy2Cloud Modernization Portal & PoC` | 170 |
| `GlobalScale OLAP & Disaster Recovery Engine` | 178 |
| `VeriTrust Cloud AI` | 181–183 |
