# next20221-m3-melhor-rota

## NExT 2022.1 - Desafio: A melhor rota

O desafio proposto foi implementar uma API que fornece operações necessárias para:


- Cadastrar/Atualizar localização e status do caminhão.

- Listar todos os caminhões com suas informações (localização e status).

- Retornar a melhor rota para o destino final (escavadeira ou área de descarga) dado o identificador do caminhão. Caso o caminhão esteja CHEIO, a melhor rota deve ser para a área de descarga mais próxima. Caso o caminhão esteja VAZIO, a melhor rota deve ser para a escavadeira mais próxima.

- Segue abaixo o mapa de uma mina que deverá ser considerado no desafio. São definidos para a mina os segmentos de estradas e direções permitidas para o tráfego dos caminhões, assim como todos os pontos de localização. Para essa mina estão definidas 3 escavadeiras e 3 áreas de descargas. Os caminhões e suas localizações devem ser cadastrados/atualizados dinamicamente via API.

<div align="center">
<img src="https://user-images.githubusercontent.com/104402971/176017558-4052cc07-b9a5-428d-8dc0-013f206f640a.png" width="700px" />
</div>

## A Solução

A solução consiste em um servidor REST desenvolvido em Spring Boot Java, construído com a ferramenta de automação e gerenciamento Maven com comunicação com bancos de dados. Obtendo as dependências Spring Data JPA, Spring Web, MySQL Driver e o Hibernate Validator.

Na API  foi criada uma arquitetura com Controller que realiza a comunicação com um Service, Repository, o mapping (URI) a nível de classe, com uma entidade modelo caminhão e o cálculo da melhor rota partindo da localização e status do veículo inserida pelo usuário. 

Para realizar os cálculos das melhores rotas foi baseado nos estudos do Algoritmo de Floyd-Warshall e expressões Lambda em uma classe Best Route em comunicação com o Controller e o modelo caminhão, recebendo como parâmetros o status e a localização de cada veículo.

## Participantes do projeto e contatos:

- Cristina Matsunaga <div>
 [Github](https://github.com/criismnaga) | [Linkedin](https://www.linkedin.com/in/cristina-matsunaga-7992394b/)

- Diego Lins <div>
[Github](https://github.com/diegolins13) | [Linkedin](https://www.linkedin.com/in/in/diegolins13/)

- Emérson Morais <div>
[Github](https://github.com/EmersonRodrigoMorais) | [Linkedin](https://www.linkedin.com/in/%C3%A9merson-rodrigo-morais-34aa0651//)

Mentor

- Dennis Dantas

## Agradecimentos
  
O desafio foi proposto pelo como projeto de conclusão do Curso NExt - Nova experiência de trabalho promovido pelo Cesar.
