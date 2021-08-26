---
description: Die Funktionen OpenEventLog, OpenBackupEventLog, RegisterEventSource, DeregisterEventSource und CloseEventLog öffnen und schließen Ereignisprotokollhandles.
ms.assetid: e42a66c2-2f1e-46f8-99c7-4701075c8ec3
title: Ereignisprotokollierungsvorgänge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 221218bdfa4fc5e4fc6a905353cde33357c4088119031062c074c75d4b8136dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901418"
---
# <a name="event-logging-operations"></a>Ereignisprotokollierungsvorgänge

Die [**Funktionen OpenEventLog,**](/windows/desktop/api/Winbase/nf-winbase-openeventloga) [**OpenBackupEventLog,**](/windows/desktop/api/Winbase/nf-winbase-openbackupeventloga) [**RegisterEventSource,**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea) [**DeregisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-deregistereventsource)und [**CloseEventLog**](/windows/desktop/api/Winbase/nf-winbase-closeeventlog) öffnen und schließen Ereignisprotokollhandles.

Die folgende Tabelle zeigt die Vorgänge, die für ein geöffnetes Ereignisprotokoll ausgeführt werden können, und die entsprechende Funktion für jeden Vorgang.



| Vorgang | Funktion                                                                                                                     |
|-----------|------------------------------------------------------------------------------------------------------------------------------|
| Backup    | [**BackupEventLog**](/windows/desktop/api/Winbase/nf-winbase-backupeventloga)                                                                                     |
| Löschen     | [**ClearEventLog**](/windows/desktop/api/Winbase/nf-winbase-cleareventloga)                                                                                       |
| Überwachen   | [**NotifyChangeEventLog**](/windows/desktop/api/Winbase/nf-winbase-notifychangeeventlog)                                                                         |
| Abfrage     | [**GetOldestEventLogRecord**](/windows/desktop/api/Winbase/nf-winbase-getoldesteventlogrecord), [ **GetNumberOfEventLogRecords**](/windows/desktop/api/Winbase/nf-winbase-getnumberofeventlogrecords) |
| Überwachungsdaten      | [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga)                                                                                         |
| Schreiben     | [**ReportEvent**](/windows/desktop/api/Winbase/nf-winbase-reporteventa)                                                                                           |



 

Die [**Funktionen OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga) und [**ReportEvent**](/windows/desktop/api/Winbase/nf-winbase-reporteventa) verwenden einen optionalen Servernamen als Parameter, damit die Vorgänge auf dem Remoteserver ausgeführt werden können. Verwenden [**Sie OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga) zum Lesen oder Ausführen administrativer Vorgänge (Sichern, Löschen, Überwachen und Abfragen) im Protokoll, und verwenden Sie [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea) zum Schreiben in das Protokoll.

Jeder Aufruf einer Ereignisprotokollierungsfunktion ist ein atomarer Vorgang. Beim Lesen aus dem Ereignisprotokoll werden nur ganze Ereignisdatensätze zurückgegeben. Wenn Sie in das Ereignisprotokoll schreiben, wird jeder Ereignisdatensatz garantiert sequenziell als vollständiger Datensatz im Protokoll geschrieben. In der folgenden Liste wird beschrieben, wie der Ereignisprotokollierungsdienst besondere Bedingungen behandelt:

-   Der Ereignisprotokollierungsdienst empfängt gleichzeitig einen Lese- und einen Schreibvorgang: Wenn sich die Leseposition am Ende der Datei befindet, schlägt der Lesevorgang mit dem Status "Dateiende" fehl (wenn der Schreibvorgang nicht abgeschlossen wurde) oder gibt den neuen Datensatz zurück (wenn der Schreibvorgang abgeschlossen wurde).
-   Der Ereignisprotokollierungsdienst schließt einen eindeutigen Vorgang ab, bevor ein Lesevorgang empfangen wird: Der Lesevorgang schlägt mit dem Status "Dateiende" fehl.
-   Der Ereignisprotokollierungsdienst schließt einen eindeutigen Vorgang ab, bevor er einen Schreibvorgang empfängt: Der Clear-Vorgang schneide das Protokoll ab, dann fügt der Schreibvorgang den neuen Datensatz am Anfang des Protokolls hinzu.

 

 



