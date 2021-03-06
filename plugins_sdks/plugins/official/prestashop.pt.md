# Prestashop

* [Requisitos](#Requirements)
* [Funcionalidades](#Features)
* [Instalação](#Installation)
* [Configurar pagamento transparente e redirect](#Configure-Credit-Card-and-Ticket-Standard)
* [Configurar Mercado Envios](#Configure-Mercado-Envios)
* [Suporte](#Support)

O módulo do Mercado Pago para Prestashop esta integrado com as funcionalidades a seguir:

|                                             	| Checkout Basico 	| Checkout Transparente 	|
|---------------------------------------------	|-----------------	|-----------------------	|
| Pagamento com Cartão de Crédito             	| ✔               	| ✔                     	|
| Pagamento com outros meios (Boleto)         	|                 	| ✔                     	|
| Split payments (Two cards)                  	| ✔               	| ✔                     	|
| Pagamento com um click (Clientes e Cartões) 	|                 	| ✔                     	|
| Assinatura (Recorrência)                    	| ✔               	|                       	|
| MercadoEnvios                               	| ✔               	|                       	|
| Devolução de Pagamentos                     	| ✔               	| ✔                     	|
| Atualização do pedido através de Cron       	|                 	| ✔                     	|
| Pagina de sucesso personalizável            	|                 	| ✔                     	|
| Calculadora de Parcelas                     	| ✔               	| ✔                     	|
| Calculadora de mercado envios               	| ✔               	| ✔                     	|

<a name="Requirements"></a>
## Requisitos: ##

|                            | Detalle                                                                                        |
|----------------------------|------------------------------------------------------------------------------------------------|
| Versões Suportadas         | Prestashop 1.6.x - 1.7.x                                                                       |
| Ambiente                   | LAMP (Linux, Apache, MySQL y PHP) ó LNMP stack                                                 |
| Sitema Operacional         | Linux x86, Windows x86-64                                                                      |
| Servidor Web               | Apache 2.x,  Nginx 1.7.x                                                                       |
| Versão PHP                 | PHP 5.6, 5.5 y 5.4                                                                             |
| Versão MySQL               | MySQL 5.6 (Oracle o Percona)                                                                   |
| Dependências               | PDO_MySQL, simplexml, mcrypt, hash, GD, DOM, iconv, curl, SOAP (for Webservices API)           |
| Configurações adicionais   | safe_mode off * memory_limit maior que 256MB (512MB é o recomendado)                           |
| SSL                        | Isso é obrigatório para ir para produção e utilizar nosso checkout transparente, Durante os testes você pode utilizar as credenciais de SandBox sem a necessidade de https.|
  

<a name="Installation"></a>
## Instalação: ##

Esse processo mostra como realizar a instalação via Marketplace:

**Instalação via Marketplace**

1. Ir em **[Prestashop Marketplace](https://addons.prestashop.com/en/payment-card-wallet/23962-mercado-pago.html/)** e clique no botão registrar para Download:
2. Depois do seu registro você pode fazer o download.
![Download](/images/prestashop-download.gif)

3. Agora acesse seu admin e se direcione a Modulos e Serviços.
![Instalação](/images/prestashop-installation.gif)

4. Muito bem! O módulo do Mercado Pago foi instalado com sucesso.
![Configuração](/images/prestashop-installation_success.png)

<a name="Configure-Credit-Card-and-Ticket-Standard"></a>
## Configurar cartão de crédito, boleto e redirect: ##

Esse processo deve de auxiliar a configuração do módulo para pagamentos com checkout transparente e redirecionado:

1. Após a instalação do módulo, se direcione para  **Mercado Pago > Configurar**, agora você precisa obeter suas credenciais.

2. Para obter suas credenciais você deve ir **Mercado Pago - Custom Checkout**, você deverá visualizar os campos **Public Key** e **Access Token**. [Obtenha suas credenciais](https://www.mercadopago.com/mla/account/credentials?type=basic)  
> Existem dois tipos de credenciais:
> * Modo Sandbox: Essa credencial é utilizada para testes.
> * Modo Produção: Essa credencial é utilizada para compras em produção, para isso user a opção de "Eu quero ir para produção".

3. Agora você pode preencher o **client id** e **client secret**, clique no botão **Login**:
![Login](/images/prestashop-credentials_1.gif)

4. Habilite o módulo customizado, preencha o **access token**, **public key** e selecione as opçãos de pagamentos:
![Pagamento transparente](/images/prestashop-credentials_2.gif)

5. Para o Checkout Standard,você precisa apenas habilitar a opção **Configurações - Mercado Pago Standard**:
![Enable Standard](/images/prestashop-standard.gif)

6. Muito bem! Você habilitou pagamentos transparentes e redirect!

<a name="Configure-Mercado-Envios"></a>
## Configurar Mercado Envios: ##

Os passos a seguir vai mostrar como habilitar o Mercado Envios.
> 	IMPORTANTE: O Mercado Envios funciona com o Mercado Pago Redirect e os outros meios de pagamentos serão desabilitados.

1. Primeiro, você precisa [habilitar o Mercado Envios na sua conta](http://shipping.mercadopago.com.ar/optin/doOptin). 

> 	IMPORTANTE: Sua conta do Mercado Pago precisa ser do tipo **Vendedor** e os produtos precisam ter as dimensões corretas.

2. Para habilitar no módulo, você precisa apenas ativar ele na opção **Mercado Envios** e clicar em **Salvar**:
![Habilitar Mercado Envios](/images/prestashop-mercadoenvios_settings.gif)

3. Muito bem! Agora você pode oferecer o Mercado Envios como meio de transportes para seus clientes!

<a name="Support"></a>
## Suporte: ##

> IMPORTANTE: Mantenha a o seu módulo atualizado, e sempre utilize a instalação via Admin ao invés de copiar e colar as pastas.

