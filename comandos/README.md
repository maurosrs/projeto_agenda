Iniciar o projeto Django

python -m venv venv
venv\Scripts\activate
pip install django
django-admin startproject project .

Configurar o git

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

git push origin master

usar o gitbash
ssh-keygen -f ~/.ssh/maurosrs_rsa -t rsa -b 4096
ssh-keygen -f ~/.ssh/maurosrs_rsa

cat ~/.ssh/maurosrs_rsa.pub

ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAACAQC0qcMPNl4IyDoCGS1bJ4aZlGLtgDXaYphzKpP41EeYoGTm2cQQXZAN5S/OmK8qZR//dcVcjv6cL66aHP4ixoEchYwF6GsnxfCw4Swn0VkLRm5MCHUdeeTdY2DMQoGg4OD2iU6Q733EAsgRBYvsXAJZm0aPeW7bZlp6W7GvIEwGrIyokOA8U9EMcqQR+m6+jR3NP49vIdOFp2RQHoh/HgV8jMuth2ieEwLmZRufnRiO3D2yR8Vj5x+GLnnYpCf4b4jdu2L8vFOMEBvL2pr96BDFhEPVqZcOocXBcwNaGerwi84JdMoYE0NethCU2xHGDoGXQfJ0PcacnIFV5wBW6eU7FDF5vyIlT5XDq1Pa1+PMqN8+tjI5gv28iQqTIndFh8wf/U9cgJnlptJTQLsPfl4H6gAAawVryfgVj+uFKKlla4QhSbS0XiwzHSabctiLCQNROQrnALTsTlR8b6+ODliqFpZ5PXg3yxmRukOWE+RqxAcV1Rn7MTC/gR+s83tJmLBDKsP/YD8bfefPhcu2hcx8brcKi2Ud8VX/aVlT115KhfewIP9PtIaHOVZe1X9JpHNeM6vRJVd2KjwdD1rDgVqKxoCwi+AuqVuwiSDlA8bV6u8XA6UVG1gsnDWnaMjTXS4LLcklR/yyf0Ys6yeRV7/hKjLUkVM3qJc/lcYnG0ZCjQ== mauro@ACSQUAL40

eval $(ssh-agent)
ssh-add ~/.ssh/maurosrs_rsa

git remote add origin git@github.com:maurosrs/projetoagenda.git


git reset HEAD .env

.gitignore
    .env
    venv
    env


git push origin main -u    