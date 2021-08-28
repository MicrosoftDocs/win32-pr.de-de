---
description: VSS ermöglicht einem Anfordernden den Zugriff auf die Schattenkopie von Volumes, die Daten für die Sicherung enthalten, und das Kopieren von Daten auf Sicherungsmedien.
ms.assetid: 187f26f2-f191-4703-9bde-3357f1ceef0c
title: Übersicht über die tatsächliche Sicherung von Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2413111467014b666d219a7a1e92efad26302e5c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475696"
---
# <a name="overview-of-actual-backup-of-files"></a>Übersicht über die tatsächliche Sicherung von Dateien

VSS ermöglicht einem Anfordernden den Zugriff auf die Schattenkopie von Volumes, die Daten für die Sicherung enthalten, und das Kopieren von Daten auf Sicherungsmedien. Writer fahren während dieses Prozesses im Allgemeinen mit dem normalen Betrieb fort. Weitere Informationen finden Sie unter [Übersicht über die Verarbeitung einer Sicherung unter VSS.](overview-of-processing-a-backup-under-vss.md)

Die folgende Tabelle zeigt die Abfolge der Aktionen und Ereignisse, die zum Sichern von Dateien erforderlich sind.




| Aktion des Anfordernden | Ereignis | Writer-Aktion | 
|------------------|-------|---------------|
| Zugreifen auf Dateien auf dem schattenkopieren Volume (siehe <a href="/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties"><strong>IVssBackupComponents::GetSnapshotProperties</strong></a>, <a href="/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop"><strong>VSS_SNAPSHOT_PROP</strong></a>) | Keine | Keine | 
| Generieren Sie die Liste der zu sichernden Dateien, und kopieren Sie Dateidaten auf Sicherungsmedien. | Keine | Keine | 
| Geben Sie den Erfolg oder Fehler der Sicherung mit <a href="/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded"><strong>IVssBackupComponents::SetBackupSucceeded an.</strong></a> | Keine | Keine | 
| Der Anfordernde gibt an, dass die Sicherung abgeschlossen wurde, indem <a href="/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete"><strong>er IVssBackupComponents::BackupComplete aufruft.</strong></a> | <a href="vssgloss-b.md"><em>BackupComplete</em></a> | Führen Sie alle Bereinigungen nach der Sicherung durch (siehe <a href="/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupcomplete"><strong>CVssWriter::OnBackupComplete</strong></a>, <a href="/windows/desktop/api/VsWriter/nl-vswriter-ivsswritercomponents"><strong>IVssWriterComponents</strong></a>, <a href="/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent"><strong>IVssComponent</strong></a>). | 
| Der Anfordernde wartet darauf, dass alle Writer den Empfang des <a href="/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete"><strong>IVssBackupComponents::BackupComplete-Ereignisses</strong></a> mithilfe von <a href="/windows/desktop/api/Vss/nn-vss-ivssasync"><strong>IVssAsync bestätigen.</strong></a> Außerdem sollte der Writerstatus überprüft werden (siehe <a href="/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus"><strong>IVssBackupComponents::GatherWriterStatus</strong></a>, <a href="/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus"><strong>IVssBackupComponents::GetWriterStatus</strong></a>). Der Anfordernde muss <strong>gatherWriterStatus</strong> zu diesem Zeitpunkt aufrufen, damit die Writersitzung in einen abgeschlossenen Zustand gesetzt wird.<blockquote>[!Note]<br />Dies ist nur auf Windows Server 2008 mit Service Pack 2 (SP2) und früher erforderlich.</blockquote><br /> | Keine | Keine | 
| Speichern Sie das Sicherungskomponentendokument und jedes Writer-Metadatendokument in XML-Dokumenten, die auf das Sicherungsmedium geschrieben werden können (siehe <a href="/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-saveasxml"><strong>IVssBackupComponents::SaveAsXML</strong></a> und <a href="/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-saveasxml"><strong>IVssExwriterMetadata::SaveAsXML</strong></a>). | Keine | Keine | 




 

## <a name="writer-actions-during-backup-of-files"></a>Writeraktionen während der Sicherung von Dateien

Nachdem die Schattenkopie abgeschlossen wurde, sollten alle E/A-Vorgänge auf dem System, das gesichert wird, fortgesetzt werden können, ohne die Integrität der Sicherung zu unterbrechen. Dies ist einer der Hauptgründe für die Schattenkopiefunktion.

Daher gibt es wie in [](overview-of-the-backup-discovery-phase.md)der Ermittlungsphase (siehe Übersicht über die Sicherungsermittlungsphase) einige Anforderungen an die Writer, während Dateien tatsächlich gesichert werden.

Nachdem eine Sicherung abgeschlossen wurde und ein Ansucher ein [*BackupComplete-Ereignis*](vssgloss-b.md) generiert hat, aufruft VSS die [**CVssWriter::OnBackupComplete-Methode**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupcomplete) jedes Writers, eine virtuelle Methode, die standardmäßig einfach **TRUE** zurückgibt. Writer können jedoch die Standardimplementierung außer Kraft setzen und Aktionen wie das Entfernen verbleibender temporärer Dateien ausführen oder die [**IVssWriterComponents-Schnittstelle**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswritercomponents) verwenden, mit der sie aufgerufen werden, um den Status der Sicherung jeder enthaltenen enthaltenen Komponenten (und aller Komponenten, die sie definieren können) durch Abrufen des entsprechenden [**IVssComponent-Objekts**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) zu überprüfen. [](vssgloss-e.md) [](vssgloss-c.md) Der Writer kann dann den Erfolg oder Fehler der Sicherung durch Aufrufen von [**IVssComponent:GetBackupSucceeded bestimmen**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupsucceeded)und entsprechend agieren. Der von **IVssComponent:GetBackupSucceeded** zurückgegebene Wert ist nur **TRUE,** wenn [](vssgloss-i.md) alle explizit in die [](vssgloss-s.md) Komponente eingeschlossenen Dateien und alle implizit eingeschlossenen Unterkomponenten erfolgreich sichern wurden.

Wenn der Aufruf von [**CVssWriter::OnBackupComplete**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupcomplete) abgeschlossen ist, sollte der Anfordernde ein letztes Mal [**IVssBackupComponents::GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) und [**IVssBackupComponents::GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) (für jeden Writer) aufrufen. Der Sitzungszustandsspeicher des Writers ist eine begrenzte Ressource, und Writer müssen schließlich Sitzungszustände wiederverwenden. Dieser Schritt markiert den Sicherungssitzungsstatus des Writers als abgeschlossen und benachrichtigt VSS, dass dieser Sicherungssitzungsslot von einem nachfolgenden Sicherungsvorgang wiederverwendet werden kann.

## <a name="requester-actions-during-backup-of-files"></a>Aktionen des Anfordernden während der Sicherung von Dateien

Wie unter [Übersicht über die Sicherungsermittlungsphase](overview-of-the-backup-discovery-phase.md)erwähnt, sollten Sie die tatsächliche Liste der zu sichernden Dateien erst generieren, wenn die Schattenkopie abgeschlossen ist.

Das [*Geräteobjekt,*](vssgloss-d.md) das der Schattenkopie eines bestimmten Volumes entspricht, wird verwendet, um zugriff auf Dateien auf dem kopierten Schattenvolumen zu erhalten, nachdem die Schattenkopie abgeschlossen wurde. Das Geräteobjekt wird aus dem [**VSS \_ SNAPSHOT \_ PROP-Objekt**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) erhalten, das von [**IVssBackupComponents::GetSnapshotProperties zurückgegeben wird.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties) Jede Schattenkopie eines Schattenkopiesets hat ein eigenes Geräteobjekt.

Das Geräteobjekt und die Pfade, die aus den Spezifikationen des Writer-Metadatendokuments der Komponenten ermittelt wurden, werden dann verwendet, um Dateien für die Sicherung auszuwählen. Weitere [Informationen finden Sie unter Requester Access to Shadow Copied Data](requestor-access-to-shadow-copied-data.md) (Zugriff des Anfordernden auf schattenkopierte Daten).

Welche Dateien in der Sicherungsliste enthalten sein werden, hängt [](vssgloss-s.md)von der Art der jeweiligen Sicherung, der Komponentenauswahl für die Sicherung und der logischen Pfadstruktur des Writers ab (siehe [Working with Selectability for Backup](working-with-selectability-for-backup.md)).

Zusätzlich zu den dateien, die in den Komponenten angegeben sind, kann ein angegebener Writer auch Explizit ausgeschlossene Dateien haben. Der Dateiausschluss muss immer beachtet werden, unabhängig davon, welche Komponenten ausgewählt sind.

Wie unter Übersicht [über](overview-of-the-backup-discovery-phase.md)die Sicherungsermittlungsphase erwähnt, kann ein bereitgestellter Ordner oder Einparpunkt in einer Schattenkopie angezeigt und gesichert werden. Ein bereitgestellter Ordner oder Einparpunkt kann jedoch nicht auf dem schattenkopierten Volume durchlaufen werden (siehe Arbeiten mit bereitgestellten Ordnern und [Parsepunkten](working-with-reparse-and-mount-points.md)).

Wenn der alternative Pfad, der von [](vssgloss-a.md) [**IVssWMFiledesc::GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) zurückgegeben wird, nicht leer ist, sollten Sie auch während eines Sicherungsvorgang mit Vorsicht darauf achten. Ein alternativer Pfad [](vssgloss-a.md) unterscheidet sich von einer alternativen Speicherortzuordnung, da er nur während Sicherungen verwendet wird, während eine alternative Speicherortzuordnung nur bei Wiederherstellungen verwendet wird.

In diesem Fall müssen die Daten nicht von ihrem normalen Speicherort (angegeben durch [**IVssWMFiledesc::GetPath),**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getpath)sondern von dem speicherort, der von [**IVssWMFiledesc::GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation)zurückgegeben wird, sichern. Bei der Wiederherstellung sollte die Datei an ihren normalen Speicherort zurückgegeben werden. Weitere Informationen finden Sie unter Nicht [standardmäßige Sicherungs- und](non-default-backup-and-restore-locations.md) Wiederherstellungsspeicherorte.

VSS legt keine Einschränkungen hinsichtlich des tatsächlichen Mechanismus zum Sichern von Daten auf einem Speichermedium oder der Auswahl dieses Mediums fest. Es wird jedoch empfohlen, die Dateien jeder Komponente jeder [*Writerinstanz*](vssgloss-w.md) als Einheit zu verarbeiten. Unter [Generieren eines Sicherungssets](generating-a-backup-set.md) finden Sie eine Erörterung der bewährten Methoden zum Generieren der Sicherungsdateiliste.

Der Erfolg oder Fehler beim Sichern von Dateien, die von einer bestimmten Komponente [](vssgloss-s.md) verwaltet werden, und (wenn sie einen Komponentensatz [*definiert),*](vssgloss-c.md)sollten ihre Unterkomponenten für eine bestimmte Writerinstanz im Sicherungskomponentendokument beibehalten werden, indem [**IVssBackupComponents::SetBackupSucceededaufgerufen wird.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded) Wenn eine Datei, die von einer Komponente oder einem Komponentensatz verwaltet wird, nicht sichern kann, wird für die gesamte Komponente ein Fehler bezeichnet. Genaue Informationen darüber, welche Datei nicht sichern konnte, sollten immer protokolliert werden.

Entwickler können es hilfreich finden, einen Datensatz auf dem Sicherungsmedium zu speichern, auf dem dateien gesichert werden, in welchen Komponenten und Komponentensatz sie Mitglied waren, welche Spezifikationen sie hatten und wie ihre ursprünglichen Pfade waren. Es kann auch nützlich sein, Informationen wie die Komponentendefinition jedes Writers zu speichern. Dies kann den Abrufvorgang vereinfachen. Diese Details bleiben jedoch dem Entwickler der anfordernden Seite erhalten.

Da Writer das Sicherungskomponentendokument beim Behandeln des [**PostSnapshot-Ereignisses**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot) ändern können, das durch den Aufruf von [**IVssBackupComponents::D oSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)generiert wurde, sollte das Sicherungskomponentendokument erst nach Abschluss dieses asynchronen Aufrufs gespeichert werden.

Obwohl dies bereits früher der Fall sein kann, ist dies auch ein praktischer Zeitpunkt zum Speichern des Writer-Metadatendokuments.

Es ist sehr wichtig, dass sowohl das Sicherungskomponentendokument als auch die Writer-Metadatendokumente mithilfe von [**IVssBackupComponents::SaveAsXML**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-saveasxml) und [**IVssExerklärWriterMetadata::SaveAsXML**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-saveasxml)beibehalten werden. Wenn nicht, ist es nicht möglich, VSS während der Dateiwiederherstellung zu verwenden.

Zusätzlich zum Speichern der ursprünglichen Metadaten kann es für einige Sicherungsanwendungen nützlich sein, eine Kopie ihrer eigenen Liste der Dateien (in ihrem eigenen optimierten Format) und der zugehörigen Writer-, Komponenten-, Wiederherstellungsprozedur- und Speicherortinformationen zum späteren Abrufen auf dem Sicherungsmedium zu speichern. Eine solche Liste kann verwendet werden, um einige der Analyse und den Vergleich von Writer-Metadatendokumenten und sicherungskomponentendokumenten während der Wiederherstellung zu vermeiden.

Zu sichernde Volumes verfügen möglicherweise über Daten, die nicht von VSS Writer verwaltet werden. Diese Daten können und sollten aus dem kopierten Schattenvolumen in einem absturzeinheitlichen [*Zustand gespeichert werden.*](vssgloss-c.md) Weitere Informationen finden Sie unter Sicherungen ohne [Writer-Beteiligung.](backups-without-writer-participation.md)

 

 




