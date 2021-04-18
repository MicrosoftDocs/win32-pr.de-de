---
description: Die folgenden Funktionen werden bei der Ereignisprotokollierung verwendet.
ms.assetid: fd5c12ec-3a3d-4b75-a573-0b27ae7a890b
title: Funktionen zur Ereignisprotokollierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 437899684861c5fc7ddbfe98c2499dc07bd9da8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347538"
---
# <a name="event-logging-functions"></a>Funktionen zur Ereignisprotokollierung

Die folgenden Funktionen werden bei der Ereignisprotokollierung verwendet.



| Funktion                                                         | BESCHREIBUNG                                                                                         |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**Backupeer-Protokoll**](/windows/desktop/api/Winbase/nf-winbase-backupeventloga)                         | Speichert das angegebene Ereignisprotokoll in einer Sicherungsdatei.                                                     |
| [**Cleareventlog**](/windows/desktop/api/Winbase/nf-winbase-cleareventloga)                           | Löscht das angegebene Ereignisprotokoll und speichert optional die aktuelle Kopie des Protokolls in einer Sicherungsdatei.  |
| [**Closeeventlog**](/windows/desktop/api/Winbase/nf-winbase-closeeventlog)                           | Schließt ein Lese Handle in das angegebene Ereignisprotokoll.                                                    |
| [**Deregistereventsource**](/windows/desktop/api/Winbase/nf-winbase-deregistereventsource)           | Schließt ein Schreib Handle in das angegebene Ereignisprotokoll.                                                   |
| [**Geteventloginformation**](/windows/desktop/api/Winbase/nf-winbase-geteventloginformation)         | Ruft Informationen zum angegebenen Ereignisprotokoll ab.                                                |
| [**Getnumofeventlogrecords**](/windows/desktop/api/Winbase/nf-winbase-getnumberofeventlogrecords) | Ruft die Anzahl der Datensätze im angegebenen Ereignisprotokoll ab.                                         |
| [**Getoldesteventlogrecord**](/windows/desktop/api/Winbase/nf-winbase-getoldesteventlogrecord)       | Ruft die absolute Datensatznummer des ältesten Datensatzes im angegebenen Ereignisprotokoll ab.               |
| [**Notifychangeeventlog**](/windows/desktop/api/Winbase/nf-winbase-notifychangeeventlog)             | Ermöglicht es einer Anwendung, Benachrichtigungen zu empfangen, wenn ein Ereignis in das angegebene Ereignisprotokoll geschrieben wird. |
| [**Openbackupeer ventlog**](/windows/desktop/api/Winbase/nf-winbase-openbackupeventloga)                 | Öffnet ein Handle für ein Sicherungs Ereignisprotokoll.                                                               |
| [**OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga)                             | Öffnet ein Handle für das angegebene Ereignisprotokoll.                                                          |
| [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga)                             | Liest eine ganze Anzahl von Einträgen aus dem angegebenen Ereignisprotokoll.                                       |
| [**Registereventsource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea)               | Ruft ein registriertes Handle für das angegebene Ereignisprotokoll ab.                                           |
| [**ReportEvent**](/windows/desktop/api/Winbase/nf-winbase-reporteventa)                               | Schreibt einen Eintrag am Ende des angegebenen Ereignis Protokolls.                                              |



 

 

 



