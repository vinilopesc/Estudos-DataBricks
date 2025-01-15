# Relatório de Estudos – Semana 3

## Dia 11
Quando iniciei a semana 3, decidi revisar alguns conceitos avançados de ETL para ter certeza de que não tinha deixado nada passar. Comecei a manhã repassando transformações complexas, como normalização e desnormalização de tabelas, e notei como isso afeta a maneira de armazenar dados no Hadoop ou em data lakes. Também explorei a criação de UDFs (User-Defined Functions), reconhecendo que elas permitem aplicar regras de negócio muito específicas diretamente no Spark, sem a necessidade de ferramentas externas. Esse tipo de flexibilidade é uma das razões pelas quais o Spark se destaca.

Durante a tarde, resolvi problemas práticos inspirados em desafios reais, por exemplo, corrigir valores ausentes, lidar com schemas que mudam de forma imprevisível e trabalhar com dados corrompidos. Foi gratificante ver como o Spark lida bem com essas dificuldades quando o pipeline é bem arquitetado. Depois de resolver esses problemas, senti que tinha uma visão mais clara de como planejar processos de ETL robustos, que não “quebram” tão facilmente ao encontrar dados fora do padrão.

## Dia 12
No segundo dia da semana, mergulhei no tema de Processamento Incremental. Foi aqui que entendi a importância de processar dados em pequenos lotes (micro-batches) ou até em modo contínuo, em vez de ficar esperando grandes lotes se acumularem. Isso permite que empresas que precisam de informações em tempo quase real (como sistemas de detecção de fraudes ou monitoramento de sensores) possam reagir rapidamente a eventos.

À tarde, coloquei a teoria em prática usando o Delta Lake. Achei fascinante como ele traz a capacidade de versionar dados e garantir propriedades ACID (atomicidade, consistência, isolamento e durabilidade) em cima de um data lake. Percebi também que a possibilidade de criar tabelas incrementais aliadas a um histórico de versões amplia muito a confiabilidade do sistema. Fazer rollback de dados ou analisar instantâneos históricos é mais simples, o que dá mais segurança para quem desenvolve pipelines críticos.

## Dia 13
No terceiro dia, dediquei a manhã ao Streaming Estruturado do Spark. Aqui, compreendi como o Spark abstrai a ideia de fluxo de dados contínuo, permitindo que a gente escreva operações em DataFrames que são, na verdade, atualizados em tempo real. Essa abordagem simplifica muito o código quando comparada a modelos de streaming mais antigos (como o DStreams), pois mantém a interface com DataFrames de maneira unificada.

À tarde, estudei como gerenciar o estado nos streams. Descobri que quando preciso fazer agregações contínuas (por exemplo, a contagem de cliques por usuário em janelas de tempo), o Spark mantém um estado que evolui com cada novo lote de dados. Essa parte requer bastante cautela, pois se o estado ficar muito grande, a aplicação pode consumir muitos recursos. Entretanto, essa funcionalidade dá um poder incrível para criar aplicações que exigem análises “on the fly” de eventos, ainda mais quando pensamos em detecção de anomalias ou contagem de sessões de usuários.

## Dia 14
No dia seguinte, aprofundei o estudo nas operações de janela (windowing). A grande sacada aqui foi perceber como o Spark Structured Streaming pode agrupar eventos que ocorrem dentro de intervalos de tempo, sejam fixos, deslizantes ou baseados em sessões. Assim, se eu quiser encontrar a quantidade de pedidos realizados a cada minuto ou a cada cinco minutos, por exemplo, já tenho uma API pronta para isso. Com esse conhecimento, vejo a utilidade em aplicações de monitoramento, seja na área de e-commerce, IoT ou análise de redes sociais.

Durante a tarde, compreendi melhor a tolerância a falhas do Spark, especialmente no contexto de streaming. Aprendi que o checkpointing salva periodicamente o progresso do stream e permite retomar o processamento exatamente do ponto em que parou caso ocorra alguma pane, garantindo que não haja perda nem duplicação de dados. Essa robustez de design me mostrou por que o Spark é tão adotado em soluções de missão crítica.

## Dia 15
No quinto dia, foquei na integração com sistemas de mensagens como Kafka e Kinesis, que são as principais fontes de dados em tempo real em muitos cenários corporativos. Conectei o Spark Structured Streaming a um tópico de Kafka para consumir mensagens e enviar resultados para um banco SQL, por exemplo. Percebi como a configuração de offsets e a definição de partições são importantes para controlar a performance e garantir que o sistema continue escalando sem problemas.

À tarde, uni todos esses conceitos na construção de um pipeline completo que ia desde a ingestão de dados em tempo real até a aplicação de algumas transformações e a gravação dos resultados em um destino final. Senti que foi o ponto alto da semana, pois consegui visualizar claramente como funcionaria uma arquitetura de processamento contínuo no mundo real. Essa compreensão me animou a pensar em diversas soluções que, antes, pareciam complexas demais para serem implementadas.

