# 🚀 DEPLOY NO RENDER.COM - GUIA RÁPIDO

## Status: ✅ PRONTO PARA DEPLOY

Seu repositório foi configurado completamente para deploy no Render.com!

## O que foi feito:

1. **✅ render.yaml** - Arquivo de configuração do Render
2. **✅ server.js** - Express server para servir a SPA em produção
3. **✅ .env.example** - Template de variáveis de ambiente
4. **✅ package.json** - Atualizado com express e script de start
5. **✅ vite.config.ts** - Otimizado para produção com minification
6. **✅ .gitignore** - Protege .env.local de ser versionado
7. **✅ README.md** - Instruções atualizadas

## Passo a passo para fazer o deploy:

### 1️⃣ Vá para Render Dashboard
```
https://dashboard.render.com
```

### 2️⃣ Crie um novo Web Service
- Clique em "New +" → "Web Service"

### 3️⃣ Conecte seu repositório GitHub
- Selecione: `phstatic1/phstatic12`
- Branch: `main`

### 4️⃣ Configure o serviço
**Nome do serviço:** `phstatic2` (ou outro que preferir)

**Build Command:**
```
npm install && npm run build
```

**Start Command:**
```
npm start
```

**Environment Variables:**
- Clique em "Add Environment Variable"
- Key: `GEMINI_API_KEY`
- Value: `[Cole aqui sua chave Gemini API]`

### 5️⃣ Deploy!
Clique em "Create Web Service" e deixe o Render fazer o resto.

---

## 📝 Seu domínio no Render será:
```
https://phstatic2.onrender.com
```
(ou `https://<seu-custom-domain>` se configurar um domínio personalizado)

## ⚙️ Variáveis de ambiente:

**IMPORTANTE:** Configure a variável `GEMINI_API_KEY` no painel do Render.

Ela está definida em:
- `vite.config.ts` - Injetada no build
- `.env.local` - Para desenvolvimento local

### Como obter sua Gemini API Key:
1. Vá para https://makersuite.google.com/app/apikey
2. Crie uma nova chave (se não tiver)
3. Copie e cole no Render Dashboard

---

## 🔄 Para fazer atualizações depois:

Basta fazer push para `main`:
```bash
git add .
git commit -m "sua mensagem"
git push origin main
```

Render fará o redeploy automaticamente! ✨

---

## 📞 Suporte:

- Documentação do Render: https://render.com/docs
- Documentação do Vite: https://vitejs.dev
- Documentação do React: https://react.dev

---

**Repositório:** https://github.com/phstatic1/phstatic12
**Pronto para produção:** ✅ SIM
