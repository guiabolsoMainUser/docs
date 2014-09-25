# Exemplo do GitHub Pages.  


## Incluindo o `HTML` do _widget_  
Para inicializar nosso `<script>`(_cobriremos na próxima seção_) legal é preciso incluir o seguinte `HTML` para ser usado como container:  

```html
<div id="exemplo-widget" data-width="800" data-height="600"></div>
```

### Os possíveis parâmetros para serem passados ao `widget`:  

* data-width:  
Parâmetro que define a largura do widget  
* data-height:  
Parâmetro que define a altura do widget  
* data-app-id:  
Consiste de seu `appId`. Caso ainda não possua um `appId`, você pode solicitar acesso [enviando-nos um email](mailto:exemplo@widgetlegal.com).  

## Incluindo o `<script>`  
Lorem ipsum dolor sit amet, consectetur adipiscing elit. Praesent eget luctus sapien. Aliquam posuere dictum dolor vel consequat. Fusce sed est fringilla lorem consectetur consequat.  

```html
<script>
    (function(d, s, id) {
        var js, fjs = d.getElementsByTagName(s)[0];
        if (d.getElementById(id)) return;
        js = d.createElement(s);
        js.id = id;
        js.src = "//plugins.guiabolso.local/gb-simulador.js#appId=436020343148643";
        fjs.parentNode.insertBefore(js, fjs);
    }(document, 'script', 'gb-js'));
</script>
```  

