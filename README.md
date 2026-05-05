# Strava Performance Dashboard

PWA (Progressive Web App) para monitoramento de performance de treinos via API do Strava.

## Como publicar no GitHub Pages

### 1. Criar o repositório

```bash
# No terminal do seu computador:
git init strava-perf
cd strava-perf
```

Copie os arquivos `index.html`, `manifest.json` e `icon.png` para esta pasta.

```bash
git add .
git commit -m "feat: strava performance dashboard"
```

Crie o repositório em github.com/new (pode ser público ou privado).

```bash
git remote add origin https://github.com/SEU_USUARIO/strava-perf.git
git push -u origin main
```

### 2. Ativar GitHub Pages

1. Acesse seu repositório no GitHub
2. Vá em **Settings → Pages**
3. Em "Source", selecione **Deploy from a branch**
4. Branch: `main` / Pasta: `/ (root)`
5. Clique em **Save**

Em ~1 minuto, o app estará disponível em:
```
https://SEU_USUARIO.github.io/strava-perf/
```

### 3. Configurar o app no Strava

1. Acesse [strava.com/settings/api](https://www.strava.com/settings/api)
2. Crie um app com qualquer nome
3. Em **"Authorization Callback Domain"**, coloque:
   ```
   SEU_USUARIO.github.io
   ```
4. Copie o **Client ID** e **Client Secret**

### 4. Conectar no app

1. Abra `https://SEU_USUARIO.github.io/strava-perf/` no **Safari do iPhone**
2. Clique em **CONECTAR** (canto superior direito)
3. Cole Client ID e Secret
4. Autorize no Strava

### 5. Adicionar à tela inicial do iPhone

1. No Safari, toque em **⬜ Compartilhar**
2. Toque em **"Adicionar à Tela de Início"**
3. Confirme o nome e toque em **Adicionar**

✅ O app aparece como ícone nativo, abre em tela cheia!

## Estrutura

```
/
├── index.html      # App completo (React + Recharts via CDN)
├── manifest.json   # Configuração PWA para iPhone
├── icon.png        # Ícone do app (gere em https://favicon.io)
└── README.md
```

## Funcionalidades

- 🔥 Streak de semanas consecutivas com barra de progresso
- 📊 6 métricas de performance (km, pace, FC, esforço, etc.)
- 📈 4 gráficos de evolução mensal
- 📅 Visualização da semana atual
- 🟠 Mapa de consistência (heatmap diário)
- 🔐 OAuth com Strava — dados reais do seu perfil
- 📱 PWA instalável no iPhone via Safari
