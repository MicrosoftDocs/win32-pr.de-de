---
description: Es ist manchmal wünschenswert, eine Schatten Kopie auf einem System zu erstellen, aber die Schatten Kopie auf einem zweiten System zu verwenden.
ms.assetid: 4ec63917-03c0-434e-892e-3d9d4c47740e
title: Importieren transportable schattenkopierter Volumes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d259fbc047d088ee1f7064804a3ee98fe48da1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131280"
---
# <a name="importing-transportable-shadow-copied-volumes"></a>Importieren transportable schattenkopierter Volumes

Es ist manchmal wünschenswert, eine Schatten Kopie auf einem System zu erstellen, aber die Schatten Kopie auf einem zweiten System zu verwenden.

Beachten Sie, dass die zu sichernden Daten normalerweise während des normalen Betriebs von einem bestimmten System (*SystemOne*) verwaltet werden und dass diese Daten physisch in einem Speicher Array oder einem Gerät gespeichert werden.

Um die Unterbrechung von *SystemOne* zu minimieren (da Sicherungs Vorgänge ressourcenintensiv sein können), ist es wünschenswert, die Sicherung mithilfe von *systemtwo* auszuführen, einem Sicherungs Server, der Zugriff auf das gleiche Speicher Array wie *SystemOne* hat.

Um eine korrekte Schatten Kopie zu gewährleisten – die Zusammenarbeit mit den Writern auf *SystemOne* und die Beibehaltung des Zustands für laufende Aufgaben – muss die Schatten Kopie von *SystemOne* ausgeführt werden.

Daher muss *SystemOne* eine [*austauschen-Schatten Kopie*](vssgloss-t.md)erstellen, die dann von *systemtwo* importiert wird.

**Windows Server 2003, Standard Edition, Windows Server 2003, Web Edition und Windows XP:** Transportable-schattenkopiesätze werden nicht unterstützt. Alle Editionen von Windows Server 2003 mit Service Pack 1 (SP1) unterstützen austauschen schattenkopiesätze.

Ein typisches Beispiel für das Importieren einer austauschen-Schatten Kopie kann auf folgende Weise fortgesetzt werden:

1.  Anfänglich wird die logische Einheit (LUN), die vom Speicher Array bereitgestellt wird, als Volume auf *SystemOne* eingebunden (z. b. F:).
2.  Ein Anforderer, der auf *SystemOne* ausgeführt wird, instanziiert eine Instanz von [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) und wird so fortgesetzt, als ob er eine Sicherung vorbereitet hätte. (Weitere Informationen finden Sie unter Übersicht über die [Sicherungs Initialisierung](overview-of-backup-initialization.md), [Übersicht über die Sicherungs Ermittlungs Phase](overview-of-the-backup-discovery-phase.md)und [Übersicht über Aufgaben vor der Sicherung](overview-of-pre-backup-tasks.md) .)
3.  Der Anforderer für *SystemOne* ändert den schattenkopiekontext, der in der Regel für den lokalen Sicherungs Vorgang verwendet wird (**VSS \_ ctx- \_ App- \_ Sicherung**), um anzugeben, dass eine austauschen-Schatten Kopie erstellt wird (**VSS \_ Volsnap \_ attr \_ austauschen**). Das austauschen-Attribut kann auch anderen schattenkopiekontexten hinzugefügt werden.
4.  Bei einem Schatten Kopier Kontext von **VSS \_ ctx \_ App \_ Backup** \| **VSS \_ Volsnap \_ attr \_ transportable** erstellt der Anforderer, der sich auf *SystemOne* befindet, eine Schatten Kopie durch Aufrufen von [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset).
5.  *SystemOne* verwendet [**IVssBackupComponents:: SaveAsXml**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-saveasxml) , um den aktuellen Status des Sicherungs Komponenten Dokuments zu speichern, und [**ivssexaminewrite Metadata:: SaveAsXml**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-saveasxml) , um die Writer-Metadatendokumente jedes Writers zu speichern. Die XML-Zeichen folgen, die diese Dokumente enthalten, werden dann für eine Anforderer verfügbar gemacht, die auf *systemtwo* ausgeführt wird.

    Der Anforderer überträgt das Dokument mit den Sicherungs Komponenten auf *systemtwo*.

    Beachten Sie, dass die anfordernde Person in *SystemOne* die Instanz von [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) an dieser Stelle nicht freigibt, wenn der Zweck der Schatten Kopie für die Sicherung vorgesehen ist. Die Schnittstelle sollte geöffnet bleiben, bis *systemtwo* die Sicherungs Vorgänge erfolgreich abgeschlossen hat. Nur dann sollte der Anforderer ein Backup [**Complete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) -Ereignis ausgeben, da einige Writer Protokolle abschneiden und nach einer erfolgreichen Sicherung andere Aufgaben ausführen. Wenn das Ziel der Schatten Kopie Data Mining oder anderen Zwecken ist, kann die Schnittstelle in diesem Schritt geschlossen werden.

6.  Der Anforderer auf *systemtwo* ruft dann [**IVssBackupComponents:: importshots**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-importsnapshots) auf, um Zugriff auf die Schatten Kopie zu erhalten, die von der anfordernden Person auf *SystemOne* erstellt wurde.
    > [!Note]  
    > Der Anforderer ist für das Serialisieren des Import schattenkopievorgangs verantwortlich. Wenn der Versuch von [**IVssBackupComponents:: importshots**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-importsnapshots) fehlschlägt, bereinigt der VSS LUNs nicht auf seine eigene Weise. Der Anforderer muss die Bereinigung von LUNs initiieren.

     

7.  Der Anforderer auf *systemtwo* führt die Sicherung des kopierten schattenkopierens genau so aus, als ob er eine Schatten Kopie sichern würde, die er selbst erstellt hat (siehe Übersicht über die [tatsächliche Sicherung von Dateien](overview-of-actual-backup-of-files.md)).

    Der Anforderer auf *systemtwo* Ruft das [*Geräte Objekt*](vssgloss-d.md) der Schatten Kopie mithilfe von [**IVssBackupComponents:: getsnapshotproperties**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties) auf der importierten Schatten Kopie ab und fügt diese an den Anfang der ursprünglichen Dateipfade an, die aus den Metadaten abgerufen wurden, um auf die zu sichernden Dateien zuzugreifen.

8.  Nachdem Sie die Schatten Kopie verwendet haben, muss der Anforderer auf *systemtwo* die Schatten Kopie löschen. Wie bei nicht transportierbaren Schatten Kopien *bedeutet dies,* dass der VSS-Dienst die Schatten Kopie löscht, wenn der schattenkopiekontext [**auf Schatten**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) Kopien mit automatischer Freigabe (z. b. **VSS- \_ ctx- \_ Sicherung**) hinweist. Wenn der Kontext andernfalls eine persistente Schatten Kopie (z. b. **VSS- \_ ctx- \_ App- \_ Rollback**) angibt, muss der Anforderer auf *systemtwo* explizit die Schatten Kopie löschen.

    Dann signalisiert die anfordernde Person auf *systemtwo* der anfordernden *Person, dass* Sie mit der Sicherung der austauschen-Schatten Kopie fertiggestellt wurde.

9.  Nachdem der Anforderer für *SystemOne* eine Benachrichtigung erhalten hat, dass die anfordernde Person auf *systemtwo* die Sicherung der austauschen-Schatten Kopie abgeschlossen hat, benachrichtigt er die Writer über das System, indem er ein [**Backup Complete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) -Ereignis mit einem Befehl für **IVssBackupComponents:: BackupComplete** erzeugt. An diesem Punkt kann der Anforderer auf *SystemOne* seine Instanz von [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents)freigeben.

Über **transportable Schatten Kopien in einem Cluster:** Transportable-Schatten Kopien müssen von außerhalb des Clusters importiert werden, solange das ursprüngliche Volume innerhalb des Clusters eingebunden wird. Informationen zum Implementieren einer schnellen Wiederherstellung in einem Cluster finden [Sie unter schnelle Wiederherstellung mithilfe von transportable-Schattenkopievolumes](fast-recovery-using-transportable-shadow-copied-volumes.md).

 

 



