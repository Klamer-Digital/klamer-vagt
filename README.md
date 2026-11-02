# klamer-vagt

Vagten bag vagten for Klamer Hub (milepæl 14 i hubbens plan).

En GitHub Action kalder hubbens offentlige `/api/health` hvert 15. minut og fejler, hvis hubben ikke
svarer 200, hvis `ok` ikke er `true`, eller hvis drift-jobbet ikke er lykkedes inden for 30 minutter.
Fejler den, sender GitHub en mail.

Repoet er offentligt, fordi planlagte workflows er gratis i offentlige repoer. Det indeholder ingen
hemmeligheder: kun hubbens offentlige adresse, som kun svarer med status og alder i minutter.

Mail ved fejl går til den GitHub-bruger, der sidst ændrede cron-linjen i
`.github/workflows/hub-vagt.yml`. Slå mail til under github.com → Settings → Notifications → Actions
("Only notify for failed workflows").
