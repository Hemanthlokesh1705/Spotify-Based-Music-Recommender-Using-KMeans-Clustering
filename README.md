# 🎧 SpotCluster: A Spotify-Based Music Recommender Using KMeans Clustering

SpotCluster is a content-based music recommendation system that groups songs from Spotify by analyzing their **audio features** using **KMeans clustering**. It helps users discover musically similar songs by learning from characteristics like energy, tempo, and valence — not just artist or genre.

---

## 📌 Features

- 🎵 Built on Spotify's audio features
- 🧠 Uses unsupervised learning (KMeans clustering)
- 📊 Visualizes cluster quality with Elbow and Silhouette methods
- 🔍 Recommends top songs from the same musical cluster
- 🛠 Cleanly handles missing values and scaled features
- 📈 Optional PCA visualization for clusters

---

## 🗂 Dataset

- Spotify dataset with **14,584 songs**
- Columns include:
  - `track_name`, `artist_name`, `popularity`
  - `danceability`, `energy`, `valence`, `tempo`, etc.

---

## 🧠 How It Works

1. **Preprocessing**:
   - Select meaningful numerical audio features
   - Handle missing values (`NaN`)
   - Normalize using `StandardScaler`

2. **Clustering**:
   - Fit KMeans on scaled features
   - Use Elbow Method & Silhouette Score to choose optimal `k`
   - Assign each song to a cluster

3. **Recommendation**:
   - User enters a song name
   - Find its cluster
   - Return top `n` most popular songs from the same cluster

---

## 🧪 Example

```python
Enter the song you like: Shape of You

🎵 Top 5 Similar Songs:
1. Stay - Artist: Zedd
2. Let Me Love You - Artist: DJ Snake
3. Closer - Artist: The Chainsmokers
...
