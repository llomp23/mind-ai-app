# 🚀 GUIA DE CONFIGURAÇÃO - MIND.AI

## ✅ O QUE JÁ FOI FEITO PARA VOCÊ

Nós já corrigimos 2 problemas grandes:

1. **✓ Página de Login Criada**
   - Agora quando você entra no app, aparece um formulário de login
   - Você precisa fazer login com email e senha
   - Só após fazer login, você consegue acessar os mentores

2. **✓ Respostas dos Mentores Corrigidas**
   - Os mentores agora mostram mensagens de erro quando algo dá errado
   - O código está melhor organizado
   - Tudo funciona mais suavemente

3. **✓ Configuração Automática de Deploy**
   - Criamos um sistema que faz deploy automático quando você faz mudanças
   - Você não precisa mais usar linhas de comando complicadas
   - Tudo acontece automaticamente pelo GitHub

---

## 📋 O QUE VOCÊ AINDA PRECISA FAZER

### 1️⃣ Adicionar Dados dos Mentores no Firebase

Os mentores precisam estar salvos no banco de dados do Firebase. Siga estes passos:

**Passo A:** Abra o console do Firebase
- Link: https://console.firebase.google.com/u/0/project/mindai-v5-1/firestore/databases/default/data

**Passo B:** Crie uma coleção chamada "mentores"
- Clique em "Criar Coleção"
- Nome: `mentores`
- Clique OK

**Passo C:** Adicione os mentores (crie documentos com esses dados):

```
mentor_01:
  name: "Dr. Saúde"
  specialty: "Saúde e Bem-estar"
  description: "Especialista em saúde preventiva"

mentor_02:
  name: "Coach Produtividade"
  specialty: "Produtividade"
  description: "Especialista em gestão de tempo"

mentor_03:
  name: "Mentor Financeiro"
  specialty: "Finanças"
  description: "Especialista em educação financeira"

... (adicione todos os 10 mentores assim)
```

### 2️⃣ Adicionar a Chave da Gemini API

A Gemini API precisa de uma chave para funcionar:

**Passo A:** Pegue sua chave Gemini
- Acesse: https://aistudio.google.com/app/apikey
- Copie a chave (não compartilhe com ninguém!)

**Passo B:** Adicione a chave no código
- No GitHub, abra o arquivo `index.html`
- Procure por: `YOUR_GEMINI_API_KEY`
- Substitua pelo sua chave

**Passo C:** Faça um commit
- Clique em "Commit changes"
- Escreva: "Add Gemini API key"

---

## 🧪 COMO TESTAR SE TUDO ESTÁ FUNCIONANDO

### Teste 1: Verificar Login
1. Abra: https://mindai-v5-1.web.app/
2. Você deve ver uma página de login
3. Faça login com email e senha (crie uma conta)
4. Você deve ver os mentores

### Teste 2: Verificar Mentores
1. Clique em um mentor
2. Digite uma pergunta
3. A Gemini API deve responder
4. Se vir uma resposta, está funcionando!

---

## 🔧 RESOLUÇÃO DE PROBLEMAS

**Problema:** Vejo erro "404" quando abro o app
- **Solução:** Aguarde 2-3 minutos para o deploy completar

**Problema:** Login não aparece
- **Solução:** Faça F5 (refresh) na página

**Problema:** Mentores não respondem
- **Solução:** Verifique se:
  - Você adicionou os mentores no Firebase
  - A chave Gemini está no arquivo `index.html`
  - Você fez login corretamente

**Problema:** Não consegui adicionar dados no Firebase
- **Solução:** 
  - Verifique se está logado no Firebase
  - Clique em "Criar Documento" (não "Criar Campo")

---

## 📚 LINKS IMPORTANTES

- **App:** https://mindai-v5-1.web.app/
- **Firebase Console:** https://console.firebase.google.com/u/0/project/mindai-v5-1/
- **GitHub Repo:** https://github.com/llomp23/mind-ai-app
- **Gemini API:** https://aistudio.google.com/app/apikey
- **Firebase Docs:** https://firebase.google.com/docs

---

## ✨ PRÓXIMOS PASSOS APÓS CONFIGURAR

Uma vez que tudo estiver funcionando:

1. ✓ Login está funcionando
2. ✓ Mentores respondem
3. ✓ App em produção

Você pode:
- Adicionar mais mentores
- Personalizar as respostas
- Melhorar o design
- Adicionar novos recursos

---

**PRECISA DE AJUDA?** 
Se algo não funcionar, me chame! 🙋
