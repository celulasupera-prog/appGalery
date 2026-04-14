# appGalery

## Como incluir mais opções de controle em um grupo

As opções do modal **Controles DP** ficam no objeto `links` dentro do `index.html`.

Cada grupo segue este formato:

```js
supera: {
  nome: 'Supera',
  controles: [
    { label: 'Folha', icon: '📄', href: 'https://...' }
  ]
}
```

### Para adicionar uma nova opção em um grupo existente

1. Abra o `index.html`.
2. Procure o bloco `const links = { ... }`.
3. Dentro do grupo desejado, adicione um novo item no array `controles`.

Exemplo (adicionando "Férias" no grupo `supera`):

```js
{ label: 'Férias', icon: '🏖️', href: 'https://seu-link-aqui' }
```

### Para criar um grupo novo

1. Adicione o novo grupo no objeto `links` com `nome` e `controles`.
2. Inclua um botão no passo 1 do modal chamando `selectGrupo('novoGrupo')`.

Exemplo de botão:

```html
<button class="modal-btn" onclick="selectGrupo('novoGrupo')">🏢 Novo Grupo</button>
```

> Dica: se você usar `href: '#'`, essa opção não aparece no modal (ela é filtrada automaticamente).
