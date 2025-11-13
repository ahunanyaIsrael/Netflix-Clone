# Netflix Clone

A modern Netflix-inspired streaming application built with React and Vite, featuring user authentication, movie/TV show browsing, and video playback capabilities.

## Features

- **User Authentication**: Sign up and login using Firebase Authentication
- **Movie & TV Show Browse**: Browse popular, top-rated, upcoming, and now-playing content
- **Search Functionality**: Search through a vast collection of movies and shows
- **Video Player**: Watch trailers directly within the application
- **Responsive Design**: Fully responsive UI that works on desktop, tablet, and mobile devices
- **Modern UI**: Netflix-inspired dark theme with smooth animations
- **Real-time Data**: Fetches movie and TV show data from TMDB API

## Tech Stack

- **Frontend Framework**: React 19.2.0
- **Build Tool**: Vite with Rolldown
- **Styling**: CSS3 with responsive media queries
- **Authentication**: Firebase Authentication
- **Database**: Firestore
- **APIs**: TMDB (The Movie Database) API
- **Routing**: React Router DOM 7.9.5
- **Notifications**: React Toastify
- **Linting**: ESLint

## Project Structure

```
src/
├── components/
│   ├── Footer/          # Footer component with social links
│   ├── NavBar/          # Navigation bar with profile dropdown
│   └── TitleCards/      # Reusable card carousel component
├── pages/
│   ├── Home/            # Main home page with hero banner
│   ├── Login/           # Authentication page (Sign In/Sign Up)
│   └── Player/          # Video player page
├── assets/              # Images and static files
├── App.jsx              # Main app component with routing
├── firebase.js          # Firebase configuration and auth functions
├── main.jsx             # React entry point
└── index.css            # Global styles
```

## Installation

1. **Clone the repository**

   ```bash
   git clone <repository-url>
   cd netflix-clone
   ```

2. **Install dependencies**

   ```bash
   npm install
   ```

3. **Set up environment variables**
   Create a `.env` file in the root directory with the following variables:

   ```
   VITE_FIREBASE_API_KEY=your_firebase_api_key
   VITE_FIREBASE_AUTH_DOMAIN=your_firebase_auth_domain
   VITE_FIREBASE_PROJECT_ID=your_firebase_project_id
   VITE_FIREBASE_STORAGE_BUCKET=your_firebase_storage_bucket
   VITE_FIREBASE_MESSAGING_SENDER_ID=your_firebase_messaging_sender_id
   VITE_FIREBASE_APP_ID=your_firebase_app_id
   VITE_TMDB_TOKEN=your_tmdb_api_token
   VITE_BASE_PATH=/Netflix-Clone
   ```

4. **Get API Keys**
   - **Firebase**: Set up a Firebase project at [Firebase Console](https://console.firebase.google.com/)
   - **TMDB**: Get your API token from [TMDB API](https://www.themoviedb.org/settings/api)

## Running the Application

### Development

```bash
npm run dev
```

The application will run at `http://localhost:5173`

### Build

```bash
npm run build
```

Creates an optimized production build in the `dist` folder.

### Preview

```bash
npm run preview
```

Preview the production build locally.

### Linting

```bash
npm lint
```

Run ESLint to check for code quality issues.

## Key Components

### [NavBar](src/components/NavBar/NavBar.jsx)

Navigation component featuring:

- Netflix logo and menu links
- Search, notifications, and profile icons
- Dynamic dark background on scroll
- Profile dropdown with logout functionality

### [TitleCards](src/components/TitleCards/TitleCards.jsx)

Reusable carousel component that:

- Fetches data from TMDB API
- Displays movie/show cards with smooth scrolling
- Links to player for video playback
- Supports different content categories

### [Player](src/pages/Player/Player.jsx)

Video player page that:

- Embeds YouTube trailers
- Displays video metadata
- Provides navigation back to home

### [Login](src/pages/Login/Login.jsx)

Authentication page with:

- Sign In and Sign Up modes
- Email/password authentication via Firebase
- Loading spinner during authentication
- Form validation and error handling

## Authentication

The app uses Firebase Authentication with the following functions:

- **signup()**: Creates new user accounts with email/password
- **login()**: Authenticates existing users
- **logout()**: Signs out current user

User data is stored in Firestore database.

## Deployment

The project is configured for deployment on Vercel using `vercel.json`. The rewrites configuration ensures proper routing for single-page application.

To deploy:

```bash
npm run build
# Deploy the dist folder to your hosting service
```

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## Performance Optimizations

- Lazy loading of components
- Optimized images and assets
- CSS media queries for responsive design
- Efficient API calls with proper caching

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

Copyright (c) 2025 Israel Ahunanya

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## Troubleshooting

### Movies not loading?

- Verify your TMDB API token is valid
- Check network tab in browser developer tools
- Ensure `.env` file has correct API credentials

### Authentication issues?

- Confirm Firebase credentials in `.env`
- Check Firebase console for authentication errors
- Verify user email format is valid

### Build errors?

- Clear `node_modules` and reinstall: `rm -rf node_modules && npm install`
- Clear Vite cache: `rm -rf dist && npm run build`

## Support

For issues and questions, please create an issue in the repository.

---

**Live Demo**: [Netflix Clone](https://netflix-clone-flame-nu.vercel.app/) 
