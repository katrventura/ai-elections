# POLITICAL DEEPFAKES FLOOD TIKTOK: Videos Generated With Artificial Intelligence Distort 2024 Presidential Race

This project is a data-driven analysis and visualization of artificial intelligence-generated political content from TikTok.

## Data Processing

### 1. Data Gathering | Jupyter notebook: 01-scraper

- Tool used: [Bellingcat hashtag analysis tool](https://github.com/bellingcat/tiktok-hashtag-analysis)
- Purpose: To gather all TikTok videos containing the hashtags #AIBiden and #AITrump
- Process: TikTok metadata of all videos for each hashtag was collected and the videos were downloaded using yt-dlp

### 2. Data Cleaning | Jupyter notebook: 02-cleaning

- Tool used: Python/pandas
- Process: Cleaned the JSON TikTok metadata, keeping only the following columns:
  - id: Unique identifier for the video
  - uniqueId: Unique identifier for the user
  - signature: User's signature or bio
  - followerCount: Number of followers for the user
  - aigcLabelType: AI-generated content label type
  - createTime: Time of video creation
  - desc: Video description
  - playCount: Number of video plays
  - shareCount: Number of times the video was shared
- Duplicates were removed, narrowing the initial 800+ dataset to 587 videos

### 3. Data Analysis | Jupyter notebook: 03-analysis

Each video was reviewed and categorized into the following:
- gamer: 217
- trump_deepfakes: 87
- trump_covers: 79
- biden_deepfakes: 57
- unknown: 51
- presidential_debates: 41
- psa_deepfakes: 28
- biden_covers: 15
- vietnamese_trump: 12

### 4. Data Visualization | Jupyter notebooks: 04-matching / 05-visualization

- Process: Each video was saved as a thumbnail and used in the initial iterations of the visualization
- Tool used: R for further analysis and visualization
