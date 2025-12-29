CLI docker: 

docker image ls -> lista de imagens 
docker container [ls] / [inspect] (listar containers)
docker ps -> lista de containers ativos
docker network -> [ls]/[inspect]/[connect]/[create]... [connect] hash container + hash network  
docker logs [hashContainer]?

[nova imagem] -> docker build -t [nomeImagem]:[tag] [path] = [.] default  

[run imagem] -> docker run -detach? -> [-d]? [-rm]? -p port:port [nomeImagem]:[tag]

--------------//----------------

[CONCEITOS]

Containers != Imagens 

Containers são voláteis e efêmeros! - podem ser excluídos a qualquer momento

Imagens -> é a base do programa (SO's + Dependências + Arquivos + Diretório de pastas) (pode ser versionado com uso de tags)

Container -> é o isolamento de toda a aplicação da imagem do sistema operacional do computador 

Cada container possui seu CGroup -> Controle de uso de recursos operacionais para a aplicação. 

--------------//----------------

Volumes (Diretório externo): 

É uma forma de persistir informações vindas de containers e podendo associar a outros containers

Armazenamento local (hosting)

Um volume não está associado fortemente a um container. 

Quando é necessário? 
Ex: arquivos, assets, uploads, logs
Ex2: Banso de dados 

CLI > 

~/DevOps/docker/backend_test_docker$ docker volume
Usage:  docker volume COMMAND

Manage volumes

Commands:
  create      Create a volume
  inspect     Display detailed information on one or more volumes
  ls          List volumes
  prune       Remove unused local volumes
  rm          Remove one or more volumes

Run 'docker volume COMMAND --help' for more information on a command.


docker volume create [primeiro-volume]
docker volume inspect [primeirp-volume]

para associar um volume a um container: 

docker run ([-v] ou [--volume] [primeiro-volume][:/pathVolume]) ( [-p] [port:port]) [-d] [nomeContainer]