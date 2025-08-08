# CDR
Ao longo deste notebook, realizamos uma análise exploratória e descritiva completa de um dataset simulado de registros de chamadas (CDR), abrangendo os tipos de registro VOICE, SMS e DATA, bem como padrões temporais e espaciais (localização).

Em Resumo, as Principais Etapas e Descobertas Incluíram:

Geração do Dataset: Criamos um dataset simulado com 5000 registros, com estrutura baseada em CDRs 3GPP, utilizando bibliotecas Python como pandas, faker, random e numpy.
Análise Descritiva por Tipo de Registro:
VOICE: Analisamos a duração das chamadas de voz, identificando uma média de aproximadamente 782 segundos, mediana de 777 segundos e moda em 9 segundos, com chamadas curtas fortemente associadas a status 'BUSY' e 'FAILED'. Registros de voz não apresentaram volume de dados.
SMS: Constatamos que registros de SMS apresentaram duração e volume de dados zero, e a coluna callStatus não era relevante. A atividade de SMS foi distribuída entre as estações base.
DATA: Identificamos que registros de dados foram os mais frequentes. As sessões de dados tiveram durações e volumes significativamente variáveis, com forte correlação positiva entre uplink e downlink. O volume médio de downlink foi significativamente maior que o de uplink. O tráfego de dados também se distribuiu de forma desigual entre as estações base.
Análise Temporal:
Preparamos os dados extraindo features temporais como hora do dia e dia da semana.
Analisamos descritivamente os padrões de tráfego por tipo de registro e localização ao longo do tempo, observando picos durante horas diurnas.
Realizamos testes de hipótese que confirmaram que a contagem total de registros é significativamente maior durante as horas de pico e que a contagem de registros durante o pico difere significativamente entre as estações base.
Testes para diferenças em volume médio de dados downlink (semana vs fim de semana) e duração média de chamadas de voz (diurno vs noturno) não apresentaram significância estatística neste dataset específico.
As visualizações temporais reforçaram os padrões diários e a variação da carga de tráfego por estação base.
Conclusão:

Este exercício de simulação e análise forneceu uma visão abrangente das características de um dataset CDR básico e demonstrou como utilizar ferramentas de análise de dados em Python (pandas, matplotlib, seaborn, scipy) para explorar e entender padrões de tráfego de rede.

É importante notar que este dataset é simulado e os padrões de tráfego observados aqui podem diferir significativamente dos padrões encontrados em redes móveis reais, que são influenciadas por uma variedade de fatores complexos do mundo real (comportamento do usuário, eventos específicos, cobertura de rede, etc.).

No entanto, os métodos e o código de análise desenvolvidos ao longo deste notebook (filtragem de dados, cálculo de estatísticas descritivas, visualizações, testes de hipótese) são gerais e aplicáveis a datasets CDR reais. A estrutura do código e o fluxo de análise podem ser reutilizados como um ponto de partida sólido para investigar o tráfego em qualquer rede, permitindo adaptar as perguntas e testes de hipótese aos padrões específicos observados nos dados reais.

Em suma, embora os resultados numéricos específicos sejam do domínio da simulação, o processo analítico e as ferramentas empregadas são valiosas para a compreensão e análise de dados de tráfego de redes de telecomunicações no mundo real.

