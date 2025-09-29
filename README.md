# Configuração do Banco de Dados no Azure e Execução da Aplicação PHP

Este projeto contém instruções para configurar um banco de dados no Azure e conectar uma aplicação PHP utilizando PDO.

---

## 1. Configurar Banco de Dados no Azure

### Passo 1: Criar uma conta no Azure
- Acesse azure.microsoft.com(https://azure.microsoft.com) e crie uma conta.

### Passo 2: Criar um Banco de Dados no Azure SQL Database
1. Acesse o Portal do Azure(https://portal.azure.com).
2. Clique em Criar um recurso.
3. Pesquise por SQL Database e clique em Criar.
4. Preencha as informações básicas:
   - Assinatura: sua assinatura do Azure.
   - Grupo de recursos: crie um novo ou use um existente.
   - Nome do banco: defina o nome do banco.
   - Servidor: crie um novo servidor SQL definindo região, admin e senha.
5. Configure o plano de preço (básico para testes).
6. Clique em Revisar + criar e depois em Criar.

### Passo 3: Configurar o firewall para permitir conexões
1. Vá ao recurso do servidor SQL criado.
2. Em Configurações > Firewall e redes virtuais, adicione seu IP local.
3. Salve as configurações.

---

## 2. Configuração dos Drivers PDO para PHP com SQL Server (Azure)

### Passo 1: Instalar extensões necessárias
Para conectar PHP ao Azure SQL Database via PDO, instale as seguintes extensões:

```bash
sudo pecl install sqlsrv
sudo pecl install pdo_sqlsrv
