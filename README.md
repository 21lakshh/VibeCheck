# 🎵 VibeCheck

**Every moment deserves its soundtrack.**  
VibeCheck is your personal music companion that creates the perfect playlist based on your current mood, weather, and situation. Using AI-powered mood analysis and Spotify integration, it delivers a tailored music experience that matches your vibe.

🌐 **[Live Demo](https://vibe-check-jet-eight.vercel.app/)**

## 🤖 How It Works - The VibeCheck Flow

1. **Location & Weather Analysis** 🌍
   - Select your location using our interactive map interface
   - Real-time weather data is fetched using OpenWeatherMap API
   - Weather conditions influence both UI aesthetics and music selection

2. **Mood Selection** 🎭
   - Choose your current emotional state
   - Select additional situational context (e.g., studying, working out, relaxing)
   - Dynamic UI adapts to your selections with weather-based animations

3. **AI-Powered Music Analysis** 🧠
   - Utilizes Groq LLM (Meta Llama 4 Scout) for intelligent music analysis
   - Processes multiple factors:
     - Current weather conditions
     - Selected mood
     - Situational context
     - Time of day
   - Generates contextually aware music recommendations

4. **Playlist Generation** 🎵
   - AI suggests 10 perfectly matched songs
   - One-click playlist creation in your Spotify account
   - Songs are curated based on:
     - Weather atmosphere
     - Emotional resonance
     - Activity compatibility
     - Musical preferences

## 🎨 Dynamic UI Features

### Weather-Based Themes
- **Rainy**: Animated rain drops with a cool, blue color palette
- **Sunny**: Bright, warm animations with sun rays
- **Cloudy**: Soft, moving cloud animations

### Mood-Responsive Design
- Smooth transitions between different states
- Interactive elements reflect current context
- Ambient background animations

## 📸 Screenshots

### Landing Page
![Landing Page](/public/ss1.jpg)

### Authentication
![Authentication](/public/ss2.jpg)

### Dashboard
![Dashboard](/public/ss3.png)

### Profile View
![Profile](/public/ss4.png)

### Music Recommendations
![Music Recommendations](/public/ss5.png)

### Friend Activity
![Friend Activity](/public/ss6.png)

## 🛠️ Tech Stack

### Frontend
- **Framework**: React with Vite
- **Styling**: TailwindCSS
- **State Management**: React Context
- **Animations**: Framer Motion, GSAP
- **Icons**: Lucide React, Tabler Icons
- **Weather Animations**: Custom CSS and GSAP animations

### Backend & Infrastructure
- **Backend-as-a-Service**: Supabase
- **Authentication**: Supabase Auth (Google OAuth)
- **Database**: PostgreSQL (via Supabase)
- **Hosting**: Vercel
- **Real-time**: Supabase Real-time subscriptions

### AI & Machine Learning
- **LLM Engine**: Groq
- **Model**: Meta Llama 4 Scout
- **Use Cases**:
  - Music mood analysis
  - Context-aware recommendations
  - Weather-music correlation
  - Situational playlist generation

### External APIs
- **Music**: Spotify Web API
- **Weather**: OpenWeatherMap API
- **Location**: Browser Geolocation API
- **Maps**: Leaflet for location selection

## 🚀 Getting Started

### Prerequisites
- Node.js (v16 or higher)
- pnpm (recommended) or npm
- Spotify Developer Account
- Supabase Account
- OpenWeatherMap API Key

### Environment Setup
Create a `.env.local` file with:
```env
VITE_SUPABASE_URL=your_supabase_url
VITE_SUPABASE_ANON_KEY=your_supabase_anon_key
VITE_SPOTIFY_CLIENT_ID=your_spotify_client_id
VITE_SPOTIFY_CLIENT_SECRET=your_spotify_client_secret
VITE_OPENWEATHER_API_KEY=your_openweather_api_key
```

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/21lakshh/VibeCheck.git
   cd VibeCheck
   ```

2. Install dependencies:
   ```bash
   pnpm install
   ```

3. Start the development server:
   ```bash
   pnpm dev
   ```

### Supabase Setup
1. Create a new Supabase project
2. Run the database migrations:
   ```sql
   -- Run the SQL files in order:
   1. database_migration.sql
   2. supabase_chat_schema.sql
   3. fix_rls_policies.sql
   ```

### Spotify Developer Setup
1. Create a Spotify Developer application
2. Add the following redirect URIs:
   - `http://localhost:5173/callback` (development)
   - `https://vibe-check-jet-eight.vercel.app/callback` (production)

## 📱 Core Features

### Authentication
- Google OAuth via Supabase
- Secure session management
- Protected routes

### Music Features
- Mood-based playlist generation
- Top tracks and artists display
- Music sharing with friends
- Playlist creation and management

### Social Features
- Friend system with request management
- Real-time chat functionality
- Music taste compatibility
- Activity feed

### Profile Management
- Customizable user profiles
- Music statistics
- Listening history
- Friend management

## 🔐 Security Features

- Secure authentication flow
- Row Level Security (RLS) in Supabase
- Protected API endpoints
- Secure token management

## 📦 Project Structure
```
VibeCheck/
├── src/
│   ├── components/    # React components
│   ├── hooks/        # Custom React hooks
│   ├── lib/          # Utility functions and API clients
│   ├── pages/        # Page components
│   └── Agents/       # AI-related functionality
├── public/           # Static assets
└── database/         # SQL migrations and schemas
```

## 🌟 Upcoming Features

- [ ] Music mood analysis using machine learning
- [ ] Group listening sessions
- [ ] Advanced music recommendations
- [ ] Custom playlist algorithms
- [ ] Enhanced social features

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📞 Support

For support, please open an issue in the GitHub repository or contact the maintainers.

---

Made with ❤️ by Unorthodox
