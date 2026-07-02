# subtitle-dictionary-service

**Automated subtitle generation service using OpenAI Whisper**  
OpenAI Whisperを使った動画字幕自動生成サービス

---

## Overview / 概要

**EN:**  
A service that searches movies via TMDB API, downloads trailers from YouTube,
transcribes audio using OpenAI Whisper, translates Hindi to Japanese,
and burns subtitles directly into videos.

**JP:**  
TMDB APIで映画を検索し、YouTubeから予告動画をダウンロード。
OpenAI Whisperで音声を文字起こしし、ヒンディー語から日本語へ翻訳後、
字幕を動画に焼き込むまでを自動化するサービスです。

---

## Tech Stack / 技術スタック

| Layer              | Technology                    |
| ------------------ | ----------------------------- |
| Backend            | Python 3, Flask               |
| AI / Transcription | OpenAI Whisper                |
| External APIs      | TMDB API, YouTube             |
| Database           | PostgreSQL                    |
| Frontend           | JavaScript, HTML/CSS, Webpack |

---

## Features / 主な機能

- Search movies using TMDB API / TMDB APIを使った映画検索
- Download movie trailers from YouTube / YouTubeから予告動画をダウンロード
- Transcribe audio using OpenAI Whisper / Whisperによる音声文字起こし
- Translate Hindi to Japanese / ヒンディー語→日本語の自動翻訳
- Generate subtitles and burn them into videos / 字幕生成と動画への焼き込み

---

## Contributions / 開発者・担当範囲

This project was built as a team. Gabriel Harada Dias handled the entire backend.  
本プロジェクトはチームで開発しました。バックエンド全体をGabriel Harada Diasが担当しました。

| Name / 氏名         | Role / 担当範囲                                                                                                                            |
| ------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| Gabriel Harada Dias | Backend (Flask, Whisper integration, TMDB/YouTube API, database) / バックエンド全体（Flask、Whisper連携、TMDB・YouTube API、データベース） |
| [Teammate name]     | [Frontend / role] / [フロントエンド・担当範囲]                                                                                             |

## Setup Instructions / セットアップ手順

### 1. Install Dependencies / 依存パッケージのインストール

```bash
pip install -r requirements.txt
```

### 2. Environment Variables / 環境変数の設定

Copy the example environment file and fill in your API keys:  
環境変数ファイルをコピーし、APIキーを入力してください：

```bash
cp .env.example .env
```

Edit `.env` and add your API keys / `.env`を編集し、以下のキーを追加してください：

- **OPENAI_API_KEY**: Get from https://platform.openai.com/api-keys
- **TMDB_API_KEY**: Get from https://www.themoviedb.org/settings/api
- **DATABASE_URL**: Your PostgreSQL connection string / PostgreSQL接続文字列
- **SECRET_KEY**: A random string for Flask sessions  
  （生成方法: `python -c "import secrets; print(secrets.token_hex(32))"`）

### 3. Run the Application / アプリの起動

```bash
python app.py
# or
flask run
```

The application will be available at / 起動後は以下でアクセスできます：  
`http://localhost:8000`

---

## Author / 作者

Gabriel Harada Dias
Kyoto Seika University, 2027 graduation  
GitHub: [@nosfer4tu](https://github.com/nosfer4tu)
