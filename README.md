
# 🎶 Music Mood Analyzer & Playlist Generator

Analyze Spotify playlists, classify songs by mood, and generate custom playlists all in your browser using **Streamlit**.

---

## 📌 Overview

The **Music Mood Analyzer & Playlist Generator** is a Streamlit web application that uses the **Spotify Web API** (via the `spotipy` library) to analyze playlists and classify tracks based on audio features such as **valence** and **energy**.

### What you can do:

* Analyze any **public Spotify playlist**
* Classify tracks into moods:

  * Happy
  * Sad
  * Relaxed
  * Neutral
* View track details with **album artwork** and **audio previews**
* Generate **mood-based playlists**
* Export analyzed data and playlists to **CSV**

---

## 📂 Project Structure

```
├── app.py              # Main Streamlit application
├── requirements.txt    # Python dependencies
└── README.md           # Project documentation
```

---

## ✨ Features

* **Spotify Playlist Analysis**
  Fetch and analyze tracks using a Spotify playlist ID.

* **Mood Classification**
  Automatically classify songs using audio features.

* **Album Art & Previews**
  Display album covers and 30-second previews (if available).

* **Custom Playlist Generation**
  Create playlists based on your selected mood and song count.

* **Data Export**
  Save results and playlists as CSV files.

---

## ⚙️ Installation & Setup

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/Dhruthi16/Music_Mood_Analyser.git
cd Music_Mood_Analyser
```

---

### 2️⃣ Create & Activate a Virtual Environment (Optional but Recommended)

**Windows**

```bash
python -m venv venv
venv\Scripts\activate
```

**Linux / macOS**

```bash
python -m venv venv
source venv/bin/activate
```

---

### 3️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

---

### 4️⃣ Get Spotify API Credentials

1. Visit the **Spotify Developer Dashboard**
2. Create a new application
3. Copy your:

   * Client ID
   * Client Secret
4. Replace the placeholders in `app.py`:

```python
CLIENT_ID = "your_client_id"
CLIENT_SECRET = "your_client_secret"
```

---

## ▶️ Running the Application

```bash
streamlit run app.py
```

The app will open in your browser at:

```
http://localhost:8501
```

---

## 🎯 How to Use

### 🔹 Analyze a Playlist

1. Enter a **Spotify Playlist ID** in the sidebar
2. Click **Analyze Playlist**
3. View:

   * Track mood classification
   * Album artwork
   * Audio previews (if available)

---

### 🔹 Generate a Playlist

1. Select a **Mood** from the sidebar
2. Enter the desired number of songs
3. Click **Generate Playlist**
4. View the playlist and **export it as CSV**

---

## 🧠 Mood Classification Logic

| Mood    | Condition                      |
| ------- | ------------------------------ |
| Happy   | valence > 0.5 and energy > 0.5 |
| Sad     | valence < 0.5 and energy < 0.5 |
| Relaxed | valence > 0.5 and energy < 0.5 |
| Neutral | All other cases                |

---

## 📦 Dependencies

* streamlit
* spotipy
* pandas
* Pillow
* requests

📜 Exact versions are listed in `requirements.txt`.

