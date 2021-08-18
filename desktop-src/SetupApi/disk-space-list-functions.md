---
description: Die folgenden Funktionen werden mit der Liste des Speicherplatzes verwendet.
ms.assetid: 18693b2d-6b0f-4f9c-b3cf-e50c36e2f2e1
title: Disk-Space List-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e20e6f656110cc3b8c2ebd607f28b5d701ce3007b4ce8812f7e3bcad2f7f5b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118887366"
---
# <a name="disk-space-list-functions"></a>Disk-Space List-Funktionen

Die folgenden Funktionen werden mit der Liste des Speicherplatzes verwendet.



| Funktion                                                                                         | BESCHREIBUNG                                                                                                                          |
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [**SetupAdjustDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupadjustdiskspacelista)                                     | Passt den erforderlichen Speicherplatz für ein angegebenes Laufwerk an.                                                                          |
| [**SetupCreateDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupcreatediskspacelista)                                     | Erstellt eine Liste mit Speicherplatz und ordnet ihr Ressourcen zu.                                                                             |
| [**SetupDestroyDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupdestroydiskspacelist)                                   | Zerstört eine Liste mit Speicherplatz und gibt die zugeordneten Ressourcen frei.                                                                   |
| [**SetupDuplicateDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupduplicatediskspacelista)                               | Dupliziert eine Liste mit Speicherplatz als neue unabhängige Liste mit Speicherplatz.                                                                   |
| [**SetupQueryDrivesInDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupquerydrivesindiskspacelista)                       | Füllt einen Puffer mit den Laufwerkspezifikationen für alle Laufwerke aus, die in der Liste speicherplatzaufgelistet sind.                                       |
| [**SetupQuerySpaceRequiredOnDrive**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryspacerequiredondrivea)                         | Gibt die Gesamtmenge des Speicherplatzes zurück, der zum Abschließen der Dateivorgänge auf einem bestimmten Laufwerk erforderlich ist, das in der Liste speicherplatzaufgelistet ist. |
| [**SetupAddToDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddtodiskspacelista)                                       | Fügt der Speicherplatzliste einen Dateikopier- oder Löschvorgang hinzu.                                                                         |
| [**SetupAddSectionToDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddsectiontodiskspacelista)                         | Fügt einer Liste mit Speicherplatz alle Dateivorgänge in einem Abschnitt **Dateien kopieren** oder **Dateien löschen** einer INF-Datei hinzu.                    |
| [**SetupAddInstallSectionToDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddinstallsectiontodiskspacelista)           | Fügt der Liste des Speicherplatzes alle Dateivorgänge in einem **Installationsabschnitt** einer INF-Datei hinzu.                                        |
| [**SetupRemoveFromDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefromdiskspacelista)                             | Entfernt einen Dateikopier- oder Löschvorgang aus einer Liste mit Speicherplatz.                                                                      |
| [**SetupRemoveSectionFromDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovesectionfromdiskspacelista)               | Entfernt alle Dateivorgänge in einem Abschnitt **"Dateien kopieren"** oder **"Dateien löschen"** einer INF-Datei aus einer Liste mit Speicherplatz.               |
| [**SetupRemoveInstallSectionFromDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremoveinstallsectionfromdiskspacelista) | Entfernt alle Dateivorgänge im Abschnitt **Installieren** einer INF-Datei aus der Liste des Speicherplatzes.                                  |



 

 

 



