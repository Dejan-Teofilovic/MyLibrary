MyLibrary is a modern and user-friendly library management web application built with React.js, Vite, Tailwind CSS, and powered by the Google API for fetching book data. It also incorporates Auth0 for secure authentication and session management, Font Awesome icons for styling, Axios for API calls, React Infinite Scroll for lazy loading, Toastify for notification messages, and `react-autocomplete` for search suggestions.

## Tech Stack 🛠️

- [Vite](https://vitejs.dev/) - Fast React.js build tool.
- [React.js](https://reactjs.org/) - JavaScript library for building user interfaces.
- [Tailwind CSS](https://tailwindcss.com/) - A utility-first CSS framework for fast and customizable styling.
- [Google Books API](https://developers.google.com/books/docs/overview) - Used as the endpoint for book data.
- [Auth0](https://auth0.com/) - Authentication and session management.
- [Font Awesome](https://fontawesome.com/) - Icon library for styling.
- [Axios](https://axios-http.com/) - Promise-based HTTP client for API calls.
- [React Infinite Scroll](https://github.com/ankeetmaini/react-infinite-scroll-component) - Infinite scrolling component for efficient pagination.
- [Toastify](https://fkhadra.github.io/react-toastify/introduction/) - React notification library for user feedback.
- [react-autocomplete](https://github.com/reactjs/react-autocomplete) - React component for search suggestions.
- [Vercel](https://vercel.com/) - Deployment platform for hosting web applications.

---

## Features ✅

- [x] An aesthetically pleasing and optimized loading animation.
- [x] New user signup and login, using Proper authentication and sessions (Sign in with social media, Email and mobile number verification gets extra brownie points).
- [x] Users can see the list of books, preferably using an actual endpoint (API) as a data source for books.
- [x] Instead of loading all the results on the page, perform an optimized pagination (infinite scrolling with lazy loading).
- [x] A well-built search bar, with suggestions (like Google Search, YouTube) that suggests and searches based on all the fields like Book name, Author name, Genre, Year of publishing, etc.
- [x] An exclusive way of indicating the availability of the books, and the number of available copies, along with the previously mentioned fields.
- [x] Users can filter and sort the list of books based on Title, Author, Subject, and Publish - date.
- [x] Show the count of books upon every search results and upon every filtering.
- [x] Implement a cart feature, upon adding books to the cart, the user will be able to check out and rent them. This should reflect in the availability and number of copies fields.

---

## Configuration - Setting Up API Keys 🛠️

To use certain features of the MyLibrary project, you'll need to configure the following API keys:

1. 📚 **Google Books API Key**: This key is required to fetch book information from Google Books API.

2. 🔐 **Auth0 Domain and Client ID**: These are required for authentication and user management.

Follow these steps to set up the API keys:

### 1. Google Books API Key

To obtain a Google Books API Key:

1. 🌐 Visit the [Google Cloud Console](https://console.cloud.google.com/).
2. 🏗️ Create a new project if you haven't already.
3. 🛠️ Navigate to the "APIs & Services" > "Credentials" section.
4. ➕ Click on "Create Credentials" and select "API Key."
5. 📋 Copy the generated API key.

### 2. Auth0 Domain and Client ID

To obtain Auth0 credentials:

1. 🌐 Visit [Auth0](https://auth0.com/) and sign in or create an account.
2. 🏗️ Create a new application or use an existing one.
3. ⚙️ Navigate to the "Settings" of your Auth0 application.
4. 📋 Find and copy the "Domain" and "Client ID."

### 3. Create a .env File

Once you have obtained the necessary API keys, create a `.env` file in the project root directory (if it doesn't already exist) and add the following environment variables with your API keys:

```env
VITE_REACT_APP_GOOGLEBOOK_API_KEY=YOUR_GOOGLEBOOK_API_KEY
VITE_REACT_APP_AUTH0_DOMAIN=YOUR_AUTH0_DOMAIN
VITE_REACT_APP_AUTH0_CLIENT_ID=YOUR_AUTH0_CLIENT_ID
```

Replace YOUR_GOOGLEBOOK_API_KEY, YOUR_AUTH0_DOMAIN, and YOUR_AUTH0_CLIENT_ID with the respective values you obtained from Google and Auth0.

Make sure to keep your .env file secure and do not share your API keys publicly.

Now, you have successfully configured the required API keys for the MyLibrary project. You can start using these keys in your code to access Google Books API and authenticate with Auth0.

---

## Project Dockerization 📦

To run RepoSavant in a Docker container, follow these steps:

1. Clone this repository.
2. Build the Docker image:

```bash[]
docker build --pull --rm -f "Dockerfile" -t mylibrary:latest
```

3. Run the Docker container:

```bash[]
docker run --rm -d  -p 8080:8080/tcp mylibrary:latest
```

---
