---
description: Die folgenden Funktionen werden mit der Speicherplatz Liste verwendet.
ms.assetid: 18693b2d-6b0f-4f9c-b3cf-e50c36e2f2e1
title: Funktionen der Disk-Space Liste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f520cc7a3ddcd0b12b27bd11768a95231a8ed4b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346518"
---
# <a name="disk-space-list-functions"></a>Funktionen der Disk-Space Liste

Die folgenden Funktionen werden mit der Speicherplatz Liste verwendet.



| Funktion                                                                                         | BESCHREIBUNG                                                                                                                          |
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [**Setupdandiskspacelist**](/windows/desktop/api/Setupapi/nf-setupapi-setupadjustdiskspacelista)                                     | Passt den erforderlichen Speicherplatz für ein bestimmtes Laufwerk an.                                                                          |
| [**Setupkreatediskspacelist**](/windows/desktop/api/Setupapi/nf-setupapi-setupcreatediskspacelista)                                     | Erstellt eine Speicherplatz Liste und weist ihr Ressourcen zu.                                                                             |
| [**Setupdestroydiskspacelist**](/windows/desktop/api/Setupapi/nf-setupapi-setupdestroydiskspacelist)                                   | Zerstört eine Speicherplatz Liste und gibt die zugeordneten Ressourcen frei.                                                                   |
| [**Setupduplicatediskspacelist**](/windows/desktop/api/Setupapi/nf-setupapi-setupduplicatediskspacelista)                               | Dupliziert eine Speicherplatz Liste als neue unabhängige Speicherplatz Liste.                                                                   |
| [**Setupquerydrivesindiskspacelist**](/windows/desktop/api/Setupapi/nf-setupapi-setupquerydrivesindiskspacelista)                       | Füllt einen Puffer mit den Laufwerk Spezifikationen für alle Laufwerke aus, die in der Liste der Speicherplätze aufgeführt sind.                                       |
| [**Setupqueryspacerequiredon-Laufwerk**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryspacerequiredondrivea)                         | Gibt die Gesamtmenge des Speicherplatzes zurück, der zum Ausführen der Datei Vorgänge auf einem bestimmten Laufwerk erforderlich ist, das in der Speicherplatz Liste aufgeführt ist. |
| [**Setupaddabdiskspacelist**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddtodiskspacelista)                                       | Fügt der Speicherplatz Liste einen Kopier-oder Löschvorgang für Dateien hinzu.                                                                         |
| [**Setupaddsectionabdiskspacelist**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddsectiontodiskspacelista)                         | Fügt alle Datei Vorgänge im Abschnitt **Kopieren von Dateien** oder **Löschen von Dateien** einer INF-Datei einer Speicherplatz Liste hinzu.                    |
| [**Setupaddinstallsectionzu diskspacelist**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddinstallsectiontodiskspacelista)           | Fügt alle Datei Vorgänge in einem **Installations** Abschnitt einer INF-Datei der Speicherplatz Liste hinzu.                                        |
| [**Setupremuvefromdiskspacelist**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefromdiskspacelista)                             | Entfernt einen Datei Kopier-oder Löschvorgang aus einer Speicherplatz Liste.                                                                      |
| [**Setupremuvesectionfromdiskspacelist**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovesectionfromdiskspacelista)               | Entfernt alle Datei Vorgänge im Abschnitt **Kopieren von Dateien** oder **Löschen von Dateien** einer INF-Datei aus einer Speicherplatz Liste.               |
| [**SetupRemoveInstallSectionFromDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremoveinstallsectionfromdiskspacelista) | Entfernt alle Datei Vorgänge im **Installations** Abschnitt einer INF-Datei aus der Speicherplatz Liste.                                  |



 

 

 



