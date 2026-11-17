# Contributing

Use a short, made-up script when reporting a bug. Include your browser and operating system, the steps to reproduce the problem, and what happened. Check that any attached screenshots show only material you can share publicly.

The app lives in `index.html`. Changes need no build step. Before opening a pull request, run it locally and check editing, play and pause, mirror modes, and script persistence after a reload. For changes to text rendering, try a line with Hebrew or Arabic mixed with English.

If you change the inline JavaScript, update the script hash in the page's Content Security Policy. Compute it from the exact text between the script tags, including the surrounding newlines and indentation:

```sh
python3 - <<'PY'
from base64 import b64encode
from hashlib import sha256
from pathlib import Path

html = Path("index.html").read_text(encoding="utf-8")
script = html.split("<script>", 1)[1].split("</script>", 1)[0]
print("sha256-" + b64encode(sha256(script.encode("utf-8")).digest()).decode())
PY
```
