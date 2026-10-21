# Minha Telinha: instalar no celular e usar sem internet

Este pacote transforma o app em um aplicativo instalável (PWA). Depois de instalado, ele abre em tela cheia, com ícone na tela inicial, e funciona sem internet.

## O que tem aqui

| Arquivo | Para que serve |
|---|---|
| `index.html` | O app inteiro |
| `manifest.webmanifest` | Nome, cores e ícones do app instalado |
| `sw.js` | Guarda o app no aparelho para abrir offline |
| `icon-192.png`, `icon-512.png`, `icon-maskable-512.png`, `apple-touch-icon.png` | Ícones |

Mantenha todos os arquivos juntos, soltos na mesma pasta (sem criar subpastas).

## Passo a passo com o GitHub Pages (gratuito)

Você precisa de uma conta no GitHub. Crie você mesmo em github.com, pois é uma conta sua.

1. **Descompacte o `.zip`** no computador. Você vai usar os arquivos, não o `.zip`.
2. No GitHub, clique em **+** (canto superior direito) e em **New repository**.
3. Em **Repository name**, digite `telinha`. Marque **Public**. Clique em **Create repository**.
4. Na página do repositório vazio, clique em **uploading an existing file**.
5. **Arraste todos os arquivos** da pasta descompactada para a página (os arquivos, não a pasta). Clique em **Commit changes**.
6. Vá em **Settings → Pages**. Em **Source**, escolha **Deploy from a branch**. Em **Branch**, escolha **main** e a pasta **/ (root)**. Clique em **Save**.
7. Espere 1 a 2 minutos e atualize a página. O endereço do app aparece no topo, neste formato:
   `https://SEU-USUARIO.github.io/telinha/`

O repositório público não expõe nada seu: o app não tem dados pessoais, porque a sua lista fica só no celular.

## Instalar no celular

1. Abra o endereço **com internet**, no Chrome (Android) ou no Safari (iPhone).
2. **Abra o app duas vezes.** A primeira visita guarda o app. A segunda guarda as fontes, para o visual ficar igual sem internet.
3. Instale:
   - **Android (Chrome):** menu ⋮ → **Instalar app** (ou **Adicionar à tela inicial**).
   - **iPhone (Safari):** botão Compartilhar → **Adicionar à Tela de Início**.
4. **Teste:** ligue o modo avião e abra pelo ícone da tela inicial. A capa com a TV deve aparecer.

## Levar a sua lista para o app instalado

Os dados ficam guardados por endereço. O endereço novo começa vazio, então leve a lista pelo Backup:

1. No app antigo (o link do Claude), vá em **Resumo → Backup** e toque em **Copiar**.
2. Cole o texto em um lugar seguro, por exemplo uma mensagem para você mesmo.
3. No app instalado, vá em **Resumo → Backup**, cole o texto no campo e toque em **Restaurar**.

No iPhone, faça o passo 3 **dentro do app instalado** (aberto pelo ícone), porque ele guarda os dados separado do Safari.

## Atualizar o app depois

1. Substitua o `index.html` no repositório (**Add file → Upload files**).
2. Em `sw.js`, troque `telinha-v1` por `telinha-v2` (e assim por diante a cada atualização).
3. O app se atualiza sozinho na segunda vez que você abrir com internet.

## Para a Play Store (opcional, depois)

Com o app hospedado neste endereço, dá para empacotá-lo como app Android (por exemplo com PWABuilder ou Bubblewrap). Você vai precisar de uma conta de desenvolvedor do Google Play (taxa única de US$ 25) e de uma política de privacidade.
