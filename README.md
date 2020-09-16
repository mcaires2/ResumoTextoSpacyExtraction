# ResumoTextoSpacyExtraction

Resumir Textos utilizando o Processamento de Linguagem Natural com Vector e Spacy

O objetivo é conseguir extrair um resumo com as principais informações relevantes de um texto escrito em lingua portuguesa.

Usamos o processamento de linguagem natural para atingir o objetivo desejado em especial Spacy na linguagem python

Para tanto criamos uma lista de stopwords em conjunto com a existente na biblioteca do spacy. O detalhe é que esta lista de stop word tem como proposta retirar palavras irrelevantes do cálculo de relevância e frequênica de palavras, evitar, que se extrai trechos irrelevantes do texto como se importantes fossem.

Criamos uma função extrair_txt de um arquivo salvo no formato txt 

Cuidado com o encoding, pode variar a depender se este txt foi extraído ou não direto de um PDF (de todo modo deixei dois encodings prontos para utilização basta ativar/desativar)

Em seguida criamos um objeto nlp e um corpus donde separamos as sentenças dos textos e colocamos todas para letras minúsculas...

Usamos o sklearn para converter texto em vetor matemático

Ao chamar o CountVectorizer alimentamos eles com a lista de stop words que criamos nas etapas anteriores

Fizemos o parse dos vetores e criamos duas listas: a primeira com as palavras tokenizadas e uma segunda lista com a contagem que cada palavra apareceu ao longo do texto. Este passo é importante para poder descobrir a palavra com maior frequência e que será - como verá - nossa base 1 quando fomos pegar o valor relativo de frequência de cada uma destas palavras. 

No passo seguinte, criamos uma lista para armazenar um dicionário contendo cada sentença e a soma dos valores relativos das palavras que a compõem.

Assim procedendo temos um rank das frases mais relevantes de todo o texto (a matemática é realmente maravilhosa!!!)

No degrau seguinte, indexamos todas as frases do texto por ordem crescente e para fins desta atividade decidimos pegar as cinco últimas frases desta nova lista porque são as com maior valor de relevância.

Pronto, a parte de processamento de linguagem natural está finalizada e o resumo já pode ser acessado por um simples comando print já embutido na célula do Google Colab

Fomos adiante e decidimos descarregar o resumo em um documento do Word

Para tanto usamos python-docx















