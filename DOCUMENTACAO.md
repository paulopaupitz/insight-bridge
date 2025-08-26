# Documentação das Funções JavaScript

## utils.js
Este arquivo contém funções utilitárias:
- `inverterData(isoDate)`: Converte uma data do formato ISO (YYYY-MM-DD) para o formato brasileiro (DD/MM/YYYY)
- `printDiv()`: Aciona a função de impressão do navegador

## table.js
Gerencia a tabela de exibição dos dados:
- `createRow(client, index)`: Cria uma nova linha na tabela com os dados do cliente
- `clearTable()`: Remove todas as linhas da tabela
- `updateTable()`: Atualiza a tabela com todos os clientes do banco de dados
- `editDeleteView(event)`: Gerencia os eventos de edição e exclusão de clientes

## storage.js
Gerencia o armazenamento local dos dados:
- `getLocalStorage()`: Recupera os dados do localStorage
- `setLocalStorage(dbClient)`: Salva os dados no localStorage
- `createClient(client)`: Adiciona um novo cliente ao banco de dados
- `readClient()`: Lê todos os clientes do banco de dados
- `updateClient(index, client)`: Atualiza os dados de um cliente específico
- `deleteClient(index)`: Remove um cliente do banco de dados

## modal.js
Controla o modal de edição:
- `openModal()`: Abre o modal de edição
- `closeModal()`: Fecha o modal de edição
- `fillModal(client)`: Preenche o modal com os dados do cliente
- `isValidModalFields()`: Verifica se todos os campos do modal são válidos
- `saveEdit()`: Salva as alterações feitas no modal

## main.js
Arquivo principal que inicializa a aplicação:
- Configura os event listeners para:
  - Botão de cadastro
  - Tabela de dados (para edição e exclusão)
  - Botão de salvar edição no modal
  - Botão de fechar modal
  - Botão de impressão

## form.js
Gerencia o formulário de cadastro:
- `isValidFields()`: Verifica se todos os campos do formulário são válidos
- `clearFields()`: Limpa todos os campos do formulário
- `saveClient()`: Salva um novo cliente no banco de dados 

insight-bridge/
├── Img/                         # Contém imagens usadas na aplicação
├── js/
│   ├── auth.js                  # Lógica de autenticação de usuário
│   ├── form.js                  # Gerencia validações de formulário e salvamento de dados
│   ├── main.js                  # Lógica principal da aplicação e listeners de eventos
│   ├── modal.js                 # Controla o comportamento do modal (abrir, fechar, preencher, salvar)
│   ├── search.js                # Implementa a funcionalidade de busca para tabelas
│   ├── storage.js               # Gerencia o armazenamento de dados no localStorage (operações CRUD para clientes e administradores)
│   ├── table.js                 # Lida com a criação e atualização dinâmica de tabelas
│   └── utils.js                 # Contém funções utilitárias (inversão de data, impressão, modo escuro)
├── pages/
│   ├── cadastro-admin.html      # Página de registro de administrador
│   ├── cadastro-cliente.html    # Página de registro de cliente
│   ├── dashboard.html           # Dashboard principal com listagem de clientes e estatísticas
│   └── relatorios.html          # Página de relatórios com lista de clientes pesquisável e opção de impressão
├── styles/
│   ├── cadastro-adm.css         # Estilo para a página de registro de administrador
│   ├── cadastro-cliente.css     # Estilo para a página de registro de cliente
│   ├── dark-theme.css           # Estilos para o modo escuro
│   ├── dashboard.css            # Estilo para a página do dashboard
│   ├── login.css                # Estilo para a página de login
│   ├── main.css                 # Importa todos os outros arquivos CSS
│   ├── modal.css                # Estilo para modais
│   ├── relatorio.css            # Estilo para a página de relatórios
│   └── style.css                # Estilo principal para elementos gerais
├── DOCUMENTACAO.md              # Documentação do projeto
├── README.md                    # Este arquivo README
└── index.html                   # Página de login