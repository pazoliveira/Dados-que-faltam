# Projeto de análise de dados acerca do Racismo Religioso e a Invisibilidade Estatística do Povo de Terreiro 

Sem dados, não há pesquisa, não há política pública e não há proteção. Registrar é, antes de tudo, um ato de permanência.

O Axés é a plataforma digital do Atlas: uma rede onde terreiros, casas de axé, roças e demais espaços sagrados das religiões de matriz africana do Distrito Federal e entorno se cadastram, contam sua história e se encontram.

Este projeto acadêmico se insere no contexto da entrega do quarto artefato do trabalho feito no PROJETO AXÉS que é da PRODUÇÃO DE MATERIAL EDUCATIVO para professores e jornalistas acerca dos problemas enfrentados pelos povos de religiões de matriz africana a partir da construção de um painel interativo análise de dados de públicos do DF e do BRASIL. 

BANCO DE DADOS ESCOLHIDOS ATÉ O MOMENTO:

SINAN / DATASUS (Violência na Saúde Pública)

O que é: O sistema do SUS que registra quem entra no hospital vítima de agressão. Existe um campo específico de "Motivação da Violência" que inclui intolerância religiosa/racismo.
Onde acessar: Plataforma TABNET DATASUS. Acesse datasus.saude.gov.br/informacoes-de-saude-tabnet/, vá em "Epidemiológicas e Morbidade" e busque por "Violência Interpessoal e Autoprovocada (VIVA)". Os microdados podem ser baixados em arquivo CSV para tratar no Python.

Câmara dos Deputados e Senado (Dados Legislativos)

O que é: APIs que listam todos os Projetos de Lei (PLs) em tramitação. Útil para monitorar tentativas atuais de cerceamento de direitos ou proteção territorial.
Onde acessar (Câmara): dadosabertos.camara.leg.br (Possui uma API RESTful excelente documentada em Swagger, perfeita para consumo com a biblioteca requests do Python).

Datajud (Painel do Judiciário)

O que é: O portal do CNJ que você já ia usar no Projeto 3.
Como aplicar neste projeto: A API pública permite consultar processos. Você pode cruzar classes processuais de "Crimes de Preconceito" (Lei 7.716/89) e ver quanto tempo, em média, a Justiça do DF demora para julgar um caso de racismo religioso em comparação com outros crimes.
Onde acessar: api-publica.datajud.cnj.jus.br

IPEDF (Microdados PDAD)

O que é: Pesquisa Distrital por Amostra de Domicílios. É o "censo" local do DF.
Onde acessar: ipe.df.gov.br/microdados/. Baixe os microdados e busque as variáveis relacionadas à declaração de religião por Região Administrativa (RA).

IBGE (Censo Demográfico e SIDRA)

O que fornece: Os dados absolutos sobre a declaração de religião, cor e raça da população brasileira, descendo até o nível de município e setor censitário. (Nota: Os dados completos de religião do Censo 2022 estão em fase de tabulação e divulgação, sendo o Censo 2010 a base histórica mais granular).

Como aplicar no projeto: O IBGE fornece a "base de cálculo". Se o Disque 100 mostra 50 ataques no DF e 50 em SP, o número absoluto não diz muito. Cruzando com o IBGE, você descobre a taxa proporcional (ex: 5 ataques a cada 1.000 praticantes de umbanda no DF vs. 1 a cada 1.000 em SP), provando estatisticamente onde a comunidade é mais vulnerável.

Onde acessar: O sistema SIDRA (sidra.ibge.gov.br) permite montar tabelas personalizadas cruzando Religião e Cor/Raça. Para automatizar no Python, o IBGE possui uma API pública excelente (servicodados.ibge.gov.br/api/docs).

SINESP (Ministério da Justiça e Segurança Pública)

O que fornece: A consolidação nacional dos Boletins de Ocorrência (BOs) registrados pelas Polícias Civis de todos os estados.

Como aplicar no projeto: Fundamental para a pergunta de pesquisa sobre o "Apagamento Institucional". Você pode cruzar os dados de denúncias do Disque 100 com os registros oficiais do SINESP para o mesmo período e estado, medindo estatisticamente a subnotificação criminal (a diferença entre quem denuncia na ouvidoria e quem consegue registrar o BO na delegacia).

Onde acessar: Disponível no Portal de Dados Abertos do Ministério da Justiça (dados.mj.gov.br), na seção de Estatísticas de Segurança Pública.

Fundação Cultural Palmares

O que fornece: O cadastro e a certificação oficial de comunidades tradicionais de matriz africana e territórios quilombolas.

Como aplicar no projeto: Essencial para a análise espacial (Geografia do Racismo). Muitos terreiros estão inseridos em comunidades que lutam pelo reconhecimento do território. Cruzar as coordenadas geográficas dessas comunidades com dados de conflitos fundiários e especulação imobiliária ajuda a mapear o risco territorial.

Onde acessar: O painel de certificações pode ser extraído do Portal de Dados Abertos do Governo Federal buscando pelas bases ativas da Fundação Palmares (dados.gov.br).

IPEA (Instituto de Pesquisa Econômica Aplicada)

O que fornece: O IPEA consolida o Atlas da Violência, uma base tratada que cruza segurança pública com indicadores socioeconômicos.

Como aplicar no projeto: Serve para contextualizar o racismo religioso dentro do racismo estrutural. O IPEA permite cruzar a violência com a vulnerabilidade social da Região Administrativa (RA) no DF, testando a hipótese de que terreiros em áreas mais pobres sofrem tipos de violência diferentes (ex: violência física vs. intolerância em escolas) daqueles em áreas nobres.

Onde acessar: A plataforma Ipeadata (ipeadata.gov.br) permite o download em formato .csv de séries históricas de indicadores sociais e de violência.


