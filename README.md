# Projeto prático "Desavio Docker"

## Parte 1 (Dockerize + nginx)
Projeto na pasta "dockerize_nginx", com as seguintes alterações:
- nginx.conf transformado em um template (nginx.conf.tmpl)
- Dockerfile do nginx alterado para copiar o template para /etc/nginx
- Entrypoint dockerize adicionado ao serviço nginx no docker-compose.yml, gerando o arquivo de configuração em /etc/nginx/conf.d
- Variáveis de ambiente APP_HOST e APP_PORT adicionadas ao serviço nginx no docker-compose.yml

## Partes 2 e 3 (Code.education rocks! usando GO)
Projeto na pasta "codeeducation". [Imagem no dockerhub](https://hub.docker.com/repository/docker/dhoialmeida/codeeducation).

O tamanho da imagem em disco é 1.51 MB. O Dockerfile constrói a imagem em 2 etapas: uma imagem temporária baseada na imagem oficial Go é utilizada para compilar o programa, e a imagem final é produzida a partir da temporária copiando o executável final.
