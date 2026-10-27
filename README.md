# Smart Pantry Manager

A Java Android application for reducing food waste by recording ingredients already at home and suggesting only recipes that can be made with all required ingredients in sufficient quantities.

## Technology choice
- **Java** for all app activities and business logic.
- **SQLite** through `SQLiteOpenHelper` for persistent local storage.
- **ListView with a custom BaseAdapter** for the pantry list; recipe lists use an Android adapter.
- No location, GPS, mapping, payment or cloud features are used.

## Features
- Create, read, update and delete pantry ingredients.
- Ingredient name, positive quantity, unit and optional expiry date.
- 20 recipes seeded into SQLite on first install.
- Strict recipe matching: every required ingredient must be present and the summed available quantity must meet the recipe quantity. Simple plural and unit normalisation is applied. Incompatible units do not count as a match.
- Recipe detail with ingredients and method.
- Settings preference stored using SharedPreferences.
- Empty-state message when no recipes qualify.

## Run in Android Studio
1. Install Android Studio and a compatible JDK (JDK 17 is suitable for this Gradle configuration).
2. Extract the project folder and choose **Open** in Android Studio; select `SmartPantryManager`.
3. Allow Gradle sync to finish. Install an Android SDK platform for API 35 if Android Studio asks for it.
4. Create an emulator (or connect a USB-debugging-enabled Android phone).
5. Press **Run** and choose the `app` configuration.

The project uses Android Gradle Plugin 8.7.3 and compile SDK 35. If your installed Android Studio recommends a compatible Gradle/SDK update, accept the IDE's compatible upgrade and re-sync.

## GitHub requirement
Create a **public** GitHub repository and push the project while developing it. The assignment requires at least 10 genuine incremental commits. Do not manufacture or backdate commits. Suggested commit milestones are in `docs/GITHUB_COMMIT_PLAN.md`. Add the final repository URL to the report after you create it.

## Assignment submission items still requiring your own evidence
The assignment requires a 5–7 minute narrated video, actual screenshots from your running app, a working GitHub repository, your student details/signature and truthful reflection on challenges. These cannot be honestly fabricated by this source package. Use `docs/VIDEO_DEMO_SCRIPT.md` and `docs/REPORT_EVIDENCE_CHECKLIST.md`, then update the report with your real screenshots, GitHub URL, student details and demonstration video before submitting.
