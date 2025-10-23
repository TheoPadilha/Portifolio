# 🌙 Modo Escuro / Claro - Documentação

## ✨ Funcionalidade Implementada

Seu portfólio agora possui um **alternador de tema** completo que permite aos visitantes escolherem entre modo claro e escuro!

---

## 🎯 Como Funciona

### Botão de Alternância
- **Localização**: Navbar, ao lado do menu
- **Ícone**: Lua (tema claro) / Sol (tema escuro)
- **Efeito**: Rotação e escala ao hover

### Comportamento Inteligente

1. **Primeira Visita**:
   - Detecta a preferência do sistema operacional do usuário
   - Se o sistema estiver em modo escuro, aplica tema escuro automaticamente
   - Se estiver claro, mantém tema claro

2. **Visitas Seguintes**:
   - Lembra da preferência do usuário (salva no localStorage)
   - Aplica automaticamente o tema escolhido

3. **Alternância Manual**:
   - Clique no botão para alternar entre temas
   - Transição suave de 0.3s
   - Preferência salva automaticamente

---

## 🎨 Cores dos Temas

### Tema Claro (Padrão)
```css
- Primária: #6366f1 (Roxo/Azul)
- Secundária: #ec4899 (Rosa)
- Fundo Claro: #f8fafc
- Fundo Escuro: #0f172a
- Texto Escuro: #1e293b
- Texto Claro: #64748b
- Branco: #ffffff
```

### Tema Escuro
```css
- Primária: #818cf8 (Roxo claro)
- Secundária: #f472b6 (Rosa claro)
- Fundo Principal: #0f172a
- Fundo Cards: #1e293b
- Texto Principal: #f1f5f9
- Texto Secundário: #cbd5e1
- Cards: #0f172a
```

---

## 🔧 Arquivos Modificados

### 1. HTML ([index.html](index.html#L26-L28))
```html
<button class="theme-toggle" id="themeToggle">
    <i class="fas fa-moon"></i>
</button>
```

### 2. CSS ([style.css](style.css))
- Variáveis CSS para tema escuro (linhas 22-46)
- Estilo do botão de tema (linhas 124-157)
- Transições suaves (linhas 53-59)
- Responsividade do botão (linhas 1200-1208)

### 3. JavaScript ([script.js](script.js#L1-L38))
- Detecção de preferência do sistema
- Salvamento no localStorage
- Alternância de tema
- Atualização do ícone

---

## ⚙️ Funcionalidades Técnicas

### LocalStorage
```javascript
// Salva preferência
localStorage.setItem('theme', 'dark');

// Recupera preferência
const savedTheme = localStorage.getItem('theme');
```

### Detecção de Preferência do Sistema
```javascript
const systemPrefersDark = window.matchMedia('(prefers-color-scheme: dark)').matches;
```

### Aplicação do Tema
```javascript
htmlElement.setAttribute('data-theme', 'dark');
```

---

## 🎭 Efeitos Visuais

### Transições Suaves
- Todas as cores transitam em 0.3s
- Backgrounds, textos e bordas animados
- Sem "flash" ao mudar tema

### Animação do Botão
- Rotação de 15° ao hover
- Escala de 1.1x
- Troca de ícone (lua ↔️ sol)

### Responsividade
- Botão menor em mobile (40px)
- Posicionado adequadamente em todas as telas
- Funciona perfeitamente com menu hambúrguer

---

## 🌟 Benefícios para o Usuário

✅ **Conforto Visual**: Reduz cansaço em ambientes escuros
✅ **Economia de Bateria**: Modo escuro consome menos energia em telas OLED
✅ **Acessibilidade**: Respeita preferências do sistema
✅ **Personalização**: Usuário escolhe o que prefere
✅ **Persistência**: Lembra da escolha entre visitas

---

## 📱 Como Testar

1. **Abra o portfólio** no navegador
2. **Clique no botão** de lua/sol no navbar
3. **Observe**:
   - Transição suave de cores
   - Ícone muda (lua ↔️ sol)
   - Todas as seções adaptam as cores
4. **Recarregue a página**: O tema escolhido permanece
5. **Teste em mobile**: Botão funciona perfeitamente

---

## 🔍 Detalhes de Implementação

### Seletor CSS
```css
[data-theme="dark"] {
    /* Variáveis do tema escuro */
}
```

### Estrutura HTML
```html
<html data-theme="dark">
    <!-- Todo o conteúdo herda as variáveis -->
</html>
```

### Ordem de Prioridade
1. Preferência salva no localStorage
2. Preferência do sistema operacional
3. Tema claro (padrão)

---

## 🎨 Customização

### Mudar Cores do Tema Escuro
Edite as variáveis em `style.css` (linhas 23-32):

```css
[data-theme="dark"] {
    --primary-color: #SUA_COR_PRIMARIA;
    --secondary-color: #SUA_COR_SECUNDARIA;
    /* ... outras cores */
}
```

### Mudar Ícones
Edite em `script.js` (linhas 30-37):

```javascript
// Trocar fa-moon e fa-sun por outros ícones
themeIcon.classList.add('fa-SEU_ICONE');
```

### Desabilitar Detecção Automática
Remova em `script.js` (linhas 14-17):

```javascript
// Comentar ou remover estas linhas
// } else if (systemPrefersDark) {
//     htmlElement.setAttribute('data-theme', 'dark');
//     updateThemeIcon('dark');
// }
```

---

## 🚀 Melhorias Futuras (Opcional)

### Adicionar Mais Temas
- Tema automático (segue sistema)
- Tema sepia (tons amarelados)
- Tema alto contraste

### Animação de Transição
- Fade in/out mais elaborado
- Ripple effect ao clicar
- Partículas decorativas

### Preferências Avançadas
- Escolher cor principal
- Ajustar contraste
- Tamanho de fonte

---

## ✅ Status

- ✅ Botão implementado
- ✅ Temas claro e escuro funcionais
- ✅ LocalStorage configurado
- ✅ Detecção de preferência do sistema
- ✅ Transições suaves
- ✅ Responsivo
- ✅ Ícones dinâmicos
- ✅ Totalmente funcional!

---

## 🎯 Uso Recomendado

**Para Desenvolvedores**:
- Use durante o dia: Tema claro
- Use à noite: Tema escuro
- Apresentações: Tema conforme ambiente

**Para Visitantes**:
- Escolha automática na primeira visita
- Liberdade para alternar quando quiser
- Preferência salva automaticamente

---

**Aproveite seu novo tema escuro!** 🌙✨
