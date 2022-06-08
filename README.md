<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400"></a></p>

<p align="center">
<a href="https://travis-ci.org/laravel/framework"><img src="https://travis-ci.org/laravel/framework.svg" alt="Build Status"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/dt/laravel/framework" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/v/laravel/framework" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/l/laravel/framework" alt="License"></a>
</p>

## About Laravel

 ## Para consumir a API, deverá ser passado um json no body da requisição com os seguintes parâmetros:
 ~~~
 token -> string
 CpfCliente -> string ( no formato =(000.000.000-00))
 valor -> float
 ~~~
 ~~~ 
 Exemplo:  
 {
	"token":"$2y$10$xhknTbnKuCs/OvmfU/K9Ruex3jMSLUt28hWLjFJvtwKuqpsqwLdvO",
	"CpfCliente":"110.418.659-38",
	"valor":10.00
}
~~~

### Devera ser realizado o cadastro do login no seguinte caminho:
url = http://10.41.1.4/

### Devera ser realizado o cadastro da empresa no seguinte caminho:
url = http://10.41.1.4/empresas/novo

### Para listar Empresas cadastradas
url = http://10.41.1.4/empresas/listar
### OBS: Caso não seja possivel listar a empresa, contate os mestres da API, para fornecer nível de usuario. Ou coloque você mesmo lá no banco nível 1. Voces tem Acesso

### Devera ser realizado o cadastro do cliente no seguinte caminho:
url = http://10.41.1.4/clientes/novo

### A requisição deverá ser feito no seguinte caminho:
url = http://10.41.1.4/api/pagamentos/

## Possíveis status de retornos:
Sucesso: Se a transação de pagamento for concluída com sucesso.
~~~
{
 "status":"Sucesso", 
 "Mensagem":"Pagamento Realizado "
}
~~~
## Serão dois os casos que poderão retornar Insucesso

Insucesso: Saldo cliente indisponível
~~~
{
 "status":"Insucesso", 
 "Mensagem":"Saldo Indisponivel "
}
~~~
Insucesso: Token Não identificado
~~~
{
 "status":"Insucesso", 
 "Mensagem":"Token não identificado "
}
~~~



