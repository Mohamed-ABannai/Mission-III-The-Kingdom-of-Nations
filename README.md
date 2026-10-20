<div align="center">

# 🏰 Mission III: The Kingdom of Nations

### 🌍 A React Debugging & API Integration Mission

![Difficulty](https://img.shields.io/badge/Difficulty-Medium-DAA520?style=for-the-badge)
![Time](https://img.shields.io/badge/Time-60%20Minutes-4682B4?style=for-the-badge)
![Unit](https://img.shields.io/badge/Unit-III-9370DB?style=for-the-badge)
![Stack](https://img.shields.io/badge/Stack-React%20%7C%20REST%20API-61DAFB?style=for-the-badge&logo=react&logoColor=black)

---

</div>

## 📜 The Royal Story

Welcome, Software Knight!

The Kingdom of Nations has suffered a terrible disaster. The Royal Archives, which contain information about every country in the world, have been corrupted.

Country cards are displaying incorrect information. The search system is malfunctioning, and the archives are struggling to communicate with the outside world.

Your mission is to restore the **Kingdom of Nations** by debugging the React application, repairing the API connection, and rebuilding the country explorer.

The kingdom is counting on you!

---

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

---

## 🛠️ Getting Started

### 1. Install Dependencies

Install the project's dependencies before starting your mission.

```bash
npm install
```

### 2. Configure Your API Access

Visit the [REST Countries documentation](https://restcountries.com/) to review the available API endpoints and authentication requirements.

**Important:** Check the starter project's API instructions before creating an API key. The public REST Countries API and any third-party or hosted API service may have different authentication requirements.

### 3. Create Your Environment File

If your assigned API service requires an API key, create a `.env` file in the project root and configure the required variables.

Example:

```env
VITE_COUNTRIES_API_URL=YOUR_API_ENDPOINT
VITE_COUNTRIES_API_KEY=your_api_key_here
```

Replace the example values with the correct configuration for your assigned API.

If your API does not require an API key, only configure the API URL.

**Remember:**

- Vite exposes client-side environment variables only when their names begin with `VITE_`.
- Never commit real secrets or private API keys to GitHub.
- Variables prefixed with `VITE_` are included in client-side code and should not be used to protect secret credentials.
- Restart the development server after changing your `.env` file.

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
- Ensure the API key, if required, is sent correctly.
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

Investigate the following:

- Is the API key valid, if required?
- Is the endpoint correct?
- Are the environment variable names correct?
- Did you restart the development server after editing `.env`?
- Are the allowed CORS origins configured correctly?
- What do the browser console and Network tab reveal?
- Is the response format what your code expects?

**Note:** CORS is controlled by the server's response headers. A React code change alone cannot fix a server that does not allow your origin.

---

## 🧙 Progressive Hints

Use these hints only when your team gets stuck. Try debugging the code before opening each hint!

<details>
<summary>🔍 Hint 1 — Environment Variables</summary>

Vite only exposes environment variables to client-side code when their names use the `VITE_` prefix.

Check how the application reads its API configuration and whether the variable names match those in your `.env` file.

</details>

<details>
<summary>🔍 Hint 2 — API Response Structure</summary>

Do not assume that the response is a plain array.

Inspect the response in the Network tab and check whether the country data is nested inside objects or arrays.

Also, check whether the server returned JSON, an error message, or an authentication response.

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

Check the condition used to display the country cards and the key passed to each card.

</details>

<details>
<summary>🔍 Hint 5 — The React Lifecycle</summary>

Review the dependency array of your effect. Consider what happens when the effect updates the same state that it depends on.

Also, check whether the loading state is reset at the correct time and whether the request runs more often than expected.

</details>

<details>
<summary>🔍 Hint 6 — CORS or Authentication?</summary>

A CORS error and an authentication error are different problems.

Check the response status in the Network tab. Verify your API key and allowed origins before assuming the React code is the cause.

A request can also fail because of an incorrect endpoint, rate limits, or a server-side error.

</details>

---

## 👑 Bonus Quests

Want to earn extra points for your team?

- **🌍 Country Counter (+3 points):** Display the number of countries currently shown.
- **🔄 Reset Filters (+3 points):** Add a button that clears the search and restores the region filter.
- **💬 Improved Feedback (+4 points):** Create a clear, user-friendly loading and error experience.

---

## 🏆 Scoring

| Challenge | Points |
|---|---:|
| 🏛️ Restore the Royal Archives | 10 |
| 🪪 Repair the Country Cards | 8 |
| 🔎 Rebuild the Search System | 8 |
| 📚 Fix the Country List | 6 |
| 🔄 Repair the React Lifecycle | 4 |
| **Main Mission Total** | **36** |
| Bonus Quests | Up to 10 |
| **Maximum Score** | **46** |

---

## 📦 Submission Requirements

Before submitting, make sure you have:

- [ ] Fixed the required bugs.
- [ ] Tested the search and region filters.
- [ ] Confirmed that country cards display correctly.
- [ ] Checked loading, error, and empty states.
- [ ] Verified that the application runs successfully.
- [ ] Committed and pushed your work to GitHub.
- [ ] Kept real API keys and secrets out of your repository.

---

<div align="center">

### 👑 The Kingdom Is Counting on You!

A true Software Knight does not simply fix the symptoms. They investigate the cause, test their solution, and protect the kingdom from future bugs.

**Good luck, Software Knights!** 🏰

*May your components render, your states stay synchronized, and your API requests succeed!*

---

**Codoria — Unit III: React**

</div>
