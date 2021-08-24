---
description: Programmierer, die Windows Update-Agent (WUA) verwenden, beginnen mit dem Hinzufügen eines Verweises auf Wuapi.dll zu ihrem aktuellen Projekt (in Visual C++, Microsoft Visual Basic oder \# C) oder indem sie in einem C- oder C++-Projekt auf Wuapi.h und Wuguid.lib verweisen.
ms.assetid: ec9cbb0b-b5d4-41f2-8a25-143130d08a3b
title: Windows Aktualisieren des Agent-Objektmodells
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e32b60f9306dfae5910418ddc07353a421e0325c0953fb1f47994ad007ded5ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119855445"
---
# <a name="windows-update-agent-object-model"></a>Windows Aktualisieren des Agent-Objektmodells

Programmierer, die Windows Update-Agent (WUA) verwenden, beginnen mit dem Hinzufügen eines Verweises auf Wuapi.dll zu ihrem aktuellen Projekt (in Visual C++, Microsoft Visual Basic oder \# C) oder indem sie in einem C- oder C++-Projekt auf Wuapi.h und Wuguid.lib verweisen. Der erste Schritt bei der Verwendung der WUA-API besteht darin, eine Instanz einer der Schnittstellen zu erstellen, indem ein Objekt aus der entsprechenden Co-Klasse erstellt wird.

In der folgenden Abbildung wird das WUA-Objektmodell beschrieben. Weitere Informationen finden Sie im Abschnitt["WUA-Objekte und zugeordnete Aufgaben".](#wua-objects-and-associated-tasks) Eine vollständige Liste aller WUA-Schnittstellen finden Sie unter [Schnittstellen.](interfaces.md)

![Windows Update-Agent-Objektmodell](images/wua-object-model.png)

## <a name="wua-objects-and-associated-tasks"></a>WUA-Objekte und zugeordnete Aufgaben

In der folgenden Tabelle sind die WUA-Objekte und die typischen Aufgaben aufgeführt, die den WUA-Objekten zugeordnet sind.



| Object                                                                | BESCHREIBUNG                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AutomaticUpdates**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdates)                         | Starten, Anhalten oder Fortsetzen Automatische Updates.                                                                                                                                                                                                  |
| [**AutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings)         | Ruft den Tag und die Uhrzeit für die Installation von Updates ab oder legt diese fest. Geben Sie an, wie Benutzer über ein Automatische Updates Ereignis benachrichtigt werden.                                                                                                                          |
| [**Kategorie**](/windows/desktop/api/Wuapi/nn-wuapi-icategory)                                         | Rufen Sie Informationen zur Kategorie des Updates ab, einschließlich Name, ID, Beschreibung, Besitzer und beabsichtigtes Produkt. Ruft eine Auflistung von Updates ab, die zu dieser Kategorie gehören. Ruft eine Auflistung der übergeordneten oder untergeordneten Kategorien ab. |
| [**CategoryCollection**](/windows/desktop/api/Wuapi/nn-wuapi-icategorycollection)                     | Greifen Sie auf eine Auflistung von Category-Objekten zu.                                                                                                                                                                                                    |
| [**DownloadResult**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadresult)                             | Rufen Sie Informationen zum Ergebnis eines Downloads ab.                                                                                                                                                                                        |
| [**InstallationResult**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationresult)                     | Rufen Sie Informationen zum Ergebnis einer Installation oder Deinstallation ab. Bestimmen Sie, ob ein Systemneustart erforderlich ist, um die Installation oder Deinstallation abzuschließen.                                                                  |
| [**Searchresult**](/windows/desktop/api/Wuapi/nn-wuapi-isearchresult)                                 | Abrufen von Informationen über das Ergebnis einer Suche nach Kategorien oder Updates. Rufen Sie eine Auflistung von Kategorien ab, die auf dem Zielcomputer durch die Suche gefunden wurden. Ruft eine Auflistung von Updates ab, die von der Suche gefunden wurden.                     |
| [**SystemInformation**](/windows/desktop/api/Wuapi/nn-wuapi-isysteminformation)                       | Abrufen von Informationen zu OEM-Hardware- und Systemneustartanforderungen auf dem Zielcomputer.                                                                                                                                        |
| [**Aktualisieren**](/windows/desktop/api/Wuapi/nn-wuapi-iupdate)                                             | Rufen Sie die meisten Informationen zum Update ab, einschließlich gebündelter Updates, Quellanforderungen, Identität, Beschreibung, Deinstallationsoptionen, Downloadpriorität, Größe und Stichtag.                                                                |
| [**UpdateCollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatecollection)                         | Greifen Sie auf eine Auflistung von Updateobjekten zu.                                                                                                                                                                                                      |
| [**UpdateDownloader**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloader)                         | Starten Sie einen asynchronen oder synchronen Download der Dateien, die den Updates zugeordnet sind.                                                                                                                                            |
| [**UpdateDownloadResult**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloadresult)                 | Rufen Sie Informationen zum Ergebnis des Downloads für ein Update ab.                                                                                                                                                                       |
| [**Updateexception**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateexception)                           | Rufen Sie die Beschreibung und den Kontext einer Ausnahme ab, die ausgelöst wird, wenn ein Updatefehler auftritt.                                                                                                                                            |
| [**UpdateExceptionCollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateexceptioncollection)       | Greifen Sie auf eine Auflistung von UpdateException-Objekten zu.                                                                                                                                                                                             |
| [**UpdateHistoryEntry**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatehistoryentry)                     | Rufen Sie Informationen zu einem Update ab, das installiert oder deinstalliert wurde, einschließlich der verarbeiteten Anwendung, des Datums und der Beschreibung.                                                                                                    |
| [**UpdateHistoryEntryCollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatehistoryentrycollection) | Greifen Sie auf eine Auflistung von UpdateHistoryEntry-Objekten zu.                                                                                                                                                                                          |
| [**UpdateInstallationResult**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstallationresult)         | Rufen Sie Informationen zum Ergebnis der Installation oder Deinstallation für ein Update ab.                                                                                                                                                  |
| [**UpdateInstaller**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstaller)                           | Starten Sie eine asynchrone oder synchrone Installation oder Deinstallation eines Updates. Starten Sie eine interaktive Dialogsequenz, um den Benutzer durch die Schritte zum Installieren von Updates zu führen.                                                              |
| [**UpdateSearcher**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher)                             | Sucht nach Updates auf dem Server anhand von Kriterien wie dem Updatetyp, der ID oder der Kategorie.                                                                                                                                            |
| [**UpdateSession**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession)                               | Starten Sie eine Sitzung, um die Updates für eine Anwendung zu suchen, herunterzuladen, zu installieren oder zu deinstallieren.                                                                                                                                                  |
| [**Webproxy**](/windows/desktop/api/Wuapi/nn-wuapi-iwebproxy)                                         | Rufen Sie HTTP-Proxyeinstellungen ab, und legen Sie sie fest.                                                                                                                                                                                                       |



 

 

 



