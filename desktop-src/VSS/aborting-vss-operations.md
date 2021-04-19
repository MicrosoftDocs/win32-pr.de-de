---
description: 'Abbruch Ereignisse können während eines Sicherungs Vorgangs in einem der folgenden Fälle generiert werden:'
ms.assetid: c2e39cdd-0ff8-4030-9bec-9e003b4d9520
title: Abbrechen von VSS-Vorgängen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35e4b82ba4227dfeb02e3da91c9bc1e77f10f492
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360590"
---
# <a name="aborting-vss-operations"></a>Abbrechen von VSS-Vorgängen

[*Abbruch*](vssgloss-a.md) Ereignisse können während eines Sicherungs Vorgangs in einem der folgenden Fälle generiert werden:

-   Ein Anforderer generiert explizit ein [*Abbruch Ereignis*](vssgloss-a.md) , indem [**IVssBackupComponents:: abortbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup)aufgerufen wird.
-   Die [*Freeze*](vssgloss-f.md) [*-und Ereignis*](vssgloss-t.md) Handler eines Writers ([**CVssWriter:: OnFreeze**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onfreeze) und [**CVssWriter:: OnThaw**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onthaw)) geben **false** zurück oder können nicht im Zeitfenster, das in [**CVssWriter:: Initialize**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-initialize)angegeben ist, abschließen.
-   Bei der Erstellung einer Schatten Kopie nach dem [*prepareforsnapshot*](vssgloss-p.md) -Ereignis ist ein Fehler des Anbieters oder VSS aufgetreten.

Abbrüche werden für Wiederherstellungs Vorgänge nicht unterstützt.

## <a name="requester-handling-and-creation-of-abort-events"></a>Behandlung und Erstellung von Abbruch Ereignissen durch Anforderer

Eine Instanz der [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) -Schnittstelle kann nur für eine Sicherung verwendet werden. Wenn bei der Verarbeitung einer Sicherung ein Fehler auftritt, ist es in der Regel am besten, die aktuelle Instanz freizugeben und zu beginnen.

Ein Anforderer sollte explizit signalisieren, dass ein Sicherungs Vorgang abgebrochen wird (mithilfe von [**IVssBackupComponents:: abortbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup)), nachdem die tatsächliche Vorbereitung für eine Sicherung, das Einbeziehen von Writern oder das Erstellen einer Schatten Kopie statt genommen hat.

Dies bedeutet, dass jedes Mal, wenn ein Anforderer einen Sicherungs Vorgang nach dem Erstellen eines [*PrepareForBackup*](vssgloss-p.md) -Ereignisses durch Aufrufen von [**IVssBackupComponents::P Analyse forbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup)abbrechen muss, [**IVssBackupComponents:: abortbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup) aufrufen und seine Rückgabe abwarten muss, bevor die aktuelle [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) -Instanz freigegeben wird.

Wenn ein Writer z. b. einen Sicherungs Vorgang überprüft hat, sollte ein Anforderer [**IVssBackupComponents:: abortbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup) verwenden, um alle anderen Writer zu benachrichtigen, dass der Sicherungs Vorgang nicht abgeschlossen wird.

Vor dem Aufruf von [**PrepareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup), oder wenn der Aufruf von **PrepareForBackup** fehlschlägt, kann ein Anforderer die aktuelle Instanz der [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) -Schnittstelle freigeben, ohne dass ein Abbruch Ereignis generiert werden muss.

Wenn z. b. die aktuelle Instanz von [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) lediglich zum Abrufen von Informationen verwendet wird, indem [**IVssBackupComponents:: gatherwrite Metadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) aufgerufen und ein [*identifizereignis*](vssgloss-i.md) erzeugt wird, kann die Instanz von **IVssBackupComponents** einfach freigegeben werden, sobald Informationen zurückgegeben wurden.

Ein Anforderer generiert eine Reihe von Ereignissen ([*prepareforsnapshot*](vssgloss-p.md), [*Freeze*](vssgloss-f.md), [*Thaw*](vssgloss-t.md)und [*PostSnapshot*](vssgloss-p.md)), wenn er [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)aufruft. Während der Behandlung von Freeze-und Thaw-Ereignissen schlägt ein Writer möglicherweise fehl und kann selbst ein Abbruch Ereignis generieren. Bei einem Fehler bei der Behandlung von prepareforsnapshot-und PostSnapshot-Ereignissen wird kein Abbruch Ereignis generiert.

Es ist nicht immer möglich, dass ein Anforderer weiß, ob ein Abbruch Ereignis generiert wurde, wenn [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) einen Fehler anzeigt. Daher sollte ein Anforderer, der einen Sicherungs Vorgang beenden muss, da der Status von **IVssBackupComponents::D osnapshotset** auf ein Problem hinweist, trotzdem [**IVssBackupComponents:: abortbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup)aufruft.

Wenn ein Anforderer [**IVssBackupComponents:: abortbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup)aufgerufen hat, ist es nicht erforderlich, [**IVssBackupComponents:: BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) vor dem Freigeben einer Instanz von [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents)aufzurufen.

## <a name="writer-handling-and-creation-of-abort-events"></a>Behandlung und Erstellung von Abbruch Ereignissen durch Writer

Wie bereits erwähnt, kann ein Writer ein Abbruch Ereignis von einem Anforderer empfangen, oder der Anbieter kann einen selbst initiieren. Außerdem kann ein Writer unter bestimmten Umständen mehrere Abbruch Ereignisse empfangen. Writer-Entwickler sollten eine beliebige Implementierung von [**CVssWriter:: OnAbort**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onabort) mit diesem Hintergrund codieren.

Bei der Behandlung eines Abbruch Ereignisses sollte ein Writer versuchen, den von ihm verwalteten Prozess in seinem normalen Betriebsstatus wiederherzustellen sowie Fehlerbehandlung und Protokollierung auszuführen.

Dies kann bedeuten, dass die Implementierung von [**CVssWriter: OnAbort**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onabort) muss möglicherweise viele, wenn nicht alle, der gleichen Aufgaben wie der Ereignishandler für Ereignishandler ([**CVssWriter:: OnThaw**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onthaw)) und den PostSnapshot-Ereignishandler ([**CVssWriter:: OnPostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot)) ausführen, und diese Handler können von **CVssWriter:: OnAbort** aufgerufen werden.

 

 



