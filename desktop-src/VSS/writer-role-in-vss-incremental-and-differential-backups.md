---
description: Die Teilnahme eines Schreibers an inkrementellen und differenziellen Sicherungen erfolgt in der Regel beim Behandeln von Identify-Ereignissen (CVssWriter::OnIdentify), PrepareForBackup (CVssWriter:OnPrepareBackup) und PostSnapshot-Ereignissen (CVssWriter:OnPostSnapshot).
ms.assetid: 85c4e003-b531-4283-83aa-dd5cc53f35b1
title: Rolle "Writer" in inkrementellen und differenziellen VSS-Sicherungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d3c84245c21a47ba5535eccdfcbf10e988cf72b30ea99ee92086a9ca8f65647
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119863870"
---
# <a name="writer-role-in-vss-incremental-and-differential-backups"></a>Rolle "Writer" in inkrementellen und differenziellen VSS-Sicherungen

Die Teilnahme eines Schreibers an inkrementellen und differenziellen Sicherungen erfolgt in der Regel bei der Behandlung von [*Identify-Ereignissen*](vssgloss-i.md) ([**CVssWriter::OnIdentify),**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) [*PrepareForBackup*](vssgloss-p.md) ([**CVssWriter:OnPrepareBackup**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpreparebackup)) und *PostSnapshot* -Ereignissen [**(CVssWriter:OnPostSnapshot).**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot) Die Beteiligung eines Writers wird durch die Unterstützung von Sicherungsstempeln und letzten Änderungszeiten und davon, ob der Anfordernde, der die Sicherung ausgeführt, [*Teildateivorgänge unterstützt.*](vssgloss-p.md)

## <a name="handling-identify-events-during-incremental-and-differential-backups"></a>Behandeln von Identifizieren von Ereignissen während inkrementeller und differenzieller Sicherungen

Beim Behandeln des Identify-Ereignisses richten Writer ihre grundlegende Architektur für den inkrementellen und differenziellen Sicherungsvorgang über die Masken sicherungsschema ([**VSS \_ BACKUP \_ SCHEMA**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema)) und Dateispezifikations-Sicherungstyp ([**VSS \_ FILE SPEC \_ BACKUP \_ \_ TYPE**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type)) ein.

Ein Writer gibt an, welche Vorgänge in seinem Writer-Metadatendokument unterstützt werden, indem eine Bitmaske von [**VSS \_ BACKUP \_ SCHEMA-Werten**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema) erstellt und an die [**IVssCreateWriterMetadata::SetBackupSchema-Methode**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setbackupschema) übergeben wird. Dadurch kann ein Writer angeben, ob er Folgendes unterstützt:

-   Inkrementelle Sicherungen (**\_ VSS BS \_ INCREMENTAL**)
-   Differenzielle Sicherungen (**VSS \_ BS \_ DIFFERENTIAL**)
-   Inkrementelle und differenzielle Sicherungen können nicht gemischt werden (**\_ VSS BS \_ EXCLUSIVE INCREMENTAL \_ \_ DIFFERENTIAL**)
-   Inkrementelle und differenzielle Sicherungen mithilfe von Sicherungsstempeln (**\_ VSS BS \_ TIMESTAMPED**)
-   Inkrementelle und differenzielle Sicherungen auf der Grundlage von Informationen über die letzte Änderung einer Datei (**\_ VSS BS \_ LAST \_ MODIFY**)

Writer verwenden die Maske des Dateispezifikations-Sicherungstyps, um Den Anfordernden Informationen auf Dateisatzebene zur Verfügung zu stellen, wie Dateien in eine inkrementelle oder differenzielle Sicherung enthalten werden.

Ein Writer kann die Dateispezifikations-Sicherungstypmaske eines Dateisets festlegen, wenn er den Dateisatz einer Komponente hinzufügt, indem er eine Bitmaske mit [**VSS \_ FILE SPEC BACKUP \_ \_ \_ TYPE-Werten**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) erstellt und sie [**an IVssCreateWriterMetadata::AddDatabaseFiles,**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles) [**IVssCreateWriterMetadata::AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)oder [**IVssCreateWriterMetadata::AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup)übergabet.

Es gibt drei "Sicherungs erforderlich"-Werte der [**VSS \_ FILE SPEC \_ BACKUP \_ \_ TYPE-Enumeration,**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) die sich auf differenzielle und inkrementelle Sicherungen auswirken:

-   **VSS \_ \_ FSBT: ALLE \_ \_ SICHERUNGEN ERFORDERLICH**
-   **VSS \_ FSBT: \_ INKREMENTELLE \_ SICHERUNG \_ ERFORDERLICH**
-   **VSS FSBT DIFFERENTIAL BACKUP REQUIRED (VSS \_ \_ FSBT-DIFFERENZIELLE \_ \_ SICHERUNG ERFORDERLICH)**

Es gibt drei "Schattenkopien erforderlich"-Werte:

-   **VSS \_ FSBT \_ ALLE \_ MOMENTAUFNAHMEN \_ ERFORDERLICH**
-   **VSS \_ FSBT: \_ INKREMENTELLE \_ \_ MOMENTAUFNAHME ERFORDERLICH**
-   **VSS FSBT DIFFERENTIAL SNAPSHOT REQUIRED (VSS \_ \_ FSBT-DIFFERENZIELLE \_ \_ MOMENTAUFNAHME ERFORDERLICH)**

Mit einem Dateispezifikations-Sicherungstyp "Shadow copy required" gekennzeichnete Dateisätze geben an, ob ein Ansteller Daten aus einer Schattenkopie kopieren muss, wenn er INKREMENTELLE, DIFFERENTIAL- oder ALL-Sicherungsvorgänge (die sowohl inkrementelle als auch differenzielle Vorgänge umfassen) ausführen muss.

Das Flag "Sicherung erforderlich", das auf INCREMENTAL-, DIFFERENTIAL- oder ALL-Sicherungsvorgänge angewendet wird, gibt an, dass der Writer erwartet, dass nach der Wiederherstellung eines Sicherungsvorgang eine Kopie der aktuellen Version des Dateisets verfügbar ist. Wenn ein Dateisatz mit "Sicherung erforderlich" gekennzeichnet ist, bedeutet dies in der Regel, dass alle seine Elemente während einer inkrementellen oder differenziellen Sicherung auf sicherungsmedien kopiert werden, unabhängig davon, wann die Sicherung oder Änderung zuletzt erfolgt ist.

Standardmäßig werden Dateisätze zu Komponenten mit dem Dateispezifikationssicherungstyp **VSS \_ FSBT \_ ALL BACKUP \_ \_ REQUIRED** \| **VSS \_ FSBT ALL SNAPSHOT REQUIRED \_ \_ \_ hinzugefügt.** Daher werden die Dateien in den meisten Dateisätzen in der Regel vollständig auf Sicherungsmedien kopiert, es sei denn, ein Writerentwickler entscheidet, die Standardeinstellung nicht zu verwenden (indem er einen anderen Dateispezifikations-Sicherungstyp, partielle Dateivorgänge oder differenzierte Dateien verwendet).

An diesem Punkt wird das Writer-Metadatendokument des Schreibers vollständig mit den meisten Informationen aufgefüllt, die ein Anfordernde benötigt, um eine differenzielle oder inkrementelle Sicherung zu starten. Die Addition der Spezifikation von Dateisatz- oder Dateiebeneninformationen zur Unterstützung der Sicherung wird während des [**PrepareForBackup-Ereignisses**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) behandelt.

## <a name="handling-prepareforbackup-events-during-incremental-and-differential-backups"></a>Behandeln von PrepareForBackup-Ereignissen während inkrementeller und differenzieller Sicherungen

Bevor der Anfordernde mit dem eigentlichen Sicherungsvorgang [](vssgloss-i.md) fortschreitet, können Writer die Spezifikation einer inkrementellen oder differenziellen Sicherung ändern, indem sie das Sicherungskomponentendokument des Anfordernden über die [**IVssComponent-Schnittstelle**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) ändern. [](vssgloss-d.md)

Da die Writer die [**IVssComponent-Schnittstelle**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) verwenden, führen sie diese Vorbereitungen in der Regel beim Behandeln des [**PrepareForBackup-Ereignisses**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) aus.

In [**CVssWriter:OnPrepareBackup**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpreparebackup)können Writer genauer angeben, wie einige Dateien für die Sicherung ausgewertet werden sollen, welche Mechanismen zum Sichern verwendet werden sollen, und möglicherweise Sicherungsstempel festlegen.

<dl> <dt>

<span id="Partial_Files"></span><span id="partial_files"></span><span id="PARTIAL_FILES"></span>Teildateien
</dt> <dd>

Wenn eine Anfordernde sie unterstützt, kann ein Writer eine inkrementelle oder differenzielle Sicherung mithilfe von partiellen Dateivorgängen implementiert haben. (Writer können durch Aufrufen von [**CVssWriter::IsPartialFileSupportEnabled**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-ispartialfilesupportenabled)bestimmen, ob ein An anfordernde Benutzer partielle Dateivorgänge unterstützt.)

Writer verwenden [**IVssComponent::AddPartialFile,**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile) um die Teile der ausgewählten Dateien anzugeben, die während des inkrementellen oder differenziellen Vorgangs sichern werden sollen. Anfordernde Müssen diese Spezifikation erfüllen und immer die angegebenen Abschnitte der Dateien sichern. (Weitere [Informationen zu Partiellen Dateivorgängen](working-with-partial-files.md) finden Sie unter Arbeiten mit Teildateien.)

Mithilfe von [**IVssComponent::AddPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile)kann ein Writer der Sicherung eine Datei hinzufügen, die zuvor nicht zu einem seiner Komponentensätze hinzugefügt wurde (von [**IVssCreateWriterMetadata::AddDatabaseFiles,**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles) [**IVssCreateWriterMetadata::AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)oder [**IVssCreateWriterMetadata::AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup)) als Teildatei. Alle neuen Dateien, die der Sicherung auf diese Weise hinzugefügt werden, müssen sich auf einem Volume befindet, das bereits für diese Sicherung schattenkopiert wird.

Wenn eine Datei an teiliellen Dateivorgängen beteiligt ist, ersetzt dies alle Dateispezifikationssicherungstypen, die ignoriert werden.

</dd> <dt>

<span id="Differenced_Files"></span><span id="differenced_files"></span><span id="DIFFERENCED_FILES"></span>Differenzierte Dateien
</dt> <dd>

Writer, die ein zuletzt geändertes Sicherungsschema **(VSS \_ BS \_ SCHEMA)** unterstützen, können differenzierte Dateien zu einer inkrementellen oder differenziellen Sicherung hinzufügen. [](vssgloss-d.md)

Bei der Angabe einer differenzierten Datei verwendet ein Writer [**IVssComponent::AddDifferencedFileByLastModifyTime**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime) und gibt einen Pfad, einen Dateinamen und ein rekursives Flag an. Diese müssen jedoch nicht mit einem in einer Komponente enthaltenen Dateisatz übereinstimmen.

Tatsächlich kann ein Writer der Sicherung als Differenzdatei eine Datei hinzufügen, die zuvor nicht zu einem seiner Komponentensätze hinzugefügt wurde (von [**IVssCreateWriterMetadata::AddDatabaseFiles,**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles) [**IVssCreateWriterMetadata::AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)oder [**IVssCreateWriterMetadata::AddFilesToFileGroup).**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup) Alle neuen Dateien, die der Sicherung auf diese Weise hinzugefügt werden, müssen sich auf einem Volume befindet, das bereits für diese Sicherung schattenkopiert wird.

In der Regel gibt ein Writer auch einen Zeitpunkt der letzten Änderung an, wenn eine differenzierte Datei hinzugefügt wird – basierend auf dem eigenen Verlaufsmechanismus des Writers. Dieser Zeitpunkt der letzten Änderung muss, sofern angegeben, immer von anfordernden Stellen verwendet werden, um zu bestimmen, ob eine Datei in eine inkrementelle oder differenzielle Sicherung eingeschlossen werden muss.

Ein Writer kann festlegen, dass beim Hinzufügen einer Differenzdatei zu einem inkrementellen oder differenziellen Sicherungssatz kein Zeitpunkt für die letzte Änderung angegeben wird. Wenn dies der Fall ist, können anfordernde Benutzer ihre eigenen Mechanismen verwenden , z. B. Protokolle vorheriger Sicherungen oder Dateisysteminformationen, um zu bestimmen, ob die differenzierte Datei in eine inkrementelle oder differenzielle Sicherung eingeschlossen werden soll.

Der Sicherungstyp der Dateispezifikation einer differenzierten Datei wird ignoriert.

</dd> <dt>

<span id="Backup_Stamps"></span><span id="backup_stamps"></span><span id="BACKUP_STAMPS"></span>Sicherungsstempel
</dt> <dd>

Writer, die Sicherungsstempel **\_ (VSS BS \_ TIMESTAMP)** unterstützen, verfügen über ein eigenes privates Format zum Speichern von Informationen zum Zeitpunkt der letzten Sicherung. Diese Informationen werden während der Sicherung vom Writer generiert.

Der Sicherungsstempel wird von der [**IVssComponent::SetBackupStamp-Methode als Zeichenfolge im Sicherungskomponentendokument**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp) gespeichert. Der Sicherungsstempel gilt für alle Dateisätze in der Komponente (oder dem Komponentensatz), die der Instanz von [**IVssComponent entspricht.**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent)

Wenn ein Anfordernder Zugriff auf den Sicherungsstempel einer vorherigen Sicherung hat, hat er ihn dem Writer durch Aufrufen von [**IVssBackupComponents::SetPreviousBackupStamp zur**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setpreviousbackupstamp)Verfügung gestellt.

Ein Writer kann diesen Zeitstempel dann mithilfe von [**IVssComponent::GetPreviousBackupStamp untersuchen.**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpreviousbackupstamp)

Beachten Sie, dass der Anfordernde lediglich die Zeichenfolge speichert und zurückgibt, die den Sicherungsstempel enthält. Er weiß nichts über das Format der Zeichenfolge oder deren Verwendung. nur der Writer verfügt über diese Informationen.

Ein Writer kann den aktuellen Sicherungsstempel mithilfe von [**IVssComponent::SetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp) aktualisieren, nachdem er [**IVssComponent::GetPreviousBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpreviousbackupstamp)aufgerufen hat, wodurch das Datum des aktuellen inkrementellen oder differenziellen Sicherungsvorgang in seinem eigenen Format aufgezeichnet wird.

</dd> </dl>

 

 



