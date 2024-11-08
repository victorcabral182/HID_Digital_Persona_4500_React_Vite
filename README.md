# HID_Digital_Persona_4500_React_Vite

I've gathered some information to make the HID Digital Persona 4500 FingerPrint Reader work in the browser using the WebSdk provided by the manufacturer, React, and Vite.JS (v4.4.9).

## Useful Links

- [Manufacturer's Tutorial](https://hidglobal.github.io/digitalpersona-devices/tutorial.html) - Here you will find a step-by-step guide from the manufacturer.
- [WebSdk on GitHub](https://github.com/hidglobal/digitalpersona-sample-angularjs/tree/master/src/modules/WebSdk) - You need to download two files: `index.d.ts` and `index.js`.
- [Lite Client Agents](https://crossmatch.hid.gl/lite-client/) - Here you will find the lite client agents provided by the manufacturer.

---

## Step by Step

### Step One
Install the `@digitalpersona/devices` package using npm or yarn:

```bash
npm install @digitalpersona/devices
```
```bash
yarn add @digitalpersona/devices
```

### Step Two
Install the lite client agent provided by the manufacturer from link 3 in the useful links section.

### Step Three
Create a folder at the root of your project and place the files downloaded from link 2 in the useful links section.
![image](https://github.com/user-attachments/assets/b16817a2-804a-4935-ba9b-2599aa476663)

### Step Four
Add a <script> tag at the end of the <body> of your index.html (root), pointing to the index.js file in the /modules/websdk folder:
<script src="/modules/websdk/index.js"></script>
![image](https://github.com/user-attachments/assets/f75f2fb3-dd51-409d-917f-9dab17f3e742)

### Step Five
If you encounter an error like this:<br>
./node_modules/@digitalpersona/devices/dist/es6/devices/websdk/channel.js:3:0-16 - Error: Module not found: Error: Can't resolve 'WebSdk' in '...\node_modules@digitalpersona\devices\dist\es6\devices\websdk'<br>

The solution is to add the following code to your vite.config.ts file:
```bash
resolve: {
  alias: {
    WebSdk: './modules/WebSdk/index.js',
  },
},
```
![image](https://github.com/user-attachments/assets/e5bd15ba-d5f3-4859-baaa-89467f4bb5f4)

### Step Six
Download the component created by @omarasael1980 and adapt it to meet your needs.

I hope this information is helpful and that you can successfully integrate the fingerprint reader into your project!

### Acknowledgments
@omarasael1980  
@a-bronx

# PT_BR Version

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
