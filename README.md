# BotFAQ
## Como Executar o Projeto Localmente

### Pré-requisitos
* **Python 3.10** ou superior instalado
* **Git** (opcional, para clonar o repositório)

### Passo a Passo de Instalação e Execução

1. **Clone o repositório e acesse a pasta principal do projeto** (onde se encontra o arquivo `manage.py`):
   ```bash
   git clone <URL_DO_SEU_REPOSITORIO>
   cd Nexo_Studio_Alunos_v1/nexo-studio-main
   ```
   *(Caso o arquivo `manage.py` já esteja na raiz do seu repositório, ignore o comando `cd` acima).*

unzip BotFAQ-site.zip
para acessar ao site usar primeiro : cd Nexo_Studio_Alunos_v1/nexo-studio-main 
python -m pip install -r requisitos.txt 
python manage.py check 
python manage.py migrate
python manage.py runserver

---

## Como Acessar a Área Administrativa e Editar o Site

O projeto conta com **dois painéis administrativos** distintos para gerenciar o conteúdo da **MG Arts**:

### 1. Painel de Gestão da Loja (Dashboard do Sistema)
Interface visual própria do sistema para editar informações comerciais, logotipo, banner, produtos, páginas institucionais e perguntas/respostas do chatbot.

1. Com o servidor rodando (`python manage.py runserver`), acesse:
   * `http://127.0.0.1:8000/login/` *(ou clique em **Entrar** na tela inicial)*
2. Utilize as credenciais criadas automaticamente pelo script `popular_site.py`:
   * **Usuário:** `mgarts`
   * **Senha:** `mgarts@2026`
3. Após o login, você será redirecionado automaticamente para o **Dashboard** (`/dashboard/`), onde poderá modificar todo o conteúdo visual e textual do site.

### 2. Django Admin (Administração Direta do Banco de Dados)
Painel técnico nativo do Django para gerenciar diretamente as tabelas e registros do sistema (`ChatbotRegra`, `Business`, `Offering`, `Page`, `Activity` e `User`).

1. Como o usuário `mgarts` possui permissão apenas de lojista (sem privilégios globais de `is_staff` / `is_superuser`), crie um **superusuário** no terminal (com o ambiente virtual ativado):
   ```bash
   python manage.py createsuperuser
   ```
2. Informe um **nome de usuário**, **e-mail** (opcional) e **senha** quando solicitado no terminal.
3. Inicie o servidor novamente (`python manage.py runserver`) e acesse:
   * `http://127.0.0.1:8000/admin/`
4. Faça login com o superusuário criado para visualizar, adicionar, editar ou excluir registros diretamente no banco de dados.
