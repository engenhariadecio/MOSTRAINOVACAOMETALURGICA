# Metalúrgica — Instruções e planta

Site simples (só HTML) para abrir no celular pelo QR code.

| Arquivo | Conteúdo |
|---|---|
| `index.html` | Menu principal |
| `pre-banho.html` | Instrução de montagem dos cestos (pré-banho) |
| `monovia.html` | Instrução de carregamento na monovia |
| `paletizacao.html` | Instrução de paletização |
| `planta.html` | Vista 3D da planta: pré-banho, banho e pintura |
| `qr.html` | Gera o QR code do site para imprimir |

## Como publicar no GitHub Pages

1. Entre em github.com e clique em **New repository**. Dê um nome (ex.: `metalurgica`) e deixe como **Public**.
2. No repositório novo, clique em **Add file → Upload files** e arraste **todos os arquivos desta pasta** (inclusive o `.nojekyll`). Clique em **Commit changes**.
3. Vá em **Settings → Pages**. Em *Branch*, escolha `main` e a pasta `/ (root)`. Clique em **Save**.
4. Aguarde 1 a 2 minutos. O endereço do site aparece no topo da página, no formato
   `https://SEU-USUARIO.github.io/metalurgica/`
5. Abra `https://SEU-USUARIO.github.io/metalurgica/qr.html` e clique em **Imprimir**. Esse QR code leva direto ao menu principal.

## Como atualizar uma instrução

Envie o novo arquivo com **o mesmo nome** (ex.: `monovia.html`) em *Add file → Upload files*. O QR code continua o mesmo.

Se o arquivo novo vier do gerador de instruções, ele não terá o botão *Voltar ao menu*. Para colocar o botão, cole esta linha logo depois da tag `<body>`:

```html
<a href="index.html" style="position:fixed;top:10px;left:10px;z-index:100000;background:#1f7a52;color:#fff;padding:10px 14px;border-radius:8px;font:600 14px sans-serif;text-decoration:none">‹ Voltar ao menu</a>
```

## Observações

- As páginas precisam de internet no celular: o motor 3D (three.js) é carregado de um CDN.
- Os nomes dos arquivos não têm acento nem espaço, para os links funcionarem em qualquer servidor.
