# codigo-de-eventos
'use strict';

var readLineSync = require("readline-sync");
var opcao, strData, dataPartes, data, insevento, palestrate, participantes, idade, quantdeEventos;
const numParticipantes = 100;
//criando vetores;
var listadeEventos = [], listaPalestrante = [], listaPartcipantes = [];

do{
    console.log("\n");
    console.log("\t\t------ sistema de cadastro de eventos -----");
    console.log("\t1 - cadastrar evento");
    console.log("\t2 - cadastrar palestrante");
    console.log("\t3 - cadastrar participantes");
    console.log("\t4 - listar evento");
    console.log("\t5 - listar palestrante");
    console.log("\t6 - listar participantes");
    console.log("\t0 - sair do sistema\n");

    opcao = readLineSync.question("\tdigite a opcao desejada:");

    switch(opcao){
    case '1':
        console.log("\t-----cadastro de eventos");
        strData = readLineSync.require("digite a data valida (00/00/0000):");
        dataPartes = strData.split("/");
        data = new Date(dataPartes[2]. dataPartes[1]-1, dataPartes[0]);
        //testando a data para fazer o cadastro de eventos
        if(data < new Date ()){
            console.log("desculpe o evento não pode ser cadastrado!");
        } else {
            insento = readLineSync.question("digite o nome do evento:");
            listaEventos.push(insevento);
        }
    break;
    case '2':
        console.log("\t-----cadastro de palestrante ----");
        palestrante = readLineSync.question("digite o nome do palestrate:");
        listaPalestrante.push(palestrante);
    break;
    case '3':
        console.log("\t----cadastro de participante----");
        participantes = listaParticipantes.lenght;
        if ("digite o numero de participantes:");
        participantes = readlineSync.question("digite o nome do participante:");
        idade = readLineSync.question("digite a idade do participante:");
        if(idade >=18){
        listaPartcipantes.push(participantes);
        console.log("evento completo, não temos mais vagas!!!");
        }else{
            console.log("participante cadastrado com sucesso!!!");
        
             console.log("não é permetido a entrada de menores de 18 anos!!!");  
        }
    break;
    case '4':
        console.log("lista de eventos:");
        quantdeEventos = listadeEventos.length
        console.log("existe" + quantdeEventos + "eventos cadastrados.");
        console.log("o nome do evento é:" + listadeEventos [0]);

    break;
    case '5':
        console.log("lista palestrantes:");
        listaPalestrante = listadeEventos.length
        console.log("existe" + quantpalestrates + "palestrantes cadastrados.");
        console.log("o nome do palestrante é:" + listaPalestrante [0]);

        
    break;
    case '6':
        console.log("lista participantes")
        quantPartipantes = listaPartcipantes.length;
        console.log("existem" + quantPartipantes + "participates cadastrado no evento");
        for(let indice = 0; indice < quantPartipantes; indice++){
            const pAtual = listaPalestrante[indice];
            console.log("o participante n" + (indice + 1) + "é:" + pAtual);
}
    
    break;
    case '0':
    break;
    console.log("\n");
    console.log("\tobrigado por utilizar nosso sistema!!!");
    break;
    default:
        console.log("\topcao invalida! tente novamente!");
    }
 } while(opcao !=0);

