Project Notes

• A colocação do Font Awesome serviu na primeira parte do projeto para introduzir o botão "maiszinho", botão de "editar" e o botão da pesquisa ao lado das caixas de input.

• Dentro do arquivo de CSS temos uma linha de código que se refere ao pointer-events:
    /* pointer-events serviu pois se clicarmos no botão o evento vai ser disparado, mas se clicarmos no ícone não seria disparado */

• EXPLICAÇÃO 01 = agora precisamos identificar o clique nos botões das tarefas já adicionadas.
    Então como existem elemento que são adicionados dinamicamente, então o mais efetivo é adicionar um evento no documento inteiro (document.addEventListener()). Dentro desse evento conseguimos identificar o elemento que foi clicado e assim que eu clicar nele, ele terá que executar um evento que pedirmos.

    • explicação 01.1 = as coisas feitas nesse evento são aplicadas no elemento "pai" então precisamos dele também.
    Usamos o closest("div"), pois queremos selecionar a "div" mais próxima, que neste caso é o elemento "pai" mais próximo.


• toggle("done") = serve para alternarmos. Ex: climamos para finalizarmos uma tarefa, mas podemos ter clicado por engano e queremos que ela volte.

• preventDefault() = Cancela o evento se for cancelável, sem parar a propagação do mesmo.