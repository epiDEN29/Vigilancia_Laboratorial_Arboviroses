## Processador de Dados Laboratoriais - Arboviroses Urbanas - 2025

#### Descrição

Este projeto consiste em um script Python para processar e analisar dados laboratoriais de arboviroses (Dengue, Zika e Chikungunya) do sistema VigiLab para o ano de 2025. O programa processa os dados, calcula estatísticas importantes e gera relatórios detalhados por município e período.

#### Fonte dos dados

Os dados processados nesse projeto devem ser oriundos da base de dados do Gerenciador de Ambiente Laboratorial (GAL). Para utilização em outras fontes de dados, o script de análise deve ser devidamente ajustado, conforme a necessidade.

#### Como baixar os dados

Login GAL > Biologia Médica > Relatórios > Epidemiológicos > Relatórios Epidemiológicos por Agravo - Dados Clínicos > preencher informações

#### Funcionalidades

- Processamento de dados por períodos de 7 dias
- Análise de resultados para Dengue, Zika e Chikungunya
- Cálculo de positividade por município
- Geração de relatórios em Excel com múltiplas planilhas
- Filtros automáticos para limpeza de dados inconsistentes

#### Pré-requisitos

- Python 3.x
- Pandas
- Arquivo de dados no formato Excel (.xlsx)

#### Instalação

Clone este repositório: git clone https://github.com/seu-usuario/vigilab-processor.git

Instale as dependências necessárias: pip install pandas openpyxl

#### Como usar

Coloque seu arquivo de dados com nome 'data.xlsx' na mesma pasta do script

Execute o script: python vigilab_processor.py

O resultado será salvo em um arquivo Excel chamado 'TotalVigiLabUrbanas_2025.xlsx'

#### Estrutura do arquivo de saída

O arquivo Excel gerado contém as seguintes planilhas:
  - DENGUE: Resultados totais para Dengue
  - CHIKUNGUNYA: Resultados totais para Chikungunya
  - ZIKA: Resultados totais para Zika
  - DENGUE_PERIODOS: Análise temporal para Dengue
  - CHIKUNGUNYA_PERIODOS: Análise temporal para Chikungunya
  - ZIKA_PERIODOS: Análise temporal para Zika

Métricas calculadas
  - Amostras Enviadas
  - Resultados Inconclusivos
  - Resultados Indeterminados
  - Resultados Não Reagentes
  - Resultados Reagentes
  - Resultados Não Detectáveis
  - Resultados Detectáveis
  - Total de Positivos
  - Positividade (%)

#### Autor
Desenvolvido por Pedro Araújo

#### Licença
Este projeto está sob a licença MIT. Veja o arquivo LICENSE para mais detalhes.

#### Contato
Para mais informações ou dúvidas, abra uma issue no repositório.
