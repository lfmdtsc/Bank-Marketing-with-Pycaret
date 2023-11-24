# Bank-Marketing-with-Pycaret

Esse banco de dados relaciona pouco mais de 40 mil clientes de um banco Português com uma variável target ('y'), onde y é yes ou no caso o cliente tenha subscrevido um depósito a prazo ou não.

A idéia fundamental por tráz desse modelo é desenvolver uma machine learn, com a utilização do Pycaret, onde possamos prever se determinados clientes finalizaram um depósito a prazo ou não após uma campanha de marketing. Esse estudo é de grande valia pois pode direcionar os esforços das instituições bancárias em determinadas idades, tipos de empregos, variáveis sociais dos clientes, minizando o custo de implementação de uma campanha robusta de marketing, trazendo resultados mais rapidamente e de forma inteligente.

Solicitação de citação: Este conjunto de dados está disponível publicamente para pesquisa. Os detalhes estão descritos em [Moro et al., 2014]. Por favor inclua esta citação se você planeja usar este banco de dados:
[Moro et al., 2014] S. Moro, P. Cortez and P. Rita. A Data-Driven Approach to Predict the Success of Bank Telemarketing. Decision Support Systems, In press, http://dx.doi.org/10.1016/j.dss.2014.03.001

Available at: [pdf] http://dx.doi.org/10.1016/j.dss.2014.03.001 [bib] http://www3.dsi.uminho.pt/pcortez/bib/2014-dss.txt

Título: Bank Marketing (with social/economic context)
Fontes:
Criado por: Sérgio Moro (ISCTE-IUL), Paulo Cortez (Univ. Minho) and Paulo Rita (ISCTE-IUL) @ 2014

Uso anterior:
O conjunto de dados completo (bank-additional-full.csv) foi descrito e analisado em:
S. Moro, P. Cortez and P. Rita. A Data-Driven Approach to Predict the Success of Bank Telemarketing. Decision Support Systems (2014), doi:10.1016/j.dss.2014.03.001.

Informações Relevantes:
Este conjunto de dados é baseado no conjunto de dados UCI "Bank Marketing" (verifique a descrição em: http://archive.ics.uci.edu/ml/datasets/Bank+Marketing).
Os dados são enriquecidos pela adição de cinco novas características/atributos sociais e económicos (indicadores nacionais de um país com cerca de 10 milhões de habitantes), publicados pelo Banco de Portugal e disponíveis publicamente em: https://www.bportugal.pt/estatisticasweb.
Este conjunto de dados é quase idêntico ao usado em [Moro et al., 2014] (não inclui todos os atributos devido a questões de privacidade).
Usando o pacote rminer e a ferramenta R (http://cran.r-project.org/web/packages/rminer/), descobrimos que a adição dos cinco novos atributos sociais e econômicos (disponibilizados aqui) leva a uma melhoria substancial na previsão de sucesso, mesmo quando a duração da chamada não está incluída. Nota: o arquivo pode ser lido em R usando: d=read.table("bank-additional-full.csv",header=TRUE,sep=";")";")
Este conjunto de dados é baseado no conjunto de dados UCI "Bank Marketing" (verifique a descrição em: http://archive.ics.uci.edu/ml/datasets/Bank+Marketing).
Os dados são enriquecidos pela adição de cinco novas características/atributos sociais e económicos (indicadores nacionais de um país com cerca de 10 milhões de habitantes), publicados pelo Banco de Portugal e disponíveis publicamente em: https://www.bportugal.pt/estatisticasweb.
Este conjunto de dados é quase idêntico ao usado em [Moro et al., 2014] (não inclui todos os atributos devido a questões de privacidade). O arquivo zip inclui dois conjuntos de dados:
bank-additional-full.csv com todos os exemplos, ordenados por data (de maio de 2008 a novembro de 2010).
bank-additional.csv com 10% dos exemplos (4119), selecionados aleatoriamente de bank-additional-full.csv.
O menor conjunto de dados é fornecido para testar algoritmos de aprendizado de máquina mais exigentes em termos computacionais (por exemplo, SVM)O objetivo da classificação binária é prever se o cliente irá subscrever um depósito bancário a prazo (variável y).
Número de instâncias: 41188 para bank-additional-full.csv
Número de atributos: 20 + atributo de saída.
Informações de atributos: Para mais informações, leia [Moro et al., 2014].
Valores de atributos ausentes: Existem vários valores ausentes em alguns atributos categóricos, todos codificados com o rótulo “desconhecido”. Esses valores ausentes podem ser tratados como um possível rótulo de classe ou usando técnicas de exclusão ou imputação.

Dados do Cliente:
-age (idade) (numérico)
-job (emprego): tipo de trabalho (categórico: "administrador.","operário","empreendedor","empregada doméstica","gestão","aposentado","autônomo","serviços","estudante" ,"técnico","desempregado","desconhecido")
-marital: (conjugal) estado civil (categórico: "divorciado","casado","solteiro","desconhecido"; obs: "divorciado" significa divorciado ou viúvo)
-education: (educação) escolaridade (categórica: "básico.4a","básico.6a","básico.9a","ensino médio","analfabeto","curso.profissional","grau.universitário","desconhecido")
-default: (inadimplência) tem crédito inadimplente? (categórico: "não","sim","desconhecido")
-housing: (habitação) tem crédito habitação? (categórico: "não","sim","desconhecido")
-loan: (empréstimo) tem empréstimo pessoal? (categórico: "não","sim","desconhecido")
-Relacionado ao Último Contato da Campanha Atual:
-contact: (contato) tipo de comunicação do contato (categórica: "celular","telefone")
-month: (mês) último mês de contato do ano (categórico: "jan", "fev", "mar", ..., "nov", "dez")
-day_of_week: (dia da semana) último dia de contato da semana (categórico: "seg","ter","qua","qui","sex")
-duration: (duração) duração do último contato, em segundos (numérico). Nota importante: este atributo afeta altamente o destino de saída (por exemplo, se duração=0 então y="não"). No entanto, a duração não é --conhecida antes de uma chamada ser realizada. Além disso, após o término da chamada, y é obviamente conhecido. Assim, esta informação só deve ser incluída para fins de benchmark e deve ser descartada se a intenção for ter um modelo preditivo realista.

Outros Atributos:
-campaign: (campanha) quantidade de contatos realizados durante esta campanha e para este cliente (numérico, inclui último contato)
-pdays: número de dias que se passaram desde que o cliente foi contatado pela última vez em uma campanha anterior (numérico; 999 significa que o cliente não foi contatado anteriormente)
-previous: (anterior) quantidade de contatos realizados antes desta campanha e para este cliente (numérico)
-poutcome: resultado da campanha de marketing anterior (categórica: "fracasso","inexistente","sucesso")

Atributos do Contexto Social e Econômico:
-emp.var.rate: taxa de variação do emprego - indicador trimestral (numérico)
-cons.price.idx: índice de preços ao consumidor - indicador mensal (numérico)
-cons.conf.idx: índice de confiança do consumidor - indicador mensal (numérico)
-euribor3m: taxa euribor 3 meses - indicador diário (numérico)
-nr.employed: número de empregados - indicador trimestral (numérico)

Variável de Saída (variável target):
-y - o cliente subscreveu um depósito a prazo? (binário: "sim","não")

