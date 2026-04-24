<h1 align="center">ConnectionGames</h1>
<p align="center">
  <strong>
    A collection of connection-based puzzle games built with Vue 3.
  </strong>
</p>

<br>

# Table of Contents
* [Overview :sparkles:](#overview-sparkles)
  * [About](#about)
  * [Features](#features)
  * [Technologies](#technologies)
* [Details :scroll:](#details-scroll)
  * [ UI and application flow](#ui-and-application-flow)
  * [Technical challenges](#technical-challenges)

<br>

# Overview :sparkles:

## About
ConnectionGames is a small suite of puzzle games focused on recreating the correct connections between objects on a board.
I built this project for fun to implement some logic games I like, to showcase my frontend skills and to try out Vue 3.

Check out the [live version](https://pasek108.github.io/ConnectionGames/).

<br>

![preview](/_for_readme/preview.png)

## Features
### Game Modes
*Every game mode features **3 difficulty levels**, scaling the logic and grid complexity to challenge players of all skill levels.*

* **Bridges:** A web version of the classic *Hashiwokakero* puzzle. Connect all the islands together with horizontal and vertical bridges. You have to follow the allowed bridge counts for each island, and paths cannot cross.
* **Squares:** Move and rotate blocks until every piece on the grid is correctly connected to its neighbors.
* **Pipes:** A variation the classic plumbing puzzle. In addition of rotating individual pieces, you must shift entire rows and columns to connect all endpoints back to the main source.

### Extra Features
* **Mobile & Touch-Friendly:** Optimized for touch interactions, allowing for a seamless gameplay experience on mobile devices and tablets.
* **Responsive Design:** Built to scale perfectly across all screen sizes, from desktop monitors to smartphones.
* **Multiple Languages:** The game is fully playable in both **English** and **Polish**.
* **UI Polish:** Features a smooth animated background and satisfying confetti visual effects when you clear a level.


## Technologies
- CSS / JavaScript
- [TypeScript](https://www.typescriptlang.org) 5.9.0
- [Vite](https://vitejs.dev) 7.1.11
- [Vue](https://vuejs.org) 3.5.22
- [Pinia](https://pinia.vuejs.org) 3.0.3
- [canvas-confetti](https://www.npmjs.com/package/canvas-confetti) 1.9.3
- [FontAwesome](https://fontawesome.com) 6.7.2
- [GoogleFonts](https://fonts.google.com)


<!--

> [!NOTE]  
> Room for improvements:
> - In-game instruction about game
> - More levels
> - More game modes (eg. Flow Free, 1 LINE)
> - More languages


## Setup
Ways to run this program: 
1. Use the [live demo](https://pasek108.github.io/ConnectGame/)
2. Download this repo and start live server ([VSCode LiveServer Extension](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer), Prepros preview etc.) 

To edit this program:
- Download this repo
- Install [Prepros](https://prepros.io)
- Add this project in Prepros
- Start coding
-->

<br>

# Details :scroll:

## UI and application flow

### Main Menu
The main menu serves as the entry point, presenting the three core game modes. Clicking any mode navigates the user to the respective level selection screen. A language toggle (English/Polish) is conveniently located in the top right corner for accessibility.

![Main Menu](/_for_readme/game_select_menu.png)

---

### Level Selection
Here, players can choose their preferred difficulty and select a specific puzzle. The UI clearly visually distinguishes between completed, unlocked, and locked levels. Progression is flexible—players can jump straight into harder difficulties without having to complete all the easy levels first. A persistent "back" button ensures smooth navigation.

![Level Selection](/_for_readme/level_select_menu.png)

---

### Game View
The core gameplay interface provides a clean, distraction-free experience. The header displays the current context (game mode and difficulty) alongside a level selector. It also features quick-action buttons for restarting the current puzzle or maximizing the board to fill the screen space.

![Game View](/_for_readme/game_view.png)

---

### Bridges Mode
An implementation of the classic *Hashiwokakero* puzzle. The board consists of islands with numeric values indicating their required number of bridge connections. The goal is to connect all islands into a single, continuous network by placing 1 or 2 bridges between them, ensuring that no paths intersect.

![Bridges Mode](/_for_readme/bridges_game_mode.png)

---

### Squares Mode
Players must restore a grid of interconnected square pieces so that all connections match up perfectly. The challenge lies in the different block constraints, indicated by color and icons:
* **Red (4 dots):** Static; cannot be moved or rotated.
* **Blue (center dot):** Can only be rotated.
* **Green (arrows in all directions):** Can be moved freely across the grid.
* **Orange (arrows + center dot):** Can be moved freely and rotated.
* **Purple (single-axis arrow):** Can only move along one specific axis.
* **Brown (single-axis + center dot):** Can move along one axis and be rotated.

![Squares Mode](/_for_readme/squares_game_mode.png)

---

### Pipes Mode
A dynamic variation of the classic pipe puzzle. Players must establish a continuous flow from the source to all endpoints. To solve the board, users must not only rotate individual pipe segments but also strategically shift entire rows and columns.

![Pipes Mode](/_for_readme/pipes_game_mode.png)
