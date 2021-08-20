---
description: Es ist möglich, dass eine Sicherungsanwendung (anfordernde Anwendung) beendet und kein BackupComplete-Ereignis generiert.
ms.assetid: 8e6a1f4f-ba62-46ea-965e-b0c6526ece89
title: Behandeln von BackupShutdown-Ereignissen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61e60a063a11f0a492407daed31ace4a62aec2a13fe824e110de272d58b84bea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998250"
---
# <a name="handling-backupshutdown-events"></a>Behandeln von BackupShutdown-Ereignissen

Es ist möglich, dass eine Sicherungsanwendung (anfordernde Anwendung) beendet und kein [*BackupComplete-Ereignis generiert.*](vssgloss-b.md) Die Sicherungsanwendung kann abstürzen oder beendet werden (z. B. über den Task-Manager) und kann [**IVssBackupComponents::BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete)nicht aufrufen.

Daher generiert die VSS-Infrastruktur (anstelle des Anfordernden) immer dann ein [*BackupShutdown-Ereignis,*](vssgloss-b.md) wenn eine an einer Sicherung beteiligte Instanz von [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) freigegeben wird, unabhängig davon, ob sie vom Anfordernden oder vom System freigegeben wird.

Wenn eine Sicherung ordnungsgemäß fortgesetzt wird, erhält ein Writer ein BackupComplete-Ereignis gefolgt von einem BackupShutdown-Ereignis.

Wenn der Vorgang abgebrochen wird (der Anfordernde generiert ein [*Abort-Ereignis*](vssgloss-a.md) durch Aufrufen von [**IVssBackupComponents::AbortBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup)) oder plötzlich einen Fehler verursacht, erhält ein Writer möglicherweise nur ein BackupShutdown-Ereignis und erhält möglicherweise keine anderen Ereignisse, die Bereinigungsvorgänge ausführen. Es liegt in der Hand eines Writers zu bestimmen, ob ein BackupShutdown-Ereignis einer ordnungsgemäßen Abfolge von Ereignissen folgt oder einen unerwarteten Fehler der Sicherungsvorgänge darstellt.

Der BackupShutdown-Ereignishandler [**CVssWriter::OnBackupShutdown**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupshutdown)empfängt die VSS-ID (GUID) des Schattenkopiesets des heruntergefahrenen \_ Sicherungsvorgang. Der Writer kann mithilfe von [**CVssWriter::OnFreeze,**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getcurrentsnapshotsetid)CVssWriter::OnThaw oder CVssWriter::OnPostSnapshot ) ermitteln, welcher Sicherungsvorgang heruntergefahren wird, wenn er die Schattenkopieset-ID während der Sicherungssequenz gespeichert hat (z. B. aus [**CVssWriter::OnFreeze,**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onfreeze) [**CVssWriter::OnThaw**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onthaw)oder [**CVssWriter::OnPostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot)).

Ein Writer sollte jedoch nicht [**CVssWriter::GetCurrentSnapshotSetId**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getcurrentsnapshotsetid) aus [**CVssWriter::OnBackupShutdown aufrufen.**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupshutdown) Außerdem kann **CVssWriter::GetCurrentSnapshotSetId** nicht aufgerufen werden, nachdem [**CVssWriter::OnPostSnapshot zurückgegeben**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot) wurde.

Es ist möglich, dass der Writer an mehreren Sicherungsvorgängen beteiligt ist. Wenn ein BackupShutdown-Ereignis aufgrund eines plötzlichen Herunterfahrens eines Anfordernden aufgerufen wird, kann die zurückgegebene VSS-ID die eines anderen Sicherungsvorgang sein, an dem der Writer beteiligt \_ war.

 

 



