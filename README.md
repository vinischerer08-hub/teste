# Entrega 1 — Modelo Conceitual (DER)
### Modelagem de um sistema de gestão de informações para uma organização de pequeno porte

> Este arquivo é o esqueleto do **README.md** do repositório GitHub do seu grupo.
> Preencha cada seção abaixo. Não apague os títulos — apenas substitua as instruções em *itálico* pelo conteúdo do seu projeto.
> O **DER** é anexado separadamente ao repositório (em imagem), mas sua justificativa entra neste README.
>
> **A organização escolhida pode ser de qualquer natureza:** empresa com fins lucrativos (livraria, lanchonete, pet shop), ONG, associação comunitária, cooperativa, instituições religiosas/comunitárias como igrejas, terreiros de religiões de matriz africana (candomblé, umbanda) ou outras. O que muda de um tipo para outro são os processos e as regras específicas — a estrutura do trabalho (levantamento de requisitos, modelagem conceitual, DER) é a mesma para todas. Termos como "empresa" e "negócio" usados abaixo devem ser lidos de forma ampla, no sentido técnico de modelagem de dados (ex.: "regras de negócio" = regras de funcionamento da organização, seja ela comercial, religiosa ou social).
>
> **Importante:** a organização precisa **existir de fato** — não é permitido inventar uma organização fictícia. O levantamento de requisitos e regras de negócio deve ser feito por meio de **pesquisa de campo na própria organização** (visitas, entrevistas com responsáveis, observação dos processos reais), então o grupo só deve escolher uma organização à qual **realmente tenha acesso**. Ao escolher, tomem cuidado com o porte: **nem tão pequena** que não gere dados suficiente para o trabalho (poucos processos, poucas entidades), **nem tão grande/complexa** que fique inviável de modelar nesta primeira etapa do curso.

---

## Metadados

* **Nomes dos alunos e RGM:** *Preencher com os nomes e RGM dos integrantes do grupo.*

---

## 1. Caracterização da Organização

(vale 7,5% — Dimensão Conceitual)

* **Nome e natureza da organização:** Waldesa Comércio, empresa com fins lucrativos que atua no comércio varejista de materiais elétricos e representações comerciais.

* **Histórico:** A empresa existe desde 1966. Começou suas atividades focada no comércio varejista de materiais elétricos e representações comerciais, estabelecendo uma forte presença regional na Grande São Paulo, com destaque para a sede e filiais em cidades como Mogi das Cruzes e na tradicional região eletroeletrônica da Rua Santa Ifigênia, na capital paulista.

* **Contexto e porte:** A unidade da Santa Ifigênia possui cerca de 40 funcionários e realiza aproximadamente 40 a 50 vendas por dia, contando atendimentos presenciais (balcão), on-line e por plataformas de e-commerce.

* **Meios de registro de informações:** As informações principais estão registradas em sistema, e pelo menos 90% também são registradas em planilhas, além do uso de WhatsApp e anotações manuais.

* **Problemas e necessidades identificados:** O principal problema encontrado foi o controle de estoque. Muitas peças são registradas manualmente com quantidades incorretas, causando os chamados "furos de estoque". Como solução paliativa, a empresa costuma realizar contagens de estoque anuais, mas ainda não possui uma solução definitiva para o problema.

* **Justificativa da escolha:** A empresa foi escolhida por ser uma organização real e acessível ao grupo, além de possuir processos que podem ser analisados e melhorados através da tecnologia.

* **Evidências da organização:**

  * Site: https://www.waldesa.com.br/
  * Instagram: https://www.instagram.com/waldesaoficial?stkn=amJsaHRrcGN5eHB5
  * As fotos da empresa serão adicionadas após autorização. Também será buscado um contato oficial para o acompanhamento do projeto (follow-up).

---

## 2. Processos de Negócio

(vale 10% — Dimensão Procedimental)

### Principais processos mapeados

* Cadastro de clientes;
* Vendas;
* Entrada e controle de estoque;
* Separação de pedidos;
* Entregas.

### Responsáveis

| Processo | Responsável                         |
| -------- | ----------------------------------- |
| Cadastro | Vendedor                            |
| Vendas   | Vendedor                            |
| Estoque  | Setor de Compras e Estoquistas      |
| Entregas | Estoquistas, vendedores e motorista |

### Como os processos funcionam

**Cadastro e Vendas:** ainda serão detalhados em contato com um dos vendedores da empresa, através de perguntas específicas sobre o passo a passo dessas etapas.

**Estoque:** o processo começa pela compra dos produtos. Quando as peças chegam, as notas fiscais são digitalizadas e todos os produtos são colocados no sistema, cada um identificado por seu código. Depois, os produtos são repostos em seus locais corretos nas prateleiras do estoque.

**Entrega:** existe um grupo na plataforma Teams, onde os vendedores enviam seus pedidos junto com a forma como cada cliente irá receber: retirada na loja, entrega pela própria empresa ou envio pelos Correios. A partir daí, o responsável pelo estoque separa os pedidos de entrega e os organiza em uma planilha. No final do dia, o motorista tem o carro carregado com todas as notas fiscais e os endereços, e as entregas são realizadas no dia seguinte.

### O que pode dar errado?

A falta de estoque, principalmente por conta dos chamados "furos de estoque".

### O que acontece após os processos?

* **Cadastro:** o cliente tem todos os seus dados armazenados no sistema.
* **Venda:** para clientes já cadastrados, é gerada a nota fiscal; para clientes sem cadastro, é gerado o cupom fiscal.
* **Entrega:** não gera nenhum documento adicional além da nota fiscal já emitida na venda.

### Como os processos se conectam?

* **Cadastro:** conecta-se ao sistema, onde ficam registradas todas as compras do cliente, orçamentos gerados, notas fiscais e pedidos.
* **Vendas:** conecta-se ao estoque, pois tudo o que está em um pedido é retirado automaticamente do sistema, com a redução da quantidade de peças correspondente.
* **Entregas:** estão diretamente ligadas às vendas, já que fazem parte do mesmo fluxo. Porém, todas as entregas finalizadas também ficam registradas em um grupo de WhatsApp.

### Etapa que poderia ser automatizada

O registro dos produtos que chegam ao estoque. A ideia é que, a partir da nota fiscal, as peças sejam colocadas automaticamente no sistema de estoque, diminuindo os erros manuais.

### Fluxogramas

Os fluxogramas dos principais processos serão anexados ao repositório.

---

## 3. Requisitos do Sistema

(esta seção e a Seção 4 "Regras de Negócio" DIVIDEM 7,5% na dimensão conceitual — juntas valem 7,5%, não 7,5% cada — + 4% exclusivos desta seção na organização/documentação)

### 3.1 Requisitos Funcionais

* **RF01:** Permitir cadastrar clientes.
* **RF02:** Permitir cadastrar produtos.
* **RF03:** Registrar vendas.
* **RF04:** Consultar o estoque.
* **RF05:** Atualizar o estoque após uma venda.
* **RF06:** Registrar entrada de produtos.
* **RF07:** Relacionar a entrada com a nota fiscal.
* **RF08:** Registrar pedidos.
* **RF09:** Informar a forma de recebimento do pedido.
* **RF10:** Registrar entregas.
* **RF11:** Consultar movimentações do estoque.
* **RF12:** Identificar divergências no estoque.
* **RF13:** Registrar automaticamente a entrada e a saída de materiais no estoque, sem necessidade de lançamento manual.
* **RF14:** Permitir a busca do cadastro do cliente por nome, CPF/CNPJ ou pelo número dos pedidos já realizados.
* **RF15:** Impedir a liberação de um pedido sem a confirmação de que o pagamento foi realizado.

### 3.2 Requisitos Não Funcionais

* **RNF01:** O sistema deve ser fácil de utilizar.
* **RNF02:** Deve possuir controle de acesso.
* **RNF03:** Deve apresentar as informações rapidamente.
* **RNF04:** Os dados devem ser protegidos.
* **RNF05:** Deve evitar registros incorretos ou duplicados.
* **RNF06:** Deve possuir backup dos dados.
* **RNF07:** Deve permitir o crescimento da quantidade de produtos, clientes e vendas.
* **RNF08:** Deve restringir a visualização das informações conforme o setor do usuário, sendo a gerência o único perfil com acesso a todas as informações do sistema.
* **RNF09:** Deve impedir que os dados dos clientes sejam copiados ou compartilhados sem autorização.
* **RNF10:** Deve funcionar off-line ao menos para o registro de saída de peças em pedidos.
* **RNF11:** Deve garantir estabilidade e disponibilidade do sistema, principalmente nas semanas de pagamento e vale.

### 3.3 Levantamento de Requisitos com a Organização (Sistema Ideal)

Em conversa com a organização sobre como seria um sistema ideal, foram levantados os seguintes pontos:

* **Funcionalidades obrigatórias:** o sistema precisaria agrupar automaticamente todos os materiais que chegam e que saem do estoque, atualizando as quantidades sem a necessidade de lançamentos manuais, facilitando o ajuste de estoque e tornando o processo o menos manual possível.
* **Perfis de uso:** a ideia é que todos os setores da empresa sejam beneficiados pelo sistema, como atendente, gerente, administrador, entre outros.
* **Visibilidade das informações:** cada setor deve visualizar apenas as informações referentes ao que envolve seu próprio trabalho. A gerência é o único perfil com acesso a todas as informações.
* **Segurança e privacidade:** os dados dos clientes precisam ser protegidos, sem possibilidade de serem copiados ou compartilhados sem autorização.
* **Funcionamento off-line:** é importante que ao menos a parte de saída de peças em pedidos funcione mesmo sem conexão com a internet. Não há exigência de que o sistema todo funcione off-line.
* **Momentos críticos:** o sistema não pode falhar principalmente nas semanas de pagamento e vale, quando a movimentação é maior.

---

## 4. Regras de Negócio

(esta seção DIVIDE com a Seção 3 "Requisitos do Sistema" os mesmos 7,5% da dimensão conceitual — juntas valem 7,5%, não 7,5% cada — + 4% exclusivos desta seção na documentação. "Regras de negócio" é o termo técnico usado em modelagem de dados para as regras de funcionamento de qualquer organização, com ou sem fins lucrativos)

### Regras operacionais

* Cada produto deve possuir um código.
* Produtos recebidos devem ser registrados no sistema.
* A entrada deve estar relacionada à nota fiscal.
* O estoque deve ser atualizado nas entradas e saídas.
* Uma venda deve possuir os produtos e quantidades vendidos.
* Todo pedido deve possuir uma forma de recebimento.
* Pedidos de entrega devem ser separados antes de serem enviados ao motorista.
* As entregas realizadas devem ser registradas.
* Não pode haver liberação de um pedido sem que o pagamento correspondente tenha sido realizado.
* A emissão de nota fiscal é uma exigência legal que deve ser seguida nas vendas aplicáveis.

### Restrições organizacionais

A empresa utiliza sistema, planilhas, Teams, WhatsApp e anotações. A utilização de vários meios pode dificultar a organização das informações.

O registro manual dos produtos também pode causar erros e contribuir para os furos de estoque.

### Observações adicionais sobre as regras

Atualmente não há limites definidos de quantidade, valor ou tempo em nenhum dos processos, nem regras não escritas que sejam seguidas apenas na prática. As regras vigentes são as descritas acima. Essas regras podem vir a mudar futuramente, conforme forem identificadas novas falhas ou problemas no funcionamento e na forma como os processos são realizados.

---

## 5. Dicionário de Dados Conceitual (Preliminar)

(vale 10% — Dimensão Procedimental - Segue o modelo do arquivo 02-03g_Exemplo_Dicionario_Dados.pdf)

### Cliente

| Atributo           | Descrição                                                         | Regra de negócio associada         |
| ------------------ | ----------------------------------------------------------------- | ---------------------------------- |
| id_cliente         | Identificação do cliente                                          | Único                              |
| nome               | Nome do cliente                                                   | Obrigatório                        |
| CPF_CNPJ           | Documento (CPF ou CNPJ)                                           | Obrigatório — identifica o cliente |
| data_nascimento    | Data de nascimento                                                | Obrigatória                        |
| telefone           | Telefone                                                          | Obrigatório                        |
| email              | E-mail                                                            | Quando informado                   |
| endereco           | Endereço                                                          | Obrigatório — usado nas entregas   |
| CEP                | CEP                                                               | Obrigatório                        |
| inscricao_estadual | Inscrição estadual                                                | Obrigatória                        |
| data_abertura      | Data de abertura                                                  | Obrigatória                        |
| cnae_principal     | Código e descrição da atividade econômica (CNAE) principal        | Obrigatório                        |
| cnae_secundarias   | Códigos e descrições das atividades econômicas (CNAE) secundárias | Obrigatório                        |

> Os dados pessoais do cliente são importantes para contato, cadastro e emissão de notas fiscais. Uma vez cadastrado, o cliente mantém todos os seus dados no sistema, com possibilidade de alteração. A busca pelo cadastro pode ser feita por nome, CPF/CNPJ ou pelo número dos pedidos já realizados pelo cliente.

### Vendedor

| Atributo    | Descrição     | Regra de negócio associada |
| ----------- | ------------- | -------------------------- |
| id_vendedor | Identificação | Único                      |
| nome        | Nome          | Obrigatório                |
| matricula   | Matrícula     | Única                      |

### Produto

| Atributo       | Descrição          | Regra de negócio associada |
| -------------- | ------------------ | -------------------------- |
| id_produto     | Identificação      | Único                      |
| codigo_produto | Código do produto  | Único                      |
| descricao      | Descrição          | Obrigatória                |
| preco          | Preço              | Valor válido               |
| unidade_medida | Unidade do produto | Conforme o produto         |

### Estoque

| Atributo         | Descrição             | Regra de negócio associada   |
| ---------------- | --------------------- | ---------------------------- |
| id_estoque       | Identificação         | Único                        |
| quantidade       | Quantidade disponível | Não negativa                 |
| localizacao      | Local do produto      | Deve existir                 |
| data_atualizacao | Última atualização    | Atualizada nas movimentações |

### Venda

| Atributo    | Descrição      | Regra de negócio associada |
| ----------- | -------------- | -------------------------- |
| id_venda    | Identificação  | Único                      |
| data_venda  | Data da venda  | Obrigatória                |
| valor_total | Valor da venda | Calculado pelos itens      |
| id_cliente  | Cliente        | Relacionado ao cliente     |
| id_vendedor | Vendedor       | Relacionado ao vendedor    |

### Item_Venda

| Atributo       | Descrição          | Regra de negócio associada |
| -------------- | ------------------ | -------------------------- |
| id_item_venda  | Identificação      | Único                      |
| id_venda       | Venda              | Deve pertencer a uma venda |
| id_produto     | Produto            | Deve existir               |
| quantidade     | Quantidade vendida | Maior que zero             |
| preco_unitario | Preço unitário     | Valor da venda             |

### Nota_Fiscal

| Atributo     | Descrição       | Regra de negócio associada |
| ------------ | --------------- | -------------------------- |
| id_nota      | Identificação   | Único                      |
| numero_nota  | Número da nota  | Identifica a nota          |
| data_emissao | Data de emissão | Obrigatória                |
| chave_acesso | Chave da nota   | Identifica a nota          |

### Pedido

| Atributo          | Descrição            | Regra de negócio associada    |
| ----------------- | -------------------- | ----------------------------- |
| id_pedido         | Identificação        | Único                         |
| data_pedido       | Data do pedido       | Obrigatória                   |
| status            | Situação do pedido   | Deve ser válido               |
| forma_recebimento | Forma de recebimento | Retirada, entrega ou Correios |
| id_cliente        | Cliente              | Relacionado ao pedido         |

### Entrega

| Atributo         | Descrição      | Regra de negócio associada |
| ---------------- | -------------- | -------------------------- |
| id_entrega       | Identificação  | Único                      |
| data_prevista    | Data prevista  | Para entregas              |
| data_entrega     | Data realizada | Após conclusão             |
| status           | Situação       | Deve ser válido            |
| endereco_entrega | Endereço       | Obrigatório para entrega   |
| id_motorista     | Motorista      | Responsável pela entrega   |

### Motorista

| Atributo     | Descrição     | Regra de negócio associada |
| ------------ | ------------- | -------------------------- |
| id_motorista | Identificação | Único                      |
| nome         | Nome          | Obrigatório                |
| telefone     | Telefone      | Quando necessário          |

### Entrada_Estoque

| Atributo     | Descrição       | Regra de negócio associada |
| ------------ | --------------- | -------------------------- |
| id_entrada   | Identificação   | Único                      |
| data_entrada | Data de entrada | Obrigatória                |
| id_nota      | Nota fiscal     | Relacionada à entrada      |
| fornecedor   | Fornecedor      | Identifica a origem        |

### Item_Entrada

| Atributo        | Descrição           | Regra de negócio associada   |
| --------------- | ------------------- | ---------------------------- |
| id_item_entrada | Identificação       | Único                        |
| id_entrada      | Entrada             | Deve pertencer a uma entrada |
| id_produto      | Produto             | Deve existir                 |
| quantidade      | Quantidade recebida | Maior que zero               |
| codigo_produto  | Código do produto   | Deve corresponder ao produto |

> **Atenção à privacidade:** os exemplos utilizados para ilustrar os atributos devem ser fictícios. Não devem ser utilizados dados reais de clientes, funcionários ou outras pessoas da organização.

---

## 6. Modelagem Conceitual (Entidades, Atributos, Relacionamentos)

(vale 7,5% na dimensão conceitual)

### Entidades reconhecidas

As principais entidades são:

**Cliente, Vendedor, Produto, Estoque, Venda, Item_Venda, Nota_Fiscal, Pedido, Entrega, Motorista, Entrada_Estoque e Item_Entrada.**

Elas foram escolhidas por representarem os principais processos identificados na empresa.

De acordo com o levantamento feito junto à organização, os únicos tipos de "pessoa" que realmente precisam ser cadastrados no sistema são **Clientes** e **Funcionários**. Este último grupo engloba os perfis de Vendedor, Estoquista e Motorista já identificados nos processos mapeados.

### Atributos e classificações

Cada entidade possui atributos relacionados às informações que precisam ser armazenadas, como identificação, datas, quantidades, valores e informações de contato.

### Relacionamentos pertinentes

* Cliente realiza vendas e pedidos.
* Vendedor realiza vendas.
* Venda possui itens.
* Produto participa das vendas.
* Produto possui controle de estoque.
* Entrada possui itens.
* Produto participa das entradas.
* Entrada está relacionada à nota fiscal.
* Pedido pode possuir uma entrega.
* Motorista realiza entregas.

### Restrições e políticas organizacionais

O modelo considera principalmente o controle das entradas e saídas de produtos, buscando manter o estoque atualizado e diminuir os furos de estoque.

---

## 7. Diagrama Entidade-Relacionamento (DER)

(vale 20% — é o item de maior peso da entrega)

O DER será anexado ao repositório em formato de imagem.

O diagrama deverá representar:

* Entidades;
* Atributos;
* Relacionamentos;
* Cardinalidades.

O modelo será baseado nos processos observados na empresa e dará atenção principalmente ao controle de estoque.

---

## 8. Justificativa Técnica

(vale 7,5% — sozinho, é o subcritério de maior peso dentro da Dimensão Conceitual)

As entidades foram escolhidas com base nos processos observados na empresa.

**Produto** e **Estoque** são importantes para representar o controle das peças. **Venda** e **Item_Venda** foram separados porque uma venda pode possuir vários produtos.

A mesma ideia foi utilizada em **Entrada_Estoque** e **Item_Entrada**, já que uma entrada pode possuir vários produtos.

**Cliente** e **Vendedor** ajudam a identificar quem participa das vendas, enquanto **Pedido**, **Entrega** e **Motorista** representam o processo de entrega.

A modelagem também considera o problema dos furos de estoque, permitindo que as entradas e saídas dos produtos sejam controladas.

---

## 9. Uso de Inteligência Artificial

(documentação obrigatória — não é opcional se o grupo usou IA em qualquer etapa: pesquisa, escrita, organização de ideias ou revisão de texto)

Foi utilizada a ferramenta **ChatGPT** para auxiliar na organização das informações e na estruturação do README.

| Item                                 | O que registrar                                                                                                               |
| ------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------- |
| **Ferramenta e etapa**               | ChatGPT — organização do trabalho e revisão do texto.                                                                         |
| **Motivação**                        | Ajudar a organizar as informações coletadas.                                                                                  |
| **Prompt(s) utilizados**             | Foi solicitado que as informações da pesquisa fossem organizadas de acordo com o modelo de README da atividade.               |
| **Resposta recebida**                | A IA ajudou a organizar processos, requisitos, regras e entidades.                                                            |
| **Fontes consultadas e verificadas** | Informações obtidas através da pesquisa realizada na organização e canais oficiais da empresa.                                |
| **Trechos rejeitados ou corrigidos** | Informações não confirmadas pela empresa serão revisadas pelo grupo.                                                          |
| **Justificativa da escolha final**   | A IA foi utilizada apenas como apoio, mantendo as informações coletadas pelo grupo como base.                                 |
| **Reflexão crítica**                 | Algumas sugestões da IA podem não representar exatamente a realidade da empresa, por isso precisam ser conferidas pelo grupo. |

---

## Critérios Atitudinais (20%)

Os critérios serão avaliados através da avaliação 360º entre os integrantes e pelo histórico de commits do GitHub.

* **Participação:** participação nas decisões do grupo.
* **Comprometimento:** cumprimento das tarefas.
* **Colaboração:** trabalho em equipe.
* **Autonomia:** busca por soluções e melhorias.

---

## Resumo dos Pesos

| Dimensão | Peso total |
|----------|-----------|
| Conceitual (contexto, requisitos/regras, modelagem, justificativa técnica) | 30% |
| Procedimental (requisitos, fluxogramas, dicionário de dados, DER) | 50% |
| Atitudinal (participação, comprometimento, colaboração, autonomia) | 20% |

**Entrega final:** README.md completo + DER anexado no repositório GitHub do grupo.
