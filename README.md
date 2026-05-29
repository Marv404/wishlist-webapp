# Feature Branches – Namenskonvention & Erstellung

In diesem Repository folgen alle Feature Branches der **Git Flow Konvention**, um Übersicht, Zusammenarbeit und Release Management zu vereinfachen.

---

## 1. Namenskonvention

| Branch-Typ       | Präfix / Format                 | Beispiel                        | Zweck |
|-----------------|---------------------------------|---------------------------------|-------|
| Feature          | `feature/<kurze-beschreibung>` | `feature/login`                 | Neue Funktionalität, Feature für nächsten Release |
| Bugfix / Fix     | `bugfix/<kurze-beschreibung>`  | `bugfix/login-crash`            | Fehlerbehebung, kein neues Feature |
| Hotfix           | `hotfix/<kurze-beschreibung>`  | `hotfix/security-patch`         | Dringende Fixes direkt in `main` |
| Release          | `release/<version>`             | `release/1.0.0`                 | Vorbereitung auf einen Release |

**Tipps für Feature-Namen:**

- Kurz und aussagekräftig (`login`, `user-profile`, `checkout-page`)  
- Nur Kleinbuchstaben, Bindestriche statt Leerzeichen  
- Optional: Jira-Ticket oder Issue-ID einfügen:  
  `feature/JIRA-123-login`  

---

## 2. Feature Branch erstellen

### a) Basisbranch wechseln

Feature Branches werden immer **vom `develop`-Branch** erstellt:

```bash
git checkout develop
git pull origin develop
