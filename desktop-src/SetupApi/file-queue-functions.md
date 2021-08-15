---
description: Die folgenden Funktionen werden mit Dateiwarteschlangen verwendet.
ms.assetid: f05e2abf-983f-4418-bf92-f5ca6502196e
title: Dateiwarteschlangenfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a70087bfcc00f2c3d86c93cc62081adc9aa50705d248d79a524435c95f480562
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118887079"
---
# <a name="file-queue-functions"></a>Dateiwarteschlangenfunktionen

Die folgenden Funktionen werden mit Dateiwarteschlangen verwendet.



| Funktion                                                             | BESCHREIBUNG                                                                                           |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**SetupCloseFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue)                   | Beendet die Warteschlange. Für alle verbleibenden Transaktionen wird kein Commit ausgeführt.                                   |
| [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)                 | Committet alle Transaktionen in der Warteschlange.                                                                      |
| [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue)                     | Initialisiert ein Handle für die Dateiwarteschlange und gibt es zurück.                                                   |
| [**SetupPromptReboot**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptreboot)                       | Fordert den Benutzer auf, seinen Computer bei Bedarf neu zu starten.                                         |
| [**SetupQueueCopy**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopya)                             | Reiht eine Dateikopie in die Warteschlange ein.                                                                                   |
| [**SetupQueueCopySection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopysectiona)               | Reiht die Dateien in einem INF-Abschnitt Zum Kopieren von Dateien in die Warteschlange ein.                                                        |
| [**SetupQueueDefaultCopy**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedefaultcopya)               | Reiht die Dateien in einem INF-Abschnitt Zum Kopieren von Dateien in die Warteschlange ein, indem die in einer INF-Datei angegebenen Standardinformationen verwendet werden. |
| [**SetupQueueDelete**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletea)                         | Reiht eine Dateilöschung in die Warteschlange ein.                                                                               |
| [**SetupQueueDeleteSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletesectiona)           | Reiht die Dateien in einem INF-Abschnitt Dateien löschen in die Warteschlange ein.                                                      |
| [**SetupQueueRename**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamea)                         | Reiht eine Datei-Umbenennung in die Warteschlange ein.                                                                                 |
| [**SetupQueueRenameSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamesectiona)           | Reiht die Dateien in einem INF-Abschnitt Dateien umbenennen in die Warteschlange ein.                                                      |
| [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea)                     | Überprüft die Dateiwarteschlange.                                                                                 |
| [**SetupSetPlatformPathOverride**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetplatformpathoverridea) | Legt die Plattformpfadüberschreibung fest.                                                                      |



 

 

 



