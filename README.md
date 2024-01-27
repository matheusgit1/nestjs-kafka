## Sobre o projeto

Esse repositório é um estudo e exemplo de aplicação usando nestjs + kafka como sistema integrado de messageria e streaming de dados em um  mini projeto de sistema de compra e pagamentos para um ecommerce, funcionando de forma desacoplado.

Arquitetura Sugerida.

![Arquitetura](https://github.com/matheusgit1/nestjs-kafka/blob/main/imagens/Captura%20de%20tela%202024-01-26%20215957.png)

## Stack utilizada

Node, Typescript, Javascript, jest, Kafka, docker, nest cli, nestjs

## Rodar a aplicação

esse repositório é feito de dois projetos menores

**orders**

**payments**

cada projeto é executado de forma distinta seguindo os passos a baixo

---

### Rodando através do docker compose up:

Acesse a pasta nestjs-kafka e abra o `VSCode` ou em quaquer editor de sua preferencia

```bash
cd nestjs-kafka && code . ##para vscode##
```

Rode os containers com o comando (use --build na primeira execução, nas demais, não é obrigatório)

```bash
docker-compose up --build
```

Entre no container do `next`:

```bash
docker-compose exec app bash
```

Instale as dependências:

```bash
npm install
```

ou se preferir, use o yarn

```bash
yarn install
```

Rode o comando para o `prisma` realizar a `migrate`:

```bash
cd apps/orders && npx prisma migrate dev
```

Para rodar a aplicação rode o comando:

```bash
npm run start:dev
```

ou se preferir, use o yarn

```bash
yarn start:dev
```


#### Payments

Rode o comando para o `prisma` realizar a `migrate`:

```bash
cd apps/payments && npx prisma migrate dev
```

Para rodar a aplicação rode o comando:

```bash
npm run start:dev payments
```



OBSERVAÇÃO: Caso precise parar os containers por algum motivo rode o comando: `docker compose down`, pois o container do `Kafka` precisa ser parado e restartado.

---

### Dev Container:

Instale as dependências:

```bash
npm install
```

#### Orders

Rode o comando para o `prisma` realizar a `migrate`:

```bash
cd apps/orders && npx prisma migrate dev
```

Para rodar a aplicação rode o comando:

```bash
npm run start:dev
```

#### Payments

Rode o comando para o `prisma` realizar a `migrate`:

```bash
cd apps/payments && npx prisma migrate dev
```

Para rodar a aplicação rode o comando:

```bash
npm run start:dev payments
```

OBSERVAÇÃO: Caso precise parar os containers por algum motivo faça como abaixo:

Digite `ctrl + shift + p` e selecione `Dev Containers: Rebuild Containers`, pois o container do `Kafka` precisa ser parado e restartado.

---


## Testes unitário

Este serviço foi implementado de forma a ser possivel criar testes unitarios e de integração.

para a execução dos testes use `npm run test:coverage`

## Sobre o Autor

Eu sou uma pessoa desenvolvedora full-stack, técnico em administração, engenheiro de automação em formação, e cientista de dados em formação. Sempre busco por excelência e entregar o máximo com a maior qualidade, sem claro, deixar de lado boas práticas.

Atualmente sou desenvolvedor full stack júnior da área de desenvolvimento de softwares, mirando senioridades cada vez mais altas.

Tenho habilidades com as stacks mais modernas, como :nodeJS, typeScript, css, html, nestJs, NextJs, aws-cloud, bancos de dados não relacionais como mongodb e redis, bancos de dados relacionais como MySql, postgres, docker, testes unitários e de integração. Atuando também em diferentes setores, como educação e telecomunicação.

## Quer entrar em contato com o desenvolvedor?

🪜 Instagram (sempre respondo): @ap_matheus

📱 Telefone e whatsapp: 55 27 997822665

📫 Email: pereira.matheusalves@gmail.com

🔗 Linkedin: https://www.linkedin.com/in/matheus-alves-pereira-4b3781222/
