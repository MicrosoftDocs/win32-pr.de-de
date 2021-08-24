---
description: Die folgenden Funktionen werden mit der Ereignisprotokollierung verwendet.
ms.assetid: fd5c12ec-3a3d-4b75-a573-0b27ae7a890b
title: Ereignisprotokollierungsfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf6ba5e43286a65b9d3456edc9cd80e8812bd9a32975ec63158c0717b41c6894
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069590"
---
# <a name="event-logging-functions"></a>Ereignisprotokollierungsfunktionen

Die folgenden Funktionen werden mit der Ereignisprotokollierung verwendet.



| Funktion                                                         | Beschreibung                                                                                         |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**BackupEventLog**](/windows/desktop/api/Winbase/nf-winbase-backupeventloga)                         | Speichert das angegebene Ereignisprotokoll in einer Sicherungsdatei.                                                     |
| [**ClearEventLog**](/windows/desktop/api/Winbase/nf-winbase-cleareventloga)                           | Clears the specified event log, and optional speichert die aktuelle Kopie des Protokolls in einer Sicherungsdatei.  |
| [**CloseEventLog**](/windows/desktop/api/Winbase/nf-winbase-closeeventlog)                           | Schließt ein Lesehandles für das angegebene Ereignisprotokoll.                                                    |
| [**DeregisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-deregistereventsource)           | Schließt ein Schreibhand handle für das angegebene Ereignisprotokoll.                                                   |
| [**GetEventLogInformation**](/windows/desktop/api/Winbase/nf-winbase-geteventloginformation)         | Ruft Informationen zum angegebenen Ereignisprotokoll ab.                                                |
| [**GetNumberOfEventLogRecords**](/windows/desktop/api/Winbase/nf-winbase-getnumberofeventlogrecords) | Ruft die Anzahl der Datensätze im angegebenen Ereignisprotokoll ab.                                         |
| [**GetOldestEventLogRecord**](/windows/desktop/api/Winbase/nf-winbase-getoldesteventlogrecord)       | Ruft die absolute Datensatznummer des ältesten Datensatzes im angegebenen Ereignisprotokoll ab.               |
| [**NotifyChangeEventLog**](/windows/desktop/api/Winbase/nf-winbase-notifychangeeventlog)             | Ermöglicht es einer Anwendung, Benachrichtigungen zu empfangen, wenn ein Ereignis in das angegebene Ereignisprotokoll geschrieben wird. |
| [**OpenBackupEventLog**](/windows/desktop/api/Winbase/nf-winbase-openbackupeventloga)                 | Öffnet ein Handle für ein Sicherungsereignisprotokoll.                                                               |
| [**OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga)                             | Öffnet ein Handle für das angegebene Ereignisprotokoll.                                                          |
| [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga)                             | Liest eine ganze Anzahl von Einträgen aus dem angegebenen Ereignisprotokoll.                                       |
| [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea)               | Ruft ein registriertes Handle für das angegebene Ereignisprotokoll ab.                                           |
| [**ReportEvent**](/windows/desktop/api/Winbase/nf-winbase-reporteventa)                               | Schreibt einen Eintrag am Ende des angegebenen Ereignisprotokolls.                                              |



 

 

 



