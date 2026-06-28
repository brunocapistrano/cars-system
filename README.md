# Django Cars

Sistema de cadastro de carros com marcas, ano de fabricacao, ano do modelo, placa, valor e foto.

## Tecnologias

- Python 3
- Django 3.2
- SQLite (banco de dados local)
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

### 4. Execute as migrations

```bash
python manage.py migrate
```

### 5. Crie um superusuario (para acessar o admin)

```bash
python manage.py createsuperuser
```

### 6. Rode o servidor

```bash
python manage.py runserver
```

Acesse http://127.0.0.1:8000/admin/ para o painel administrativo e http://127.0.0.1:8000/cars/ para a listagem de carros.
