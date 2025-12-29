CLI docker: 

docker image ls -> lista de imagens 
docker container [ls] / [inspect] (listar containers)
docker ps -> lista de containers ativos
docker network -> [ls]/[inspect]/[connect]/[create]... [connect] hash container + hash network  
docker logs [hashContainer]?

[nova imagem] -> docker build -t [nomeImagem]:[tag] [path] = [.] default  

[run imagem] -> docker run -detach? -> [-d]? [-rm]? -p port:port [nomeImagem]:[tag]