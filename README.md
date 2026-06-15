# Anatomia dos Bots: Como perfis automatizados atacaram as urnas eletrônicas nas Eleições de 2022

Entre abril e outubro de 2022, redes articuladas de bots concentraram esforços para minar a credibilidade do sistema eleitoral. disseminando fakenews sobre as urnas eletrônicas. O pico de atividade ocorreu em junho, disparando narrativas infladas artificialmente por perfis com comportamento clássico de automação: altíssimo volume de postagens diárias concentrado em contas com pouquíssimos seguidores. 

A Tática de Engajamento: A análise revela que o foco não era o debate, mas o uso de técnicas de engajamento cruzado para burlar os algoritmos de recomendação da plataforma X (Twitter) e levar aos top trends conteúdos que minavam a credibilidade da urna e pediam pela auditoria por meio de voto em papel. 

## Sobre a pesquisa

Este repositório é um exercício de jornalismo e análise de dados, considerando uma base de 25.659 tweets que eu coletei entre 27 de abril e 2 de outubro de 2022, quando a rede social "X" (ex-Twitter) ainda disponibilizada uma API gratuita que permitia o streaming de postagens. 

Coletei tweets especificamente sobre "urna eletrônica", pois minha meta era avaliar a ação de perfis automatizados na disseminação de fakenews envolvendo nossa "pilili" nas polêmicas eleições passadas. 

Fiz uma análise de sentimentos, com ajuda da biblioteca "pysentimiento", criada por pesquisadores argentinos. Como ela usa modelos baseados em Transformers (como o BERTweet e o RoBERTuito), ela foi fundamental para analisar o Twitter em espanhol e português durante o período eleitoral - ao contrário de outras populares nativas em inglês. 

Após rodar o algoritmo, fiz um refinamento das classificações e criei um dataframe focado apenas nos negativos (45% do total). Para conceituar perfil de bot fui bem conservadora: perfis com postagens diárias acima de 100 tweets - considerando somente como suspeitos os que postavam mais de 50 tweets diários.

## Insights principais:

* Pico de Atividade: forte atuação em maio , mas pico absoluto no mês de junho.
* Muitos posts, poucos seguidores: o gráfico de dispersão, que expõe outllliers, revela que os perfis automatizados possuem poucos engajamentos, mas um volume de tweets por dia estratosférico (chegando a quase 6 mil em alguns casos). É o comportamento clássico de contas criadas apenas para inflar a rede.
* O baixo engajamento dos perfis automáticos indicam que o foco principal deles é enganar os algoritmos de recomendação e colocar os assuntos de uma agenda específica nos top trends - assim como colocar determinados perfis e hashtags entre os mais "falados" do dia inorganicamente.
* Os Alvos da Rede: Os gráficos mostram que a estratégia dos bots não era aleatória. O maior alvo de respostas (in_reply_to) foi o perfil oficial do TSEjusbr (esforço para minar a credibilidade do órgão), seguido de perto pelo perfil de jairbolsonaro (para gerar engajamento cruzado com a base de apoiadores) e por veículos de imprensa como JovemPanNews.
* Palavras-chave: Os termos mais utilizados nos posts negativos sobre urna eletrônica publicados por perfis automatizados remetem a fakenews, fraude, STF, TSE e Bolsonaro.

## Dashboard em Power BI:
