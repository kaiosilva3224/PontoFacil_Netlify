# PontoFacil

Sistema de controle de ponto eletrônico baseado na web com múltiplos subdomínios.

## Estrutura do Projeto

### Páginas Principais
- **index.html** - Página inicial com login e registro
- **admin.html** - Painel administrativo do sistema
- **empresa.html** - Gestão de empresas e funcionários
- **ponto.html** - Interface de controle de ponto

### Subdomínios
- `pontofacil.app.br` - Página principal
- `admin.pontofacil.app.br` - Painel administrativo
- `app.pontofacil.app.br` - Gestão de empresas
- `ponto.pontofacil.app.br` - Controle de ponto

## Tecnologias Utilizadas

- **Frontend**: HTML5, CSS3, JavaScript
- **Backend**: Firebase (Authentication + Firestore)
- **Hosting**: Netlify com deployment automatizado
- **PWA**: Service Worker e Web App Manifest

## Configuração de Deployment

O projeto utiliza Netlify para hosting com configuração de subdomínios através do arquivo `netlify.toml`.

### Estrutura de Arquivos
```
├── index.html          # Página principal
├── admin.html          # Painel admin
├── empresa.html        # Gestão de empresas
├── ponto.html          # Controle de ponto
├── manifest.json       # PWA manifest
├── service-worker.js   # Service worker
├── netlify.toml        # Configuração Netlify
├── _redirects          # Fallback SPA
└── images/             # Ícones PWA
    ├── icon-192x192.png
    └── icon-512x512.png
```

## Firebase Configuration

O projeto está integrado com Firebase para:
- **Authentication**: Login/registro de usuários
- **Firestore**: Banco de dados NoSQL
- **Hosting**: Backup de hosting (opcional)

## Deployment

O deployment é automatizado através do GitHub + Netlify:
1. Push para o repositório GitHub
2. Netlify detecta mudanças automaticamente
3. Build e deploy automático
4. Subdomínios configurados automaticamente

## Desenvolvimento Local

Para desenvolvimento local, abra os arquivos HTML diretamente no navegador ou use um servidor local:

```bash
# Usando Python
python -m http.server 8000

# Usando Node.js
npx serve .
```

## Contribuição

1. Faça fork do projeto
2. Crie uma branch para sua feature (`git checkout -b feature/nova-funcionalidade`)
3. Commit suas mudanças (`git commit -am 'Adiciona nova funcionalidade'`)
4. Push para a branch (`git push origin feature/nova-funcionalidade`)
5. Abra um Pull Request
