Criação de Storage Account no Azure com Terraform

Introdução
Este projeto ilustra a criação de uma Storage Account no Azure utilizando o Terraform. O objetivo é fornecer um guia prático e didático para iniciantes, introduzindo conceitos básicos de infraestrutura como código (IaC) e o armazenamento em nuvem.

Estrutura do Repositório
O repositório é organizado para facilitar o entendimento e a manutenção do projeto. Abaixo está a estrutura dos diretórios e arquivos:

AZURE-STORAGE-ACCOUNT/

│
├── desktop.ini             #  Arquivo de configuração local para o diretório

├── locals.tf               #  Definição de variáveis locais (tags comuns)

├── main.tf                 #  Configuração principal do Terraform e do backend remoto

├── outputs.tf              #  Declaração das saídas, como a URL da Storage Account

├── variables.tf            #  Declaração de variáveis reutilizáveis

└── storage.tf              #  Recursos Terraform para criar a Storage Account e configurações relacionadas

Descrição dos Arquivos

3.1 desktop.ini

Arquivo interno do sistema, usado para personalizar o diretório. Neste projeto, ele não tem impacto direto na execução do Terraform, mas está incluído para demonstração de organização.

3.2 locals.tf

Contém variáveis locais, como tags padrão aplicadas aos recursos. Essas tags ajudam a identificar o proprietário e o método de gerenciamento dos recursos.

3.3 main.tf

Arquivo principal do projeto. Nele, são configurados:

Versão mínima do Terraform.

Provedor Azure Resource Manager (azurerm).

Backend remoto para armazenar o estado do Terraform.

3.4 outputs.tf

Define as saídas do Terraform, como a URL da Storage Account criada. Estas informações podem ser usadas para acessar ou integrar com outros sistemas.

3.5 variables.tf

Declara variáveis reutilizáveis para facilitar a parametrização do projeto. Inclui, por exemplo, a região padrão onde os recursos serão criados.

3.6 storage.tf

Arquivo onde estão definidos todos os recursos necessários para a criação da Storage Account, incluindo:

Grupo de recursos.

Configuração da Storage Account (tipo de redundância, tipo de armazenamento, etc.).

Configuração de rede e acessos.

Explicação do Fluxo de Trabalho

Passo a Passo para Desenvolvimento

Clonar o Repositório
Baixe o repositório localmente para começar.

git clone <URL_DO_REPOSITORIO>
cd AZURE-STORAGE-ACCOUNT

Inicializar o Terraform
Prepare o ambiente Terraform no diretório do projeto.

terraform init

Validar Configurações
Confirme que os arquivos estão configurados corretamente.

terraform validate

Planejar e Aplicar
Gere um plano de execução e aplique as configurações.

terraform plan
terraform apply

Verificar Saídas
Após a aplicação, a URL da Storage Account será exibida como saída.

Requisitos

Conta Azure ativa com permissões administrativas.

Terraform instalado (versão 1.3.0 ou superior).

Acesso ao CLI do Azure para verificação de configurações.

Expansões Futuras

Configurar monitoramento da Storage Account com Azure Monitor.

Implementar políticas de acesso e segurança adicionais.

Automatizar a inicialização com configurações de logging e versionamento
