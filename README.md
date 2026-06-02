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
