# 🎵 Music Shelf

> A personal collection of my favorite songs, presented in a clean, responsive, and interactive web interface.

<p align="center">
  <img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white" alt="HTML5">
  <img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white" alt="CSS3">
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" alt="JavaScript">
</p>

<p align="center">
  <strong>🎧 Discover my favorite tunes in one place.</strong>
</p>

---

## ✨ Features

### 🎵 Personal Music Collection

Music Shelf contains a curated collection of songs from different artists and genres.

Each song includes:

* 🖼️ Album/song artwork
* 🎵 Song title
* 👤 Artist name
* 🟢 Spotify link
* 🔴 YouTube Music link

---

### 🎨 Modern UI

The website uses a dark, warm color palette with:

* Gradient background
* Glassmorphism header
* Rounded cards
* Soft shadows
* Hover effects
* Smooth transitions
* Responsive grid layout

---

### 📌 Sticky Header

The header stays visible while scrolling.

When the page is scrolled, the header automatically collapses to take up less space.

```text
Before scrolling
┌─────────────────────────────────────────┐
│             Music Shelf                 │
│       Discover my favorite tunes       │
└─────────────────────────────────────────┘

After scrolling
┌─────────────────────────────────────────┐
│             Music Shelf                 │
└─────────────────────────────────────────┘
```

---

### 🖼️ Interactive Song Cards

Each song is displayed as an individual card.

Hovering over a card creates a floating effect and highlights the card.

The artwork also smoothly scales when hovered.

---

### 🔗 Music Links

Every song provides two ways to listen:

**Spotify**

Opens the song on Spotify in a new tab.

**YouTube Music**

Opens the corresponding song on YouTube Music in a new tab.

---

## 🎧 Current Songs

The current collection includes:

|  # | Song                | Artist                     |
| -: | ------------------- | -------------------------- |
| 01 | Lovesong            | Adele                      |
| 02 | Atlantis            | Seafret                    |
| 03 | WILDFLOWER          | Billie Eilish              |
| 04 | Let Down            | Radiohead                  |
| 05 | Lovers Rock         | TV Girl                    |
| 06 | double take         | Dhruv                      |
| 07 | Confident           | Justin Bieber              |
| 08 | Killshot            | Magdalena Bay              |
| 09 | Sailor Song         | Gigi Perez                 |
| 10 | Cool for the Summer | Demi Lovato                |
| 11 | The Machine         | Reed Wonder, Aurora Olivas |
| 12 | Loser               | Tame Impala                |
| 13 | Harvey              | Her's                      |
| 14 | Reflections         | The Neighbourhood          |
| 15 | Golden Brown        | The Stranglers             |
| 16 | Love Story          | Indila                     |
| 17 | Lilith              | Saint Avangeline           |

---

## 🛠️ Technologies Used

### HTML5

Used to create the structure of the website.

### CSS3

Used for:

* Layout
* Colors
* Gradients
* Card design
* Animations
* Transitions
* Responsive grid
* Glassmorphism effects

### JavaScript

Used to:

* Store the song data
* Dynamically generate song cards
* Create Spotify and YouTube Music links
* Handle image interactions
* Control the sticky header animation

---

## 📂 Project Structure

```text
Music-Shelf/
│
├── index.html
│
├── Assets/
│   ├── Adele.jpg
│   ├── Atlantis.jpg
│   ├── WILDFLOWER.jpg
│   ├── LetDown.jpg
│   ├── LoversRock.jpg
│   ├── doubletake.jpg
│   ├── Confident.jpg
│   ├── Killshot.jpg
│   ├── SailorSong.jpg
│   ├── CoolForTheSummer.jpg
│   ├── TheMachine.jpg
│   ├── Loser.jpg
│   ├── Harvey.jpg
│   ├── Reflections.jpg
│   ├── GoldenBrown.jpg
│   ├── LoveStory.jpg
│   └── Lilith.jpg
│
└── README.md
```

---

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/YOUR-USERNAME/music-shelf.git
```

### 2. Open the project

```bash
cd music-shelf
```

### 3. Launch the website

Open:

```text
index.html
```

in your browser.

That's it! No additional dependencies or installation are required.

---

## ➕ Adding a New Song

Songs are stored inside the JavaScript `songs` array.

To add another song, add a new object:

```javascript
{
    Title: "Song Name",
    Artist: "Artist Name",
    image: "Assets/SongName.jpg",
    spotify: "https://open.spotify.com/track/...",
    ytmusic: "https://music.youtube.com/watch?v=..."
}
```

Then place the corresponding image inside the `Assets` folder.

The website automatically creates the card.

---

## 🎨 Design

The project uses a warm dark theme.

### Main Colors

```text
Background
#292323 → #655151

Cards
#1F150C

Primary Text
#FFFFFF

Secondary Text
#A7A7A7

Song Text
#E1DCC9

Accent Gradient
#382A1A → #D5CB9B
```

The design combines these colors with transparency, blur, shadows, and gradients to create a modern music-library aesthetic.

---

## ✨ Animations

Music Shelf uses CSS transitions to make interactions feel smoother.

### Card Hover

```css
.card:hover {
    transform: translateY(-8px);
}
```

Cards move upward when hovered.

### Image Hover

```css
.card img:hover {
    transform: scale(1.05);
}
```

The artwork slightly enlarges when hovered.

### Header Collapse

JavaScript detects scrolling:

```javascript
window.addEventListener('scroll', () => {
    if (window.scrollY > 50) {
        headerCard.classList.add('collapsed');
    } else {
        headerCard.classList.remove('collapsed');
    }
});
```

This automatically changes the header when the user scrolls.

---

## 📱 Responsive Layout

The songs are displayed using CSS Grid:

```css
.grid {
    display: grid;
    grid-template-columns:
        repeat(auto-fill, minmax(220px, 1fr));
    gap: 20px;
}
```

This allows the number of columns to automatically adapt to the available screen width.

```text
Desktop

┌────────┐ ┌────────┐ ┌────────┐ ┌────────┐
│ Song   │ │ Song   │ │ Song   │ │ Song   │
└────────┘ └────────┘ └────────┘ └────────┘


Tablet

┌────────┐ ┌────────┐
│ Song   │ │ Song   │
└────────┘ └────────┘


Mobile

┌──────────────┐
│     Song     │
└──────────────┘
┌──────────────┐
│     Song     │
└──────────────┘
```

---

## 🔮 Future Improvements

Some ideas for future versions:

* [ ] 🔍 Add song search
* [ ] 🎼 Add genre filtering
* [ ] 🔀 Add shuffle functionality
* [ ] ❤️ Add favorite songs
* [ ] 🌙 Add light/dark mode
* [ ] 🎚️ Add sorting options
* [ ] 🎵 Add an embedded music player
* [ ] 📱 Improve mobile navigation
* [ ] 💾 Save favorites using `localStorage`
* [ ] 🖼️ Add animated album artwork
* [ ] 📊 Add music statistics
* [ ] 🚀 Deploy the website with GitHub Pages

---

## 🤝 Contributing

This is primarily a personal music collection, but suggestions and improvements are welcome.

If you find a bug or have an idea:

1. Open an issue.
2. Explain the problem or suggestion.
3. Include screenshots when useful.
4. Submit a pull request if you've made a fix.

---

## 📜 License

This project is intended for personal and educational use.

Music, artwork, and external links belong to their respective artists, platforms, and copyright holders.

---

## 👨‍💻 Author

G.Yashwanth Kumar

Built with:

```text
HTML • CSS • JavaScript • 🎵
```

---

## ⭐ Support

If you like the project, consider giving the repository a ⭐.

<p align="center">

### 🎧 Thanks for checking out Music Shelf!

**Made with ❤️ and a lot of music.**

</p>

