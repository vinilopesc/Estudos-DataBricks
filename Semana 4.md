# Relatório de Estudos – Semana 4

## Dia 16
No início da quarta semana, mudei o foco para a construção de pipelines de produção, onde a confiabilidade e a automação se tornam cruciais. Passei a manhã entendendo conceitos de DevOps aplicados a dados e notei que, nesse contexto, não basta desenvolver o pipeline: é preciso garantir que ele possa ser facilmente versionado, testado e monitorado. Tudo isso me fez ver que a engenharia de dados tem muito a ganhar ao incorporar práticas de desenvolvimento de software mais consolidadas.

Durante a tarde, aprofundei o uso da API de Jobs do Databricks para agendar processos ETL. Com isso, pude definir rotinas que rodam periodicamente ou em resposta a determinados eventos, sem depender de scripts externos ou tarefas manuais. Essa automação facilita muito a vida de quem mantém pipelines em produção, pois reduz o risco de erros humanos e melhora a previsibilidade dos processos.

## Dia 17
No dia seguinte, foquei em orquestração de tarefas com Apache Airflow. Aprendi a criar DAGs (Directed Acyclic Graphs) que descrevem dependências e ordem de execução das tarefas, organizando melhor os pipelines, principalmente quando envolvem múltiplas etapas interdependentes. Entendi que esse nível de controle é fundamental em cenários empresariais complexos, onde uma tarefa só pode começar quando outra termina com sucesso.

À tarde, me aprofundei nas práticas de monitoramento e logging. Vi como o Databricks e outras ferramentas (como a ELK Stack) conseguem captar logs, métricas de uso e informações de performance em tempo real. Essa camada de visibilidade me mostrou que não basta o pipeline funcionar: é preciso ter clareza sobre o que está acontecendo “por dentro” para conseguir identificar gargalos, prever problemas e corrigir incidentes rapidamente.

## Dia 18
No terceiro dia, passei a manhã entendendo como funcionam pipelines de Integração Contínua e Deploy (CI/CD) para projetos de dados. Notei que o uso de Git e ferramentas de automação (GitLab CI, GitHub Actions, Jenkins) se torna essencial para garantir que cada mudança no código seja testada e validada. Descobri que há também boas práticas para versionar esquemas de dados ou garantir que mudanças bruscas não quebrem o pipeline no meio do caminho.

Durante a tarde, refleti sobre melhores práticas em produção, especialmente relacionadas à escalabilidade e manutenção de longo prazo. Ficou nítido que prever o crescimento dos dados e implementar estratégias de autoscaling é uma forma de evitar problemas futuros, pois o volume de dados tende a aumentar a cada dia. Também aprendi que manter scripts de manutenção e planejamento de custos evita surpresas na conta do provedor de nuvem e garante a longevidade do projeto.

## Dia 19
No penúltimo dia, mergulhei nos temas de governança de dados, que englobam políticas de compliance, privacidade e segurança da informação. Sempre ouvi falar em LGPD e GDPR, mas percebi que, na prática, isso exige uma série de cuidados na hora de coletar, armazenar e processar dados. Durante a manhã, estudei como mapear dados sensíveis, criar trilhas de auditoria e estabelecer controles de acesso, entendendo que cada usuário ou grupo deve ter permissões adequadas ao seu perfil.

À tarde, explorei os recursos de governança disponíveis no Databricks. Descobri que a plataforma conta com catálogos de dados e ferramentas para gerenciar metadados, o que facilita a descoberta de datasets por diferentes áreas da empresa. Além disso, ajuda a garantir que cada conjunto de dados esteja devidamente documentado, minimizando riscos de uso indevido ou interpretações errôneas.

## Dia 20
No último dia, concluí a parte de governança aprofundando-me na implementação de políticas de segurança e controle de acesso. Foi interessante ver como o Databricks permite configurar regras em nível de cluster, notebook e job, dando bastante granularidade às permissões. Também aprendi a gerar logs de auditoria para rastrear quem acessou quais dados, algo fundamental para atender regulações de conformidade.

Na parte da tarde, fiz uma revisão geral de tudo e aproveitei para realizar três simulados contendo 45 questões cada. Obtive acertos de 32, 38 e 30, nessa ordem, o que me ajudou a ver onde já estou bem seguro (principalmente nos tópicos de ETL e otimização de consultas) e onde ainda preciso reforçar os estudos (alguns detalhes de governança e streaming contínuo). Essa avaliação final me deu uma boa visão do que devo revisar, mas também me deixou satisfeito com o progresso alcançado ao longo dessas quatro semanas intensas de estudo.
