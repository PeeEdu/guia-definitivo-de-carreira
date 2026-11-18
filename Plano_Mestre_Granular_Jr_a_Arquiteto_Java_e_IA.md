# Plano Mestre Granular: De Desenvolvedor Java Júnior a Arquiteto de Software & Engenheiro de IA

**Objetivo:** Trilha profunda e desmembrada assunto por assunto, guiando a evolução técnica desde o reforço de base e nível **Júnior** até **Arquiteto de Software**, com **1 projeto real por módulo**, **1 projeto exclusivo para cada um dos 41 Design & Architectural Patterns** e um **Super Projeto Final**.  
**Horizonte Total Estimado:** 4 a 5,5 anos de evolução consistente e prática deliberada.  
**Referências Auditadas:** `roadmap.sh/java` | `roadmap.sh/backend` | `roadmap.sh/software-architect`

---

## Benchmark Oficial (`roadmap.sh`)

| Trilha Oficial | Competências Cobertas Integralmente nos Módulos | Módulos Correspondentes |
| :--- | :--- | :--- |
| **`roadmap.sh/java`** | **Fundamentos Java & POO**, Coleções e Complexidade Big-O, Generics, Streams, NIO.2, Maven/Gradle Multi-módulo, JVM Internals (ClassLoader, JIT, GraalVM, Memória), Garbage Collectors (G1GC, ZGC), Concorrência Avançada & **Virtual Threads**, JPA/Hibernate, HikariCP, **Todos os 23 Design Patterns GoF** e **Todos os 22 Tipos de Testes**. | Módulos 01, 02, 04, 05, 06, 07, 09 e 11 |
| **`roadmap.sh/backend`** | Linux, Redes (TCP/IP, DNS, TLS/mTLS, HTTP/1.1, HTTP/2, HTTP/3), **CI/CD (GitHub Actions)**, PostgreSQL Avançado (**ACID**), **Redis**, Mensageria (**RabbitMQ, SQS/SNS e Kafka**), APIs (**REST, gRPC, SSE, WebSockets**), Segurança (**OWASP Top 10, OAuth 2.0, OIDC, Keycloak**), Testes Não-Funcionais e **Engenharia de IA / Agentes**. | Módulos 02, 03, 07, 08, 11, 12, 13, 14, 15, 18 e 19 |
| **`roadmap.sh/software-architect`** | Esferas (*Application, Solution, Enterprise*), **C4 Model & Diagrams-as-Code**, **AS-IS / TO-BE / Gap Analysis / Arquitetura de Transição**, **arc42, RFCs & ADRs**, **ATAM, STRIDE & Wardley Mapping**, Padrões Distribuídos (**ACID vs BASE, 2PC, Saga, Outbox, CQRS, Event Sourcing, BFF, Sidecar, Strangler Fig**), Estilos (*Monólito Modular, Hexagonal, Clean, DDD*), Teoremas (**CAP** e **PACELC**), **Kubernetes + KEDA**, **Terraform**, **OpenTelemetry**, SRE, FinOps e **OLTP vs OLAP / CDC**. | Módulos 10, 12, 15, 16, 17, 19, 20, 21 e Super Projeto |

---

## Parte 1: Progressão Profissional no Mercado (Requisitos por Nível)

O mercado avalia sua senioridade pelo **escopo de autonomia, complexidade técnica resolvida, clareza de comunicação arquitetural e impacto no negócio**. Abaixo estão os critérios exatos de passagem de cada degrau até Arquiteto.

### 1. Desenvolvedor Júnior $\rightarrow$ Pleno
* **Tempo médio de transição:** 1 a 2 anos.
* **Foco central:** Autonomia tática para entregar funcionalidades completas com qualidade de produção sem depender de supervisão constante.
* **Requisitos Técnicos Obrigatórios:**
  * Dominar **Git** colaborativo (`rebase`, resolução limpa de conflitos, PRs coesos e revisão de código construtiva) — *Módulo 01*.
  * Compreender **HTTP, Redes básicas, Docker** e diagnosticar falhas em pipelines de **CI/CD (GitHub Actions)** — *Módulos 02 e 03*.
  * Ter base impecável em **Fundamentos Java, POO, `equals/hashCode`, `BigDecimal`, Exceções, `java.time`, Coleções e `Streams`** — *Módulos 04 e 05*.
  * Dominar **SQL, transações ACID, Flyway e JPA/Hibernate**: criar índices corretos, entender `@Transactional` e eliminar queries $N+1$ — *Módulos 07 e 10*.
  * Implementar autenticação/autorização com **Spring Security (JWT / OAuth 2.0)** e mitigar vulnerabilidades do **OWASP Top 10** — *Módulo 08*.
  * Aplicar os **Design Patterns GoF** essenciais do cotidiano (*Strategy, Factory, Builder, Adapter, Decorator, Proxy, State*) sem *over-engineering* — *Módulo 09*.
  * Escrever **Testes Unitários, Slice Tests e Testes de Integração reais com Testcontainers** — *Módulo 11*.
  * Consumir e publicar mensagens em filas garantindo **idempotência** e **DLQ (*Dead Letter Queue*)** — *Módulos 14 e 15*.
  * Saber ler diagramas **C4 Model (Níveis 1 e 2)** e consultar **ADRs** existentes antes de alterar fluxos críticos — *Módulo 20*.

### 2. Desenvolvedor Pleno $\rightarrow$ Sênior
* **Tempo médio de transição:** 2 a 3 anos atuando como Pleno.
* **Foco central:** *Ownership* ponta a ponta em produção, domínio de sistemas distribuídos, performance sob carga, desenho de componentes e mentoria técnica.
* **Requisitos Técnicos Obrigatórios:**
  * Diagnosticar gargalos de **JVM, Garbage Collector, Thread Dumps, Heap Dumps** e dominar **Concorrência / Virtual Threads** e locks de banco (*Optimistic vs Pessimistic*) — *Módulos 05, 06 e 07*.
  * Dominar todos os **Padrões GoF e Distribuídos** (**ACID vs BASE, Saga Coreografada e Orquestrada, Outbox, CQRS, Event Sourcing, Circuit Breaker, Bulkhead**), **DDD** e **Arquitetura Hexagonal / Clean** — *Módulos 09, 10 e 12*.
  * Elevar a barra de qualidade com **Testes de Mutação (PITest), Propriedades (jqwik), Contrato (Pact), Arquitetura (ArchUnit), Carga/Pico/Soak (k6) e Caos (Toxiproxy)** — *Módulo 11*.
  * Dominar **Redis avançado** (Cache L1+L2, invalidação, *Distributed Locks* e *Rate Limiting* via Lua) — *Módulo 13*.
  * Projetar fluxos assíncronos resilientes escolhendo corretamente entre **RabbitMQ, AWS SQS/SNS e Apache Kafka** — *Módulos 14 e 15*.
  * Operar microsserviços em **Kubernetes** (Probes, limites de memória/CPU sem `OOMKilled`, **KEDA**) com rastreamento via **OpenTelemetry + Grafana** — *Módulos 16 e 17*.
  * Documentar decisões do time em **ADRs** e desenhar diagramas **C4 (Contexto, Container, Dinâmico)** como código — *Módulo 20*.

### 3. Desenvolvedor Sênior $\rightarrow$ Especialista / Staff Engineer
* **Tempo médio de transição:** 1,5 a 2,5 anos atuando como Sênior.
* **Foco central:** Multiplicação técnica entre várias equipes, definição de padrões corporativos, modernização de legados críticos e **FinOps**.
* **Requisitos Técnicos Obrigatórios:**
  * Criar *Golden Paths* de **CI/CD**, bibliotecas internas, templates de infraestrutura (**Terraform / Helm**) e governança de testes para dezenas de desenvolvedores — *Módulos 03, 11 e 16*.
  * Conduzir decisões técnicas transversais por meio de **RFCs (*Request for Comments*)**, **ADRs**, modelagem de ameaças (**STRIDE**) e dossiês **arc42** — *Módulo 20*.
  * Mapear arquiteturas legadas (**AS-IS**) e liderar ondas seguras de migração para o estado futuro (**TO-BE**) com *Gap Analysis* e *Arquiteturas de Transição* — *Módulo 20*.
  * Liderar engenharia de **Confiabilidade (SLI/SLO/Error Budgets)** e redução mensurável de custos de nuvem — *Módulo 17*.
  * Arquitetar plataformas de **IA Generativa, RAG Híbrido e Agentes Autônomos** com *Guardrails* LGPD, **AI Evals** e controle estrito de custo de tokens — *Módulos 18 e 19*.

### 4. Especialista $\rightarrow$ Arquiteto de Software
* **Tempo médio de transição:** 1+ ano contínuo de consolidação estratégica.
* **Foco central:** Ponte executiva entre **Negócio e Tecnologia**, gestão de trade-offs corporativos, sustentabilidade financeira de longo prazo e evolução de todo o ecossistema.
* **Requisitos do Mercado (`roadmap.sh/software-architect`):**
  * Transitar entre as 3 esferas da profissão:
    * **Application Architect:** Padrões internos de código, qualidade estrutural, modularidade e *Fitness Functions*.
    * **Solution Architect:** Desenho fim a fim de soluções integrando múltiplos sistemas, nuvem, mensageria, segurança, IA e parceiros externos (**AS-IS $\rightarrow$ Transição $\rightarrow$ TO-BE**).
    * **Enterprise Architect:** Governança de portfólio corporativo (matriz **TIME / 6R**), estratégia **Buy vs. Build (Wardley Mapping & TCO)**, **TOGAF ADM pragmático**, compliance regulatório e alinhamento organizacional (**Lei de Conway**).
  * Dominar avaliação formal de trade-offs (**ATAM**), **System Design em larga escala**, **OLTP vs OLAP (CDC)** e **Disaster Recovery (RPO/RTO)** — *Módulos 20 e 21*.

---

## Parte 2: Guia Prático de Estudos & Metodologia de Alta Retenção

Estudar uma trilha de vários anos exige método de engenharia. Sem um sistema claro, você cai no *Tutorial Hell* (assiste dezenas de horas de vídeo, tem a ilusão de que entendeu, mas trava diante de um projeto em branco ou de uma reunião de arquitetura). Siga rigorosamente este guia em **todos os 21 módulos**:

### 1. A Regra $20 / 60 / 20$ de Alocação de Tempo
Para cada $10\text{ horas}$ estudadas em um módulo, divida seu esforço assim:
* **$20\%$ Teoria Direta na Fonte ($2\text{h}$):** Priorize documentação oficial (Java Docs, Spring, PostgreSQL, Kafka, Kubernetes, C4 Model, arc42), especificações (RFCs) e livros de referência. Use vídeos apenas para ter visão panorâmica inicial.
* **$60\%$ Prática Deliberada & Quebra Controlada ($6\text{h}$):** Codificação do projeto exclusivo do módulo (ou do mini-projeto de cada Design Pattern) **sem copiar código pronto** e execução de experimentos de falha.
* **$20\%$ Consolidação, Modelagem & Revisão ($2\text{h}$):** Desenhar diagramas **C4 Model** como código (Mermaid / Structurizr DSL), escrever **ADRs** e explicar o tema com suas próprias palavras (Método Feynman).

### 2. O Ciclo de 4 Passos Dentro de Cada Módulo
Nunca marque um módulo como concluído apenas por ter lido os tópicos. Execute este ciclo:
1. **Passo 1 — Mapeamento Mental & C4 Rápido:** Leia os tópicos do módulo e desenhe o diagrama de **Contexto e Container (C4)** mostrando como as peças se conectam e *qual dor real* aquela tecnologia ou padrão resolve.
2. **Passo 2 — *Break-It Lab* (Laboratório de Falha Proposital):** Um Sênior/Arquiteto se destaca quando as coisas dão errado. Em todo módulo, provoque o erro de propósito localmente:
   * *Estudando Fundamentos Java?* Quebre o contrato `hashCode()` de uma chave de `HashMap` e veja o objeto "sumir" da coleção.
   * *Estudando JVM?* Force um `OutOfMemoryError` e abra o *Heap Dump* no Eclipse MAT.
   * *Estudando Saga/Mensageria?* Mate o container do microsserviço de estoque após o pagamento aprovar e valide se o estorno compensatório executa sozinho.
3. **Passo 3 — Construção do Projeto Exclusivo com Escopo Fechado:** Trate os projetos principais como **MVPs reais** (com README executivo, diagrama C4 em Mermaid, testes e `docker-compose.yml`). Para os **41 projetos de Design Patterns**, crie um repositório multi-módulo organizado (`java-design-patterns-realworld`) com um módulo independente e testado para cada padrão.
4. **Passo 4 — Redação de ADRs (*Architecture Decision Records*):** Na pasta `/docs/adr` de cada projeto, registre em 1 página: *Qual era o contexto (AS-IS)? Quais alternativas descartei? Qual escolhi (TO-BE) e quais os trade-offs assumidos?*

### 3. Rotina Semanal Sustentável (Para Quem Trabalha $8\text{h}$/dia — Zero Burnout)
Uma meta consistente de **$8\text{h}$ a $10\text{h}$ líquidas por semana** constrói um Arquiteto extraordinário sem esgotamento:
* **Segunda, Quarta e Quinta ($1\text{h}15$ por dia):** Leitura técnica focada + pequenos laboratórios (*Break-It Labs* ou implementação de 1 Design Pattern por semana).
* **Terça e Sexta ($1\text{h}00$ por dia):** Refatoração, escrita de testes automatizados, diagramação C4 ou revisão espaçada das notas.
* **Sábado de Manhã ($3\text{h}00$ a $3\text{h}30$ em *Deep Work* sem celular):** Construção focada do **Projeto Prático do Módulo**.
* **Domingo:** Descanso obrigatório para consolidação neural.
* *Modo Manutenção para Semanas Caóticas:* Em semanas de plantão ou entrega pesada no trabalho, reduza para $20\text{ min}$ diários — apenas **nunca fique duas semanas seguidas zerado**.

### 4. Como Usar IA nos Estudos como Engenheiro (e Não como Muleta)
* **Proibido nos estudos:** Pedir *"Gere o código completo do padrão Saga"* e apenas colar na IDE.
* **Uso Recomendado (IA como Staff Engineer / Architecture Review Board):**
  * *"Desenhei esta transição AS-IS $\rightarrow$ TO-BE para extrair o motor de pagamentos de um monólito. Atue como um Principal Architect e aponte riscos de consistência de dados, latência e rollback que esqueci."*
  * *"Implementei a Saga Orquestrada abaixo em Java 21. Aponte todas as falhas caso a rede caia entre o passo 2 e o passo 3."*
  * *"Faça 5 perguntas difíceis de System Design e ATAM sobre este módulo para testar se realmente aprendi."*

### 5. Checklist "Definição de Pronto (DoD)" para Avançar de Módulo
Só avance do Módulo $N$ para o Módulo $N+1$ quando marcar **SIM** nos 4 itens:
- [ ] Consigo explicar este assunto e desenhar sua arquitetura no quadro branco por $5\text{ minutos}$ sem ler anotações?
- [ ] Provoquei pelo menos 1 cenário real de falha/bug neste tema e sei diagnosticá-lo?
- [ ] O(s) projeto(s) deste módulo sobe(m) localmente, possui(em) testes passando e diagrama C4 no GitHub?
- [ ] Documentei claramente em ADR **quando usar** e **quando NÃO usar** a solução estudada?

### 6. Bibliografia Essencial ao Longo da Jornada
* **Fundamentos & Java Efetivo:** *Effective Java* (Joshua Bloch) e *Java Concurrency in Practice* (Brian Goetz).
* **Padrões & Domínio:** *Design Patterns* (GoF), *Patterns of Enterprise Application Architecture* (Martin Fowler), *Microservices Patterns* (Chris Richardson) e *Implementing Domain-Driven Design* (Vaughn Vernon).
* **Testes:** *Unit Testing Principles, Practices, and Patterns* (Vladimir Khorikov).
* **Documentação, Modelagem & Arquitetura:** *The C4 Model / Software Architecture for Developers* (Simon Brown), *Communication Patterns* (Jacqui Read — excelente em C4, arc42 e AS-IS/TO-BE!), *Fundamentals of Software Architecture* & *Software Architecture: The Hard Parts* (Mark Richards & Neal Ford) e *Designing Data-Intensive Applications* (Martin Kleppmann).
* **IA Aplicada:** *AI Engineering* (Chip Huyen).

---

## Parte 3: Os 21 Módulos Especializados

---

### Módulo 01: Git, GitHub Internals & Fluxos de Engenharia Colaborativa
**Tempo Estimado:** 1 mês  
**Foco de Aprofundamento:** Dominar a estrutura interna do Git e a governança de versionamento em times de alta performance.

* **Conteúdo Detalhado:**
  * Internals da pasta `.git`: objetos endereçáveis por hash SHA (*Blobs*, *Trees*, *Commits*, *Tags*) formando um DAG; ponteiros `HEAD` e branches.
  * `git merge` (*fast-forward* vs *three-way*) vs `git rebase` (histórico linear limpo e regra de ouro em branches compartilhadas).
  * Comandos cirúrgicos: `git rebase -i` (*squash, fixup, reword, drop*), `git cherry-pick`, `git revert`, `git stash`, `git reflog`, `git bisect` (busca binária em $O(\log n)$ para achar regressões) e `git worktree` (múltiplas branches simultâneas em pastas distintas).
  * Estratégias: **Trunk-Based Development** + *Feature Flags* vs **GitHub Flow** vs **GitFlow**.
  * Governança: **Conventional Commits**, **SemVer ($MAJOR.MINOR.PATCH$)**, Git Hooks, `CODEOWNERS`, *Branch Protection Rulesets* e *Code Review* técnico.
* **Projeto Exclusivo: `RepoGuard CLI`**
  * Utilitário CLI que audita repositórios via GitHub API, valida *Conventional Commits*, mede *Lead Time* e tamanho de PRs, gera `CHANGELOG.md` SemVer automático e instala Git Hooks padronizados na equipe.

---

### Módulo 02: Linux, Redes, Protocolos Web & Build Tools Java
**Tempo Estimado:** 1,5 a 2 meses  
**Foco de Aprofundamento:** Dominar o sistema operacional, o tráfego de rede pacote a pacote e o empacotamento Java corporativo.

* **Conteúdo Detalhado:**
  * **Linux:** Processos, sinais (`SIGTERM` vs `SIGKILL`), permissões POSIX, *File Descriptors* (`ulimit`), memória/swap e diagnóstico (`ps`, `htop`, `lsof`, `ss`, `dig`, `curl -v`, `jq`, `journalctl`).
  * **Redes & Segurança de Transporte:** Modelo OSI vs **TCP/IP**, *3-Way Handshake*, Keep-Alive, **DNS** (A, CNAME, TXT, SRV, TTL), **TLS 1.3** e **mTLS** (autenticação mútua por certificados X.509).
  * **Protocolos HTTP:** **HTTP/1.1** (*Head-of-Line Blocking*) vs **HTTP/2** (multiplexação binária) vs **HTTP/3** (**QUIC** sobre UDP); Reverse Proxy (**NGINX / Envoy**), Load Balancing L4 vs L7 e CORS (*Preflight*).
  * **Maven & Gradle Avançado:** Ciclo de vida, criação de **BOM (*Bill of Materials*)**, `dependency:tree`, *Enforcer Plugin*, `surefire` vs `failsafe` e projetos **Multi-Módulo**.
* **Projeto Exclusivo: `CertWatch & NetProbe` (Micro-SaaS)**
  * Monitor contínuo para empresas que audita validade de certificados TLS/SSL, propagação DNS, suporte HTTP/2 e latência TCP, enviando alertas preventivos antes que certificados vençam e derrubem APIs em produção.

---

### Módulo 03: Engenharia de CI/CD & DevSecOps com GitHub Actions
**Tempo Estimado:** 2 meses  
**Foco de Aprofundamento:** Construir esteiras automatizadas rápidas, seguras e imutáveis do commit até a nuvem.

* **Conteúdo Detalhado:**
  * **CI vs Continuous Delivery vs Continuous Deployment**.
  * **GitHub Actions Profundo:** Triggers (`push`, `pull_request`, `workflow_dispatch`, `schedule`), `concurrency`, `strategy.matrix`, **Caching avançado** (Maven/Gradle + camadas Docker Buildx) e *Self-Hosted Runners* (**ARC**).
  * **DevSecOps na Pipeline:** Federação **OIDC Passwordless** com AWS/GCP/Azure (zero chaves fixas!), **SAST** (**CodeQL / Semgrep**), **SCA & SBOM** (*Dependabot / CycloneDX*), varredura de imagens (**Trivy**), detecção de segredos vazados (**Gitleaks**) e assinatura de imagens (**Cosign**).
  * **Escala:** **Reusable Workflows (`workflow_call`)**, **Composite Actions**, ambientes com aprovação e **GitOps (ArgoCD)**.
* **Projeto Exclusivo: `PipeShield DevSecOps Kit`**
  * Pacote reutilizável de esteiras GitHub Actions para times Java contendo build multi-módulo em cache, Testcontainers, CodeQL, Gitleaks, Trivy, assinatura Cosign, OIDC e deploy automatizado com rollback.

---

### Módulo 04: Reforço Rápido de Fundamentos Java (Base Sólida & POO sem Lacunas)
**Tempo Estimado:** 2 a 3 semanas (Revisão Intensiva de Nivelamento)  
**Foco de Aprofundamento:** Eliminar vícios e lacunas sutis da base Java que causam bugs graves de precisão financeira, `NullPointerException`, perda de objetos em coleções e código difícil de manter.

* **Conteúdo Detalhado (Revisão Direta ao Ponto):**
  * **Tipos, Memória Básica & Precisão Numérica:**
    * Tipos primitivos (`byte, short, int, long, float, double, boolean, char`) vs *Wrapper Classes* (`Integer, Long, BigDecimal`).
    * Armadilhas reais de *Autoboxing / Unboxing*: `NullPointerException` silencioso ao converter `Integer null` para `int`, e o cache interno de `Integer` ($-128$ a $127$) — por que comparar objetos com `==` funciona para $100$ mas falha em $200$.
    * **Dinheiro em Java:** Por que `double` e `float` (ponto flutuante binário IEEE 754: $0.1 + 0.2 = 0.30000000000000004$) são proibidos em finanças; uso correto de `BigDecimal(String)`, `scale` e `RoundingMode`.
    * **Semântica de Passagem de Parâmetros:** Java é **100% Pass-by-Value** (entender como a cópia do valor da referência é empilhada na *Stack* apontando para o objeto na *Heap*).
  * **Strings & Manipulação Textual:** Imutabilidade da `String`, funcionamento do *String Pool*, concatenação em loops (`StringBuilder` vs `+`), *Text Blocks* (`"""`) e expressões regulares pré-compiladas (`Pattern.compile`).
  * **POO Aplicada de Verdade:**
    * **Encapsulamento Forte:** Modificadores `private`, *package-private* (visibilidade de pacote para proteger o módulo), `protected` e `public`; invariantes validadas no construtor (nunca criar objetos em estado inválido com dezenas de `setters` soltos).
    * **Herança vs Composição:** Regra *É-UM* genuíno vs *TEM-UM*.
    * **Polimorfismo:** Sobrecarga (*Overloading* — compilação) vs Sobrescrita (*Overriding* — despacho dinâmico em runtime).
    * **Classes Abstratas vs Interfaces Modernas:** Métodos `default`, `static` e `private` em interfaces; `@FunctionalInterface`.
  * **O Contrato Sagrado de `java.lang.Object`:**
    * Implementação correta de `equals()` e `hashCode()`: por que objetos mutáveis usados como chave ou classes que sobrescrevem `equals` sem `hashCode` quebram `HashMap` e `HashSet`.
    * Ordenação natural com `Comparable<T>` vs ordenações múltiplas com `Comparator<T>`.
  * **Modificadores, Enums Ricos & `Optional`:**
    * Uso correto de `static`, blocos de inicialização e `final`.
    * **Enums Poderosos:** Enums Java com atributos, construtores privados e comportamento polimórfico por constante.
    * **Uso Correto de `Optional<T>`:** Exclusivamente para **retorno de métodos** (`map`, `flatMap`, `orElseGet` vs `orElse` e `orElseThrow`; jamais usar em parâmetros ou atributos JPA).
  * **Tratamento Profissional de Exceções:**
    * Hierarquia `Throwable` $\rightarrow$ `Error` vs `Exception` (*Checked* vs *Unchecked* `RuntimeException`), **`try-with-resources`** (`AutoCloseable`) e hierarquia limpa de exceções de domínio.
  * **API Moderna de Datas (`java.time`) & I/O Essencial:**
    * `LocalDate`, `LocalTime`, `LocalDateTime`, `Instant` (UTC), `ZonedDateTime` (`America/Sao_Paulo`), `Duration`, `Period`, `DateTimeFormatter`, `java.nio.file.Files` e **Jackson** (`ObjectMapper`).
* **Projeto Exclusivo: `FinTrack Core` (Motor de Finanças Pessoais & Parcelamento em Java Puro)**
  * Aplicação em Java puro que calcula faturas de cartão, compras parceladas com dízimas em `BigDecimal`, conversão de fusos horários internacionais (`ZonedDateTime`), categorização por **Enums ricos**, deduplicação via `equals/hashCode` e exportação/importação CSV e JSON via `try-with-resources`.

---

### Módulo 05: Java Moderno (17 a 21+), Estruturas de Dados & JVM Internals
**Tempo Estimado:** 2,5 a 3 meses  
**Foco de Aprofundamento:** Dominar complexidade algorítmica das coleções do JDK, recursos modernos do Java 21+ e funcionamento interno de memória e compilação da JVM.

* **Conteúdo Detalhado:**
  * **Estruturas de Dados & Big-O (`roadmap.sh/java`):** Custos $O(1)$, $O(\log n)$, $O(n)$, $O(n \log n)$ em `ArrayList` vs `LinkedList`, `ArrayDeque`, `PriorityQueue` (Heap), `TreeMap` (Árvore Rubro-Negra) e anatomia interna do `HashMap` (*load factor* $0.75$, colisões e *treeification* quando bucket $\ge 8$).
  * **Java 17 a 21+ Avançado:** `record`, `sealed classes/interfaces`, *Pattern Matching for `switch`*, *Record Patterns*, Generics (*PECS: Producer Extends, Consumer Super*), `Streams` avançados, `Collectors` customizados e **Java NIO.2** (*Channels*, *ByteBuffers*, *Memory-Mapped Files*).
  * **JVM Internals:** *ClassLoader*, leitura de *Bytecode* (`javap -c`), **JIT** (*C1/C2*, *Inlining*, *Escape Analysis*) vs **AOT (GraalVM Native Image)**.
  * **Memória & Garbage Collectors:** **Heap** (*Eden, Survivor, Old*), **Metaspace**, **Thread Stacks**, **Off-Heap**; ajuste fino de **G1GC** e **ZGC Generational**.
  * **Diagnóstico:** **JDK Flight Recorder (JFR)**, **Async-Profiler** (*Flame Graphs*) e caça a *Memory Leaks* com **Eclipse MAT**.
* **Projeto Exclusivo: `SwiftRecon — Motor Ultra-Rápido de Conciliação de Arquivos Gigantes`**
  * Conciliador B2B de arquivos CSV/EDI de $10\text{ GB}+$ via Java NIO.2 mantendo memória constante abaixo de $256\text{ MB}$ de Heap e distribuído como binário nativo **GraalVM**.

---

### Módulo 06: Programação Concorrente, Multithreading & Virtual Threads (Loom)
**Tempo Estimado:** 2 a 2,5 meses  
**Foco de Aprofundamento:** Escrever código altamente concorrente livre de *Race Conditions*, *Deadlocks* e *Thread Pinning*.

* **Conteúdo Detalhado:**
  * **Java Memory Model (JMM):** Caches de CPU, visibilidade, *Happens-Before*, `volatile` e imutabilidade.
  * **Primitivas & Locks:** Operações **CAS** (`AtomicReference`, `LongAdder`), `ReentrantLock`, `ReadWriteLock`, `StampedLock`, `Semaphore`, `CountDownLatch`, `CyclicBarrier`.
  * **Pools & Assincronismo:** `ThreadPoolExecutor` (*CPU-bound* vs *I/O-bound*), `ForkJoinPool` e `CompletableFuture`.
  * **Java 21+ Project Loom:** **Virtual Threads** (modelo $M:N$), detecção e eliminação de *Thread Pinning*, controle de concorrência externa via `Semaphore` (nunca fazer pool de Virtual Threads), **`StructuredTaskScope`** e **`ScopedValue`**.
* **Projeto Exclusivo: `FarePulse — Agregador Concorrente em Tempo Real`**
  * Cotador simultâneo de frete/passagens disparando $150+$ requisições externas paralelas com **Virtual Threads + `StructuredTaskScope`**, aplicando timeouts rigorosos e consolidação em $< 300\text{ ms}$.

---

### Módulo 07: PostgreSQL Avançado, Transações Concorrentes & JPA/Hibernate Tuning
**Tempo Estimado:** 3 meses  
**Foco de Aprofundamento:** Dominar os internals do PostgreSQL e extrair performance cirúrgica do Hibernate/HikariCP.

* **Conteúdo Detalhado:**
  * **Internals do PostgreSQL:** Páginas de $8\text{ KB}$, **WAL**, **MVCC**, *Dead Tuples* e `AUTOVACUUM`.
  * **Isolamento & Concorrência:** Anomalias (*Dirty Read, Non-Repeatable Read, Phantom Read, Lost Update, Write Skew*) e níveis `READ COMMITTED`, `REPEATABLE READ` e `SERIALIZABLE`.
  * **Indexação & Planos de Query:** Índices **B-Tree**, **GIN** (`JSONB`), **BRIN**, *Covering Indexes (`INCLUDE`)*, `EXPLAIN (ANALYZE, BUFFERS)`, particionamento de tabelas e migrations **Zero-Downtime com Flyway** (*Expand & Contract*).
  * **HikariCP & JPA/Hibernate:** Fórmula de dimensionamento do HikariCP:
    $$\text{Conexões} = (\text{Núcleos de CPU} \times 2) + \text{Spindle Efetivo}$$
    Ciclo de vida JPA, `@Transactional(readOnly = true)`, `open-in-view: false`, erradicação de $N+1$ (`JOIN FETCH`, `@EntityGraph`, *Record Projections*), batch inserts e **Optimistic (`@Version`) vs Pessimistic Locking (`SELECT ... FOR UPDATE SKIP LOCKED`)**.
* **Projeto Exclusivo: `SplitPay Ledger` (Core Contábil White-Label)**
  * Carteira digital e motor de *Split de Pagamentos* para marketplaces com partidas dobradas, migrations Flyway e blindagem contra saques concorrentes duplicados no PostgreSQL.

---

### Módulo 08: Segurança de Aplicações Back-end (AppSec, OAuth 2.0, OIDC & OWASP)
**Tempo Estimado:** 2 a 2,5 meses  
**Foco de Aprofundamento:** Proteger APIs corporativas e sistemas Multi-Tenant contra invasões, sequestro de sessão e vazamento de dados.

* **Conteúdo Detalhado:**
  * **Criptografia Prática:** Hashing de senhas (**Argon2id / BCrypt**), integridade (**HMAC-SHA256**), simétrica (**AES-256-GCM**) e assimétrica (**RSA / Ed25519**).
  * **OWASP Top 10 API:** Mitigação de **BOLA / IDOR**, *Mass Assignment*, **SSRF**, *Injection* e *Path Traversal*.
  * **Spring Security 6 & Identidade Federada:** `SecurityFilterChain`, **OAuth 2.0** (*Authorization Code + PKCE*, *Client Credentials*, *Refresh Token Rotation*), **OIDC**, validação **JWT via JWKS** e integração com **Keycloak**.
  * **Autorização & LGPD:** **RBAC**, **ABAC**, gestão segura de *API Keys* com hash SHA-256, *Field-Level Encryption* e trilha de auditoria imutável.
* **Projeto Exclusivo: `TenantVault IAM` (Micro-SaaS de Identidade & API Keys B2B)**
  * Serviço plugável de organizações Multi-Tenant, convites, permissões RBAC/ABAC, chaves de API com escopo, SSO via Keycloak e log de auditoria LGPD.

---

### Módulo 09: Design Patterns Clássicos GoF em Java 21+ (Todos os 23 Padrões — 1 Projeto por Pattern)
**Tempo Estimado:** 3 meses  
**Foco de Aprofundamento:** Dominar cada um dos **23 Design Patterns do Gang of Four (GoF)** no Java 21+ e Spring Boot, construindo **1 mini-projeto prático e realista para cada padrão**.

* **Princípios Norteadores:** **SOLID**, **GRASP**, **DRY**, **KISS**, **YAGNI**, **Tell, Don't Ask**, **Law of Demeter** e **Composição sobre Herança**.

#### A. Padrões Criacionais (5 Padrões = 5 Projetos Práticos)
1. **Singleton** — *Garante instância única compartilhada globalmente de forma thread-safe.*
   * **Projeto 09.01 — `FeatureToggleRegistry`:** Gerenciador em memória *thread-safe* de Feature Flags e configurações dinâmicas com recarga atômica sem reiniciar a API.
2. **Factory Method** — *Delega a criação de objetos especializados para métodos fábrica desacoplando o chamador da classe concreta.*
   * **Projeto 09.02 — `MultiBankSlipGenerator`:** Emissor polimórfico de boletos e QR Codes Pix (Itaú, Bradesco, Banco do Brasil) selecionado dinamicamente pelo código FEBRABAN.
3. **Abstract Factory** — *Cria famílias inteiras de objetos relacionados e compatíveis entre si sem especificar suas classes concretas.*
   * **Projeto 09.03 — `GlobalInvoiceSuite`:** Motor de faturamento internacional que instancia famílias coesas por país (`BR`: CPF/CNPJ + ICMS/ISS + NF-e XML; `US`: EIN + Sales Tax + Invoice PDF).
4. **Builder** — *Constrói objetos complexos imutáveis passo a passo com validação fluente (Staged Builder + Java `record`).*
   * **Projeto 09.04 — `LoanContractBuilder`:** Montador fluente e à prova de estado inválido para contratos de crédito bancário com avalistas, garantias, carência e indexadores.
5. **Prototype** — *Clona profundamente objetos pré-configurados custosos de montar a partir do zero.*
   * **Projeto 09.05 — `InsurancePolicyCloner`:** Gerador rápido de cotações de seguro empresarial clonando e customizando matrizes complexas de coberturas e franquias base.

#### B. Padrões Estruturais (7 Padrões = 7 Projetos Práticos)
6. **Adapter** — *Converte a interface incompatível de uma biblioteca ou sistema externo para o contrato limpo esperado pelo seu domínio.*
   * **Projeto 09.06 — `LegacyBiometricsAdapter`:** Adaptador que conecta um domínio moderno JSON/REST de abertura de contas a um provedor legado de biometria facial em SOAP/XML.
7. **Bridge** — *Separa uma abstração de sua implementação para que ambas evoluam independentemente ($M + N$ classes em vez de $M \times N$).*
   * **Projeto 09.07 — `OmniReportBridge`:** Gerador corporativo que cruza independentemente tipos de relatório (*DRE Financeiro, Posição de Estoque, Comissões*) com motores de renderização (*PDF, Excel XLSX, HTML, CSV*).
8. **Composite** — *Compõe objetos em estruturas de árvore tratando itens individuais e grupos compostos pela mesma interface.*
   * **Projeto 09.08 — `KitAndComboPricingTree`:** Calculadora de preços, peso de frete e impostos para e-commerce onde um produto simples e uma cesta promocional aninhada de kits respondem ao mesmo contrato.
9. **Decorator** — *Anexa responsabilidades adicionais a um objeto dinamicamente em camadas respeitando o princípio Open/Closed.*
   * **Projeto 09.09 — `DynamicTariffDecorator`:** Pipeline empilhável de cálculo de remessa internacional (Valor Base $\rightarrow$ Spread Cambial $\rightarrow$ IOF $\rightarrow$ Seguro Viagem $\rightarrow$ Desconto VIP).
10. **Facade** — *Fornece uma interface unificada e simples para um conjunto complexo de subsistemas.*
    * **Projeto 09.10 — `DigitalOnboardingFacade`:** Endpoint único de credenciamento de lojista que encapsula consulta de CNPJ, checagem de listas restritivas, validação bancária e criação de carteira.
11. **Flyweight** — *Compartilha estado intrínseco imutável entre milhões de objetos em memória para economizar gigabytes de RAM.*
    * **Projeto 09.11 — `SkuTaxFlyweightEngine`:** Catálogo em memória capaz de manter $2\text{ milhões}$ de itens ativos compartilhando objetos imutáveis de regras NCM/CEST, marcas e categorias em poucos megabytes.
12. **Proxy** — *Controla o acesso ao objeto original adicionando segurança, cache, lazy-loading ou auditoria (base do Spring AOP).*
    * **Projeto 09.12 — `CreditScoreSmartProxy`:** Proxy de proteção para consultas pagas ao bureau de crédito que verifica permissão do operador, mascara dados LGPD no log e retorna cache local evitando cobrança repetida.

#### C. Padrões Comportamentais (11 Padrões = 11 Projetos Práticos)
13. **Chain of Responsibility** — *Passa uma requisição ao longo de uma corrente de handlers onde cada elo valida, enriquece ou barra o fluxo.*
    * **Projeto 09.13 — `CardAntifraudChain`:** Esteira sequencial de autorização de cartão de crédito (Saldo $\rightarrow$ Horário Noturno $\rightarrow$ Distância Geográfica $\rightarrow$ Frequência por Minuto).
14. **Command** — *Encapsula uma ação como um objeto autônomo serializável permitindo fila, auditoria e reversão (undo).*
    * **Projeto 09.14 — `AuditedBankCommandBus`:** Executor de operações financeiras (`AgendarPix`, `BloquearCartao`, `AlterarLimite`) com log auditável completo e suporte a reversão operacional.
15. **Interpreter** — *Define uma gramática e um interpretador para avaliar regras dinâmicas escritas como texto.*
    * **Projeto 09.15 — `EligibilityRuleDSL`:** Motor onde analistas de negócio escrevem expressões como `(RENDA > 5000 AND SCORE >= 700) OR CLIENTE_VIP` avaliadas dinamicamente em Java sem novo deploy.
16. **Iterator** — *Percorre elementos de uma fonte complexa ou remota sequencialmente sob demanda sem expor sua representação interna.*
    * **Projeto 09.16 — `CloudStatementLazyIterator`:** Iterador Java que varre milhões de linhas de extratos paginados na AWS S3/API externa buscando lotes sob demanda sem estourar memória.
17. **Mediator** — *Centraliza comunicações caóticas muitos-para-muitos entre componentes em um coordenador único.*
    * **Projeto 09.17 — `ControlTowerChatMediator`:** Hub de atendimento omnichannel coordenando a transferência limpa de conversas entre Bot de Triagem, Atendente Humano, Supervisor e Auditoria.
18. **Memento** — *Salva e restaura snapshots anteriores do estado interno de um objeto sem violar seu encapsulamento.*
    * **Projeto 09.18 — `ContractDraftTimeMachine`:** Editor jurídico colaborativo de minutas contratuais com histórico de snapshots imutáveis, comparação de mudanças e *rollback* para qualquer versão anterior.
19. **Observer** — *Notifica automaticamente múltiplos interessados desacoplados sempre que um objeto muda de estado.*
    * **Projeto 09.19 — `InvoicePaidEventHub`:** Publicador interno Spring (`@TransactionalEventListener`) que, ao confirmar baixa de fatura, libera licença de software, credita comissão do vendedor e dispara recibo.
20. **State** — *Altera o comportamento de um objeto quando seu estado interno muda, eliminando condicionais gigantes de `if/switch` de status.*
    * **Projeto 09.20 — `ClaimLifecycleStateMachine`:** Máquina de estados rigorosa de Sinistro de Seguro (`ABERTO` $\rightarrow$ `EM_VISTORIA` $\rightarrow$ `APROVADO` $\rightarrow$ `INDENIZADO` / `NEGADO`) onde transições ilegais são impossíveis por design.
21. **Strategy** — *Define uma família de algoritmos intercambiáveis injetados em tempo de execução.*
    * **Projeto 09.21 — `SmartCommissionStrategy`:** Motor comercial que seleciona automaticamente a estratégia de cálculo de comissão (Varejo, Atacado, Franquia, Black Friday) injetada via `Map<String, Strategy>` no Spring.
22. **Template Method** — *Define o esqueleto invariável de um algoritmo na superclasse permitindo customizar apenas etapas específicas.*
    * **Projeto 09.22 — `UniversalBankReconciler`:** Esqueleto padronizado de importação contábil (Validar Assinatura $\rightarrow$ Ler Linhas $\rightarrow$ Conciliar $\rightarrow$ Gerar Resumo) com leitores específicos para OFX, CNAB 240 e CSV.
23. **Visitor** — *Adiciona novas operações sobre uma estrutura de objetos distintos sem modificar as classes dos elementos (`sealed interface` + Pattern Matching no Java 21+).*
    * **Projeto 09.23 — `RegulatoryTaxVisitor`:** Exportador que percorre uma carteira heterogênea de investimentos (`RendaFixa`, `Acao`, `FundoImobiliario`, `Cripto`) calculando Imposto de Renda e relatório BACEN com checagem exaustiva do compilador.

---

### Módulo 10: Padrões Transacionais (ACID / BASE), Corporativos & Distribuídos (Todos os 18 Padrões — 1 Projeto por Pattern)
**Tempo Estimado:** 3,5 meses  
**Foco de Aprofundamento:** Dominar os **modelos de consistência (ACID vs BASE)** e todos os **Design Patterns Arquiteturais, Transacionais e de Microsserviços** exigidos de Engenheiros Sêniores e Arquitetos, construindo **1 projeto focado por padrão**.

#### A. Modelos de Consistência & Transações Distribuídas (6 Padrões = 6 Projetos Práticos)
1. **Transação Local ACID (*Atomicity, Consistency, Isolation, Durability*)** — *Garante operações tudo-ou-nada mantendo invariantes íntegras no banco relacional.*
   * **Projeto 10.01 — `AcidVaultTransfer`:** Motor bancário local em PostgreSQL provando na prática as 4 propriedades ACID sob testes de concorrência pesada e falha simulada no meio do débito/crédito.
2. **Modelo BASE (*Basically Available, Soft state, Eventually consistent*)** — *Prioriza disponibilidade extrema e baixa latência aceitando convergência assíncrona.*
   * **Projeto 10.02 — `BaseSocialEngagement`:** Contador de curtidas, visualizações e carrinho de e-commerce altamente disponível que nunca bloqueia o usuário mesmo sob oscilação do banco principal, reconciliando o estado em segundos.
3. **Two-Phase Commit (2PC / Protocolo XA)** — *Coordena transação distribuída síncrona em duas fases (Prepare + Commit) entre múltiplos recursos.*
   * **Projeto 10.03 — `XaTwoPhaseLab`:** Coordenador transacional JTA/XA entre dois bancos PostgreSQL distintos demonstrando garantia atômica síncrona e provando em benchmark por que o bloqueio de locks reduz a vazão em microsserviços.
4. **Saga Pattern — Coreografada (*Choreography-based Saga*)** — *Transações locais ACID coordenadas por troca descentralizada de eventos de domínio e eventos compensatórios.*
   * **Projeto 10.04 — `ChoreoTravelBooking`:** Reserva de viagem distribuída (`VooService` $\leftrightarrow$ `HotelService` $\leftrightarrow$ `PagamentoService`) onde falha na reserva do hotel dispara automaticamente eventos de estorno da passagem aérea sem orquestrador central.
5. **Saga Pattern — Orquestrada (*Orchestration-based Saga*)** — *Um orquestrador central com máquina de estados persistida comanda cada microsserviço passo a passo e dispara compensações na ordem inversa exata.*
   * **Projeto 10.05 — `OrchestratedLoanSaga`:** Orquestrador de concessão de crédito consignado (Averbar Margem $\rightarrow$ Validar Biometria $\rightarrow$ Emitir CCB $\rightarrow$ Disparar PIX) com compensação determinística e painel de estado de cada Saga.
6. **Transactional Outbox & Idempotent Inbox Pattern** — *Elimina o bug crítico de Dual-Write salvando a mudança de negócio e o evento na tabela `outbox` na mesma transação ACID, garantindo consumo único via tabela `inbox`.*
   * **Projeto 10.06 — `ZeroLossOutboxRelay`:** Microsserviço de pagamentos que nunca perde nem duplica eventos mesmo derrubando o broker de mensageria no exato milissegundo da confirmação da compra.

#### B. Padrões de Dados, Domínio & Evolução de Arquitetura (6 Padrões = 6 Projetos Práticos)
7. **CQRS (*Command Query Responsibility Segregation*)** — *Separa o modelo rico de escrita (Commands) do modelo desnormalizado e ultra-rápido de leitura (Queries).*
   * **Projeto 10.07 — `TicketArenaCQRS`:** Sistema de venda de ingressos onde compras validam regras estritas no PostgreSQL (Command) e a consulta do mapa de assentos responde em $< 5\text{ ms}$ via projeção otimizada de leitura (Query).
8. **Event Sourcing** — *Persiste todas as mudanças como uma sequência imutável de fatos (eventos) permitindo auditoria temporal completa e reconstrução de estado.*
   * **Projeto 10.08 — `TimeTravelWalletES`:** Conta digital auditável onde é possível consultar o saldo exato em qualquer segundo do passado e reconstruir projeções inteiras a partir do *Event Store* + *Snapshots*.
9. **Repository, Unit of Work & Specification Pattern (PoEAA / DDD)** — *Isola persistência do domínio e compõe regras complexas de filtragem como predicados reutilizáveis.*
   * **Projeto 10.09 — `RealEstateSpecSearch`:** Buscador avançado de imóveis combinando dezenas de filtros opcionais via `Specification` limpa e tipada sem concatenar strings SQL.
10. **API Gateway & BFF (*Backend for Frontend*)** — *Cria fachadas de borda sob medida para a necessidade específica de cada cliente (Mobile enxuto vs Web Dashboard rico).*
    * **Projeto 10.10 — `DualChannelBankingBFF`:** Dois BFFs (Mobile e Internet Banking Web) agregando dados de Conta, Cartão e Investimentos em uma única chamada otimizada por dispositivo.
11. **Anti-Corruption Layer (ACL)** — *Camada de tradução defensiva que impede que modelos sujos e nomes crípticos de um sistema legado contaminem seu novo domínio limpo.*
    * **Projeto 10.11 — `LegacyErpShieldACL`:** Microsserviço moderno de logística blindado contra um banco legado com tabelas `TB_CLI_99` e códigos numéricos mágicos por meio de tradutores ACL dedicados.
12. **Strangler Fig Pattern** — *Migra sistemas legados críticos gradualmente redirecionando funcionalidades fatia por fatia na borda até aposentar o sistema antigo com risco zero.*
    * **Projeto 10.12 — `MonolithStranglerProxy`:** Gateway inteligente que intercepta rotas de um sistema legado monolítico, desvia `/v2/pagamentos` para o novo microsserviço Java 21, compara respostas em *Shadow Mode* e permite *rollback* instantâneo.

#### C. Padrões de Resiliência, Nuvem & Escala (6 Padrões = 6 Projetos Práticos)
13. **Circuit Breaker & Graceful Fallback** — *Interrompe chamadas para dependências externas degradadas imediatamente (Fail-Fast), evitando efeito dominó.*
    * **Projeto 10.13 — `MultiGatewayCircuitGuard`:** Processador de pagamentos que detecta degradação na Adquirente A em $3\text{ segundos}$, abre o circuito e chaveia automaticamente as vendas para a Adquirente B sem perder receita.
14. **Bulkhead Pattern (Isolamento de Recursos)** — *Divide pools de threads/conexões em compartimentos estanques para que a lentidão de uma rota secundária não afunde todo o sistema.*
    * **Projeto 10.14 — `BulkheadApiProtector`:** API comercial onde a exportação pesada de relatórios em PDF fica confinada em um compartimento limitado, garantindo que o endpoint crítico de vendas continue respondendo em $20\text{ ms}$.
15. **Retry com Exponential Backoff + Jitter** — *Refaz chamadas com falhas transitórias espaçando exponencialmente o tempo com variação aleatória contra tempestades de reconexão.*
    * **Projeto 10.15 — `JitterRetryWebhookClient`:** Cliente HTTP resiliente para integração com APIs governamentais instáveis (SEFAZ / Receita) evitando *Thundering Herd*.
16. **Claim Check Pattern** — *Desvia payloads pesados para um Object Storage (S3/MinIO) e trafega apenas uma chave leve de referência pela mensageria.*
    * **Projeto 10.16 — `LargeMedicalExamPipeline`:** Pipeline de laudos médicos e tomografias ($200\text{ MB}$) que armazena o arquivo criptografado no MinIO/S3 e envia apenas o metadado leve de $1\text{ KB}$ pela fila.
17. **Sidecar Pattern** — *Acopla funcionalidades transversais de infraestrutura em um container irmão ao lado da aplicação principal.*
    * **Projeto 10.17 — `SecretInjectorSidecarLab`:** Composição Docker/Kubernetes onde um container Sidecar renova credenciais temporárias e coleta métricas de rede de forma transparente para uma API Spring Boot limpa.
18. **Distributed Lock & Leader Election Pattern** — *Garante exclusão mútua ou elege um único nó coordenador em um cluster com dezenas de réplicas idênticas.*
    * **Projeto 10.18 — `ClusterBillingLeader`:** Serviço de fechamento mensal de assinaturas rodando com $4$ réplicas ativas onde um eleitor distribuído garante que apenas o nó Líder dispare as cobranças — assumindo outro nó em $2\text{ s}$ se o líder cair.

---

### Módulo 11: Engenharia de Testes & Qualidade Total (TODOS os 22 Tipos de Testes)
**Tempo Estimado:** 3 meses  
**Foco de Aprofundamento:** Dominar absolutamente **todos os tipos de testes utilizados hoje** em engenharia de software de elite.

* **Modelos & Estratégia:** Pirâmide de Testes vs *Testing Trophy / Honeycomb*, *Test Doubles* (**Dummy, Stub, Spy, Mock, Fake**), Escola Clássica (Detroit) vs Londres e *Shift-Left / Shift-Right*.
* **Os 22 Tipos de Testes na Prática:**
  1. **Unitários:** JUnit 5 + AssertJ + Mockito + `Clock` fixo ($< 5\text{ ms}$).
  2. **Mutação:** **PITest** auditando eficácia real das asserções contra mutantes no bytecode.
  3. **Baseados em Propriedades & Fuzzing:** **jqwik** e **Jazzer** gerando milhares de inputs extremos.
  4. **Slice Tests:** `@WebMvcTest`, `@DataJpaTest`, `@JsonTest`, `@RestClientTest`.
  5. **Integração:** **Testcontainers** + **WireMock** + **Awaitility**.
  6. **Componente (*Subcutaneous*):** Microsserviço inteiro testado em caixa-preta isolada.
  7. **Contrato:** **Pact**, **Spring Cloud Contract** e validação **OpenAPI / Schema Registry**.
  8. **End-to-End (E2E):** **Playwright** e **REST Assured** nas jornadas vitais.
  9. **Aceitação / BDD:** **Cucumber / Gherkin**.
  10. **Regressão, Snapshot & *Golden Master*:** Congelamento de saídas históricas para refatoração segura.
  11. **Smoke & Sanity Tests:** Verificação rápida de saúde pós-deploy.
  12. **Arquitetura (*Fitness Functions*):** **ArchUnit** protegendo camadas e regras de código no build.
  13. **Load Testing (*Carga* — k6 / Gatling):** Validar $p95/p99$ sob tráfego nominal e de pico esperado.
  14. **Stress Testing (*Estresse* — k6 / Gatling):** Encontrar o limite máximo de ruptura e recuperação.
  15. **Spike Testing (*Pico Súbito* — k6):** Explosão instantânea de tráfego validando filas e *Rate Limit*.
  16. **Soak / Endurance Testing (*Resistência Longa*):** Carga contínua por horas caçando *Memory Leaks* lentos.
  17. **Scalability Testing (*Escalabilidade*):** Medir ganho linear ao adicionar novas réplicas.
  18. **Chaos Engineering (*Testes de Caos*):** **Toxiproxy** e **Chaos Mesh** simulando rede lenta e queda de nós.
  19. **Segurança Automatizada:** **SAST, SCA, DAST (OWASP ZAP)** e suites anti-**BOLA/IDOR**.
  20. **Compatibilidade de Migration & DR Drills:** Código $V1$ rodando sobre banco $V2$ + restauração cronometrada de backup.
  21. **Shift-Right em Produção:** **Synthetic Monitoring**, **Canary Release** e **Shadow Traffic**.
  22. **Testes de IA (*AI / LLM Evals*):** *Golden Datasets*, **LLM-as-a-Judge** e métricas **RAGAS**.
* **Projeto Exclusivo: `CertiPulse — Suite & Plataforma de Certificação de APIs Críticas`**
  * *Harness* automatizado que submete uma API financeira aos 22 tipos de testes (incluindo mutação PITest, caos Toxiproxy, DAST OWASP ZAP e estresse k6) emitindo laudo executivo de aprovação para produção.

---

### Módulo 12: Arquitetura Limpa, Hexagonal, DDD & APIs Modernas (REST, gRPC, SSE, WebSockets)
**Tempo Estimado:** 3 meses  
**Foco de Aprofundamento:** Modelar negócios complexos isolados de frameworks e dominar comunicação síncrona e streaming em tempo real.

* **Conteúdo Detalhado:**
  * **DDD Estratégico & Tático:** *Event Storming*, Subdomínios (*Core, Supporting, Generic*), **Bounded Contexts**, *Linguagem Ubíqua*, Entidades ricas, *Value Objects*, **Aggregates**, *Domain Services* e *Domain Events*.
  * **Estilos Arquiteturais:** **Hexagonal (Ports & Adapters)**, **Clean Architecture** pragmática e **Monólito Modular com Spring Modulith**.
  * **Protocolos de API:** **REST Sênior** (RFC 7807 `ProblemDetail`, paginação por cursor *Keyset* em $O(1)$, `Idempotency-Key`, `ETag`), **gRPC + Protobuf** sobre HTTP/2 (Unary e Streaming) e tempo real com **SSE** vs **WebSockets**.
* **Projeto Exclusivo: `MedCore Modulith` (SaaS de Gestão Clínica & Telemedicina)**
  * Sistema médico construído em **DDD + Hexagonal + Spring Modulith**, com REST paginado por cursor, painel de atendimento em tempo real via **SSE/WebSockets** e motor interno de autorização de exames via **gRPC**.

---

### Módulo 13: Redis Profundo — Estruturas Avançadas, Cache Multi-Nível, Locks & Rate Limiting
**Tempo Estimado:** 2 meses  
**Foco de Aprofundamento:** Usar todo o poder do Redis para performance sub-milissegundo e coordenação distribuída.

* **Conteúdo Detalhado:**
  * **Internals & Topologia:** *Single-Threaded Event Loop*, políticas de *Eviction*, persistência **RDB vs AOF**, **Redis Sentinel vs Redis Cluster** ($16.384$ *hash slots*).
  * **Estruturas Avançadas:** `Strings`, `Hashes`, `Lists`, `Sets`, **`Sorted Sets (ZSET)`** (rankings e filas agendadas), **`Bitmaps`**, **`HyperLogLog`** (contagem única massiva em $12\text{ KB}$), **`Geo`** e **`Redis Streams`**.
  * **Cache de Alta Escala:** **Cache Híbrido L1 (Caffeine) + L2 (Redis)**; prevenção de *Cache Stampede*, *Cache Penetration* (**Bloom Filters**) e *Cache Avalanche* (TTL com *Jitter*).
  * **Atomicidade:** **Redisson Distributed Locks** com *Watchdog* e **Rate Limiting (*Token Bucket / Sliding Window*) em Lua Scripts**.
* **Projeto Exclusivo: `FlashDrop & ShieldGate` (Motor de Vendas Relâmpago & API Protector)**
  * Plataforma para lançamentos disputados (*Drops* de ingressos/tênis) com fila justa em `ZSET`, bloqueio de bots via *Bloom Filter* + *Rate Limit* em Lua e reserva atômica de estoque sem *overselling*.

---

### Módulo 14: Mensageria Tradicional & Serverless — Fundamentos, RabbitMQ & AWS SQS/SNS
**Tempo Estimado:** 2,5 a 3 meses  
**Foco de Aprofundamento:** Dominar todos os fundamentos universais de mensageria, roteamento avançado AMQP com **RabbitMQ** e filas serverless na nuvem com **AWS SQS e SNS**.

* **Conteúdo Detalhado:**
  * **Fundamentos Universais de Mensageria:** Desacoplamento temporal, *Peak Shaving*, *Competing Consumers* vs *Publish-Subscribe (Fan-out)*, *Request-Reply Assíncrono*, *Push vs Pull*, *Backpressure*, semânticas (*At-most-once*, *At-least-once*, *Exactly-once*), **Idempotent Consumer**, *Poison Pills* e **DLQ**.
  * **RabbitMQ Profundo (AMQP 0-9-1):** `Connection` vs `Channel`, *Virtual Hosts*, os 4 tipos de **Exchanges** (`Direct`, `Fanout`, `Topic`, `Headers`), *Publisher Confirms*, **Prefetch Count (`basic.qos`)**, `ACK / NACK`, **DLX (*Dead Letter Exchange*)**, filas com TTL/Delay, *Priority Queues* e **Quorum Queues** (consenso Raft).
  * **AWS SQS & SNS Profundo:** **SQS Standard vs FIFO** (`MessageGroupId` e `MessageDeduplicationId`), **Long Polling**, *Batching*, armadilhas de **Visibility Timeout** (renovação dinâmica via *Heartbeat*) e topologia **Fan-out (1 SNS $\rightarrow$ N SQS com *Filter Policies*)** com Spring Cloud AWS 3 + LocalStack.
* **Projeto Exclusivo: `HookDispatch & OmniNotify` (Micro-SaaS de Webhooks & Notificações)**
  * Hub garantido de disparo de notificações e **Webhooks B2B assinados com HMAC**, usando **RabbitMQ** com filas de prioridade (2FA fura fila de relatórios) e **SNS + SQS** para retentativas resilientes e portal de reprocessamento de DLQ pelo cliente.

---

### Módulo 15: Apache Kafka Profundo, Streaming de Eventos, Schema Registry & CDC
**Tempo Estimado:** 3 meses  
**Foco de Aprofundamento:** Dominar a arquitetura interna do **Apache Kafka**, evolução de contratos de eventos, **Debezium CDC** e processamento contínuo em tempo real.

* **Conteúdo Detalhado:**
  * **Internals do Kafka:** Log distribuído *append-only*, *Sequential Disk I/O*, *OS Pagecache* e transferência **Zero-Copy**; consenso **KRaft** (sem ZooKeeper).
  * **Particionamento & Durabilidade:** Tópicos, **Partições**, *Partition Key* (ordenação garantida por chave), Offsets, Réplicas Líder/Seguidoras, **ISR (*In-Sync Replicas*)**, *Log Compaction* e configuração zero-perda (`acks=all`, `min.insync.replicas=2`, `enable.idempotence=true`).
  * **Consumidores & Retries no Spring Kafka:** *Consumer Groups* (limite $\text{Consumidores} \le \text{Partições}$), `CooperativeStickyAssignor`, monitoramento de **Consumer Lag** e **Non-Blocking Retries (`@RetryableTopic`) + DLT**.
  * **Contratos & Streaming:** **Schema Registry + Apache Avro / Protobuf** (*Backward/Forward Compatibility*), captura de banco em tempo real com **Debezium CDC** e agregações em janelas temporais com **Kafka Streams**.
* **Projeto Exclusivo: `FraudStream Kafka Engine` (Motor Antifraude & Eventos Bancários em Tempo Real)**
  * Pipeline em **Java 21 + Kafka (KRaft) + Avro Schema Registry + Debezium CDC + Kafka Streams** capaz de analisar transações PIX/Cartão em janelas deslizantes de segundos, calculando velocidade de gasto e bloqueando anomalias instantaneamente.

---

### Módulo 16: Containers Otimizados, Kubernetes Profundo (KEDA) & Terraform
**Tempo Estimado:** 3,5 a 4 meses  
**Foco de Aprofundamento:** Provisionar infraestrutura como código e orquestrar microsserviços Java auto-escaláveis no **Kubernetes** sem desperdício nem quedas por memória.

* **Conteúdo Detalhado:**
  * **Containers Java de Produção:** *Multi-stage Dockerfiles*, *Spring Boot Layered JARs*, imagens **Distroless**, usuário `non-root` e **Graceful Shutdown**.
  * **Kubernetes (K8s) Completo:** *Control Plane* e *Worker Nodes*; `Pod`, `Deployment`, `StatefulSet`, `Job/CronJob`, `Service`, **Gateway API / Ingress**, `ConfigMap`, `Secret`, `PDB` e `NetworkPolicy` (Zero-Trust).
  * **JVM no Kubernetes:** Ajuste preciso de `requests/limits` evitando *CPU Throttling* e **`OOMKilled` (Exit Code 137)** (`-XX:MaxRAMPercentage=70.0`); separação correta entre `startupProbe`, `readinessProbe` e `livenessProbe`.
  * **Auto-Scaling & IaC:** **HPA** + **KEDA** (escalando pods automaticamente pelo *Lag* do Kafka ou tamanho da fila SQS/RabbitMQ), **Helm Charts**, noções de **Service Mesh** e infraestrutura declarativa com **Terraform**.
* **Projeto Exclusivo: `KubeElastic Cloud Blueprint`**
  * Infraestrutura completa em **Terraform + Helm** subindo cluster Kubernetes com microsserviços Java tunados, probes resilientes, *NetworkPolicies* e **KEDA** escalando *workers* de $1$ a $20$ réplicas sob pico de fila.

---

### Módulo 17: Observabilidade Full-Stack (OpenTelemetry), SRE & FinOps de Nuvem
**Tempo Estimado:** 2 meses  
**Foco de Aprofundamento:** Enxergar cada milissegundo de um sistema distribuído, governar disponibilidade por **Error Budgets** e dominar a economia unitária na nuvem.

* **Conteúdo Detalhado:**
  * **OpenTelemetry (OTel):** Propagação de contexto W3C (`traceparent`) entre HTTP, gRPC, Kafka, RabbitMQ e banco SQL; métricas customizadas com Micrometer.
  * **Stack LGTM:** **Prometheus** (PromQL, percentis $p50, p95, p99$, métodos RED e USE), **Grafana Loki** (logs JSON correlacionados por `traceId`), **Grafana Tempo / Jaeger** (Tracing Distribuído) e **Grafana**.
  * **SRE & Cloud FinOps:** Definição de **SLI, SLO, SLA**, cálculo de **Error Budget**, alertas por *Burn Rate*, *Blameless Post-Mortem* e **Unit Economics** (custo exato de nuvem por cliente/transação).
* **Projeto Exclusivo: `PulseRadar SRE & FinOps Suite`**
  * Central de telemetria e governança financeira acoplada a APIs Spring Boot exibindo queima de **SLO** em tempo real, rastreamento ponta a ponta e margem financeira líquida por Tenant SaaS.

---

### Módulo 18: Engenharia de IA em Java — LLMs, Embeddings, `pgvector` & RAG Híbrido
**Tempo Estimado:** 2,5 meses  
**Foco de Aprofundamento:** Integrar Inteligência Artificial Generativa em sistemas Java corporativos com respostas tipadas, fundamentadas em documentos privados e livres de alucinação.

* **Conteúdo Detalhado:**
  * **Fundamentos de Engenharia de LLMs:** Tokenização, janela de contexto, custo assimétrico *Input vs Output*, `temperature`, *System Prompts*, **Structured Outputs** (resposta convertida direto para `record` Java via JSON Schema) e streaming via **SSE**.
  * **Stack Java de IA:** **Spring AI** e **LangChain4j** integrando OpenAI, Anthropic, Google Gemini e modelos locais via **Ollama**.
  * **Bancos Vetoriais & RAG de Produção:** Embeddings, similaridade de cosseno, índices **HNSW** no **PostgreSQL (`pgvector`)** e **Redis Vector**; ingestão de PDFs complexos, *Chunking Semântico*, **Hybrid Search** (vetorial + lexical **BM25** fundidos via **RRF**), *Cross-Encoder Re-ranking*, citação obrigatória de fontes e avaliação quantitativa (**RAGAS**).
* **Projeto Exclusivo: `LexVault Hybrid RAG` (Copiloto Documental B2B Multi-Tenant)**
  * SaaS jurídico/médico/contábil em **Java 21 + Spring AI + `pgvector`** onde empresas consultam milhares de contratos e manuais internos recebendo respostas exatas com citação clicável da página e cláusula original.

---

### Módulo 19: Agentes Autônomos de IA em Java, MCP, Guardrails & FinOps de Tokens
**Tempo Estimado:** 3 meses  
**Foco de Aprofundamento:** Dominar o passo a passo de construção de **Agentes Autônomos seguros em Java** e as técnicas arquiteturais para **reduzir de $60\%$ a $85\%$ o gasto de tokens**.

* **A. Passo a Passo Prático: Como Criar Agentes de IA em Java**
  1. **Decisão *Workflow vs Agente*:** Fluxo previsível fica em código Java determinístico; use Agentes quando o sistema precisar planejar e escolher ferramentas dinamicamente.
  2. **Padrão Multi-Agente (*Router / Supervisor*):** Um agente leve classifica a intenção e delega para sub-agentes focados (*Extrator*, *Auditor*, *Executor*).
  3. **Ferramentas Seguras (`@Tool` / Function Calling) & MCP:** Exponha métodos Java validados e servidores **MCP (*Model Context Protocol*)**, injetando sempre `tenantId/userId` pelo `SecurityContext` do Spring (jamais confie em IDs sugeridos pelo prompt).
  4. **Memória Dupla:** Curto prazo da conversa no **Redis** com TTL + longo prazo semântico no **PostgreSQL (`pgvector`)**.
  5. **Limites de Execução & Human-in-the-Loop:** `maxIterations` contra loops infinitos, *Circuit Breaker* multi-provedor e pausa para aprovação humana em decisões críticas.
  6. **Guardrails & Privacidade LGPD:** Detector de *Prompt Injection* e **PII Masking** (mascarar CPF/nomes antes de enviar à LLM externa e reverter localmente).
  7. **AI Evals Contínuos:** Suite automatizada com *LLM-as-a-Judge* validando precisão a cada mudança de prompt.

* **B. FinOps de IA: 7 Técnicas para Minimizar Gasto de Tokens**
  1. **Filtro Determinístico em Java ($0\text{ Tokens}$):** Regras simples, hashes de arquivo repetido e validações formais resolvidas antes da IA.
  2. **Semantic Cache no Redis ($0\text{ Tokens}$):** Busca vetorial no Redis retornando respostas para perguntas semanticamente equivalentes ($\text{similaridade} \ge 0.95$) em $5\text{ ms}$.
  3. **Model Routing (*Cascading*):** Triagem e tarefas simples em modelos *Mini/Flash/Ollama* (até $20\times$ mais baratos), escalando para modelos *Frontier* apenas casos complexos.
  4. **Estruturação para *Prompt Caching* ($50\%$ a $90\%$ OFF):** Manter instruções, schemas e manuais fixos no prefixo inicial do prompt e dados variáveis apenas no final.
  5. **Compressão de Payload (CSV/Markdown Enxuto vs JSON):** Trocar listas JSON verbosas por tabelas enxutas economizando até $40\%$ dos tokens de entrada + controle rígido de `maxTokens` de saída.
  6. **Janela Deslizante + Sumarização Assíncrona:** Enviar apenas as últimas $4$ interações + resumo compacto mantido em background.
  7. **Kafka + Batch API ($50\%$ OFF):** Enfileirar processamentos não-urgentes no Kafka e despachar em lote pela *Batch API* com metade do custo.
* **Projeto Exclusivo: `DocuAudit AI` (SaaS Multi-Agente de Auditoria com Billing de Tokens)**
  * Plataforma B2B que audita dossiês imobiliários, médicos e financeiros com múltiplos agentes em Java 21, máscara LGPD, *Semantic Cache* no Redis, *Model Routing* e motor de tarifação (*Token Ledger*) por cliente.

---

### Módulo 20: Modelagem, Documentação Viva & Transformação Arquitetural (C4 Model, AS-IS / TO-BE, arc42, RFC/ADR & Governança)
**Tempo Estimado:** 2,5 a 3 meses  
**Foco de Aprofundamento:** Dominar todas as ferramentas visuais, frameworks de documentação, análise de trade-offs e planejamento de migração que diferenciam um programador sênior de um **Arquiteto de Soluções / Software / Corporativo**.

#### A. C4 Model Completo (Simon Brown) & Diagrams-as-Code
Esqueça diagramas caóticos misturando nuvens, tabelas de banco e classes na mesma tela. O **C4 Model** funciona como o zoom do Google Maps sobre o software:
1. **Nível 1 — System Context (Contexto do Sistema):**
   * Mostra o seu sistema como uma caixa central cercada pelos **Usuários/Personas** e **Sistemas Externos** (ex.: BACEN, Bureaus, Gateways, ERPs legados). Público: Diretoria, Produto, Negócio e Engenharia.
2. **Nível 2 — Container Diagram:**
   * Dá zoom dentro do sistema revelando as **unidades executáveis ou de armazenamento implantáveis independentemente** (*Web App, Mobile App, APIs Spring Boot, Workers Kafka, Banco PostgreSQL, Redis, S3*) e os protocolos exatos entre eles (`HTTPS/JSON`, `gRPC/mTLS`, `AMQP`). *Atenção: "Container" no C4 significa unidade de execução/dados, não necessariamente Docker!*
3. **Nível 3 — Component Diagram:**
   * Dá zoom dentro de **um** Container complexo mostrando seus blocos internos (Adapters de Entrada, Use Cases, Domain Services, Repositories/Gateways). Regra sênior: gere apenas para containers de alta criticidade para evitar documentação obsoleta.
4. **Nível 4 — Code:**
   * Diagramas de classes UML ou Entidade-Relacionamento gerados automaticamente sob demanda pela IDE apenas em núcleos algorítmicos densos.
5. **Os 3 Diagramas Suplementares Obrigatórios do C4:**
   * **System Landscape:** Visão corporativa acima do Nível 1 exibindo como todos os sistemas internos da empresa interagem entre departamentos.
   * **Dynamic Diagram:** Fluxo numerado passo a passo em tempo de execução ($1 \rightarrow 2 \rightarrow 3 \dots$) ilustrando como os Containers colaboram em um caso de uso crítico (ex.: fluxo de uma Saga de empréstimo ou autenticação OIDC).
   * **Deployment Diagram:** Mapeamento real dos Containers C4 sobre a infraestrutura física/nuvem (Regiões AWS, VPCs, Subnets Públicas/Privadas, Clusters EKS, Pods, RDS Multi-AZ).
6. **Diagrams-as-Code (Arquitetura Versionada no Git):**
   * Domínio de **Structurizr DSL** (onde você define o modelo de arquitetura uma única vez em texto e renderiza dezenas de visões C4 interativas automaticamente), **Mermaid**, **PlantUML** e **IcePanel** integrados ao CI/CD.

#### B. Arquitetura de Transformação: AS-IS $\rightarrow$ Gap Analysis $\rightarrow$ Arquiteturas de Transição $\rightarrow$ TO-BE
Na vida real, arquitetos raramente começam projetos 100% do zero (*Greenfield*); 90% das vagas de Arquiteto exigem modernizar ecossistemas existentes (*Brownfield*):
1. **Mapeamento AS-IS (*Baseline Architecture* — Estado Atual Real):**
   * Técnicas de arqueologia de software: auditar o que **realmente roda em produção** (via traces OpenTelemetry, logs de gateway, queries de banco compartilhado, jobs agendados ocultos e entrevistas com operação), identificando **SPOFs (*Single Points of Failure*)**, acoplamentos aferentes/eferentes, gargalos de latência, riscos de segurança, dores de negócio e custo atual (Baseline TCO).
2. **Desenho TO-BE (*Target Architecture* — Visão Alvo):**
   * Projetar a arquitetura norteadora para o horizonte de $12$ a $36\text{ meses}$ diretamente conectada a metas mensuráveis de negócio (ex.: reduzir tempo de onboarding de $24\text{h}$ para $15\text{s}$, suportar $10\times$ mais clientes ou isolar escopo PCI-DSS/LGPD), fugindo de *Hype Driven Development*.
3. **Gap Analysis (Matriz de Lacunas) & Racionalização de Portfólio:**
   * Comparação estruturada entre AS-IS e TO-BE nas **4 dimensões do TOGAF ADM**: *Arquitetura de Negócio, Arquitetura de Dados, Arquitetura de Aplicação e Arquitetura Tecnológica/Cloud*.
   * Classificação de ativos legados usando a **Matriz TIME do Gartner** (*Tolerate, Invest, Migrate, Eliminate*) e os **6 Rs de Migração para Nuvem** (*Rehost, Replatform, Refactor/Re-architect, Repurchase, Retire, Retain*).
4. **Transition Architectures (*Plateaus* / Ondas Intermediárias $T_1, T_2, T_3$):**
   * O maior erro de um arquiteto inexperiente é propor uma reescrita *Big Bang* de $18\text{ meses}$ que congela entregas de negócio e fracassa.
   * Você deve desenhar **estados intermediários seguros e autossustentáveis**:
     * *Onda $T_1$:* Colocar API Gateway na borda + Observabilidade + *Anti-Corruption Layer (ACL)*.
     * *Onda $T_2$:* Extrair leitura crítica via *Debezium CDC* para réplica desacoplada (*CQRS*).
     * *Onda $T_3$:* Extrair domínio crítico via *Strangler Fig* rodando em *Shadow Mode / Parallel Run* com *Feature Flag* de rollback em $1\text{ segundo}$ até descomissionar a tabela legada no **TO-BE**.

#### C. Frameworks de Documentação Viva, Decisão & Avaliação ("O Kit Completo de Arquiteto")
* **Template `arc42`:** O padrão internacional mais adotado para documentar arquiteturas de forma enxuta e completa em 12 seções padronizadas (1. Introdução e Metas, 2. Restrições, 3. Escopo e Contexto, 4. Estratégia de Solução, 5. Visão de Blocos/C4, 6. Visão de Runtime, 7. Visão de Implantação, 8. Conceitos Transversais, 9. Decisões/ADRs, 10. Requisitos de Qualidade, 11. Riscos e Dívidas Técnicas, 12. Glossário de Domínio).
* **RFCs (*Request for Comments*) vs ADRs (*Architecture Decision Records*):**
  * **RFC:** Documento colaborativo aberto **antes** da decisão para propostas de alto impacto, contendo motivação, desenho proposto, impacto em times, segurança, custos FinOps e alternativas descartadas.
  * **ADR (Padrão MADR / Michael Nygard):** Registro conciso e imutável no Git **após** o consenso (`Status: Proposed | Accepted | Deprecated | Superseded by ADR-0014`).
* **Atributos de Qualidade (ISO/IEC 25010), Cenários Mensuráveis & ATAM (*Architecture Tradeoff Analysis Method*):**
  * Traduzir pedidos vagos (*"precisa escalar e ser seguro"*) em **Quality Attribute Scenarios** testáveis (*Fonte $\rightarrow$ Estímulo $\rightarrow$ Artefato $\rightarrow$ Ambiente $\rightarrow$ Resposta $\rightarrow$ Medida*) e aplicar matrizes ponderadas (**Pugh Matrix**) e **ATAM** para explicitar *Sensitivity Points* e *Trade-offs* aos executivos.
* **Descoberta Colaborativa, Riscos & Estratégia Executiva:**
  * **Event Storming** (*Big Picture*, *Process Level* e *Design Level*), **Domain Storytelling** e **Context Mapping (DDD)** (*Shared Kernel, Customer-Supplier, Conformist, ACL, Open Host Service*).
  * **Threat Modeling (STRIDE) & Risk Storming:** Identificar ameaças (*Spoofing, Tampering, Repudiation, Information Disclosure, Denial of Service, Elevation of Privilege*) direto sobre o diagrama C4 de Containers.
  * **Wardley Mapping & Matriz Buy vs. Build (TCO):** Mapear componentes na curva de evolução (*Genesis $\rightarrow$ Custom Built $\rightarrow$ Product/SaaS $\rightarrow$ Commodity*) para saber onde construir diferencial competitivo próprio em Java e onde comprar pronto (ex.: Auth/IAM, antifraude comoditizado).
  * **TOGAF ADM & ArchiMate Pragmático:** Governança leve sem burocracia paralisante (*Architecture Advice Process* em vez de *Ivory Tower*).

* **Projeto Exclusivo: `Legacy2Cloud Modernization Portal & PoC` (Dossiê Completo de Arquiteto)**
  * Dado um estudo de caso realista de um monólito bancário/saúde crítico sofrendo quedas diárias e travamento de banco compartilhado, você construirá um **Portal Docs-as-Code interativo (Structurizr DSL + arc42 + MkDocs/Docusaurus)** contendo: diagnóstico **AS-IS**, classificação **TIME/6R**, **Gap Analysis** nas 4 dimensões, todos os diagramas **C4 Model (Níveis 1 a 4 + Landscape + Dynamic + Deployment K8s)**, modelagem de ameaças **STRIDE**, **Wardley Map (Buy vs. Build)**, **3 Arquiteturas de Transição ($T_1, T_2, T_3$)** até o **TO-BE**, 1 **RFC executiva**, **10 ADRs** e a PoC funcional em Java 21 da **Onda $T_1$** (*Strangler Proxy + ACL + Shadow Traffic*).

---

### Módulo 21: System Design em Larga Escala, Arquitetura de Dados (OLTP/OLAP), Multi-Região & Governança
**Tempo Estimado:** 4 a 5 meses  
**Foco de Aprofundamento:** Consolidar engenharia para milhões de usuários simultâneos, pipelines analíticos em tempo real e continuidade global de negócios.

* **Conteúdo Detalhado:**
  * **Teoria & Estimativas de Escala (*Back-of-the-Envelope*):** Teoremas **CAP** e **PACELC**; cálculos rápidos de capacidade (*QPS de leitura/escrita, largura de banda, armazenamento de $5\text{ anos}$, RAM de Cache*), *Consistent Hashing*, **Database Sharding**, *Read Replicas* e **CDNs / Edge Computing**.
  * **Arquitetura Corporativa de Dados (`OLTP vs OLAP`):** Separação entre bancos transacionais (**PostgreSQL**) e analíticos colunares (**ClickHouse / BigQuery / Snowflake**) alimentados em tempo real via **Debezium CDC + Kafka**, *Data Mesh* (*Data as a Product*) e busca textual de alta velocidade em **OpenSearch / Elasticsearch**.
  * **Continuidade de Negócio & Multi-Região:** Estratégias de Disaster Recovery (*Backup & Restore*, *Pilot Light*, *Warm Standby*, *Multi-Site Active-Active*) cumprindo metas estritas e testadas de **RPO (*Recovery Point Objective*)** e **RTO (*Recovery Time Objective*)**.
  * **Design Organizacional:** **Lei de Conway**, *Inverse Conway Maneuver* e **Team Topologies** (*Stream-aligned, Platform, Enabling e Complicated-Subsystem teams*).
* **Projeto Exclusivo: `GlobalScale OLAP & Disaster Recovery Engine`**
  * Arquitetura completa integrando pipeline transacional $\rightarrow$ **Debezium CDC $\rightarrow$ Kafka $\rightarrow$ ClickHouse + OpenSearch** para dashboards analíticos sub-segundo sobre dezenas de milhões de registros, acompanhada de simulação automatizada e cronometrada de **Failover Regional (RPO/RTO)**.

---

## Parte 4: O SUPER PROJETO FINAL (CAPSTONE) — **VeriTrust Cloud AI**

**Tempo Estimado de Construção:** 4 a 6 meses  
**Tese de Produto Real (SaaS B2B Enterprise Multi-Tenant):** Plataforma unificada de **Onboarding Digital, Motor Dinâmico de Risco/Antifraude, Orquestração Garantida de Eventos e Auditoria Autônoma de Dossiês por IA** para Fintechs, Seguradoras, Saúde e Grandes Marketplaces.

### Integração Total dos 21 Módulos em Produção:
1. **Modelagem Executiva & Documentação Viva (Módulo 20):** Portal **arc42 + Structurizr DSL** público no repositório com **C4 Model completo** (Landscape, Contexto, Containers, Componentes, Dinâmico e Deployment), matriz **Buy vs. Build**, modelagem **STRIDE**, plano evolutivo **MVP (AS-IS inicial) $\rightarrow$ Scale-Up ($T_1/T_2$) $\rightarrow$ Enterprise Multi-Região (TO-BE)**, **RFCs** e caderno de **ADRs**.
2. **Engenharia, Redes & DevSecOps (Módulos 01, 02 e 03):** Fluxo Git padronizado, mTLS/TLS 1.3 e pipelines **GitHub Actions Reusable Workflows** com CodeQL, Trivy, Gitleaks, assinatura Cosign, OIDC e GitOps ArgoCD.
3. **Core Java 21, Banco ACID & Segurança IAM (Módulos 04, 05, 06, 07 e 08):** Código sólido usando `BigDecimal` e `java.time`, binários otimizados, **Virtual Threads**, **PostgreSQL** particionado com **Flyway** e locks transacionais, protegido por **Keycloak (OIDC)**, API Keys e criptografia LGPD.
4. **Domínio Limpo, Todos os Padrões & Qualidade Certificada (Módulos 09, 10, 11 e 12):** Aplicação real dos padrões **GoF** e distribuídos (**ACID + BASE, Saga Orquestrada, Transactional Outbox/Inbox, CQRS, BFF, Circuit Breaker, Bulkhead, Claim Check**), **DDD + Hexagonal**, APIs **REST + gRPC + SSE** e certificação pelos **22 tipos de testes**.
5. **Malha de Baixa Latência & Eventos (Módulos 13, 14 e 15):** **Redis** (Cache L1/L2, *Bloom Filter*, *Redisson Locks* e *Rate Limit* em Lua), **Apache Kafka** (espinha dorsal de eventos com Avro + Kafka Streams), **RabbitMQ** (filas operacionais com prioridade) e **AWS SQS/SNS** (entrega resiliente de Webhooks HMAC).
6. **Cloud-Native, SRE, IA Multi-Agente & Analytics (Módulos 16, 17, 18, 19 e 21):** Cluster **Kubernetes + KEDA** provisionado via **Terraform**, observabilidade **OpenTelemetry + Grafana + SLOs + FinOps**, auditoria autônoma por **Agentes de IA em Java com RAG Híbrido (`pgvector`) e Semantic Cache** economizando até $80\%$ de tokens, e pipeline analítico **CDC $\rightarrow$ ClickHouse**.

---

## Parte 5: Mapa Consolidado dos 21 Módulos e Todos os Projetos

| Módulo | Assunto Isolado para Aprofundamento | Tempo Estimado | Projetos Práticos Exclusivos | Marco de Carreira |
| :---: | :--- | :---: | :--- | :--- |
| **01** | Git, GitHub Internals & Fluxos Colaborativos | 1 mês | `RepoGuard CLI` | Base Profissional |
| **02** | Linux, Redes, Protocolos HTTP/TLS & Build Tools | 1,5 a 2 meses | `CertWatch & NetProbe` | Base de Infra & Build |
| **03** | **CI/CD & DevSecOps (GitHub Actions)** | 2 meses | `PipeShield DevSecOps Kit` | Automação Profissional |
| **04** | **Reforço Rápido de Fundamentos Java & POO** | 2 a 3 semanas | `FinTrack Core` | **Base Java Blindada** |
| **05** | Java 17–21+, Estruturas de Dados & **JVM Internals** | 2,5 a 3 meses | `SwiftRecon File Engine` | Domínio da Plataforma |
| **06** | Concorrência, Multithreading & **Virtual Threads** | 2 a 2,5 meses | `FarePulse Aggregator` | Alta Vazão & Concorrência |
| **07** | **PostgreSQL Avançado**, Transações & JPA Tuning | 3 meses | `SplitPay Ledger` | Dados Transacionais |
| **08** | **Segurança Back-end** (OAuth 2.0, OIDC, OWASP) | 2 a 2,5 meses | `TenantVault IAM` | **Pleno Consolidado** |
| **09** | **Design Patterns Clássicos GoF (Todos os 23)** | 3 meses | **23 Mini-Projetos Exclusivos** ($1$ por Pattern GoF) | Excelência em Design OO |
| **10** | **Padrões Transacionais (ACID/BASE) & Distribuídos (18)** | 3,5 meses | **18 Mini-Projetos Exclusivos** (ACID, BASE, Saga, Outbox, CQRS...) | Padrões de Arquitetura |
| **11** | **Engenharia de Testes** (TODOS os 22 Tipos) | 3 meses | `CertiPulse Quality Suite` | Qualidade Nível Sênior |
| **12** | Clean/Hexagonal, **DDD** & APIs (REST, gRPC, SSE) | 3 meses | `MedCore Modulith` | Modelagem de Domínio |
| **13** | **Redis Profundo** (Cache L1/L2, Locks, Lua, ZSET) | 2 meses | `FlashDrop & ShieldGate` | Escala Sub-Milissegundo |
| **14** | Fundamentos de Filas, **RabbitMQ & AWS SQS/SNS** | 2,5 a 3 meses | `HookDispatch & OmniNotify` | Mensageria & Roteamento |
| **15** | **Apache Kafka Profundo**, Avro, CDC & Streams | 3 meses | `FraudStream Kafka Engine` | **Sênior Consolidado** |
| **16** | Containers, **Kubernetes (KEDA)** & Terraform | 3,5 a 4 meses | `KubeElastic Blueprint` | Engenharia Cloud-Native |
| **17** | **Observabilidade (OTel)**, SRE & Cloud FinOps | 2 meses | `PulseRadar SRE & FinOps` | Confiabilidade & Custos |
| **18** | **IA em Java**: LLMs, Embeddings, `pgvector` & RAG | 2,5 meses | `LexVault Hybrid RAG` | Engenharia de IA Aplicada |
| **19** | **Agentes de IA em Java**, MCP, Guardrails & FinOps | 3 meses | `DocuAudit AI` | **Especialista / Staff** |
| **20** | **Modelagem & Transformação (C4, AS-IS/TO-BE, arc42, ADR/RFC)** | 2,5 a 3 meses | `Legacy2Cloud Modernization Portal` | Arquitetura de Soluções |
| **21** | **System Design**, OLTP/OLAP, Multi-Região (DR) & Governança | 4 a 5 meses | `GlobalScale OLAP & DR Engine` | Arquitetura Enterprise |
| **FINAL** | **Super Projeto Integrador (Todos os 21 Módulos)** | 4 a 6 meses | **`VeriTrust Cloud AI`** | **Arquiteto de Software** |