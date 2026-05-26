# gerador-recibo

Modelo de recibo em **HTML + CSS** com campos editáveis direto na tela, salvamento automático no navegador e impressão/exportação em PDF otimizada para folha A4.

Tudo em um único arquivo ([index.html](index.html)) — sem dependências, sem build, sem servidor.

## Funcionalidades

- 📝 **Campos editáveis na tela** — clique em qualquer dado destacado (emitente, valor, pagador, data etc.) e digite por cima.
- 💾 **Salvamento automático** — o que você digita é guardado no navegador (`localStorage`) e recarregado na próxima vez que abrir a página.
- 🗑️ **Botão Limpar** — apaga os dados salvos e restaura o modelo padrão.
- 🖨️ **Impressão / PDF** — layout em A4 com `@page` e `@media print`; destaques de edição e botões somem na impressão.
- 🎨 **Tema personalizável** via variáveis CSS.

## Como usar

1. Abra o arquivo [index.html](index.html) no navegador (duplo clique).
2. Clique nos campos destacados e preencha os dados do recibo.
3. As alterações são salvas sozinhas — pode fechar e reabrir sem perder nada.
4. Clique em **🖨️ Imprimir / Salvar PDF** (ou `Ctrl + P`) e, em *Destino*, escolha **Salvar como PDF**.
5. Para começar um recibo do zero, clique em **🗑️ Limpar**.

## Personalização

As cores e a fonte ficam nas variáveis CSS no início do `<style>`, em `:root`:

| Variável            | Função                          |
| ------------------- | ------------------------------- |
| `--cor-destaque`    | Cor principal (título, bordas)  |
| `--cor-texto`       | Cor do texto                    |
| `--cor-secundaria`  | Cor de textos secundários       |
| `--cor-borda`       | Cor das linhas/campos           |
| `--cor-fundo-suave` | Fundo da caixa de valor         |
| `--fonte`           | Família tipográfica             |

Para adicionar ou remover campos editáveis, basta marcar (ou desmarcar) o elemento com `contenteditable="true"` — o JavaScript detecta automaticamente todos os campos com esse atributo e cuida do salvamento.

## Observações

- Os dados ficam salvos **apenas no navegador e no computador** onde foram digitados (`localStorage`). Não há sincronização entre dispositivos.
- Limpar o histórico/dados de navegação do navegador também apaga os dados salvos do recibo.

## Tecnologias

HTML5 · CSS3 · JavaScript (vanilla) — nenhuma biblioteca externa.
