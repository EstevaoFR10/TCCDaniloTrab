# Plano de Experimento – Avaliação TDD vs. Desenvolvimento Tradicional

## 1. Identificação básica

| Item | Descrição |
| :--- | :--- |
| **1.1 Título do experimento** | Avaliação do Impacto do Desenvolvimento Orientado a Testes (TDD) na Qualidade de Código e Esforço de Desenvolvimento. |
| **1.2 ID / código** | EXP-TCC-TDD-001 |
| **1.3 Versão do documento e histórico de revisão** | v1.0 (Criação inicial) |
| **1.4 Datas (criação, última atualização)** | Criação: 18/11/2025 | Última Atualização: 18/11/2025 |
| **1.5 Autores (nome, área, contato)** | Estêvão de Faria Rodrigues, Engenharia de Software, efrodrigues@sga.pucminas.br |
| **1.6 Responsável principal (PI / dono do experimento)** | Danilo de Quadros Maia Filho |
| **1.7 Projeto / produto / iniciativa relacionada** | Projeto de Trabalho de Conclusão de Curso (TCC) em Engenharia de Software. |

## 2. Contexto e problema

| Item | Descrição |
| :--- | :--- |
| **2.1 Descrição do problema / oportunidade** | Existe uma divergência na literatura empírica sobre o *trade-off* entre o custo de adoção do TDD (esforço) e o benefício gerado (qualidade). Busca-se quantificar se a melhora na qualidade do código (menos defeitos e complexidade) justifica o eventual aumento no tempo de desenvolvimento em um ambiente controlado. |
| **2.2 Contexto organizacional e técnico** | Contexto acadêmico. Participantes são estudantes de Engenharia de Software com experiência intermediária em POO e testes unitários. Desenvolvimento em linguagem Java, utilizando Git/GitHub para versionamento e IDEs padronizadas. |
| **2.3 Trabalhos e evidências prévias** | Estudos de Nagappan et al. (Microsoft) indicam que o TDD reduz a densidade de defeitos. Outras metanálises mostram resultados mistos sobre o esforço de desenvolvimento. O experimento buscará replicar e refinar as medições de esforço e complexidade. |
| **2.4 Referencial teórico e empírico essencial** | Test-Driven Development (TDD): ciclo Red-Green-Refactor; Métricas de Qualidade (Complexidade Ciclomática e Cobertura de Testes); Medição de Esforço (Time Tracking). |

## 3. Objetivos e questões (Goal / Question / Metric)

| Item | Descrição |
| :--- | :--- |
| **3.1 Objetivo geral (Goal template)** | Analisar o efeito da utilização da técnica de Desenvolvimento Orientado a Testes (TDD), com o propósito de quantificar o impacto na qualidade do código e no esforço de desenvolvimento, a partir da perspectiva do pesquisador/aluno e da organização (custo), no contexto de desenvolvimento de funcionalidades de software de complexidade média por estudantes de Engenharia de Software. |
| **3.2 Objetivos específicos** | **O1:** Comparar a complexidade do código (M1) entre grupos TDD e Tradicional. **O2:** Comparar a densidade de defeitos (M2) entre os grupos. **O3:** Medir a diferença no esforço (M3) para completar as tarefas. |
| **3.3 Questões de pesquisa / de negócio** | **Q1:** A adoção do TDD resulta em um código de menor Complexidade Ciclomática? **Q2:** Os desenvolvedores que utilizam TDD introduzem significativamente menos defeitos? **Q3:** O tempo total gasto com TDD é significativamente diferente do desenvolvimento tradicional? |
| **3.4 Métricas associadas (GQM)** | **M1 (Qualidade):** Complexidade Ciclomática média por método (Unidade: Número inteiro, Fonte: SonarQube). **M2 (Qualidade):** Densidade de Defeitos (Defeitos por KLOC) (Unidade: Defeitos/KLOC, Fonte: Logs da fase de Testes de Aceitação). **M3 (Esforço):** Tempo Total de Desenvolvimento (Unidade: Horas, Fonte: Time tracking individual e logs do Git). |

## 4. Escopo e contexto do experimento

| Item | Descrição |
| :--- | :--- |
| **4.1 Escopo funcional / de processo** | **Incluído:** Desenvolvimento de três módulos de complexidade média, medição de esforço e coleta de métricas de qualidade. **Excluído:** Fases de Requisitos (o requisito será fornecido), *deploy* em produção e manutenção. |
| **4.2 Contexto do estudo** | Tipo: Acadêmico (laboratório de estudantes). Projeto: Funcionalidades CRUD simples/médias. Perfil de Experiência: Estudantes com conhecimento intermediário. |
| **4.3 Premissas** | Proficiência equivalente na linguagem de programação; Ambiente de desenvolvimento estável e padronizado; Requisitos funcionais claros e não ambíguos. |
| **4.4 Restrições** | Duração máxima de 4 semanas para a execução; Orçamento zero para licenças de software; Dependência de uma amostra de conveniência (estudantes). |
| **4.5 Limitações previstas** | Validade Externa limitada, pois a amostra é composta por estudantes (não profissionais industriais). Possível viés de auto-relato no tempo de desenvolvimento (M3). |

## 5. Stakeholders e impacto esperado

| Item | Descrição |
| :--- | :--- |
| **5.1 Stakeholders principais** | Pesquisador/Aluno, Orientador, Professores da área de Software. |
| **5.2 Interesses e expectativas dos stakeholders** | Gerar conhecimento científico válido (TCC/publicação); Obter evidências para subsidiar a decisão sobre a inclusão/ênfase do TDD no currículo. |
| **5.3 Impactos potenciais no processo / produto** | O código produzido é de descarte. O único impacto é o tempo alocado pelos participantes na execução das tarefas (estimado e controlado no cronograma). |

## 6. Riscos de alto nível, premissas e critérios de sucesso

| Item | Descrição |
| :--- | :--- |
| **6.1 Riscos de alto nível** | R1: Viés de treinamento (participantes TDD já têm mais experiência). R2: Desistência de participantes. R3: Falha na coleta automática de métricas. |
| **6.2 Critérios de sucesso globais (go / no-go)** | Coleta completa e consistente de dados de pelo menos 80% das tarefas; Capacidade de realizar o teste de hipóteses com poder estatístico $\geq 0.80$. |
| **6.3 Critérios de parada antecipada (pré-execução)** | Não atingir o número mínimo de 20 participantes recrutados após o período de treinamento; Reprovação do plano pelo Comitê de Ética. |

## 7. Modelo conceitual e hipóteses

| Item | Descrição |
| :--- | :--- |
| **7.1 Modelo conceitual do experimento** | A **Técnica de Desenvolvimento** (Fator Independente: TDD vs. Tradicional) é a variável manipulada, que se espera influenciar as **Variáveis Dependentes** (Qualidade e Esforço). O desenho cruzado mitiga o impacto das diferenças de habilidade individual. |
| **7.2 Hipóteses formais (H0, H1)** | **H0 (Nula):** Não há diferença significativa entre TDD e o desenvolvimento tradicional nas médias de Complexidade Ciclomática ($\mu_{TDD} = \mu_{TD}$), Densidade de Defeitos ($\mu_{TDD} = \mu_{TD}$) e Esforço ($\mu_{TDD} = \mu_{TD}$). **H1 (Alternativa):** O TDD resulta em códigos com Complexidade Ciclomática e Densidade de Defeitos significativamente menores, e em Esforço significativamente maior ($\mu_{TDD} < \mu_{TD}$ para qualidade; $\mu_{TDD} > \mu_{TD}$ para esforço). |
| **7.3 Nível de significância e considerações de poder** | **Nível de significância:** $\alpha = 0,05$. O **poder estatístico** será calculado previamente (Análise de Poder) para garantir que o tamanho da amostra (10.4) seja suficiente para detectar um efeito de tamanho médio (Cohen's d = 0.5) com $1-\beta \geq 0.80$. |

## 8. Variáveis, fatores, tratamentos e objetos de estudo

| Item | Descrição |
| :--- | :--- |
| **8.1 Objetos de estudo** | Três tarefas de desenvolvimento de software (Módulos A, B, C), de complexidade funcional controlada e equivalente. |
| **8.2 Sujeitos / participantes (visão geral)** | Estudantes de Engenharia de Software (semiprofissionais). |
| **8.3 Variáveis independentes (fatores) e seus níveis** | **Fator:** Técnica de Desenvolvimento. **Níveis:** (1) TDD (Desenvolvimento Orientado a Testes); (2) TD (Desenvolvimento Tradicional). |
| **8.4 Tratamentos (condições experimentais)** | **Tratamento TDD:** Obrigatório seguir o ciclo *Red-Green-Refactor*. **Tratamento TD:** Não há restrição sobre a ordem de escrita de código/testes. |
| **8.5 Variáveis dependentes (respostas)** | Complexidade Ciclomática (M1), Densidade de Defeitos (M2), Tempo Total de Desenvolvimento (M3). |
| **8.6 Variáveis de controle / bloqueio** | Linguagem de programação (Java), Ambiente de Desenvolvimento (IDE padronizada), e Experiência Prévia em Programação (será medida e usada como covariável). |
| **8.7 Possíveis variáveis de confusão conhecidas** | Diferenças na motivação individual e a ordem de execução das tarefas (abordada pelo contrabalanço). |

## 9. Desenho experimental

| Item | Descrição |
| :--- | :--- |
| **9.1 Tipo de desenho** | **Desenho de Sujeitos por Bloco Cruzado Incompleto** (*Within-Subjects Design*). Justificativa: Cada sujeito atua como seu próprio controle, reduzindo o impacto da variabilidade de habilidade individual (validez interna). |
| **9.2 Randomização e alocação** | Randomização da ordem das tarefas e da sequência de tratamento (ex: TDD, TD, TDD) para cada participante, feita por sorteio simples. |
| **9.3 Balanceamento e contrabalanço** | Contrabalanço total: Todos os participantes experimentam ambos os tratamentos em tarefas diferentes, minimizando o efeito de ordem ou aprendizado ao longo do tempo. |
| **9.4 Número de grupos e sessões** | 1 Grupo de participantes. 1 Sessão de Treinamento e 3 Sessões de Execução (uma para cada tarefa/tratamento). |
| **9.5 [Imagem do diagrama de design cruzado]** |  |

## 10. População, sujeitos e amostragem

| Item | Descrição |
| :--- | :--- |
| **10.1 População-alvo** | Desenvolvedores de software com perfil de experiência intermediária (2-5 anos de prática). |
| **10.2 Critérios de inclusão de sujeitos** | Ser estudante a partir do 4º período de Eng. Software; Ter realizado a disciplina de Testes de Software; Ter disponibilidade de 10 horas/semana por 4 semanas. |
| **10.3 Critérios de exclusão de sujeitos** | Falta de proficiência na linguagem de programação; Conflito de interesses (ex: ser desenvolvedor senior na empresa parceira). |
| **10.4 Tamanho da amostra planejado (por grupo)** | Total de 24 participantes. Este número é uma meta que será confirmada pelo cálculo de Poder (7.3) para garantir robustez estatística. |
| **10.5 Método de seleção / recrutamento** | Amostra de conveniência, recrutada por convite aberto a turmas de disciplinas de Eng. Software. |
| **10.6 Treinamento e preparação dos sujeitos** | Sessão inicial de 2 horas sobre o ambiente de desenvolvimento e os requisitos. O grupo TDD receberá um treinamento adicional de 1 hora focado no ciclo *Red-Green-Refactor*. |

## 11. Instrumentação e protocolo operacional

| Item | Descrição |
| :--- | :--- |
| **11.1 Instrumentos de coleta** | Questionário pré-experimento; Formulário de *Time Tracking* (planilha/online); Ferramenta SonarQube (para M1); Roteiro de Testes de Aceitação (para M2); Logs de Git (para M3 e validação). |
| **11.2 Materiais de suporte** | Documentos de Requisitos Funcionais e Não Funcionais das 3 tarefas; Termo de Consentimento Informado; Guia Rápido do TDD (para o grupo TDD). |
| **11.3 Procedimento experimental (protocolo – visão passo a passo)** | 1. Recrutamento e Consentimento. 2. Questionário pré-experimento. 3. Treinamento. 4. Distribuição das credenciais e ordem de execução (randomizada). 5. Execução (3 rodadas, uma para cada tarefa/tratamento) com registro de tempo. 6. Coleta final do código e execução dos Testes de Aceitação. |
| **11.4 Plano de piloto** | Será realizado um Piloto com 5 estudantes (excluídos da amostra principal) para validar a clareza dos requisitos, o tempo médio de conclusão (para ajuste do esforço estimado), e a usabilidade dos instrumentos de coleta (Time Tracking e SonarQube). |

## 12. Plano de análise de dados (pré-execução)

| Item | Descrição |
| :--- | :--- |
| **12.1 Estratégia geral de análise** | Comparação das médias das variáveis dependentes (M1, M2, M3) entre os grupos TDD e TD, utilizando testes estatísticos que consideram o desenho de medidas repetidas (*within-subjects*). |
| **12.2 Métodos estatísticos planejados** | **Teste de Hipóteses:** Análise de Variância (ANOVA) para Medidas Repetidas, ou, caso as premissas (normalidade/homocedasticidade) não sejam atendidas, o **Teste de Wilcoxon Signed-Rank** (não paramétrico) para as variáveis dependentes. |
| **12.3 Tratamento de dados faltantes e outliers** | *Outliers* serão identificados via IQR; dados implausíveis (erros de registro) serão excluídos. Dados faltantes (desistência) resultarão na exclusão dos dados pareados do participante. |
| **12.4 Plano de análise para dados qualitativos** | Comentários e observações dos participantes serão submetidos à Análise de Conteúdo Temática para identificar padrões e categorias (ex: "dificuldade de adaptação ao TDD", "clareza do requisito"). |

## 13. Avaliação de validade (ameaças e mitigação)

| Item | Descrição |
| :--- | :--- |
| **13.1 Validade de conclusão** | *Ameaça:* Baixo poder estatístico. *Mitigação:* Cálculo de tamanho da amostra (7.3). *Ameaça:* Viés de Medida (do auto-relato do tempo). *Mitigação:* Triangulação com logs do Git. |
| **13.2 Validade interna** | *Ameaça:* Efeito de História (eventos externos). *Mitigação:* Contrabalanço do tratamento e execução em período de tempo concentrado. *Ameaça:* Efeito de Ordem. *Mitigação:* Randomização e Desenho Cruzado. |
| **13.3 Validade de constructo** | *Ameaça:* Ambiguidade na definição de "TDD". *Mitigação:* Treinamento específico (10.6) e verificação de *compliance* via questionário pós-execução. |
| **13.4 Validade externa** | *Ameaça:* Amostra de conveniência (estudantes). *Mitigação:* Documentação detalhada do perfil da amostra para delimitar o escopo da generalização (validez analítica). |
| **13.5 Resumo das principais ameaças e estratégias de mitigação** | Ameaças críticas: Viés de Experiência e Auto-relato de Tempo. Mitigação: Desenho *Within-Subjects* e Triangulação de Dados. |

## 14. Ética, privacidade e conformidade

| Item | Descrição |
| :--- | :--- |
| **14.1 Questões éticas** | Pressão para participação (mitigada por ser voluntária); Uso de incentivos (pontos extras na disciplina) padronizados para ambos os grupos. |
| **14.2 Consentimento informado** | Todos os participantes assinarão um Termo de Consentimento detalhado, que explica a finalidade da pesquisa, os riscos mínimos e a garantia de anonimato. |
| **14.3 Privacidade e proteção de dados** | Dados de desempenho (código e métricas) serão pseudoanonimizados (uso de IDs numéricos). Os dados serão armazenados em repositório privado com acesso restrito. |
| **14.4 Aprovações necessárias** | Aprovação do Comitê de Ética em Pesquisa (CEP) e aceite do Professor da disciplina. |

## 15. Recursos, infraestrutura e orçamento

| Item | Descrição |
| :--- | :--- |
| **15.1 Recursos humanos e papéis** | Pesquisador (Execução, Análise); Orientador (Supervisão Científica); Professor (Coordenação Logística). |
| **15.2 Infraestrutura técnica necessária** | Repositório Git; Servidor para ferramenta de Análise de Código (SonarQube); Ambiente de desenvolvimento (IDE) padronizado. |
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
| **17.3 Processo de controle de mudanças no plano** | Qualquer alteração no escopo ou desenho deve ser registrada em um novo versionamento (v1.1, v2.0) e aprovada pelo Orientador antes de ser aplicada. |

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
| **20.1 Checklist de prontidão** | [X] Plano de Experimento (v1.0) aprovado. [ ] Aprovação do Comitê de Ética obtida. [ ] Recrutamento da amostra mínima (20 participantes) concluído. [ ] Infraestrutura técnica configurada. [ ] Piloto realizado e ajustes incorporados. |
| **20.2 Aprovações finais para iniciar a operação** | Aceite formal do Orientador e do Professor da disciplina no checklist. |