## Sumário
- [Sumário](#sumário)
- [Configurações Iniciais](#configurações-iniciais)
- [Dia 02 - Configuração Inicial](#dia-02---configuração-inicial)
  - [Instalação do Next, React e DOM](#instalação-do-next-react-e-dom)
- [Dia 10 - Configuração do Prettier](#dia-10---configuração-do-prettier)
- [Dia 15 - Configuração de Testes](#dia-15---configuração-de-testes)

---

## Configurações Iniciais

**Obs:** Caso clone o repositório do Github, ele virá sem a pasta `node_modules`. 

Para instalá-la, basta digitar no terminal:
  ```sh
    npm install
  ```

## Dia 02 - Configuração Inicial

🛠️ **NVM** Node Version Manager
- Para mostrar operações possíveis do Node:
  ```sh
    nvm --help
  ```
- Para listar todas as versões atuais disponíveis:
  ```sh
    nvm ls
  ```
- Para instalar uma versão específica do Node:
  ```sh
    nvm install <version>
  ```

Para definir uma versão específica como padrão, crie um arquivo chamado `.nvmrc` na raiz do projeto.

Obs. **Sempre deixe uma linha em branco ao final do arquivo**.


### Instalação do Next, React e DOM

Crie um manifesto (`package.json`)
  ```sh
    npm install next@13.1.6 react@18.2.0 react-dom@18.2.0
  ```

Ao final do arquivo `package.json` deverá conter as dependências corretamente listadas.

Para iniciar o servidor, adicione ao `package.json` dentro de `scripts`:
  ```sh
    "dev": "next dev"
  ```

E no terminal, digite:
  ```sh
    npm run dev
  ```

**Obs:** Essa ação apresentará um erro porque não há uma pasta onde o Next pode encontrar os recursos para renderizar uma página.
Para corrigir, crie uma pasta chamada de `pages`e dentro dela um aquivo `index.js`(opcional) para teste.

Agora, ao iniciar o servidor, ele deverá funcionar corretamente e criar a pasta `.next` automaticamente na raiz do projeto.

O Next, por padrão, roda na porta `3000`.

---

## Dia 10 - Configuração do Prettier
Instalação do Prettier como dependência de desenvolvimento
  ```sh
    npm install --save-dev prettier
  ```

  - Adicione ao `package.json`:
    ```sh
      "lint:check": "prettier --check ."
    ```

  - Para verificar a formatação:
    ```sh
      npm run lint:check
    ```

  - Para habilitar a correção automática, adicione:
      ```sh
        "lint:fix": "prettier --write ."
      ```

  - Para executar as correções:
    ```sh
      npm run lint:fix
    ```


---

## Dia 15 - Configuração de Testes
Instalação do Jest (Versão 29.6.2) para testes automatizados.
  ```sh
    npm install --save-dev jest@29.6.2
  ```

  - No `package.json`, adicione aos `scripts`:
    ```sh
      "test": "jest"
    ```
  
  - Para executar os testes:
    ```sh
      npm run test
    ```

  **Obs:** Caso não haja nenhum teste criado, um erro será exibido.

Para manter o Jest rodando e testando automaticamente, adicione aos `scripts`:
```sh
  "test:watch": "jest --watch"
```

- Para executar os testes:
  ```
    npm run test:watch
  ```

--- 