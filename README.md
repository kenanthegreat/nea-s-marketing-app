# Kalendar Promocija

Fajlovi:
- `kalendar.html` (javni prikaz)
- `admin.html` (admin panel)
- `app-config.js` (Firebase config za oba ekrana)

## Lokalni test
1. Otvori `kalendar.html` u browseru.
2. Otvori `admin.html` i prijavi se lozinkom `admin123`.

## Objava na GitHub Pages
1. Kreiraj GitHub repozitorij (npr. `kalendar-promocija`).
2. U ovom folderu pokreni:

```bash
git add .
git commit -m "Cloud realtime calendar app"
git push
```

3. Na GitHub:
`Settings -> Pages -> Build and deployment -> Deploy from a branch -> main / (root) -> Save`

4. URL nakon deploya:
`https://USERNAME.github.io/REPO/`

## Firebase (globalna web app varijanta)
1. U Firebase Console napravi projekat.
2. Uključi Firestore Database (Native mode).
3. U `app-config.js` upiši svoj Web App config (`apiKey`, `projectId`, itd.).
4. Sačuvaj i deployaj na GitHub Pages.

Nakon toga:
- `admin.html` upisuje u Firestore.
- `kalendar.html` sluša Firestore real-time.
- izmjene su odmah vidljive na svim uređajima.

## Firestore pravila za početak (samo test)
```txt
rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
    match /{document=**} {
      allow read, write: if true;
    }
  }
}
```

Za produkciju obavezno pooštri pravila i dodaj autentikaciju admina.
