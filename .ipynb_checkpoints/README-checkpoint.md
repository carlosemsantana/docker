# <center> Implementar um Registry local</center>


### Introdução


Esta página foi elaborada com informações básicas sobre como você pode manter seus **Containers** usando o Docker Distribution em seu ambiente local.


O [Docker Distribuition](https://github.com/distribution/distribution) é um *registry* repositório de imagens Docker local que serve para guardar e compartilhar as suas imagens. 


### Aviso


Esta é uma sugestão de uma configuração inicial para o Registry local e em máquinas de testes ou desenvolvimento. Não implemente um servidor de registro em produção sem proteção por TLS e um mecanismo de controle de acesso.


### Pré-requisitos:    

    - Máquina com sistema operacional Linux.
    - Você precisa ter o Docker instalado em sua máquina local.


### Criar o Registry Local


Para que possamos ter o Docker Distribuition de forma simples e funcional, guardando e distribuindo nossas imagens Docker localmente, basta rodá-lo como um *container*, execute o seguinte comando:


![](img/docker-registry.png)

<!-- #region -->
```python
$ docker container run -d -p 5000:5000 --restart=always --name registry registry:2
```
<!-- #endregion -->

**Resultado da execução**


![](img/resultado-1.png)


O container ID **50086bf481e753e39f8098487594cf85827d040af41f5c989fccffbc8dc0d782** foi criado com sucesso!


Você pode verificar se o container "registry" está em execução, através de um dos comandos abaixo:

<!-- #region -->
```python
$ docker container ls 

$ docker container ps 

$ docker ps

```
<!-- #endregion -->

![](img/docker-container-ls.png)


![](img/docker-container-ps.png)


![](img/docker-ps.png)


O *container* foi criado e está em execução. Agora vamos testá-lo realizando a submissão de uma imagem de teste no repositório.


Quando você criar um *container* registry, uma estrutura de diretórios será construída em sua máquina local onde  todas as imagens enviadas serão organizadas. Para descobrir a localização do repositório, observe o comando abaixo:


**Lembrando que:**  O repositório será montado no sitema de arquivos Linux somente se o *container* registry estiver em execução (rodando)

<!-- #region -->
```python
$ df -h
```
<!-- #endregion -->

![](img/df-h.png)


**Referências:**

1. [Docker](https://www.docker.com/get-started)
2. [Docker Registry](https://docs.docker.com/registry/deploying/)
3. Descomplicando o Docker 2a edição<br>
   Jeferson Fernando Noronha Vitalino<br>
   Marcus André Nunes Castro


