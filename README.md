# <center> Implementar um Registry local</center>


### Introdução


Esta página foi elaborada com informações básicas sobre como você pode manter seus **Containers** usando o Docker Distribution em seu ambiente local.


O [Docker Distribuition](https://github.com/distribution/distribution) é um *registry* repositório de imagens Docker local que serve para guardar e compartilhar as suas imagens. 


### Aviso


Esta é uma sugestão de uma configuração inicial para o Registry local e em máquinas de testes ou desenvolvimento. Não implemente um servidor de registro em produção sem proteção por TLS e um mecanismo de controle de acesso.


### Pré-requisitos:    


    - Você precisa ter o Docker instalado em sua máquina local.


### Criar o Registry Local


Para que possamos ter o Docker Distribuition de forma simples e funcional, guardando e distribuindo nossas imagens Docker localmente, basta rodá-lo como um *container*, execute o seguinte comando:


<p>


<img align = 'left' src="img/docker-registry.png " alt="Comando Docker para criar um container registry">

<p>


<p>

<!-- #region -->
```python
$ docker container run -d -p 5000:5000 --restart=always --name registry registry:2
```
<!-- #endregion -->

<p>


<p>

**Resultado da execução**

<p>

<img align = 'left' src="img/resultado-1.png " alt="Resposta do comando">

<p>

continua...


**Referências:**

1. [Docker](https://www.docker.com/get-started)
2. [Docker Registry](https://docs.docker.com/registry/deploying/)
3. Descomplicando o Docker 2a edição<br>
   Jeferson Fernando Noronha Vitalino<br>
   Marcus André Nunes Castro



```python

```

```python

```
