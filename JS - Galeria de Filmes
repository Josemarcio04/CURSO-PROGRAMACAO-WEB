function criarVetorFilmes(){
    let vetorFilmes = [
        {titulo: "Matrix", genero: "Ação", ano: 1999, nota: 5},
        {titulo: "Titanic", genero: "Romance", ano: 1997, nota: 4},
        {titulo: "Coringa", genero: "Drama", ano: 2019, nota: 5},
        {titulo: "Vingadores: Ultimato", genero: "Ação", ano: 2019, nota: 2},
        {titulo: "Parasita", genero: "Drama", ano: 2019, nota: 0},
        {titulo: "À procura do amor", genero: "Romance", ano: 2013, nota: 3},
        {titulo: "Indiana Jones e os Caçadores da Arca Perdida", genero: "Aventura", ano: 1981, nota: 2},
        {titulo: "O Senhor dos Anéis: A Sociedade do Anel", genero: "Aventura", ano: 2001, nota: 5},
        {titulo: "As Branquelas", genero: "Comédia", ano: 2004, nota: 1},
        {titulo: "Se Beber, Não Case!", genero: "Comédia", ano: 2009, nota: 3},
        {titulo: "Interestelar", genero: "Aventura", ano: 2014, nota: 5},
        {titulo: "Jurassic Park", genero: "Aventura", ano: 1993, nota: 5},
        {titulo: "Toy Story", genero: "Comédia", ano: 1995, nota: 4},
        {titulo: "Homem-Aranha: Sem Volta Para Casa", genero: "Ação", ano: 2021, nota: 5},
        {titulo: "Forrest Gump", genero: "Drama", ano: 1994, nota: 5}
    ]

    return vetorFilmes;
}

function filtrarInput(vetorFilmes){

    let input = document.getElementById("input");
    let textoInput = input.value.toLowerCase();

    if (textoInput !== ""){
        vetorFilmes = vetorFilmes.filter(function(filme){
            return filme.titulo.toLowerCase().includes(textoInput);
        });
    }

    return vetorFilmes;
}

function filtrarGenero(vetorFilmes){

    let selectGenero = document.getElementById("selectGenero");

    if (selectGenero.value === "Ação"){
        vetorFilmes = vetorFilmes.filter(function(filme){
            return filme.genero === "Ação";
        });
    } else if (selectGenero.value === "Romance"){
        vetorFilmes = vetorFilmes.filter(function(filme){
            return filme.genero === "Romance";
        });
    } else if (selectGenero.value === "Aventura"){
        vetorFilmes = vetorFilmes.filter(function(filme){
            return filme.genero === "Aventura";
        });
    } else if (selectGenero.value === "Drama"){
        vetorFilmes = vetorFilmes.filter(function(filme){
            return filme.genero === "Drama";
        });
    } else if (selectGenero.value === "Comédia"){
        vetorFilmes = vetorFilmes.filter(function(filme){
                return filme.genero === "Comédia";
            });
        };

    return vetorFilmes;
}

function filtrarNota(vetorFilmes){

    let selectNota = document.getElementById("selectNota");

    if (selectNota.value === "0"){
        vetorFilmes = vetorFilmes.filter(function(filme){
            return filme.nota >= 0;
        });
    } else if (selectNota.value === "1"){
        vetorFilmes = vetorFilmes.filter(function(filme){
            return filme.nota >= 1;
        });
    } else if (selectNota.value === "2"){
        vetorFilmes = vetorFilmes.filter(function(filme){
            return filme.nota >= 2;
        });
    } else if (selectNota.value === "3"){
        vetorFilmes = vetorFilmes.filter(function(filme){
            return filme.nota >= 3;
        });
    } else if (selectNota.value === "4"){
        vetorFilmes = vetorFilmes.filter(function(filme){
            return filme.nota >= 4;
        });
    } else if (selectNota.value === "5"){
        vetorFilmes = vetorFilmes.filter(function(filme){
            return filme.nota >= 5;
        });
    }

    return vetorFilmes;
}

function ordenar(vetorFilmes){

    let selectOrdenar = document.getElementById("selectOrdenar");

    if (selectOrdenar.value === "Alfabética"){
        vetorFilmes.sort(function(a, b){
            return a.titulo.localeCompare(b.titulo);
        });
    } else if (selectOrdenar.value === "Ano crescente"){
        vetorFilmes.sort(function(a, b){
            return a.ano - b.ano;
        });

    } else if (selectOrdenar.value === "Ano decrescente"){
        vetorFilmes.sort(function(a, b){
            return b.ano - a.ano;
        });
    }

    return vetorFilmes;
}

function ordenarPorDecada(vetorFilmes){

    let selectDecada = document.getElementById("selectDecada");

    for (let i = 0; i < vetorFilmes.length; i++){
        
        if (selectDecada.value === "Anos 70"){
            vetorFilmes = vetorFilmes.filter(function(filme){
                return filme.ano >= 1970 && filme.ano <= 1979;
            });
        } else if (selectDecada.value === "Anos 80"){
            vetorFilmes = vetorFilmes.filter(function(filme){
                return filme.ano >= 1980 && filme.ano <= 1989;
            });
        } else if (selectDecada.value === "Anos 90"){
            vetorFilmes = vetorFilmes.filter(function(filme){
                return filme.ano >= 1990 && filme.ano <= 1999;
            });
        } else if (selectDecada.value === "Anos 2000"){
            vetorFilmes = vetorFilmes.filter(function(filme){
                return filme.ano >= 2000 && filme.ano <= 2009;
            });
        } else if (selectDecada.value === "Anos 2010+"){
            vetorFilmes = vetorFilmes.filter(function(filme){
                return filme.ano >= 2010;
            });
        }
    }

    return vetorFilmes;
}

function atualizarContador(vetorFilmesFiltrado, vetorFilmes){
    let totalFilmesFiltrado = document.getElementById("totalFilmesFiltrado");
    let totalFilmes = document.getElementById("totalFilmes");

    totalFilmesFiltrado.textContent = vetorFilmesFiltrado.length;
    totalFilmes.textContent = vetorFilmes.length;
}

function formatarContainerPorGenero(container, genero){

    if (container.classList.contains("containerRomance" || "containerAcao" || "containerAventura" || "containerComedia" || "containerDrama")){

        // Nada a fazer. Caso em que anteriormente ja foi adicionada uma classe ao container.
    } else {

        if (genero === "Romance"){
            container.classList.add("containerRomance");
        } else if (genero === "Ação"){
            container.classList.add("containerAcao");
        } else if (genero === "Aventura"){
            container.classList.add("containerAventura");
        } else if (genero === "Comédia"){
            container.classList.add("containerComedia");
        } else  if (genero === "Drama"){
            container.classList.add("containerDrama");
        }
    }
}

function contrutorCopiaContainer(titulo, genero, ano, nota, botaoFavoritar){
    let containerCopia = document.createElement("div");
    containerCopia.id = "copiaContainer" + titulo;
    formatarContainerPorGenero(containerCopia, genero);

    let tituloCopia = document.createElement("h3");
    tituloCopia.id = "tituloCopia" + titulo;
    tituloCopia.textContent = titulo;
    containerCopia.appendChild(tituloCopia);

    let generoCopia = document.createElement("p");
    generoCopia.textContent = genero;
    containerCopia.appendChild(generoCopia);

    let anoCopia = document.createElement("p");
    anoCopia.textContent = ano;
    containerCopia.appendChild(anoCopia);

    let notaCopia = document.createElement("p");
    notaCopia.textContent = nota;
    containerCopia.appendChild(notaCopia);

    let botaoFavoritarCopia = document.createElement("button");
    botaoFavoritarCopia.id = "botaoFavoritarCopia" + titulo;
    botaoFavoritarCopia.textContent = "⭐ Favoritar";
    botaoFavoritarCopia.classList.add("botaoFavorito");
    botaoFavoritarCopia.addEventListener("click", function(){
        let containerCopia = document.getElementById("copiaContainer" + titulo);
        let painelFavoritos = document.getElementById("painelFavoritos");
        painelFavoritos.removeChild(containerCopia);

        if(painelFavoritos.children.length === 0){
            let tituloPainelFavoritos = document.getElementById("tituloPainelFavoritos");
            tituloPainelFavoritos.textContent = "";
        }
        
        botaoFavoritar.classList.remove("botaoFavorito");
    });

    containerCopia.appendChild(botaoFavoritarCopia);

    return containerCopia;
}

function adicionarOuRemoverFavoritos(titulo, genero, ano, nota, botaoFavoritar){

    botaoFavoritar.classList.toggle("botaoFavorito");
    
    if (botaoFavoritar.classList.contains("botaoFavorito")){ // Adicionar

        let tituloPainelFavoritos = document.getElementById("tituloPainelFavoritos");
        tituloPainelFavoritos.textContent = "⭐ Filmes Favoritos";
        let copiaContainer = contrutorCopiaContainer(titulo, genero, ano, nota, botaoFavoritar);
        let painelFavoritos = document.getElementById("painelFavoritos");
        painelFavoritos.appendChild(copiaContainer);

    } else{ // Remover

        let copiaContainer = document.getElementById("copiaContainer" + titulo);
        let painelFavoritos = document.getElementById("painelFavoritos");
        painelFavoritos.removeChild(copiaContainer);

        if(painelFavoritos.children.length === 0){
            let tituloPainelFavoritos = document.getElementById("tituloPainelFavoritos");
            tituloPainelFavoritos.textContent = "";
        }
    }
}

function formatarBotaoFavoritar(titulo, botaoFavoritar){

    let tituloCopia = document.getElementById("tituloCopia" + titulo);
    if(tituloCopia === null || tituloCopia === undefined){
        // Nada a fazer. Caso em que não há titulos com esse nome nos favoritos.
    } else {
        // Há titulos com esse nome nos favoritos.
        botaoFavoritar.classList.add("botaoFavorito");
    }
}

function exibirFilmes(vetorFilmes){

    let painel = document.getElementById("painel");
    painel.textContent = "";

    for (let i = 0 ; i< vetorFilmes.length; i++){

        let container = document.createElement("div");
        formatarContainerPorGenero(container, vetorFilmes[i].genero);
        painel.appendChild(container);

        let titulo = document.createElement("h3");
        titulo.textContent = vetorFilmes[i].titulo;
        container.appendChild(titulo);

        let genero = document.createElement("p");
        genero.textContent = vetorFilmes[i].genero;
        container.appendChild(genero);

        let ano = document.createElement("p");
        ano.textContent = vetorFilmes[i].ano;
        container.appendChild(ano);

        let nota = document.createElement("p");
        nota.textContent = vetorFilmes[i].nota + " / 5 ⭐";
        container.appendChild(nota);

        let botaoFavoritar = document.createElement("button");
        botaoFavoritar.textContent = "⭐ Favoritar";
        formatarBotaoFavoritar(titulo.textContent, botaoFavoritar);
        botaoFavoritar.addEventListener("click", function(){

            adicionarOuRemoverFavoritos(titulo.textContent, genero.textContent, ano.textContent, nota.textContent, botaoFavoritar);
        });
        container.appendChild(botaoFavoritar);
    }    
}

function filtrarEExibir(vetorFilmes){

    let vetorFilmesFiltrado = filtrarInput(vetorFilmes);
    
    vetorFilmesFiltrado = filtrarGenero(vetorFilmesFiltrado);

    vetorFilmesFiltrado = filtrarNota(vetorFilmesFiltrado);

    vetorFilmesFiltrado = ordenar(vetorFilmesFiltrado);

    vetorFilmesFiltrado = ordenarPorDecada(vetorFilmesFiltrado);

    atualizarContador(vetorFilmesFiltrado, vetorFilmes);

    exibirFilmes(vetorFilmesFiltrado);
}

function limparFiltros(vetorFilmes){

    let selectGenero = document.getElementById("selectGenero");
    let selectNota = document.getElementById("selectNota");
    let selectOrdenar = document.getElementById("selectOrdenar");
    let selectDecada = document.getElementById("selectDecada");
    let input = document.getElementById("input");

    selectGenero.value = "Todos";
    selectNota.value = "Todas";
    selectOrdenar.value = "Padrão";
    selectDecada.value = "Todas";
    input.value = "";

    filtrarEExibir(vetorFilmes);
}

function alternarModo(){

    let corpo = document.getElementById("corpo");
    let botaoModo = document.getElementById("botaoModo");

    corpo.classList.toggle("modoEscuro");

    if (corpo.classList.contains("modoEscuro")){
        botaoModo.classList.remove("botaoModoEscuro");
        botaoModo.classList.add("botaoModoClaro");
        botaoModo.textContent = "☀️ Modo Claro";
    } else{
        botaoModo.classList.remove("botaoModoClaro");
        botaoModo.classList.add("botaoModoEscuro");
        botaoModo.textContent = "🌙 Modo Escuro";
    }
}

let vetorFilmes = criarVetorFilmes();

filtrarEExibir(vetorFilmes);

let selectGenero = document.getElementById("selectGenero");
selectGenero.addEventListener("change", function(){
    filtrarEExibir(vetorFilmes);
});

let selectNota = document.getElementById("selectNota");
selectNota.addEventListener("change", function(){
    filtrarEExibir(vetorFilmes);
});

let selectOrdenar = document.getElementById("selectOrdenar");
selectOrdenar.addEventListener("change", function(){
    filtrarEExibir(vetorFilmes);
});

let selectDecada = document.getElementById("selectDecada");
selectDecada.addEventListener("change", function(){
    filtrarEExibir(vetorFilmes);
});

let botaoLimparFiltros = document.getElementById("botaoLimparFiltros");
botaoLimparFiltros.addEventListener("click", function(){
    limparFiltros(vetorFilmes);
});

let input = document.getElementById("input");
input.addEventListener("input", function(){
    filtrarEExibir(vetorFilmes);
});

let botaoModo = document.getElementById("botaoModo");
botaoModo.addEventListener("click", function(){
    alternarModo();
});
