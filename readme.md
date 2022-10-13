# Documentacion

- Primero analice las paginas para revisar su estructura y ver los contenedores que necesitaba modificar, ademas de ver el video de como deberia quedar, y pensar que estilos iba a usar
- linke los estilos "practice" a todas las paginas para comenzar a trabajar

        <link rel="stylesheet" href="css/practice.css">

- Vi que todas la paginas tenian una estructura similar por lo que comienzo a crear estilos generales para no usar demasiado css y acomodar el 60% de la pagina en todas las paginas

        .wrap-body{
            display: flex;
            flex-direction: column;
            justify-content: flex-start;
            align-items: center;
        }
        header, #container, footer{
            width: 1000px;
        }
        header{
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

- Ademas agregue un par de clases nuevas para trabajar mas comodamente, por ejemplo en el footer

        .f-i{
            display: grid;
            grid-template: 1fr / repeat(3, 1fr);
            gap: 20px;
        }

- Comence organizando la primera pagina, dandole un display grid a el contenedor de los hover

        .c-b{
            display: grid;
            grid-template: repeat(3, 1fr) / 1fr repeat(2,100px) 1fr;
        }
        .c-b > div{
        width: 100%;
        }
        .c-b >div:nth-child(2){
            grid-column: 2 / 5;
        }
        .c-b >div:nth-child(3){
            grid-column: 1 / 4;
        }
        .c-b >div:nth-child(5){
            grid-column: 1 / 3;
        }
        .c-b >div:nth-child(6){
            grid-column: 3 / 5;
        }

- Segui con la modelo debajo del mismo aplicando estos estilos

        .box-text{
            display: grid;
            grid-template: 1fr / repeat(2, 1fr);
            justify-items: center;
        }
        .box-text > *{
            grid-column: 1;
        }
        .box-text a{
            width: 180px;
        }

- La pagina About quedo igual al video con los estilos generales, solo corregi su contenedor interno con un grid

        .c-f{
            display: grid;
            grid-template: 1fr / repeat(3, 1fr);
            gap: 30px;
        }

- En la pagina del blog vi que ya tenia un grid solo estaba mal hecho y solo corregi lo que estaba mal, ademas de darle un width a las imagenes ya que no lo tenian y por esto no se mostraban, ademas ya estaban cuadradas donde deberian

        .archive-post .box-text{
            grid-template: 1fr/ 1fr;
            justify-items: inherit;
        }
        .archive-post .box-image{
            width: 500px;
        }

- En la pagina del formulario solo agregue un display grid y un margin al h3 para que quedara identica al video

        .f-i{
            display: grid;
            grid-template: 1fr / repeat(3, 1fr);
            gap: 20px;
        }
        .contact-form h3{
            margin: 0;
            padding: 40px 0 60px;
        }

- Con estos pocos estilos arregle todas las paginas completamente, para que se viera como en el video
- Solo tuve un error y fue usar este estilo al principio del todo, el cual comente para dejar registro, al usarlo descuadraba todo porque es una clase muy usada en las paginas, entonces segui analizando la pagina buscando una solucion mejor, el cual remplace con .wrap-body

        .row{
            display: flex;
            justify-content: space-between;
            align-items: center;
        }



Designed by Zerotheme
Website : http://www.zerotheme.com
Zerogrid System for Responsive Design - http://www.zerotheme.com/zerogrid-a-simple-grid-system-for-responsive-design

/*----License----*/
+ You have the rights to use the resources for personal and commercial project(s) purposes.
+ You are not allowed to remove back link at the footer in template. You should contact us about this. http://www.zerotheme.com/contact-us
+ You are allowed to remove back link with basic templates. You can find basic templates at http://www.zerotheme.com/free-basic-responsive-html5-themes
+ You can not resell, redistribute, license, or sub-license any of the templates without direct permission from Zerotheme.com.
+ You are not allowed to provide direct link to download or preview template. You must link back to Zerotheme template page where users can find the download and preview template.
