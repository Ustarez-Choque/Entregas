#Sistema Bancario con Java 
##Descripción
Este proyecto consiste en el modelado de un sistema bancario orientado a objetos, cuyo objetivo es administrar los clientes y las cuentas de un banco, permitiendo realizar diferentes operaciones financieras según el tipo de cuenta. El sistema contempla distintos tipos de clientes y cuentas, aplicando los principios de la Programación Orientada a Objetos (POO), como la herencia, el encapsulamiento, el polimorfismo y la abstracción.
Además, se incorpora un nuevo producto bancario a la Cuenta Convertibilidad, que permite operar tanto en pesos como en dólares.

###- Clientes
El sistema contempla dos tipos de clientes, identificados mediante un número único de cliente.

###- Cliente individual
Atributos:
Número de cliente.
Nombre.
Apellido.
DNI.

###- Cliente empresa
Atributos:
Número de cliente.
Nombre de fantasía.
CUIT.

Tipos de cuentas
Todas las cuentas bancarias poseen un número de cuenta, un cliente asociado y un saldo. Cada tipo de cuenta implementa sus propias reglas de operación.

1. Caja de Ahorro
Permite administrar dinero y obtener intereses mensuales.

Atributos:
Número de cuenta.
Cliente asociado.
Saldo.
Tasa de interés.

Operaciones:
Depositar efectivo: permite ingresar dinero sin restricciones de monto máximo.
Extraer efectivo: permite retirar dinero siempre que no se supere el saldo disponible.
Cobrar intereses: permite acreditar los intereses mensuales correspondientes según la tasa establecida.

2. Cuenta Corriente
Permite operar con efectivo y cheques, además de utilizar un monto autorizado para girar en descubierto.

Atributos:
Número de cuenta.
Cliente asociado.
Saldo.
Monto autorizado para giro en descubierto.

Operaciones:
Depositar efectivo: permite ingresar dinero en la cuenta.
Depositar cheques: permite depositar cheques que contienen un monto, un banco emisor y una fecha de pago.
Extraer efectivo: permite retirar dinero utilizando el saldo disponible y, si es necesario, el límite autorizado de descubierto.

3. Cuenta Convertibilidad
Es un nuevo producto destinado exclusivamente a clientes empresa. Permite operar con pesos argentinos y dólares estadounidenses.

Atributos:
Número de cuenta.
Cliente empresa asociado.
Saldo en pesos.
Saldo en dólares.
Monto autorizado para giro en descubierto en pesos.
Tasa de conversión entre pesos y dólares.

Operaciones:
Depositar efectivo: permite ingresar pesos.
Extraer efectivo: permite retirar pesos utilizando el saldo y el límite autorizado de descubierto.
Depositar dólares: permite incrementar el saldo en dólares.
Extraer dólares: permite retirar dólares siempre que exista saldo suficiente, sin posibilidad de utilizar el giro en descubierto.
Depositar cheques: permite depositar cheques, siguiendo las reglas de la cuenta corriente.
Convertir pesos a dólares: permite convertir un monto en pesos a dólares mediante una tasa de conversión configurable.
Convertir dólares a pesos: permite convertir un monto en dólares a pesos mediante una tasa de conversión configurable.
Las operaciones de conversión deben validar los saldos disponibles y aplicar la tasa correspondiente como parámetro.
