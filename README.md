# CineVerse-Movie-Ticket-Booking-System

CineVerse is a movie booking application developed as a first-year university project in csci112 course using C++/CLI with Windows Forms. It enables users to explore movies by category, view detailed movie information, select showtimes, book seats, and manage bookings through an intuitive interface. The application integrates with Microsoft Excel for data storage, using OLEDB to handle user accounts, movie details, and booking records. Designed to simulate a cinema ticketing system, CineVerse offers user registration, profile management, dynamic movie selection, and booking cancellation, all within a visually engaging and interactive UI.

Developed by a team of five first-year university students, CineVerse showcases their skills in C++/CLI, Windows Forms, and Excel-based data management. The name "CineVerse" reflects its cinematic universe, offering diverse movie categories such as Marvel, Anime, DC, Disney, and Book Adaptions.

## Project Structure

- **cs112/**: Root project folder.
  - **data/**: Stores the application's data files.
    - `cinema_data.xlsx`: Excel file with user data (columns: id, username, password).
    - `Movies.xlsx`: Excel file with movie data (columns: name, imagePath, imagePath2, imagePath3, imagePath4, imagePath5, rate, description, showtimes, price).
    - `Booking.xlsx`: Excel file with booking data (columns: Showtime, Seat, Movie Name, Price, username, Status).
  - **Pictures/**: Directory for GUI images.
    - `images/`: General images (e.g., logo.png, imdb.png).
    - `pics/`: Movie-related images.
    - `categoral images/`: Category-specific images (subfolders: Marvel, Anime, DC, Disney, Book Adaptions).
  - **Src/**: Contains C++ source files.
    - `Adaptations.cpp`: Implementation for Book Adaptions category functionality.
    - `Anime.cpp`: Implementation for Anime category functionality.
    - `DC.cpp`: Implementation for DC category functionality.
    - `disney.cpp`: Implementation for Disney category functionality.
    - `homeForm.cpp`: Implementation for the home window.
    - `loginForm.cpp`: Implementation for the login window and application entry point.
    - `profileForm.cpp`: Implementation for the user profile and booking history.
    - `MovieDetailForm.cpp`: Implementation for the movie details and booking form.
    - `signinForm.cpp`: Implementation for the user registration form.
    - `main.cpp`: Application entry point.
    - `Marvel.cpp`: Movie data management implementation.
    - `ExcelManger.cpp`: Excel data handling implementation.
  - **include/**: Contains header files.
    - `Adaptations.h`: Book Adaptions category window.
    - `Anime.h`: Anime category window.
    - `DC.h`: DC category window.
    - `disney.h`: Disney category window.
    - `MovieDetailForm.h`: Movie details and booking form.
    - `profileForm.h`: User profile and booking history form.
    - `signinForm.h`: User registration form.
    - `users.h`: User class definition.
    - `loginForm.h`: Login form.
    - `Marvel.h`: Movie class and data management.
    - `ExcelManger.h`: Excel data handling utilities.
  - **Resources/**: Contains resource files for UI elements.
    - `Adaptations.resx`: Resources for Book Adaptions category window.
    - `Anime.resx`: Resources for Anime category window.
    - `DC.resx`: Resources for DC category window.
    - `disney.resx`: Resources for Disney category window.
    - `MovieDetailForm.resx`: Resources for movie details form.
    - `profileForm.resx`: Resources for profile form.
    - `signinForm.resx`: Resources for sign-up form.
    - `loginForm.resx`: Resources for login form.
    - `Marvel.resx`: Resources for movie UI elements.
    - `ExcelManger.resx`: Resources for Excel utilities.
  - **cs112.sln**: Visual Studio solution file.
  - **README.md**: Project documentation.

## Features

- **User Authentication**:
  - **Sign Up**: Users can register with a username and password, securely stored in `cinema_data.xlsx`.
  - **Log In**: A secure login system provides access to personalized features like booking and profile management.
- **Movie Browsing**:
  - **Category Selection**: Choose from categories like Marvel, Anime, Animation, Disney, or Book Adaptions.
  - **Dynamic Movie Display**: Movie names and posters are dynamically loaded from `Movies.xlsx` for each category.
- **Movie Booking**:
  - **Dynamic Movie Details**: Selecting a movie opens a detailed window with images, ratings, descriptions, and showtimes.
  - **Showtime and Seat Selection**: Pick a showtime and seats from a 3x5 grid with real-time availability updates.
  - **Booking Confirmation**: Booked seats are saved to `Booking.xlsx`, including movie name, showtime, seat, price, and user details.
  - **Cancellation System**: Cancel bookings from the cancelation button, updating `Booking.xlsx`.
- **Profile Management**:
  - **Booking History**: View past and upcoming bookings in separate lists.
- **Excel Integration**:
  - **Uses OLEDB to store and retrieve user data, movie details, and bookings in Excel files**.
- **Interactive UI**:
  - **Features hover effects, custom cursors, and dynamic panels** for an enhanced user experience.
  - **Includes logos, IMDb icons, and movie posters** for a cinematic feel.

## How to Run

- Download the project files (`CineVerse.sln`, `Data` folder with `cinema_data.xlsx`, `Movies.xlsx`, `Booking.xlsx`, `Pictures` folder with `pics`, `images`, `categoral images` subfolders, `Src` folder with `.cpp` files, `Include` folder with `.h` files, `Material` folder with `.resx` files), and ensure all are in the same directory with cs112.sln.
- Install Microsoft Visual Studio with C++/CLI support (2019 or later, with .NET Framework 4.7.2 or later).
- Install Microsoft Access Database Engine 2010 Redistributable (64-bit or 32-bit, matching your system) for OLEDB connectivity.
- Configure the project in Visual Studio by running cs112.sln file.
- Ensure `Data` files and `Pictures` folders are copied to the same directory.

## Usage

- **Launch the Application:**
  - Run `cs112.sln` in Visual Studio to open the login or sign-up form.
- **Sign Up:**
  - In the sign-up form (`signinForm`), enter a username, password, and confirm password, then click "Sign up" to register in `cinema_data.xlsx`.
- **Log In:**
  - Use the login form (`loginForm`) to authenticate with username and password.
- **Browse Movies:**
  - Navigate to the movie selection form (via `Marvel.h` or similar).
  - Select a movie to view details in `MovieDetailForm`.
- **Book Seats:**
  - In `MovieDetailForm`, select a showtime and seats (green: available).
  - Click "Book Seat" to save to `Booking.xlsx`.
  - Use "Cancel" to cancel bookings.
- **View Profile:**
  - In `profileForm`, toggle between past and upcoming bookings.
  - Use the sidebar to navigate or log out.

## Team Members

- **Mariam Elbadry:**

  - Designed and implemented the movie booking window (`MovieDetailForm.h`).
  - Enabled showtime and seat selection with a 3x5 grid and ticket booking.
  - Extracted movie details from `Movies.xlsx`.

- **Mariam Gamal:**

  - Developed the user profile window (`profileForm.h`).
  - Displayed past and upcoming bookings from `Booking.xlsx`.
  - Created a cancellation system for bookings.

- **Dareen Hassan:**

  - Built the home, sign-up (`signinForm.h`), and login (`loginForm.h`) windows.
  - Managed user data storage in `cinema_data.xlsx`.
  - Designed a dynamic panel for movie details.

- **Iren Nabil:**

  - Created the category window for selecting movie categories.
  - Implemented a system to display category-specific movies.

- **Fatma Eldahahn:**

- Developed the movies window with a dynamic panel.

Displayed movie names and posters from `Movies.xlsx`.





The project is organized into five main folders for modularity and ease of setup:


CineVerse/
├── Data/
│   ├── cinema_data.xlsx          # User data (id, username, password)
│   ├── Movies.xlsx               # Movie data (name, images, rating, description, showtimes, price)
│   └── Booking.xlsx              # Booking data (Showtime, Seat, Movie Name, Price, username, Status)
├── Pictures/
│   ├── pics/                     # General images (e.g., logo.png, imdb.png)
│   │   ├── logo.png
│   │   ├── imdb.png
│   │   └── [other general images]
│   ├── images/                   # Movie-related images
│   │   ├── [movie images].png
│   └── categoral images/         # Category-specific images
│       ├── Marvel/
│       │   ├── [Marvel images].png
│       ├── Anime/
│       │   ├── [Anime images].png
│       ├── Animation/
│       │   ├── [Animation images].png
│       ├── Disney/
│       │   ├── [Disney images].png
│       └── Book Adaptions/
│           ├── [Book Adaption images].png
├── Src/
│   ├── main.cpp                  # Application entry point
│   ├── Marvel.cpp                # Movie class implementation
│   ├── ExcelManger.cpp           # Excel data handling implementation
│   ├── [other .cpp files]        # Additional implementation files
├── Include/
│   ├── MovieDetailForm.h         # Movie details and booking form
│   ├── profileForm.h             # User profile and booking history form
│   ├── signinForm.h              # User registration form
│   ├── users.h                   # User class definition
│   ├── loginForm.h               # Login form
│   ├── Marvel.h                  # Movie class and data management
│   ├── ExcelManger.h             # Excel data handling utilities
│   └── [other .h files]          # Additional headers
├── Material/
│   ├── MovieDetailForm.resx      # Resources for MovieDetailForm
│   ├── profileForm.resx          # Resources for profileForm
│   ├── signinForm.resx           # Resources for signinForm
│   ├── loginForm.resx            # Resources for loginForm
│   ├── Marvel.resx               # Resources for Marvel form
│   ├── ExcelManger.resx          # Resources for ExcelManger utilities
│   └── [other .resx files]       # Additional resource files
├── CineVerse.sln                 # Visual Studio solution file
└── README.md                     # Project documentation
