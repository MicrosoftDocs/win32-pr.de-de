---
description: Requester ist für den Lebenszyklus eines Sicherungs Komponenten Dokuments primär verantwortlich.
ms.assetid: 287b7b9a-ac04-4a74-83c1-2cdd4a571ac1
title: Lebenszyklus von Sicherungs Komponenten Dokumenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4bcb0263f46466d7be2bc19f3c8809167b2da08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373353"
---
# <a name="backup-components-document-life-cycle"></a>Lebenszyklus von Sicherungs Komponenten Dokumenten

Requester ist für den Lebenszyklus eines Sicherungs Komponenten Dokuments primär verantwortlich.

Dieses Steuerelement wird von einer Instanz des [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) -Schnittstellen Objekts, das von " [**kreatevssbackupcomponents**](/windows/desktop/api/VsBackup/nf-vsbackup-createvssbackupcomponents)" zurückgegeben wird, ausgeführt.

Ein Anforderer muss ein Sicherungs Komponenten Dokument vor einer Sicherung oder Wiederherstellung initialisieren, indem [**IVssBackupComponents:: initializeforbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforbackup) oder [**IVssBackupComponents:: initializeforrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforrestore)aufgerufen wird. Der Anforderer kann das Dokument als leer oder eine zuvor gespeicherte Kopie des Dokuments laden.

Bei Sicherungs Vorgängen wird in der Regel ein Sicherungs Komponenten Dokument als leer initialisiert. Die Daten werden im Rahmen der Verarbeitung der Sicherung mit der Zusammenarbeit der Schreiber des Systems gefüllt.

Bei Wiederherstellungs Vorgängen wird in der Regel ein Sicherungs Komponenten Dokument aus einem gespeicherten Dokument initialisiert, das während der ersten Sicherung generiert wurde. Dies ermöglicht die Wiederherstellung (in Verbindung mit der Untersuchung gespeicherter Writer-Metadatendokumente), um zu bestimmen, welche Daten anfänglich gesichert und wie Sie wieder hergestellt werden sollten.

Das Sichern von über [*tragbaren Schatten Kopien*](vssgloss-t.md) ist eine Ausnahme von dieser Regel. In diesem Fall könnte eine Schatten Kopie von einem System (wo es zusammen mit dem ersten Sicherungs Komponenten Dokument erstellt wurde) in ein anderes verschoben werden, indem die logische Einheit eines freigegebenen Speichergeräts neu zugewiesen wird. Um unter diesen Umständen zu sichern, lädt ein Anforderer den gespeicherten Sicherungs Status und geht von der Stelle aus, an der das ursprüngliche System verbleibt. (Weitere Informationen finden Sie unter [Importieren von transportable-schattenkopierten Volumes](importing-transportable-shadow-copied-volumes.md).)

Im Verlauf der Verarbeitung einer Sicherung entscheidet der Anforderer, welche Komponenten tatsächlich kopiert werden sollen, wenn die Komponenten als [*für die Sicherung wählbar*](vssgloss-s.md)gekennzeichnet sind, die [*logischen Pfade*](vssgloss-l.md)der Komponente und die eigene interne Logik.

Einige der Komponenten werden explizit in den Sicherungs Vorgang [*eingeschlossen*](vssgloss-e.md) . Informationen über die Komponente werden dem Dokument mit den Sicherungs Komponenten hinzugefügt. Andere werden implizit in die Sicherung [*eingeschlossen*](vssgloss-i.md) . Informationen zu den hinzugefügten Komponenten werden dem Dokument mit den Sicherungs Komponenten nicht hinzugefügt.

Alle nicht auswählbaren Writer für Sicherungs Komponenten ohne auswählbaren Vorgänger in ihrem logischen Pfad, und diejenigen, die von der Anforderer ausgewählt werden, werden explizit hinzugefügt.

Sowohl nicht auswählbar als auch auswählbare Sicherungs Komponenten können implizit hinzugefügt werden, wenn Sie über einen auswählbaren Vorgänger in ihrem logischen Pfad verfügen, der explizit in der Sicherung enthalten ist. Diese Komponenten ([*unter Komponenten*](vssgloss-s.md)) sind Mitglieder der [*Komponenten Sätze*](vssgloss-s.md) , die durch ihren auswählbaren Vorgänger definiert werden.

Bei der Behandlung von Wiederherstellungs Vorgängen verwendet die anfordernde Person bei der Wiederherstellung die Wahl der [*Wiederherstellung*](vssgloss-s.md) anstelle der selectlichkeit der Sicherung in Verbindung mit logischen Pfadinformationen und ihrer internen Logik, um zu entscheiden, welche Dateien wieder hergestellt werden

Wenn eine Komponente, die der Sicherung implizit hinzugefügt wurde, jetzt explizit der Wiederherstellung hinzugefügt werden soll, aktualisiert der Anforderer das Dokument mit den Sicherungs Komponenten mit den Informationen dieser Komponente.

Informationen zu den gespeicherten Komponenten sind sowohl für Anforderer als auch für Writer über Instanzen der [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) -Schnittstelle verfügbar.

Dies erfolgt über [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) -Schnittstellen, die Writer Abfragen und (bis zum Ende von [**PostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot) -und [**postrestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostrestore) -Ereignissen) Informationen im Sicherungs Komponenten Dokument ändern können.

Wenn der Ereignishandler [**CVssWriter:: onpreparebackup**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpreparebackup), [**CVssWriter:: onprerestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onprerestore), [**CVssWriter:: OnPostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot), [**CVssWriter:: OnBackupComplete**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupcomplete)oder [**CVssWriter:: OnPostRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostrestore) aufgerufen wird, empfängt ein Writer eine Instanz einer [**ivssschreitercomponents**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswritercomponents) -Schnittstelle.

Beachten Sie, dass das Sicherungs Komponenten Dokument bei der Generierung des [**BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) -Ereignisses schreibgeschützt ist. Daher kann [**CVssWriter:: OnBackupComplete**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupcomplete) die [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) -Schnittstelle nicht verwenden, um Sie zu ändern.

Über die [**ivssschreitercomponents**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswritercomponents) -Schnittstelle kann der Writer Instanzen der [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) -Schnittstelle abrufen, die ihm den Zugriff auf alle seine Komponenten ermöglicht, die dem Dokument mit den Sicherungs Komponenten explizit hinzugefügt werden, und seinen Status ändern. Weitere Informationen finden Sie unter [Übersicht über die Verarbeitung einer Sicherung unter VSS](overview-of-processing-a-backup-under-vss.md) und [im Überblick über die Verarbeitung einer Wiederherstellung unter VSS](overview-of-processing-a-restore-under-vss.md).

Sicherungs Komponenten Dokumente werden aus dem Arbeitsspeicher entfernt, wenn die [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) -Schnittstelle freigegeben wird, und müssen mithilfe von [**IVssBackupComponents:: SaveAsXml**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-saveasxml)gespeichert werden, oder alle Ihre Informationen gehen verloren.

Wenn außerdem ein [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) -Dokument ordnungsgemäß freigegeben wird, wird ein [**BackupShutdown**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupshutdown) -Ereignis generiert und [*Schatten Kopien mit automatischer Freigabe*](vssgloss-a.md) gelöscht.

 

 



