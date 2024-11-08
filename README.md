# HID_Digital_Persona_4500_React_Vite

Reuni algumas informações para fazer o HID Digital Persona 4500 FingerPrint Reader funcionar no navegador utilizando a WebSdk fornecida pela própria fabricante, React e Vite.JS (v4.4.9).

## Links Úteis

- [Tutorial da fabricante](https://hidglobal.github.io/digitalpersona-devices/tutorial.html) - Aqui você vai encontrar o passo a passo pela própria fabricante.
- [WebSdk no GitHub](https://github.com/hidglobal/digitalpersona-sample-angularjs/tree/master/src/modules/WebSdk) - Você deverá baixar os dois arquivos: `index.d.ts` e `index.js`.
- [Lite Client Agents](https://crossmatch.hid.gl/lite-client/) - Aqui você encontrará os lite client agents fornecidos pela fabricante.

---

## Passo a Passo

### Primeiro Passo
Instale o pacote `@digitalpersona/devices` usando npm ou yarn:

```bash
npm install @digitalpersona/devices
```
```bash
yarn add @digitalpersona/devices
```

### Segundo Passo
Instale o lite client agent fornecido pela fabricante no link 3 da seção de links úteis.

### Terceiro Passo
Crie uma pasta na raiz do seu projeto e insira os arquivos baixados do link 2 da seção de links úteis.
![image](https://github.com/user-attachments/assets/b16817a2-804a-4935-ba9b-2599aa476663)

### Quarto Passo
Adicione uma tag <script> no final do <body> do seu index.html (root), apontando para o arquivo index.js na pasta /modules/websdk:
<script src="/modules/websdk/index.js"></script>
![image](https://github.com/user-attachments/assets/f75f2fb3-dd51-409d-917f-9dab17f3e742)

### Quinto Passo
Se você enfrentar um erro como este:<br>
./node_modules/@digitalpersona/devices/dist/es6/devices/websdk/channel.js:3:0-16 - Error: Module not found: Error: Can't resolve 'WebSdk' in '...\node_modules@digitalpersona\devices\dist\es6\devices\websdk'<br>

A solução é adicionar o seguinte código ao seu arquivo vite.config.ts:
```bash
resolve: {
  alias: {
    WebSdk: './modules/WebSdk/index.js',
  },
},
```
![image](https://github.com/user-attachments/assets/e5bd15ba-d5f3-4859-baaa-89467f4bb5f4)

### Sexto Passo
Faça o download do componente criado por @omarasael1980 e adapte-o para atender às suas necessidades.

Espero que essas informações sejam úteis e que você consiga integrar o leitor de digitais com sucesso no seu projeto!

### Agradecimentos
@omarasael1980
@a-bronx
