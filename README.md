# Jogo da Memória • Memory Game (React + TypeScript)

Este repositório contém um jogo da memória simples construído com React 18, TypeScript e styled-components. O projeto foi criado com Create React App (CRA) e inclui utilitários de testes do Testing Library.

This repository contains a simple Memory Game built with React 18, TypeScript, and styled-components. The project was scaffolded with Create React App (CRA) and includes Testing Library utilities.

---

## 🇧🇷 Seção em Português

### Visão Geral
Um jogo da memória onde o objetivo é encontrar os pares de cartas idênticas. O tabuleiro é preenchido com ícones SVG e a cada jogada o contador de movimentos é atualizado. O temporizador conta apenas enquanto uma partida está ativa e pode ser reiniciado a qualquer momento.

### Funcionalidades
- React 18 + TypeScript
- Estilização com styled-components
- Ícones SVG locais para as cartas
- Grid responsivo (4 colunas; em telas pequenas, 3 colunas)
- Controles do jogo: tempo decorrido, número de movimentos e botão Reiniciar
- Lógica do jogo com hooks (useState, useEffect)
- Base com Create React App (react-scripts)

### Pré-requisitos
- Node.js 16+ (recomendado 16 ou 18)
- npm (ou yarn, se preferir)

### Instalação e Execução
1. Instale as dependências
```
npm install
```
2. Inicie o servidor de desenvolvimento
```
npm start
```
3. Acesse em http://localhost:3000

### Scripts Disponíveis
- Iniciar em desenvolvimento: `npm start`
- Rodar testes: `npm test`
- Gerar build de produção: `npm run build`
- Ejetar configurações do CRA: `npm run eject` (irreversível)

### Como Jogar
1. Clique em duas cartas para revelá-las.
2. Se forem iguais, permanecem viradas (marcadas como permanentes). Se forem diferentes, voltam a ficar escondidas após 1 segundo.
3. O contador de movimentos incrementa a cada tentativa (par de cliques) e o relógio conta enquanto a partida está ativa.
4. Use o botão “Reiniciar” para começar uma nova partida.

### Estrutura do Projeto (resumo)
```
src/
  App.tsx               # Lógica principal do jogo e estados
  App.styles.ts         # Estilos base e layout responsivo
  components/
    Button/             # Botão com ícone opcional
    GridItem/           # Carta do tabuleiro (comportamento e visual)
    InfoItem/           # Exibe pares label/valor (Tempo, Movimentos)
  data/
    items.ts            # Lista de ícones (pares) usados no jogo
  types/
    GridItemType.ts     # Tipagem do item de grade
  utils/
    formatTimeElapsed.ts# Utilitário de formatação mm:ss
```

### Personalização
- Adicionar novos ícones: coloque SVGs em `src/svgs/` e registre-os em `src/data/items.ts`. O grid é preenchido com `items.length * 2` cartas automaticamente.
- Estilos/Responsividade: ajuste em `src/App.styles.ts` (por exemplo, número de colunas do grid).
- Textos/Idioma: labels como “Tempo”, “Movimentos” e “Reiniciar” podem ser alterados em `src/App.tsx` e componentes relacionados.

### Testes
O projeto está preparado com Testing Library (jest-dom, @testing-library/react, user-event). Para executar:
```
npm test
```
Caso não existam testes adicionais criados, o comando abrirá o runner padrão do CRA.

### Stack Técnica
- React 18
- TypeScript 4
- styled-components 5
- Create React App (react-scripts 5)
- Testing Library (jest-dom, @testing-library/react, user-event)

### Licença
Nenhuma licença específica foi definida neste repositório. Caso deseje, adicione um arquivo `LICENSE` (por exemplo, MIT) e ajuste esta seção.

---

## 🇺🇸 English Section

### Overview
A memory matching game where the goal is to find pairs of identical cards. The board is populated with local SVG icons. Each attempt increases the move counter. The timer runs only while a game is active and can be reset at any time.

### Features
- React 18 + TypeScript
- Styling with styled-components
- Local SVG icons for the cards
- Responsive grid (4 columns; 3 columns on small screens)
- Game controls: elapsed time, move counter, and Reset button
- Game logic implemented with React hooks (useState, useEffect)
- Scaffolded with Create React App (react-scripts)

### Prerequisites
- Node.js 16+ (16 or 18 recommended)
- npm (or yarn if you prefer)

### Installation & Run
1. Install dependencies
```
npm install
```
2. Start the development server
```
npm start
```
3. Open http://localhost:3000

### Available Scripts
- Start dev server: `npm start`
- Run tests: `npm test`
- Build for production: `npm run build`
- Eject CRA config: `npm run eject` (irreversible)

### How to Play
1. Click two cards to reveal them.
2. If they match, they stay revealed (marked as permanent). If not, they will hide again after 1 second.
3. The move counter increases after each pair attempt, and the timer runs while the game is active.
4. Use the “Reiniciar/Reset” button to start a new game.

### Project Structure (summary)
```
src/
  App.tsx               # Main game logic and state
  App.styles.ts         # Base styles and responsive layout
  components/
    Button/             # Button with optional icon
    GridItem/           # Board card (behavior and visuals)
    InfoItem/           # Displays label/value pairs (Time, Moves)
  data/
    items.ts            # Icon (pair) list used by the game
  types/
    GridItemType.ts     # Grid item type definition
  utils/
    formatTimeElapsed.ts# mm:ss formatting utility
```

### Customization
- Add new icons: place SVGs in `src/svgs/` and register them in `src/data/items.ts`. The grid automatically uses `items.length * 2` cards.
- Styles/Responsiveness: adjust `src/App.styles.ts` (e.g., number of grid columns).
- Text/Language: labels like “Tempo/Time”, “Movimentos/Moves”, and “Reiniciar/Reset” can be changed in `src/App.tsx` and related components.

### Testing
The project is configured with Testing Library (jest-dom, @testing-library/react, user-event). To run:
```
npm test
```
If there are no additional tests yet, CRA’s default test runner will open.

### Tech Stack
- React 18
- TypeScript 4
- styled-components 5
- Create React App (react-scripts 5)
- Testing Library (jest-dom, @testing-library/react, user-event)

### License
No specific license is defined in this repository. If desired, add a `LICENSE` file (e.g., MIT) and update this section accordingly.

---

Se precisar, posso adicionar uma captura de tela (screenshot) e instruções de implantação (por exemplo, GitHub Pages). If you want, I can also include a screenshot and deployment instructions (e.g., GitHub Pages).