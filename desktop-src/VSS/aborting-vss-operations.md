---
description: 'Abbruchereignisse können während eines Sicherungsvorgangs in einem der folgenden Fälle generiert werden:'
ms.assetid: c2e39cdd-0ff8-4030-9bec-9e003b4d9520
title: Abbrechen von VSS-Vorgängen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 120ef8fb16c23d77a24526aad0fd62e56c1888a76dc2de884140094c6591cd78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998270"
---
# <a name="aborting-vss-operations"></a>Abbrechen von VSS-Vorgängen

[*Abbruchereignisse*](vssgloss-a.md) können während eines Sicherungsvorgangs in einem der folgenden Fälle generiert werden:

-   Ein Anfordernder generiert explizit ein [*Abort-Ereignis,*](vssgloss-a.md) indem [**er IVssBackupComponents::AbortBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup)aufruft.
-   Die [*Freeze-*](vssgloss-f.md) und [*Thaw-Ereignishandler*](vssgloss-t.md) eines Writers ([**CVssWriter::OnFreeze**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onfreeze) und [**CVssWriter::OnThaw**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onthaw)) geben **false** zurück oder können in dem in [**CVssWriter::Initialize**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-initialize)angegebenen Zeitfenster nicht abgeschlossen werden.
-   Bei der Erstellung einer Schattenkopie nach dem [*PrepareForSnapshot-Ereignis*](vssgloss-p.md) tritt ein Fehler des Anbieters oder von VSS auf.

Abbrüche werden für Wiederherstellungsvorgänge nicht unterstützt.

## <a name="requester-handling-and-creation-of-abort-events"></a>Verarbeitung und Erstellung von Abbruchereignissen durch den Anforderer

Eine Instanz der [**IVSSBackupComponents-Schnittstelle**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) kann nur für eine Sicherung verwendet werden. Wenn also bei der Verarbeitung einer Sicherung ein Fehler auftritt, empfiehlt es sich im Allgemeinen, die aktuelle Instanz freizugeben und neu zu starten.

Ein Anforderer sollte explizit signalisieren, dass er einen Sicherungsvorgang (mit [**IVssBackupComponents::AbortBackup)**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup)erst abbricht, nachdem die eigentliche Vorbereitung für eine Sicherung mit Writern oder die Erstellung einer Schattenkopie erfolgt ist.

Dies bedeutet, dass jedes Mal, wenn ein Anforderer einen Sicherungsvorgang beenden muss, nachdem er ein [*PrepareForBackup-Ereignis*](vssgloss-p.md) generiert hat, indem er [**IVssBackupComponents::P repareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup)aufruft, [**IVssBackupComponents::AbortBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup) aufruft und auf seine Rückgabe wartet, bevor die aktuelle [**IVSSBackupComponents-Instanz**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) freigegeben wird.

Wenn beispielsweise ein Writer einen Sicherungsvorgang verhindert hat, sollte ein Anforderer [**IVssBackupComponents::AbortBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup) verwenden, um alle anderen Writer zu benachrichtigen, dass der Sicherungsvorgang nicht abgeschlossen wird.

Vor dem Aufrufen von [**PrepareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup)oder wenn der Aufruf von **PrepareForBackup** fehlschlägt, kann ein Anforderer die aktuelle Instanz der [**IVSSBackupComponents-Schnittstelle**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) freigeben, ohne ein Abort-Ereignis generieren zu müssen.

Wenn beispielsweise die aktuelle Instanz von [**IVSSBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) nur zum Abrufen von Informationen verwendet wird, indem [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) aufgerufen und ein [*Identify-Ereignis*](vssgloss-i.md) generiert wird, kann die Instanz von **IVSSBackupComponents** einfach freigegeben werden, sobald Informationen zurückgegeben wurden.

Ein Anforderer generiert eine Reihe von Ereignissen ([*PrepareForSnapshot*](vssgloss-p.md), [*Freeze*](vssgloss-f.md), [*Thaw*](vssgloss-t.md)und [*PostSnapshot*](vssgloss-p.md)), wenn er [**IVssBackupComponents::D oSnapshotSet aufruft.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) Bei der Behandlung der Freeze- und Thaw-Ereignisse schlägt ein Writer möglicherweise fehl und kann selbst ein Abbruchereignis generieren. Wenn die Ereignisse PrepareForSnapshot und PostSnapshot nicht behandelt werden, wird kein Abbruchereignis generiert.

Es ist nicht immer möglich, dass ein Anforderer weiß, ob ein Abbruchereignis generiert wurde, wenn [**IVssBackupComponents::D oSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) einen Fehler angibt. Daher sollte ein Anforderer, der einen Sicherungsvorgang beenden muss, weil der Status von **IVssBackupComponents::D oSnapshotSet** darauf hinweist, dass ein Problem weiterhin [**IVssBackupComponents::AbortBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup)aufrufen sollte.

Wenn ein Anforderer [**IVssBackupComponents::AbortBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup)aufgerufen hat, ist es nicht erforderlich, [**IVssBackupComponents::BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) aufzurufen, bevor eine Instanz von [**IVSSBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents)freigegeben wird.

## <a name="writer-handling-and-creation-of-abort-events"></a>Writer-Behandlung und -Erstellung von Abbruchereignissen

Wie bereits erwähnt, kann ein Writer ein Abbruchereignis von einem Anforderer empfangen, oder der Anbieter kann ein Ereignis selbst auslösen. Außerdem ist es möglich, dass ein Writer unter bestimmten Umständen mehrere Abbruchereignisse empfängt. Writer-Entwickler sollten jede Implementierung von [**CVssWriter::OnAbort**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onabort) unter Berücksichtigung dieses Themas programmieren.

Bei der Behandlung eines Abbruchereignisses sollte ein Writer versuchen, den von ihm verwalteten Prozess in den normalen Ausführungszustand wiederherzustellen und fehlerbehandlung und Protokollierung durchzuführen.

Dies kann bedeuten, dass eine Implementierung von [**CVssWriter::OnAbort**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onabort) möglicherweise viele, wenn nicht alle Aufgaben derselben Aufgaben ausführen muss wie der Thaw-Ereignishandler ([**CVssWriter::OnThaw**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onthaw)) und der PostSnapshot-Ereignishandler ([**CVssWriter::OnPostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot)), und diese Handler können innerhalb von **CVssWriter::OnAbort** aufgerufen werden.

 

 



