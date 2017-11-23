---
# RISC X CISC

O projeto do Conjunto de Instruções inicia com a escolha de uma entre duas abordagens, a abordagem RISC e a CISC. O termo **RISC** é a abreviação de **Reduced Instruction Set Computer**, ou Computador de Conjunto de Instruções Reduzido e **CISC** vem de **Complex Instruction Set Computer**, ou Computador de Conjunto de Instruções Complexo. Um computador RISC parte do pressuposto de que um conjunto simples de instruções vai resultar numa Unidade de Controle simples, barata e rápida. Já os computadores CISC visam criar arquiteturas complexas o bastante a ponto de facilitar a construção dos compiladores, assim, programas complexos são compilados em programas de máquina mais curtos. Com programas mais curtos, os computadores CISC precisariam acessar menos a memória para buscar instruções e seriam mais rápidos.

* CISC
* Micoroprogramação: Criar novas funções adicionadas diretamente ao hardware, facilitando o trabalho do programador.
* Resultado: Programas com poucas instruções, resultando uma quantidade menor de acessos à memória.
    * Motivações:
        *  Velocidade da memória vs. velocidade da CPU
        *  Densidade do código: Programas com poucas instruções representam menos acessos à memória.
        *  Compatibilidade entre as máquinas: Manter as instruções de modelos anteriores.
        *  Suporte para as linguagens de alto nível: Aproximar a linguagem das novas linguagens de alto nível e reduzir a disparidade semântica.
    * Desvantagens:
        * Processador **sobrecarregado, complexo, maior e mais lento**.


* RISC
	* 85%  do programa consiste em apenas três tipos de instruções: assinalamentos, comandos if e chamadas de procedimentos
	* Desnecessário a inclusão de microprogramas no processador que quase nunca são utilizados.
    * Instruções complexas devem ser incluídas somente quando o benefício no desempenho compensar a degradação de velocidade.
	* O uso de microprogramação deve ser evitado
			§ Aumento significativo da velocidade das memórias resultou na utilização de software em substituição aos microprogramas.
	* O compilador deve substituir eficientemente as operações complexas eliminadas do hardware.
			§ Otimização é fundamental.
    * O projeto de compiladores deve ser realizado juntamente com o projeto dos processadores.
Em suma, RISC é viável graças ao avanço do software.
    * Vantagens:
        * Processador **mais simples, mais rápido e mais barato.**
        * Menor número de circuitos internos, permite clocks mais altos.
        * Qual é o tamanho do código gerado para uma máquina RISC em relação a uma CISC para um determinado programa ?
            * Geralmente possui mais instruções.
            * Potêncialmente para executar de forma mais eficiente, possui instruções mais simples, com operandos inteiros (tempos de busca e execução de cada instrução é muito menor que o o de uma instrução mais complexa)
            * Trechos de instruções mais simples em linguagem de máquina podem ser melhor utilizados pelo compilador (ao invés de instruções complexas que não podem ser decompostas)
    * Desvantagens:
        * Não são boas para cálculo em ponto flutuante sem a ajuda de hardware.



    ![alt](riscxcisc.png)
* Qual a melhor abordagem ?
Sempre que este assunto é apresentado aos alunos, surge a pergunta crucial sobre qual é a melhor abordagem, a RISC ou a CISC? Esta é uma pergunta difícil e sem resposta definitiva. A melhor resposta que acho é de que depende do uso que se quer fazer do processador.

Processadores RISC geralmente resultam em projetos menores, mais baratos e que consumem menos energia. Isso torna-os muito interessante para dispositivos móveis e computadores portáteis mais simples. Já os processadores CISC trabalham com clock muito elevado, são mais caros e mais poderosos no que diz respeito a desempenho. Entretanto, eles são maiores e consomem mais energia, o que os torna mais indicados para computadores de mesa e notebooks mais poderosos, além de servidores e computadores profissionais.

Os processadores CISC iniciaram com processadores mais simples e depois foram incorporando mais funcionalidades. Os fabricantes, como a Intel e a AMD, precisavam sempre criar novos projetos mas mantendo a compatibilidade com as gerações anteriores. Ou seja, o Conjunto de Instruções executado pelo 486 precisa também ser executado pelo Pentium para os programas continuassem compatíveis. O Pentium IV precisou se manter compatível ao Pentium e o Duo Core é compatível com o Pentium IV. Isso tornou o projeto dos processadores da Intel e AMD muito complexos, mas não pouco eficientes. Os computadores líderes mundiais em competições de desempenho computacional utilizam processadores CISC.

Já o foco dos processadores RISC está na simplicidade e previsibilidade. Além do benefício da previsibilidade do tempo de execução ao Pipeline, ele também é muito interessante para aplicações industriais. Algumas dessas aplicações são chamadas de Aplicações de Tempo Real. Essas aplicações possuem como seu requisito principal o tempo para realizar as tarefas. Assim, o Sistema Operacional precisa saber com quantos milissegundos um programa será executado. Isso só é possível com processadores RISC, com poucos estágios de Pipeline, poucos tipos de instrução, execução em ordem etc. Mesmo que os processadores RISC sejam mais lentos do que os CISC, eles são mais utilizados nessas aplicações críticas e de tempo real, como aplicações industriais, de automação e robótica.

---