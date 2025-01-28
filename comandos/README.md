# Iniciar o projeto Django

python -m venv venv
venv\Scripts\activate
pip install django
django-admin startproject project .
python manage.py startapp contact

# Configurar o git

git config --global user.name 'Seu nome'
git config --global user.email 'seu_email@gmail.com'
git config --global init.defaultBranch main

git config --global user.name 'maurosrs'
git config --global user.email 'maurosrs@gmail.com'
git config --global init.defaultBranch main

git config --list

https://github.com/login

# Configure o .gitignore
https://djangowaves.com/tips-tricks/gitignore-for-a-django-project/


git init
git add .
git commit -m 'Mensagem'
git remote add origin URL_DO_GIT

git status
git log --online

git remote add origin https://github.com/maurosrs/projeto_agenda.git
git remote rm origin

git remote add origin git@github.com:maurosrs/projeto_agenda.git

git push origin main

usar no gitbash
ssh-keygen -f ~/.ssh/maurosrs_rsa -t rsa -b 4096
ssh-keygen -f ~/.ssh/maurosrs_rsa

cat ~/.ssh/maurosrs_rsa.pub

ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAACAQC0qcMPNl4IyDoCGS1bJ4aZlGLtgDXaYphzKpP41EeYoGTm2cQQXZAN5S/OmK8qZR//dcVcjv6cL66aHP4ixoEchYwF6GsnxfCw4Swn0VkLRm5MCHUdeeTdY2DMQoGg4OD2iU6Q733EAsgRBYvsXAJZm0aPeW7bZlp6W7GvIEwGrIyokOA8U9EMcqQR+m6+jR3NP49vIdOFp2RQHoh/HgV8jMuth2ieEwLmZRufnRiO3D2yR8Vj5x+GLnnYpCf4b4jdu2L8vFOMEBvL2pr96BDFhEPVqZcOocXBcwNaGerwi84JdMoYE0NethCU2xHGDoGXQfJ0PcacnIFV5wBW6eU7FDF5vyIlT5XDq1Pa1+PMqN8+tjI5gv28iQqTIndFh8wf/U9cgJnlptJTQLsPfl4H6gAAawVryfgVj+uFKKlla4QhSbS0XiwzHSabctiLCQNROQrnALTsTlR8b6+ODliqFpZ5PXg3yxmRukOWE+RqxAcV1Rn7MTC/gR+s83tJmLBDKsP/YD8bfefPhcu2hcx8brcKi2Ud8VX/aVlT115KhfewIP9PtIaHOVZe1X9JpHNeM6vRJVd2KjwdD1rDgVqKxoCwi+AuqVuwiSDlA8bV6u8XA6UVG1gsnDWnaMjTXS4LLcklR/yyf0Ys6yeRV7/hKjLUkVM3qJc/lcYnG0ZCjQ== mauro@ACSQUAL40

eval $(ssh-agent)
ssh-add ~/.ssh/maurosrs_rsa

git remote add origin git@github.com:maurosrs/projeto_agenda.git


git reset HEAD .env

.gitignore
    .env
    venv
    env


git push origin main -u    


# Rodar o servidor
python manage.py runserver

# Migrando a base de dados do Django

python manage.py makemigrations
python manage.py migrate

# Criando e modificando a senha de um super usuário Django

python manage.py createsuperuser
python manage.py changepassword USERNAME

usuario = mauro
senha = 123456


# Modulos
https://docs.djangoproject.com/pt-br/4.2/topics/db/models/

https://docs.djangoproject.com/pt-br/4.2/ref/models/fields/#field-choices

# Shell do Django
python manage.py shell

from contact.models import Contact
Contact
c = Contact(first_name='Gustavo')
c
c.save()
c.last_name = 'Teixeira'
c.phone = '1231231232'
c.save()
c.delete()
c = Contact.objects.get(id=2)
c.pk

c = Contact.objects.all()
for contato in c: contato.first_name

c = Contact.objects.all().filter(id=2)

c = Contact.objects.all().order_by('-id')
c = Contact.objects.all().order_by('id')

c = Contact.objects.create(first_name='Edu', last_name='Vieira)

quit()

from django.contrib.auth.models import User
user = User.objects.create_user(username='usuario,  password='123')
user.is_staff = True
user.save()
user.delete()
quit()

# Trabalhando com o model do Django

Importe o módulo
from contact.models import Contact

Cria um contato (Lazy)
Retorna o contato
contact = Contact(**fields)
contact.save()

Cria um contato (Não lazy)
Retorna o contato
contact = Contact.objects.create(**fields)

Seleciona um contato com id 10
Retorna o contato
contact = Contact.objects.get(pk=10)

Edita um contato
Retorna o contato
contact.field_name1 = 'Novo valor 1'
contact.field_name2 = 'Novo valor 2'
contact.save()

Apaga um contato
Depende da base de dados, geralmente retorna o número
de valores manipulados na base de dados
contact.delete()

Seleciona todos os contatos ordenando por id DESC
Retorna QuerySet[]
contacts = Contact.objects.all().order_by('-id')

Seleciona contatos usando filtros
Retorna QuerySet[]
contacts = Contact.objects.filter(**filters).order_by('-id')

# Collection Static
python manage.py collectstatic

# Instalar o Pillow
pip install pillow

# Instalar o Faker
pip install faker

# Criar contatos fakers
python utils/create_contacts.py

# Filtrar
https://docs.djangoproject.com/en/4.2/ref/models/querysets/#field-lookups

# Paginação
https://docs.djangoproject.com/en/4.2/topics/pagination/

# CSFR
https://pt.wikipedia.org/wiki/Cross-site_request_forgery

https://docs.djangoproject.com/en/5.1/ref/csrf/