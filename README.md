# Siqi Gu — Personal Homepage

Source for my personal academic homepage at [sikygu.github.io](https://sikygu.github.io), built as a plain static site — no framework, no build step.

## Structure

```
index.html          Page content (About / News / Education / Publications / Research / Honors / Contact)
css/style.css        Styling
js/script.js         Small nav script
assets/profile.jpg   Profile photo
assets/Siqi_Gu_CV.pdf CV, linked from the header
```

## Local preview

```bash
python3 -m http.server 8000
```

then open `http://localhost:8000`.

## Updating

Edit the files directly, then:

```bash
git add .
git commit -m "update"
git push
```

Changes go live at sikygu.github.io a minute or two after pushing.
