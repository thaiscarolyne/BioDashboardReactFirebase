# 📊 Dashboard de Bioimpedância Familiar

Este projeto é um dashboard interativo para monitoramento de bioimpedância, focado no acompanhamento da evolução de massa muscular, peso e gordura corporal de membros da família. Desenvolvido com React e Firebase, ele permite uma visualização clara do progresso físico ao longo do tempo.

<img width="1118" height="816" alt="image" src="https://github.com/user-attachments/assets/91554e7a-2aca-4971-99ea-f72d8333718b" />

## ✨ Funcionalidades

* Gestão de Membros: Registro individual para acompanhamento personalizado.

* Histórico Dinâmico: Registro, edição e exclusão de medições de peso, % de gordura e % de músculo.

* Gráficos de Evolução: Visualização detalhada utilizando eixos duplos (Peso vs. Componentes em kg) com filtro de período (Último ano ou Todo o histórico).

* Segurança de Dados: Separação de credenciais sensíveis via firebase-config.js.

* Backup e Restauração: Opções para salvar e importar dados localmente em formato JSON.

## 🚀 Tecnologias Utilizadas

Frontend: React (via CDN) e Chart.js.

Backend: Firebase Firestore (Banco de dados NoSQL).

Segurança: Variáveis de configuração isoladas e regras de acesso Firestore.

## 🛠️ Configuração Local

Para rodar este projeto ou subir no seu GitHub com segurança:

Clone o repositório:

git clone https://github.com/seu-usuario/dashboard-bioimpedancia.git

Configure as credenciais: Crie um arquivo chamado firebase-config.js dentro da pasta public do projeto:

```json
const firebaseConfig = {
  apiKey: "SUA_API_KEY",
  authDomain: "seu-projeto.firebaseapp.com",
  projectId: "seu-projeto-id",
  storageBucket: "seu-projeto.appspot.com",
  messagingSenderId: "123456789",
  appId: "1:123456789:web:abc123def"
};
window.firebaseConfig = firebaseConfig;
```


Segurança do Git: Certifique-se de que o seu .gitignore contenha as seguintes linhas para não expor seus dados:

firebase-config.js
backup_bio_*.json

## ☁️ Deploy no Firebase
Para colocar o site no ar (online) usando o Firebase Hosting:

### 1. Preparação no Console do Firebase
Crie um projeto no Firebase Console.

Crie um banco de dados Firestore e configure as regras de segurança para permitir leitura/escrita.

Ative o Hosting no menu lateral.

### 2. Instalação e Inicialização
No seu terminal, dentro da pasta do projeto:


##### Instale as ferramentas do Firebase (caso não tenha)
`
npm install -g firebase-tools
`

#### Faça login na sua conta Google
`
firebase login
`

#### Inicialize o projeto
`
firebase init
`

  * Hosting: Selecione esta opção.
  * Public Directory: Digite public (ou a pasta onde está seu index.html).
  * Single-page app: Selecione No (pois é um HTML simples).
  * GitHub Action: Selecione No (a menos que queira automatizar o deploy).

### 3. Publicação
Sempre que fizer uma alteração e quiser atualizar o site online:

`
firebase deploy
` 
