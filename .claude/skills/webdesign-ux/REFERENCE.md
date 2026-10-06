# Referência rápida: webdesign-ux

## 10 heurísticas de usabilidade (Nielsen)
1. Visibilidade do status do sistema
2. Correspondência entre o sistema e o mundo real
3. Controle e liberdade do usuário (desfazer, voltar, cancelar)
4. Consistência e padrões
5. Prevenção de erros
6. Reconhecimento em vez de memorização
7. Flexibilidade e eficiência de uso (atalhos para experientes)
8. Design estético e minimalista
9. Ajudar a reconhecer, diagnosticar e corrigir erros
10. Ajuda e documentação

## Severidade de problemas
| Nível | Critério |
|---|---|
| Alta | Impede concluir a tarefa ou causa perda de dados |
| Média | Atrapalha, mas o usuário consegue concluir |
| Baixa | Incômodo estético ou de eficiência |

## Tokens iniciais (CSS)
```css
:root {
  /* Cores */
  --cor-primaria: #1d4ed8;
  --cor-primaria-hover: #1e40af;
  --cor-texto: #111827;
  --cor-texto-suave: #4b5563;
  --cor-fundo: #ffffff;
  --cor-superficie: #f3f4f6;
  --cor-borda: #d1d5db;
  --cor-sucesso: #15803d;
  --cor-alerta: #b45309;
  --cor-erro: #b91c1c;

  /* Espaçamento (base 4 px) */
  --esp-1: 4px;  --esp-2: 8px;  --esp-3: 12px;
  --esp-4: 16px; --esp-6: 24px; --esp-8: 32px; --esp-12: 48px;

  /* Tipografia (escala 1.25) */
  --fonte: system-ui, -apple-system, "Segoe UI", Roboto, sans-serif;
  --txt-sm: 0.875rem; --txt-base: 1rem; --txt-lg: 1.25rem;
  --txt-xl: 1.563rem; --txt-2xl: 1.953rem; --txt-3xl: 2.441rem;

  /* Forma */
  --raio: 8px;
  --sombra: 0 1px 3px rgba(0, 0, 0, 0.12);
}

@media (prefers-color-scheme: dark) {
  :root {
    --cor-texto: #f3f4f6;
    --cor-texto-suave: #9ca3af;
    --cor-fundo: #0f172a;
    --cor-superficie: #1e293b;
    --cor-borda: #334155;
  }
}

:focus-visible { outline: 3px solid var(--cor-primaria); outline-offset: 2px; }

@media (prefers-reduced-motion: reduce) {
  * { animation: none !important; transition: none !important; }
}
```

## Estrutura de landing page (padrão)
1. Cabeçalho com marca e uma ação
2. Hero: promessa clara + ação principal + prova visual
3. Problema ou benefícios (3 itens)
4. Como funciona (3 passos)
5. Prova social (depoimentos, números reais fornecidos pelo usuário)
6. Perguntas frequentes
7. Chamada final para ação + rodapé

## Estrutura de formulário
- Peça só o necessário; um campo por linha em mobile.
- Rótulo acima do campo; tipo de input correto (`email`, `tel`, `inputmode`).
- Validação ao sair do campo e mensagem específica.
- Botão de envio com verbo claro e estado de carregamento.
- Confirmação visível do resultado e do próximo passo.

## Modelo de crítica de interface
```
Resumo: ...
| Problema | Onde | Severidade | Correção |
|---|---|---|---|
| ... | ... | Alta | ... |
Pontos fortes: ...
Top 3 prioridades: 1) ... 2) ... 3) ...
```

## Teste rápido com usuários (5 pessoas)
1. Defina uma tarefa realista ("encontre e agende uma consulta").
2. Peça para pensar em voz alta; não ajude.
3. Anote onde hesitam, erram ou desistem.
4. Agrupe os problemas por frequência e severidade; corrija os mais graves primeiro.
