# Music Popularity Capstone: Afrobeat Analysis

**Group 7** · Machine Learning and AI (Essentials) · Thrive Campus

We are the data team at a music streaming service. Using Spotify audio data for the **Afrobeat** genre, this project answers three questions from the A&R department:

1. **What makes a track popular?** Can audio alone explain why some songs take off? *(regression)*
2. **Can we spot a hit before it charts?** So the playlist team promotes the right tracks. *(classification)*
3. **What moods exist inside the genre?** To build playlists around how music feels. *(clustering)*

## Project Structure
| File | What it is |
|---|---|
| `music_popularity_capstone.ipynb` | The main notebook: data cleaning, charts and all machine learning models |
| `spotify_tracks.csv` | The dataset (114,000 Spotify tracks across 114 genres) |
| `Afrobeat_Popularity_Report.md` | Our final report for a non-technical reader |
| `requirements.txt` | The Python packages needed to run the notebook |
| `SETUP_GUIDE.md` | Step-by-step setup instructions (Google Colab or your own computer) |

## How to Run It
The quickest way, if you already have Python 3.10 or newer:

```bash
git clone https://github.com/Tdaniels4real/music-popularity-capstone.git
cd music-popularity-capstone
pip install -r requirements.txt
jupyter notebook music_popularity_capstone.ipynb
```

Then choose **Kernel → Restart Kernel and Run All Cells**. The notebook runs from top to bottom without errors.

`spotify_tracks.csv` must stay in the **same folder** as the notebook. For full instructions, including Google Colab and virtual environments, see [SETUP_GUIDE.md](SETUP_GUIDE.md).

## The Data
The dataset is the [Spotify Tracks Dataset](https://www.kaggle.com/datasets/maharshipandya/-spotify-tracks-dataset) from Kaggle. It downloads as `dataset.csv` and has been renamed to `spotify_tracks.csv`. A copy is already included in this repository, so you do not need to download it.

After filtering to Afrobeat and cleaning (removing 1 duplicate track), we worked with **999 tracks**.

## Key Findings
| Question | Result |
|---|---|
| **Predict popularity** | Our best model (Linear Regression) is typically **9.04 points** off on a 0–100 scale and explains only **1.9%** of popularity (R² = 0.019). Audio alone barely explains popularity; marketing, playlists and fanbase matter far more. |
| **Spot the hits** | Our best model (Logistic Regression) is **62%** accurate (precision 0.61, recall 0.44), only a little better than always guessing "not a hit" (55%). It missed 50 of 90 real hits in the test set. |
| **Find the moods** | Afrobeat falls into **4 moods**: High-Energy Bangers, Sunny Dance Grooves, Intense & Dark, and Mellow Acoustic. All four have similar average popularity (23.8 to 25.6). |
| **Tune the model** | Grid Search improved the Decision Tree's accuracy only slightly, from 0.520 to 0.535. |

**Our main recommendation:** the streaming service should not judge Afrobeat tracks on audio alone. It should use audio data to organise mood-based playlists, and use the hit model only as a first screening step for human editors.

## Use of AI
As allowed by the project brief, we used an AI assistant (Claude) to explain concepts and errors, to help write and format parts of the notebook (mainly some section of parts 4 to 6), and to check our report against the notebook results. Every result comes from running our own notebook.