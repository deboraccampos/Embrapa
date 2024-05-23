# API Embrapa

Este é um simples script de API Flask do dataset da Embrapa que permite baixar um arquivo CSV de uma URL e salvá-lo no Amazon S3. A classe `MotorEmbrapaGrupo37` é responsável por essa funcionalidade, enquanto o servidor Flask fornece um endpoint `/upload-file` para acionar o processo de download e upload do arquivo CSV.

## Requisitos

- Python 3.x
- Flask
- pandas
- requests
- awswrangler

## Configuração

1. Clone o repositório:
- git clone https://github.com/deboraccampos/Embrapa.git

2. Instale as dependências:
- pip install -r requirements.txt

3. Configure suas credenciais da AWS:
- Configure suas credenciais da AWS no seu ambiente local ou use outros métodos de autenticação suportados pelo `awswrangler`.

## Uso

1. Inicie o servidor Flask:
- python main.py
  
2. Faça uma solicitação GET para o endpoint `/upload-file` com o nome do arquivo desejado como um parâmetro de consulta:
- http://127.0.0.1:5000/upload-file?file_name=nome_do_seu_arquivo_csv

3. Verifique a resposta do servidor para ver se o arquivo foi baixado e salvo com sucesso no S3.
