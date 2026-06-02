# Simulacao-Redes-de-Computadores-C
Universidade de Vassouras<Br>
Disciplina Estrutura de Dados<Br>
Professor: Gioliano Albertoni <Br>



**Exercício 5 - Simulação de Redes de Computadores**  

Você foi contratado para simular uma rede simples de computadores que utiliza comutação de
pacotes.  
Cada pacote enviado pela rede possui:  
• número do pacote  
• tamanho (KB)  
• tempo estimado de transmissão  
Implemente o sistema usando fila, pilha e lista encadeada.  

**Parte 1 — Fila (Pacotes aguardando transmissão)**  
Os pacotes chegam à interface de rede e aguardam envio.  
Use uma fila para armazenar os pacotes na ordem de chegada.  
Operações:  
• adicionar pacote à fila  
• transmitir (remover) próximo pacote  
• mostrar fila de espera  
Pacotes recebidos:  
• Pacote 1 → 500 KB  
• Pacote 2 → 300 KB  
• Pacote 3 → 700 KB  
• Pacote 4 → 200 KB  
**Pergunta:  
Qual pacote será transmitido primeiro?** 
O primeiro pacote transmitido será o Pacote 1, porque a fila segue o modelo FIFO (First In, First Out), onde o primeiro elemento que entra é o primeiro a sair.

**Parte 2 — Pilha (Pacotes com erro)**
Pacotes que falharam na transmissão devem ser armazenados para retransmissão.
Use uma pilha.
Operações:  
• registrar pacote com erro  
• retransmitir último pacote com erro  
• mostrar pilha  
Exemplo:  
Pacote 2 falhou  
Pacote 4 falhou  
**Pergunta:
Qual será retransmitido primeiro?**  
O primeiro pacote retransmitido será o Pacote 4, porque a pilha segue o modelo LIFO (Last In, First Out), onde o último elemento inserido é o primeiro a ser removido.

**Parte 3 — Lista Encadeada (Pacotes ativos na rede)**  
Os pacotes atualmente circulando pela rede devem ser mantidos em uma lista.  
Cada pacote deve conter:  
• ID  
• origem  
• destino  
• status (em trânsito / entregue)  
Operações:  
• inserir pacote  
• buscar pacote  
• remover pacote entregue  
• listar pacotes  
Situação prática  
Simule:  
1. Chegada de 4 pacotes.  
2. Transmissão de 2 pacotes.  
3. Um pacote apresenta erro e vai para pilha.  
4. Um pacote é entregue e removido da lista.


**Perguntas teóricas**
1. Por que a fila representa bem a transmissão de pacotes?
   A fila representa bem a transmissão de pacotes porque os pacotes chegam continuamente à rede e precisam ser enviados na ordem em que foram recebidos. Esse comportamento é semelhante ao funcionamento real de roteadores e switches, que organizam os pacotes em sequência para evitar perda de ordem na comunicação.

3. Por que a pilha pode representar retransmissão?
   A pilha representa retransmissão porque o último pacote que apresentou erro geralmente é o primeiro a ser tratado novamente. Isso ocorre porque o sistema tenta corrigir rapidamente as falhas mais recentes, seguindo o modelo LIFO.  
   
5. Por que a lista encadeada ajuda no controle de pacotes ativos?
   A lista encadeada ajuda no controle de pacotes ativos porque permite inserir, remover e buscar pacotes dinamicamente sem necessidade de tamanho fixo. Em uma rede, os pacotes entram e saem constantemente, e a lista encadeada facilita esse gerenciamento de forma eficiente.
   
7. Qual estrutura melhor representa atraso de fila?
   A estrutura que melhor representa atraso de fila é a fila. Isso ocorre porque, quanto maior a quantidade de pacotes aguardando transmissão, maior será o tempo de espera até que cada pacote seja enviado pela rede.
