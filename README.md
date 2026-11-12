# anthem-workshop

National Anthem Project: GMU Practice Workshop 1 (Branch, Push, Pull, Merge, Resolve a Conflict).

A small Flask app that shows the Indian National Anthem. It was built by a three-person team, with each person working from their own Linux user account.

## Team

| User   | Role      | Responsibility                                  |
|--------|-----------|-------------------------------------------------|
| satish | Team Lead | Owns the repository, merges, resolves conflicts |
| rajesh | Developer | Writes the application and the anthem content   |
| ramesh | Tester    | Finds problems, fixes formatting and text       |

## Project structure

```
anthem-workshop/
├── anthem.txt            # first line of the anthem (Part 1)
├── app.py                # Flask application (Part 2)
└── templates/
    └── index.html        # anthem page (Parts 2 to 4)
```

## What the history shows

| Part | Exercise                    | Result                                                                           |
|------|-----------------------------|----------------------------------------------------------------------------------|
| 0    | Configure three users       | Commits carry the names Satish, Rajesh and Ramesh                                |
| 1    | Publish and clone           | Satish published the repo; Rajesh and Ramesh cloned it                           |
| 2    | Push and pull               | Rajesh added the app, Ramesh added the second line, Satish pulled both           |
| 3    | Branch, merge, delete       | `feature/second-stanza` (2 commits) merged into `main`, then deleted             |
| 4    | Merge conflict              | `title-english` and `title-bilingual` both changed the `<h1>`; Satish resolved it |
| 5    | Undo and recover            | Local only: `reset --hard` and recovery with `git reflog`                        |

See it with:

```bash
git log --oneline --graph
git shortlog -sn
git blame templates/index.html
```

## Run the app

```bash
pip install flask
python3 app.py
# open http://<server-ip>:5000
```
