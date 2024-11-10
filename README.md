# Full Cycle Challenge - Docker Image com Go Lang

Este é um desafio proposto para criar uma imagem Docker mínima com o Go Lang que ao ser executada imprime a mensagem **"Full Cycle Rocks!!"** no console. O objetivo principal é criar uma imagem otimizada com menos de 2MB, usando conceitos de multi-stage build no Docker.

## Como Executar a Imagem Publicada

Para executar a imagem diretamente do Docker Hub, basta rodar:

```bash
docker run gabrielalmir/fullcycle
```

## Como Configurar e Executar o Projeto

### Pré-Requisitos

- Docker instalado
- Conta no [Docker Hub](https://hub.docker.com/)

### Passos para Configuração e Execução

1. Clone o repositório:

   ```bash
   git clone https://github.com/gabrielalmir/full-cycle-docker-desafio-1
   cd full-cycle-docker-desafio-1
   ```

2. Construa a Imagem Docker:

   Utilize o Dockerfile para criar a imagem localmente.

   ```bash
   docker build -t gabrielalmir/fullcycle .
   ```

3. Teste a Imagem:

   Execute o container para verificar se a mensagem aparece corretamente no console.

   ```bash
   docker run gabrielalmir/fullcycle
   ```

   O resultado esperado deve ser:

   ```plaintext
   Full Cycle Rocks!!
   ```

4. Tamanho da Imagem:

   Para verificar o tamanho da imagem, use o comando abaixo:

   ```bash
   docker images gabrielalmir/fullcycle
   ```

   A imagem deve ter menos de 2MB.

   Saída:

   ```bash
   REPOSITORY               TAG       IMAGE ID       CREATED         SIZE
   gabrielalmir/fullcycle   latest    60ae03419c5f   5 minutes ago   1.46MB
   ```

5. Publicação no Docker Hub:

   Caso queira publicar a imagem, faça login e utilize o comando:

   ```bash
   docker login
   docker push gabrielalmir/fullcycle
   ```

