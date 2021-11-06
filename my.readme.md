# stack com apm
docker-compose -f docker-compose.yml -f extensions/apm-server/apm-server-compose.yml up -d

# create and start com logs
docker-compose -f docker-compose.yml -f extensions/apm-server/apm-server-compose.yml up -d && docker-compose logs -t -f

# start without create
docker-compose -f docker-compose.yml -f extensions/apm-server/apm-server-compose.yml start && docker-compose logs -t -f

# delete e recriacao
docker-compose down --remove-orphans && docker-compose -f docker-compose.yml -f extensions/apm-server/apm-server-compose.yml up -d && docker-compose logs -t -f

# Logs
docker-compose logs -t -f

# mudar em .env a versao do stack
docker-compose build

# remove all stack
docker-compose down --remove-orphans