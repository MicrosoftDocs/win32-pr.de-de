---
description: Programmierer, die Windows Update-Agent (WUA) verwenden, fügen zunächst einen Verweis auf Wuapi.dll zu Ihrem aktuellen Projekt (in Visual C++, Microsoft Visual Basic oder C \# ) oder durch Verweisen auf "wuapi. h" und "wuguid. lib" in einem C-oder C++-Projekt hinzu.
ms.assetid: ec9cbb0b-b5d4-41f2-8a25-143130d08a3b
title: Windows Update-Agent-Objektmodell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5060a76c850ea9ad97e9132f661d4b64f4f4fd03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104561413"
---
# <a name="windows-update-agent-object-model"></a>Windows Update-Agent-Objektmodell

Programmierer, die Windows Update-Agent (WUA) verwenden, fügen zunächst einen Verweis auf Wuapi.dll zu Ihrem aktuellen Projekt (in Visual C++, Microsoft Visual Basic oder C \# ) oder durch Verweisen auf "wuapi. h" und "wuguid. lib" in einem C-oder C++-Projekt hinzu. Der erste Schritt bei der Verwendung der WUA-API besteht darin, eine Instanz einer der Schnittstellen zu erstellen, indem ein Objekt aus der entsprechenden Co-Klasse erstellt wird.

In der folgenden Abbildung wird das WUA-Objektmodell beschrieben. Weitere Informationen finden Sie im Abschnitt "[WUA-Objekte und zugehörige Aufgaben](#wua-objects-and-associated-tasks)". Eine vollständige Liste aller WUA-Schnittstellen finden Sie unter [Schnittstellen](interfaces.md).

![Windows Update-Agent-Objektmodell](images/wua-object-model.png)

## <a name="wua-objects-and-associated-tasks"></a>WUA-Objekte und zugehörige Aufgaben

In der folgenden Tabelle sind die WUA-Objekte und die typischen Aufgaben aufgeführt, die den WUA-Objekten zugeordnet sind.



| Object                                                                | BESCHREIBUNG                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AutomaticUpdates**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdates)                         | Starten, anhalten oder fortsetzen automatische Updates.                                                                                                                                                                                                  |
| [**Automaticupdatessettings**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings)         | Ruft den Tag und die Uhrzeit zum Installieren von Updates ab oder legt Sie fest. Geben Sie an, wie Benutzer über ein automatische Updates Ereignis benachrichtigt werden.                                                                                                                          |
| [**Kategorie**](/windows/desktop/api/Wuapi/nn-wuapi-icategory)                                         | Abrufen von Informationen über die Kategorie des Updates, einschließlich Name, ID, Beschreibung, Besitzer und beabsichtigter Produkt. Ruft eine Sammlung von Updates ab, die zu dieser Kategorie gehören. Ruft eine Auflistung der übergeordneten oder untergeordneten Kategorien ab. |
| [**Categorycollection**](/windows/desktop/api/Wuapi/nn-wuapi-icategorycollection)                     | Greifen Sie auf eine Auflistung von kategorieobjekten zu.                                                                                                                                                                                                    |
| [**Download Ergebnis**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadresult)                             | Abrufen von Informationen über das Ergebnis eines Downloads.                                                                                                                                                                                        |
| [**Installationresult**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationresult)                     | Abrufen von Informationen über das Ergebnis einer Installation oder einer Neuinstallation. Stellen Sie fest, ob ein Systemneustart erforderlich ist, um die Installation oder die Installation abzuschließen.                                                                  |
| [**SearchResult**](/windows/desktop/api/Wuapi/nn-wuapi-isearchresult)                                 | Abrufen von Informationen über das Ergebnis einer Suche nach Kategorien oder Updates. Ruft eine Auflistung der Kategorien ab, die auf dem Zielcomputer durch die Suche gefunden wurden. Ruft eine Sammlung von Updates ab, die von der Suche gefunden wurden.                     |
| [**System Information**](/windows/desktop/api/Wuapi/nn-wuapi-isysteminformation)                       | Abrufen von Informationen zu OEM-Hardware-und Systemneustart Anforderungen auf dem Zielcomputer.                                                                                                                                        |
| [**Aktualisieren**](/windows/desktop/api/Wuapi/nn-wuapi-iupdate)                                             | Rufen Sie die meisten Informationen zum Update ab, einschließlich gebündelte Updates, Quell Anforderungen, Identität, Beschreibung, Deinstallations Optionen, Download Priorität, Größe und Stichtag.                                                                |
| [**Updatecollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatecollection)                         | Greifen Sie auf eine Auflistung von Update Objekten zu.                                                                                                                                                                                                      |
| [**Updatedownloader**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloader)                         | Starten Sie einen asynchronen oder synchronen Download der Dateien, die mit den Updates verknüpft sind.                                                                                                                                            |
| [**Updatedownloadresult**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloadresult)                 | Abrufen von Informationen zum Ergebnis des Downloads für ein Update.                                                                                                                                                                       |
| [**UpdateException**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateexception)                           | Abrufen der Beschreibung und des Kontexts einer Ausnahme, die beim Auftreten eines Update Fehlers ausgelöst wird.                                                                                                                                            |
| [**Updateexceptioncollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateexceptioncollection)       | Greifen Sie auf eine Auflistung von UpdateException-Objekten zu.                                                                                                                                                                                             |
| [**Updatehistoryentry**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatehistoryentry)                     | Abrufen von Informationen über ein installiertes oder deinstalliertes Update, einschließlich der verarbeiteten Anwendung, des Datums und der Beschreibung.                                                                                                    |
| [**Updatehistoryentrycollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatehistoryentrycollection) | Greifen Sie auf eine Auflistung von updatehistoryentry-Objekten zu.                                                                                                                                                                                          |
| [**Updateingestallationresult**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstallationresult)         | Abrufen von Informationen über das Ergebnis der Installation oder der Deinstallation für ein Update.                                                                                                                                                  |
| [**Updateingestaller**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstaller)                           | Startet eine asynchrone oder synchrone Installation oder die Installation eines Updates. Starten Sie eine interaktive Dialog Sequenz, um den Benutzer durch die Schritte zum Installieren von Updates zu leiten.                                                              |
| [**Updatesearcher**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher)                             | Sucht nach Updates auf dem Server nach Kriterien wie dem Updatetyp, der ID oder der Kategorie.                                                                                                                                            |
| [**Verbindung**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession)                               | Starten Sie eine Sitzung, um die Updates für eine Anwendung zu suchen, herunterzuladen, zu installieren oder zu deinstallieren.                                                                                                                                                  |
| [**WebProxy**](/windows/desktop/api/Wuapi/nn-wuapi-iwebproxy)                                         | Abrufen und Festlegen von http-Proxy Einstellungen                                                                                                                                                                                                       |



 

 

 



