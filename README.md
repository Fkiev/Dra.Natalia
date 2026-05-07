# Dra. Natália Garcia — Landing Page

Site institucional da Dra. Natália Garcia, advogada trabalhista em Goiânia (OAB/GO 73080).

## Estrutura

```
.
├── index.html              # Pagina unica (HTML + CSS + JS embutidos)
├── vercel.json             # Configuracoes de deploy (cache + headers)
├── assets/
│   ├── dra-natalia-hero.jpg
│   └── dra-natalia-sobre.jpg
└── README.md
```

Sem build. Sem dependencias. Site 100% estatico.

## Deploy no Vercel — 3 opções

### Opção 1: Drag and drop (mais rápido, sem conta tecnica)

1. Acesse https://vercel.com/new
2. Faça login (Google, GitHub ou e-mail)
3. Clique em **"Deploy"** no canto superior direito → **"Browse"** ou arraste a pasta inteira
4. Aguarde 30 segundos. URL provisoria pronta (`projeto.vercel.app`)
5. Em **Settings → Domains**, adicione o dominio proprio (ex: `dranataliagarcia.com.br`)

### Opção 2: Vercel CLI (recomendado para atualizações futuras)

```bash
# 1. Instalar a CLI uma vez
npm i -g vercel

# 2. Dentro da pasta do projeto
cd "caminho/para/2026-05-06_dra-natalia-trabalhista"

# 3. Deploy
vercel

# 4. Para subir versao final em producao
vercel --prod
```

A CLI vai pedir login na primeira vez e cria o projeto automaticamente.

### Opção 3: Via GitHub (deploy automatico a cada push)

1. Crie um repositorio no GitHub (privado ou publico).
2. Suba os arquivos:
   ```bash
   git init
   git add .
   git commit -m "Site Dra. Natalia Garcia"
   git branch -M main
   git remote add origin https://github.com/SEU_USUARIO/dranataliagarcia.git
   git push -u origin main
   ```
3. Em https://vercel.com/new, importe o repositorio.
4. A cada `git push`, o Vercel reconstrói o site automaticamente.

## Domínio próprio

Depois do deploy, em **Settings → Domains**:

1. Clique em **"Add"** e digite `dranataliagarcia.com.br` (ou o dominio escolhido).
2. O Vercel mostra os registros DNS para configurar no registrador (Registro.br, GoDaddy, Hostinger, etc):
   - **Tipo A** → `76.76.21.21`
   - **CNAME** (para `www`) → `cname.vercel-dns.com`
3. Apos configurar no DNS, o Vercel emite SSL gratuito automaticamente em ate 1h.

## O que o vercel.json faz

- **Cache de imagens** por 1 ano (rapidez no carregamento).
- **HTML sempre revalidado** (atualizacoes aparecem na hora).
- **Headers de seguranca** (anti-clickjacking, anti-MIME-sniffing, referrer policy).
- **URLs limpas** (sem `.html` no final).

## Manutenção

Para atualizar texto ou imagens:

1. Edite `index.html` ou substitua arquivos em `assets/`.
2. Use uma das opcoes acima:
   - **CLI**: `vercel --prod`
   - **GitHub**: `git commit -am "ajuste" && git push`
   - **Drag and drop**: arraste a pasta atualizada na dashboard do Vercel.

## Contato técnico

Site construido por [Vertice](#).
WhatsApp da Dra. Natalia para validacoes de copy: (62) 99672-4509.
