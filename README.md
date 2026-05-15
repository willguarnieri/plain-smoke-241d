# Dra. Daniela Pestilli — Site

Pasta pronta para publicação online. Tudo aqui dentro é estático (HTML + imagens) e pode ser hospedado em qualquer serviço de hospedagem de site estático — sem servidor, sem build.

## Conteúdo

```
deploy/
├── index.html          ← página principal
├── 404.html            ← página de erro amigável
├── robots.txt          ← libera indexação para buscadores
├── sitemap.xml         ← mapa do site para Google
└── assets/
    ├── logo.jpeg
    └── profissional.jpeg
```

## Opções de publicação (gratuitas)

### 1. Netlify (recomendado — mais simples)
1. Acesse https://app.netlify.com/drop
2. Arraste a pasta **`deploy/`** inteira para a área de upload
3. Pronto. Vai gerar uma URL tipo `nome-aleatorio.netlify.app`
4. Em **Domain settings** → **Add custom domain** → coloque `danypestilli.com.br`
5. Netlify mostra os DNS que precisam ser configurados no registrador do domínio (Registro.br ou onde foi comprado)

### 2. Vercel
1. Acesse https://vercel.com → **New Project** → **Upload**
2. Arraste a pasta **`deploy/`**
3. Em **Settings** → **Domains** → adicione `danypestilli.com.br`

### 3. GitHub Pages
1. Crie um repositório no GitHub
2. Faça upload dos arquivos da pasta `deploy/`
3. Em **Settings** → **Pages** → escolha a branch `main` e pasta `/ (root)`
4. Para domínio próprio, adicione um arquivo `CNAME` com `danypestilli.com.br` e configure DNS

### 4. Hostinger / outras hospedagens tradicionais
1. Acesse o painel cPanel ou Gerenciador de Arquivos
2. Faça upload do conteúdo da pasta `deploy/` para a pasta `public_html/`
3. Pronto. O domínio já apontará para o `index.html` automaticamente

## Configurando o domínio danypestilli.com.br

No registrador do domínio (provavelmente Registro.br), aponte os DNS conforme instruções do serviço escolhido. Em geral:
- **Netlify / Vercel**: usar nameservers do serviço, ou criar registros `A` e `CNAME`
- **Hostinger**: já vem com hospedagem, basta apontar o domínio nas configurações

O propagação de DNS pode levar de alguns minutos até 24h.

## Após publicar — checklist SEO

- [ ] Registre o site no [Google Search Console](https://search.google.com/search-console)
- [ ] Envie o `sitemap.xml` (https://danypestilli.com.br/sitemap.xml)
- [ ] Cadastre o consultório no [Google Meu Negócio](https://www.google.com/business/)
- [ ] Verifique se o WhatsApp e Instagram estão respondendo

## Atualizando o site

Para fazer mudanças, edite o `index.html` (ou peça aqui) e refaça o upload da pasta no serviço escolhido. Netlify e Vercel permitem arrastar de novo por cima da versão anterior.
