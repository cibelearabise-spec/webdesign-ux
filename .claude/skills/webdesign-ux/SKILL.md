---
name: webdesign-ux
description: Use quando o usuário pedir criação, redesign, revisão ou crítica de sites, landing pages, apps web/mobile, dashboards ou interfaces em geral. Cobre pesquisa e fluxo de UX, arquitetura de informação, design visual (tipografia, cor, grid, componentes), acessibilidade, microcopy e entrega em HTML/CSS/JS.
---

# Web design e User Experience

## Quando usar
- Criar ou redesenhar página, site, app, dashboard ou fluxo de telas.
- Revisar uma interface existente (print, código ou descrição) e apontar problemas de usabilidade.
- Definir arquitetura de informação, jornada do usuário ou design system.
- Escrever microcopy (botões, erros, estados vazios, onboarding).

## Regras gerais
- Responda em português do Brasil.
- Entregue direto na conversa (código em blocos, listas e tabelas). Só gere arquivos ou artefatos se o usuário pedir.
- Evite perguntas. Se faltar contexto (público, objetivo, marca), assuma o padrão mais razoável, declare as suposições em até 3 linhas e siga.
- Stack padrão, salvo pedido diferente: HTML + CSS + JavaScript puro em arquivo único, mobile-first, sem dependências externas além de fontes.
- Toda decisão de design relevante deve ter uma justificativa curta ligada ao usuário ou ao objetivo, e não apenas ao gosto.

## Fluxo de trabalho

### 1. Entender (UX)
Registre em poucas linhas:
- **Usuário**: quem é, em que contexto usa (celular em pé, computador no trabalho etc.).
- **Objetivo principal**: a única ação que a tela precisa facilitar.
- **Tarefas-chave**: 3 a 5 coisas que o usuário precisa conseguir fazer.
- **Restrições**: marca, prazo, tecnologia, acessibilidade.

### 2. Estruturar
- Defina a arquitetura de informação: o que existe, como se agrupa, como se navega.
- Desenhe o fluxo em passos numerados (entrada → ação → confirmação → próximo passo).
- Mantenha no máximo 5 a 7 itens de navegação principal.
- Priorize conteúdo pela importância para a tarefa do usuário.

### 3. Desenhar (UI)
- **Hierarquia**: um ponto focal por tela; o que importa é maior, mais contrastado ou mais isolado.
- **Grid e espaçamento**: escala de 4/8 px; espaço em branco para agrupar (proximidade) em vez de caixas em excesso.
- **Tipografia**: no máximo 2 famílias; escala modular (ex.: 1.25); corpo de texto entre 16 e 18 px; linhas de 45 a 75 caracteres; altura de linha 1.5 para texto corrido.
- **Cor**: 1 cor de ação (primária), neutros em escala, cores semânticas (sucesso, alerta, erro). Cor nunca é o único sinal de um estado.
- **Componentes**: defina todos os estados (padrão, hover, foco, ativo, desabilitado, carregando, erro, vazio, sucesso).
- **Tokens**: declare cores, espaçamentos, raios e sombras como variáveis CSS (`:root`) e reutilize.

### 4. Acessibilidade (obrigatório)
- Contraste mínimo WCAG AA: 4,5:1 para texto normal, 3:1 para texto grande e componentes de interface.
- HTML semântico (`header`, `nav`, `main`, `button`, `label`), com um único `h1` e hierarquia de títulos sem saltos.
- Navegação completa por teclado, com foco visível (nunca remova `outline` sem substituto).
- Alvos de toque de pelo menos 44x44 px em mobile.
- Texto alternativo em imagens informativas; `aria-label` em botões só com ícone.
- Respeite `prefers-reduced-motion` e `prefers-color-scheme`.
- Formulários: rótulo sempre visível, mensagem de erro junto ao campo e dizendo como corrigir.

### 5. Microcopy
- Botões com verbo + objeto ("Agendar consulta", e não "Enviar").
- Erros: o que houve + como resolver, sem culpar o usuário.
- Estados vazios: explique o que a área faz e ofereça a primeira ação.
- Tom consistente com a marca; frases curtas.

### 6. Performance e responsividade
- Mobile-first, com breakpoints guiados pelo conteúdo e não por aparelhos.
- Unidades relativas (`rem`, `%`, `clamp()`); imagens com `max-width: 100%`.
- Evite bibliotecas pesadas quando CSS puro resolve; reserve espaço para imagens (evita salto de layout).

## Formato de entrega
**Para criar algo novo:**
1. Suposições e objetivo (até 3 linhas).
2. Estrutura da página/fluxo (lista curta).
3. Código completo e funcional (HTML/CSS/JS), com tokens no `:root`.
4. Decisões de UX em 3 a 5 tópicos, cada um com o porquê.
5. Próximos passos sugeridos (teste com usuários, medições).

**Para revisar algo existente:**
1. Resumo geral em 2 a 3 linhas.
2. Problemas em tabela: Problema | Onde | Severidade (alta/média/baixa) | Correção.
3. O que já está bom (para preservar).
4. As 3 mudanças de maior impacto, em ordem de prioridade.

Consulte o `REFERENCE.md` para heurísticas, escalas e checklists.

## Anti-padrões a evitar
- Visual genérico de template: gradiente roxo em fundo branco, cartões idênticos e sombras exageradas.
- Texto cinza-claro sobre fundo claro; placeholders no lugar de rótulos.
- Carrossel automático, modais em cascata e pop-ups logo na entrada.
- Vários botões primários competindo na mesma tela.
- Ícones sem rótulo em ações importantes.
- Animação decorativa que atrasa a tarefa.
- Inventar dados reais (preços, depoimentos, métricas): use marcadores claramente identificados como exemplo.

## Checklist final (confira antes de entregar)
- [ ] A ação principal é óbvia em 5 segundos?
- [ ] Contraste, foco visível e teclado funcionam?
- [ ] Todos os estados dos componentes foram tratados?
- [ ] Funciona em 360 px de largura e em tela grande?
- [ ] O texto está claro, curto e em português correto?
- [ ] Cada decisão relevante tem justificativa?
