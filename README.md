# 🧱 Depósito Realizar - Material de Construção

<p align="center">
  <img src="IMG-20261016-WA0010.jpg" width="400" alt="Logo Depósito Realizar">
</p>

Sistema de recibos para impressora térmica **58mm PRC2** - Igarapé/MG.

📍 Av. Geraldo 341, Igarapé - MG | 📞 31 99652-2639

### O que é este projeto?

PDV simples que imprime recibos não-fiscais direto na impressora térmica via `localhost:26543/ser`.

### 🖨️ Como funciona

- Imprime em bobina 58mm (48mm útil)
- Logo em preto puro, sem fundo azul (não borra)
- Não corta o TOTAL - usa flexbox

### 📁 Arquivos

- `index.html` - Template do recibo
- `IMG-20261016-...` - Logo térmica correta (versão grande)

### 🚀 Como usar

1. Abra o `index.html`
2. A logo já está configurada para `44mm` para ocupar toda a bobina
3. Para imprimir:
```js
fetch('http://localhost:26543/ser', {
  method: 'POST',
  body: document.getElementById('recibo').innerHTML
})
