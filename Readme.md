# Plano de Experimento – Avaliação TDD vs. Desenvolvimento Tradicional (v4.1)

## 1. Identificação básica

| Item | Descrição |
| :--- | :--- |
| **1.1 Título do experimento** | Avaliação Quantitativa e Qualitativa do Desenvolvimento Orientado a Testes (TDD) no Esforço, Qualidade e Percepção do Desenvolvedor. |
| **1.2 ID / código** | EXP-TCC-TDD-001-V4 |
| **1.3 Versão do documento e histórico de revisão** | v4.1 (Atualização dos dados de Autoria e Responsabilidade) |
| **1.4 Datas (criação, última atualização)** | Criação: 18/11/2025 | Última Atualização: 21/11/2025 |
| **1.5 Autores (nome, área, contato)** | Estêvão de Faria Rodrigues, Engenharia de Software, efrodrigues@sga.pucminas.br |
| **1.6 Responsável principal (PI / dono do experimento)** | Danilo de Quadros Maia Filho |
| **1.7 Projeto / produto / iniciativa relacionada** | Projeto de Trabalho de Conclusão de Curso (TCC) em Engenharia de Software. |

## 2. Contexto e problema

| Item | Descrição |
| :--- | :--- |
| **2.1 Descrição do problema / oportunidade** | Quantificar o *trade-off* real da adoção do TDD em projetos de complexidade média: o aumento potencial no esforço inicial se justifica pela melhora na qualidade de código (complexidade, acoplamento e redução de defeitos)? |
| **2.2 Contexto organizacional e técnico** | Contexto acadêmico/laboratório de desenvolvimento. Participantes são estudantes de Engenharia de Software com experiência intermediária em POO e testes unitários. Desenvolvimento em linguagem Java/Python, com versionamento Git. |
| **2.3 Trabalhos e evidências prévias** | Estudos de Nagappan et al. (2008) indicam que o TDD pode reduzir a densidade de defeitos (40% a 90%). Metanálises (Rafiq & Misic, 2012) mostram que o impacto na produtividade (esforço) é inconclusivo ou levemente negativo. |
| **2.4 Referencial teórico e empírico essencial** | Test-Driven Development (TDD): ciclo Red-Green-Refactor; Métricas de Qualidade OO (Coesão, Acoplamento, Complexidade Ciclomática); Medição de Esforço e Produtividade. |

## 3. Objetivos e questões (Goal / Question / Metric)

**3.1 Objetivo geral (Goal template)**

Analisar o efeito da utilização da técnica de Desenvolvimento Orientado a Testes (TDD), com o propósito de quantificar seu impacto no custo (esforço) e no benefício (qualidade e design) gerado, a partir da perspectiva do pesquisador/aluno e da organização (custo), no contexto de desenvolvimento de funcionalidades de software de complexidade média por estudantes de Engenharia de Software.

**3.2 & 3.3 & 3.4. GQM Completo (Objetivos, Questões e Métricas)**

| Objetivo Específico (Goal) | Perguntas de Pesquisa (Question) | Métricas Associadas (Metric) |
| :--- | :--- | :--- |
| **O1: Avaliar o Esforço e a Produtividade (Custo)** | **Q1.1:** O TDD resulta em um aumento significativo no tempo total para concluir as tarefas? | M1 (Tempo Total), M5 (Nº Commits) |
| | **Q1.2:** Há diferença no tempo dedicado especificamente à atividade de Teste entre os grupos? | M10 (Tempo em Testes), M1 (Tempo Total) |
| | **Q1.3:** O TDD impacta a estabilidade do processo de desenvolvimento (retrabalho)? | M5 (Nº Commits), M8 (Taxa Retrabalho) |
| **O2: Avaliar a Qualidade Interna (Design)** | **Q2.1:** O TDD produz código com menor complexidade estrutural e maior coesão? | M2 (Complexidade Ciclomática), M6 (Coesão Média) |
| | **Q2.2:** Há diferença no acoplamento do código gerado pelos diferentes tratamentos? | M7 (Acoplamento Média), M2 (Complexidade Ciclomática) |
| | **Q2.3:** A Cobertura de Testes gerada pelos participantes TDD é superior? | M4 (Cobertura Testes), M6 (Coesão Média) |
| **O3: Avaliar a Qualidade Externa (Defeitos)** | **Q3.1:** A técnica TDD reduz a densidade e a severidade dos defeitos encontrados na fase de aceite? | M3 (Densidade Defeitos), M11 (Severidade Defeitos) |
| | **Q3.2:** A redução de defeitos compensa o esforço de retrabalho do processo? | M3 (Densidade Defeitos), M8 (Taxa Retrabalho) |
| | **Q3.3:** O TDD aumenta a qualidade do código entregue em termos de funcionalidade e cobertura? | M11 (Severidade Defeitos), M4 (Cobertura Testes) |
| **O4: Avaliar a Percepção e a Satisfação do Desenvolvedor** | **Q4.1:** Os participantes consideram que o TDD lhes tomou mais tempo ou foi mais difícil de aplicar? | M9 (Satisfação), M10 (Tempo em Testes) |
| | **Q4.2:** A percepção de produtividade se correlaciona com as métricas objetivas de *commits*? | M5 (Nº Commits), M9 (Satisfação) |
| | **Q4.3:** Os desenvolvedores percebem uma melhoria na qualidade do design do código com TDD? | M4 (Cobertura Testes), M9 (Satisfação) |

## 4. Escopo e contexto do experimento

| Item | Descrição |
| :--- | :--- |
| **4.1 Escopo funcional / de processo** | **Incluído:** Desenvolvimento de três módulos de software (CRUD/Lógica de Negócio) de complexidade média, medição de esforço e coleta de métricas de qualidade. **Excluído:** Fases de Requisitos (o requisito será fornecido), *deploy* em produção e manutenção. |
| **4.2 Contexto do estudo** | Tipo: Acadêmico (laboratório de estudantes). Projeto: Funcionalidades CRUD simples/médias. Perfil de Experiência: Estudantes com conhecimento intermediário. |
| **4.3 Premissas** | Proficiência equivalente na linguagem de programação (Java/Python); Ambiente de desenvolvimento estável e padronizado; Requisitos funcionais claros. |
| **4.4 Restrições** | Duração máxima de 4 semanas para a execução; Orçamento zero para licenças de software; Dependência de uma amostra de conveniência (estudantes). |
| **4.5 Limitações previstas** | Validade Externa limitada (amostra acadêmica). Possível viés de auto-relato na métrica de esforço (M1, M10). |

## Tabela de Métricas Detalhadas (M1 a M11)

| Métrica | Nome da Métrica | Descrição | Unidade | Fonte de Dados |
| :--- | :--- | :--- | :--- | :--- |
| **M1** | Tempo Total de Desenvolvimento | Esforço total gasto desde o recebimento do requisito até a conclusão da tarefa. | Horas | *Time tracking* individual (formulário) |
| **M2** | Complexidade Ciclomática Média | Média de caminhos independentes por método, indicando a complexidade estrutural. | Número Inteiro | SonarQube / Ferramenta de Análise Estática |
| **M3** | Densidade de Defeitos | Número de defeitos funcionais encontrados por mil linhas de código (KLOC). | Defeitos/KLOC | Logs da fase de Testes de Aceitação |
| **M4** | Cobertura de Testes | Percentual de linhas/blocos de código cobertos por testes unitários. | Percentual (%) | Ferramenta de Cobertura (ex: JaCoCo) |
| **M5** | Número de Commits | Quantidade de vezes que o desenvolvedor registra uma alteração no repositório. | *Commits* por tarefa | Logs do Git |
| **M6** | Coesão Média (LCOM4) | Média da Lack of Cohesion in Methods (LCOM4), onde valores menores indicam melhor coesão. | Valor Real (0 a 1) | SonarQube / Ferramenta de Análise Estática |
| **M7** | Acoplamento Média (CBO) | Média de *Coupling Between Objects* (CBO), número de classes acopladas a uma dada classe. | Número Inteiro | SonarQube / Ferramenta de Análise Estática |
| **M8** | Taxa de Retrabalho | Proporção de linhas de código modificadas ou revertidas após o commit inicial da funcionalidade. | Percentual (%) | Logs do Git (Ferramenta de análise de *churn*) |
| **M9** | Satisfação do Desenvolvedor | Percepção de facilidade, produtividade e qualidade do design percebida pelo desenvolvedor. | Escala Likert (1-5) | Questionário Pós-Experimento |
| **M10** | Tempo Gasto em Testes | Esforço gasto exclusivamente na escrita, execução e refatoração de testes. | Horas | *Time tracking* individual (formulário) |
| **M11** | Severidade Média dos Defeitos | Média da gravidade dos defeitos encontrados (ex: 1=Menor, 5=Crítico). | Escala de Gravidade (1-5) | Avaliação do Pesquisador (durante Testes de Aceitação) |

## 5. Stakeholders e impacto esperado

| Item | Descrição |
| :--- | :--- |
| **5.1 Stakeholders principais** | Pesquisador/Aluno, Orientador, Professores da área de Software. |
| **5.2 Interesses e expectativas dos stakeholders** | Gerar evidências empíricas sobre a eficácia do TDD em um ambiente acadêmico controlado; Validar o conteúdo pedagógico da disciplina de testes. |
| **5.3 Impactos potenciais no processo / produto** | O código produzido é de descarte. O único impacto é o tempo alocado pelos participantes na execução das tarefas (estimado e controlado no cronograma). |

## 6. Riscos de alto nível, premissas e critérios de sucesso

| Item | Descrição |
| :--- | :--- |
| **6.1 Riscos de alto nível** | R1: Viés de treinamento (participantes TDD já têm mais experiência). R2: Desistência de participantes. R3: Falha na coleta automática de métricas. |
| **6.2 Critérios de sucesso globais (go / no-go)** | Coleta completa e consistente de dados de pelo menos 80% das tarefas; Capacidade de realizar o teste de hipóteses com poder estatístico $\geq 0.80$. |
| **6.3 Critérios de parada antecipada (pré-execução)** | Não atingir o número mínimo de 24 participantes recrutados após o período de treinamento; Reprovação do plano pelo Comitê de Ética. |

## 7. Modelo conceitual e hipóteses

| Item | Descrição |
| :--- | :--- |
| **7.1 Modelo conceitual do experimento** | O **Fator** (TDD vs. Tradicional) influencia as **Respostas** (Métricas de Esforço, Qualidade e Percepção). O Desenho Cruzado é usado para anular a influência da **Variável de Bloqueio** (Habilidade Individual). |
| **7.2 Hipóteses formais (H0, H1)** | **H0 (Nula):** Não há diferença significativa entre TDD e TD nas médias de esforço (M1, M10), qualidade (M2, M3, M4, M6, M7) e percepção (M9). **H1 (Alternativa):** TDD resulta em complexidade (M2) e acoplamento (M7) significativamente menores, coesão (M6) e cobertura (M4) significativamente maiores, e densidade de defeitos (M3) menor, podendo resultar em esforço (M1) maior. |
| **7.3 Nível de significância e considerações de poder** | **Nível de significância:** $\alpha = 0,05$. O **poder estatístico** será calculado previamente (Análise de Poder) para garantir que o tamanho da amostra (24 participantes) seja suficiente para detectar um efeito de tamanho médio (Cohen's d = 0.5) com $1-\beta \geq 0.80$. |

## 8. Variáveis, fatores, tratamentos e objetos de estudo

| Item | Descrição |
| :--- | :--- |
| **8.1 Objetos de estudo** | Três tarefas de desenvolvimento de software (Módulos A, B, C) de complexidade funcional controlada e equivalente. |
| **8.2 Sujeitos / participantes (visão geral)** | Estudantes de Engenharia de Software (semiprofissionais). |
| **8.3 Variáveis independentes (fatores) e seus níveis** | **Fator:** Técnica de Desenvolvimento. **Níveis:** (1) TDD (Desenvolvimento Orientado a Testes); (2) TD (Desenvolvimento Tradicional). |
| **8.4 Tratamentos (condições experimentais)** | **Tratamento TDD:** Obrigatório seguir o ciclo *Red-Green-Refactor*. **Tratamento TD:** Não há restrição sobre a ordem de escrita de código/testes. |
| **8.5 Variáveis dependentes (respostas)** | M1, M2, M3, M4, M5, M6, M7, M8, M9, M10, M11. |
| **8.6 Variáveis de controle / bloqueio** | Linguagem de programação (Java/Python), Ambiente de Desenvolvimento (IDE padronizada), Experiência Prévia em Programação (medida no pré-questionário). |
| **8.7 Possíveis variáveis de confusão conhecidas** | Diferenças na motivação individual e a ordem de execução das tarefas (abordada pelo contrabalanço). |

### Tabela de Variáveis Dependentes e Descrições

Esta tabela sumariza as variáveis de resultado (Métricas) que serão coletadas e analisadas para testar as hipóteses formais (7.2).

| Variável | Métrica | Descrição | Unidade | Tipo de Variável |
| :--- | :--- | :--- | :--- | :--- |
| **Esforço Total** | M1 | Tempo total gasto desde o recebimento do requisito até a conclusão da tarefa. | Horas | Quantitativa Contínua |
| **Complexidade** | M2 | Média de caminhos independentes por método (Complexidade Ciclomática). | Número Inteiro | Quantitativa Discreta |
| **Densidade Defeitos** | M3 | Nº de defeitos funcionais encontrados por mil linhas de código (KLOC). | Defeitos/KLOC | Quantitativa Contínua |
| **Cobertura Testes** | M4 | Percentual de linhas/blocos de código cobertos por testes unitários. | Percentual (%) | Quantitativa Contínua |
| **Número Commits** | M5 | Quantidade de vezes que o desenvolvedor registra uma alteração no repositório (indicador de granularidade). | *Commits* | Quantitativa Discreta |
| **Coesão Média** | M6 | Média da Lack of Cohesion in Methods (LCOM4). | Valor Real (0 a 1) | Quantitativa Contínua |
| **Acoplamento Média** | M7 | Média de *Coupling Between Objects* (CBO). | Número Inteiro | Quantitativa Discreta |
| **Taxa Retrabalho** | M8 | Proporção de linhas de código modificadas ou revertidas após o commit inicial da funcionalidade. | Percentual (%) | Quantitativa Contínua |
| **Satisfação** | M9 | Percepção de facilidade, produtividade e qualidade do design percebida. | Escala Likert (1-5) | Qualitativa Ordinal |
| **Tempo em Testes** | M10 | Esforço gasto exclusivamente na escrita, execução e refatoração de testes. | Horas | Quantitativa Contínua |
| **Severidade Defeitos** | M11 | Média da gravidade dos defeitos encontrados (ex: 1=Menor, 5=Crítico). | Escala de Gravidade (1-5) | Qualitativa Ordinal |

## 9. Desenho experimental

| Item | Descrição |
| :--- | :--- |
| **9.1 Tipo de desenho** | **Desenho de Sujeitos por Bloco Cruzado Completo/Incompleto** (*Within-Subjects Design*). Justificativa: Cada sujeito atua como seu próprio controle, reduzindo o impacto da variabilidade de habilidade individual (validez interna). |
| **9.2 Randomização e alocação** | Randomização da ordem das tarefas e da sequência de tratamento para cada participante, feita por sorteio simples, respeitando o princípio de contrabalanço. |
| **9.3 Balanceamento e contrabalanço** | Contrabalanço total: Todos os participantes experimentam ambos os tratamentos em tarefas diferentes, minimizando o efeito de ordem ou aprendizado ao longo do tempo. |
| **9.4 Número de grupos e sessões** | 1 Grupo de participantes. 1 Sessão de Treinamento e 3 Sessões de Execução (uma para cada tarefa/tratamento). |

### Tabela de Fatores, Tratamentos e Combinações

Esta tabela detalha a manipulação das variáveis independentes (fatores) e como as condições (tratamentos) são combinadas e aplicadas no experimento.

| Fator (Variável Independente) | Níveis do Fator | Tratamentos (Condições Experimentais) | Combinação no Desenho (Contrabalanço) |
| :--- | :--- | :--- | :--- |
| **Técnica de Desenvolvimento** | (1) TDD | Implementação seguindo rigorosamente o ciclo **Red-Green-Refactor** para cada funcionalidade. | **Desenho Cruzado (Within-Subjects):** Cada participante realiza tarefas equivalentes (A, B, C) sob ambos os tratamentos em ordens diferentes. |
| | (2) TD (Tradicional) | Implementação sem restrição de ordem na escrita de código ou testes (Test-Last permitido). | Exemplo de Sequência (Participante 1): Módulo A (TDD), Módulo B (TD), Módulo C (TDD). |
| **Tarefa** (Variável de Bloqueio) | Módulo A, Módulo B, Módulo C | Tarefas de desenvolvimento funcionalmente distintas, mas com complexidade e esforço equivalentes, baseadas nos mesmos requisitos de domínio. | A randomização da sequência (A-B-C, B-C-A, etc.) anula o efeito da ordem das tarefas. |

## 10. População, sujeitos e amostragem

| Item | Descrição |
| :--- | :--- |
| **10.1 População-alvo** | Desenvolvedores de software com perfil de experiência intermediária (2-5 anos de prática). |
| **10.2 Critérios de inclusão de sujeitos** | Ser estudante a partir do 4º período de Eng. Software; Ter realizado a disciplina de Testes de Software; Ter disponibilidade de 10 horas/semana por 4 semanas. |
| **10.3 Critérios de exclusão de sujeitos** | Falta de proficiência na linguagem de programação; Conflito de interesses ou experiência sênior prévia (mais de 5 anos de experiência industrial). |
| **10.4 Tamanho da amostra planejado (por grupo)** | Total de **24 participantes** (12 na ordem A-B-C, 12 na ordem C-B-A, etc.). |
| **10.5 Método de seleção / recrutamento** | Amostra de conveniência, recrutada por convite aberto a turmas de disciplinas de Eng. Software. |
| **10.6 Treinamento e preparação dos sujeitos** | Sessão inicial de 2 horas sobre o ambiente e requisitos. O grupo TDD receberá um treinamento adicional de 1 hora focado no ciclo *Red-Green-Refactor*. |

## 11. Instrumentação e protocolo operacional

| Item | Descrição |
| :--- | :--- |
| **11.1 Instrumentos de coleta** | Questionário pré-experimento (Experiência); Formulário de *Time Tracking* (M1, M10); Ferramenta SonarQube (M2, M6, M7); Roteiro de Testes de Aceitação (M3, M11); Ferramenta de Cobertura (M4); Logs de Git (M5, M8); Questionário Pós-Experimento (M9). |
| **11.2 Materiais de suporte** | Documentos de Requisitos Funcionais e Não Funcionais das 3 tarefas; Termo de Consentimento Informado; Guia Rápido do TDD (para o grupo TDD). |
| **11.3 Procedimento experimental (protocolo – visão passo a passo)** | 1. **Fase Pré-Execução e Triagem (Stakeholder: Pesquisador, Participantes)**: Recrutamento e assinatura do Termo de Consentimento (14.2). Aplicação do Questionário Pré-Experimento (Instrumento) para coleta da Experiência Prévia (Variável de Controle). 2. **Fase de Treinamento e Randomização (Stakeholder: Pesquisador)**: Sessão de 2h sobre o ambiente e requisitos. Treinamento adicional de 1h sobre TDD (10.6). Atribuição randômica da sequência de tarefas e tratamentos (TDD/TD) (9.2). 3. **Fase de Execução (3 Rodadas - *Within-Subjects*):** Para cada participante e módulo (Objeto de Estudo): O participante inicia o Formulário de *Time Tracking* (Instrumento para M1, M10) e começa o desenvolvimento seguindo o Tratamento (TDD ou TD). Ele registra o código no Git (Fonte de Dados para M5, M8). 4. **Fase de Coleta de Dados Objetivos (Stakeholder: Pesquisador)**: Após a conclusão da tarefa, o Pesquisador submete o código à Ferramenta SonarQube (Instrumento para M2, M6, M7) e à Ferramenta de Cobertura (Instrumento para M4). O Pesquisador executa o Roteiro de Testes de Aceitação, registrando Defeitos (M3) e Severidade (M11). 5. **Fase de Pós-Execução e Percepção (Stakeholder: Pesquisador, Participantes)**: Aplicação do Questionário Pós-Experimento (Instrumento para M9 - Satisfação/Percepção). Início da Limpeza de Dados e Plano de Análise Estatística (12.2) para testar as Hipóteses Formais (7.2). |
| **11.4 Plano de piloto** | Será realizado um Piloto com 5 estudantes (excluídos da amostra principal) para validar a clareza dos requisitos, o tempo médio de conclusão (para ajuste do esforço estimado), e a usabilidade dos instrumentos de coleta. |

## 12. Plano de análise de dados (pré-execução)

| Item | Descrição |
| :--- | :--- |
| **12.1 Estratégia geral de análise** | Comparação das médias das variáveis dependentes entre os tratamentos (TDD vs. TD) usando testes de medidas repetidas para responder a cada questão do GQM. |
| **12.2 Métodos estatísticos planejados** | **Teste de Hipóteses:** Análise de Variância (ANOVA) para Medidas Repetidas. Se as premissas não forem atendidas (normalidade/esfericidade), será utilizado o **Teste de Friedman** ou **Teste de Wilcoxon Signed-Rank** (não paramétricos). |
| **12.3 Tratamento de dados faltantes e outliers** | *Outliers* serão identificados via IQR; dados implausíveis (erros de registro) serão excluídos. Desistência (dados faltantes) resultará na exclusão dos dados pareados do participante. |
| **12.4 Plano de análise para dados qualitativos** | Dados da M9 e comentários serão submetidos à Análise de Conteúdo Temática para identificar padrões e categorias (ex: "dificuldade de adaptação ao TDD", "benefício na manutenibilidade"). |

## 13. Avaliação de validade (ameaças e mitigação)

| Item | Descrição |
| :--- | :--- |
| **13.1 Validade de conclusão** | *Mitigação:* Cálculo de tamanho da amostra (7.3) para garantir poder estatístico. *Mitigação:* Triangulação do Esforço (M1) com logs do Git (M5) para mitigar viés de auto-relato. |
| **13.2 Validade interna** | *Mitigação:* Contrabalanço total e randomização para mitigar Efeitos de Ordem e Maturação. Uso de tarefas equivalentes (Módulos A, B, C) para mitigar Efeito de Tarefa. |
| **13.3 Validade de constructo** | *Mitigação:* Treinamento específico (10.6) e verificação de *compliance* (via logs do Git para M5 e M8) para garantir que a prática de TDD foi aplicada corretamente. |
| **13.4 Validade externa** | *Limitação:* Amostra de conveniência (estudantes). *Mitigação:* Documentação detalhada do perfil da amostra para delimitar o escopo da generalização. |
| **13.5 Resumo das principais ameaças e estratégias de mitigação** | Ameaças críticas: Viés de Experiência e Auto-relato de Tempo. Mitigação: Desenho *Within-Subjects* e Triangulação de Dados. |

## 14. Ética, privacidade e conformidade

| Item | Descrição |
| :--- | :--- |
| **14.1 Questões éticas** | Pressão para participação (mitigada por ser voluntária); Uso de incentivos (pontos extras na disciplina) padronizados para ambos os grupos. |
| **14.2 Consentimento informado** | Todos os participantes assinarão um Termo de Consentimento detalhado, que explica a finalidade da pesquisa, os riscos mínimos e a garantia de anonimato. |
| **14.3 Privacidade e proteção de dados** | Dados de desempenho serão pseudoanonimizados (uso de IDs numéricos). Os dados serão armazenados em repositório privado com acesso restrito e descartados após 5 anos. |
| **14.4 Aprovações necessárias** | Aprovação do Comitê de Ética em Pesquisa (CEP) e aceite do Professor da disciplina. |

## 15. Recursos, infraestrutura e orçamento

| Item | Descrição |
| :--- | :--- |
| **15.1 Recursos humanos e papéis** | Pesquisador (Execução, Análise); Orientador (Supervisão Científica); Professor (Coordenação Logística). |
| **15.2 Infraestrutura técnica necessária** | Repositório Git; Servidor para ferramenta de Análise Estática (SonarQube); Ferramenta de Cobertura (JaCoCo/Coverage.py); Ambiente de desenvolvimento (IDE) padronizado. |
| **15.3 Materiais e insumos** | Formulários online de coleta de dados; Documentos de requisitos. |
| **15.4 Orçamento e custos estimados** | Custos primários em horas de dedicação do pesquisador e orientador. Não há custos diretos com licenças ou *hardware*. |

## 16. Cronograma, marcos e riscos operacionais

| Item | Descrição |
| :--- | :--- |
| **16.1 Macrocronograma** | Semanas 1-2: Preparação (Plano, Instrumentos, CEP). Semana 3: Recrutamento e Treinamento. Semanas 4-7: Execução (Coleta de Dados). Semanas 8-10: Análise e Relatório. |
| **16.2 Dependências entre atividades** | A execução (Semana 4) depende da aprovação do CEP e da conclusão do Piloto. |
| **16.3 Riscos operacionais e plano de contingência** | Risco: Desistência em massa. Contingência: Recrutamento inicial com 10% de excedente (amostra de reserva). |

## 17. Governança do experimento

| Item | Descrição |
| :--- | :--- |
| **17.1 Papéis e responsabilidades formais** | Orientador (Decisão Científica); Pesquisador (Execução Operacional); Professor (Logística e Suporte). |
| **17.2 Ritos de acompanhamento pré-execução** | Reunião semanal de 30 min com o Orientador para monitoramento do plano e revisão dos instrumentos. |
| **17.3 Processo de controle de mudanças no plano** | Qualquer alteração no escopo ou desenho deve ser registrada em um novo versionamento (v4.1, v5.0) e aprovada pelo Orientador antes de ser aplicada. |

## 18. Plano de documentação e reprodutibilidade

| Item | Descrição |
| :--- | :--- |
| **18.1 Repositórios e convenções de nomeação** | Repositório Git privado do TCC. Convenção: `EXP-TCC-TDD-001_[Artefato]_[Versão]`. |
| **18.2 Templates e artefatos padrão** | Modelos dos questionários, roteiros de testes de aceitação e Termo de Consentimento. |
| **18.3 Plano de empacotamento para replicação futura** | O repositório final incluirá: o plano de experimento, o *dataset* anonimizado e o script de análise estatística em R/Python (visando replicação futura). |

## 19. Plano de comunicação

| Item | Descrição |
| :--- | :--- |
| **19.1 Públicos e mensagens-chave pré-execução** | Participantes: Foco na confidencialidade, voluntariedade e na contribuição científica. Orientador/Professor: Status das aprovações. |
| **19.2 Canais e frequência de comunicação** | E-mail (comunicações formais, convite); Chat (dúvidas operacionais). |
| **19.3 Pontos de comunicação obrigatórios** | Aprovação do CEP; Início da execução; Conclusão da coleta de dados. |

## 20. Critérios de prontidão para execução (Definition of Ready)

| Item | Descrição |
| :--- | :--- |
| **20.1 Checklist de prontidão** | [ ] Plano de Experimento (v4.1) aprovado. [ ] Aprovação do Comitê de Ética obtida. [ ] Recrutamento da amostra mínima (24 participantes) concluído. [ ] Infraestrutura técnica configurada. [ ] Piloto realizado e ajustes incorporados. |
| **20.2 Aprovações finais para iniciar a operação** | Aceite formal do Orientador e do Professor da disciplina no checklist. |