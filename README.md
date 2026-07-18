# Sistema de Aquisição e Monitoramento de Dados OBD-II utilizando LabVIEW e ELM327

## Descrição

Este projeto apresenta o desenvolvimento de uma aplicação em **LabVIEW** para aquisição, processamento e armazenamento
de dados provenientes da interface de diagnóstico automotivo **OBD-II**, utilizando um adaptador **ELM327** conectado via protocolo **TCP/IP**.

O sistema foi desenvolvido como parte da disciplina de **Instrumentação** do curso de
Engenharia Mecânica da Universidade Federal do Amazonas (UFAM), tendo como objetivo monitorar parâmetros operacionais
de um motor **Ford Zetec 1.8** em tempo real.

A aplicação realiza a comunicação com a ECU do veículo, interpreta as respostas do protocolo OBD-II, converte
os valores para unidades físicas conforme a norma SAE J1979 e apresenta os resultados em uma interface gráfica desenvolvida em LabVIEW.

---

## Funcionalidades

- Comunicação TCP/IP com o adaptador ELM327;
- Envio de comandos OBD-II;
- Leitura das respostas da ECU;
- Tratamento e limpeza das strings recebidas;
- Conversão automática dos dados utilizando as equações da norma SAE J1979;
- Exibição dos parâmetros em tempo real;
- Geração de gráficos temporais (Waveform Charts);
- Aquisição contínua dos dados experimentais;
- Exportação automática dos resultados para arquivos CSV;
- Interface gráfica desenvolvida em LabVIEW.

---

## Parâmetros monitorados

Atualmente o sistema é capaz de adquirir os seguintes PIDs:

| PID | Parâmetro |
|------|-----------|
| 0105 | Temperatura do fluido de arrefecimento |
| 010C | RPM do motor |
| 010D | Velocidade do veículo |
| 010F | Temperatura do ar de admissão |
| 0110 | Vazão mássica de ar (MAF) |
| 0111 | Posição da borboleta |
| 010B | Pressão absoluta do coletor (MAP) |
| 0142 | Tensão do módulo de controle |
| 012F | Nível de combustível |
| 0100 | PIDs suportados pela ECU |

---

## Tecnologias utilizadas

- LabVIEW
- TCP/IP
- OBD-II
- ELM327
- SAE J1979
- CSV
- Microsoft Excel

---

## Funcionamento

O sistema estabelece comunicação com o ELM327 via rede TCP/IP. Após a conexão, comandos de inicialização podem ser enviados ao
dispositivo para configuração da comunicação.

Em seguida, o usuário informa o PID desejado e o software envia automaticamente o comando à ECU.
A resposta recebida é tratada por rotinas de processamento de strings, convertida para unidades físicas através das
equações definidas pela norma SAE J1979 e apresentada em tempo real na interface.

Durante o ensaio, os dados são armazenados continuamente em memória por meio de Shift Registers e Arrays.
Ao final da aquisição, todas as amostras são organizadas em uma matriz e exportadas para um arquivo CSV, permitindo
análises posteriores em softwares como Microsoft Excel, MATLAB ou Python.

---

## Estrutura do projeto

```
Projeto
│
├── Interface LabVIEW
├── Comunicação TCP/IP
├── Processamento das respostas
├── Conversão dos PIDs
├── Gráficos em tempo real
├── Aquisição de dados
└── Exportação CSV
```

---

## Aplicações

Este projeto pode ser utilizado em:

- Ensino de Instrumentação;
- Diagnóstico automotivo;
- Monitoramento de motores;
- Aquisição experimental de dados;
- Estudos sobre protocolos OBD-II;
- Desenvolvimento de sistemas de monitoramento veicular.

---

## Autores

**Tiago de Moura Xavier**
**Lucas de Amaral Correa**
**João Pedro Pereira e Pereira**

Graduandos em Engenharia Mecânica  
Universidade Federal do Amazonas (UFAM)

---

Este projeto foi desenvolvido para fins acadêmicos e educacionais.
