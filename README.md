# resumo_cloudformation_
Resumo completo sobre CloudFormation


"""
📦 AWS CloudFormation — Resumo Completo

Este arquivo contém anotações e conceitos estudados sobre AWS CloudFormation, formatos de modelos,
benefícios, criação de stacks e diferença para Terraform.

-------------------------------------------------------------
🟦 O que é AWS CloudFormation

AWS CloudFormation é um serviço de Infraestrutura como Código (IaC) que permite criar, modificar e
gerenciar recursos AWS utilizando arquivos de template (YAML ou JSON).

Com ele, podemos automatizar a criação de:
- Redes (VPC, Subnets, Gateways)
- Instâncias EC2
- Bancos de Dados
- Funções Lambda
- Storage (S3)
- Segurança (IAM, Security Groups)
- Balanceadores, Filas e muito mais

Ele cria tudo em uma **Stack**, que representa um conjunto de recursos gerenciados juntos.

-------------------------------------------------------------
✅ Benefícios do AWS CloudFormation

- Automação e padronização da infraestrutura
- Reprodutibilidade entre ambientes (dev, stage, prod)
- Auditoria e versionamento com Git
- Reutilização de templates
- Rollback automático em falhas
- Total integração com serviços AWS
- Documentação viva da infraestrutura (Infra como Código)

-------------------------------------------------------------
📝 Formatos para criação de modelos

CloudFormation suporta dois formatos:

1️⃣ **YAML** (recomendado — mais simples e legível)  
2️⃣ **JSON** (suportado — mais verboso)

Exemplo mínimo YAML:

AWSTemplateFormatVersion: "2010-09-09"
Description: Exemplo de Bucket S3

Resources:
  MeuBucket:
    Type: AWS::S3::Bucket
    Properties:
      BucketName: exemplo-cf-bucket-demo

-------------------------------------------------------------
🧭 Acessando o AWS CloudFormation para criar uma Stack

Formas de criar uma stack:

✅ Console AWS (Interface Web)  
✅ CLI (linha de comando)  
✅ API  
✅ CloudShell

Passos no console:
1. Acessar AWS CloudFormation
2. Create Stack
3. Upload do arquivo template
4. Configurar permissões e parâmetros
5. Criar stack e acompanhar execução

-------------------------------------------------------------
⚙️ Deploy via CLI

aws cloudformation create-stack \
  --stack-name MinhaStack \
  --template-body file://template.yml

-------------------------------------------------------------
🆚 Diferença entre CloudFormation e Terraform

| CloudFormation | Terraform |
|---------------|-----------|
| Ferramenta da AWS | Multicloud (AWS, Azure, GCP, etc) |
| Suporte nativo a serviços AWS | Depende de providers |
| YAML/JSON | HCL (linguagem própria e mais clara) |
| Rollback automático | Requer configuração |
| Fortemente integrado com AWS | Mais flexível e portável |

Em resumo:
- Quer multicloud? → **Terraform**
- É 100% AWS e quer integração total? → **CloudFormation**

-------------------------------------------------------------

📌 Conclusão

CloudFormation é uma ferramenta essencial para automatizar infraestrutura na AWS.  
Ele permite criar ambientes completos e consistentes, com versionamento, automação
e boas práticas DevOps.

"""
