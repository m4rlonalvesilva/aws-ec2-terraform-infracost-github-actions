# CRIAÇÃO DO REPOSITÓRIO

git init
git status
git add .
git status
git commit -m 'first commit'
git branch -M main
git remote add origin git@github.com:m4rlonalvesilva/aws-ec2-terraform-infracost-github-actions.git
git push -u origin main

______________________________________________

# INSTALAÇÃO INFRACOST
curl -fsSL https://raw.githubusercontent.com/infracost/infracost/master/scripts/install.sh | sh

# VERIFICAR VERSÃO
infracost --version

# REGISTRAR API KEY
infracost configure get api_key

# CONFIGURAR MOEDA
infracost configure set currency BRL 

# VERIFICAR GASTOS C/ INFRACOST
infracost breakdown --path .

______________________________________________

# TERRAFORM
terraform init
terraform fmt
terraform validate
terraform plan --out='plan.out'
terraform apply 'plan.out'

______________________________________________

# PULL REQUEST

git checkout -b feature/git-action