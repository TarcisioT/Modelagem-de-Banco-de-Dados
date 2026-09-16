# Entrega 1 — Modelo Conceitual (DER)
### Modelagem de um sistema de gestão de informações para uma organização de pequeno porte


---

## 1. Caracterização da Organização

- **Nome e natureza da organização:** Hortifruti União - Tatuapé, empresa privada, com fins lucrativos do ramo de comércio varejista alimentício.
- **Contexto e porte:** empresa com fins lucrativos de médio porte, 110 funcionários, com um faturamento de 5 milhões/mês (aproximadamente).
- **Problemas e necessidades identificados:** o levantamento feito no Hortifruti União, notamos um problema com o controle de validade dos produtos. Como o mercado trabalha com muita quantidade e variedade de mercadorias, acompanhar as datas de vencimento acaba sendo complicado. Por isso, itens perto de vencer ou já vencidos podem ficar nas prateleiras mais tempo do que deveriam, o que gera perdas e exige mais atenção dos funcionários na hora de conferir. Com base nisso, vimos a necessidade de um sistema para registrar e acompanhar as datas de validade dos produtos. Assim, dá para consultar quais estão perto de vencer, o que ajuda a retirar ou dar prioridade a esses itens e contribui para reduzir as perdas.*
- **Justificativa da escolha:** escolhemos essa organização porque um dos integrantes do grupo tem contato com um dos responsáveis pelo estabelecimento, o que abriu caminho para acessar o local e fazer a pesquisa de campo. O Hortifruti União também tem processos que interessam à disciplina de Modelagem de Banco de Dados, como controle de estoque, acompanhamento da validade dos produtos, compras de fornecedores e registro de vendas. Esses processos oferecem dados e regras de negócio suficientes para montar um modelo conceitual consistente.
- **Evidências da organização:**  https://www.google.com/maps/@-23.5357427,-46.5791203,747a,86.7y,87.54h,101.01t/data=!3m7!1e1!3m5!1swJUlDJQ1_PRKkzMQx4lZhg!2e0!6shttps:%2F%2Fstreetviewpixels-pa.googleapis.com%2Fv1%2Fthumbnail%3Fcb_client%3Dmaps_sv.tactile%26w%3D900%26h%3D600%26pitch%3D-11.012688400441263%26panoid%3DwJUlDJQ1_PRKkzMQx4lZhg%26yaw%3D87.54143764466257!7i16384!8i8192?entry=ttu&g_ep=EgoyMDI2MDkwNi4wIKXMDSoASAFQAw%3D%3D (Google Maps)
- Endereço: Rua Filipe Camarão, 67 Tatuapé, São Paulo.
- Número de contato: (11)99317-0906
- Fachada do mercado: <img width="1600" height="1200" alt="fachada_mercado" src="https://github.com/user-attachments/assets/96ddf354-d13e-41de-be66-00efc5e769c5" />

- Inteiror do mercado: <img width="1600" height="1200" alt="interior_mercado" src="https://github.com/user-attachments/assets/b969924b-67c7-4e15-8554-971d6f0eec40" />

- Estoque do mercado: <img width="1600" height="1200" alt="estoque_mercado" src="https://github.com/user-attachments/assets/b0589bb0-c2bd-4588-b628-0f5c1cb43df1" />



---

## 2. Processos de Negócio


- **Principais processos mapeados:** Controle de estoque e vendas
  
- **Fluxogramas:**
  - (fluxograma vendas)
  <img width="565" height="857" alt="fluxograma venda" src="https://github.com/user-attachments/assets/df8b9e98-4f99-426c-a255-53805583e70a" />





  - (fluxograma estoque)
  <img width="454" height="885" alt="fluxograma estoque" src="https://github.com/user-attachments/assets/ae68a1f7-b61f-4a3c-a188-dd305fa9f004" />



---

## 3. Requisitos do Sistema


### 3.1 Requisitos Funcionais
- O sistema deve permitir cadastrar produtos
- O sistema deve atualizar automaticamente a quantidade em estoque após cada venda
- O sistema deve permitir consultar a quantidade disponível de um produto
- O sistema deve permitir cadastrar fornecedores
- O sistema deve permitir associar produtos aos fornecedores que os fornecem
- O sistema deve permitir registrar pedidos de compra feitos a um forncedor
- O sistema deve permitir registrar uma venda com um ou mais produtos
- O sistema deve calcular automaticamente o valor total da venda
- O sistema deve permitr cancelar uma venda e devolver os teins ao estoque

### 3.2 Requisitos Não Funcionais

- Desempenho: o sistema deve suportar multiplos caixas operando ao mesmo tempo sem lentidão
- Disponibilidade: o sistema deve estar dispoínvel durante todo o horário de funcionamento da loja, em caso de queda de internet, o sistema deve continuar permitindo as vendas, sincronizando tudo quando volta.
- Segurança: o sistema deve exigir login e senha (apenas pessoal autorizado).
- Usabilidade: a interface do caixa deve ser simples o suficiente para o que funcionários com pouco treinamento técnico.
---

## 4. Regras de Negócio

- **Regras operacionais:**
- Um produto não pode ser vendido após a data de validade.
- Estoque: a reposição de estoque só pode ser registrada mediante a nota fiscal do fornecedor
- Fornecedor: Um pedido de compra só deve ser realizado para um fornecedor cadastrado, Um fornecedor só pode ser cadastrado com CNPJ válido e dados completos.
- Vendas: uma venda cancelada deve devolver automaticamente os itens ao estoque.
- **Restrições organizacionais:** Exigência legal: Obrigadatoriedade da emissão de notas fiscais das vendas por exigência tributária, produtos perecíveis devem ter a data  de validade em dia por exigência da vigilância sanitária.
---

## 5. Dicionário de Dados Conceitual (Preliminar)


Para cada entidade identificada, liste:

| Atributo | Descrição | Regra de negócio associada |
|----------|-----------|------------------------------|
| *nome do atributo* | *o que ele representa* | *se houver alguma regra (obrigatoriedade, valores possíveis, etc.)* |

*Mantenha o dicionário organizado e padronizado (mesmo formato de tabela para todas as entidades).*

**Atenção à privacidade:** se forem usados exemplos de valores para ilustrar os atributos, esses exemplos devem ser **fictícios** — não utilize dados reais de clientes, fiéis, beneficiários, doadores ou funcionários da organização (nomes, CPFs, contatos etc.), mesmo que tenham sido observados durante a pesquisa de campo. Os exemplos devem apenas ser **coerentes com as operações reais** observadas.

---

## 6. Modelagem Conceitual (Entidades, Atributos, Relacionamentos)


- **Entidades reconhecidas:**
- Produto: Representa os produtos comercializados pelo mercado, sendo necessário para controlar informações como nome, tipo, categoria e preço.
- Categoria_Produto: Permite classificar os produtos em categorias, facilitando sua organização e identificação
- Item_Venda: Representa cada produto incluído em uma venda, permitindo registrar quantidade e valor unitário vendido
- Item_Compra: Representa cada produto incluído em um pedido de compra, permitindo registrar quantidade e valor de cada item.
- Pedido_Compra: Representa os pedidos de produtos feitos aos fornecedores, permitindo controlar as compras realizadas pelo mercado.
- Fornecedor: Representa as empresas que fornecem produtos ao mercado, permitindo registrar e relacionar os fornecedores às compras realizadas.
- Estoque: Representa o controle dos produtos armazenados, permitindo registrar quantidade e informações relacionadas ao armazenamento.
- Funcionário: Representa os funcionários responsáveis pelas atividades relacionadas às vendas e ao funcionamento do mercado.
- Venda: Representa as vendas realizadas pelo mercado, permitindo registrar informações da transação e relacioná-la ao cliente e aos produtos vendidos.
- Cliente: Representa as pessoas que realizam compras no mercado, permitindo armazenar seus dados e relacioná-los às vendas realizadas.
- Lote: Representa cada lote recebido de um produto, permitindo controlar separadamente sua quantidade, data de entrada e data de validade.
- **Atributos e classificações:**
- 
- 
- **Relacionamentos pertinentes:** *como as entidades se conectam.*
- **Restrições e políticas organizacionais aplicadas ao modelo.**

---

## 7. Diagrama Entidade-Relacionamento (DER)
<img width="808" height="757" alt="Captura de tela 2026-09-16 201619" src="https://github.com/user-attachments/assets/6aef4a8c-9599-4efa-ba6e-5c5e4502a59e" />



---

## 8. Justificativa Técnica


Usamos essas entidades e atributos porque foram os dados que nos apresentaram durante a visita/entrevista, usufruímos dessas informações também pois acreditamos que é o que faz mais sentido dentro de um ecossistema de supermercado, por exemplo: o mercado não possui cadastro de clientes, porém decidimos colocar a entidade "cliente" por partirmos da premissa de "fazer sentido" por ser a entidade que efetua a compra de um produto. Apontamos esses relacionamentos e cardinalidades de acordo com o nível de entendimento sobre o conteúdo disponível em slides acadêmicos.

---

## 9. Uso de Inteligência Artificial


Se o grupo usou alguma ferramenta de IA (ChatGPT, Claude, Gemini, Perplexity etc.) em qualquer parte do trabalho, registre **para cada uso relevante**:

| Item | O que registrar |
|------|------------------|
| **Ferramenta e etapa** |  Claude: Usado para auxiliar no aprendizado do github, porque ninguém do grupo era familiarizado com essa ferramenta. Gemini: Usado na criação do DER.  |
| **Motivação** | Claude: porque de acordo com as nossas pesquisas, concluímos que seria a melhor opção dentre as outras IA's, por ser mais técnico. Gemini: foi apenas uma escolha por preferência. |
| **Prompt(s) utilizados** |  Claude: sucessivas perguntas de como funciona o github. Por exemplo: "como adicionar um colaborador ao github", "como salvar as alterações feitas dentro do arquivo Readme". |
| **Resposta recebida** | Resposta do Claude: Vá até o repositório no GitHub onde você quer adicionar o colaborador. Clique na aba Settings no menu superior — você precisa ser dono do repositório ou ter permissão de administrador para ver essa opção. No menu lateral esquerdo, clique em Collaborators and teams (ou apenas Collaborators). Clique no botão Add people (pode pedir para confirmar sua senha). Digite o nome de usuário do GitHub, nome completo ou e-mail da pessoa que você quer convidar, e escolha o nível de permissão dela: Read, Triage, Write, Maintain ou Admin. Por fim, clique em Add [nome] to this repository. A pessoa vai receber um convite por e-mail ou notificação no GitHub, que ela precisa aceitar para ter acesso.  |
| **Fontes consultadas e verificadas** |  |
| **Trechos rejeitados ou corrigidos** |  |
| **Justificativa da escolha final** | Decidimos manter as IA's escolhidas por atingir um nível bom de satisfação e coerência nas respostas geradas por elas. |
| **Reflexão crítica** |  |



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

**Entrega final:** README.md completo + DER anexado no repositório GitHub do grupo.
