# 🧠 Case de Processo Seletivo – Análise de Produto & Growth | Palavritas

Este projeto consiste na resolução de um **case técnico de Processo Seletivo para Analista de Dados (Produto & Growth)**, cujo objetivo foi analisar o comportamento dos usuários do jogo **Palavritas** e responder à principal pergunta de negócio proposta pelo Head de Produto:

> **"O que está determinando se um usuário volta a jogar — e o que podemos fazer para aumentar isso?"** 

Além da análise exploratória dos dados, o case exigiu documentação completa das etapas de limpeza, investigação dos dados, geração de insights e elaboração de propostas de melhoria com hipóteses testáveis e métricas de sucesso.

---

# 🧩 Etapas Desenvolvidas

## 1. Tratamento e Diagnóstico dos Dados

A base disponibilizada era composta por diferentes arquivos contendo informações sobre sessões de jogo, tentativas realizadas pelos usuários e perfil cadastral.

Para facilitar o processo de tratamento e garantir maior controle sobre cada conjunto de dados, as bases foram inicialmente tratadas de forma independente e posteriormente integradas para realização das análises.

Durante essa etapa foram realizadas atividades como:

* Importação e validação das bases;
* Padronização dos tipos de dados;
* Identificação e tratamento de valores nulos;
* Padronização de categorias;
* Verificação de registros inconsistentes;
* Integração das bases através das chaves de relacionamento;
* Nova etapa de validação após a junção das tabelas.

### Tratamento dos valores nulos

Foi identificado que aproximadamente **32,84%** dos registros das variáveis de perfil continham valores ausentes.

Após análise do contexto do negócio, verificou-se que esses registros não representavam erros de coleta, mas sim **usuários que jogaram anonimamente, sem possuir cadastro na plataforma**.

Por esse motivo, optou-se por substituir os valores nulos pela categoria:

> **"Não informado"**

Essa decisão preserva os registros para análise e evita interpretações equivocadas dos gráficos relacionados ao perfil dos usuários.

### Diagnóstico dos dados

Durante a validação também foi identificada uma inconsistência entre a documentação do case e a base disponibilizada.

Embora o enunciado informe que o jogador possui **até seis tentativas** para acertar a palavra, foram encontrados registros contendo **até dez tentativas**, indicando uma possível divergência entre a regra do jogo descrita e os dados coletados.

Essa inconsistência foi documentada durante a análise, uma vez que poderia impactar diretamente interpretações relacionadas à dificuldade das partidas.

---

# 📊 Análise Exploratória dos Dados (EDA)

Após o tratamento das bases foi realizada uma análise exploratória completa buscando identificar fatores relacionados à retenção dos usuários e ao comportamento dentro da plataforma.

As análises contemplaram, entre outras, as seguintes dimensões:

* Volume de acessos por horário;
* Horário típico de jogo;
* Taxa de retorno dos usuários;
* Retenção em D30;
* Perfil demográfico dos jogadores;
* Cargo, setor e faixa salarial;
* Frequência de uso de aplicativos de delivery;
* Assinatura da newsletter;
* Dispositivo utilizado;
* Palavras com maior dificuldade;
* Quantidade de tentativas por partida;
* Evolução do Streak (dias consecutivos);
* Performance dos jogadores nas primeiras tentativas.

Além da análise descritiva, foram investigadas possíveis relações entre comportamento dos usuários e retenção, buscando responder quais fatores influenciam o retorno ao jogo.

---

# 📈 Principais Insights

## 📌 Horário de utilização

Foi identificado que o maior volume de acessos ocorre entre **22h e 23h**, seguido pelo período da manhã (entre **6h e 8h**).

Em contrapartida, o período da tarde apresentou o menor nível de atividade dos usuários.

Esse comportamento evidencia oportunidades para campanhas de notificações, lembretes e ações de reengajamento em horários estratégicos.

---

## 📌 Dificuldade das palavras

As palavras com maior índice de derrota apresentaram um padrão bastante consistente.

Grande parte delas continha:

* acentos;
* caracteres especiais;
* maior complexidade ortográfica.

Esse resultado sugere que a dificuldade do jogo está fortemente associada ao uso de palavras acentuadas, podendo influenciar negativamente a experiência dos usuários.

---

## 📌 Formação do hábito (Streak)

A análise demonstrou que a probabilidade de retorno aumenta progressivamente até aproximadamente o quarto dia consecutivo de utilização.

Após esse período observa-se maior volatilidade na retenção, indicando que manter o hábito torna-se significativamente mais difícil.

Esse comportamento aponta para a necessidade de mecanismos que incentivem a continuidade da sequência de dias jogados.

---

## 📌 Perfil dos usuários

Foi observado que as taxas de retenção permanecem relativamente homogêneas entre diferentes faixas etárias.

Já quando analisado o período do dia, verificou-se comportamento distinto:

* usuários que jogam pela manhã apresentam maior retenção;
* jogadores noturnos representam o maior volume absoluto de acessos, porém possuem menor fidelização.

Esse resultado demonstra que alto volume de utilização não necessariamente implica maior retenção.

---

## 📌 Usuários não cadastrados

A categoria **"Não informado"**, composta pelos usuários anônimos, apresentou comportamento semelhante ao dos usuários cadastrados em diversos indicadores.

Esse resultado levanta uma hipótese interessante:

Parte desses jogadores pode já possuir cadastro na plataforma e utilizar partidas anônimas para praticar antes de registrar oficialmente sua tentativa diária.

Embora essa hipótese não possa ser confirmada apenas com os dados disponíveis, ela representa uma oportunidade para futuras investigações.

---

# 💡 Hipóteses de Produto

## Hipótese 1

Acredito que notificações enviadas nos horários de maior propensão ao retorno aumentam a retenção diária dos usuários, pois aproveitam momentos de maior disponibilidade para jogar.

**Ação:**

Implementar campanhas de notificações push entre **6h–8h** e **21h–22h**, incentivando o retorno ao jogo.

**Critério de sucesso:**

Aumento da taxa de retorno diário e crescimento do volume de acessos nesses períodos.

---

## Hipótese 2

Acredito que palavras excessivamente difíceis reduzem a retenção porque geram frustração nas primeiras experiências do usuário.

**Ação:**

Criar um sistema de balanceamento da dificuldade das palavras, alternando desafios simples e complexos ao longo da semana.

**Critério de sucesso:**

Redução da taxa de derrotas nas palavras críticas sem diminuição do tempo médio de permanência.

---

## Hipótese 3

Acredito que usuários que atingem quatro dias consecutivos de jogo apresentam maior potencial de fidelização, sendo esse o momento ideal para incentivar a continuidade do hábito.

**Ação:**

Criar recompensas por streak, conquistas, desafios semanais ou bônus específicos entre o quarto e o quinto dia consecutivo.

**Critério de sucesso:**

Aumento da retenção após o quinto dia e crescimento da duração média das sequências de jogo.

---

## Hipótese 4

Acredito que jogadores que identificam corretamente mais letras nas primeiras tentativas possuem maior probabilidade de retornar no dia seguinte, enquanto usuários que necessitam muitas tentativas tendem a abandonar o jogo com maior frequência.

**Ação:**

Investigar a relação entre desempenho inicial e retenção e, caso confirmada, implementar mecanismos adaptativos, como dicas progressivas ou redução temporária da dificuldade para jogadores com baixo desempenho.

**Critério de sucesso:**

Redução da taxa de abandono entre usuários com muitas tentativas e aumento da retenção no dia seguinte.

---

# 📊 Bônus – Dashboard de Business Intelligence (Power BI)

Além das análises **desenvolvidas em Python**, foi construído um dashboard interativo no Power BI com o objetivo de transformar os principais indicadores em uma ferramenta de monitoramento contínuo para equipes de Produto e Growth.

O painel foi desenvolvido a partir da base consolidada e permite acompanhar, de forma visual e dinâmica, métricas relacionadas ao comportamento dos usuários, retenção e engajamento ao longo do tempo.

### Funcionalidades do Dashboard
- Monitoramento diário da retenção de usuários;
- Distribuição dos acessos por horário;
- Evolução das partidas realizadas;
- Indicadores de desempenho das hipóteses propostas;
- Acompanhamento dos principais KPIs de Produto.

    `Objetivo: Demonstrar como as análises desenvolvidas poderiam ser incorporadas ao dia a dia da equipe, permitindo acompanhar continuamente o impacto das ações implementadas e apoiar decisões baseadas em dados.`

(Inserir print do dashboard nesta seção.)
---

# 🤖 Bônus – Segmentação de Usuários com Machine Learning (K-Means)

Com o objetivo de complementar a Análise Exploratória de Dados (EDA) e aumentar a robustez das conclusões, foi aplicado o algoritmo de **Machine Learning não supervisionado K-Means.**

Diferentemente de modelos supervisionados, o K-Means não busca prever um resultado específico, mas identificar grupos naturais de usuários com comportamentos semelhantes.

Neste projeto, o algoritmo foi utilizado para **validar estatisticamente** as hipóteses levantadas durante a análise exploratória, identificando padrões consistentes de comportamento entre diferentes perfis de jogadores.

#### Perfis identificados
**Cluster 0 — Treino Oculto (13,3%)**
- 100% de derrotas;
- 100% de retorno no dia seguinte;
- maior concentração de usuários sem cadastro.

Os resultados reforçam a hipótese de que parte desses usuários realiza partidas anônimas para descobrir a palavra antes da tentativa oficial.

---

**Cluster 1 — Frustração Real (45,5%)** \
Maior grupo identificado pelo algoritmo.

Características:
- elevada taxa de derrotas;
- baixa retenção;
- principal responsável pelo churn observado na plataforma.

Esse cluster confirmou estatisticamente que a dificuldade excessiva das palavras representa um dos principais fatores associados ao abandono.

---

**Cluster 2 — Jogador Competitivo (15,7%)** \
Perfil resiliente, composto principalmente por usuários corporativos em cargos de liderança.

Características:
- equilíbrio entre vitórias e derrotas;
- maior retenção mensal;
- comportamento consistente ao longo do tempo.

---

**Cluster 3 — Alta Performance (25,3%)** \
Grupo composto por jogadores altamente eficientes.

Características:
- elevada taxa de acertos;
- poucas tentativas por partida;
- retenção estável.

---

### Validação das Hipóteses
A utilização do K-Means permitiu confirmar que diversas hipóteses levantadas na EDA permaneciam consistentes quando analisadas de forma multivariada.

O modelo demonstrou que:
- idade apresenta distribuição semelhante entre todos os grupos;
- renda possui comportamento homogêneo entre os clusters;
- sistema operacional (Android/iOS) não influencia o comportamento dos usuários;
- o engajamento é explicado principalmente pelo comportamento durante o jogo, e não por características demográficas.

Esses resultados forneceram maior embasamento estatístico para as recomendações propostas ao longo do case.

---

### 🔄 Atualização dos Insights

Algumas conclusões inicialmente levantadas durante a EDA foram posteriormente confirmadas pela segmentação via Machine Learning.

### 📌 Dificuldade das palavras

A EDA indicava que palavras contendo acentos e caracteres especiais apresentavam maior taxa de derrota.

A segmentação realizada pelo K-Means confirmou esse comportamento ao identificar um cluster composto predominantemente por usuários frustrados, reforçando que o nível de dificuldade influencia diretamente a retenção dos jogadores.

---

### 📌 Perfil dos usuários

Inicialmente observou-se pouca diferença entre idade, renda e dispositivo utilizado.

Após a aplicação do K-Means, verificou-se que essas variáveis realmente não são determinantes para explicar o comportamento dos usuários, validando estatisticamente que o engajamento está relacionado principalmente à experiência proporcionada pelo jogo.

---

### 📌 Usuários não cadastrados

Durante a EDA foi levantada a hipótese de que parte dos usuários anônimos pudesse utilizar partidas sem login como forma de treinamento.

O Cluster 0 apresentou exatamente esse padrão de comportamento, oferecendo evidências quantitativas que fortalecem essa hipótese e justificam investigações futuras por parte da equipe de Produto.

---

# 📊 Ferramentas Utilizadas

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* K-Means
* Power BI
* Jupyter Notebook

---

# 🎯 Competências Demonstradas

* Data cleaning
* Data wrangling
* Integração de bases
* Análise exploratória de dados (EDA)
* Storytelling com dados
* Product analytics
* Growth analytics
* Machine learning não supervisionado
* Clusterização com K-Means
* Business intelligence
* Desenvolvimento de dashboards
* Formulação e validação de hipóteses
* Comunicação de insights para stakeholders

---

# ℹ️ Informações adicionais

Este projeto foi desenvolvido a partir de um **case técnico de processo seletivo**, utilizando exclusivamente as informações disponibilizadas no material da avaliação e informações públicas presentes no site do **The News**.

Dessa forma, todas as análises, hipóteses e recomendações foram elaboradas considerando apenas os dados fornecidos, sem conhecimento interno sobre o funcionamento da plataforma ou acesso às regras de negócio utilizadas pela empresa.

---

# ✅ Conclusão

O projeto demonstra a aplicação prática da análise de dados em um contexto real de **Produto & Growth**, contemplando desde o tratamento e integração das bases até a construção de hipóteses de negócio baseadas em evidências.

Além da Análise Exploratória de Dados (EDA), foram desenvolvidos um **dashboard interativo em Power BI** para monitoramento contínuo dos principais indicadores e uma **segmentação de usuários utilizando Machine Learning (K-Means)**, que permitiu validar estatisticamente as hipóteses levantadas durante a análise.

A combinação entre tratamento de dados, visualização, inteligência de negócios e aprendizado de máquina proporcionou uma compreensão mais profunda do comportamento dos usuários, transformando dados em recomendações estratégicas para aumentar a retenção, melhorar a experiência do jogador e apoiar a tomada de decisão orientada por dados.