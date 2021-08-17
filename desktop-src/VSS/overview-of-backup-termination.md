---
description: Die folgende Tabelle zeigt die Abfolge der Aktionen und Ereignisse, die erforderlich sind, damit ein Sicherungsvorgang beendet wird. Weitere Informationen finden Sie unter Übersicht über die Verarbeitung einer Sicherung unter VSS.
ms.assetid: 12dcb2d1-614b-4c4c-a47c-342f79b20a62
title: Übersicht über die Sicherungsbeendigung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52fd57822a62cf3fa39cee2b17d79ae2545afa07bd722d26cacda68cba3b6695
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117937968"
---
# <a name="overview-of-backup-termination"></a>Übersicht über die Sicherungsbeendigung

Die folgende Tabelle zeigt die Abfolge der Aktionen und Ereignisse, die erforderlich sind, damit ein Sicherungsvorgang beendet wird. Weitere Informationen finden Sie unter [Übersicht über die Verarbeitung einer Sicherung unter VSS.](overview-of-processing-a-backup-under-vss.md)



| Aktion des Anfordernden                                                                                                                                                                                                              | Ereignis                                                                 | Writer-Aktion                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Der Anfordernde beendet die Schattenkopie, indem er die [**IVssBackupComponents-Schnittstelle**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) frei gibt oder [**IVssBackupComponents::D eleteSnapshots aufruft.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-deletesnapshots) | Keine                                                                  | Keine                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) wird durch Aufrufen von [**IUnknown::Release veröffentlicht.**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)                                                                                                   | [*BackupShutdown*](vssgloss-b.md) | Der Writer behandelt das Ereignis mit [**CVssWriter::OnBackupShutdown,**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupshutdown)wodurch alle Zustandsbereinigungen im Zusammenhang mit dem Schattenkopiesatz möglich sind. If the backup operation failed—that is, it did not generate a [**BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) event—the writer may also have to perform error handling. Weitere Informationen finden Sie unter [Behandeln von BackupShutdown-Ereignissen.](handling-backupshutdown-events.md) |



 

Da eine [**IVssBackupComponents-Schnittstelle**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) nicht wiederverwendet werden kann und der Destruktor der Schnittstelle die Schattenkopien beendet, gibt es in der Regel keinen Grund, [**IVssBackupComponents::D eleteSnapshots aufzurufen.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-deletesnapshots) Diese Methode ist für die Verwendung in Verbindung mit der Fehlerbehandlung und dem Abbrechen von Sicherungen konzipiert (siehe Abbrechen von [VSS-Vorgängen).](aborting-vss-operations.md)

 

 
