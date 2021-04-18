---
description: In der folgenden Tabelle wird die Abfolge der Aktionen und Ereignisse aufgeführt, die erforderlich sind, damit ein Sicherungs Vorgang beendet wird. Weitere Informationen finden Sie unter Übersicht über die Verarbeitung einer Sicherung unter VSS.
ms.assetid: 12dcb2d1-614b-4c4c-a47c-342f79b20a62
title: Übersicht über das Beenden der Sicherung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d9268bd8fd4ec51be2ee7a891d4dffb3a5cb1b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345286"
---
# <a name="overview-of-backup-termination"></a>Übersicht über das Beenden der Sicherung

In der folgenden Tabelle wird die Abfolge der Aktionen und Ereignisse aufgeführt, die erforderlich sind, damit ein Sicherungs Vorgang beendet wird. Weitere Informationen finden Sie [unter Übersicht über die Verarbeitung einer Sicherung unter VSS](overview-of-processing-a-backup-under-vss.md).



| Requestaktion                                                                                                                                                                                                              | Ereignis                                                                 | Writer-Aktion                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Der Anforderer beendet die Schatten Kopie durch Freigeben der [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) -Schnittstelle oder durch Aufrufen von [**IVssBackupComponents::D eletesnapshots**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-deletesnapshots). | Keine                                                                  | Keine                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) wird durch Aufrufen von [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)freigegeben.                                                                                                   | [*BackupShutdown*](vssgloss-b.md) | Der Writer behandelt das Ereignis mit [**CVssWriter:: OnBackupShutdown**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupshutdown), das es ermöglicht, jeden Zustand zu bereinigen, der mit dem Schattenkopiesatz verknüpft ist. Wenn der Sicherungs Vorgang fehlgeschlagen ist – d. h. es wurde kein Backup [**Complete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) -Ereignis generiert –, muss der Writer möglicherweise auch eine Fehlerbehandlung durchführen. Weitere Informationen finden Sie unter [Behandeln von BackupShutdown-Ereignissen](handling-backupshutdown-events.md) . |



 

Da eine [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) -Schnittstelle nicht wieder verwendet werden kann und der debugtor der Schnittstelle die Schatten Kopien beendet, gibt es in der Regel keinen Grund, [**IVssBackupComponents::D eletesnapshots**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-deletesnapshots)aufzurufen. Diese Methode ist für die Verwendung in Verbindung mit der Fehlerbehandlung und das Abbrechen von Sicherungen konzipiert (siehe [Abbrechen von VSS-Vorgängen](aborting-vss-operations.md)).

 

 
