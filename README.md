# 🧾 Painel de Comandas

Este é um projeto desenvolvido com **Next.js + TypeScript**, hospedado na **Vercel** e conectado a um servidor local Python que simula impressoras de produção via IP. O objetivo é receber e visualizar comandas de setores como cozinha, bar, pizzaria e sushi, enviadas automaticamente como impressão adicional pelo sistema TOTVS Chef.

---

## 🚀 Funcionalidades (em construção)

- Receber comandas via `POST /api/notificacao`
- Listar comandas em tempo real via `GET /api/notificacoes`
- Exibir painel de visualização em `/painel`
- Estrutura de código modular e escalável
- Preparado para futura persistência em banco (Firebase, Supabase, etc.)

---

## 🛠️ Como executar localmente

Clone o repositório e instale as dependências:

```bash
npm install
```

Inicie o servidor de desenvolvimento:

```bash
npm run dev
```

Abra [http://localhost:3000](http://localhost:3000) no navegador para visualizar a aplicação.

---

## 📂 Estrutura do projeto

```
pages/
├── api/
│   ├── hello.ts            # endpoint de teste padrão
│   ├── notificacao.ts      # (em breve) recebe as comandas
│   └── notificacoes.ts     # (em breve) retorna as comandas
├── index.tsx               # página inicial
├── painel.tsx              # (em breve) painel de visualização
public/
styles/
```

---

## 📋 Documentação de progresso

Todo o histórico e planejamento está registrado em:

📄 [`CHANGELOG.md`](./CHANGELOG.md)

---

## 📦 Tecnologias utilizadas

- [Next.js](https://nextjs.org/)
- [TypeScript](https://www.typescriptlang.org/)
- [Tailwind CSS](https://tailwindcss.com/)
- Hospedagem: [Vercel](https://vercel.com/)

---

## 📡 Integração com servidor Python

As impressoras de produção são simuladas com um script Python (`print_server.py`) que escuta portas IP e envia as comandas como `POST` para a rota `/api/notificacao`. A identificação do setor será feita via metadados ou prefixos nas mensagens.

---

## 📌 Próximos passos

- Criar rotas da API
- Conectar com o Python
- Criar painel `/painel`
- Adicionar autenticação opcional
- Migrar para banco de dados real

---

## 📤 Deploy

Este projeto é automaticamente publicado na Vercel ao fazer push para a branch `main`.
