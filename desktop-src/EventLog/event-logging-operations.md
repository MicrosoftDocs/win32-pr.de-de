---
description: Die Funktionen "OpenEventLog", "openbackupeer ventlog", "registereventsource", "deregistereventsource" und "closeeventlog" öffnen und schließen Ereignisprotokoll Handles.
ms.assetid: e42a66c2-2f1e-46f8-99c7-4701075c8ec3
title: Ereignis Protokollierungs Vorgänge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 065acd268788de8c9674baa1fe47a3b89a719d4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106355654"
---
# <a name="event-logging-operations"></a>Ereignis Protokollierungs Vorgänge

Die Funktionen " [**OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga)", " [**openbackupeer ventlog**](/windows/desktop/api/Winbase/nf-winbase-openbackupeventloga)", " [**registereventsource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea)", " [**deregistereventsource**](/windows/desktop/api/Winbase/nf-winbase-deregistereventsource)" und " [**closeeventlog**](/windows/desktop/api/Winbase/nf-winbase-closeeventlog) " öffnen und schließen Ereignisprotokoll Handles.

In der folgenden Tabelle werden die Vorgänge, die für ein offenes Ereignisprotokoll ausgeführt werden können, und die entsprechende Funktion für jeden Vorgang angezeigt.



| Vorgang | Funktion                                                                                                                     |
|-----------|------------------------------------------------------------------------------------------------------------------------------|
| Backup    | [**Backupeer-Protokoll**](/windows/desktop/api/Winbase/nf-winbase-backupeventloga)                                                                                     |
| Clear     | [**Cleareventlog**](/windows/desktop/api/Winbase/nf-winbase-cleareventloga)                                                                                       |
| Monitor   | [**Notifychangeeventlog**](/windows/desktop/api/Winbase/nf-winbase-notifychangeeventlog)                                                                         |
| Abfrage     | [**Getoldesteventlogrecord**](/windows/desktop/api/Winbase/nf-winbase-getoldesteventlogrecord), [ **getnumofeventlogrecords**](/windows/desktop/api/Winbase/nf-winbase-getnumberofeventlogrecords) |
| Lesen      | [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga)                                                                                         |
| Schreiben     | [**ReportEvent**](/windows/desktop/api/Winbase/nf-winbase-reporteventa)                                                                                           |



 

Die Funktionen " [**OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga) " und "Report [**Event**](/windows/desktop/api/Winbase/nf-winbase-reporteventa) " akzeptieren einen optionalen Servernamen als Parameter, sodass die Vorgänge auf dem Remote Server ausgeführt werden können. Verwenden Sie [**OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga) zum Lesen oder Ausführen administrativer Vorgänge (sichern, löschen, überwachen und Abfragen) im Protokoll, und verwenden Sie [**registereventsource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea) zum Schreiben in das Protokoll.

Jeder aufzurufende Ereignis Protokollierungsfunktion ist ein atomarer Vorgang. Wenn Sie aus dem Ereignisprotokoll lesen, werden nur ganze Ereignisdaten Sätze zurückgegeben. Wenn Sie in das Ereignisprotokoll schreiben, wird sichergestellt, dass jeder Ereignisdaten Satz sequenziell als ein kompletter Datensatz im Protokoll geschrieben wird. In der folgenden Liste wird beschrieben, wie der Ereignis Protokollierungs Dienst besondere Bedingungen behandelt:

-   Der Ereignis Protokollierungs Dienst empfängt gleichzeitig einen Lesevorgang und einen Schreibvorgang: Wenn sich die Lese Position am Ende der Datei befindet, schlägt entweder der Lesevorgang mit dem Status "Dateiende" fehl (wenn der Schreibvorgang nicht abgeschlossen wurde), oder er gibt den neuen Datensatz zurück (wenn der Schreibvorgang abgeschlossen wurde).
-   Der Ereignis Protokollierungs Dienst schließt einen Löschvorgang ab, bevor ein Lesevorgang empfangen wird: der Lesevorgang schlägt mit dem Status "Dateiende" fehl.
-   Der Ereignis Protokollierungs Dienst schließt einen Löschvorgang ab, bevor ein Schreibvorgang empfangen wird: der Löschvorgang verkürzt das Protokoll, und der neue Datensatz wird am Anfang des Protokolls durch den Schreibvorgang hinzugefügt.

 

 



