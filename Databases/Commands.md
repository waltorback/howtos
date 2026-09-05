### создать репозиторий
```bash
git clone https://github.com/waltorback/hoots.git
```

### инсталяция brew
```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

```

### инсталяция podman
```bash
brew install podman
```

### инициализация podman
```bash
 podman machine init
```

```bash
podman machine start 
```

### хранилище контейнеров 
```url
https://app.docker.com/accounts/waltorback
```

### создать podman volume
```bash
podman volume create mysql_data
```

### создание и запуск контейнера 
```bash
podman run -d \
  --name mysql-container \
  -p 3306:3306 \
  -e MYSQL_ROOT_PASSWORD=qwerty1234 \
  -v mysql_data:/var/lib/mysql:Z \
  docker.io/library/mysql:latest
```

### список образов контейнеров 
```bash
 podman images
```

### список запущенных контейнеров 
```bash
 podman ps
```

```bash
podman ps --all
```

### остановить контейнер
```bash
podman stop <container id> #индендификатор контейнера
```

### запустить контейнер 
```bash
podman start <container id> #индентификатор контейнера
```

