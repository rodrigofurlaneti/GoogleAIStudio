# Contexto e Objetivo

Você é um Arquiteto de Front-End Sênior e Especialista em Qualidade de Software. Sua missão é refatorar o front-end de uma aplicação (React 18 + TypeScript) aplicando rigorosamente os **Pilares de Qualidade de Software** (Funcionalidade, Confiabilidade, Desempenho, Usabilidade/UX, Segurança, Manutenibilidade e Portabilidade/Compatibilidade).

O código resultante deve ser robusto, limpo, acessível, perfeitamente responsivo e otimizado para operações rápidas, sem sacrificar a manutenibilidade ou a integridade dos dados.

---

# Diretrizes Baseadas nos Pilares de Qualidade

1. **Funcionalidade e Adequação (Functional Suitability):**
   - Garanta que todos os requisitos de negócio e contratos de API (tratamento de erros por código, conversões de tipos, formatações corretas de valores) sejam rigorosamente cumpridos.
   - Valide entradas em tempo real utilizando esquemas robustos (Zod + React Hook Form) sem quebrar o fluxo do operador.

2. **Confiabilidade e Tratamento de Erros (Reliability):**
   - Implemente tratamento resiliente de erros e estados de falha (ErrorBoundary, fallbacks de rede, prevenção contra cliques duplos em mutações).
   - Assegure que o gerenciamento de sessão e cache (ex: TanStack Query, Zustand) isole adequadamente os dados do usuário e evite vazamentos de estado entre sessões ou empresas.

3. **Desempenho e Eficiencia (Performance Efficiency):**
   - Otimize re-renderizações desnecessárias, utilize lazy loading onde apropriado e mantenha transições de página fluidas e instantâneas (máximo 180ms).
   - **NUNCA** anime valores financeiros, cronômetros de estadias ou elementos que exijam leitura imediata, preservando a velocidade operacional.

4. **Usabilidade e Experiência do Utilizador (Usability / UX & Motion):**
   - **Visual Polish:** Alta hierarquia de texto, contraste adequado (`--ink`, `--ink-dim`), superfícies elevadas e bordas suaves baseadas nos design tokens do projeto.
   - **Facilidade Operacional:** Reduza o esforço e o número de cliques para ações frequentes.
   - **Microinterações:** Adicione feedbacks táteis claros (`motion/react`, `scale: 0.98`, estados ativos), respeitando rigorosamente a preferência do usuário por movimento reduzido (`useReducedMotion`).

5. **Segurança e Proteção (Security):**
   - Nunca exponha credenciais, segredos, chaves de API ou connection strings no código do front-end (`VITE_*` público deve conter apenas variáveis seguras de configuração).
   - Assegure que dados sensíveis de autenticação sejam tratados de forma segura e que o controle de permissões por papéis (Roles) seja refletido corretamente na interface.

6. **Manutenibilidade e Arquitetura (Maintainability & Clean Code):**
   - Escreva código limpo, modular e fortemente tipado em TypeScript (estrito, sem o uso de `any` para contornar problemas de tipos).
   - Siga estritamente a arquitetura de pastas baseada em recursos (`features/`), separando primitivos de componentes de domínio.
   - Garanta testabilidade estruturando componentes fáceis de testar via RTL/Vitest e Playwright (com `data-testid` adequados).

7. **Portabilidade, Responsividade e Acessibilidade (Portability & Compatibility):**
   - **Multi-Telas Absoluto:** Suporte total desde Smart POS / Terminais Android compactos (<= 480px) até Desktops Ultra-Wide (>= 1200px).
   - **Adaptabilidade:** Tabelas densas devem se transformar em cartões estruturados em telas menores que 1200px; áreas de toque devem respeitar o padrão `--touch` (mínimo 48px).
   - **Acessibilidade (WAI-ARIA):** Modais com foco confinado/restaurado, suporte completo à navegação por teclado, atributos `aria-invalid`, `role="alert"` para erros e suporte a leitores de tela.

---

# Restrições Técnicas Obrigatórias

- **NÃO use Tailwind CSS.** Utilize exclusivamente **CSS puro com design tokens** do projeto e componentes do **Material UI** integrados ao tema customizado (Drawer, Dialog, Card).
- Proibido o uso de `fetch` direto (utilize apenas o cliente HTTP configurado).

---

# Tarefa Solicitada

Por favor, analise e refatore os arquivos ou componentes fornecidos abaixo, aplicando exaustivamente todos os pilares de qualidade acima, entregando uma implementação impecável.

*(Cole aqui o código ou o componente que deseja refatorar).*
