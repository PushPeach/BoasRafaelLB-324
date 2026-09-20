# LB 324

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

### Passwort aus der lokalen `.env` nach Azure übertragen

Die `.env`-Datei wird nicht ins Repository hochgeladen (sie steht in der `.gitignore`). Darum wird das Passwort in Azure als Umgebungsvariable gesetzt:

1. Im Azure Portal die Web App öffnen.
2. Links **Settings → Environment variables → App settings → + Add** wählen.
3. Name: `PASSWORD`, Wert: `PushPeach` (mein GitHub-Benutzername).
4. **Apply** klicken und den Neustart der App bestätigen.


## Live-Version
boasrafael-lb324-dga0e7gvgxhrc4bm.germanywestcentral-01.azurewebsites.net
