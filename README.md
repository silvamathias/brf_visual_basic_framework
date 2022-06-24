# vbf Visual Basic Framework

## Descrição

    __VBF__ é um grupo de funções criado para auxiliar no desenvolvimento de ferramentas em *VBA*. Embora a necessidade de contar com tais recursos tenha surgido na época em que atuei
no mercado financeiro a ideia de organizá-los em funções veio posteriormente e com a quarentena iniciada em 2020 foi possível começar seu desenvolvimento. Atuantes na área financeira  possuem o maior potencial de usufruir a totalidade dos benefícios deste recurso, contudo qualquer usuário do pacote *MS Office* terá ganho ao usar o __VBF__ em:

* Acessar banco de dados;
* Manipular dados;
* Manipular arquivos e pastas salvos no computador;
* Envio de e-mail;
* Baixar dados disponível na web;
* Elabor relatórios automáticos.

    As funções estão separadas em grupos para facilitar o uso. Contam com um prefixo para facilitar a identificação enquanto se utiliza.
Atualmente conta com 10 grupos de funções e 56 funções.

**prefixo** | **tipo** | **Descrição**
:-----:|:-----:|:-----
api|api_windows|Funções que usam as API's do windows
app|Excel app settings|Funções que manipulam o programa Excel.
def|directory and files settings|Funções usadas para manipular arquivos e diretórios do computador
dtg|work with datagroup|Funções que manipulam dados estruturados disponíveis em diversos formatos (txt, xls, recordset, etc)
eml|e-mail settings|Funções para manipular odjetos Outlook
fun|usinng in sheet|Funções que podem ser usadas em planilhas como uma função normal do Excel
msg|user interface|Funções para facilitar a comunicação com o usuário final
sql|sql connection|Funções para usar a linguagem sql em arquivos (csv, xls,etc) e bancos de dados
vld|data validate|Funções para validar os valores das variáveis
xls|excel file and objects settings|Funções para manipular arquivos Excel e seus objetos

    O código utiliza do inglês em seu desenvolvimento, no entanto todas as funções que possuem uma mensagem de texto como retorno, esta é feita por padrão em português (PT-BR) porém
nestas existe a possibilidade de configurar o retorno em inglês (EN). Variáveis não possuem tradução, contudo este tutorial será feito inicialmente em português (PT-BR) visando
ajudar os falantes da língua em se desenvolverem como programador. O tutorial em inglês será disponibilizado/atualizado logo em seguida

## Tutorial

### api_windows

----

#### api_download_web_file

###### Descrição:

    Baixa arquivos disponíveis em sites.

###### Parâmetros

**Nome** | **Opcional** | **Tipo** | **Descrição**
:-----:|:-----:|:-----:|:-----
url_file|obrigatório|String|A *URL* completo do arquivo na internet
file|obrigatório|String|O nome que se deseja usar para salvar o arquivo no computador
path|opcional|String|O caminho no computador onde deseja salvar o arquivo. Caso não seja informado será salvo na mesma pasta onde o arquivo *Excel* está salvo.

###### retorno

**Variant**

###### Exemplo de uso

~~~vbnet
'Declara as variáveis
Dim dwld as Variant
Dim site_ind as String
Dim pt_temp as String
Dim arq as String

'URL completa do arquivo contendo o site e o nome do arquivo
site_ind = "https://www.anbima.com.br/informacoes/indicadores/arqs/indicadores.xls"

'Nome que será usado para salvar o arquivo no computador
arq = "Anbima_indicadores.xls"

'Nome da pasta onde o arquivo será salvo
pt_temp = ThisWorkbook.Path & "\temp"

'Chama a função usando as variáveis declaradas acima
dwld = vbf.api_download_web_file(site_ind, arq, pt_temp)

~~~

----

#### api_user_windows

###### Descrição:

    Retorna o usuário atual.

###### Parâmetros

    Não aplicado

###### retorno

**String**

###### Exemplo de uso

~~~vbnet
'Declara as variáveis
Dim user_id as String

'Chama a função para obter o usuário atual do sistema
user_id = vbf.api_user_windows()

~~~

----

### sql connection

----

Em desenvolvimento...
