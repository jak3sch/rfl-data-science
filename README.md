## Pipelines

### Variables

Für die automatische Erstellung von Daten im `data` Verzeichnis werden Piplines genutzt.

In der [gitLab Gruppe](https://gitlab.com/jakob-eschler/data-science/fantasy-football/rfl-group) werden dafür Umgebungsvariablen gesetzt.

| Name           | Value                                                                                      | Description                                                                                            |
| -------------- | ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ |
| `GITLAB_URL`   | `https://USERNAME:PASSWORD@gitlab.com/jakob-eschler/data-science/fantasy-football/rfl.git` | URL des Repositories, in das die Daten gepusht werden sollen. Inklusive Login Daten                    |
| `CURRENT_YEAR` | `2022`                                                                                     | Aktuelle Jahreszahl, die als Dateinamen genutzt werden können. **Muss mit Saisonstart erhöht werden.** |

### Pipelines

| Name                                                                                        | Description                                                                            | Dependencies | Schedule                 | Status                                                                                                                                                                      |
| ------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | ------------ | ------------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [Starter](https://gitlab.com/jakob-eschler/data-science/fantasy-football/rfl-group/starter) | Erzeugt die [rfl-starter Daten](https://github.com/jak3sch/rfl/tree/main/data/starter) |              | Wöchentlich Do 17 Uhr    | <img src="https://gitlab.com/jakob-eschler/data-science/fantasy-football/rfl-group/starter/badges/main/pipeline.svg?ignore_skipped=true" type="image/svg+xml" height="20"/> |
| [WAR](https://gitlab.com/jakob-eschler/data-science/fantasy-football/rfl-group/war)         | Erzeugt die [rfl-war Daten](https://github.com/jak3sch/rfl/tree/main/data/war)         | Starter      | Wöchentlich Do 17:30 Uhr | <img src="https://gitlab.com/jakob-eschler/data-science/fantasy-football/rfl-group/war/badges/main/pipeline.svg?ignore_skipped=true" type="image/svg+xml" height="20"/>     |
| [ELO](https://gitlab.com/jakob-eschler/data-science/fantasy-football/rfl-group/elo)         | Erzeugt die [rfl-elo Daten](https://github.com/jak3sch/rfl/tree/main/data/elo)         |              | Wöchentlich Do 17 Uhr    |
