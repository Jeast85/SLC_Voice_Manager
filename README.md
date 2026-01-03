# SLC Voice Pack Manager (v1.0)

**SLC Voice Pack Manager** is a tool designed to help you create, manage, and enhance custom voice packs for *Self Loading Cargo* (SLC). It allows you to create realistic Cabin Crew scripts, generate high-quality audio using generic or AI voices, and apply authentic "Intercom" effects.

---

## 📦 What's included?
1.  **SLC_Voice_Manager.exe**: The main application.
2.  **ffmpeg.exe**: Required for processing audio effects (do not delete!).
3.  **transavia_cabincrew.json**: A complete example voice pack (Transavia Dutch styling).

---

## 🚀 Getting Started (Tutorial)

### Step 1: Editor (Create your Script)
1.  Open the app. It starts in the **Variant Editor**.
2.  Click **"New / Reset"** to load a blank template with all standard SLC events (like `CrewGreetingPassenger`, `CrewSafetyAnnouncement`, etc.).
3.  Select an event from the list on the left.
4.  On the right, click **"+ Add Variation"**:
    *   **Text**: Type what the crew should say (e.g., "Dames en heren, welkom aan boord.").
    *   **Suffix**: (Optional) Add a filename suffix like `-morning` or `-arrEHAM` to make SLC play this specific clip only at certain times/locations.
5.  Repeat for as many events as you like.
6.  Click **"Save JSON"** to save your work (e.g., as `mypack.json`).

### Step 2: Generator (Make it real)
1.  Go to the **Generator** tab.
2.  **Choose your Method**:
    *   **SLC Text Files (TXT)**: **The Power User Choice!** This generates a complete folder structure with `.txt` files properly named for SLC.
        *   **Dynamic & Live**: SLC reads these files content *live* in the sim.
        *   **Variables**: Supports variables like `{timeofday}`, `{destination}`, etc.
        *   **Your Choice of Voice**: SLC uses these text files to generate audio using either **Standard Windows Voices** OR its own **Cloud API Integrations** (ElevenLabs/etc.) if you have them set up in SLC settings.
        *   *Why use this?* It saves you hours of manually creating text files and folders. Just type your script, click Generate, and drop the folder into SLC.
    *   **ElevenLabs Audio (MP3)**: Use this for high-quality AI voices (Reference: ElevenLabs API).
3.  If using **ElevenLabs**:
    *   Enter your **API Key** and **Voice ID**.
    *   Use **"Test Connection / Generate 1 Sample"** to verify everything works before spending credits.
    *   Uncheck **"Simulation Mode"** when you are ready to generate the real files.
4.  Click **"Start Generation"**. The app will create a folder structure ready for SLC.

### Step 3: Audio Effects (The "Intercom" Vibe)
*Make your crystal-clear AI voices sound like they are coming through a real aircraft PA system.*

1.  Go to the **Audio Effects** tab.
2.  Click **"Select Source Folder"** and choose the folder containing your generated MP3s (e.g., `Converted_Pack_Audio`).
3.  **Tweaking the Sound**:
    *   **Intercom EQ**: Use the slider to make it sound "narrow" (like a cheap phone) or "wide" (clearer).
    *   **Distortion**: adds a bit of grit/drive.
    *   **Normalize Volume**: Ensures all clips have a consistent loudness.
4.  Click **"PREVIEW SAMPLE"** to hear a random test clip with your current settings.
5.  When satisfied, click **"CREATE FX PACK"**.
    *   The app creates a **copy** of your folder (e.g., `Converted_Pack_Audio_FX`).
    *   It processes all files in that new folder. **Your original files remain untouched.**

---

## 📂 Installation in Self Loading Cargo
1.  Take your final folder (e.g., the `_FX` folder or the `TXT` folder).
2.  Rename it to something simple, e.g., `TransaviaNL`.
3.  Copy this folder into your SLC installation directory:
    *   `\Self Loading Cargo\VoicePacks\CabinCrew\`
4.  In SLC, go to **Settings > Audio > Cabin Crew** and select your new pack.

---


## 💡 Top Tips
*   **Safety First**: The Generator starts in "Simulation Mode" by default so you don't accidentally waste API credits.
*   **Variations**: The more variations you add to an event (e.g., 5 different ways to say "Hello"), the more realistic SLC will feel.
*   **Files**: Keep `ffmpeg.exe` in the same folder as the application for the Audio Effects to work.

**Enjoy your flight! ✈️**


![Editor Screenshot](images/SLC%20Voice%20Pack%20Manager%2003_01_2026%2019_35_16.png)
