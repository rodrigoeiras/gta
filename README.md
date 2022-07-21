## Proposta de Pesquisa
### Análise de Sentimentos Baseada em Aspectos para Detecção de Eventos Severos em Plataforma Off-Shore de O&G Equipada com Computação de Borda Móvel (MEC)

----

### Motivações

* Dificuldade de entendimento de um evento severo por parte de operadores da companhia que estão on-shore na base de operações
* Classificação errada de um evento por parte do operador off-shore ocasionando em lentidão de ação responsiva ou uso de recurso em excesso em um evento erroneamente rotulado como severo
* Latência e ou erros de comunicação dos eventos em plataformas equipadas com links convencionais de baixa velocidade
* Necessidade de sincronização sistêmica ou proximidade com a base de operações on-shore para carregamento/descarregamento completo de informações
* Impossibilidade de fazer recomendações de ações em eventos em uma plataforma desconectada ou com baixa velocidade de conexão de dados
* Eventos severos podem impactar reputações de marcas e ou valores de mercados caso os dados sejam expostos em nuvem pública
* Treinamentos do algoritmo em nuvem publica podem se tornar custosos tanto em termos de valores a pagar a um provedor de nuvem quanto de tempo de comunicação



### Objetivo Geral

* Desenvolver um modelo de arquitetura de sistema que permita que companhias de O&G possam aprimorar o desempenho e a segurança de operações off-shore através de Inteligência Artificial



### Objetivos Específicos

* Viabilizar uma aplicação sustentada por uma MEC que permita, em tempo real, que o operador através da própria descrição inserida no evento, conheça o melhor rótulo a se classificar o evento.
* Permitir que classificações locais do algoritmo, possam ser replicadas para a núvem privada e ou para núvem pública (com criptografia) para enriquecimento da tarefa de treinamento da aplicação em conjunto com outras instâncias do sistema de recomendação em operação em outras plataformas.
* Certificar de qual método é o mais recomendado para inferencias e classificações textuais considerando uma computação de borda móvel com recursos limitados de processamento e armazenamento.
* Capacidade de inferir localmente no dispostivo móvel (pre-trained data) a severidade do evento sendo criado em caso de queda de conexão ou falha de comunicação com a MEC.


### Principais Gaps da Literatura

* H. Sankar1 V. Subramaniyaswamy1 V. Vijayakumar2 Sangaiah Arun Kumar3 R. Logesh1 A. Umamakeswari1 (Intelligent sentiment analysis approach using edge
computing-based deep learning technique, 2018)
  * Uso de aspectos da linguagem não foi considerado.
  * Somente considerou CNN
  * Somente utilizou avaliações de filmes nos algoritmos, limitando o alcance da aplicação

* Tausif Diwan1 & Jitendra V. Tembhurne1 (Sentiment analysis: a convolutional neural networks perspective, 2021)
  * CNN foi utilizada principalmente como extratora de caracteristicas e não como classificadora.
  * Acurácia do modelo fica comprometida ao desconsiderar o sentido léxico de palavras.
  * Transfêrencia de dados pré-treinados entre domínios diferentes

* Ilir Murturi, Cosmin Avasalcai, Christos Tsigkanos and Schahram Dustdar (Edge-to-Edge Resource Discovery using Metadata Replication, 2019)
  * Número de nós necessários para formar vizinhos em uma rede de borda e comprovar a replicação
  * Número de requisições concorrentes para replicação
  * Influencia do tamanho do meta-dado a ser replicado ficou em aberto
  * Roteamento entre nós foi ignorado

* Dafuallah Esameldien Dafaallah, Ahmad Sobri Hashim (Awareness at Oil and Gas Platforms Using Machine Learning, 2020)
  * Baixa acurácia em todos os modelos testados
  * Não considerou aspectos da linguagem
  * Não considerou CNN
  * Dados sobre O&G não foram utilizados, não comprovando aderência ao negócio proposto

* Ambreen Nazir , Yuan Rao, Lianwei Wu , and Ling Sun (Issues and Challenges of Aspect-based Sentiment Analysis: A Comprehensive Survey, 2022)
  * Transferencia entre domínios diferentes implica baixa acurácia. (ex, dados de avaliações de hotel sendo usados para avaliar restaurantes) No entanto, sub-domínios podem ser avaliados. (Dados de operações on-shore sendo aproveitados para operações off-shore)
  * Aprendizado multimodal: textos, com videos e ou imagens para enriquecimento da recomendação. Os trabalhos avaliados ignoram a prática.
  * Sumarização de aspectos centrada em entidades pode ser especialmente interessante no idioma portugues devido a depencia e interpretação baseada no contexto.
  
* Lele Ma Shanhe Yi Qun Li (Efficient Service Handoff Across Edge Servers via Docker Container Migration, 2017)
  * Não considera o uso de MEC
  * Segurança na transferência de containers não foi considerada
  * Somente considerou WiFi para migração e transferência dos containers
