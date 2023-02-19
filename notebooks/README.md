# Estrutura da pasta "notebooks"

A pasta "notebooks" contém os arquivos Jupyter Notebook que são responsáveis pela extração dos dados do portal da Câmara Municipal de Sorocaba. Esses notebooks são executados periodicamente por meio de uma GitHub Action configurada no repositório.

## Organização da pasta

A pasta "notebooks" é organizada da seguinte forma:

* **extracao.ipynb**: Este notebook contém o código responsável pela extração dos dados do portal da Câmara Municipal de Sorocaba. Ele realiza o download dos arquivos em PDF contendo as informações de gastos do mês anterior e faz o processamento desses dados para gerar o arquivo JSON que será utilizado na geração das imagens.

* **geracao_imagem.ipynb**: Este notebook é responsável pela geração das imagens a partir do arquivo JSON gerado pelo notebook de extração. Ele utiliza a biblioteca Pillow para gerar as imagens e salvá-las na pasta "imagens".

* **arquivo_config.yml**: Este arquivo contém as configurações necessárias para a execução dos notebooks na GitHub Action. Ele define as dependências que devem ser instaladas e os comandos que devem ser executados para a extração dos dados e geração das imagens.

## GitHub Action

A pasta "notebooks" é utilizada em conjunto com uma GitHub Action que realiza a execução dos notebooks periodicamente. A Action está configurada para ser executada no primeiro dia útil de cada mês, a fim de garantir que as informações mais recentes estejam sempre disponíveis.

Ao final da execução, a Action realiza o commit e o push das imagens geradas para o repositório no GitHub. Dessa forma, as imagens podem ser acessadas facilmente pela página do projeto e pelos usuários interessados em monitorar os gastos dos vereadores de Sorocaba.

A estrutura da pasta "notebooks" é simples e eficiente, permitindo a organização e a execução automatizada dos notebooks de extração e geração de imagens.
