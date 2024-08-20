## Vigilância Laboratorial de Arboviroses - Pará

Este projeto realiza o processamento e a análise de dados laboratoriais relacionados à vigilância de arboviroses no estado do Pará. O código permite filtrar, processar e organizar os dados de requisições de exames laboratoriais para os agravos de DENGUE, ZIKA e CHIKUNGUNYA, gerando um arquivo Excel com os resultados organizados em diferentes abas para cada agravo.

## Descrição do Projeto

O script é responsável por:
- Carregamento de Dados: Utiliza a biblioteca pandas para carregar dados de um arquivo Excel armazenado no Google Drive.
- Filtragem e Processamento: Filtra os dados de acordo com o agravo de interesse (DENGUE, ZIKA ou CHIKUNGUNYA) e remove linhas com status de exame irrelevantes ou incompletos.
- Contagem e Organização dos Resultados: Conta os resultados dos exames e organiza as informações em uma tabela pivotada, somando o total de amostras enviadas e de casos positivos.
- Exportação dos Dados: Salva os resultados processados em um novo arquivo Excel, com uma aba dedicada para cada agravo.

## Estrutura do Projeto

VigiLab_Pará_Arboviroses.xlsx: Arquivo Excel gerado pelo script, contendo os resultados dos exames para DENGUE, ZIKA e CHIKUNGUNYA.
data.xlsx: Arquivo Excel de entrada contendo as requisições laboratoriais.

## Pré-requisitos
- Python 3.x
- Google Colab (opcional, mas recomendado)
- Bibliotecas Python: pandas

## Como Utilizar
- Montar o Google Drive: O script monta o Google Drive para acessar os arquivos diretamente da nuvem.
from google.colab import drive
drive.mount('/content/drive')

## Carregar os dados
- Substitua o caminho do arquivo pelo caminho do seu arquivo de dados de entrada.
- O script usa pandas para ler o arquivo Excel.

dados = pd.read_excel('/content/drive/My Drive/Vigilância Laboratorial/data.xlsx')

## Processamento dos dados
- A função processar_dados_agravo(dados, agravo) é utilizada para processar e organizar os dados para cada agravo.
- Os resultados são então salvos em um novo arquivo Excel.

output_path = '/content/drive/My Drive/Vigilância Laboratorial/VigiLab_Pará_Arboviroses.xlsx'

## Salvando os Resultados
- Os dados processados são salvos em diferentes abas do arquivo Excel de saída, facilitando a análise e interpretação.

with pd.ExcelWriter(output_path) as writer:
    df_dengue.to_excel(writer, sheet_name='DENGUE')
    df_zika.to_excel(writer, sheet_name='ZIKA')
    df_chikungunya.to_excel(writer, sheet_name='CHIKUNGUNYA')

## Conclusão
- O script finaliza com uma mensagem de sucesso.
print(f"Tabela salva com sucesso!")

## Autor
Desenvolvido por Pedro Araújo.
