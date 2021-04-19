---
description: Wenn Sie nach dem Ausführen einer Installation sicherstellen müssen, dass eine bestimmte Funktion, Komponente oder Datei installiert ist, aktivieren Sie während der Installation die Option ausführliche Protokollierung. Siehe Windows Installer Protokollierung und Befehlszeilenoptionen.
ms.assetid: c4547e5d-ea71-494f-9d92-c7fef23bcc0f
title: Überprüfen der Installation von Features, Komponenten, Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7cab15b4f0590ee5613865d4b7c21439eec6dbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348340"
---
# <a name="checking-the-installation-of-features-components-files"></a>Überprüfen der Installation von Features, Komponenten, Dateien

Wenn Sie nach dem Ausführen einer Installation sicherstellen müssen, dass eine bestimmte Funktion, Komponente oder Datei installiert ist, aktivieren Sie während der Installation die Option ausführliche Protokollierung. Siehe [Windows Installer Protokollierung](windows-installer-logging.md) und [Befehlszeilenoptionen](command-line-options.md).

Das ausführliche Protokoll enthält einen Eintrag für jedes Feature und jede Komponente, die das Installationspaket installieren kann. Das Protokoll gibt Aufschluss über den Status dieses Features oder der Komponente vor der Installation, den Zustand, der von der Installation angefordert wurde, und den Zustand, in dem das Installationsprogramm die Funktion oder Komponente verlassen hat. In den folgenden Beispielen werden Funktions-und Komponenten Einträge im Protokoll angezeigt.

``` syntax
MSI (s) (40:A4): Feature: QuickTest; Installed: Absent;   Request:
 Local;   Action: Local
MSI (s) (40:A4): Component: QuickTest; Installed: Absent;   Request:
 Local;   Action: Local
```

Dieses ausführliche Protokoll zeigt Folgendes an:

-   der Installationsstatus des Schnelltest Features und der Komponente waren vor dem Ausführen des Pakets nicht vorhanden.
-   das Paket hat eine lokale Installation angefordert.
-   die Funktion und die Komponente wurden nach dem Ausführen des Pakets beide im lokal installierten Zustand belassen.

Die im Protokoll installierte Bezeichnung bezieht sich auf den aktuellen Installationsstatus des Features oder der Komponente, "Request" bezieht sich auf den angeforderten Installationsstatus des Features oder der Komponente. "Action" bezieht sich auf den tatsächlichen Aktionszustand des Features oder der Komponente.

In der folgenden Tabelle sind die möglichen Komponenten-oder Featurezustände aufgelistet, die im Protokoll angezeigt werden können.



| Protokolleintrag              | BESCHREIBUNG                                                                                                     |
|------------------------|-----------------------------------------------------------------------------------------------------------------|
| Anforderung: NULL          | Keine Anforderung.                                                                                                     |
| Aktion: NULL           | Es wurde keine Aktion ausgeführt.                                                                                                |
| Installiert: nicht vorhanden      | Die Komponente oder das Feature ist zurzeit nicht installiert.                                                                |
| Anforderung: nicht vorhanden        | Die Komponente oder das Feature der Installationsanforderungen muss deinstalliert werden.                                                      |
| Aktion: nicht vorhanden         | Der Installer deinstalliert tatsächlich die Komponente oder das Feature.                                                             |
| Installiert: lokal       | Die Komponente oder das Feature ist zurzeit für die lokale Installation installiert.                                                       |
| Anforderung: lokal         | Die Komponente oder das Feature der Installationsanforderungen muss installiert sein, um lokal auszuführen.                                           |
| Aktion: lokal          | Der Installer installiert tatsächlich die Komponente oder das Feature, um lokal auszuführen.                                                  |
| Installiert: Quelle      | Die Komponente oder das Feature ist zurzeit zum Ausführen von der Quelle installiert.                                                 |
| Angefordert: Quelle      | Bei der Installation wird die Installation der Komponente oder des Features von der Quelle angefordert.                                |
| Aktion: Quelle         | Das Installationsprogramm installiert die Komponente oder das Feature, das aus der Quelle ausgeführt werden soll.                                        |
| Installiert: Ankündigung   | Das Feature ist zurzeit angekündigt. Komponenten werden nie angekündigt.                                               |
| Anforderung: ankündigen     | Das Feature "Installationsanforderungen" wird als angekündigte Funktion installiert.                                            |
| Aktion: ankündigen      | Das Installationsprogramm installiert das Feature tatsächlich als angekündigte Funktion.                                               |
| Anforderung: neu installieren     | Das Feature für Installationsanforderungen muss neu installiert werden. Komponenten verwenden den Neuinstallations Status nicht.                            |
| Aktion: neu installieren      | Das Installationsprogramm installiert die Funktion tatsächlich neu.                                                                          |
| Installiert: aktuell     | Das Feature ist zurzeit im standardmäßig erstellten Installations Zustand installiert.                                           |
| Anforderung: aktuell       | Das Installations Anforderungs Feature wird im standardmäßig erstellten Installations Zustand installiert.                               |
| Aktion: aktuell        | Das Installationsprogramm installiert das Feature tatsächlich im standardmäßigen Installations Zustand.                                  |
| Aktion: file missing     | Das Installationsprogramm deinstalliert tatsächlich die Dateien der Komponente und lässt alle anderen Ressourcen der Komponente installiert.      |
| Aktion: hkcrabsent     | Der Installer entfernt tatsächlich die HKCR-Informationen der Komponente. Datei-und nicht-HKCR-Informationen bleiben erhalten.                  |
| Aktion: hkcrfilemissing | Der Installer entfernt tatsächlich die HKCR-Informationen und-Dateien der Komponente. Alle anderen Ressourcen der Komponente bleiben erhalten. |



 

Das ausführliche Protokoll enthält einen Eintrag für jede Datei, die vom Paket installiert werden kann. Das Protokoll gibt Aufschluss darüber, was an der Datei vorgenommen wurde, und bietet eine Erläuterung. Die Datei Einträge im Protokoll werden wie im folgenden Beispiel angezeigt.

``` syntax
MSI (s) (40:A4): File: C:\Test\TESTDB.EXE;  Won't Overwrite;  Existing
 file is of an equal version
```

Dieses Protokoll gibt an, dass das Installationsprogramm die vorhandene Testdb.exe Datei nicht überschreibt, da die vorhandene Datei mit der installierten Version identisch ist.

> [!Note]  
> Wenn Sie ein Installationspaket erstellen müssen, das während der Installation auf dem Computer des Benutzers nach einer vorhandenen Datei oder einem Verzeichnis sucht, verwenden Sie die unter [Suchen nach vorhandenen Anwendungen, Dateien, Registrierungs Einträgen oder INI-Datei Einträgen](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md)beschriebenen Methode.

 

 

 



