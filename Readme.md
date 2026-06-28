# Case Processo Seletivo — Analista de Dados Produto & 

## 1 Etapa - Tratamento de dados
A base de dados estava em conjunto, mas foi realizado o download de forma separada para facilitar o manuseio dos dados e o tratamento dos mesmo, pois como o planejado o tratamento dos dados seria realizado de forma separada e no final unificados.

A base de dados 2ª não precisa de tratamento dos dados.

As bases de dados foram tratadas de forma separada visando dar maior precisão ao tratamento dos dados, e passou por outra etapa após unificação para corrigir erros e valores nulos que possam surgir.

Obs: Durante a etapa de limpeza, os valores nulos mapeados nas variáveis de perfil (32,84%) foram padronizados sob a categoria 'Não informado'. É crucial destacar na análise que esse volume expressivo não representa meros esquecimentos em perguntas isoladas, mas sim perfis de usuários não cadastrados na plataforma. Portanto, ao observar a categoria 'Não informado' nos gráficos de idade, salário ou cargo, o leitor deve interpretá-la como o comportamento do grupo de jogadores anônimos/não identificados.


- Analisar, foi informado no enuciado que o leitor tem ate 6 tentativas para acertar a palavra, mas o máximo de tentativas seguindo a base de dados é 10, no caso depois das 6 tentativas pode tentar varias outras vezes que não ira contar ou é um dado incompativel...

## 2 Etapa - Análise exploratória de dados (EDA)

No final criar uma proposta, respondendo ""O que está determinando se um usuário volta a jogar — e o que podemos fazer para aumentar isso?" e "o que você mudaria ou testaria no Palavritas na próxima semana?"
Formato: 
- **Hipótese:** "Acredito que X porque Y"
- **Ação:** proposta concreta
- **Critério de sucesso:** "Saberei que funcionou quando Z"

Buscar analisar: "Usuários que acertam mais letras nas primeiras tentativas tendem a voltar no dia seguinte?

Ou

Usuários que precisam de muitas tentativas possuem menor retenção?

Isso responde exatamente à pergunta:

O que determina se um usuário volta a jogar?

É uma análise que vai além da EDA descritiva e começa a investigar fatores associados ao comportamento do usuário."


**Pode ser uma hipotese, ação e critério de sucesso: MELHORAR**
"""
O gráfico revela que os horários de pico de acesso ao quiz ocorrem no final da noite, especificamente entre 22h e 23h, registrando o maior volume. Logo em seguida, com uma diferença visível, surge o período da manhã entre 6h, 7h e 8h, que mantém um nível de acessos equilibrado e alto. Por outro lado, o quiz registra o menor engajamento de forma disparada durante o período da tarde, estável entre 12h e 17h, onde o volume cai drasticamente.

Recomendação estratégica: Esses padrões indicam claramente quais janelas de horário devem ser priorizadas em ações de marketing e notificações para maximizar o engajamento com os usuários.

Metrica a ser acompanhada para sucesso da hipotese, para manter os usuarios jogando de forma mais constantes: 2 - A) Volume de acesso por hora...
"""

"""
A análise do ranking das 10 palavras com maior taxa de derrota revela um padrão claro: as 6 palavras mais desafiadoras para os usuários (PAZÃO, DANÇA, NIXÃO, HERÓI, ORAÇÃO e CIÚME) possuem acentos ou sinais gráficos, registrando uma taxa de derrota próxima a 80%. Essa observação é um insumo valioso de game design, pois comprova que a presença de caracteres especiais eleva drasticamente a dificuldade do jogo. 

Recomendação estratégica: Esse conhecimento pode ser utilizado estrategicamente para calibrar a dificuldade do quiz, alternando entre palavras mais simples ou mais complexas a depender do objetivo de engajamento da plataforma.

Metrica a ser acompanhada para sucesso da hipotese, para manter os usuarios jogando de forma mais constantes: 2 - C) Análise das palavras...
"""

"""
A análise da probabilidade de retorno por sequência (Streak) revela que o hábito de jogo se fortalece progressivamente até o 4º dia consecutivo, onde a chance de retorno atinge o pico estável de 30%.

Contudo, a partir do 5º dia, observa-se um aumento expressivo na volatilidade dos dados (alargamento do Intervalo de Confiança), sugerindo que manter o engajamento a longo prazo torna-se imprevisível e desafiador para o usuário.

Recomendação estratégica: Para mitigar a fadiga do hábito e evitar o desabamento da retenção observado após o 7º dia, a plataforma deve implementar gatilhos de incentivo (notificações com bônus, desafios especiais de meio de semana ou recompensas por manter o streak) focados especialmente em usuários que estão cruzando a marca do 4º e do 5º dia de jogo consecutivo.

Metrica a ser acompanhada para sucesso da hipotese, para manter os usuarios jogando de forma mais constantes: 3 - A) Engajamento vs. Performance...
"""

"""
A análise de retenção em 30 dias revela que a fidelidade á plataforma é homogênea entre as gerações, estabilizando-se entre 31% para todas as faixas etárias. Esse comportamento uniforme comprova o apelo universal do quiz. O grupo "Não informado" (jogadores anônimos) acompanha exatamente o mesmo patamar de fidelidade, confirmando que os usuários sem cadastro possuem alto valor e são tão fiéis quanto os cadastrados.

Por outro lado, quando avaliamos o comportamento por turno, há variações importantes: os usuários matutinos (Morning) são os mais fiéis, registrando a maior taxa de retenção da base com cerca de 37%, o que sugere que o jogo funciona melhor quando integrado à rotina matinal. Em contrapartida, o período da noite (Night) apresenta o menor índice de retenção, ficando em aproximadamente 29%. Esse dado traz um contraponto crucial: embora a noite registre o maior volume absoluto de acessos, ela é a menos eficiente para fidelizar a longo prazo.

Recomendação estratégica: Como a taxa de inatividade geral atinge 69%, as ações de melhoria devem focar em mecânicas globais de retenção (como sistemas de níveis, conquistas ou um modo competitivo), em vez de campanhas segmentadas por idade. Além disso, para transformar os jogadores casuais da noite em usuários recorrentes, a plataforma pode disparar notificações push logo no início do dia (ex: entre 7h e 8h), incentivando a criação de um hábito matutino saudável na base.

Metrica a ser acompanhada para sucesso da hipotese, para manter os usuarios jogando de forma mais constantes: 3 - B) Perfil de quem some...
"""

"""

"""

Pode ocorrer, probabiidade dos usuarios não cadastrados no sistema, sejam os usuarios já cadastrados, jogando o jogo de forma anonima, para não perder as chances e acertar quando for jogar de forma definitiva???


## Bonus: Dashboard

INSERIR:
💡 Dica de Ouro para o seu PortfólioPara que o Power BI não pareça apenas um gráfico isolado, inclua uma seção no seu README chamada "📊 Monitoramento Contínuo (Business Intelligence)".Lá, você pode colocar um print do dashboard e explicar:"Para que o time de operações possa acompanhar o sucesso das hipóteses propostas em tempo real, desenvolveu-se um dashboard no Power BI alimentado pela base unificada. O painel monitora oscilações diárias nas taxas de retenção e distribuições de horários."~

## Informações adicionais
Sobre o The News “notícias relevantes e imparciais, direto no seu email gratuitamente, todo dia, às 06:06”

Vale ressaltar que não tenho completa noção do funcionamento do The News, somente do que foi disponibilizado no case e do que consta no próprio site para os usuários em geral…

## K-means

INSEIR:
Com o objetivo de complementar a análise exploratória, foi aplicado o algoritmo de agrupamento K-Means. Diferentemente dos modelos supervisionados, o K-Means não busca prever um resultado específico, mas identificar grupos de usuários com características semelhantes. Essa abordagem permite compreender diferentes perfis de jogadores e apoiar estratégias de retenção e personalização.

Para complementar a Análise Exploratória de Dados (AED) e dar robustez estatística às hipóteses levantadas, aplicou-se o algoritmo de aprendizado não supervisionado **K-Means** focado em agrupar os usuários por similaridade de comportamento operacional.

Em vez de trazer novas métricas, **o modelo foi utilizado para confirmar e unificar as descobertas prévias**, provando como os fatores se correlacionam de forma integrada. O algoritmo dividiu a base em 4 perfis claros de jogadores:

*   **Cluster 0 — O Treino Oculto (13,3%):** Registra 100% de derrotas, mas possui 100% de retorno no dia seguinte e os maiores índices de dados ocultos (50,8% de renda omissa). **Confirma matematicamente** a tese de usuários jogando deslogados em guias anônimas para descobrir a palavra secreta.
*   **Cluster 1 — A Frustração Real (45,5%):** O grupo majoritário da base. Registra 100% de derrotas nas 6 tentativas e 0% de retorno imediato. **Isola o foco do Churn de 69%** da plataforma, gerado pela frustração com palavras complexas.
*   **Cluster 3 — A Alta Performance (25,3%):** Usuários de elite com 100% de vitórias rápidas (média de 2,32 tentativas) e retenção estável.
*   **Cluster 2 — O Jogador Real Competitivo (15,7%):** Perfil resiliente com equilíbrio saudável de vitórias (52%) e derrotas (48%), composto majoritariamente por lideranças corporativas seniores (Diretores e Coordenadores) que sustentam a maior retenção mensal da base (37%).

O Veredito do Modelo para o Negócio:
O cruzamento de dados dos clusters provou que as distribuições de idade, renda e sistema operacional (iOS/Android) são homogêneas entre os grupos. Isso valida que **fatores demográficos ou tecnológicos não ditam o engajamento ou o abandono do jogador**. O sucesso do produto depende estritamente da experiência psicológica do usuário diante da dificuldade do quiz, justificando os planos de ação propostos (Modo Treino, Escudo de Streak e Balanceamento Ortográfico) para blindar a saúde do ecossistema.
