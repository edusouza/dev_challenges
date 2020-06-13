Imaginem que somos contratados para desenvolver um software que controle as negociações de bolsa de valores. Mas como funciona uma bolsa de valores?

Temos a Bolsa (a empresa). Nelas, são negociadas ações de diversas empresas. E temos as pessoas (físicas e jurídicas) que compram e vendem ações das empresas listadas em bolsa por valores que elas acham adequados.

- Como funciona as negociações?

Uma pessoa pode colocar ordens de compra e venda.

O que é uma ordem de compra? Uma ordem de compra é o desejo de uma pessoa de comprar uma ação de determinada empresa por um preço (iremos detalhar os tipos de ordens mais pra frente). 

O que é uma ordem de venda? Uma ordem de venda é o desejo de uma pessoa de vender uma ação que possui de determinada empresa por um preço.

Tipos de ordem

Neste exemplo, existem 2 tipos de ordem: Limitada e a mercado

Ordens Limitadas: As ordens limitadas tem esse nome devido à sua natureza. Os valores desejados devem ser atingidos para que a operação seja executada.

Uma ordem de compra limitada é executada sempre que existir uma ordem de venda de outra pessoa por um preço igual ou menor.

Ex.: Foi enviada uma ordem de compra da ação da empresa X por um valor de R$ 1,00. As ordens de venda da mesma ação da empresa X estão a R$ 1,02. Só existirá negócio se houver uma ordem de venda com valor igual ou menor a R$ 1,00.

Uma ordem de venda limitada é executada sempre que existir uma ordem de compra com valores maiores ou iguais ao valor de venda.

Ex.: Foi enviada uma ordem de venda da ação da empresa X por um valor de R$ 1,03. A maior ordem de compra da mesma empresa X é de R$ 1,00. Até que exista uma ordem de compra por R$ 1,03 ou maior (p.ex. R$ 1,06), a ordem não será executada.

Além disso, podem existir mais de uma ordem com o mesmo valor. Nesse caso, devem ser executadas as ordens que chegaram primeiro. 

--
O Desafio

Implementar esse sofware de negociação de ações da Bolsa de valores:

Devemos ter a própria Bolsa, que poderá ter N empresas listadas, ou seja, com ações que podem ser negociadas.

Cada empresa tem um número X de ações.

Também devemos ter as pessoas (física e jurídica) que podem negociar na bolsa. Cada pessoa possui uma carteira, isto é, um valor em dinheiro, que pode ser usado para comprar ou vender ações e as ações que ele comprou.

Cada pessoa também deve ter um histórico de negociações concluídas com sucesso, com o tipo de ordem (compra ou venda), o preço executados e a quantidade executada. Negociações não concluídas não precisam ser guardadas.

Uma pessoa pode enviar quantas ordens quiser, mas a ordem só será executada:
1) Se for uma ordem de venda, só poderá vender a quantidade de ações que já possuir
2) Se for uma ordem de compra, só poderá comprar a quantidade de ações que seu dinheiro permitir.

Para que uma ordem seja executada:

1) Se for uma ordem de compra, a ordem será executada se houver uma ordem de venda com preço menor ou igual ao de compra.
2) se for uma ordem de venda, a ordem será executada se houver uma ordem de compra com preço maior ou igual ao de venda.

Quando a negociação é concluída, as ordens são retiradas, marcadas como concluídas e a quantidade de ações negociadas são transferidas da parte vendedora para a parte compradora. 

Se houver mais de uma ordem de compra para apenas uma ordem de venda, apenas a ordem que chegou primeiro é executada. O mesmo acontece na ponta contrária. Se houver mais de uma ordem de venda para apenas uma ordem de compra, apenas a ordem que chegou primeiro será executada.

Não são permitidas ordens com valores zerados ou negativos. 

- Algumas perguntas que precisam ser respondidas durante o "pregão".

- Qual o market cap de uma determinada empresa? (valor da ação no momento X número de ações disponíveis no mercado)
- Qual o capital de determinada pessoa ($ em posse + (ações * valor de mercado da ação))
- Volume negociado soma(ações * valor negociado)