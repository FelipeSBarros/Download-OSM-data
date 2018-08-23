# Baixando dados do Open Street Map

Neste respositório vamos divulgar os scripts e comandos usados para baixar dados do Open Street Map (OSM).

Há várias formas de baixar dados do Open Street Map, inclusive por programação, seja R ou Python….

Vamos mostrar algumas, aos poucos.

Para não começar com o clássico R ou Python, decidi apresentar primeiro o Over Pass  Turbo.

* [Over Pass Turbo](#over-pass-turbo)  
[![Assista ao video Baixando dados do Open Street Map com Over Pass Turbo](https://img.youtube.com/vi/wDk_Q3iZ--E/0.jpg)](https://youtu.be/wDk_Q3iZ--E)

## Over Pass Turbo

[Over Pass Turbo](https://overpass-turbo.eu/) é considerada uma interface gráfica que permite executar consultas no banco de dados do OSM, assim como visualizar o resultado em um *webmap* e, claro, baixar tais dados em vários formatos.

O Over Pass Turbo não serve apenas para nos facilitar o acesso aos dados, ele permite fazer vários tipos de consultas, sejam espaciais ou não, e por isso é considerado como uma ferramenta de **mineração de dados** do OSM.
Assista ao [video](https://youtu.be/wDk_Q3iZ--E) para entender mais a respeito.

Com o Over Pass Turbo pode-se acessar os dados e realizar consultas espaciais com o assistente (*wizard*) ou por linguagem de programação; Em ambos os casos, podemos ter acesso aos diferentes elementos que compoem os dados o OSM:  nodes, ways, relations, e area. Para fazer bom uso dessa ferramenta fantástica, dê uma olhada nos [links](#Algun-links-importantes:).

#### Códigos usados no video:

* Consulta usando o assistente (*wizard*)  

```
# buscando bares em Belo Horizonte
amenity=bar in "Belo Horizonte"

# Buscando escolas no Brasil
amenity=school in "Rio de Janeiro"

```

* Usando a linguagem de programação

```
# Escolas até 100 metros das paradas de ônibus
area[name="Rio de Janeiro"];
node(area)[highway=bus_stop];
node(around:100)[amenity=school];
out;
```

#### Alguns links importantes:  

* [Wiki do assistente de consulta](https://wiki.openstreetmap.org/wiki/Overpass_turbo/Wizard);  
* [Wiki da linguagem usada pelo Over Pass Turbo](https://wiki.openstreetmap.org/wiki/Overpass_API/Overpass_QL);
* [Wiki da API Over Pass](https://wiki.openstreetmap.org/wiki/Overpass_API)  
* [Repositório do projeto Over Pass Turbo](https://github.com/tyrasd/overpass-turbo)
