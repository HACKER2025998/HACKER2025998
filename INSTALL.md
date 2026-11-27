# 🚀 Installation du README — xhackerip

Ton README de profil vit dans le repo spécial **`HACKER2025998/HACKER2025998`** (il existe déjà, il contient ton ancien « Hi there 👋 »).

## Contenu du pack

```
README.md                              ← le profil
assets/hero.svg                        ← bannière (matrix, glitch, radar, scanline)
assets/terminal.svg                    ← terminal Kali animé (whoami, nmap des skills)
assets/network.svg                     ← topologie réseau live (paquets, ACL DENY, alerte SIEM)
assets/timeline.svg                    ← parcours animé
assets/divider.svg · assets/footer.svg ← séparateurs + vagues de fin
profile/*.svg                          ← cartes stats/langages/snake (provisoires, régénérées chaque jour)
.github/workflows/profile-cards.yml    ← GitHub Action qui génère les cartes
```

## 1. Envoyer les fichiers

**Option A — en ligne de commande (recommandé)**

```bash
git clone https://github.com/HACKER2025998/HACKER2025998.git
cd HACKER2025998
# copie TOUT le contenu du pack ici (y compris le dossier caché .github)
cp -r /chemin/vers/xhackerip-readme/. .
rm -f INSTALL.md
git add -A
git commit -m "feat: profile README v2 — animated"
git push
```

**Option B — depuis le site GitHub**
Ouvre le repo → **Add file → Upload files** → glisse `README.md`, `assets/` et `profile/` → Commit.
Le dossier `.github` est caché sur la plupart des systèmes : crée plutôt le fichier à la main via **Add file → Create new file**, nomme-le `.github/workflows/profile-cards.yml` et colle son contenu.

## 2. Lancer la télémétrie (une seule fois)

1. Onglet **Actions** du repo → workflow **Profile cards** → **Run workflow**.
2. Attends ~1 minute : les cartes `profile/*.svg` sont remplacées par tes vraies stats et le snake.
3. Ensuite, ça se met à jour **tout seul chaque jour**.

> Si le job échoue sur « git push » (403) : **Settings → Actions → General → Workflow permissions → Read and write permissions** → Save, puis relance.

## 3. Personnaliser

| Tu veux changer… | Où |
|:--|:--|
| Le texte qui se tape sous la bannière | paramètre `lines=` de l'URL `readme-typing-svg` dans `README.md` (lignes séparées par `;`) |
| Les lignes du terminal / la topologie / la timeline | modifie les textes directement dans les `.svg` (ce sont des fichiers texte) |
| Les couleurs | cyan `00F0FF` · magenta `FF2E97` · vert `39FF88` · ambre `FFB800` · fond `05070F` |
| Ajouter un projet | copie un bloc `<td>…</td>` dans la section `PROJECTS` |

## Notes

- Toutes les animations « wow » sont des **SVG hébergés dans ton repo** : aucune dépendance externe, elles ne tomberont jamais en panne.
- Les seuls widgets externes restants sont le texte tapé, le streak, l'activity graph et le compteur de vues. S'il y en a un qui ne s'affiche pas un jour, c'est le service qui est saturé : le reste du profil n'est pas touché.
- Ton numéro de téléphone n'est volontairement **pas** dans le README (un profil GitHub est public et indexé). Le portfolio reste le point de contact.
