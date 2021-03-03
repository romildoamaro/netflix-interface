# netflix-interface

/*main.css*/
:root{
    --vermelho:#E50914;
    --preta:#141414;
}

*{
    margin:0;
    padding:0;
    box-sizing: border-box;  
}

/*elementos base*/

body{
    background: var(--preta);
    font-family: 'Arial', Times, serif;
    color:white;
}

header .container{
    display: flex;
    flex-direction:row;
    align-items: center;
    justify-content: space-between;  
}

header .logo{
    margin-left: 5px;
    color: var(--vermelho);
    font-family: "Arial Black", Times;
    font-size: 40px;
}

header nav a {
    text-decoration: none;
    color: #aaa;
    margin-right:10px; 
}

header nav a:hover{
    color: #fff;
}

/*filme principal*/

.filme-principal{
    
    font-size:16px;
    background-image: url("/img/capa2.jpg") no-repeat; 

 height: 400px;
background-size: cover ;

display: flex;
flex-direction: column;
justify-content: center;
align-items: flex-start;
     
}


.filme-principal .descricao{
    margin-top: 10px;
    margin-bottom: 90px;
}

.titulo{
    margin-top: 15%;
font-size: 40px;
font-family: 'Trebuchet MS,' 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;

}

.botao{
    background-color: rgba(0,0,0,.50);
    border: none;
    color: white;

    padding: 10px 5px;
    margin-right: 15px;
    font-size: 12px;

    cursor: pointer;
    transition: .3s ease all;
}

.botao:hover{
    background-color: white;
    color: black;
}

.botao i{
    margin-right: 8px;
}

.container{
    margin-left: 5px;
}

.filme-principal .container{
    width: 75%;
}

.box-filme{
    height: 100%;
    width: 100%;
    display: block;
}

.carrosel-filmes{
    margin-top: 30px;
}

/*index.html*/

<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Netflix Clone</title>
    <link rel="stylesheet" type="text/css" href="style/main.css" media="screen" />
    
<!--responsividade-->
<link rel="stylesheet" href="style/responsive.css">

    <!--owl css-->
    <link rel="stylesheet" href="style/owl/owl.carousel.min.css">
    <link rel="stylesheet" href="style/owl/owl.theme.default.min.css">
</head>
<body>
    <header>
       <div class="container">
           <h2 class="logo">NETFLIX</h2>
           <nav>
            <a href="#">Inicio</a>
            <a href="#">Séries</a>
            <a href="#">Filmes</a>
            <a href="#">Documentários</a>
           </nav>
        </div>
    </header>
                        <main>
                            <div class="filme-principal">
                                
                                
                              <div class="container">
                                  <h3 class="titulo">LUPIN</h3>
                                  <p class="descricao">Na adolescência, a vida de Assane Diop dá uma guinada radical quando seu pai morre após ser acusado de um crime que não cometeu. Vinte e cinco anos depois, Assane se inspira em "Arsène Lupin, o Ladrão de Casaca" para vingá-lo. Nova temporada disponível.</p>
                                  <div class="botoes">
                                      <button role="button" class="botao">
                                          <i class="fas fa-play"></i>
                                          ASSISTIR AGORA
                                      </button>
                                      <button role="button" class="botao">
                                        <i class="fas fa-info-circle"></i>
                                          MAIS INFORMAÇÕES
                                      </button>
                                  </div>
                            </div>
                            
                           </div> 
                        </main>

                        <div class="carrosel-filmes">
                           <div class="owl-carousel owl-theme">
                               <div class="item">
                                   <img class="box-filme" src="img/img1.jpg" alt="">

                               </div>
                               <div class="item">
                                <img class="box-filme" src="img/img2.jpg" alt="">

                            </div>
                            <div class="item">
                                <img class="box-filme" src="img/img3.jpg" alt="">

                            </div>
                            <div class="item">
                                <img class="box-filme" src="img/img4.jpg" alt="">

                            </div>      
                            <div class="item">
                                <img class="box-filme" src="img/img5.jpg" alt="">

                            </div>      
                            <div class="item">
                                <img class="box-filme" src="img/img6.jpg" alt="">

                            </div>      
                            <div class="item">
                                <img class="box-filme" src="img/img7.jpg" alt="">

                            </div>      
                            <div class="item">
                                <img class="box-filme" src="img/img8.jpg" alt="">

                            </div>      
                            <div class="item">
                                <img class="box-filme" src="img/img9.jpg" alt="">

                            </div>      
                            <div class="item">
                                <img class="box-filme" src="img/img10.jpg" alt="">

                            </div>                            
                           </div>
                        </div>
                    
                        <script src="https://kit.fontawesome.com/477d2921d6.js" crossorigin="anonymous"></script>
                
                        <script src="js/owl/jquery.min.js"></script>
                        <script src="js/owl/owl.carousel.min.js"></script>
                        <script src="js/owl/main.js"></script>
             
</body>
</html>

/*main.js*/

$('.owl-carousel').owlCarousel({
    loop:true,
    margin:10,
    nav:true,
    responsive:{
        0:{
            items:1
        },
        600:{
            items:3
        },
        1000:{
            items:5
        }
    }
})
