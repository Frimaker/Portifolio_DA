# Criando um Schema
Considerando um exemplo de loja generico, primeiro deve-se criar um diagrama do modelo do banco de dados e colocando todas as chaves primárias com autoincremento.

Tenha em mente que as relações dessas tabelas são de 1:N (uma para muitos), cada município na tabela pode estar atrelado ao mesmo estado porque um estado tem mais de um município e não o contrário, vários clientes podem ter o mesmo municipio e várias contas a receber podem ser do mesmo cliente.

Porém, para que as referências possam ser feitas, que a criação das tabelas siga esta ordem: “estado”, “município”, “cliente”, “contareceber”. Visto que “estado” possui apenas chave primária, ele deve ser a primeira tabela criada e em seguida a tabela “município” que possui como chave estrangeira o ID de “estado”, e assim por diante.

Agora é preciso copiar os scripts em SQL e executá-los na query, assim teremos criado o banco de dados e adicionado as suas tabelas.

![Criando um Schema0](https://github.com/Frimaker/frimaker.github.io/blob/main/frimakerPNG/Criando%20um%20Schema/Criando%20um%20schema0.png?raw=true)

![Criando um Schema1](https://github.com/Frimaker/frimaker.github.io/blob/main/frimakerPNG/Criando%20um%20Schema/Criando%20um%20schema1.png?raw=true)

## Lembrando que deve-se colocar as **contraints** nas foreign keys para evitar que falte dados

### "ON DELETE NO ACTION" e "ON UPDATE NO ACTION"

![Criando um Schema2](https://github.com/Frimaker/frimaker.github.io/blob/main/frimakerPNG/Criando%20um%20Schema/Criando%20um%20schema2.png?raw=true)

## Agora devemos testar o banco inserindo alguns dados.

![Criando um Schema3](https://github.com/Frimaker/frimaker.github.io/blob/main/frimakerPNG/Criando%20um%20Schema/Criando%20um%20schema3.png?raw=true)
![Criando um Schema4](https://github.com/Frimaker/frimaker.github.io/blob/main/frimakerPNG/Criando%20um%20Schema/Criando%20um%20schema4.png?raw=true)
![Criando um Schema5](https://github.com/Frimaker/frimaker.github.io/blob/main/frimakerPNG/Criando%20um%20Schema/Criando%20um%20schema5.png?raw=true)
![Criando um Schema6](https://github.com/Frimaker/frimaker.github.io/blob/main/frimakerPNG/Criando%20um%20Schema/Criando%20um%20schema6.png?raw=true)


Agora basta criar a visão (VIEW) e executá-la para vermos o resultado esperado:

• ID da conta a receber 

• Nome e CPF do Cliente associado à conta 

• Data de vencimento da conta 

• Valor da conta

![Criando um Schema7](https://github.com/Frimaker/frimaker.github.io/blob/main/frimakerPNG/Criando%20um%20Schema/Criando%20um%20schema7.png?raw=true)

Assim mantemos tudo organizado, compartimentalizado e fácil de conectar quando precisar retirar informações específicas.
