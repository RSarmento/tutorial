# tutorial
Tutorial de Scrapy aplicado ao site JusBrasil

## Scrapy
A ferramenta scrapy foi usada para acessar os processos e salvar suas informações. 
Foi usado o guia de instalação disponível na documentação da ferramenta [1]: 
  * Criar projeto tutorial usando o comando **scrapy startproject tutorial** 
	* Na classe principal definir função de extração de texto, função de iniciação de requisição com o endereço *https://stj.jusbrasil.com.br/jurisprudencia/*, adicionando o número sequencial do processo, função de parsing que extrai as informações do cabeçalho, da ementa e do acórdão
	* Definir na classe Item os campos esperados do cabeçalho, ementa e acórdão
	* Descomentar as linhas da clasee ITEM_PIPELINES no arquivo **settings.py** e incluir o arquivo que define o exportador de arquivo, no caso **JsonItemExporter**
	* Definir classe **JsonItemExporter** no arquivo **pipelines.py** 
	* Executar comando **scrapy crawl tutorial --set FEED_URI=output.json --set FEED_FORMAT=json**

## Referências
	https://docs.scrapy.org/en/latest/intro/install.html
