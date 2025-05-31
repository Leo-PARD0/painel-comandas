## 🧾 CHANGELOG – Painel de Comandas

### 📌 Etapa 0 – Contexto do projeto

- Objetivo: Criar um painel web para capturar e visualizar comandas enviadas via impressão IP (como impressora adicional do TOTVS Chef).
- Infraestrutura:
  - Servidor local com Python (`print_server.py`) escutando impressões via portas IP
  - Servidor web (frontend + backend) hospedado na Vercel via GitHub

---

### 📌 Etapa 1 – Preparação do ambiente local

- [x] Criado repositório no GitHub chamado `painel-comandas`
- [x] Definida a descrição comercial do projeto no repositório
- [x] Decidido não incluir licença (projeto de uso interno)
- [x] Instalado o **Git** via site oficial
- [x] Instalado o **Node.js LTS** via `winget`:
  ```bash
  winget install OpenJS.NodeJS.LTS
  ```
- [x] Verificado funcionamento:
  ```bash
  node -v  → v22.16.0  
  npx -v   → 10.9.2
  ```
- [x] Corrigido erro de execução de scripts no PowerShell com:
  ```powershell
  Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
  ```

---

### 📌 Etapa 2 – Preparação do projeto web

- [x] Clonado o repositório localmente:
  ```bash
  git clone https://github.com/Leo-PARD0/painel-comandas.git
  cd painel-comandas
  ```
- [x] Iniciado o projeto com Next.js + TypeScript:
  ```bash
  npx create-next-app@latest . --typescript
  ```
  Respostas esperadas no prompt:
  - TypeScript: ✅ Yes  
  - ESLint: ✅ Yes  
  - Tailwind CSS: ✅ Yes (opcional)  
  - `src/` folder: ❌ No  
  - App Router: ❌ No (usamos Pages Router)

---

### 📌 Etapa 3 – Primeiros endpoints e painel

- [x] Commitado o projeto base:
  ```bash
  git add .
  git commit -m "Inicia projeto com Next.js, TypeScript e .gitignore completo"
  git push origin main
  ```
- [x] Commitado o projeto com adição:
```changelog.md```
- [ ] Criar rota `POST /api/notificacao` para receber comandas do print_server.py  
- [ ] Criar rota `GET /api/notificacoes` para listar comandas no painel  
- [ ] Criar página `/painel.tsx` para exibição das comandas no navegador  
- [ ] Conectar o painel com o script Python que simula a impressora IP  
- [ ] (Futuro) Migrar de `JSON` local para banco de dados externo (Firebase, Supabase, PlanetScale etc.)
