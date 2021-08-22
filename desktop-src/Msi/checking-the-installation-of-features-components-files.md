---
description: Wenn Sie nach dem Ausführen einer Installation überprüfen müssen, ob eine bestimmte Funktion, Komponente oder Datei installiert wurde, aktivieren Sie während der Installation die Ausführliche Protokollierungsoption. Weitere Informationen Windows Installer-Protokollierung und Befehlszeilenoptionen.
ms.assetid: c4547e5d-ea71-494f-9d92-c7fef23bcc0f
title: Überprüfen der Installation von Features, Komponenten, Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 866b4f7b042c97660e43a92fc55eeb99e2f1e9f3574a9b03c4d3d6e6096504c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145605"
---
# <a name="checking-the-installation-of-features-components-files"></a>Überprüfen der Installation von Features, Komponenten, Dateien

Wenn Sie nach dem Ausführen einer Installation überprüfen müssen, ob eine bestimmte Funktion, Komponente oder Datei installiert wurde, aktivieren Sie während der Installation die Ausführliche Protokollierungsoption. Weitere Informationen [Windows Installer-Protokollierung und](windows-installer-logging.md) [Befehlszeilenoptionen.](command-line-options.md)

Das ausführliche Protokoll enthält einen Eintrag für jedes Feature und jede Komponente, die das Installationspaket installieren kann. Das Protokoll gibt an, welcher Zustand dieses Features oder dieser Komponente vor der Installation war, welcher Zustand von der Installation angefordert wurde und in welchem Zustand das Installationsprogramm das Feature oder die Komponente verlassen hat. Feature- und Komponenteneinträge im Protokoll werden wie in den folgenden Beispielen angezeigt.

``` syntax
MSI (s) (40:A4): Feature: QuickTest; Installed: Absent;   Request:
 Local;   Action: Local
MSI (s) (40:A4): Component: QuickTest; Installed: Absent;   Request:
 Local;   Action: Local
```

Dieses ausführliche Protokoll gibt Dies an:

-   Der Installationsstatus des QuickTest-Features und der Komponente war vor dem Ausführen des Pakets nicht vorhanden.
-   Das Paket hat eine lokale Installation dieser angefordert.
-   Das Feature und die Komponente waren nach dem Ausführen des Pakets im lokal installierten Zustand.

Die Bezeichnung "Installiert" im Protokoll verweist auf den aktuellen Installationsstatus des Features oder der Komponente, "Anforderung" bezieht sich auf den angeforderten Installationsstatus des Features oder der Komponente. "Aktion" bezieht sich auf den tatsächlichen Aktionszustand des Features oder der Komponente.

In der folgenden Tabelle sind die möglichen Komponenten- oder Featurezustände aufgeführt, die im Protokoll angezeigt werden können.



| Protokolleintrag              | Beschreibung                                                                                                     |
|------------------------|-----------------------------------------------------------------------------------------------------------------|
| Anforderung: NULL          | Keine Anforderung.                                                                                                     |
| Aktion: NULL           | Es wurde keine Aktion ergriffen.                                                                                                |
| Installiert: Absent      | Die Komponente oder das Feature ist derzeit nicht installiert.                                                                |
| Anforderung: Absent        | Komponente oder Feature für Installationsanforderungen müssen deinstalliert werden.                                                      |
| Aktion: Nicht vorhanden         | Das Installationsprogramm deinstalliert tatsächlich die Komponente oder das Feature.                                                             |
| Installiert: Lokal       | Die Komponente oder das Feature ist derzeit installiert, um lokal ausgeführt zu werden.                                                       |
| Anforderung: Lokal         | Die Komponente oder das Feature "Installationsanforderungen" muss installiert werden, um lokal ausgeführt zu werden.                                           |
| Aktion: Lokal          | Das Installationsprogramm installiert tatsächlich die Komponente oder das Feature, um lokal ausgeführt zu werden.                                                  |
| Installiert: Quelle      | Die Komponente oder das Feature ist derzeit installiert, um von der Quelle aus ausgeführt zu werden.                                                 |
| Angefordert: Quelle      | Die Installation fordert an, dass die Komponente oder das Feature installiert wird, um von der Quelle aus ausgeführt zu werden.                                |
| Aktion: Quelle         | Das Installationsprogramm installiert tatsächlich die Komponente oder das Feature, um von der Quelle aus ausgeführt zu werden.                                        |
| Installiert: Ankündigung   | Das Feature wird derzeit angekündigt. Komponenten werden nie angekündigt.                                               |
| Anforderung: Ankn.     | Das Feature "Installationsanforderungen" wird als angekündigtes Feature installiert.                                            |
| Aktion: Ankn.      | Das Installationsprogramm installiert das Feature tatsächlich als angekündigtes Feature.                                               |
| Anforderung: Neuinstallation     | Das Feature "Installationsanforderungen" wird neu installiert. Komponenten verwenden den Neuinstallationsstatus nicht.                            |
| Aktion: Neuinstallation      | Das Installationsprogramm installiert das Feature neu.                                                                          |
| Installiert: Aktuell     | Das Feature ist derzeit im standardmäßig erstellten Installationsstatus installiert.                                           |
| Anforderung: Aktuell       | Das Feature "Installationsanforderungen" muss im standardmäßig erstellten Installationsstatus installiert sein.                               |
| Aktion: Aktuell        | Das Installationsprogramm installiert das Feature tatsächlich im standardmäßig erstellten Installationsstatus.                                  |
| Aktion: FileAbsent     | Das Installationsprogramm deinstalliert tatsächlich die Dateien der Komponente und lässt alle anderen Ressourcen der Komponente installiert.      |
| Aktion: HKCRAbsent     | Das Installationsprogramm entfernt tatsächlich die HKCR-Informationen der Komponente. Datei- und Nicht-HKCR-Informationen bleiben erhalten.                  |
| Aktion: HKCRFileAbsent | Das Installationsprogramm entfernt tatsächlich die HKCR-Informationen und -Dateien der Komponente. Alle anderen Ressourcen der Komponente bleiben erhalten. |



 

Das ausführliche Protokoll enthält einen Eintrag für jede Datei, die vom Paket installiert werden kann. Das Protokoll teilt mit, was mit der Datei geschehen ist, und bietet eine Erläuterung. Dateieinträge im Protokoll werden wie im folgenden Beispiel angezeigt.

``` syntax
MSI (s) (40:A4): File: C:\Test\TESTDB.EXE;  Won't Overwrite;  Existing
 file is of an equal version
```

Dieses Protokoll gibt an, dass das Installationsprogramm die vorhandene Testdb.exe nicht überschreibt, da die vorhandene Datei mit der installierten Version identisch ist.

> [!Note]  
> Wenn Sie ein Installationspaket erstellen müssen, das während einer Installation nach einer vorhandenen Datei oder einem vorhandenen Verzeichnis auf dem Computer des Benutzers sucht, verwenden Sie die unter Suchen nach vorhandenen [Anwendungen, Dateien,](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md)Registrierungseinträgen oder .ini-Dateieinträgen beschriebene Methode.

 

 

 



