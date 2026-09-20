# LB 324

## Aufgabe 2

## Aufgabe 2

### pre-commit installieren

```bash
python -m venv .venv
.venv\Scripts\Activate.ps1        # Mac/Linux: source .venv/bin/activate
pip install -r requirements.txt pre-commit
pre-commit install --hook-type pre-commit --hook-type pre-push
```

- Bei jedem `git commit` wird der Code automatisch mit **black** formatiert.
- Bei jedem `git push` werden die Tests mit **pytest** ausgeführt. Schlagen sie fehl, wird der Push abgebrochen.
- Manuell ausführen: `pre-commit run --all-files` (Commit-Hooks) bzw. `pre-commit run --hook-stage pre-push --all-files` (Tests).

## Aufgabe 4
Erklären Sie hier, wie Sie das Passwort aus Ihrer lokalen `.env` auf Azure übertragen.
