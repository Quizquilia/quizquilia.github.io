# Bloggen auf quizquilia.de

Jeder Beitrag ist eine einfache Textdatei (Markdown) im Ordner `_posts`. Sobald sie dort liegt und
in `main` gespeichert ist, baut GitHub die Seite automatisch neu – nach ein bis zwei Minuten ist der Beitrag online.

## 1. Beitrag anlegen (im Browser auf github.com)

1. Das Repository `quizquilia.github.io` öffnen, in den Ordner **`_posts`** gehen.
2. **Add file → Create new file**.
3. Dateiname nach dem Muster `JJJJ-MM-TT-kurzer-titel.md`, z. B. `2026-11-03-schlechte-verleihtitel.md`
   (Kleinbuchstaben, Bindestriche statt Leerzeichen, keine Umlaute). Das Datum im Namen ist das Veröffentlichungsdatum.
4. Als Inhalt oben diese Kopfzeilen, darunter den Text:

   ```
   ---
   title: "Schlechte Verleihtitel"
   tags: [quizidee]
   ---

   Hier beginnt der Text.
   ```

   `tags` ist optional, die Zeile kann weg. Die Vorlage liegt auch in `_drafts/vorlage.md`.
5. Schreibhilfe: `## Überschrift`, `**fett**`, `*kursiv*`, `- Aufzählung`, `> Zitat`, `[Linktext](https://adresse.de)`.

## 2. Am Handy (GitHub-App)

Die App kann Dateien bearbeiten, aber nicht gut neue anlegen. Am einfachsten: im Handy-Browser
github.com öffnen und wie oben vorgehen (bei Bedarf „Desktop-Version anfordern“ wählen).
Vorhandene Beiträge lassen sich in der App über den Stift-Button ändern.

## 3. Claude bitten

Einfach schreiben: „Leg einen Entwurf für einen Beitrag zu … an.“ Claude legt die Datei auf einem
eigenen Branch an und öffnet einen Pull Request. Inhalte, Fakten und Fragen lieferst du; Claude erfindet keine.

## 4. Vorschau und Veröffentlichung

- **Direkt veröffentlichen:** Datei in `_posts` auf `main` speichern („Commit changes“ → direkt auf `main`). Danach 1–2 Minuten warten; Fortschritt unter dem Reiter *Actions* („pages build and deployment“).
- **Erst prüfen:** Beim Speichern „Create a new branch … and start a pull request“ wählen. Im Pull Request ist der Text lesbar; veröffentlicht wird erst mit **Merge**.
- **Entwurf:** Dateien in `_drafts/` erscheinen nie auf der Seite. Zum Veröffentlichen nach `_posts/` verschieben (Stift-Button → Dateiname/Pfad ändern, Datum voranstellen).
- **Lokale Vorschau (optional, für Technik-Fans):** `bundle install`, dann `bundle exec jekyll serve --drafts`.

## 5. Wenn etwas nicht erscheint

- Dateiname prüfen (Datum vorn, Endung `.md`, Ordner `_posts`).
- Die drei Striche `---` oben und unten im Kopf müssen vorhanden sein.
- Fehler stehen im Reiter *Actions* beim fehlgeschlagenen Lauf.

Der RSS-Feed liegt unter `https://quizquilia.de/feed.xml`.
