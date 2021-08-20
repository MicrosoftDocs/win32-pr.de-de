---
description: 'Um einen inkrementellen oder differenziellen Sicherungsvorgang zu unterstützen, muss ein Anfordernde folgende Schritte durchführen:'
ms.assetid: a77700e3-8217-460e-bec9-1041d03eec41
title: An anfordernde Rolle in inkrementellen und differenziellen VSS-Sicherungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 637d4bf97b97d484080c85a2345599a05e4bbd89f88a0c1786b5bda911a83331
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118122005"
---
# <a name="requester-role-in-vss-incremental-and-differential-backups"></a>An anfordernde Rolle in inkrementellen und differenziellen VSS-Sicherungen

Um einen [*inkrementellen*](vssgloss-i.md) [*oder differenziellen Sicherungsvorgang*](vssgloss-d.md) zu unterstützen, muss ein Anfordernde folgende Schritte durchführen:

1.  Bestimmen Sie, in welchem Grad Writer-Unterstützung verfügbar ist (mithilfe von [**IVssBackupComponents::GetWriterMetadata,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata) um Zugriff auf Informationen in Writer-Metadatendokumenten zu erhalten), und bestimmen Sie insbesondere, welches Sicherungsschema unterstützt wird ([**VSS \_ BACKUP \_ SCHEMA**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema)).
2.  Legen Sie einen geeigneten Sicherungsstatus fest.
3.  Abrufen von Spezifikationen auf Datei- und Dateisatzebene für eine inkrementelle oder differenzielle Sicherung.
4.  Führen Sie die Sicherung aus.

## <a name="requester-determination-of-incremental-and-differential-support-and-configuration"></a>Bestimmen der inkrementellen und differenziellen Unterstützung und Konfiguration durch den An anfordernden

Ein Anfordernde muss Informationen zur Writerunterstützung abrufen, bevor er Komponenten für die Aufnahme in eine inkrementelle oder differenzielle Sicherung oder das Festlegen eines eigenen Zustands auswählt.

<dl> <dt>

<span id="Determining_Writer_Support"></span><span id="determining_writer_support"></span><span id="DETERMINING_WRITER_SUPPORT"></span>Bestimmen der Writer-Unterstützung
</dt> <dd>

Ein Anfrager bestimmt, ob ein angegebener Writer inkrementelle oder differenzielle VSS-Sicherungen unterstützt, indem er die Sicherungsschemamaske des Writers mithilfe der [**IVssExwriterMetadata::GetBackupSchema-Methode**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema) abruft.

Die Sicherungsschemamaske eines Writers, der inkrementelle oder differenzielle VSS-Techniken unterstützt, enthält **entweder VSS \_ BS \_ INCREMENTAL** oder **VSS \_ BS \_ DIFFERENTIAL** oder beides. Writer können auch Einschränkungen für ihre Teilnahme mit dem **\_ VSS BS \_ EXCLUSIVE INCREMENTAL \_ \_ DIFFERENTIAL-Flag** angeben. (Weitere Informationen zu Sicherungsschemas finden Sie unter [**VSS \_ BACKUP \_ SCHEMA.**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema)

</dd> <dt>

<span id="Setting_Requester_Backup_State"></span><span id="setting_requester_backup_state"></span><span id="SETTING_REQUESTER_BACKUP_STATE"></span>Festlegen des Sicherungsstatus des Anfordernden
</dt> <dd>

Eine Anfordernde gibt an, dass es sich bei einer Sicherung um eine inkrementelle oder differenzielle Sicherung handelt, indem ein Sicherungstyp entweder auf **VSS \_ BT \_ INCREMENTAL** oder **VSS \_ BT \_ DIFFERENTIAL** mithilfe der [**IVssBackupComponents::SetBackupState-Methode**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate) festgelegt wird, bevor ein [**PrepareForBackup-Ereignis**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) generiert wird.

Die [**IVssBackupComponents::SetBackupState-Methode**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate) wird auch verwendet, um anzugeben, ob der Anfordernde partielle Dateiunterstützung [*bietet,*](vssgloss-p.md)die häufig verwendet wird, um bestimmte inkrementelle Sicherungs- und Wiederherstellungsvorgänge zu implementieren.

</dd> </dl>

## <a name="getting-writer-specifications-for-incremental-and-differential-backups"></a>Abrufen von Writerspezifikationen für inkrementelle und differenzielle Sicherungen

Die Dateisicherungsspezifikationsinformationen auf Dateisatzebene ([**VSS \_ FILE SPEC BACKUP \_ \_ \_ TYPE**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type)), die im Writer-Metadatendokument jedes Writers enthalten sind, können nach der erfolgreichen Rückgabe von [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata)untersucht werden.

Ein Writer kann jedoch differenzierte Dateien [](vssgloss-p.md) [*hinzufügen*](vssgloss-d.md) oder nach teilweiser Dateiunterstützung fragen, bis die Verarbeitung des [*PostSnapshot-Ereignisses erfolgreich war.*](vssgloss-p.md)

Differenzierte Datei- und Teildateiunterstützungsspezifikationen können den Dateispezifikations-Sicherungstyp überschreiben, sodass anfordernde Benutzer möglicherweise eine vollständige Analyse aller Writerspezifikationen zu inkrementellen und differenziellen Sicherungen bis nach der erfolgreichen Rückgabe von [**IVssBackupComponents::P repareForBackup zurückversetzen möchten.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup)

<dl> <dt>

<span id="Getting_File_Backup_Specification_Information"></span><span id="getting_file_backup_specification_information"></span><span id="GETTING_FILE_BACKUP_SPECIFICATION_INFORMATION"></span>Abrufen von Dateisicherungsspezifikationsinformationen
</dt> <dd>

Die Dateisicherungsspezifikationsinformationen auf Dateisatzebene ([**VSS \_ FILE SPEC BACKUP \_ \_ \_ TYPE**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type)) sind im Writer-Metadatendokument jedes Writers enthalten und können unmittelbar nach der erfolgreichen Rückgabe von [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata)überprüft werden.

Anfordernde müssen Dateisicherungsspezifikationsmasken ([**VSS \_ FILE SPEC BACKUP \_ \_ \_ TYPE**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type)) für jeden Dateisatz jeder Komponente eines Writers abrufen, die [](vssgloss-i.md) in die inkrementelle oder differenzielle Sicherung eingeschlossen werden sollen, unabhängig davon, ob die Komponente explizit oder implizit eingeschlossen wurde. [](vssgloss-e.md)

Ein Anfrager kann mithilfe von [**IVssBackupComponents::GetWriterComponentsCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponentscount) und [**IVssBackupComponents::GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents)bestimmen, welches Writer-Metadatendokument abgefragt werden muss. Die Instanz der [**IVssWriterComponentsExt-Schnittstelle,**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext) die von **IVssBackupComponents::GetWriterComponents** zurückgegeben wird, stellt Writerinformationen über die [**IVssWriterComponentsExt::GetWriterInfo-Methode**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getwriterinfo) bereit.

Der Anfordernde erhält Komponenteninformationen über Instanzen der [**IVssWMComponent-Schnittstelle,**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) die einer eingeschlossenen Komponente entspricht, die von einem bestimmten Writer mithilfe von [**IVssExerklärWriterMetadata::GetComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getcomponent)verwaltet wird.

Die Informationen zu Dateisätzen, die von der Komponente verwaltet werden, die der [**IVssWMComponent-Schnittstelle**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) entspricht, werden durch Aufrufe von [**IVssWMComponent::GetFile,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getfile) [**IVssWMComponent::GetDatabaseFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabasefile)oder [**IVssWMComponent::GetDatabaseLogFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabaselogfile) (entsprechend) erhalten.

Diese Aufrufe können Instanzen der [**IVssWMFiledesc-Schnittstelle**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) für jeden der Dateisätze einer Komponente zurückgeben.

Der Sicherungstyp der Dateispezifikation eines Dateisets wird durch Aufrufen von [**IVssWMFiledesc::GetBackupTypeMask ermittelt.**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getbackuptypemask)

</dd> <dt>

<span id="Getting_Partial_File_and_Differenced_File_Information"></span><span id="getting_partial_file_and_differenced_file_information"></span><span id="GETTING_PARTIAL_FILE_AND_DIFFERENCED_FILE_INFORMATION"></span>Abrufen von Informationen zu teil- und differenzierten Dateien
</dt> <dd>

Ein Anfordernder erhält partielle Datei- und differenzierte Dateiinformationen über die [**IVssComponent-Schnittstelle.**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent)

Ein An anfordernder Benutzer kann alle Writer, die in einer Sicherung enthalten sind, mithilfe von [**IVssBackupComponents::GetWriterComponentsCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponentscount) und [**IVssBackupComponents::GetWriterComponents iterieren.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents)

Die Instanz einer [**IVssWriterComponentsExt-Schnittstelle,**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext) die von [**IVssBackupComponents::GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents) zurückgegeben wird, ermöglicht den Zugriff auf alle [](vssgloss-e.md) Instanzen der [**IVssComponent-Schnittstelle,**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) die den explizit eingeschlossenen Komponenten eines bestimmten Writers über die [**Methoden IVssWriterComponentsExt::GetComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getcomponent) und [**IVssWriterComponentsExt::GetComponentCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getcomponentcount) entspricht.

Ein An anfordernder Benutzer muss alle Instanzen von [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) für alle Writer durchgehen, deren Schema die inkrementelle oder differenzielle Sicherung unterstützt, d. h. Writer, deren Sicherungsschemamaske, wie von [**IVssExwriterMetadata::GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema)zurückgegeben, **VSS \_ BS \_ INCREMENTAL** enthält, wenn der Sicherungstyp **VSS \_ BT \_ INCREMENTAL** ist, oder **VSS \_ BS \_ DIFFERENTIAL,** wenn der Sicherungstyp **VSS \_ BS \_ DIFFERENTIAL** ist.

Partielle Dateiinformationen werden durch Aufrufen von [**IVssComponent::GetPartialFileCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfilecount) und [**IVssComponent::GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile) (siehe Arbeiten mit Teildateien) [ermittelt.](working-with-partial-files.md)

Für Writer, die Sicherungsvorgänge auf der Grundlage der letzten Änderungsdaten einer Datei unterstützen (Writer, deren Sicherungsschemamaske, wie von [**IVssExerklärwriterMetadata::GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema)zurückgegeben, **VSS \_ BS \_ LAST \_ MODIFY** enthält), werden differenzierte Dateiinformationen durch Aufrufen von [**IVssComponent::GetDifferencedFilesCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfilescount) und [**IVssComponent::GetDifferencedFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfile)erhalten.

Beachten Sie, dass es sich bei unterschiedlichen Dateien möglicherweise um neue Dateien handelt, d.&a; Dateien, die derzeit im Writer-Metadatendokument eines bestimmten Writers keine Mitglieder eines Dateisets sind.

Anfordernde sollten dateien nicht finden, die sowohl für partielle Dateivorgänge als auch als differenzierte Dateien enthalten sind. Wenn ein Anmelder auf einen solchen Fall trifft, sollte er einen Writerfehler zurückgeben und protokollieren.

Ein Anfordernde kann weiterhin mit dem Sichern der Dateien des problematischen Writers fortfahren. In diesem Fall sollte dies jedoch gemäß der Spezifikation in den differenzierten Dateiinformationen der Fall sein.

</dd> </dl>

## <a name="implementing-incremental-or-differential-backups"></a>Implementieren von inkrementellen oder differenziellen Sicherungen

Vor der Implementierung einer Sicherung sollten Anfrager [](vssgloss-i.md) über [](vssgloss-d.md) Informationen darüber verfügen, welche Writer eine inkrementelle oder differenzielle Sicherung, alle angeforderten Teildateivorgänge, alle differenzierten Dateien und den Dateispezifikations-Sicherungstyp aller anderen Dateien unterstützen.

<dl> <dt>

<span id="Nonsupporting_Writers"></span><span id="nonsupporting_writers"></span><span id="NONSUPPORTING_WRITERS"></span>Nicht unterstützte Writer
</dt> <dd>

Writer, deren Schema die inkrementelle oder differenzielle Sicherung nicht unterstützt (Writer, deren Sicherungsschemamaske, wie von [**IVssExerklärwriterMetadata::GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema)zurückgegeben, **VSS \_ BS \_ INCREMENTAL** enthält, wenn der Sicherungstyp **VSS \_ BT \_ INCREMENTAL** ist oder **vss \_ BS \_ DIFFERENTIAL** nicht enthält, wenn der Sicherungstyp VSS BS DIFFERENTIAL ist), können keine direkte Unterstützung für einen inkrementellen oder differenziellen **\_ Sicherungsvorgang \_** bereitstellen.

Dies bedeutet nicht unbedingt, dass die Daten der Writer nicht an einem inkrementellen oder differenziellen Sicherungsvorgang beteiligt sind. Die Entscheidung, was zu tun ist, liegt jedoch im Ermessen des Anfordernden. Der Anfordernde kann eine der folgenden Aufgaben unternehmen:

-   Sichern Sie keine Dateien, die zu den nicht unterstützten Writern gehören (geben Sie dies für den Benutzer eindeutig an).
-   Sichern aller Dateien von nicht unterstützten Writern
-   Führen Sie eine inkrementelle Sicherung mithilfe von Dateisystemdaten und den eigenen Verlaufsprotokollen des Anfordernden durch.

Die letzte Alternative sollte mit großer Sorgfalt verwendet werden, und dies nur, wenn der Anfordernde versteht, ob die beteiligten Writer die inkrementelle oder differenzielle Sicherung und Wiederherstellung von Daten unabhängig vom VSS-Mechanismus unterstützen können.

</dd> <dt>

<span id="Supporting_Writers"></span><span id="supporting_writers"></span><span id="SUPPORTING_WRITERS"></span>Unterstützen von Writern
</dt> <dd>

Ein Anfordernde muss (in der reihenfolge) alle differenzierten Dateien eines [](vssgloss-p.md) Writers [*verarbeiten,*](vssgloss-d.md)dann alle teiliellen Dateianforderungen verarbeiten und dann die verbleibenden Dateien entsprechend ihrem Dateispezifikations-Sicherungstyp sichern ([**VSS FILE \_ SPEC BACKUP \_ \_ \_ TYPE**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type)).

1.  **Sichern differenzisierter Dateien:**

    Für Writer, die Sicherungsvorgänge auf der Grundlage der letzten Änderungsdaten unterstützen (Writer, deren Sicherungsschemamaske, wie von [**IVssExerklärwriterMetadata::GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema)zurückgegeben, **VSS \_ BS \_ LAST \_ MODIFY** enthält), verwendet ein An anfordernder den Pfad, die Dateispezifikation und die Informationen zum Rekursionsflag, die von [**IVssComponent::GetDifferencedFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfile) zurückgegeben werden, um eine Liste von Dateien als Kandidaten für die inkrementelle Sicherung oder Wiederherstellung zu generieren.

    [**IVssComponent::GetDifferencedFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfile) kann auch einen Zeitpunkt der letzten Änderung zurückgeben (ausgedrückt als [**FILETIME-Struktur).**](/windows/win32/api/minwinbase/ns-minwinbase-filetime)

    Wenn der zeitpunkt der letzten Änderung, der vom Writer angegeben wird, ungleich 0 (null) ist, verwendet der Anfordernde diese als Grundlage (anstelle [](vssgloss-i.md) von [](vssgloss-d.md) Dateisysteminformationen oder den eigenen gespeicherten Daten des Anfordernden), um zu bestimmen, ob die Datei in die inkrementelle oder differenzielle Sicherung einbezogen werden soll.

    Dies ist beispielsweise der Fall, wenn der Zeitpunkt der letzten Änderung einer Datei wie vom Writer zurückgegeben:

    -   Nach der letzten vollständigen Sicherung sollte die Datei sowohl in inkrementellen als auch differenziellen Sicherungen enthalten sein.
    -   Nach der letzten vollständigen Sicherung, aber vor der letzten inkrementellen Sicherung sollte die Datei in inkrementelle Sicherungsvorgänge eingeschlossen werden, aber keine differenziellen Sicherungen.

    Wenn der zeitpunkt der letzten Änderung, der vom Writer angegeben wird, 0 (null) ist, muss der Anfordernde Dateisysteminformationen und seine eigenen gespeicherten Daten verwenden, um den Änderungszeitpunkt der differenzierten Datei zu bestimmen.

2.  **Verwenden von Teildateivorgängen:**

    Wenn ein Writer angefordert hat, dass eine Datei mit einem teiliellen Dateivorgang gesichert wird, verwendet der Anfordernde die Dateioffsetinformationen, um die angegebenen Dateisegmente auf Sicherungsmedien zu speichern. (Weitere [Informationen zu Partiellen Dateivorgängen](working-with-partial-files.md) finden Sie unter Arbeiten mit Teildateien.

    Wie bereits erwähnt, sollte ein Writer eine Datei nicht sowohl als differenzierte Datei als auch als Teilnehmer an einem Teildateivorgang festlegen. Wenn ein Anmelder auf einen solchen Fall trifft, sollte er einen Writerfehler zurückgeben und protokollieren.

    Ein Anfordernde kann weiterhin mit dem Sichern der Dateien des problematischen Writers fortfahren. In diesem Fall sollte dies jedoch gemäß der Spezifikation in den differenzierten Dateiinformationen der Fall sein.

3.  **Arbeiten mit dem Dateispezifikations-Sicherungstyp:**

    Nachdem alle differenzierten Dateien und teiliellen Dateivorgänge verarbeitet wurden, verarbeitet der Anfordernde nun alle verbleibenden Dateien im Sicherungssatz auf Der Grundlage seines Dateispezifikations-Sicherungstyps ([**VSS \_ FILE SPEC BACKUP \_ \_ \_ TYPE**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type)).

    Es gibt drei "Sicherungs erforderlich"-Werte der [**VSS \_ FILE SPEC \_ BACKUP \_ \_ TYPE-Enumeration,**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) die sich auf differenzielle und inkrementelle Sicherungen auswirken:

    -   VSS \_ \_ FSBT: ALLE \_ \_ SICHERUNGEN ERFORDERLICH
    -   VSS \_ FSBT: \_ INKREMENTELLE \_ SICHERUNG \_ ERFORDERLICH
    -   VSS FSBT DIFFERENTIAL BACKUP REQUIRED (VSS \_ \_ FSBT-DIFFERENZIELLE \_ \_ SICHERUNG ERFORDERLICH)

    Es gibt drei "Schattenkopien erforderlich"-Werte:

    -   VSS \_ FSBT \_ ALLE \_ MOMENTAUFNAHMEN \_ ERFORDERLICH
    -   VSS \_ FSBT: \_ INKREMENTELLE \_ \_ MOMENTAUFNAHME ERFORDERLICH
    -   VSS FSBT DIFFERENTIAL SNAPSHOT REQUIRED (VSS \_ \_ FSBT-DIFFERENZIELLE \_ \_ MOMENTAUFNAHME ERFORDERLICH)

    Dateisätze, die mit dem Dateispezifikationssicherungstyp "Schattenkopie erforderlich" gekennzeichnet sind, geben an, dass ein Ansteller Daten aus einer Schattenkopie kopieren muss, wenn er INKREMENTELLE, DIFFERENZIELLE oder ALL-Sicherungsvorgänge (einschließlich inkrementeller und differenzieller Vorgänge) ausführen muss.

    Das Flag "Sicherung erforderlich", das auf INCREMENTAL-, DIFFERENTIAL- oder ALL-Sicherungsvorgänge angewendet wird, gibt an, dass der Writer erwartet, dass nach der Wiederherstellung eines Sicherungsvorgang eine Kopie der aktuellen Version des Dateisets verfügbar ist. Dies bedeutet in der Regel, dass ein An anfordernde Mitarbeiter alle Seine Elemente während einer inkrementellen oder differenziellen Sicherung auf sicherungsmedien kopiert, wenn ein Dateisatz mit "Sicherung erforderlich" gekennzeichnet ist, unabhängig davon, wann die Sicherung oder Änderung zuletzt erfolgt ist.

    Standardmäßig werden Dateisätze zu Komponenten mit dem Dateispezifikationssicherungstyp VSS \_ FSBT \_ ALL BACKUP REQUIRED \_ \_ \| VSS \_ FSBT ALL SNAPSHOT REQUIRED \_ \_ \_ hinzugefügt. Wenn ein Writer den Sicherungstyp der Dateispezifikation nicht explizit festgelegt hat, müssen an anfordernde Personen daher diese Dateien kopieren, die nicht von partiellen Dateivorgängen verarbeitet werden, oder bestimmte differenzierte Dateien in den meisten Dateisätzen werden in der Regel vollständig auf Sicherungsmedien kopiert.

</dd> <dt>

<span id="Backup_Stamps"></span><span id="backup_stamps"></span><span id="BACKUP_STAMPS"></span>Sicherungsstempel
</dt> <dd>

Writer, die Sicherungsstempel (VSS BS TIMESTAMP) unterstützen, können Sicherungsstempelinformationen generieren, die zur Unterstützung zukünftiger inkrementeller und differenzieller Sicherungs- und \_ \_ Wiederherstellungsvorgänge verwendet werden sollen.

Das Format und die Informationen in Zeichenfolgen, die Sicherungsstempelinformationen enthalten, sind für den Writer, der sie generiert, privat. der Anfordernde weiß nicht, wie diese Informationen zu verarbeiten sind.

Unterstützende Writer speichern den Sicherungsstempel im Sicherungskomponentendokument mithilfe der [**IVssComponent::SetBackupStamp-Methode**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp) als Zeichenfolge.

Die Rolle der Anfordernden bei der Verarbeitung von Sicherungsstempelinformationen besteht (sofern vorhanden), um sie dem Writer durch Aufrufen von [**IVssBackupComponents::SetPreviousBackupStamp**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setpreviousbackupstamp) in einem zukünftigen Sicherungs- oder Wiederherstellungsvorgang zur Verfügung zu stellen.

</dd> </dl>

 

 
