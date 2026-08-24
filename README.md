# Sistema — protótipo PWA

Este é um protótipo local, sem backend e sem IA real ainda.

## O que já funciona
- escolha de energia atual;
- check-in rápido com alternativas;
- texto livre;
- gravação de áudio usando o microfone;
- salvamento de registros em armazenamento local;
- salvamento de áudio em IndexedDB;
- funcionamento offline depois que a PWA é carregada;
- instalação na tela inicial em navegadores compatíveis.

## Como testar sem computador
A maneira mais simples é hospedar estes arquivos em um serviço estático gratuito, como GitHub Pages, Netlify ou Cloudflare Pages, e abrir o link no Chrome do Android.
Depois use a opção “Adicionar à tela inicial” / “Instalar app”.

Importante: abrir `index.html` diretamente como arquivo local pode impedir service worker e microfone em alguns navegadores. O ideal é usar HTTPS.

## Próxima etapa para IA real
Não coloque uma chave da OpenAI diretamente dentro deste `index.html`.
O correto é:
1. App envia o registro para um backend seu.
2. Backend chama a API da IA.
3. Backend devolve a resposta.
4. App mostra a resposta e salva apenas o necessário.

Isso evita expor sua chave e permite aplicar regras do Manual Mestre.
