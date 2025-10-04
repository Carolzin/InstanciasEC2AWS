# ♨️ Desafio DIO Santander Code Girls - Gerenciamento de Instâncias EC2 na AWS

## 📚 Sobre o Projeto

Esse projeto foi desenvolvido como parte do desafio prático da formação na DIO, com o objetivo de consolidar conhecimentos sobre **instâncias EC2**, **armazenamento com S3**, e **arquitetura básica na AWS**.


## 📌 Diagrama da Arquitetura

![Diagrama da Arquitetura](./Imagens/diagrama%20-%20Copia.png)


### 🧭 Explicação do Diagrama

Este diagrama representa uma arquitetura simples, mas funcional, para hospedar uma aplicação web na nuvem utilizando serviços da AWS.

#### ▶️ Fluxo de Acesso

1. **Usuários (Internet)**  
   Pessoas acessam o sistema por meio de um navegador ou outro cliente web, a partir da internet.

2. **Internet Gateway (IGW)**  
   Um *Internet Gateway* é anexado à VPC e permite a comunicação entre os recursos da VPC e a internet. Ele é essencial para que instâncias na sub-rede pública consigam enviar e receber dados da internet.

3. **VPC (Virtual Private Cloud)**  
   Uma VPC é uma rede virtual isolada onde os recursos da AWS são implantados. Aqui, definimos uma arquitetura segura e controlada para nossos recursos.

4. **Sub-rede Pública**  
   Dentro da VPC, criamos uma **sub-rede pública**, ou seja, uma sub-rede associada a uma rota que aponta para o IGW. Recursos dentro desta sub-rede podem ter IPs públicos e se comunicar diretamente com a internet.

5. **Instância EC2 (Servidor Web)**  
   Uma instância EC2 foi criada dentro da sub-rede pública e configurada como um servidor web (por exemplo, com Apache ou Nginx). Ela recebe um IP público, permitindo acesso direto via internet, e responde às requisições dos usuários.

6. **Bucket S3**  
   O bucket S3 é utilizado como armazenamento de objetos (arquivos estáticos como imagens, CSS, JavaScript ou até backups). Embora o S3 seja um serviço global (não fica "dentro" da VPC), ele aparece no diagrama porque pode ser utilizado pela aplicação na EC2, seja para ler dados, armazenar arquivos ou servir conteúdo estático ao usuário final.

---
## 🔗 Recursos Úteis
- [Documentação Oficial AWS EC2](https://docs.aws.amazon.com/pt_br/ec2/)
- [Documentação Oficial AWS S3](https://docs.aws.amazon.com/pt_br/s3/)

