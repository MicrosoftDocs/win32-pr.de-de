---
description: Anfordernde sind primär für den Lebenszyklus eines Sicherungskomponentendokuments verantwortlich.
ms.assetid: 287b7b9a-ac04-4a74-83c1-2cdd4a571ac1
title: Lebenszyklus von Sicherungskomponentendokumenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4804625f979e0d5621d96a2230c1419354d0dbeb4c368312dbd3943e0ac0c4bc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124530"
---
# <a name="backup-components-document-life-cycle"></a>Lebenszyklus von Sicherungskomponentendokumenten

Anfordernde sind primär für den Lebenszyklus eines Sicherungskomponentendokuments verantwortlich.

Dieses Steuerelement wird von einer Instanz des [**IVssBackupComponents-Schnittstellenobjekts**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) verwendet, das von [**CreateVssBackupComponents zurückgegeben wird.**](/windows/desktop/api/VsBackup/nf-vsbackup-createvssbackupcomponents)

Ein Anfordernder muss ein Sicherungskomponentendokument vor einer Sicherung oder Wiederherstellung initialisieren, indem er [**IVssBackupComponents::InitializeForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforbackup) oder [**IVssBackupComponents::InitializeForRestore aufruft.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforrestore) Der Anfordernde kann das Dokument als leer initialisieren oder eine zuvor gespeicherte Kopie des Dokuments laden.

Bei Sicherungsvorgängen wird ein Sicherungskomponentendokument in der Regel als leer initialisiert. Die Daten werden während der Verarbeitung der Sicherung in Zusammenarbeit mit den Writern des Systems ausgefüllt.

Bei Wiederherstellungsvorgängen wird ein Sicherungskomponentendokument in der Regel aus einem gespeicherten Dokument initialisiert, das während der ersten Sicherung generiert wurde. Dies ermöglicht es der Wiederherstellung (in Verbindung mit der Untersuchung gespeicherter Writer-Metadatendokumente), zu bestimmen, welche Daten ursprünglich sichern wurden und wie sie wiederhergestellt werden sollen.

Das Sichern [*transportierbarer Schattenkopien*](vssgloss-t.md) ist eine Ausnahme von dieser Regel. In diesem Fall hätte eine Schattenkopie von einem System (in dem sie zusammen mit dem ersten Sicherungskomponentendokument erstellt wurde) in ein anderes verschoben werden können, indem die logische Einheit eines freigegebenen Speichergeräts neu zugewiesen wurde. Um unter diesen Umständen zu sichern, lädt eine Anfordernde den gespeicherten Sicherungsstatus und geht an der Stelle fort, an der das ursprüngliche System aufgelassen hat. (Weitere Informationen finden Sie unter [Importing Transportable Shadow Copied Volumes](importing-transportable-shadow-copied-volumes.md).)

Während der Verarbeitung einer Sicherung entscheidet der An anfordernde Benutzer, welche Komponenten tatsächlich kopiert werden sollen, [](vssgloss-l.md)und zwar auf der Grundlage, welche Komponenten als für die Sicherung auswählbar markiert [*sind,*](vssgloss-s.md)die logischen Pfade der Komponente und ihre eigene interne Logik.

Einige der Komponenten werden explizit [*in den Sicherungsvorgang*](vssgloss-e.md) eingeschlossen. Informationen zur Komponente werden dem Dokument Sicherungskomponenten hinzugefügt. Andere werden [*implizit in die*](vssgloss-i.md) Sicherung eingeschlossen. Informationen zu den hinzugefügten Komponenten werden dem Dokument sicherungskomponenten nicht hinzugefügt.

Alle nicht auswählbaren Komponenten eines Writers für Sicherungskomponenten ohne einen auswählbaren Vorgänger in ihrem logischen Pfad und diejenigen, die für sicherungskomponenten ausgewählt werden können, die der Anfordernde auswählt, werden explizit hinzugefügt.

Sowohl nicht auswählbare als auch auswählbare Sicherungskomponenten können implizit hinzugefügt werden, wenn sie über einen auswählbaren Vorgänger im logischen Pfad verfügen, der explizit in der Sicherung enthalten ist. Diese Komponenten ([*Unterkomponenten*](vssgloss-s.md)) sind Member [*von*](vssgloss-s.md) Komponentensätzen, die durch ihren auswählbaren Vorgänger definiert werden.

Bei der Verarbeitung von Wiederherstellungsvorgängen verwendet der Anfordernde die Auswählbarkeit für die Wiederherstellung anstelle der Auswählbarkeit für die Sicherung in Verbindung mit informationen zum logischen Pfad und seiner eigenen internen Logik, um zu entscheiden, welche Dateien wiederhergestellt werden. [](vssgloss-s.md)

Wenn eine Komponente, die der Sicherung implizit hinzugefügt wurde, jetzt explizit zur Wiederherstellung hinzugefügt werden soll, aktualisiert der Anfordernde das Sicherungskomponentendokument mit den Informationen dieser Komponente.

Informationen zu den gespeicherten Komponenten sind sowohl für Anfordernde als auch für Writer über Instanzen der [**IVssComponent-Schnittstelle**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) verfügbar.

Über [**IVssComponent-Schnittstellen**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) können Writer Abfragen durchführen und (bis zum Ende der [**PostSnapshot-**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot) und [**PostRestore-Ereignisse)**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostrestore) Informationen im Dokument zu Sicherungskomponenten ändern.

Wenn [**CVssWriter::OnPrepareBackup,**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpreparebackup) [**CVssWriter::OnPreRestore,**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onprerestore) [**CVssWriter::OnPostSnapshot,**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot) [**CVssWriter::OnBackupComplete**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupcomplete)oder [**der CVssWriter::OnPostRestore-Ereignishandler**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostrestore) aufgerufen wird, empfängt ein Writer eine Instanz einer [**IVssWriterComponents-Schnittstelle.**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswritercomponents)

Beachten Sie, dass das Backup Components-Dokument bei der Generierung des [**BackupComplete-Ereignisses**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) als schreibgeschützt gilt und [**CVssWriter::OnBackupComplete**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupcomplete) daher nicht die [**IVssComponent-Schnittstelle**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) verwenden kann, um es zu ändern.

Über die [**IVSSWriterComponents-Schnittstelle**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswritercomponents) kann der Writer Instanzen der [**IVssComponent-Schnittstelle**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) abrufen, die ihm den Zugriff auf alle seine Komponenten ermöglichen, die explizit dem Sicherungskomponentendokument hinzugefügt wurden, und ihren Zustand ändern. Weitere Informationen finden Sie unter [Übersicht über die Verarbeitung einer Sicherung unter VSS](overview-of-processing-a-backup-under-vss.md) und Übersicht über die Verarbeitung einer [Wiederherstellung unter VSS.](overview-of-processing-a-restore-under-vss.md)

SicherungskomponentenDokumente werden aus dem Arbeitsspeicher entfernt, wenn die [**IVssBackupComponents-Schnittstelle**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) freigegeben wird, und müssen mithilfe von [**IVssBackupComponents::SaveAsXML**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-saveasxml)gespeichert werden, da alle Informationen verloren gehen.

Wenn ein [**IVssBackupComponents-Dokument**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) ordnungsgemäß freigegeben wird, wird außerdem ein [**BackupShutdown-Ereignis**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupshutdown) generiert und Schattenkopien der automatischen Freigabe gelöscht.[](vssgloss-a.md)

 

 



