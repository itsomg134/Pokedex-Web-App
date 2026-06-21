# Pokédex Web App

A modern, responsive Pokédex website built with vanilla HTML, CSS, and JavaScript. Browse, search, and explore Pokémon with a sleek glassmorphism UI design.

![Pokédex Preview](https://raw.githubusercontent.com/PokeAPI/sprites/master/sprites/pokemon/other/official-artwork/25.png)

##  Features

-  **Real-time Search** - Find Pokémon by name instantly
-  **Responsive Design** - Works perfectly on desktop, tablet, and mobile
-  **Glassmorphism UI** - Modern frosted glass aesthetic with gradient backgrounds
-  **High-Quality Artwork** - Official Pokémon artwork for each entry
-  **Type Badges** - Color-coded type indicators (Fire, Water, Grass, etc.)
-  **Pagination** - Browse through Pokémon with smooth page navigation
-  **Fast Performance** - Optimized API calls with parallel fetching
-  **386 Pokémon** - Covers Generations I-III by default


<img width="1873" height="1235" alt="image" src="https://github.com/user-attachments/assets/b0940e05-7e09-4105-85ae-1bb0110e2bbf" />

## Technologies Used

- **HTML5** - Semantic structure
- **CSS3** - Custom properties, Flexbox, Grid, animations
- **JavaScript (ES6+)** - Async/await, Fetch API, DOM manipulation
- **[PokéAPI](https://pokeapi.co/)** - Free Pokémon data REST API
- **Font Awesome 6** - Icon library
- **Google Fonts** - Inter typeface

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/pokedex.git
   ```

2. Navigate to the project directory:
   ```bash
   cd pokedex
   ```

3. Open `index.html` in your browser:
   ```bash
   # Using Python's simple HTTP server
   python -m http.server 8000
   
   # Or just double-click index.html
   ```

No build tools or dependencies required! 🎉

## Usage

1. **Browse Pokémon** - Scroll through the grid or use pagination buttons
2. **Search** - Type a Pokémon name in the search bar and press Enter or click "Find"
3. **View Details** - Each card shows the Pokémon's image, ID number, and types
4. **Clear Search** - Empty the search field to reset and view all Pokémon

## Customization

### Change Pokémon Limit
Edit line ~230 in `index.html`:
```javascript
const response = await fetch(`${API_BASE}/pokemon?limit=386&offset=0`);
```
Change `386` to your desired number (max 898 for all generations).

### Modify Colors
The CSS uses custom type colors in lines ~134-150:
```css
.grass { background: #78C850; }
.fire { background: #F08030; }
/* Add or modify type colors here */
```

## Project Structure

```
pokedex/
├── index.html          # Main application file
├── screenshots/        # Screenshots for README
│   ├── main.png
│   └── search.png
└── README.md           # Project documentation
```

## 🌟 Key Implementation Details

- **Parallel Data Fetching** - Uses `Promise.all()` to fetch multiple Pokémon details simultaneously
- **Client-Side Filtering** - Search happens instantly without additional API calls
- **Lazy Loading** - Images load as they enter the viewport
- **Error Handling** - Graceful fallbacks for failed API requests
- **Accessibility** - Semantic HTML and ARIA-friendly structure

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

### Ideas for Contributions
- Add modal with detailed Pokémon stats
- Implement type filtering
- Add evolution chain display
- Include shiny sprite toggle
- Add dark/light theme switch
- Implement infinite scroll

## 📝 API Reference

This project uses the [PokéAPI](https://pokeapi.co/docs/v2):
- `GET /pokemon?limit=386` - Fetch Pokémon list
- `GET /pokemon/{name}` - Fetch individual Pokémon details

## 🐛 Known Issues

- Some Pokémon may have missing artwork (falls back to sprite)
- Rate limiting may occur with very large lists
- Mobile performance may vary on older devices

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
