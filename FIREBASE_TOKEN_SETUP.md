# 🔑 COMO GERAR O TOKEN DO FIREBASE

Seu GitHub Actions precisa de um token para fazer deploy automaticamente. Este arquivo explica como gerar esse token **SEM usar terminal**.

## ✅ Passo 1: Abrir o Firebase Console

1. Abra: https://console.firebase.google.com
2. Selecione o projeto: **mindai-v5-1**

## ✅ Passo 2: Gerar a Chave do Serviço (Recomendado - Mais Seguro)

Esta é a **forma RECOMENDADA** e mais simples:

### 2.1 Vá para "Configurações do Projeto"
- No Firebase Console, clique na ⚙️ (engrenagem) no canto superior esquerdo
- Clique em "Configurações do projeto"

### 2.2 Abra a aba "Contas de Serviço"
- Procure pela aba "Contas de Serviço"
- Clique nela

### 2.3 Gere uma Nova Chave Privada
- Clique em "Gerar nova chave privada"
- Um arquivo JSON será baixado automaticamente
- **NÃO compartilhe este arquivo com ninguém!**

### 2.4 Copie o Conteúdo do Arquivo JSON
- Abra o arquivo JSON que foi baixado
- Copie **TODO** o conteúdo (Ctrl+A, depois Ctrl+C)

## ✅ Passo 3: Adicionar o Token ao GitHub

1. Abra: https://github.com/llomp23/mind-ai-app/settings/secrets/actions
2. Clique em "New repository secret"
3. Preencha assim:
   - **Name:** `FIREBASE_TOKEN`
   - **Secret:** Cole o conteúdo JSON que você copiou
4. Clique em "Add secret"

## ✅ Passo 4: Modificar o Arquivo deploy.yml

Agora precisa trocar uma linha no arquivo deploy.yml para usar a chave corretamente:

1. No GitHub, abra: https://github.com/llomp23/mind-ai-app/blob/main/.github/workflows/deploy.yml
2. Clique no ícone de lápis (✏️) para editar
3. Procure pela linha que tem: `--token [4]` 
4. **Troque tudo isso:**

```
firebase deploy --only hosting --project mindai-v5-1 --token ${{ secrets.FIREBASE_TOKEN }}
```

5. Clique em "Commit changes"

## 🎉 Pronto!

O deployment automático já deve estar funcionando! Agora quando você fizer mudanças no repositório, o GitHub Actions vai:

✅ Baixar o código  
✅ Fazer o build  
✅ Fazer o deploy no Firebase automaticamente  

## ❓ Dúvidas?

Se algo não funcionar, verifique:
- A chave JSON está colada corretamente no secret
- O nome do secret está exatamente: `FIREBASE_TOKEN`
- O arquivo deploy.yml foi editado com a linha correta

---

## 📚 Referências

- Firebase Console: https://console.firebase.google.com
- GitHub Secrets: https://github.com/llomp23/mind-ai-app/settings/secrets/actions
- Deploy.yml: https://github.com/llomp23/mind-ai-app/blob/main/.github/workflows/deploy.yml
