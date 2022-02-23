# Challenge de BI - 2ª Semana - Alura

#### Dashboard da Alura Food

Foi desenvolvido um dashboard para a Alura Food, que tem interesse em expandir seu negócio na Índia. Para isso, foram criadas métricas e análise dos dados disponibilizados para tomar a melhor decisão.

#### Base de Dados
A base de dados consiste em uma planilha do google sheets, cinco arquivos Json e uma conexão com uma API, com a seguinte estrutura:

**Tabela codigo_paises**
* codigo_paises


**Tabela avaliacoes_restaurantes**
* Restaurant Id
* Restaurant Name
* Country Code
* City
* Address
* Locality
* Locality Verbose
* Longitude
* Latitude
* Cuisines
* Average Cost for two
* Currency
* Has Table booking
* Has Online delivery
* Is delivering
* Switch to order menu
* Price range
* Aggregate Rating
* Rating color
* Rating text
* Votes

**Dim_cambio**
* Value.code
* Value.codein
* Value.name
* Value.high
* Value.low
* Value.create_date

A tabela  **Dim_cousines** será criada a partir da **Tabela avaliacoes_restaurantes**

**Dim_cousines**
* id restaurante
* cousines

## Ferramentas Utilizadas no Projeto

Foi utilizado apenas o Power BI para o desenvolvimento do Dashboard e uma paleta de cores para tornar o dashboard acessível a pessoas que possuem daltonismo

## Tratamento dos Dados

**Tabela codigo_paises**

* Promover cabeçalhos
* Separação de colunas por dígitos e não digitos
* Substituição de valores (_ por “espaço”)
* Transformação de cortar para eliminar espaços antes do nome do país.
* Maiúscula na primeira letra
* Renomear colunas para (Id país e Nome país)
* Renomear tabela para Dim_paises.

**Tabela avaliacoes_restaurantes**

* Manter apenas a coluna sobre restaurantes
* Expandir todas colunas
* Excluir colunas que não serão utilizadas
* Filtrar coluna de id país para exibir o código 1
* Tipar as colunas
* Tipar a coluna "aggregate_rating" por localidade.
* Substituir valores das colunas que tem 0 e 1 como registro para Sim e Não

**Dim_cousines**

* Remoção de duplicatas
* Dividir coluna por delimitador
* Texto aparado

**Dim_cambio**

* Remoção de colunas que não serão utilizadas
* Tipar as colunas
* Alteração de tipo dos valores por localidade

## Métricas

* Filtrar por cidade, restaurantes e se tem reserva
* total de restaurantes na índia
* Preço médio
* Média de avaliação
* Porcentagem de restaurantes que tem ou não online delivery.
* 5 cidades que mais possuem restaurantes
* 10 culinárias que mais são exploradas na Índia.
* Imagens dos restaurantes
* Restaurantes por cidade e suas classificações
* Preço médio através das moedas BRL, USD e EUR.

## Relacionamentos

# Tabela de fato:

* Avaliações Restaurante

# Dimensões:

* Países
* Cousines
* Câmbio

# Relacionamentos:

* Avaliações Restaurante(n) - (n)dim_Cousines = muitos para muitos (n-n)
* Avaliações Restaurante(n) - (1)dim_Paises = muitos para um (n-1)

## Link do Dashboard
https://app.powerbi.com/view?r=eyJrIjoiODg4YTMzMWMtODRjNy00MDRhLThlODgtNGM4ZDliZTg2OGY3IiwidCI6Ijk0NjZmMmYwLTI4ZmQtNDYxMi04MjhkLTQ0YzdlNzU4MDA3OCJ9&pageName=ReportSection
