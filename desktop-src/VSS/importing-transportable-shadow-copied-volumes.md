---
description: Manchmal ist es wünschenswert, eine Schattenkopie auf einem System zu erstellen, aber die Schattenkopie auf einem zweiten System zu verwenden.
ms.assetid: 4ec63917-03c0-434e-892e-3d9d4c47740e
title: Importieren transportierbarer Schattenkopievolumes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73cee5d491cde59767a321094f0a7de2f34da97b29c6ed02e5cc490643b4dcd5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119510260"
---
# <a name="importing-transportable-shadow-copied-volumes"></a>Importieren transportierbarer Schattenkopievolumes

Manchmal ist es wünschenswert, eine Schattenkopie auf einem System zu erstellen, aber die Schattenkopie auf einem zweiten System zu verwenden.

Stellen Sie sich den Fall vor, dass zu sichernde Daten normalerweise von einem bestimmten System (*systemOne*) während des normalen Betriebs verwaltet werden und dass diese Daten physisch in einem Speicherarray oder einer Appliance gespeichert werden.

Um die Unterbrechung von *systemOne* zu minimieren (da Sicherungsvorgänge ressourcenintensiv sein können), ist es wünschenswert, die Sicherung mit *systemTwo* durchzuführen, einem Sicherungsserver, der Zugriff auf das gleiche Speicherarray wie *systemOne hat.*

Um eine ordnungsgemäße Schattenkopie sicherzustellen – in Zusammenarbeit mit den Writern auf *systemOne* und der entsprechenden Beibehaltung des Zustands für laufende Aufgaben – sollte die Schattenkopie von *systemOne ausgeführt werden.*

Daher muss *systemOne* eine transportierbare [*Schattenkopie erstellen,*](vssgloss-t.md)die *systemTwo* dann importiert.

**Windows Server 2003, Standard Edition, Windows Server 2003, Web Edition und Windows XP:** Transportierbare Schattenkopiesätze werden nicht unterstützt. Alle Editionen von Windows Server 2003 mit Service Pack 1 (SP1) unterstützen transportierbare Schattenkopiesätze.

Ein typisches Beispiel für den Import einer transportierbaren Schattenkopie kann wie folgt fortgesetzt werden:

1.  Zunächst wird die logische Einheit (LUN), die vom Speicherarray bereitgestellt wird, als Volume auf *systemOne* (z.B. F:) bereitgestellt.
2.  Eine anfordernde Instanz, die auf *systemOne* ausgeführt wird, instanziiert eine Instanz von [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) und geht so vor, als würde sie eine Sicherung vorbereiten. (Weitere Informationen finden Sie [](overview-of-the-backup-discovery-phase.md)unter Übersicht über die [](overview-of-pre-backup-tasks.md) [Sicherungsin initialisierung,](overview-of-backup-initialization.md)Übersicht über die Sicherungsermittlungsphase und Übersicht über Aufgaben vor der Sicherung.)
3.  Die Anfordernde auf *systemOne* ändert den Schattenkopiekontext, der in der Regel für den lokalen Sicherungsvorgang (**VSS \_ CTX \_ APP \_ BACKUP**) verwendet wird, um anzugeben, dass eine transportierbare Schattenkopie erstellt wird **(VSS \_ VOLSNAP \_ ATTR \_ TRANSPORTABLE**). Das transportierbare Attribut kann auch anderen Schattenkopiekontexten hinzugefügt werden.
4.  Bei einem Schattenkopiekontext von **VSS \_ CTX \_ APP \_ BACKUP** VSS VOLSNAP ATTR TRANSPORTABLE erstellt der An anfordernde In systemOne eine Schattenkopie, indem er \| **\_ \_ \_** [**IVssBackupComponents::D oSnapshotSet aufruft.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) 
5.  *SystemOne* verwendet [**IVssBackupComponents::SaveAsXML,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-saveasxml) um den aktuellen Zustand des Sicherungskomponentendokuments zu speichern, und [**IVssExwriterMetadata::SaveAsXML,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-saveasxml) um die Writer-Metadatendokumente der einzelnen Writer zu speichern. Die XML-Zeichenfolgen, die diese Dokumente enthalten, werden dann einem Anfordernden zur Verfügung gestellt, der unter *systemTwo ausgeführt wird.*

    Der Anfordernde überträgt das Sicherungskomponentendokument *an systemTwo.*

    Beachten Sie, dass der Anfordernde auf *systemOne* seine Instanz von [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) an diesem Punkt nicht frei gibt, wenn der Zweck der Schattenkopie für die Sicherung ist. Die Schnittstelle sollte geöffnet bleiben, *bis systemTwo* die Sicherungsvorgänge erfolgreich abgeschlossen hat. Erst dann sollte die anfordernde Seite ein [**BackupComplete-Ereignis**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) aussetzen, da einige Writer Protokolle abschneiden und nach einer erfolgreichen Sicherung andere Arbeiten durchführen. Wenn das Ziel der Schattenkopie Data Mining oder andere Zwecke ist, kann die Schnittstelle in diesem Schritt geschlossen werden.

6.  Der Anfordernde in *systemTwo* ruft dann [**IVssBackupComponents::ImportSnapshots**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-importsnapshots) auf, um Zugriff auf die Schattenkopie zu erhalten, die vom Anfordernden auf *systemOne erstellt wurde.*
    > [!Note]  
    > Der Anfordernde ist für die Serialisierung des Importschattenkopie-Vorgangs verantwortlich. Wenn beim Aufruf von [**IVssBackupComponents::ImportSnapshots**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-importsnapshots) ein Fehler auftritt, bereinigt der VSS luNs nicht selbst. Der Anfordernde muss die Bereinigung von LUNs initiieren.

     

7.  Der Anfordernde auf *systemTwo* führt die Sicherung des kopierten Schattenmaterials genau so aus, als würde er eine Schattenkopie sichern, die er selbst erstellt hat (siehe Übersicht über die tatsächliche Sicherung von [Dateien).](overview-of-actual-backup-of-files.md)

    Die Anfordernde in *systemTwo* erhält das [](vssgloss-d.md) Geräteobjekt der Schattenkopie mithilfe von [**IVssBackupComponents::GetSnapshotProperties**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties) für die importierte Schattenkopie und fügt diese an den Anfang der ursprünglichen Dateipfade an, die aus den Metadaten für den Zugriff auf zu sichernde Dateien erhalten wurden.

8.  Nachdem die Schattenkopie verwendet wurde, muss die Anfordernde in *systemTwo* die Schattenkopie löschen. Wie bei nicht transportierbaren Schattenkopien wird der VSS-Dienst durch das Freigeben der [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) auf *systemTwo* dazu führen, dass der VSS-Dienst die Schattenkopie löscht, wenn der Schattenkopiekontext automatische Freigabeschattenkopien angibt (z. B. **VSS \_ CTX \_ BACKUP).** Andernfalls, wenn der Kontext eine persistente Schattenkopie angibt (z. B. **VSS \_ CTX \_ APP \_ ROLLBACK**), muss die Anfordernde in *systemTwo* die Schattenkopie explizit löschen.

    Anschließend signalisiert der Anfordernde auf *systemTwo* dem Anfordernden auf *systemOne,* dass er die Sicherung der transportierbaren Schattenkopie abgeschlossen hat.

9.  Nachdem die anfordernde Seite von *systemOne* eine Benachrichtigung erhalten hat, dass der Anfordernde auf *systemTwo* die Sicherung der transportierbaren Schattenkopie abgeschlossen hat, benachrichtigt er die Writer auf seinem System, indem er ein [**BackupComplete-Ereignis**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) mit einem Aufruf von **IVssBackupComponents::BackupComplete generiert.** An diesem Punkt kann der Anfordernde auf *systemOne* seine Instanz von [**IVssBackupComponents veröffentlichen.**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents)

**Transportierbare Schattenkopien in einem Cluster:** Transportierbare Schattenkopien müssen von außerhalb des Clusters importiert werden, solange das ursprüngliche Volume im Cluster bereitgestellt wird. Informationen zum Implementieren einer schnellen Wiederherstellung in einem Cluster finden Sie unter Schnelle Wiederherstellung [mit transportierbaren Schattenkopievolumes.](fast-recovery-using-transportable-shadow-copied-volumes.md)

 

 



