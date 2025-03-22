

# Music Player in React

A web-based music player application built with React, allowing users to play, pause, and manage a personalized music playlist. This project features a responsive design, audio controls, and a library management system, making it easy to enjoy music on both desktop and mobile devices.

## Preview
The final output includes a sleek interface with a navigation bar, song display, player controls, and a library sidebar to manage your music collection.

## Prerequisites
Before you begin, ensure you have the following installed:
- **Node.js**: Required to run the React application.
- **npm**: Comes with Node.js, used for package management.

## Technologies Used
- **React**: JavaScript library for building the user interface.
- **JavaScript**: Core programming language for functionality.
- **HTML/CSS**: Structure and styling of the application.
- **Sass**: CSS preprocessor for enhanced styling.
- **FontAwesome**: Icons for player controls and UI elements.

## Features
- **User-Friendly Interface**: Intuitive controls for play, pause, volume adjustment, and track progress.
- **Music Library Management**: Add, remove, and select songs from a customizable playlist.
- **Audio Controls**: Play, pause, skip, and auto-play next song functionality.
- **Track Progress Display**: Visual progress bar showing current time and duration.
- **Responsive Design**: Works seamlessly on desktop and mobile devices.

## Project Structure
```
music-player/
├── src/
│   ├── components/
│   │   ├── Library.js
│   │   ├── LibrarySong.js
│   │   ├── PlayerSong.js
│   │   ├── Navb.js
│   │   └── Song.js
│   ├── styles/
│   │   ├── app.scss
│   │   ├── library.scss
│   │   ├── nav.scss
│   │   ├── player.scss
│   │   └── song.scss
│   ├── App.js
│   ├── data.js
│   └── index.js
├── package.json
└── README.md
```

## Setup Instructions
Follow these steps to set up and run the project locally:

1. **Create a New React Project**  
   Open your terminal and run:
   ```bash
   npx create-react-app music-player
   ```

2. **Navigate to the Project Directory**  
   ```bash
   cd music-player
   ```

3. **Install Dependencies**  
   Install the required npm packages:
   ```bash
   npm install --save @fortawesome/react-fontawesome
   npm install --save @fortawesome/free-solid-svg-icons
   npm install sass
   ```

4. **Replace Source Files**  
   - Copy the provided `App.js` and `data.js` into the `src/` folder.
   - Create a `components/` folder in `src/` and add `Library.js`, `LibrarySong.js`, `PlayerSong.js`, `Navb.js`, and `Song.js`.
   - Create a `styles/` folder in `src/` and add `app.scss`, `library.scss`, `nav.scss`, `player.scss`, and `song.scss`.

5. **Customize the Playlist**  
   Edit `src/data.js` to add your own songs. The file currently includes a sample list of Billboard hits with YouTube links (see "Using YouTube Links" below).

6. **Run the Application**  
   Start the development server:
   ```bash
   npm start
   ```
   Open your browser and visit `http://localhost:3000/` to see the music player in action.

## Using YouTube Links
The `data.js` file includes YouTube URLs in the `audio` field for each song. Note the following:
- **Current Limitation**: The `<audio>` tag in `App.js` cannot directly play YouTube video URLs (e.g., `https://www.youtube.com/watch?v=VIDEO_ID`). These links are placeholders.
- **Workaround Options**:
  1. **Extract Audio**: Use a third-party service (e.g., `youtube-dl`) to convert YouTube links to MP3 URLs and update the `audio` fields with these direct links.
  2. **YouTube API**: Modify `App.js` to use the YouTube IFrame Player API with `<iframe>` instead of `<audio>` for playback (requires additional setup).
  3. **Host MP3s**: Replace YouTube links with hosted MP3 files for seamless playback.
- **Legal Note**: Ensure you have permission to use any audio content, especially if distributing the app, as YouTube’s Terms of Service restrict unauthorized use.

Example `data.js` snippet with YouTube links:
```javascript
{
  name: "The Twist",
  cover: "https://picsum.photos/200/300?random=1",
  artist: "Chubby Checker",
  audio: "https://www.youtube.com/watch?v=im9XuJJXylw",
  color: ["#FF6F61", "#6B5B95"],
  id: uuidv4(),
  active: true,
}
```

## Dependencies
The `package.json` includes:
```json
"dependencies": {
  "@fortawesome/free-solid-svg-icons": "^6.4.2",
  "@fortawesome/react-fontawesome": "^0.2.0",
  "react": "^18.2.0",
  "react-dom": "^18.2.0",
  "react-scripts": "5.0.1",
  "sass": "^1.68.0"
}
```

## Troubleshooting
- **Audio Not Playing**: If using YouTube links, ensure they’re replaced with direct MP3 URLs or implement the YouTube API.
- **Styles Not Loading**: Verify Sass is installed and the `.scss` files are correctly imported in `App.js`.
- **Component Errors**: Check that all component files are correctly implemented (not fully provided in the document).

## Credits
- Built following the tutorial from [GeeksforGeeks: Building a Music Player in React](https://www.geeksforgeeks.org/building-a-music-player-in-react/).
- Song data inspired by Billboard’s "Greatest of All Time Hot 100 Songs."

## License
This project is for educational purposes only. Ensure compliance with copyright laws when using audio content.

---

