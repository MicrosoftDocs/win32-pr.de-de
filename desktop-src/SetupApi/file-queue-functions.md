---
description: Die folgenden Funktionen werden bei Datei Warteschlangen verwendet.
ms.assetid: f05e2abf-983f-4418-bf92-f5ca6502196e
title: Datei Warteschlangen Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9acaf1fb1fbd2dc4f020577a1ae68d6ec9b2e95c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347475"
---
# <a name="file-queue-functions"></a>Datei Warteschlangen Funktionen

Die folgenden Funktionen werden bei Datei Warteschlangen verwendet.



| Funktion                                                             | BESCHREIBUNG                                                                                           |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**Setupclosefilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue)                   | Beendet die Warteschlange. Für alle verbleibenden Transaktionen wird kein Commit ausgeführt.                                   |
| [**Setupcommitfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)                 | Führt einen Commit für alle Transaktionen in der Warteschlange                                                                      |
| [**Setupopeinfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue)                     | Initialisiert und gibt ein Handle für die Datei Warteschlange zurück.                                                   |
| [**Setuppromptreboot**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptreboot)                       | Fordert den Benutzer auf, seinen Computer ggf. neu zu starten.                                         |
| [**Setupqueuecopy**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopya)                             | Fügt eine Dateikopie in die Warteschlange                                                                                   |
| [**Setupqueuecopysection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopysectiona)               | Fügt die Dateien in eine Warteschlange für den INF-Kopiervorgang ein.                                                        |
| [**Setupqueuedefaultcopy**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedefaultcopya)               | Fügt die Dateien in einer INF-Datei mit den in einer INF-Datei angegebenen Standardinformationen in die Warteschlange ein. |
| [**Setupqueuedelete**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletea)                         | Fügt eine Datei Löschung in die Warteschlange                                                                               |
| [**Setupqueuedeletesection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletesectiona)           | Fügt die Dateien in einen INF-Abschnitt zum Löschen von Dateien ein.                                                      |
| [**Setupqueuerename**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamea)                         | Fügt eine Datei Umbenennung in die Warteschlange                                                                                 |
| [**Setupqueuerenamesection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamesectiona)           | Fügt die Dateien in einen INF-Abschnitt zum Umbenennen von Dateien ein.                                                      |
| [**Setupscanfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea)                     | Scannt die Datei Warteschlange.                                                                                 |
| [**Setupsetplatformpathoverride**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetplatformpathoverridea) | Legt die Platt Form Pfad Überschreibung fest.                                                                      |



 

 

 



