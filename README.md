# 🏰 Mission III: The Kingdom of Nations

### 🌍 A React Debugging & API Integration Mission

![Difficulty](https://img.shields.io/badge/Difficulty-Medium-DAA520?style=for-the-badge)
![Time](https://img.shields.io/badge/Time-60%20Minutes-4682B4?style=for-the-badge)
![Unit](https://img.shields.io/badge/Unit-III-9370DB?style=for-the-badge)
![Stack](https://img.shields.io/badge/Stack-React%20%7C%20REST%20API-61DAFB?style=for-the-badge&logo=react&logoColor=black)

---

## 📜 The Royal Story

Welcome, Software Knight!

The Kingdom of Nations has suffered a terrible disaster. The Royal Archives, which contain information about every country in the world, have been corrupted.

Country cards are displaying incorrect information. The search system is malfunctioning, and the archives are struggling to communicate with the outside world.

Your mission is to restore the **Kingdom of Nations** by debugging the React application, repairing the API connection, and rebuilding the country explorer.

The kingdom is counting on you!

## 🎯 Mission Objectives

By completing this mission, you will practice:

- Debugging React components and JSX.
- Managing state with `useState`.
- Fetching API data with `useEffect`.
- Handling loading states and errors.
- Working with forms and controlled inputs.
- Filtering and searching data.
- Rendering lists with unique React keys.
- Using environment variables.
- Troubleshooting API requests and CORS errors.

## 🛠️ Getting Started

### 1. Install Dependencies

```bash
npm install
```

### 2. Configure Your API Access

Visit the [REST Countries documentation](https://restcountries.com/docs) and create an account if required. Generate an API key.

In your API key settings, configure the allowed origins for your local development environment:

- `localhost`
- `127.0.0.1` (if you use this address)

Enter the hostname only. Do not include the protocol, port, or path.

### 3. Create Your Environment File

Create a `.env` file in the project root and add your configuration:

```env
VITE_COUNTRIES_API_URL=https://api.restcountries.com/countries/v5
VITE_COUNTRIES_API_KEY=your_api_key_here
```

Replace `your_api_key_here` with your actual API key.

**Important:** Never commit your real API key to GitHub. Keep your `.env` file private, and restart the development server after changing environment variables.

### 4. Start the Application

```bash
npm run dev
```

Open the local URL shown in your terminal.

---

## ⚔️ Mission Challenges

### 🏛️ Challenge 1: Restore the Royal Archives — 10 Points

The Royal Archives cannot retrieve country information correctly.

Your tasks:

- Repair the API configuration and request.
- Ensure the API key is sent correctly.
- Read the response structure correctly.
- Store the retrieved countries in React state.
- Handle loading and error states.

### 🪪 Challenge 2: Repair the Country Cards — 8 Points

The country cards are displaying missing or incorrect information.

Your tasks:

- Display each country's name, capital, region, population, and flag.
- Handle missing or incomplete API data safely.
- Format population values correctly.
- Ensure JSX renders the information without errors.

### 🔎 Challenge 3: Rebuild the Search System — 8 Points

The kingdom's search and filtering systems are no longer reliable.

Your tasks:

- Repair the country search input.
- Make sure the input reflects the correct state.
- Restore filtering by region.
- Ensure search and region filters work together.

### 📚 Challenge 4: Fix the Country List — 6 Points

The archive's country list is not rendering as expected.

Your tasks:

- Display the country cards correctly.
- Handle the empty-list state.
- Ensure each rendered card has a stable, unique key.

### 🔄 Challenge 5: Repair the React Lifecycle — 4 Points

The application is making unnecessary requests or displaying incorrect loading behavior.

Your tasks:

- Review the effect that fetches the country data.
- Correct the effect dependencies.
- Prevent unnecessary repeated requests.
- Ensure loading and error states behave correctly.

### 🧭 Challenge 6: Troubleshoot the API Connection

The archives may still fail to connect even after the code has been repaired.

Check the following:

- Is the API key valid?
- Is the endpoint correct?
- Are the environment variable names correct?
- Did you restart the development server after editing `.env`?
- Are the allowed CORS origins configured correctly?
- What do the browser console and Network tab reveal?

---

## 🧙 Progressive Hints

Use these hints only when your team gets stuck. Try debugging the code before opening each hint!

<details>
<summary>🔍 Hint 1 — Environment Variables</summary>

Vite only exposes environment variables to client-side code when their names use the `VITE_` prefix.

Check how the application reads its API configuration.

</details>

<details>
<summary>🔍 Hint 2 — API Response Structure</summary>

Do not assume that the response is a plain array.

Inspect the response in the Network tab and check whether the country data is nested inside objects or arrays.

</details>

<details>
<summary>🔍 Hint 3 — Controlled Inputs</summary>

A controlled input should receive its current value from the correct state variable and update that state when the user types.

Check whether the search input and region selector are connected to the appropriate state.

</details>

<details>
<summary>🔍 Hint 4 — Rendering Lists</summary>

An empty array is still truthy in JavaScript.

Also, React needs a stable, unique key when rendering a list of components.

</details>

<details>
<summary>🔍 Hint 5 — The React Lifecycle</summary>

Review the dependency array of your effect. Consider what happens when the effect updates the same state that it depends on.

Also, check whether the loading state is reset at the correct time.

</details>

<details>
<summary>🔍 Hint 6 — CORS or Authentication?</summary>

A CORS error and an authentication error are different problems.

Check the response status in the Network tab. Verify your API key and allowed origins before assuming the React code is the cause.

</details>

---

## 👑 Bonus Quests

Want to earn extra points for your team?

- **Country Counter (+3 points):** Display the number of countries currently shown.
- **Reset Filters (+3 points):** Add a button that clears the search and restores the region filter.
- **Improved Feedback (+4 points):** Create a clear, user-friendly loading and error experience.

## 🏆 Scoring

| Challenge | Points |
|---|---:|
| Restore the Royal Archives | 10 |
| Repair the Country Cards | 8 |
| Rebuild the Search System | 8 |
| Fix the Country List | 6 |
| Repair the React Lifecycle | 4 |
| **Main Mission Total** | **36** |
| Bonus Quests | Up to 10 |
| **Maximum Score** | **46** |

## 📦 Submission Requirements

Before submitting, make sure you have:

- Fixed the required bugs.
- Tested the search and region filters.
- Confirmed that country cards display correctly.
- Checked loading, error, and empty states.
- Verified that the application runs successfully.
- Committed and pushed your work to GitHub.
- Kept your real API key out of your repository.

**Remember:** A true Software Knight does not simply fix the symptoms. They investigate the cause, test their solution, and protect the kingdom from future bugs.

Good luck, Software Knights! 🏰