# TRABAJOS DE SEPTIEMBRE Y OCTUBRE
## INTEGRANTES:
* Fabrizio Zuñiga
* Adrian Josue Alvarado Sanchez
>Proposito: Afiliar y unir un metodo de pagos de culqi con HTML Y CSS
###### RECOMENDACION:
###### Tener instalador el [**LIVE SERVER**](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer)
## Sistema de Pagos con CULQI
+ Paso 1
   * Comenzar con el index HTML
   * Entrar a [**culqi**](https://afiliate.culqi.com/) para afiliarte

![image](https://github.com/Bloddy20Moon/BuhoSep2023/assets/118792974/991109c2-e568-4c75-8bbc-7fa533df87f3)

+ Paso 2
  * Ya dentro, debes afiliarte llenando tus datos:
![image](https://github.com/Bloddy20Moon/BuhoSep2023/assets/118792974/6bcdbf4a-b300-477b-a3c4-2acb8eb8be87)

+ Paso 3
   * Copiamos el codigo en el HTML
```html
  <script src="https://checkout.culqi.com/js/v4"></script>
</head>
<body>
  <script>
    Culqi.publicKey = 'pk_test_XBWsfPU0w7KmcLF9';
  </script>

  <script>
    Culqi.settings({
      title: 'El TiendoBar',
      currency: 'PEN',
      description: 'Tequila Blanco/Condones',
      amount: 10000,
      order: 'ord_live_0CjjdWhFpEAZlxlz'
    });
  </script>

  <script>
    Culqi.options({
      style: {
        logo: 'IMG/unnamed.png',
        maincolor: '#0ec1c1',
        buttontext: '#ffffff',
        maintext: '#4A4A4A',
        desctext: '#4A4A4A'
      }
    });
  </script>

  <div class="container">
    <div class="payment-form">
      <h1>Realizar Pago</h1>
      <form id="payment-form">
        <div class="form-group">
          <label for="card-number">Número de Tarjeta</label>
          <input type="text" id="card-number" pattern="[0-9]*" inputmode="numeric" placeholder="Ingrese su número de tarjeta" required>
        </div>
        
        <div class="form-group">
          <label for="expiry">Fecha de Vencimiento</label>
          <input type="text" id="expiry" pattern="[0-9]*" inputmode="numeric" placeholder="MM/YY" required>
        </div>
        
        <div class="form-group">
          <label for="cvv">Código de Seguridad (CVV)</label>
          <input type="text" id="cvv" pattern="[0-9]*" inputmode="numeric" placeholder="CVV" required>
        </div>
        
        <button id="btn_pagar">Pagar</button>
      </form>
    </div>
  </div>

  <script>
    const btn_pagar = document.getElementById('btn_pagar');
  
    btn_pagar.addEventListener('click', function (e) {
      Culqi.open();
      e.preventDefault();
    });
  </script>

  <script>
    function culqi() {
      if (Culqi.token) {  
        const token = Culqi.token;
        console.log(`Se ha creado el objeto Token: ${token}.`);
      } else if (Culqi.order) {  
        const order = Culqi.order;
        console.log(`Se ha creado el objeto Order: ${order}. para PagoEfectivo`);
      } else {
        console.log(`Error: ${Culqi.error.merchant_message}.`);
      }
    }
  </script>
```
+ Paso 4
   * Para que no se vea vacio tome un fondo de la pagina de [**svgbackgrounds**](https://www.svgbackgrounds.com/backgrounds/)
![image](https://github.com/Bloddy20Moon/BuhoSep2023/assets/118792974/0b2e085a-469f-4757-84e2-247910bb7fac)


+ Paso 5
   * Ya con todo quedaría la pagina así:
![image](https://github.com/Bloddy20Moon/BuhoSep2023/assets/118792974/45fe9f91-3dd7-43d5-beae-006acfac2b90)
    * El archivo esta en el github, si deseas entrar, [**pulsa aqui**](https://github.com/Bloddy20Moon/BuhoSep2023/tree/main/Culqui)



https://github.com/Bloddy20Moon/BuhoSep2023/assets/118792974/42f0f6b8-4e74-4008-9ffc-41d6897af2f8

