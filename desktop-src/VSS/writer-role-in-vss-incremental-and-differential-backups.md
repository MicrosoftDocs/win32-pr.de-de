---
description: 'Die Teilnahme an inkrementellen und differenziellen Sicherungen durch einen Writer findet in der Regel statt, wenn die Ereignisse "identifisswriter:: OnIdentify", "PrepareForBackup" (CVssWriter: onpreparebackup) und "PostSnapshot" (CVssWriter: OnPostSnapshot) verarbeitet werden.'
ms.assetid: 85c4e003-b531-4283-83aa-dd5cc53f35b1
title: Schreib Rolle in inkrementellen und differenziellen VSS-Sicherungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2cda57d907bed4572f0c0f71f9ee829bee18299
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526255"
---
# <a name="writer-role-in-vss-incremental-and-differential-backups"></a>Schreib Rolle in inkrementellen und differenziellen VSS-Sicherungen

Die Teilnahme an inkrementellen und differenziellen Sicherungen durch einen Writer [](vssgloss-i.md) findet in der Regel statt, wenn die Ereignisse "[**identifisswriter:: OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify)", " [*PrepareForBackup*](vssgloss-p.md) " ([**CVssWriter: onpreparebackup**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpreparebackup)) und " *PostSnapshot* " ([**CVssWriter: OnPostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot)) verarbeitet werden. Wie ein Writer teilnimmt, ist dadurch strukturiert, ob er Sicherungs-und Zeit Änderungs Zeiten unterstützt und ob der Anforderer, der die Sicherung ausgeführt hat, [*partielle Datei Vorgänge*](vssgloss-p.md)unterstützt.

## <a name="handling-identify-events-during-incremental-and-differential-backups"></a>Behandeln von Ereignis Ereignissen bei inkrementellen und differenziellen

Bei der Behandlung des Identifizierungs Ereignisses richten Writer ihre grundlegende Architektur für den inkrementellen und differenziellen Sicherungs Vorgang über das Sicherungs Schema ([**VSS- \_ Sicherungs \_ Schema**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema)) und den Sicherungstyp für die Datei Spezifikation ([**VSS- \_ dateispezifikentyp \_ \_ \_**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type))

Ein Writer gibt an, welche Vorgänge er in seinem Writer-Metadatendokument unterstützt, indem er eine Bitmaske von [**VSS- \_ Sicherungs \_ Schema**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema) Werten erstellt und an die [**ivsskreateschreitermetadata:: setbackupschema**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setbackupschema) -Methode übergibt. Dadurch kann ein Writer angeben, ob er Folgendes unterstützt:

-   Inkrementelle Sicherungen (**\_ \_ inkrementell VSS**
-   Differenzielle Sicherungen (**VSS- \_ SB- \_ differenziell**)
-   Inkrementelle und differenzielle Sicherungen können nicht gemischt werden (**\_ \_ exklusive \_ inkrementelle \_ VSS**-Sicherungen
-   Inkrementelle und differenzielle Sicherungen mit Sicherungs Stempeln (**VSS- \_ SB- \_ Zeit** Stempel)
-   Inkrementelle und differenzielle Sicherungen auf Basis von Informationen über die letzte Änderung einer Datei (Letzte Änderung von **VSS- \_ SB \_ \_**)

Writer verwenden die dateispezifikations-Sicherungstyp Maske, um den anfordernden Informationen über das Einschließen von Dateien in einer inkrementellen oder differenziellen Sicherung zur Verfügung zu stellen.

Ein Writer kann die dateispezifikations-Sicherungstyp Maske eines Datei Satzes festlegen, wenn der Datei Satz einer Komponente hinzugefügt wird, indem eine Bitmaske von [**\_ \_ \_ \_ Sicherungstyp Werten der VSS-Datei**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) Spezifikation erstellt und an [**ivsskreateschreitermetadata übergeben wird: adddatabasefiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles), [**ivsskreateschreitermetadata:: adddatabaselogfiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)oder [**ivsskreateschreitermetadata:: addfilestofilegroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup).

Es gibt drei Werte für "Backup required" der [**VSS- \_ dateispezifikations- \_ \_ \_ Sicherungstyp**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) -Enumeration, die differenzielle und inkrementelle Sicherungen

-   **VSS \_ fsbt \_ alle \_ Sicherungen \_ erforderlich**
-   **\_ \_ inkrementelle Sicherung von VSS fsbt \_ \_ erforderlich**
-   **VSS- \_ fsbt- \_ differenzielle \_ Sicherung \_ erforderlich**

Es gibt drei Werte für "schattenkopiebedarf":

-   **VSS \_ fsbt \_ alle \_ Momentaufnahmen \_ erforderlich**
-   **VSS \_ fsbt- \_ inkrementelle \_ Momentaufnahme \_ erforderlich**
-   **VSS- \_ fsbt- \_ differenzielle \_ Momentaufnahme \_ erforderlich**

Dateigruppen, die mit dem Sicherungstyp "Schatten Kopie erforderlich" gekennzeichnet sind, geben an, ob ein Anforderer Daten aus einer Schatten Kopie kopieren muss, wenn inkrementelle, differenzielle oder alle (die sowohl inkrementelle als auch differenzielle Vorgänge umfassen) Sicherungs Vorgänge ausführen.

Das Flag "Backup required", das auf inkrementelle, differenzielle oder alle Sicherungs Vorgänge angewendet wird, gibt an, dass der Writer eine Kopie der aktuellen Version des Datei Satzes erwartet, die nach der Wiederherstellung eines beliebigen Sicherungs Vorgangs verfügbar ist. Dies bedeutet in der Regel, dass, wenn ein Dateisatz mit "Sicherung erforderlich" gekennzeichnet ist, alle zugehörigen Mitglieder während einer inkrementellen oder differenziellen Sicherung auf Sicherungsmedien kopiert werden, unabhängig davon, wann die Sicherung oder Änderung zuletzt durchgeführt wurde.

Standardmäßig werden Dateigruppen Komponenten mit dem Sicherungstyp der Datei Spezifikation **VSS \_ fsbt \_ alle \_ Sicherungen \_ erforderlich** \| **VSS \_ fsbt \_ alle Momentaufnahmen \_ \_ erforderlich**. Wenn ein Writer-Entwickler daher nicht die Standardeinstellung (durch Auswahl eines anderen Sicherungstyp für die Datei Spezifikation, mithilfe partieller Datei Vorgänge oder mithilfe differenzierter Dateien) beschließt, werden die Dateien in den meisten Datei Sätzen in der Regel vollständig auf die Sicherungsmedien kopiert.

An diesem Punkt wird das Writer-Metadatendokument des Writers vollständig mit den meisten Informationen aufgefüllt, die ein Anforderer benötigt, um eine differenzielle oder inkrementelle Sicherung zu starten. Beim [**PrepareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) -Ereignis wird die Additions Angabe von Datei Satz-oder dateiebeneninformationen zur Unterstützung der Sicherung behandelt.

## <a name="handling-prepareforbackup-events-during-incremental-and-differential-backups"></a>Behandeln von PrepareForBackup-Ereignissen bei inkrementellen und differenziellen

Bevor der Anforderer mit dem eigentlichen Sicherungs Vorgang fortfährt, können Writer die Angabe einer [*inkrementellen*](vssgloss-i.md) oder [*differenziellen*](vssgloss-d.md) Sicherung ändern, indem Sie das Dokument mit den Sicherungs Komponenten der Anforderer über die [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) -Schnittstelle ändern.

Da die Writer die [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) -Schnittstelle verwenden, führen Sie normalerweise diese Vorbereitungen aus, während das [**PrepareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) -Ereignis verarbeitet wird.

In [**CVssWriter: onpreparebackup**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpreparebackup)können Writer genauer angeben, wie einige Dateien für die Sicherung ausgewertet werden sollen, geben Sie an, welche Mechanismen bei der Sicherung verwendet werden sollen, und legen Sie möglicherweise Sicherungs Stempel fest.

<dl> <dt>

<span id="Partial_Files"></span><span id="partial_files"></span><span id="PARTIAL_FILES"></span>Partielle Dateien
</dt> <dd>

Wenn eine anfordernde Person Sie unterstützt, kann ein Writer auswählen, dass eine inkrementelle oder differenzielle Sicherung mithilfe von partiellen Datei Vorgängen implementiert wird. (Writer können bestimmen, ob eine anfordernde Person partielle Datei Vorgänge unterstützt, indem Sie [**CVssWriter:: ispartialfilesupportenabled**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-ispartialfilesupportenabled)aufrufen.)

Writer verwenden [**IVssComponent:: addpartialfile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile) , um die Teile der ausgewählten Dateien anzugeben, die während der inkrementellen oder differenziellen Operation gesichert werden sollen. Anfordernde Personen müssen diese Spezifikation berücksichtigen und müssen immer die angegebenen Abschnitte der Dateien sichern. (Weitere Informationen zu partiellen Datei Vorgängen finden Sie [unter Arbeiten mit partiellen Dateien](working-with-partial-files.md) .)

Verwenden von [**IVssComponent:: addpartialfile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile), ein Writer kann der Sicherung eine Datei hinzufügen, die nicht zuvor zu einem der zugehörigen Komponenten Sätze (von [**ivsskreateschreitermetadata:: adddatabasefiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles), [**ivsskreateschreitermetadata:: adddatabaselogfiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)oder [**ivsskreateschreitermetadata:: addfilestofilegroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup)) als Teil Datei hinzugefügt wurde. Alle neuen Dateien, die der Sicherung auf diese Weise hinzugefügt werden, müssen sich auf einem Volume befinden, das für diese Sicherung bereits als Schatten kopiert wird.

Wenn eine Datei an partiellen Datei Vorgängen beteiligt ist, löst dies alle Datei Spezifikations Sicherungstyp aus, die ignoriert werden.

</dd> <dt>

<span id="Differenced_Files"></span><span id="differenced_files"></span><span id="DIFFERENCED_FILES"></span>Differenzierte Dateien
</dt> <dd>

Writer, die ein zuletzt geändertes Sicherungs Schema (**VSS- \_ \_ Schema**) unterstützen, können einer inkrementellen oder differenziellen Sicherung [*differenzierte Dateien*](vssgloss-d.md) hinzufügen.

Beim Angeben einer differenzierten Datei verwendet ein Writer [**IVssComponent:: adddifferencedfilebylastmodifytime**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime) und gibt einen Pfad, einen Dateinamen und ein rekursives Flag an – diese müssen jedoch nicht mit einem in einer Komponente enthaltenen Datei Satz identisch sein.

Tatsächlich kann ein Writer eine Datei hinzufügen, die nicht zuvor zu einem ihrer Komponenten Sätze (von [**ivsskreateschreitermetadata:: adddatabasefiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles), [**ivsskreateschreitermetadata:: adddatabaselogfiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)oder [**ivsskreateschreitermetadata:: addfilestofilegroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup)) hinzugefügt wurde. Alle neuen Dateien, die der Sicherung auf diese Weise hinzugefügt werden, müssen sich auf einem Volume befinden, das für diese Sicherung bereits als Schatten kopiert wird.

In der Regel gibt ein Writer auch eine Uhrzeit der letzten Änderung an, wenn eine differenzierte Datei – basierend auf dem eigenen Verlaufs Mechanismus des Writers hinzugefügt wird. Diese letzte Änderungszeit muss, falls angegeben, immer von anfordernden verwendet werden, um zu bestimmen, ob eine Datei in eine inkrementelle oder differenzielle Sicherung eingeschlossen werden muss.

Ein Writer darf nicht angeben, dass beim Hinzufügen einer differenzierten Datei zu einem inkrementellen oder differenziellen Sicherungs Satz eine Uhrzeit der letzten Änderung angegeben werden soll. Wenn dies der Fall ist, können Anforderer ihre eigenen Mechanismen – beispielsweise Protokolle vorheriger Sicherungen oder Dateisystem Informationen – verwenden, um zu bestimmen, ob die differenzielle Datei in eine inkrementelle oder differenzielle Sicherung eingeschlossen werden soll.

Der Sicherungstyp für die Datei Spezifikation einer beliebigen differenzierten Datei wird ignoriert.

</dd> <dt>

<span id="Backup_Stamps"></span><span id="backup_stamps"></span><span id="BACKUP_STAMPS"></span>Sicherungs Stempel
</dt> <dd>

Writer, die Sicherungs Stempel (**VSS \_ - \_ Zeitstempel**) unterstützen, verfügen über ein eigenes privates Format zum Speichern von Informationen zum Zeitpunkt der letzten Sicherung. Diese Informationen werden während der Sicherung vom Writer generiert.

Der Sicherungs Stempel wird im Dokument mit den Sicherungs Komponenten als Zeichenfolge von der [**IVssComponent:: setbackupstamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp) -Methode gespeichert. Der Sicherungs Stempel gilt für alle Datei Sätze in der Komponente (bzw. den Komponenten Satz), die der Instanz von [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent)entsprechen.

Wenn ein Anforderer Zugriff auf den Sicherungs Stempel einer vorherigen Sicherung hat, wird er durch Aufrufen von [**IVssBackupComponents:: setpreviousbackupstamp**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setpreviousbackupstamp)für den Writer verfügbar gemacht.

Ein Writer kann diesen Zeitstempel dann mithilfe von [**IVssComponent:: getpreviousbackupstamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpreviousbackupstamp)untersuchen.

Beachten Sie, dass der Anforderer lediglich die Zeichenfolge speichert und zurückgibt, die den Sicherungs Stempel enthält. Es weiß nichts über das Format der Zeichenfolge oder seine Verwendung. nur der Writer verfügt über diese Informationen.

Ein Writer kann den aktuellen Sicherungs Stempel mithilfe von [**IVssComponent:: setbackupstamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp) aktualisieren, nachdem er [**IVssComponent:: getpreviousbackupstamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpreviousbackupstamp)aufgerufen hat, sodass das Datum des aktuellen inkrementellen oder differenziellen Sicherungs Vorgangs im eigenen Format aufgezeichnet wird.

</dd> </dl>

 

 



