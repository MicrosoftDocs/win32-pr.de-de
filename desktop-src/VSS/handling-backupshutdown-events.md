---
description: Es ist möglich, dass eine Sicherungs Anwendung (Anforderer) beendet wird und kein BackupComplete-Ereignis generiert.
ms.assetid: 8e6a1f4f-ba62-46ea-965e-b0c6526ece89
title: Behandeln von BackupShutdown-Ereignissen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 939e8e64ca9ee463b0b8331e607f8068c3325d5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356911"
---
# <a name="handling-backupshutdown-events"></a>Behandeln von BackupShutdown-Ereignissen

Es ist möglich, dass eine Sicherungs Anwendung (Anforderer) beendet wird und kein [*BackupComplete*](vssgloss-b.md) -Ereignis generiert. Die Sicherungs Anwendung kann abstürzen oder beendet werden (z. b. über den Task-Manager) und kann [**IVssBackupComponents:: BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete)nicht aufzurufen.

Daher generiert die VSS-Infrastruktur (anstelle der anfordernden Person) ein [*BackupShutdown*](vssgloss-b.md) -Ereignis, wenn eine Instanz von [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) , die an einer Sicherung teilnimmt, freigegeben wird, unabhängig davon, ob Sie vom Anforderer oder vom System freigegeben wird.

Wenn eine Sicherung ordnungsgemäß ausgeführt wird, empfängt ein Writer ein BackupComplete-Ereignis, gefolgt von einem BackupShutdown-Ereignis.

Wenn der Vorgang abgebrochen wird (der Anforderer generiert ein [*Abbruch Ereignis*](vssgloss-a.md) durch Aufrufen von [**IVssBackupComponents:: abortbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup)) oder abrupt fehlschlägt, empfängt ein Writer möglicherweise nur ein BackupShutdown-Ereignis, und es werden möglicherweise keine anderen Ereignisse empfangen, die Bereinigungs Vorgänge ausführen. Es liegt an einem Writer, festzustellen, ob ein BackupShutdown-Ereignis einer ordnungsgemäßen Ereignis Sequenz folgt oder dass ein unerwarteter Fehler bei den Sicherungs Vorgängen auftritt.

Der BackupShutdown-Ereignishandler [**CVssWriter:: OnBackupShutdown**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupshutdown)empfängt die VSS- \_ ID (GUID) des schattenkopiessets des herunter gefahrenen Sicherungs Vorgangs. Der Writer kann dies verwenden, um zu bestimmen, welcher Sicherungs Vorgang heruntergefahren wird, wenn er die Schattenkopiesatz-ID während der Sicherungs Sequenz (z. b. aus [**CVssWriter:: OnFreeze**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onfreeze), [**CVssWriter:: OnThaw**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onthaw)oder [**CVssWriter:: OnPostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot)) mit [**CVssWriter:: getcurrentsnapshotsetid**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getcurrentsnapshotsetid)gespeichert hat.

Allerdings sollte ein Writer [**CVssWriter:: getcurrentsnapshotctid**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getcurrentsnapshotsetid) nicht innerhalb von [**CVssWriter:: OnBackupShutdown**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupshutdown)aufrufen. Außerdem kann **CVssWriter:: getcurrentsnapshotctid** nicht aufgerufen werden, nachdem [**CVssWriter:: OnPostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot) zurückgegeben wurde.

Der Writer kann an mehreren Sicherungs Vorgängen beteiligt sein, und wenn ein BackupShutdown-Ereignis aufgrund eines abrupten herunter Fahrens eines Anforderers aufgerufen wird, kann die zurückgegebene VSS- \_ ID ein anderer Sicherungs Vorgang sein, an dem der Writer beteiligt war.

 

 



