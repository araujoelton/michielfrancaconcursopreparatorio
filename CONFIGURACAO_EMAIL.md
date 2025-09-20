# Configuração do Envio de E-mail

Para que o formulário de contato funcione corretamente, você precisa configurar o EmailJS. Siga os passos abaixo:

## 1. Criar conta no EmailJS

1. Acesse [https://www.emailjs.com/](https://www.emailjs.com/)
2. Crie uma conta gratuita
3. Faça login no painel

## 2. Configurar o serviço de e-mail

1. No painel do EmailJS, vá em "Email Services"
2. Clique em "Add New Service"
3. Escolha seu provedor de e-mail (Gmail, Outlook, etc.)
4. Siga as instruções para conectar sua conta de e-mail
5. Anote o **Service ID** gerado

## 3. Criar template de e-mail

1. Vá em "Email Templates"
2. Clique em "Create New Template"
3. Use o seguinte template:

**Assunto:** Nova mensagem do site - {{from_name}}

**Conteúdo:**
```
Nova mensagem recebida através do site:

Nome: {{from_name}}
E-mail: {{from_email}}
Telefone: {{telefone}}
Curso de interesse: {{curso_interesse}}

Mensagem:
{{message}}

---
Enviado através do site Michel França Curso Preparatório
```

4. Salve o template e anote o **Template ID**

## 4. Obter chave pública

1. Vá em "Account" > "General"
2. Copie a **Public Key**

## 5. Atualizar o código

No arquivo `script.js`, substitua os seguintes valores:

- `YOUR_PUBLIC_KEY` pela sua Public Key
- `YOUR_SERVICE_ID` pelo seu Service ID  
- `YOUR_TEMPLATE_ID` pelo seu Template ID

## 6. Testar

1. Abra o site no navegador
2. Preencha o formulário de contato
3. Envie uma mensagem de teste
4. Verifique se o e-mail foi recebido

## Limites da conta gratuita

- 200 e-mails por mês
- 2 templates
- 1 serviço de e-mail

Para mais e-mails, considere fazer upgrade para um plano pago.
