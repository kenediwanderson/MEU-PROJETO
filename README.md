# MEU-PROJETO


### 🚀 Estrutura do Repositório GitHub

├── src/                   # Código-fonte (HTML, CSS, JS, imagens)
├── docs/                  # Documentação adicional (opcional)
├── dist/                  # Versão otimizada para produção
├── .gitignore
├── package.json           # (se usar Node.js)
├── README.md              # Documentação principal (entregável obrigatório)
└── LICENSE                # Licença (opcional, mas recomendado)
```

---

### 🔀 1. Controle de Versão (Git/GitHub)

#### ✅ Estratégia de Branching — GitFlow

Use o seguinte fluxo:

* `main` → branch de produção (somente releases estáveis)
* `develop` → branch de desenvolvimento
* `feature/*` → novas funcionalidades
* `hotfix/*` → correções emergenciais na produção
* `release/*` → preparação de versões estáveis

**Exemplo de fluxo de trabalho:**

```bash
git checkout develop
git checkout -b feature/acessibilidade
# Implementa a feature
git add .
git commit -m "feat(acessibilidade): adiciona suporte total a leitores de tela"
git push origin feature/acessibilidade
# Cria Pull Request -> merge -> develop
```

#### ✅ Commits Semânticos

Padrão recomendado (Conventional Commits):

| Tipo        | Uso                                          |
| ----------- | -------------------------------------------- |
| `feat:`     | Nova funcionalidade                          |
| `fix:`      | Correção de bug                              |
| `docs:`     | Documentação                                 |
| `style:`    | Ajustes de formatação, sem impacto funcional |
| `refactor:` | Melhoria de código sem mudar comportamento   |
| `perf:`     | Melhoria de performance                      |
| `test:`     | Testes adicionados ou ajustados              |
| `chore:`    | Tarefas de build, dependências, etc.         |

Exemplo:

```
feat(ui): adiciona modo escuro acessível
fix(a11y): corrige contraste insuficiente no menu principal
```

#### ✅ Releases e Versionamento Semântico

Use o formato `vMAJOR.MINOR.PATCH` — por exemplo:

* `v1.0.0` → primeira versão estável
* `v1.1.0` → nova funcionalidade adicionada
* `v1.1.1` → correção de bug

---

### ♿ 2. Acessibilidade (WCAG 2.1 Nível AA)

Checklist essencial:

* [ ] **Navegação por teclado**: todos os botões, links e formulários são acessíveis via `Tab` e `Enter`.
* [ ] **Estrutura semântica**: uso correto de `<header>`, `<main>`, `<section>`, `<footer>`, `<nav>`, etc.
* [ ] **Contraste mínimo 4.5:1**: teste com [WebAIM Contrast Checker](https://webaim.org/resources/contrastchecker/).
* [ ] **Leitores de tela**: adicionar `aria-label`, `role`, `alt` em imagens.
* [ ] **Modo escuro e alto contraste**: CSS custom properties (`--bg-color`, `--text-color`) e `prefers-color-scheme`.

---

### ⚙️ 3. Otimização para Produção

* [ ] **Minificação**: use ferramentas como:

  * `html-minifier` (HTML)
  * `cssnano` (CSS)
  * `terser` (JavaScript)
* [ ] **Compressão de imagens**:

  * Use `imagemin`, `tinypng.com` ou `squoosh.app`
* [ ] **Geração da pasta `/dist`** com todos os arquivos otimizados
