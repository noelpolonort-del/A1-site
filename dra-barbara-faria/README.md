# Site Dra. Bárbara Faria — deploy na Vercel

Site estático de uma página só (`index.html`), sem build, sem dependências. Pronto pra subir assim que você tiver o CLI da Vercel logado no seu computador (o login não funciona daqui do sandbox — ver conversa).

## Passo a passo (no seu computador)

1. Instale o CLI, se ainda não tiver:
   ```
   npm i -g vercel
   ```

2. Entre nesta pasta e faça login (abre o navegador pra autenticar):
   ```
   cd dra-barbara-faria
   vercel login
   ```

3. Primeiro deploy (gera uma URL de preview `.vercel.app` pra conferir antes):
   ```
   vercel
   ```
   Aceite as perguntas padrão (criar novo projeto, sem framework/build — é HTML puro).

4. Quando estiver aprovado, publique em produção:
   ```
   vercel --prod
   ```

5. (Opcional) Domínio próprio — depois que ela fechar e você tiver o domínio (ex. `drabarbarafaria.com.br`):
   ```
   vercel domains add drabarbarafaria.com.br
   ```
   e aponte o DNS conforme a Vercel indicar (normalmente um registro CNAME/A).

## O que já vem configurado

- `vercel.json`: URLs limpas e headers básicos de segurança (nosniff, X-Frame-Options, referrer policy).
- Nenhum framework, nenhuma variável de ambiente necessária — é uma página só, com fontes carregadas do Google Fonts e imagens embutidas em base64.

## Se quiser testar antes de instalar o CLI

Dá pra arrastar a pasta inteira em vercel.com/new (deploy manual pela interface, sem terminal) — funciona igual.
