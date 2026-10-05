# Entrega 1 — Modelo Conceitual (DER)
### Modelagem de um sistema de gestão de informações para uma organização de pequeno porte

---

## Metadados

- *Matheus Nogales dos Santos, RGM: 47810629*
- *Carlos Eduardo ALves Lopes da Silva, RGM: 48465097*
- *Lucas Gabriel de Oliveira Castro, RGM: 47627891*
- *Karoline Almeida de Araújo, RGM: 48379867*

## 1. Caracterização da Organização
*(vale 7,5% — Dimensão Conceitual)*

- **Nome e natureza da organização:** *Bar do Ernesto - Restaurante e Pizzaria*
- **Contexto e porte:** *Organização com fins lucrativos; médio porte; no momento, possui 9 colaboradores; volume de vendas regular.*
- **Problemas e necessidades identificados:** *O maior problema identificado é falta de organização e controle no estoque.*
- **Justificativa da escolha:** *Um dos membros do grupo já era familiar com o dono do local*
- **Evidências da organização:** *R. Abel Tavares, 2470 - Jardim Belem, São Paulo* ![Frente_do_Restaurante](Imagens/Restaurante1) 

---

## 2. Processos de Negócio
*(vale 10% — Dimensão Procedimental)*

- **Principais processos mapeados:** *Cadastros de cliente; Sistema de entrega; Fornecimento de ingrediente/utilidades; Cadastro de Funcionários; Controle de estoque.*

---

## 3. Requisitos do Sistema
*(esta seção e a Seção 4 "Regras de Negócio" DIVIDEM 7,5% na dimensão conceitual — juntas valem 7,5%, não 7,5% cada — + 4% exclusivos desta seção na organização/documentação)*

### 3.1 Requisitos Funcionais
*O que o sistema precisa FAZER (ex.: "o sistema deve permitir registrar uma venda").*
- O sistema deve permitir o registro de clientes;
- O sistema deve permitir o registro de colaboradores e entregadores; 
- O sistema deve permitir a edição de endereço e número de telefone.

### 3.2 Requisitos Não Funcionais
*Características de qualidade (ex.: desempenho, segurança, usabilidade, disponibilidade).*
- Dados sensiveís como telefone e endereço devem ser criptografados e armazenados de forma segura;
- Páginas com dados não sensiveís devem carregar em menos de 2 segundos;
- O sistema deve permanecer ativo por aproximadamente 60% - 65% do dia.
---

## 4. Regras de Negócio
*(esta seção DIVIDE com a Seção 3 "Requisitos do Sistema" os mesmos 7,5% da dimensão conceitual — juntas valem 7,5%, não 7,5% cada — + 4% exclusivos desta seção na documentação. "Regras de negócio" é o termo técnico usado em modelagem de dados para as regras de funcionamento de qualquer organização, com ou sem fins lucrativos)*

- **Regras operacionais:**
- * Identificador Principal: Número do telefone/WhatsApp cadastrado como nome de identificação.
- *Endereço de Entrega*: Campo Obrigatório (Rua, número, bairro, complemento e ponto de referência). Sem endereço, o pedido não pode    ser finalizado.
- *Canais de Origem**: Registro da origem da venda (iFood, 99, Ligação Direta ou WhatsApp).
informada.
- *Logística Interna**: Configuração específica para os 1 a 2 Motoboys (controle de taxas de entrega, entregas concluídas e rotas).
- Módulo de Fornecedores
- *Dados do Cadastro**: Nome do fornecedor, produtos fornecidos e prazo médio de entrega.
- *Canais de Pedido Preferenciais**: Marcação do canal direto para compras (Aplicativo, WhatsApp ou Ligação Telefônica).


---

## 5. Dicionário de Dados Conceitual (Preliminar)
*(vale 10% — Dimensão Procedimental - Segue o modelo do arquivo 02-03g_Exemplo_Dicionario_Dados.pdf)*

Para cada entidade identificada, liste:

| Atributo | Descrição | Regra de negócio associada |
|----------|-----------|------------------------------|
| *nome do atributo* | *o que ele representa* | *se houver alguma regra (obrigatoriedade, valores possíveis, etc.)* |

*Mantenha o dicionário organizado e padronizado (mesmo formato de tabela para todas as entidades).*

**Atenção à privacidade:** se forem usados exemplos de valores para ilustrar os atributos, esses exemplos devem ser **fictícios** — não utilize dados reais de clientes, fiéis, beneficiários, doadores ou funcionários da organização (nomes, CPFs, contatos etc.), mesmo que tenham sido observados durante a pesquisa de campo. Os exemplos devem apenas ser **coerentes com as operações reais** observadas.

---

## 6. Modelagem Conceitual (Entidades, Atributos, Relacionamentos)
*(vale 7,5% na dimensão conceitual)*

- **Entidades reconhecidas:** *Cliente* = quem solicita e recebe pedidos à longa distância; *Colaborador* = quem trabalha permanentemente num estabelecimento público ou privado; *Entregador* = encarregado da entrega das compras ao cliente; *Pedido* = produto que o cliente requisitou; *Conta* = pagamento a ser feito pelo serviço/pedido.
- **Atributos e classificações:** *Nome* = Cliente, Colaborador, Entregador; *Telefone* = Cliente, Colaborador, Entregador; *Endereço (Atributo Composto(Numero, Cidade, Rua, Bairro))* = Cliente, Colaborador. *Descrição* = Pedido; *Valor* = Conta; *Data_Vencimento* = Conta; *id_cliente*; *id_colaborador*; *id_entregador*; *num_pedido*; *num_conta*.
- **Relacionamentos pertinentes:** *Pagamento, Fazer Pedido, Entregar Pedido, Possuir.* 

---

## 7. Diagrama Entidade-Relacionamento (DER)
*(vale 20% — é o item de maior peso da entrega)*

- Anexe o DER (em imagem).
- O diagrama deve representar corretamente:
  - Entidades
  - Atributos
  - Relacionamentos
  - **Cardinalidades**
- O modelo deve ser **consistente** e já demonstrar potencial de **escalabilidade e integração** (pensando nas próximas etapas do projeto).

---

## 8. Justificativa Técnica
*(vale 7,5% — sozinho, é o subcritério de maior peso dentro da Dimensão Conceitual)*

*Explique e defenda as decisões de abstração e modelagem tomadas: por que essas entidades, esses atributos, esses relacionamentos e essas cardinalidades — e não outras alternativas possíveis?*

---

## 9. Uso de Inteligência Artificial
*(documentação obrigatória — não é opcional se o grupo usou IA em qualquer etapa: pesquisa, escrita, organização de ideias ou revisão de texto)*

Se o grupo usou alguma ferramenta de IA (ChatGPT, Claude, Gemini, Perplexity etc.) em qualquer parte do trabalho, registre **para cada uso relevante**:

| Item | O que registrar |
|------|------------------|
| **Ferramenta e etapa** | Qual IA foi usada e em qual parte do trabalho (ex.: pesquisa sobre o setor da organização, redação do README, organização dos requisitos, revisão ortográfica/gramatical). |
| **Motivação** | Por que o grupo recorreu à IA nesse ponto específico. |
| **Prompt(s) utilizados** | Texto exato (ou muito próximo) do que foi perguntado/pedido à IA. |
| **Resposta recebida** | Resumo ou trecho relevante da resposta da IA. |
| **Fontes consultadas e verificadas** | Se a IA citou fontes/dados, quais foram checadas pelo grupo e como (ex.: comparação com o que foi observado na visita de campo). |
| **Trechos rejeitados ou corrigidos** | O que da resposta da IA foi descartado, editado ou corrigido manualmente, e por quê. |
| **Justificativa da escolha final** | Por que o grupo manteve, adaptou ou rejeitou o que a IA sugeriu. |
| **Reflexão crítica** | Limites, vieses ou erros identificados no uso da IA nessa etapa (ex.: informação desatualizada, alucinação, generalização incorreta sobre o tipo de organização). |

*Se o grupo não usou nenhuma ferramenta de IA, declare isso explicitamente nesta seção.*

---

## Critérios Atitudinais (20%)
**Estes critérios NÃO constam explicitamente como item de entrega no README.** Eles são avaliados por meio de **Avaliação 360º entre os integrantes do grupo** (cada membro avalia os colegas de equipe) e, no caso da Colaboração, também pela **colaboração equilibrada no histórico de commits** do repositório GitHub — não pela leitura do restante do repositório nem pela apresentação:

- **Participação (5%):** envolvimento nas discussões técnicas e nas decisões do grupo.
- **Comprometimento (5%):** cumprimento de prazos e responsabilidades assumidas.
- **Colaboração (5%):** respeito às contribuições dos colegas, cooperação na construção do projeto e colaboração equilibrada no histórico de commits do repositório GitHub.
- **Autonomia (5%):** busca independente de soluções e proposta de melhorias.

---

## Resumo dos Pesos

| Dimensão | Peso total |
|----------|-----------|
| Conceitual (contexto, requisitos/regras, modelagem, justificativa técnica) | 30% |
| Procedimental (requisitos, fluxogramas, dicionário de dados, DER) | 50% |
| Atitudinal (participação, comprometimento, colaboração, autonomia) | 20% |

**Entrega final:** README.md completo + DER + Dicionário de Dados em HTML (com exceção dos cursos GTI) anexado no repositório GitHub do grupo.
