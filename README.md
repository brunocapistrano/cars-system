# Django Cars

Sistema de cadastro de carros com marcas, ano de fabricacao, ano do modelo, placa, valor e foto.

## Tecnologias

- Python 3
- Django 6.0
- PostgreSQL (banco de dados)
- Pillow (para upload de imagens)

## Como rodar o projeto

### 1. Clone o repositorio

```bash
git clone <url-do-repositorio>
cd django-cars
```

### 2. Crie e ative um ambiente virtual

**Windows (PowerShell):**
```powershell
python -m venv venv
.\venv\Scripts\Activate.ps1
```

**Linux/macOS:**
```bash
python3 -m venv venv
source venv/bin/activate
```

### 3. Instale as dependencias

```bash
pip install -r requirements.txt
```

### 4. Configure o banco de dados PostgreSQL

Crie um banco de dados chamado `carros` no PostgreSQL:

**Windows:**
```powershell
psql -U postgres -c "CREATE DATABASE carros;"
```

**Linux/macOS:**
```bash
sudo -u postgres psql -c "CREATE DATABASE carros;"
```

Edite o arquivo `app/settings.py` com as credenciais do seu banco:

```python
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        'NAME': 'carros',
        'USER': 'postgres',
        'PASSWORD': 'sua-senha',
        'HOST': 'localhost',
        'PORT': '5432',
    }
}
```

### 5. Execute as migrations

```bash
python manage.py migrate
```

### 6. Crie um superusuario (para acessar o admin)

```bash
python manage.py createsuperuser
```

### 7. Rode o servidor

```bash
python manage.py runserver
```

Acesse http://127.0.0.1:8000/admin/ para o painel administrativo e http://127.0.0.1:8000/cars/ para a listagem de carros.
