# Setup Guide

You can run this project in your browser with Google Colab, or on your own computer.

Whichever option you choose, the notebook and `spotify_tracks.csv` **must be in the same folder**. The notebook reads the file by name and does not look in subfolders.

---

## Option 1: Run in Google Colab (Recommended)
If you do not want to install Python, you can run the whole project in your browser.

1. Go to [Google Colab](https://colab.research.google.com/) and sign in with a Google account.
2. Click **File → Open notebook**, choose the **GitHub** tab, paste `https://github.com/Tdaniels4real/music-popularity-capstone` and open `music_popularity_capstone.ipynb`.
   *(Alternatively, download the notebook from GitHub and use **File → Upload notebook**.)*
3. On the left side of the screen, click the **Folder icon** (Files).
4. Click the **Upload** icon and upload `spotify_tracks.csv` (download it from the GitHub repository first). Wait until the upload finishes.
5. In the top menu, click **Runtime → Run all** to run the project from top to bottom.

> Colab deletes uploaded files when the session ends, so you will need to upload `spotify_tracks.csv` again each time you start a new session.

---

## Option 2: Run on Your Own Computer

### 1. Prerequisites
- **Python 3.10 or newer**: download it from [python.org](https://www.python.org/downloads/).
  *Windows users: tick the box that says **"Add Python to PATH"** during installation.*
- **pip**: included automatically with Python from python.org.
- **An internet connection**: needed once, to download the project and install the packages.

### 2. Get the Files
**With Git:**
```bash
git clone https://github.com/Tdaniels4real/music-popularity-capstone.git
cd music-popularity-capstone
```

**Without Git:** on the GitHub page, click **Code → Download ZIP**, then extract the ZIP file.

Check that these files are in the same folder:
- `music_popularity_capstone.ipynb`
- `spotify_tracks.csv`
- `requirements.txt`

> If `spotify_tracks.csv` is missing, download the [Spotify Tracks Dataset](https://www.kaggle.com/datasets/maharshipandya/-spotify-tracks-dataset) from Kaggle (free account needed), rename `dataset.csv` to `spotify_tracks.csv`, and put it in the project folder.

### 3. Open a Terminal in the Project Folder
- **Windows:** open Command Prompt or PowerShell.
- **macOS:** open the Terminal app.
- **Linux:** open your terminal.

Move into the project folder with `cd`, for example `cd music-popularity-capstone`.

### 4. Create a Virtual Environment (Recommended)
A virtual environment keeps this project's packages separate from other projects on your computer.

**Windows (Command Prompt):**
```bash
python -m venv venv
venv\Scripts\activate
```

**Windows (PowerShell):**
```powershell
python -m venv venv
venv\Scripts\Activate.ps1
```
*(If PowerShell says running scripts is disabled, run `Set-ExecutionPolicy -Scope CurrentUser RemoteSigned` once, then try again.)*

**macOS & Linux:**
```bash
python3 -m venv venv
source venv/bin/activate
```
*(If Linux says `venv` or `pip` is missing, install them with `sudo apt update && sudo apt install python3-venv python3-pip`.)*

When the environment is active, you will see `(venv)` at the start of your terminal line.

### 5. Install the Packages
```bash
pip install -r requirements.txt
```

### 6. Open the Notebook
```bash
jupyter notebook
```
This opens a tab in your web browser. Click `music_popularity_capstone.ipynb` to open it.

*(You can also open the notebook in VS Code with the Python and Jupyter extensions. Select the `venv` environment as the kernel.)*

### 7. Run Everything
1. In the Jupyter menu, click **Kernel**.
2. Select **Restart Kernel and Run All Cells**.
3. The notebook runs every cell in order, from top to bottom. It takes about a minute.

---

## Troubleshooting
| Error you see | What it usually means |
|---|---|
| `FileNotFoundError: spotify_tracks.csv` | The CSV is not in the same folder as the notebook, or it is still called `dataset.csv`. |
| `ModuleNotFoundError: No module named 'sklearn'` (or `pandas`, `seaborn`…) | The packages are not installed in the environment you are using. Activate your `venv` and run `pip install -r requirements.txt` again. |
| `'python' is not recognized` (Windows) | Python was not added to PATH. Reinstall Python and tick **"Add Python to PATH"**. |
| Charts do not appear | Run the cells in order from the top, using **Restart Kernel and Run All Cells**. |
