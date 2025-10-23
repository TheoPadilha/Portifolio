# 🚀 Guia de Deploy na Vercel - Passo a Passo

## 📋 Pré-requisitos

1. Conta no GitHub (criar em: https://github.com)
2. Conta na Vercel (criar em: https://vercel.com)
3. Git instalado no computador

---

## 🔧 Passo 1: Instalar Git (se ainda não tiver)

### Windows:
1. Baixe em: https://git-scm.com/download/win
2. Instale com as opções padrão
3. Reinicie o computador

### Verificar instalação:
```bash
git --version
```

---

## 📁 Passo 2: Criar Repositório no GitHub

### 2.1 - No GitHub:
1. Acesse: https://github.com
2. Faça login (ou crie uma conta)
3. Clique em **"New"** (botão verde, canto superior direito)
4. Configure:
   - **Repository name:** `portifolio` ou `meu-portifolio`
   - **Description:** "Meu portfólio profissional"
   - **Public** (marque esta opção)
   - **NÃO** marque "Add a README"
5. Clique em **"Create repository"**

### 2.2 - Copie os comandos que aparecem
Você verá algo como:
```bash
git remote add origin https://github.com/SEU-USUARIO/portifolio.git
```
**Copie esses comandos!** Vamos usar no próximo passo.

---

## 💻 Passo 3: Inicializar Git no Projeto

### 3.1 - Abrir Terminal na Pasta do Projeto

**Opção 1 - Windows Explorer:**
1. Abra a pasta: `C:\Users\theoh\Documents\OneDrive\Área de Trabalho\portifolio`
2. Clique na barra de endereços
3. Digite `cmd` e pressione Enter

**Opção 2 - VS Code:**
1. Abra a pasta do projeto no VS Code
2. Menu: Terminal → New Terminal
3. Ou pressione: `Ctrl + '`

### 3.2 - Executar Comandos Git

Digite um comando por vez, pressionando Enter após cada:

```bash
git init
```
*Inicializa o repositório Git*

```bash
git add .
```
*Adiciona todos os arquivos*

```bash
git commit -m "Initial commit - Portfólio completo"
```
*Cria o primeiro commit*

```bash
git branch -M main
```
*Renomeia branch para main*

```bash
git remote add origin https://github.com/SEU-USUARIO/portifolio.git
```
**⚠️ IMPORTANTE:** Substitua `SEU-USUARIO` pelo seu nome de usuário do GitHub!

```bash
git push -u origin main
```
*Envia para o GitHub*

**Se pedir login:**
- Username: seu usuário do GitHub
- Password: use um Personal Access Token (explicação abaixo)

---

## 🔑 Personal Access Token (se necessário)

Se pedir senha e não funcionar:

1. Vá em: https://github.com/settings/tokens
2. Clique em **"Generate new token"** → **"Classic"**
3. Configure:
   - **Note:** "Vercel Deploy"
   - **Expiration:** 90 days
   - **Marque:** `repo` (todas as opções)
4. Clique em **"Generate token"**
5. **COPIE O TOKEN** (você só verá uma vez!)
6. Use o token como senha no `git push`

---

## 🌐 Passo 4: Deploy na Vercel

### 4.1 - Criar conta na Vercel:
1. Acesse: https://vercel.com
2. Clique em **"Sign Up"**
3. Escolha: **"Continue with GitHub"**
4. Autorize a Vercel a acessar seus repositórios

### 4.2 - Importar Projeto:
1. No dashboard da Vercel, clique em **"Add New"** → **"Project"**
2. Você verá seus repositórios do GitHub
3. Encontre **"portifolio"** e clique em **"Import"**

### 4.3 - Configurar Deploy:
1. **Project Name:** deixe como está ou mude para algo como `theopadilha-dev`
2. **Framework Preset:** selecione **"Other"**
3. **Root Directory:** deixe `./`
4. **Build & Development Settings:** deixe tudo padrão
5. Clique em **"Deploy"**

### 4.4 - Aguardar Deploy:
- A Vercel vai fazer o deploy automaticamente
- Aguarde 1-2 minutos
- Você verá: **"Congratulations! 🎉"**

---

## 🎉 Pronto! Seu site está no ar!

### Sua URL será algo como:
```
https://portifolio-seunome.vercel.app
```

### Para domínio personalizado:
1. Na Vercel, vá em **Settings** → **Domains**
2. Adicione seu domínio personalizado
3. Configure o DNS conforme instruções

---

## 🔄 Atualizações Futuras

Sempre que fizer mudanças no portfólio:

```bash
git add .
git commit -m "Descrição da mudança"
git push
```

A Vercel vai fazer o deploy automaticamente! ✨

---

## 📱 Compartilhar Portfólio

Depois do deploy, compartilhe seu portfólio:

- ✅ LinkedIn (adicionar no perfil)
- ✅ Instagram (bio)
- ✅ WhatsApp (status)
- ✅ Currículo (adicionar URL)

---

## 🆘 Problemas Comuns

### "Git não é reconhecido"
**Solução:** Instale o Git e reinicie o computador

### "Permission denied"
**Solução:** Use Personal Access Token em vez de senha

### "Repository not found"
**Solução:** Verifique se copiou a URL correta do GitHub

### "Build failed" na Vercel
**Solução:** Verifique se todos os arquivos foram commitados

---

## 📞 Precisa de Ajuda?

Se tiver algum erro, me mande:
1. Print do erro
2. Comando que executou
3. Mensagem de erro completa

---

## ✅ Checklist Final

- [ ] Git instalado
- [ ] Conta GitHub criada
- [ ] Repositório criado no GitHub
- [ ] Código enviado para GitHub (`git push`)
- [ ] Conta Vercel criada
- [ ] Projeto importado na Vercel
- [ ] Deploy concluído com sucesso
- [ ] Site acessível na URL da Vercel

---

**Boa sorte com o deploy! 🚀**
