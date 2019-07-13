### Sistemas Operacionais - 2º Bimestre - 2019 - Lista 2



	- Questões da avaliação:
	
### -(1) Questão 1: 
	
		A exigência para que todos os drivers de dispositivos tenham o mesmo padrão serve não só para distinguir o uso de cada dispositivo independente de seu funcionamento individual, como também para simplificar a construção de aplicações e das camadas mais elevadas do próprio sistema operacional. A individualização de interfaces poderia levar a uma utilização mais específica do dispositivo, porém o custo da individualização em quesito performático, de desenvolvimento e de experiência de usuário seria desnecessariamente grande.

### - (2) Questão 2: 

		- a) Raid 0 possui o maior espaço útil de disco dos níveis, pois não precisa manter cópias de segurança.

		- b) Raid 1 poderia ser usado para obter a quantidade de discos de “segurança” necessárias (qualquer que seja, até 3 discos), logo seria a melhor opção para uma grande tolerância de falhas (N-1).

		- c) Especificadamente Raid 0 (striping) seria a melhor opção para um mais alto desempenho de leitura.

		- d) Novamente Raid 0 (striping) seria a melhor opção para um mais alto desempenho, desta vez de escrita.

		- e) Raid 5 seria o nível mais eficaz para manter o espaço útil, as velocidades e tolerância a falhas, já que armazena as informações de paridade uniformemente entre todos os discos, porém preservando um bom desempenho no acesso aos dados e sendo bem mais eficiente no uso do espaço que o espelhamento (Raid 1).

### -(3) Questão 3: 

		Podemos definir o tipo de arquivo de maneiras diferentes, seja pelos últimos caracteres no nome do arquivo (por exemplo imagem1.jpeg), por bytes inseridos no início do arquivo, denominados “números mágicos” (muito usado nos sistemas UNIX), na inserção de atributos adicionais no sistema de arquivos (usado no MacOS9) ou ainda o Tipos MIME, mais voltado para a transferência de arquivos pela internet, que separa os arquivos através de uma notação uniformizada de “tipo/subtipo”. Todos possuem a vantagem de definir o tipo do arquivo, embora a maioria das formas de atribuição contribuam para a incompatibilidade de arquivos entre sistemas específicos, caso a devida conversão não seja feita.

### -(4) Questão 4:

		- a) Falso. Eles não são especificadamente numéricos, sendo na verdade bytes inseridos no início de um arquivo.
		- b) Falso. Embora o sistema operacional windows seja o mais utilizado no mundo, existe toda uma pletora de diferentes sistemas (como e-mail por exemplo) amplamente usados e que definem tipos de arquivos de maneiras diferentes, logo é uma afirmação difícil de se provar.
		- c) Falso. UNIX usam bytes inseridos no começo do arquivo, em vez de caracteres inseridos no final.
		- d) Verdadeiro. A afirmação está correta.
		- e) Verdadeiro.
		- f) Falso. O MIME é utilizado pelo MacOS X e pelo BeOS, enquanto suponho que o LINUX utilize os números mágicos.

### -(5) Questão 5:

		As formas de acesso a arquivos são Acesso Sequencial, geralmente utilizado em todos os sistemas operacionais do mercado utilizando um ponteiro de acesso e seguindo uma sequência no arquivo; Acesso Aleatório, muito importante para bancos de dados, buscando o local específico onde cada leitura e escrita vai ocorrer, sem ter que percorrer o arquivo em sequência; Acesso Mapeado em Memória, usado extensivamente pelo núcleo para carregar código executável, geralmente associa o arquivo a um vetor de bytes equivalente, que pode ser carregado em pedaços caso o arquivo seja muito grande, mas cujas posições são equivalentes ao arquivo; e Acesso Indexado, usado por certos sistemas operacionais, possui uma estrutura interna chave/valor, onde os dados são armazenados no valor e a chave serve como índices.

### - (6) Questão 6:

		Os quatro tipos de travas sobre arquivos compartilhados são: Travas Obrigatórias, impostas pelo núcleo de forma incontrolável, negando o acesso do arquivo a outros processos até que a trava concedida a um processo específico seja retirada; Travas Recomendadas, gerenciadas pelo suporte de execução (bibliotecas), são mais versáteis e podem ser ignoradas por outros processos, mas geralmente são usadas para gerenciar a concorrência entre processos de uma mesma aplicação; Travas Exclusivas, garantem acesso exclusivo ao arquivo, impedindo que outros processos possam ter uma trava própria sobre o arquivo; Travas Compartilhadas, impedem a criação de outras travas sobre o arquivo, mas permitem a existência das que já foram criadas anteriormente.


### - (7) Questão 7:

		As quatro semânticas de acesso a arquivos são: Semântica Imutável, onde um arquivo compartilhado não pode ser modificado, apenas lido; Semântica UNIX, todas as mudanças nos arquivos são visíveis imediatamente a todos os processos que mantêm aquele arquivo aberto; Semântica de Sessão, cada processo usa um arquivo durante uma sessão, que começa quando o arquivo é aberto e finaliza quando ele é fechado, porém todas as mudanças só são vistas pela mesma sessão ou por outras que são abertas após o fechamento dela; Semântica de Transação, similar à semântica de sessão, porém todas as modificações são visíveis de acordo com as operações feitas pelos processos, ao invés da sessão em si.

### - (8) Questão 8:

		A maior parte das operações e estruturas de dados definidas nos discos pelos sistemas operacionais (em geral) são baseadas em blocos lógicos, em que cada arquivo ou diretório ocupa um ou mais blocos lógicos para seu armazenamento. Todo disco é dividido em diversos desses blocos lógicos pelo SO para permitir uma melhor gerência do espaço e melhor desempenho de leitura/escrita.

### - (9) Questão 9:

		Na gestão de blocos livre através de bitmaps, um pequeno conjunto de blocos na área reservada do volume é usado para manter um mapa de bits, com 0 representando uma área livre e 1 uma área já preenchida.

### - (7) Questão 7:
		
		Não há especificada no texto, além dos separadores diferentes (“\” para o windows e “/” para o linux). Por outro lado, poderia ser salientado que apenas o windows separa os discos/partições como unidades diferentes (C:, D:, E:, etc…) enquanto tudo fica no diretório raiz (/) do Linux. O diretório /bin armazena os executáveis, a maior parte dos programas fica em /usr (Unix System Resources) e as bibliotecas ficam em usr/lib. Por outro lado, o Windows mantém partições e nos faz instalar tudo no padrão Arquivos de Programas, que é um diretório da partição escolhida. Os documentos geralmente são salvos na pasta documentos, enquanto no linux é no /home. Logicamente, eles diferem pouco de si, com exceção das hierarquias padrão.
