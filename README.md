# VISITAAE — Visitas por bairro e rua

Sistema responsivo para registrar visitas de campo por bairro e rua, com envio dos dados para o Google Sheets.

## Funcionalidades

- 15 bairros/áreas e 442 ruas/localidades cadastradas;
- seleção de 1ª ou 2ª visita;
- situação da visita e necessidade de retorno;
- candidatos para Deputado Estadual, Deputado Federal, Senador, Governador e Presidente;
- localização opcional;
- integração com Google Sheets por Google Apps Script;
- layout responsivo para computador e celular.

## Requisitos

- Node.js 22 ou superior;
- npm;
- Visual Studio Code ou outro editor.

## Abrir no Visual Studio Code

1. Extraia o arquivo ZIP.
2. Abra a pasta `visitaae-vscode-github` no Visual Studio Code.
3. Abra o terminal integrado.
4. Execute:

```bash
npm install
npm run dev
```

5. Abra `http://localhost:3000` no navegador.

## Onde editar

- Formulário, candidatos e integração: `app/page.tsx`
- Aparência e responsividade: `app/globals.css`
- Bairros e ruas: `app/data/territorios.json`
- Título e descrição: `app/layout.tsx`

## Google Sheets

No sistema, clique em **Configurar** ou **Conectar agora**. Copie o código exibido para o Google Apps Script, publique-o como Aplicativo da Web e cole no sistema o endereço terminado em `/exec`.

O endereço da implantação fica salvo somente no navegador utilizado. Ao trocar de domínio ou aparelho, conecte novamente.

## Publicar no GitHub

Crie um repositório vazio no GitHub e execute dentro da pasta do projeto:

```bash
git init
git add .
git commit -m "Publicar sistema VISITAAE"
git branch -M main
git remote add origin https://github.com/SEU_USUARIO/visitaae.git
git push -u origin main
```

Substitua `SEU_USUARIO` pelo seu usuário do GitHub.

## Publicar no Vercel pelo GitHub

1. Entre no Vercel.
2. Clique em **Add New → Project**.
3. Importe o repositório `visitaae` do GitHub.
4. Mantenha o framework **Next.js** e clique em **Deploy**.

Também é possível publicar pelo terminal:

```bash
npx vercel --prod
```

## Build de produção

```bash
npm run build
npm start
```
