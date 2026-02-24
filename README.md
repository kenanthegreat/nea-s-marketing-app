# Kalendar Promocija

Fajlovi:
- `kalendar.html` (javni prikaz)
- `admin.html` (admin panel)

## Lokalni test
1. Otvori `kalendar.html` u browseru.
2. Otvori `admin.html` i prijavi se lozinkom `admin123`.

## Objava na GitHub Pages
1. Kreiraj novi GitHub repozitorij (npr. `kalendar-promocija`).
2. U ovom folderu pokreni:

```bash
git init
git add .
git commit -m "Initial calendar app"
git branch -M main
git remote add origin https://github.com/USERNAME/REPO.git
git push -u origin main
```

3. Na GitHub:
   `Settings -> Pages -> Build and deployment -> Deploy from a branch -> main / (root) -> Save`

4. Nakon deploya dobit ćeš URL:
   `https://USERNAME.github.io/REPO/`

## Važna napomena (bez Firebase)
- Aplikacija trenutno koristi `localStorage`.
- To znači da su podaci lokalni po browseru/uređaju.
- Ako marketing osoba doda događaj u adminu, taj događaj se **ne šalje automatski** svim korisnicima online.

Za zajedničke online podatke (svi korisnici vide iste izmjene) treba povezati Firebase/Firestore.
