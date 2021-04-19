---
description: 'Um einen inkrementellen oder differenziellen Sicherungs Vorgang zu unterstützen, muss ein Anforderer Folgendes ausführen:'
ms.assetid: a77700e3-8217-460e-bec9-1041d03eec41
title: Requestrolle in inkrementellen und differenziellen VSS-Sicherungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 718a5a0b22d9cc1cfa31404b3a0ac71a3a07731f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345891"
---
# <a name="requester-role-in-vss-incremental-and-differential-backups"></a>Requestrolle in inkrementellen und differenziellen VSS-Sicherungen

Um einen [*inkrementellen*](vssgloss-i.md) oder [*differenziellen*](vssgloss-d.md) Sicherungs Vorgang zu unterstützen, muss ein Anforderer Folgendes ausführen:

1.  Bestimmen Sie, welche Art von Writer-Unterstützung verfügbar ist (mithilfe von [**IVssBackupComponents:: getschreibmetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata) , um Zugriff auf Informationen in Writer-Metadatendokumenten zu erhalten) – bestimmen Sie insbesondere, welches Sicherungs Schema unterstützt wird ([**VSS- \_ Sicherungs \_ Schema**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema)).
2.  Legen Sie einen geeigneten Sicherungs Status fest.
3.  Abrufen von Spezifikationen auf Datei-und Dateiebene für eine inkrementelle oder differenzielle Sicherung.
4.  Führen Sie die Sicherung aus.

## <a name="requester-determination-of-incremental-and-differential-support-and-configuration"></a>Bestimmung der inkrementellen und differenziellen Unterstützung und Konfiguration

Eine anfordernde Person muss Informationen über die Writer-Unterstützung erhalten, bevor Sie Komponenten für die Einbindung in eine inkrementelle oder differenzielle Sicherung oder einen eigenen Zustand auswählen.

<dl> <dt>

<span id="Determining_Writer_Support"></span><span id="determining_writer_support"></span><span id="DETERMINING_WRITER_SUPPORT"></span>Ermitteln der Schreibunterstützung
</dt> <dd>

Ein Anforderer bestimmt, ob ein bestimmter Writer VSS-inkrementelle oder differenzielle Sicherungen unterstützt, indem er die Sicherungs Schema Maske des Writers mithilfe der Methode [**ivssexamineschreitermetadata:: getbackupschema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema) abruft.

Die Sicherungs Schema Maske eines Writers, der VSS-inkrementelle oder differenzielle Techniken unterstützt, enthält entweder **\_ \_ inkrementelle VSS** -oder **VSS- \_ SB- \_ differenzielle** Daten Writer können auch Einschränkungen hinsichtlich ihrer Teilnahme mit dem **\_ \_ exklusiven \_ inkrementellen \_ differenziellen Flag von VSS SB** angeben. (Weitere Informationen zu Sicherungs Schemas finden Sie unter [**VSS- \_ Sicherungs \_ Schema**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema) ).

</dd> <dt>

<span id="Setting_Requester_Backup_State"></span><span id="setting_requester_backup_state"></span><span id="SETTING_REQUESTER_BACKUP_STATE"></span>Festlegen des Sicherungs Zustands der requestperson
</dt> <dd>

Ein Anforderer gibt an, dass eine Sicherung eine inkrementelle oder differenzielle Sicherung ist, [**indem ein**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) Sicherungstyp entweder auf **VSS \_ BT \_ inkrementell** oder **VSS \_ BT- \_ differenziell** festgelegt wird, indem die [**IVssBackupComponents:: SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate) -Methode verwendet wird.

Die [**IVssBackupComponents:: SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate) -Methode wird auch verwendet, um anzugeben, ob die anfordernde Person [*Teil Dateiunterstützung*](vssgloss-p.md)bereitstellt, die häufig verwendet wird, um bestimmte inkrementelle Sicherungs-und Wiederherstellungs Vorgänge zu implementieren.

</dd> </dl>

## <a name="getting-writer-specifications-for-incremental-and-differential-backups"></a>Erhalten von Schreib Spezifikationen für inkrementelle und differenzielle

Die Informationen zur Datei Sicherungs Spezifikation auf Dateiebene ([**VSS- \_ Datei \_ Spezifikation \_ - \_ Sicherungstyp**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type)), die in den Writer-Metadatendokumenten der einzelnen Writer enthalten sind, stehen nach der erfolgreichen Rückgabe von [**IVssBackupComponents:: gatherwrite Metadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata)zur Untersuchung zur Verfügung.

Allerdings kann ein Writer [*differenzierte Dateien*](vssgloss-d.md) hinzufügen oder eine [*partielle Dateiunterstützung*](vssgloss-p.md) anfordern, bis die Verarbeitung des [*PostSnapshot*](vssgloss-p.md) -Ereignisses erfolgreich war.

Unterstützung für differenzierende Dateien und partielle Dateiunterstützung kann den Sicherungstyp für die Datei Spezifikation überschreiben, sodass Anforderer eine vollständige Analyse aller Writer-Spezifikationen über inkrementelle und differenzielle Sicherungen ausführen kann, bis die erfolgreiche Rückgabe von [**IVssBackupComponents::P Analyse forbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup)erfolgt ist.

<dl> <dt>

<span id="Getting_File_Backup_Specification_Information"></span><span id="getting_file_backup_specification_information"></span><span id="GETTING_FILE_BACKUP_SPECIFICATION_INFORMATION"></span>Informationen zur Datei Sicherungs Spezifikation werden erhalten.
</dt> <dd>

Die Informationen zur Datei Sicherungs Spezifikation auf Dateiebene ([**VSS- \_ Datei \_ Spezifikation \_ - \_ Sicherungstyp**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type)) ist in den Writer-Metadatendokumenten der einzelnen Writer enthalten und kann sofort nach der erfolgreichen Rückgabe von [**IVssBackupComponents:: gatherwrite-Metadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata)überprüft werden.

Anfordernde Personen müssen für jede Datei Gruppe der einzelnen Writer-Komponenten, die in die inkrementelle oder differenzielle Sicherung eingeschlossen werden sollen, Datei Sicherungs-Spezifikations Masken ([**VSS-Datei Spezifikation- \_ \_ \_ \_ Sicherungstyp**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type)) abrufen, unabhängig davon, ob die Komponente [*explizit*](vssgloss-e.md) oder [*implizit*](vssgloss-i.md) eingeschlossen wurde.

Ein Anforderer kann ermitteln, welches Writer-Metadatendokument mithilfe von [**IVssBackupComponents:: getwritercomponentscount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponentscount) und [**IVssBackupComponents:: getwritercomponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents)abgefragt werden muss. Die Instanz der [**ivssschreitercomponentlxt**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext) -Schnittstelle, die von **IVssBackupComponents:: getschreitercomponents** zurückgegeben wird, stellt Writer-Informationen über die [**ivssschreitercomponentslog:: getschreiterinfo**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getwriterinfo) -Methode bereit.

Der Anforderer ruft Komponenten Informationen über Instanzen der [**ivsswmcomponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) -Schnittstelle ab, die einer von einem bestimmten Writer verwalteten Komponente mithilfe von [**ivssexamineschreibmetadata:: getComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getcomponent)entspricht.

Die Informationen zu Datei Sätzen, die von der Komponente verwaltet werden, die der [**ivsswmcomponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) -Schnittstelle entspricht, werden durch Aufrufe von [**ivsswmcomponent:: GetFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getfile), [**ivsswmcomponent:: getdatabasefile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabasefile)oder [**ivsswmcomponent:: getdatabaselogfile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabaselogfile) (nach Bedarf) abgerufen.

Diese Aufrufe können Instanzen der [**ivsswmfiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) -Schnittstelle für jede Datei Gruppe einer Komponente zurückgeben.

Der Sicherungstyp für die Datei Angabe eines Datei Satzes wird durch Aufrufen von [**ivsswmfiledesc:: getbackuptypemask**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getbackuptypemask)abgerufen.

</dd> <dt>

<span id="Getting_Partial_File_and_Differenced_File_Information"></span><span id="getting_partial_file_and_differenced_file_information"></span><span id="GETTING_PARTIAL_FILE_AND_DIFFERENCED_FILE_INFORMATION"></span>Informationen zu Teil Dateien und differenzierten Dateien
</dt> <dd>

Ein Anforderer ruft über die [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) -Schnittstelle partielle Datei-und differenzielle Dateiinformationen ab.

Ein Anforderer kann alle in einer Sicherung enthaltenen Writer mithilfe von [**IVssBackupComponents:: getwritercomponentscount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponentscount) und [**IVssBackupComponents:: getwritercomponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents)durchlaufen.

Die Instanz einer [**ivssschreitercomponentlogxt**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext) -Schnittstelle, die von [**IVssBackupComponents zurückgegeben wird: getbeschreitercomponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents) ermöglicht den Zugriff auf alle Instanzen der [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) -Schnittstelle, die den [*explizit enthaltenen*](vssgloss-e.md) Komponenten eines bestimmten Writers über die Methoden [**ivssschreitercomponentsxt:: getComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getcomponent) und [**ivssschreitercomponentsxt:: getcomponentcount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getcomponentcount) entspricht.

Ein Anforderer muss alle Instanzen von [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) für alle Writer durchlaufen, deren Schema die inkrementelle oder differenzielle Sicherung unterstützt – d. h. Writer, deren Sicherungs Schema Maske von [**ivssexaminewritermetadata:: getbackupschema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema)zurückgegeben wird, enthalten **\_ \_ inkrementelle VSS** -Werte, wenn der Sicherungstyp auf **VSS \_ BT \_ inkrementell** festgelegt ist, oder **VSS- \_ SB- \_ differenziell** , wenn der Sicherungstyp **\_ \_ VSS**-

Informationen zu partiellen Dateien werden durch den Aufruf von [**IVssComponent:: GetPartialFileCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfilecount) und [**IVssComponent:: GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile) abgerufen (siehe [Arbeiten mit partiellen Dateien](working-with-partial-files.md)).

Für Writer, die Sicherungs Vorgänge auf Grundlage der Daten der letzten Änderung einer Datei unterstützen (Writer, deren Sicherungs Schema Maske ist) wie von [**ivssexaminewrite Metadata:: getbackupschema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema)zurückgegeben, enthält die **\_ \_ Letzte \_ Änderung von VSS**.), werden differenzielle Dateiinformationen durch den Aufruf von [**IVssComponent:: getdifferencedfilescount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfilescount) und [**IVssComponent:: getdifferencedfile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfile)abgerufen.

Beachten Sie, dass differenzierte Dateien möglicherweise neue Dateien sind – d. h. Dateien, die keine Elemente eines beliebigen Datei Satzes sind, der derzeit im Writer-Metadatendokument eines bestimmten Writers steht.

Anforderer sollten keine Dateien finden, die sowohl für partielle Datei Vorgänge als auch als differenzierte Dateien enthalten sind. Wenn ein Anforderer einen solchen Umstand trifft, sollte er einen Writer-Fehler zurückgeben und protokollieren.

Ein Anforderer kann weiterhin mit dem Sichern der Dateien des problematischen Writers fortfahren, aber in diesem Fall entsprechend der Spezifikation, die in den differenzierten Dateiinformationen gefunden wurde.

</dd> </dl>

## <a name="implementing-incremental-or-differential-backups"></a>Inkrementelle oder differenzielle Sicherungen

Vor der Implementierung einer Sicherung sollten Requester Informationen darüber haben, welche Writer eine [*inkrementelle*](vssgloss-i.md) oder [*differenzielle*](vssgloss-d.md) Sicherung, alle angeforderten partiellen Datei Vorgänge, alle differenzierten Dateien und den Sicherungstyp der Datei Spezifikation für alle anderen Dateien unterstützen.

<dl> <dt>

<span id="Nonsupporting_Writers"></span><span id="nonsupporting_writers"></span><span id="NONSUPPORTING_WRITERS"></span>Nicht unterstützende Writer
</dt> <dd>

Writer, deren Schema die inkrementelle oder differenzielle Sicherung nicht unterstützt (Writer, deren Sicherungs Schema Maske wie von [**ivssexaminewrite Metadata:: getbackupschema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema)zurückgegeben wird, enthält **\_ \_ inkrementelle VSS** -Werte, wenn der Sicherungstyp **VSS \_ BT \_ inkrementell** ist oder keine **VSS- \_ SB- \_ differenzielle differenzielle** Sicherung enthält, wenn der Sicherungstyp **VSS- \_ SB- \_ differenziell** ist.

Dies bedeutet nicht unbedingt, dass die Schreiber Daten nicht an einem inkrementellen oder differenziellen Sicherungs Vorgang beteiligt sind. Die Entscheidung, was zu tun ist, liegt jedoch im Ermessen der Anforderer. Der Anforderer kann eine der folgenden Aktionen ausführen:

-   Sichern Sie keine Dateien, die zu den nicht unterstützenden Writern gehören (Dies wird für den Benutzer eindeutig angezeigt).
-   Alle Dateien nicht unterstützter Writer sichern
-   Ausführen einer inkrementellen Sicherung mithilfe von Dateisystem Daten und der eigenen Verlaufs Protokolle des Anforderers.

Die letzte Alternative sollte sehr sorgfältig verwendet werden. Dies gilt nur, wenn die anfordernde Person weiß, ob die beteiligten Writer eine inkrementelle oder differenzielle Sicherung und Wiederherstellung von Daten unabhängig vom VSS-Mechanismus unterstützen können.

</dd> <dt>

<span id="Supporting_Writers"></span><span id="supporting_writers"></span><span id="SUPPORTING_WRITERS"></span>Unterstützende Writer
</dt> <dd>

Ein Anforderer muss alle [*differenzierten Dateien*](vssgloss-d.md)eines Writers verarbeiten, dann alle [*partiellen Datei*](vssgloss-p.md) Anforderungen verarbeiten und die verbleibenden Dateien gemäß dem Sicherungstyp der Datei Spezifikation (VSS-Datei Spezifikation-[**\_ \_ \_ \_ Sicherungstyp**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type)) sichern.

1.  **Sichern von differenzierten Dateien:**

    Für Writer, die Sicherungs Vorgänge auf der Grundlage der letzten Änderungs Daten unterstützen (Writer, deren Sicherungs Schema Maske wie von [**ivssexaminewrite Metadata:: getbackupschema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema)zurückgegeben, enthält die **\_ \_ Letzte \_ Änderung von VSS**-Daten), verwendet ein Anforderer die von [**IVssComponent:: getdifferencedfile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfile) zurückgegebenen Informationen für Pfad, Datei Spezifikation und Rekursions Kennzeichen, um eine Liste der Dateien als Kandidaten für die inkrementelle Sicherung oder Wiederherstellung zu generieren.

    [**IVssComponent:: getdifferencedfile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfile) kann auch eine Uhrzeit der letzten Änderung (ausgedrückt als [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) -Struktur) zurückgeben.

    Wenn der vom Writer angegebene Zeitpunkt der letzten Änderung nicht NULL ist, wird er von der anfordernden Person als Grundlage verwendet (anstelle der Dateisystem Informationen oder der eigenen gespeicherten Daten des Anforderers), um zu bestimmen, ob die Datei in die [*inkrementelle*](vssgloss-i.md) oder [*differenzielle*](vssgloss-d.md) Sicherung eingeschlossen werden soll.

    Beispiel: Wenn die Zeit der letzten Änderung einer Datei vom Writer zurückgegeben wurde:

    -   Nach der letzten vollständigen Sicherung sollte die Datei sowohl in inkrementelle als auch in differenziellen Sicherungen eingeschlossen werden.
    -   Nach der letzten vollständigen Sicherung, aber vor der letzten inkrementellen Sicherung, sollte die Datei in inkrementellen Sicherungs Vorgängen, aber nicht in differenziellen Sicherungen eingeschlossen werden.

    Wenn der Zeitpunkt der letzten Änderung des Writers NULL ist, muss der Anforderer die Dateisystem Informationen und seine eigenen gespeicherten Daten verwenden, um die Änderungszeit der differenzierten Datei zu bestimmen.

2.  **Verwenden von partiellen Datei Vorgängen:**

    Wenn ein Writer angefordert hat, dass eine Datei mithilfe eines partiellen Datei Vorgangs gesichert werden soll, verwendet der Anforderer die Dateioffset Informationen, um die angegebener Datei Segmente auf den Sicherungsmedien zu speichern. (Weitere Informationen zu partiellen Datei Vorgängen finden Sie [unter Arbeiten mit partiellen Dateien](working-with-partial-files.md) ).

    Wie bereits erwähnt, sollte ein Writer eine Datei nicht als differenzierte Datei und als Teilnehmer an einem Teil Datei Vorgang festlegen. Wenn ein Anforderer einen solchen Umstand trifft, sollte er einen Writer-Fehler zurückgeben und protokollieren.

    Ein Anforderer kann weiterhin mit dem Sichern der Dateien des problematischen Writers fortfahren, aber in diesem Fall entsprechend der Spezifikation, die in den differenzierten Dateiinformationen gefunden wurde.

3.  **Arbeiten mit dem Sicherungstyp "Datei Spezifikation":**

    Wenn alle differenzierten Dateien und partiellen Datei Vorgänge verarbeitet wurden, verarbeitet der Anforderer nun alle verbleibenden Dateien im Sicherungs Satz auf Grundlage des Sicherungs Typs der Datei Spezifikation ([**VSS-Datei Spezifikation- \_ \_ \_ \_ Sicherungstyp**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type)).

    Es gibt drei Werte für "Backup required" der [**VSS- \_ dateispezifikations- \_ \_ \_ Sicherungstyp**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) -Enumeration, die differenzielle und inkrementelle Sicherungen

    -   VSS \_ fsbt \_ alle \_ Sicherungen \_ erforderlich
    -   \_ \_ inkrementelle Sicherung von VSS fsbt \_ \_ erforderlich
    -   VSS- \_ fsbt- \_ differenzielle \_ Sicherung \_ erforderlich

    Es gibt drei Werte für "schattenkopiebedarf":

    -   VSS \_ fsbt \_ alle \_ Momentaufnahmen \_ erforderlich
    -   VSS \_ fsbt- \_ inkrementelle \_ Momentaufnahme \_ erforderlich
    -   VSS- \_ fsbt- \_ differenzielle \_ Momentaufnahme \_ erforderlich

    Dateigruppen, die mit dem Sicherungstyp "Schatten Kopie erforderlich" mit dem Sicherungstyp "Datei Angabe" gekennzeichnet sind, geben an, dass ein Anforderer Daten aus einer Schatten Kopie kopieren muss, wenn inkrementelle, differenzielle oder alle (einschließlich inkrementeller und differenzieller

    Das Flag "Backup required", das auf inkrementelle, differenzielle oder alle Sicherungs Vorgänge angewendet wird, gibt an, dass der Writer eine Kopie der aktuellen Version des Datei Satzes erwartet, die nach der Wiederherstellung eines beliebigen Sicherungs Vorgangs verfügbar ist. Dies bedeutet in der Regel, dass ein Anforderer während einer inkrementellen oder differenziellen Sicherung alle Mitglieder auf Sicherungsmedien kopiert, unabhängig davon, wann die Sicherung oder Änderung zuletzt durchgeführt wurde.

    Standardmäßig werden Dateigruppen Komponenten mit dem Sicherungstyp der Datei Spezifikation VSS \_ fsbt \_ alle \_ Sicherungen \_ erforderlich \| VSS \_ fsbt \_ alle Momentaufnahmen \_ \_ erforderlich. Wenn ein Writer andernfalls den Sicherungstyp für die Datei Spezifikation nicht explizit festlegt, müssen anfordernde Personen diese Dateien kopieren, die nicht von partiellen Datei Vorgängen behandelt werden, oder in den meisten Datei Sätzen angegebene differenzierende Dateien werden in der Regel vollständig auf die Sicherungsmedien kopiert.

</dd> <dt>

<span id="Backup_Stamps"></span><span id="backup_stamps"></span><span id="BACKUP_STAMPS"></span>Sicherungs Stempel
</dt> <dd>

Writer, die Sicherungs Stempel (VSS- \_ SB \_ -Zeitstempel) unterstützen, können Sicherungs Stempel Informationen generieren, mit denen zukünftige inkrementelle und differenzielle Sicherungs-und Wiederherstellungs Vorgänge unterstützt werden.

Das Format und die Informationen in Zeichen folgen, die Sicherungs Stempel Informationen enthalten, sind für den Writer, der Sie generiert, privat. der Anforderer weiß nicht, wie diese Informationen verarbeitet werden.

Unterstützende Writer speichern den Sicherungs Stempel im Sicherungs Komponenten Dokument als Zeichenfolge mithilfe der [**IVssComponent:: setbackupstamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp) -Methode.

Die Rolle des Anforderers bei der Behandlung von Sicherungs Stempel Informationen ist (falls vorhanden), um Sie für den Writer verfügbar zu machen, indem [**IVssBackupComponents:: setpreviousbackupstamp**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setpreviousbackupstamp) in einem zukünftigen Sicherungs-oder Wiederherstellungs Vorgang aufgerufen wird.

</dd> </dl>

 

 
