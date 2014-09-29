# GuiaBolso Simulador
---------------------

### Como funciona?
O nosso simulador é um _widget_ que é carregado dinamicamente, sem bloquear o carregamento do conteúdo do seu site (como estilos _CSS_ ou arquivos _JavaScript_). Você insere um elemento `HTML` onde deseja que o _widget_ fique visível na página, e, para inicializar o _widget_, colocará um `<script>` no final da sua página, antes de fechar a _tag_ `<body>`. Este `<script>` então identificará através de um `appId` qual widget carregar, e irá iniciar o _widget_ de acordo com as definições de **largura** e **altura**, como descrevemos em mais detalhes a seguir.  


### Incluindo o `HTML` do _widget_  
Para inicializar nosso `<script>`(_cobriremos na próxima seção_) de inicialização é preciso primeiramente incluir o seguinte `HTML` para ser usado como _container_:  

```html
<div id="gb-widget" data-width="234" data-height="639" data-app-id="{seu appId vem aqui}"></div>
```

> Este `HTML` será usado para definir o lugar onde devemos carregar o conteúdo de nosso _widget_.
> Informe corretamente os parâmetros de **largura** e **altura** para evitar um comportamento indesejado, como por exemplo, quebrar o layout sobrepondo outros elementos da página.  


 - Os parâmetros abaixo devem ser informados para que o `widget` funcione corretamente:  
    - `data-width` (_valor padrão_: 234)  
        Define a **largura** em **pixels** que o _widget_ usará na página. _(Se não for passado nenhum valor, ou o valor passado for menor que o valor padrão, descartaremos o parâmetro passado e utilizaremos o valor padrão)_  
    - `data-height` (_valor padrão_: 639)  
        Define a **altura** em **pixels** que o _widget_ usará na página. _(Se não for passado nenhum valor, ou o valor passado for menor que o valor padrão, descartaremos o parâmetro passado e utilizaremos o valor padrão)_  
    - `data-app-id`  
        É aqui que você deve informar seu `appId`. O `appId` é o que nos permite identificar seu acesso ao _widget_ antes de colocá-lo em sua página. _(Se o `appId` não for informado ou for inválido, o widget não inicializará)_  

> Para solicitar um `appId` envie um email para [dev@guiabolso.com.br](mailto:dev@guiabolso.com.br&subject=Simulador%20appId%20request).  


### Incluindo o `<script>`  
Coloque o seguinte trecho de código antes de fechar a _tag_ `<body>` na página que o _widget_ será carregado:    

```html
<script>
    (function(d, s, id) {
        var js, fjs = d.getElementsByTagName(s)[0];
        if (d.getElementById(id)) return;
        js = d.createElement(s);
        js.id = id;
        js.src = "//plugins.guiabolso.com.br/gb-simulador.js";
        fjs.parentNode.insertBefore(js, fjs);
    }(document, 'script', 'gb-js'));
</script>
```  

