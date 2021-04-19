---
description: VSS ermöglicht einem Anforderer den Zugriff auf die Schatten Kopie von Volumes, die Daten für die Sicherung enthalten, und das Kopieren von Daten auf das Sicherungsmedium.
ms.assetid: 187f26f2-f191-4703-9bde-3357f1ceef0c
title: Übersicht über die tatsächliche Sicherung von Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98a504ff5a41725e33a2eb27792a3c6c89d00276
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356910"
---
# <a name="overview-of-actual-backup-of-files"></a>Übersicht über die tatsächliche Sicherung von Dateien

VSS ermöglicht einem Anforderer den Zugriff auf die Schatten Kopie von Volumes, die Daten für die Sicherung enthalten, und das Kopieren von Daten auf das Sicherungsmedium. Writer setzen in der Regel während dieses Prozesses den normalen Betrieb fort. Weitere Informationen finden Sie [unter Übersicht über die Verarbeitung einer Sicherung unter VSS](overview-of-processing-a-backup-under-vss.md).

In der folgenden Tabelle wird die Abfolge der Aktionen und Ereignisse aufgeführt, die für die Sicherung der zu sichernden Dateien erforderlich sind.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Requestaktion</th>
<th>Ereignis</th>
<th>Writer-Aktion</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Zugreifen auf Dateien auf dem schattenkopierten Volume (siehe <a href="/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties"><strong>IVssBackupComponents:: getsnapshotproperties</strong></a>, <a href="/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop"><strong>VSS_SNAPSHOT_PROP</strong></a>)</td>
<td>Keine</td>
<td>Keine</td>
</tr>
<tr class="even">
<td>Generieren Sie die Liste der zu sichernden Dateien, und kopieren Sie die Datei Daten auf das Sicherungsmedium.</td>
<td>Keine</td>
<td>Keine</td>
</tr>
<tr class="odd">
<td>Geben Sie den Erfolg oder das Fehlschlagen der Sicherung mit <a href="/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded"><strong>IVssBackupComponents:: setbackupsuccess</strong></a>an.</td>
<td>Keine</td>
<td>Keine</td>
</tr>
<tr class="even">
<td>Der Anforderer gibt an, dass die Sicherung abgeschlossen wurde, indem <a href="/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete"><strong>IVssBackupComponents:: BackupComplete</strong></a>aufgerufen wird.</td>
<td><a href="vssgloss-b.md"><em>BackupComplete</em></a></td>
<td>Ausführen einer Bereinigung nach der Sicherung (siehe <a href="/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupcomplete"><strong>CVssWriter:: OnBackupComplete</strong></a>, <a href="/windows/desktop/api/VsWriter/nl-vswriter-ivsswritercomponents"><strong>ivssschreitercomponents</strong></a>, <a href="/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent"><strong>IVssComponent</strong></a>).</td>
</tr>
<tr class="odd">
<td>Der Anforderer wartet darauf, dass alle Writer den Empfang des <a href="/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete"><strong>IVssBackupComponents:: BackupComplete</strong></a> -Ereignisses mithilfe von <a href="/windows/desktop/api/Vss/nn-vss-ivssasync"><strong>IVssAsync</strong></a>bestätigen. Außerdem sollte der Writer-Status überprüft werden (siehe <a href="/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus"><strong>IVssBackupComponents:: gatherschreiterstatus</strong></a>, <a href="/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus"><strong>IVssBackupComponents:: getschreiterstatus</strong></a>). Der Anforderer muss zu diesem Zeitpunkt <strong>gatherschreibstatus</strong> auslösen, damit die Writer-Sitzung auf den Status abgeschlossen festgelegt wird.
<blockquote>
[!Note]<br />
Dies ist nur auf Windows Server 2008 mit Service Pack 2 (SP2) und früher erforderlich.
</blockquote>
<br/></td>
<td>Keine</td>
<td>Keine</td>
</tr>
<tr class="even">
<td>Speichern Sie das Dokument mit den Sicherungs Komponenten und die einzelnen Writer-Metadatendokumente in XML-Dokumenten, die auf die Sicherungsmedien geschrieben werden können (siehe <a href="/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-saveasxml"><strong>IVssBackupComponents:: SaveAsXml</strong></a> und <a href="/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-saveasxml"><strong>ivssexaminewrite Metadata:: SaveAsXml</strong></a>).</td>
<td>Keine</td>
<td>Keine</td>
</tr>
</tbody>
</table>



 

## <a name="writer-actions-during-backup-of-files"></a>Writer-Aktionen während der Sicherung von Dateien

Nachdem die Schatten Kopie abgeschlossen wurde, sollten alle e/a-Vorgänge auf dem System, das gesichert wird, fortgesetzt werden können, ohne die Integrität der Sicherung zu unterbrechen. Dies ist eine der wichtigsten Gründe für die Verwendung der Schattenkopiefunktion.

Daher gibt es wie in der Ermittlungsphase (siehe [Übersicht über die Sicherungs Ermittlungsphase](overview-of-the-backup-discovery-phase.md)) nur wenige Anforderungen an die Writer, während Dateien tatsächlich gesichert werden.

Nachdem eine Sicherung abgeschlossen wurde und ein Anforderer ein [*BackupComplete*](vssgloss-b.md) -Ereignis generiert hat, ruft VSS die [**CVssWriter:: OnBackupComplete**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupcomplete) -Methode jedes Writers auf, eine virtuelle Methode, die standardmäßig einfach **true** zurückgibt. Writer können jedoch die Standard Implementierung überschreiben und solche Aktionen ausführen, indem Sie die verbleibenden temporären Dateien entfernen, oder die mit aufgerufene [**ivsswritercomponents**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswritercomponents) -Schnittstelle verwenden, um den Zustand der Sicherung der einzelnen [*enthaltenen expliziten*](vssgloss-e.md) Komponenten (und sämtlicher [*Komponenten Sätze*](vssgloss-c.md) , die Sie definieren können) zu überprüfen, indem Sie das entsprechende [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) -Objekt abrufen. Der Writer kann dann den Erfolg oder das Fehlschlagen der Sicherung durch Aufrufen von [**IVssComponent: getbackupsuccess**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupsucceeded)ermitteln und darauf reagieren. Der von **IVssComponent: getbackuperfolgreiches** zurückgegebene Wert ist nur dann **true** , wenn alle explizit enthaltenen Dateien in der Komponente und alle implizit in eine der zugehörigen [*unter Komponenten*](vssgloss-s.md) [*eingeschlossen*](vssgloss-i.md) wurden.

Wenn der Aufruf von [**CVssWriter:: OnBackupComplete**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupcomplete) abgeschlossen ist, sollte der Anforderer ein letztes Mal [**IVssBackupComponents:: gatherschreiterstatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) und [**IVssBackupComponents:: getschreiterstatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) (für jeden Writer) aufrufen. Der Schreib Sitzungs Zustands Speicher ist eine begrenzte Ressource, und Writer müssen die Sitzungs Zustände schließlich wieder verwenden. Durch diesen Schritt wird der Status der Sicherungs Sitzung des Writers als abgeschlossen markiert und VSS benachrichtigt, dass dieser Sicherungs Sitzungs Slot von einem nachfolgenden Sicherungs Vorgang wieder verwendet werden kann.

## <a name="requester-actions-during-backup-of-files"></a>Requestaktionen während der Sicherung von Dateien

Wie in [der Übersicht über die Sicherungs Ermittlungs Phase](overview-of-the-backup-discovery-phase.md)erwähnt, sollten Sie die tatsächliche Liste der zu sichernden Dateien erst generieren, wenn die Schatten Kopie abgeschlossen ist.

Das [*Geräte Objekt*](vssgloss-d.md) , das der Schatten Kopie eines bestimmten Volumes entspricht, wird verwendet, um Zugriff auf Dateien auf dem schattenkopierten Volume zu erhalten, nachdem die Schatten Kopie abgeschlossen wurde. Das Device-Objekt wird vom [**VSS \_ Snapshot \_**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) -Replikation-Objekt abgerufen, das von [**IVssBackupComponents:: getinapshotproperties**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties)zurückgegeben wurde. Jede Schatten Kopie eines schattenkopiesatzes verfügt über ein eigenes Geräte Objekt.

Mit dem Geräte Objekt und den Pfaden, die von den Dokument Spezifikationen des Writer-Metadatendokuments abgerufen werden, werden dann Dateien für die Sicherung ausgewählt. Weitere Informationen finden [Sie unter Anforderer Zugriff auf Schatten](requestor-access-to-shadow-copied-data.md) Kopien von Daten.

Welche Dateien in der Sicherungsliste enthalten sein werden, hängt von der Art der Sicherung, von der Komponenten [*Auswahl für die Sicherung*](vssgloss-s.md)und der logischen Pfad Struktur des Writers ab (Weitere Informationen finden Sie unter [Arbeiten mit selectlichkeit für die Sicherung](working-with-selectability-for-backup.md)).

Zusätzlich zu den in den-Komponenten angegebenen Dateien können von einem bestimmten Writer auch explizit Dateien ausgeschlossen werden. Der Datei Ausschluss muss immer beachtet werden, unabhängig davon, welche Komponenten ausgewählt werden.

Auch in [der Übersicht über die Sicherungs Ermittlungs Phase](overview-of-the-backup-discovery-phase.md)kann ein bereitgestellter Ordner oder Analyse Punkt in einer Schatten Kopie angezeigt werden und gesichert werden. Ein bereitgestellter Ordner oder Analyse Punkt kann jedoch nicht auf dem schattenkopierten Volume durchsucht werden (siehe [Arbeiten mit bereitgestellten Ordnern und Analyse Punkten](working-with-reparse-and-mount-points.md)).

Die Sorgfalt sollte auch während eines Sicherungs Vorgangs erfolgen, wenn der von [**ivsswmfiledesc:: getalternateloation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) zurückgegebene [*Alternative Pfad*](vssgloss-a.md) nicht leer ist. Ein alternativer Pfad unterscheidet sich von einer [*alternativen Speicherort Zuordnung*](vssgloss-a.md) darin, dass er nur während der Sicherungen verwendet wird, während eine Alternative Speicherort Zuordnung nur während der Wiederherstellung verwendet wird.

In diesem Fall werden die Daten nicht von Ihrem normalen Speicherort (angegeben durch [**ivsswmfiledesc:: getpath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getpath)) gesichert, sondern von dem Speicherort, der von [**ivsswmfiledesc:: getalternateloation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation)zurückgegeben wird. Bei der Wiederherstellung muss die Datei an Ihren normalen Speicherort zurückgegeben werden. Weitere Informationen finden Sie unter [nicht standardmäßige Sicherungs-und Wiederherstellungs Speicherorte](non-default-backup-and-restore-locations.md) .

VSS gibt keine Einschränkungen für den eigentlichen Mechanismus der Sicherung von Daten auf einem Speichermedium oder der Wahl des Mediums an. Es wird jedoch empfohlen, dass die Dateien der einzelnen Komponenten jeder [*Writer-Instanz*](vssgloss-w.md) als Einheit verarbeitet werden. Eine Erläuterung bewährter Methoden zum Erstellen der Sicherungsdatei Liste finden Sie unter [Erstellen eines Sicherungs Satzes](generating-a-backup-set.md) .

Der Erfolg oder das Fehlschlagen der Sicherung von Dateien, die von einer bestimmten Komponente verwaltet werden, und (wenn ein [*Komponenten Satz*](vssgloss-c.md)definiert wird), sollte die [*unter Komponenten*](vssgloss-s.md) für eine bestimmte Writer-Instanz im Dokument mit den Sicherungs Komponenten beibehalten werden, indem [**IVssBackupComponents:: setbackupsuccess**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded)aufgerufen wird. Wenn eine von einer Komponente oder einem Komponenten Satz verwaltete Datei nicht gesichert werden kann, wird die gesamte Komponente als fehlerhaft bezeichnet. Genaue Informationen darüber, welche Datei nicht gesichert werden konnte, sollten immer protokolliert werden.

Entwickler finden es möglicherweise hilfreich, einen Datensatz auf dem Sicherungsmedium zu speichern, von dem die Dateien gesichert werden, die Komponenten und Komponenten, in denen Sie Mitglied sind, ihre Spezifikation und deren ursprüngliche Pfade. Es kann auch hilfreich sein, Informationen wie die Komponenten Definition jedes Writers zu speichern. Dies kann den Abruf Vorgang vereinfachen. Diese Details werden jedoch dem Anforderer-Entwickler überlassen.

Da Writer das Dokument mit den Sicherungs Komponenten ändern können, während das [**PostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot) -Ereignis verarbeitet wird, das durch den Anforderer-Befehl von [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)generiert wurde, sollte das Dokument mit den Sicherungs Komponenten erst gespeichert werden, nachdem der asynchrone Vorgang abgeschlossen wurde.

Obwohl es möglicherweise schon früher stattfindet, ist dies auch ein bequemer Zeitpunkt, das Writer-Metadatendokument zu speichern.

Es ist sehr wichtig, dass das Dokument mit den Sicherungs Komponenten und die Writer-Metadatendokumente mithilfe von [**IVssBackupComponents:: SaveAsXml**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-saveasxml) und [**ivssexamineschreitermetadata:: SaveAsXml**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-saveasxml)beibehalten werden. Wenn dies nicht der Fall ist, kann VSS beim Wiederherstellen der Datei nicht verwendet werden.

Zusätzlich zum Speichern der ursprünglichen Metadaten ist es für einige Sicherungs Anwendungen möglicherweise hilfreich, eine Kopie Ihrer eigenen Liste der Dateien (in Ihrem eigenen optimierten Format) – und deren zugeordneten Writer, Komponenten, Wiederherstellungs Prozeduren und Standortinformationen – auf den Sicherungsmedien zu speichern, damit Sie später abgerufen werden können. Eine solche Liste kann verwendet werden, um die Verarbeitung und den Vergleich von Writer-Metadatendokumenten und den Dokumenten der Sicherungs Komponente während der Wiederherstellung zu vermeiden.

Volumes, die gesichert werden, verfügen möglicherweise über Daten, die nicht von VSS-Writern verwaltet werden. Diese Daten können und aus dem Schatten kopierten Volume gesichert werden, wo Sie sich in einem [*Absturz konsistenten Zustand*](vssgloss-c.md)befinden. Weitere Informationen finden Sie unter [Sicherungen ohne Writer-Teilnahme](backups-without-writer-participation.md) .

 

 




