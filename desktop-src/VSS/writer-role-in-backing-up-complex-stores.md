---
description: Erfahren Sie mehr über die Rolle "Writer" bei inkrementellen und differenziellen Sicherungen, die eine enge Zusammenarbeit zwischen Anfordernden und Writern erfordern.
ms.assetid: 3cf5dd1f-dc58-42bc-925f-fee7d34053c5
title: Rolle "Writer" beim Sichern komplexer Speicher
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30e34952cc4a2184d2f9abcc43283d24f64bdcc3
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262152"
---
# <a name="writer-role-in-backing-up-complex-stores"></a>Rolle "Writer" beim Sichern komplexer Speicher

Wie bei allen wichtigen Vorgängen unter VSS erfordern [*inkrementelle*](vssgloss-i.md) und [*differenzielle*](vssgloss-d.md) Sicherungen eine enge Zusammenarbeit zwischen Anfordernden und Writern.

## <a name="backup-types"></a>Sicherungstypen

Die Infrastruktur bietet spezielle Unterstützung für fünf Sicherungstypen. Die Schritte lassen sich wie folgt beschreiben:

-   Full (**VSS \_ BT \_ FULL**). Dateien werden unabhängig vom letzten Sicherungsdatum gesichert. Der Sicherungsverlauf jeder Datei wird aktualisiert, und dieser Sicherungstyp kann als Grundlage für eine inkrementelle oder differenzielle Sicherung verwendet werden. Wenn Protokolldateien enthalten sind, werden sie möglicherweise als Ergebnis dieser Sicherung abgeschnitten.

    Zum Wiederherstellen einer vollständigen Sicherung ist nur ein einzelnes Sicherungsimage erforderlich.

-   Differenziell (**VSS \_ BT \_ DIFFERENTIAL**). Die VSS-API wird verwendet, um sicherzustellen, dass nur Dateien, die seit der letzten vollständigen Sicherung geändert oder hinzugefügt wurden, auf ein Speichermedium kopiert werden sollen. alle Zwischensicherungsinformationen werden ignoriert. Dies kann ganze Dateien oder bestimmte Bereiche in Dateien umfassen. Eine differenzielle Sicherung ist einer vollständigen Sicherung zugeordnet und kann im Allgemeinen erst wiederhergestellt werden, wenn die vollständige Sicherung wiederhergestellt wurde. Wenn Protokolldateien enthalten sind, werden sie in der Regel nicht als Ergebnis dieser Sicherung abgeschnitten.

    Das Wiederherstellen einer differenziellen Sicherung erfordert das ursprüngliche Sicherungsimage und das letzte differenzielle Sicherungsimage, das seit der letzten vollständigen Sicherung erstellt wurde.

-   Inkrementell (**VSS \_ BT \_ INCREMENTAL**). Die VSS-API wird verwendet, um sicherzustellen, dass nur Dateien, die seit der letzten vollständigen oder inkrementellen Sicherung geändert oder hinzugefügt wurden, auf ein Speichermedium kopiert werden sollen. Dies kann ganze Dateien oder bestimmte Bereiche in Dateien umfassen. Einige Writer lassen nicht zu, dass inkrementelle Sicherungen mit differenziellen Sicherungen gemischt werden. Wenn Protokolldateien enthalten sind, werden sie möglicherweise als Ergebnis dieser Sicherung abgeschnitten.

    Das Wiederherstellen einer inkrementellen Sicherung erfordert das ursprüngliche Sicherungsimage und alle inkrementellen Sicherungsimages, die seit der ersten Sicherung erstellt wurden.

-   Protokollsicherung (**VSS \_ BT \_ LOG**). Nur die Protokolldateien eines Writers (Dateien, die einer Komponente mit der [**IVssCreateWriterMetadata::AddDataBaseLogFiles-Methode**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) hinzugefügt und durch einen Aufruf von [**IVssWMComponent::GetDatabaseLogFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabaselogfile)abgerufen werden) werden unterstützt. Dieser Sicherungstyp ist für VSS spezifisch. Protokollsicherungen werden in der Regel sehr häufig erstellt. In der Regel wird die Protokolldatei als Ergebnis dieser Sicherung abgeschnitten.
-   Kopiesicherung (**VSS \_ BT \_ COPY**). Wie beim VSS BT FULL-Sicherungstyp werden Dateien unabhängig vom \_ \_ letzten Sicherungsdatum gesichert. Der Sicherungsverlauf jeder Datei wird jedoch nicht aktualisiert, und dieser Sicherungstyp kann nicht als Grundlage für eine inkrementelle oder differenzielle Sicherung verwendet werden. Protokolldateien sollten nie als Ergebnis einer Kopiersicherung abgeschnitten werden.

<dl> <dt>

<span id="Partial_File_Support"></span><span id="partial_file_support"></span><span id="PARTIAL_FILE_SUPPORT"></span>Teilweise Dateiunterstützung
</dt> <dd>

Einige Writer unterstützen die Dateiwiederherstellung durch das Überschreiben von Teilen der Dateien, die sie verwalten. Ein Anfordernder kann so entworfen werden, dass er dies nutzt. Wenn dies der Fall ist, wird dies durch Festlegen der Informationen in [**IVssBackupComponents::SetBackupState angegeben.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate)

</dd> </dl>

Die Writer geben an, welche Art von Sicherungen unterstützt werden, indem [**sie IVssCreateWriterMetadata::SetBackupSchema**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setbackupschema) aufrufen, während das [*Identify-Ereignis verarbeitet*](vssgloss-i.md) wird. Der *dsSchemaMask-Parameter* für die **IVssCreateWriterMetadata::SetBackupSchema-Methode** ist eine Bitmaske, die angibt, welche Sicherungstypen unterstützt werden. Alle Writer müssen vollständige Sicherungen unterstützen.

<dl> <dt>

<span id="VSS_BS_DIFFERENTIAL"></span><span id="vss_bs_differential"></span>**VSS \_ BS \_ DIFFERENTIAL**
</dt> <dd>

Gibt die Unterstützung für differenzielle Sicherungen an.

</dd> <dt>

<span id="VSS_BS_INCREMENTAL"></span><span id="vss_bs_incremental"></span>**VSS \_ BS \_ INCREMENTAL**
</dt> <dd>

Gibt die Unterstützung für inkrementelle Sicherungen an.

</dd> <dt>

<span id="VSS_BS_LOG"></span><span id="vss_bs_log"></span>**VSS \_ \_ BS-PROTOKOLL**
</dt> <dd>

Gibt die Unterstützung für Protokollsicherungen an.

</dd> <dt>

<span id="VSS_BS_COPY"></span><span id="vss_bs_copy"></span>**VSS \_ BS \_ COPY**
</dt> <dd>

Gibt die Unterstützung für Kopiesicherungen an.

</dd> <dt>

<span id="VSS_BS_EXCLUSIVE_INCREMENTAL_DIFFERENTIAL"></span><span id="vss_bs_exclusive_incremental_differential"></span>**VSS \_ BS \_ EXCLUSIVE \_ INCREMENTAL \_ DIFFERENTIAL**
</dt> <dd>

Gibt an, dass ein Writer das Mischen inkrementeller Sicherungen mit differenziellen Sicherungen nicht unterstützt.

</dd> </dl>

Der Writer kann bestimmen, welcher Sicherungstyp ausgeführt wird, indem er [**CVssWriter::GetBackupType aufruft.**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getbackuptype) Der früheste Zeitpunkt, an dem dies ausgeführt werden kann, ist die Verarbeitung des PrepareForBackup-Ereignisses. **CVssWriter::GetBackupType** gibt einen Member der [**VSS \_ BACKUP \_ TYPE-Enumeration**](/windows/desktop/api/Vss/ne-vss-vss_backup_type) zurück. Wenn der Sicherungstyp vom Writer nicht unterstützt wird, sollte der Writer die Sicherung als vollständige Sicherung behandeln.

## <a name="backup-stamps"></a>Sicherungsstempel

Inkrementelle und differenzielle Sicherungen sind immer an eine vorherige Sicherung gebunden. Es gibt zwei Möglichkeiten, Sicherungen zu verknüpfen. Bei einfachen Datenspeichern kann der Anfordernde die Korrelation zwischen Sicherungen nachverfolgen. Für komplexere Datenspeicher muss der Writer jedoch seinen eigenen Zeitstempel mit der Sicherung verwalten. dieser Zeitstempel kann die Protokollposition, Prüfpunktinformationen und so weiter nachverfolgen. Ein Writer gibt an, dass er eigene Zeitstempel benötigt, indem er das **\_ VSS BS \_ TIMESTAMPED-Bit** beim Aufrufen von [**IVssCreateWriterMetadata::SetBackupSchema eingibt.**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setbackupschema)

Ein Writer kann einen Zeitstempel mit jeder Komponente speichern, die sichern wird. Der Writer speichert den Zeitstempel, indem er [**IVssComponent::SetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp)aufruft und eine Zeichenfolgendarstellung des Stempels für den *wszBackupStamp-Parameter* übergibt. Im Allgemeinen wird diese Methode von einem Writer während der Verarbeitung des [*PostSnapshot-Ereignisses*](vssgloss-p.md) aufruft. Für Sicherungen, die keine Schattenkopie beinhalten, wird das PostSnapshot-Ereignis jedoch nicht gesendet. In diesem Fall muss **IVssComponent::SetBackupStamp** während der Verarbeitung des [*PrepareForBackup-Ereignisses aufgerufen*](vssgloss-p.md) werden.

Wenn eine inkrementelle oder differenzielle Sicherung ausgeführt wird, gibt der Anfordernde dem Writer den Sicherungsstempel der vorherigen Sicherung an, die als Basis für diese Sicherung dient. Der Writer kann während der Verarbeitung des PrepareForBackup- oder PostSnapshot-Ereignisses auf diesen vorherigen Sicherungsstempel zugreifen, indem er [**IVssComponent::GetPreviousBackupStamp aufruft.**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpreviousbackupstamp) Der Writer kann den zurückgegebenen Stempel verwenden, um zu bestimmen, was zu sichern ist.

## <a name="backup-strategies"></a>Sicherungsstrategien

### <a name="file-backup-files-strategies"></a>Strategien für Dateisicherungsdateien

Häufig müssen bestimmte Dateien, die in den Writer-Metadaten gemeldet werden, nur gesichert werden, wenn bestimmte Sicherungstypen erstellt werden. Einige Dateien sind möglicherweise nur erforderlich, wenn eine vollständige Sicherung erstellt wird. Andere Dateien sind möglicherweise nur erforderlich, wenn eine inkrementelle oder differenzielle Sicherung durchgeführt wird. VSS stellt eine Methode für die Writer zur Verfügung, um dem Anfordernden diese Informationen anzugeben. Beim Hinzufügen von Dateien zu Komponenten mithilfe von [**IVssCreateWriterMetadata::AddDatabaseFiles,**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles) [**IVssCreateWriterMetadata::AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)oder [**IVssCreateWriterMetadata::AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup)gibt der *parameter dwBackupTypeMask* an, für welche Sicherungstypen diese Dateien gesichert werden müssen. Die Maske kann einen oder mehrere der folgenden Werte enthalten:

<dl> <dt>

<span id="VSS_FSBT_FULL_BACKUP_REQUIRED"></span><span id="vss_fsbt_full_backup_required"></span>**VOLLSTÄNDIGE VSS \_ \_ \_ FSBT-SICHERUNG \_ ERFORDERLICH**
</dt> <dd>

Erforderlich für vollständige Sicherungen.

</dd> <dt>

<span id="VSS_FSBT_DIFFERENTIAL_BACKUP_REQUIRED"></span><span id="vss_fsbt_differential_backup_required"></span>**VSS FSBT DIFFERENTIAL BACKUP REQUIRED (VSS \_ \_ FSBT-DIFFERENZIELLE \_ \_ SICHERUNG ERFORDERLICH)**
</dt> <dd>

Erforderlich für differenzielle Sicherungen.

</dd> <dt>

<span id="VSS_FSBT_INCREMENTAL_BACKUP_REQUIRED"></span><span id="vss_fsbt_incremental_backup_required"></span>**VSS \_ FSBT: \_ INKREMENTELLE \_ SICHERUNG \_ ERFORDERLICH**
</dt> <dd>

Erforderlich für inkrementelle Sicherungen.

</dd> <dt>

<span id="VSS_FSBT_LOG_BACKUP_REQUIRED"></span><span id="vss_fsbt_log_backup_required"></span>**VSS \_ \_ FSBT-PROTOKOLLSICHERUNG \_ \_ ERFORDERLICH**
</dt> <dd>

Erforderlich für Protokollsicherungen.

</dd> <dt>

<span id="VSS_FSBT_ALL_BACKUP_REQUIRED"></span><span id="vss_fsbt_all_backup_required"></span>**VSS \_ \_ FSBT: ALLE \_ \_ SICHERUNGEN ERFORDERLICH**
</dt> <dd>

Für alle Sicherungstypen erforderlich; dies ist die Standardeinstellung.

</dd> </dl>

Diese Spezifikation überschreibt die Selektivitätsspezifikation der Komponente. Stellen Sie sich beispielsweise eine Komponente vor, deren Dateien alle mit **VSS \_ FSBT \_ LOG BACKUP \_ \_ REQUIRED** gekennzeichnet sind, jedoch nicht mit **VSS \_ FSBT FULL BACKUP \_ \_ \_ REQUIRED.** Angenommen, diese Komponente kann nicht für die Sicherung ausgewählt werden (*bSelectable* war false, als [**IVssCreateWriterMetadata::AddComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponent) aufgerufen wurde). Im Fall einer Protokollsicherung bedeutet dies, dass alle Dateien in dieser Komponente immer gesichert werden müssen. Im Fall einer vollständigen Sicherung muss jedoch keine der Dateien gesichert werden, obwohl die Selektivität der Komponente impliziert, dass sie gesichert werden sollte.

### <a name="backup-by-last-modify-time"></a>Sicherung nach zeitpunkt der letzten Änderung

Eine Möglichkeit für einen Writer, anzugeben, welche Dateien sich geändert haben, ist die Verwendung des Differenzdateimechanismus. Ein Writer kann angeben, dass bestimmte Dateien in einer Komponente nur dann sichern werden sollen, wenn sie seit einer bestimmten Zeit geändert wurden. Der Writer ruft [**IVssComponent::AddDifferencedFilesByLastModifyTime**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime) mit einer Dateispezifikation und einem Zeitpunkt der letzten Änderung auf. **IVssComponent::AddDifferencedFilesByLastModifyTime** wird in der Regel während der Verarbeitung des PostSnapshot-Ereignisses aufgerufen, obwohl es während der Verarbeitung des PrepareForBackup-Ereignisses aufgerufen werden kann. Der Anfordernde muss dann alle Dateien sichern, die der Dateispezifikation entsprechen, die sich seit dem angegebenen Zeitpunkt geändert haben. Wenn der Writer den Sicherungsstempelmechanismus verwendet, wird dieser Zeitpunkt der letzten Änderung basierend auf dem vorherigen Sicherungsstempel im Sicherungsdokument bestimmt. Der Writer kann auch 0 (null) für die letzte Änderung übergeben. Dies bedeutet, dass der Anfordernde für die Bestimmung des Zeitpunkts der letzten Sicherung und der seit diesem Zeitpunkt geänderten Dateien verantwortlich ist.

### <a name="partial-file-backup"></a>Partielle Dateisicherung

Eine weitere Möglichkeit für einen Writer, Änderungen an der anfordernden Person anzugeben, ist die Verwendung des Mechanismus für partielle Dateien. Ein Writer kann Bytebereiche in Komponentendateien angeben, die gesichert werden müssen. Der Writer kann diese Dateibereiche während der Verarbeitung des PostSnapshot- oder PrepareForBackup-Ereignisses angeben. Der Writer ruft [**IVssComponent::AddPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile) auf, um der Sicherung partielle Dateispezifikationen hinzuzufügen. Eine partielle Dateispezifikation besteht aus einem Pfad und einem Dateinamen sowie Informationen darüber, welche Bereiche in der Datei gesichert werden müssen.

### <a name="file-specification-rules"></a>Dateispezifikationsregeln

[**IVssComponent::AddDifferencedFilesByLastModifyTime**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime) oder [**IVssComponent::AddPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile) können beide verwendet werden, um dateispezifikationen zu ändern, die während des Identify-Ereignisses angegeben wurden, oder um der Spezifikation vollständig neue Dateien hinzuzufügen. Wenn der Writer informationen ändert, die während des Identify-Ereignisses mithilfe von **IVssComponent::AddDifferencedFilesByLastModifyTime** festgelegt wurden, muss die Dateispezifikation genau mit einer der Dateispezifikationen in der aktuellen Komponente übereinstimmen. Die Dateispezifikation darf dateien in der aktuellen Komponente nicht teilweise überlappen und darf nicht mit Dateien in anderen Komponenten übereinstimmen. Dateien, die mit **IVssComponent::AddPartialFile** angegeben werden, können sich jedoch teilweise überlappen, wenn eine andere Dateispezifikation angegeben wird. Informationen, die von **IVssComponent::AddDifferencedFilesByLastModifyTime** oder **IVssComponent::AddPartialFile** festgelegt wurden, überschreiben die zuvor festgelegten Informationen mithilfe der [**IVssCreateWriterMetadata-Schnittstelle**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata) als Reaktion auf das Identify-Ereignis.

Allgemeine Dateispezifikationen können einen Wert für einen alternativen Speicherort aufweisen (festgelegt durch den *wszAlternateLocation-Parameter* von [**IVssCreateWriterMetadata::AddFilesToFileGroup),**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup)der einen alternativen Speicherort zum Abrufen der Datei zum Zeitpunkt der Sicherung angibt. Wenn die Dateispezifikation, die über die Mechanismen differenced-file oder partial-file festgelegt wurde, mit einer vorhandenen Dateispezifikation übereinstimmt, die über einen alternativen Speicherort verfügt, ruft die Sicherungsanwendung die Daten von diesem alternativen Speicherort ab.

Wenn die in [**IVssComponent::AddDifferencedFilesByLastModifyTime**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime) oder in [**IVssComponent::AddPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile) festgelegte Datei nicht übereinstimmt und dateien in der Komponente, die gesichert werden, werden jetzt alle übereinstimmenden Dateien zur Sicherung hinzugefügt. Achten Sie darauf, dass der Writer nur Dateien hinzufügt, die auf einem Volume vorhanden sind, das bereits während dieser Arbeit schattenkopiert wird. Andernfalls kann der Anforderer diese Dateien möglicherweise nicht sichern. Wenn diese Funktionen während der Verarbeitung des PostSnapshot-Ereignisses aufgerufen werden, kann dies mithilfe der [**CVssWriter::IsPathAffected-Methode**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-ispathaffected) bestimmt werden. Wenn er während der Behandlung des PrepareForBackup-Ereignisses aufgerufen wird, muss der Writer diese Bestimmung mithilfe einer anderen Methode vornehmen.

### <a name="backup-without-a-shadow-copy"></a>Sicherung ohne Schattenkopie

Bestimmte Dateitypen müssen möglicherweise nicht von einem Schattenkopievolume gesichert werden. Dies gilt beispielsweise häufig für Datenbankprotokolldateien. Da Protokolldateien monoton zunehmen und ein Writer genau angeben kann, welche Teile der Datei mithilfe von Teildateien gesichert werden sollen, ist es häufig möglich, das Protokoll vom ursprünglichen Volume zu sichern. Als Optimierung kann ein Writer markieren, welche Dateien Schattenkopien für verschiedene Sicherungstypen erfordern, indem er die im *dwBackupTypeMask-Parameter* von [**IVssCreateWriterMetadata::AddDatabaseFiles,**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles) [**IVssCreateWriterMetadata::AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)oder [**IVssCreateWriterMetadata::AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup)festgelegten Flags verwendet. Folgende Flags werden unterstützt:

<dl> <dt>

<span id="VSS_FSBT_FULL_SNAPSHOT_REQUIRED"></span><span id="vss_fsbt_full_snapshot_required"></span>**VOLLSTÄNDIGE VSS \_ \_ \_ FSBT-MOMENTAUFNAHME \_ ERFORDERLICH**
</dt> <dd>

Schattenkopie für vollständige Sicherungen erforderlich.

</dd> <dt>

<span id="VSS_FSBT_DIFFERENTIAL_SNAPSHOT_REQUIRED"></span><span id="vss_fsbt_differential_snapshot_required"></span>**VSS \_ FSBT \_ DIFFERENTIAL SNAPSHOT \_ \_ ERFORDERLICH**
</dt> <dd>

Schattenkopie für differenzielle Sicherungen erforderlich.

</dd> <dt>

<span id="VSS_FSBT_INCREMENTAL_SNAPSHOT_REQUIRED"></span><span id="vss_fsbt_incremental_snapshot_required"></span>**INKREMENTELLE VSS \_ \_ \_ FSBT-MOMENTAUFNAHME \_ ERFORDERLICH**
</dt> <dd>

Schattenkopie für inkrementelle Sicherungen erforderlich.

</dd> <dt>

<span id="VSS_FSBT_LOG_SNAPSHOT_REQUIRED"></span><span id="vss_fsbt_log_snapshot_required"></span>**VSS \_ \_ FSBT-PROTOKOLLMOMENTAUFNAHME \_ \_ ERFORDERLICH**
</dt> <dd>

Schattenkopie für Protokollsicherungen erforderlich.

</dd> <dt>

<span id="VSS_FSBT_ALL_SNAPSHOT_REQUIRED"></span><span id="vss_fsbt_all_snapshot_required"></span>**VSS \_ FSBT \_ – ALLE \_ MOMENTAUFNAHMEN \_ ERFORDERLICH**
</dt> <dd>

Schattenkopie ist für alle Sicherungstypen erforderlich. Dies ist die Standardeinstellung.

</dd> </dl>

Wenn ein bestimmtes Volume nur Komponenten enthält, für die keine Schattenkopie für diese Sicherung erforderlich ist, kann der Anforderer den Schritt zum Erstellen einer Schattenkopie für dieses Volume überspringen. Alle Daten auf diesem Volume können direkt vom ursprünglichen Volume auf das Sicherungsmedium kopiert werden.

## <a name="backup-cleanup"></a>Sicherungsbereinigung

Wenn der Writer eine Protokollkürzung oder eine andere Bereinigung nach der Sicherung durchführen muss, ist der richtige Ort hierfür die Verarbeitung des [*BackupComplete-Ereignisses.*](vssgloss-b.md) Das [*BackupShutdown-Ereignis*](vssgloss-b.md) wird einige Zeit nach BackupComplete gesendet, sodass einige Bereinigungen auch im BackupShutdown-Ereignishandler durchgeführt werden können.

Das BackupShutdown-Ereignis wird immer nach beendigung einer Sicherung gesendet. Wenn der Anforderer beim Ausführen einer Sicherung ungewöhnlich beendet wird, wird BackupShutdown sofort gesendet, ohne zuerst BackupComplete zu senden. Wenn der Writer einen Beliebigen Zustand bereinigen muss, kann dies hier erfolgen. In diesem Fall sollte die Protokollkürzung jedoch nicht erfolgen, da die Sicherung nicht notwendigerweise abgeschlossen wurde.

## <a name="restore-strategies"></a>Wiederherstellungsstrategien

Die grundlegenden Aufgaben von Writern bei der Wiederherstellung bestehen darin, zu überprüfen, ob die Wiederherstellung bei der Behandlung des PreRestore-Ereignisses erfolgen kann und ob die Wiederherstellung bei der Behandlung des PostRestore-Ereignisses erfolgt ist. Komplexere Speicher führen auch einen Wiederherstellungsprozess im PostRestore-Handler aus. Wenn die Wiederherstellung Teil einer inkrementellen oder differenziellen Wiederherstellung ist, möchte der Writer diesen Wiederherstellungsprozess in der Regel verzögern, bis alle inkrementellen oder differenziellen Wiederherstellungen abgeschlossen sind. [**IVssComponent::GetAdditionalRestores**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getadditionalrestores) gibt an, ob dies die endgültige Wiederherstellung dieser Komponente ist oder ob weitere Wiederherstellungen folgen. Wenn **IVssComponent::GetAdditionalRestores** **true** zurückgibt, sollte der Writer seine Wiederherstellungsprozedur für diese Komponente nicht ausführen.

## <a name="new-targets"></a>Neue Ziele

Wenn dies vom Writer unterstützt wird, kann der Anforderer Datendateien an einem anderen Speicherort als dem ursprünglichen Sicherungszeitspeicherort wiederherstellen. Ein Writer gibt Unterstützung für diesen Wiederherstellungsmodus an, indem das **VSS \_ BS \_ WRITER SUPPORTS \_ NEW \_ \_ TARGET-Bit** im *dsSchemaMask-Parameter* festgelegt wird, wenn [**IVssCreateWriterMetadata::SetBackupSchema**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setbackupschema)aufgerufen wird. Ein Writer ruft die neuen Speicherorte für Komponentendateien zur Wiederherstellungszeit ab, indem [**er IVssComponent::GetNewTargetCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtargetcount) und [**IVssComponent::GetNewTarget aufruft.**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtarget)

## <a name="directed-targets"></a>Directed Targets

Bei komplizierten Wiederherstellungsszenarien kann ein Writer Bereiche einer gesicherten Datei verschiedenen Bereichen derselben oder einer anderen Datei zuordnen. Dies kann mithilfe des Zielmechanismus erfolgen. Dazu muss ein Writer zuerst angeben, dass dies geschieht, indem [**er IVssComponent::SetRestoreTarget aufruft**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoretarget)und **VSS \_ RT \_ DIRECTED** für den *Zielparameter* übergibt. Anschließend ruft der Writer für jede Zuordnung [**IVssComponent::AddDirectedTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddirectedtarget)auf. Diese Methode verwendet einen vollständigen Pfad zu einer Quelldatei in der Sicherung und einen vollständigen Pfad zu einer Zieldatei, in der wiederhergestellt wird. Außerdem wird eine Bereichsliste für jede dieser Dateien verwendet. Der Writer ruft diese Funktionen während der Behandlung des PreRestore-Ereignisses auf, und der Anforderer ist dann für die Wiederherstellung der angegebenen Bereiche in der Quelldatei in den zugeordneten Bereichen in der Zieldatei verantwortlich. Das Format der Bereichszeichenfolge ist dasselbe wie in [ **IVssComponent::AddPartialFile.**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile)

## <a name="private-writer-metadata"></a>Private Writer-Metadaten

Es ist häufig nützlich, dass ein Writer private Metadaten mit einer Sicherung verwaltet, um eine inkrementelle oder differenzielle Wiederherstellung ordnungsgemäß durchzuführen. Ein Writer kann [**IVssComponent::SetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupmetadata) aufrufen, während er entweder PrepareForBackup oder PostSnapshot zum Speichern von Metadaten verarbeitet. Auf diese Metadaten kann der Writer während PreRestore oder PostRestore zugreifen, indem [**IVssComponent::GetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata)aufgerufen wird. Metadaten können auch mit partieller Dateispezifikation gespeichert werden, indem der *wszMetadata-Parameter* von [**IVssComponent::AddPartialFile verwendet wird.**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile) Auf diese Metadaten wird über den *pbstrMetadata-Parameter* von [**IVssComponent::GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile)zugegriffen. Der Writer kann auch Metadaten zwischen [**CVssWriter::OnPreRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onprerestore) und [**CVssWriter::OnPostRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostrestore)an sich selbst übergeben. In **CVssWriter::OnPreRestore** werden die Metadaten durch Aufrufen von [**IVssComponent::SetRestoreMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoremetadata)festgelegt. In **CVssWriter::OnPostRestore** werden die Metadaten durch Aufrufen von [**IVssComponent::GetRestoreMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoremetadata)abgerufen.

-   [Writer-Rolle in inkrementellen und differenziellen VSS-Sicherungen](writer-role-in-vss-incremental-and-differential-backups.md)
-   [Anfordererrolle in inkrementellen und differenziellen VSS-Sicherungen](requestor-role-in-vss-incremental-and-differential-backups.md)

 

 



