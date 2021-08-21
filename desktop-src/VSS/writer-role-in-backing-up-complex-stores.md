---
description: Erfahren Sie mehr über die Rolle "Writer" in inkrementellen und differenziellen Sicherungen, die eine enge Zusammenarbeit zwischen Anforderern und Writern erfordern.
ms.assetid: 3cf5dd1f-dc58-42bc-925f-fee7d34053c5
title: Schreibrolle beim Sichern komplexer Speicher
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbb4041ca2d05e1adf6920db617a315764f4f691768fad732c419691cf93799f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118842324"
---
# <a name="writer-role-in-backing-up-complex-stores"></a>Schreibrolle beim Sichern komplexer Speicher

Wie bei allen wichtigen Vorgängen unter VSS erfordern [*inkrementelle*](vssgloss-i.md) und [*differenzielle*](vssgloss-d.md) Sicherungen eine enge Zusammenarbeit zwischen Anforderern und Writern.

## <a name="backup-types"></a>Sicherungstypen

Die Infrastruktur bietet spezielle Unterstützung für fünf Sicherungstypen. Die Schritte lassen sich wie folgt beschreiben:

-   Full (**VSS \_ BT \_ FULL**). Dateien werden unabhängig vom Datum der letzten Sicherung gesichert. Der Sicherungsverlauf jeder Datei wird aktualisiert, und dieser Sicherungstyp kann als Grundlage für eine inkrementelle oder differenzielle Sicherung verwendet werden. Wenn Protokolldateien vorhanden sind, werden sie möglicherweise aufgrund dieser Sicherung abgeschnitten.

    Zum Wiederherstellen einer vollständigen Sicherung ist nur ein einzelnes Sicherungsimage erforderlich.

-   Differenziell (**VSS \_ BT \_ DIFFERENTIAL**). Die VSS-API wird verwendet, um sicherzustellen, dass nur Dateien, die seit der letzten vollständigen Sicherung geändert oder hinzugefügt wurden, auf ein Speichermedium kopiert werden sollen. alle Zwischensicherungsinformationen werden ignoriert. Dies kann ganze Dateien oder bestimmte Bereiche innerhalb von Dateien umfassen. Eine differenzielle Sicherung ist einer vollständigen Sicherung zugeordnet und kann im Allgemeinen erst wiederhergestellt werden, nachdem die vollständige Sicherung wiederhergestellt wurde. Wenn Protokolldateien vorhanden sind, werden sie aufgrund dieser Sicherung in der Regel nicht abgeschnitten.

    Zum Wiederherstellen einer differenziellen Sicherung sind das ursprüngliche Sicherungsimage und das letzte differenzielle Sicherungsimage erforderlich, das seit der letzten vollständigen Sicherung erstellt wurde.

-   Inkrementell (**VSS \_ BT \_ INCREMENTAL**). Die VSS-API wird verwendet, um sicherzustellen, dass nur Dateien, die seit der letzten vollständigen oder inkrementellen Sicherung geändert oder hinzugefügt wurden, auf ein Speichermedium kopiert werden. Dies kann ganze Dateien oder bestimmte Bereiche innerhalb von Dateien umfassen. Einige Writer lassen nicht zu, dass inkrementelle Sicherungen mit differenziellen Sicherungen kombiniert werden. Wenn Protokolldateien vorhanden sind, werden sie möglicherweise aufgrund dieser Sicherung abgeschnitten.

    Zum Wiederherstellen einer inkrementellen Sicherung sind das ursprüngliche Sicherungsimage und alle inkrementellen Sicherungsimages erforderlich, die seit der ersten Sicherung erstellt wurden.

-   Protokollsicherung (**VSS \_ BT \_ LOG**). Nur die Protokolldateien eines Writers (Dateien, die einer Komponente mit der [**IVssCreateWriterMetadata::AddDataBaseLogFiles-Methode**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) hinzugefügt und durch einen Aufruf von [**IVssWMComponent::GetDatabaseLogFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabaselogfile)abgerufen werden) werden gesichert. Dieser Sicherungstyp ist spezifisch für VSS. Protokollsicherungen werden häufig durchgeführt. In der Regel wird die Protokolldatei aufgrund dieser Sicherung abgeschnitten.
-   Kopiesicherung (**VSS \_ BT \_ COPY**). Wie beim VSS \_ BT \_ FULL-Sicherungstyp werden Dateien unabhängig vom letzten Sicherungsdatum gesichert. Der Sicherungsverlauf jeder Datei wird jedoch nicht aktualisiert, und dieser Sicherungstyp kann nicht als Grundlage für eine inkrementelle oder differenzielle Sicherung verwendet werden. Protokolldateien sollten nie als Ergebnis einer Kopiersicherung abgeschnitten werden.

<dl> <dt>

<span id="Partial_File_Support"></span><span id="partial_file_support"></span><span id="PARTIAL_FILE_SUPPORT"></span>Partielle Dateiunterstützung
</dt> <dd>

Einige Writer unterstützen die Dateiwiederherstellung durch das Überschreiben von Teilen der dateien, die sie verwalten. Ein Anforderer kann so entworfen werden, dass er dies nutzt. Wenn dies der Fall ist, wird dies durch Festlegen der Informationen in [**IVssBackupComponents::SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate)angegeben.

</dd> </dl>

Die Writer geben an, welche Art von Sicherungen unterstützt werden, indem [**IVssCreateWriterMetadata::SetBackupSchema**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setbackupschema) während der Verarbeitung des [*Identify-Ereignisses*](vssgloss-i.md) aufgerufen wird. Der *dsSchemaMask-Parameter* für die **IVssCreateWriterMetadata::SetBackupSchema-Methode** ist eine Bitmaske, die angibt, welche Sicherungstypen unterstützt werden. Alle Writer müssen vollständige Sicherungen unterstützen.

<dl> <dt>

<span id="VSS_BS_DIFFERENTIAL"></span><span id="vss_bs_differential"></span>**VSS \_ BS \_ DIFFERENTIAL**
</dt> <dd>

Gibt die Unterstützung für differenzielle Sicherungen an.

</dd> <dt>

<span id="VSS_BS_INCREMENTAL"></span><span id="vss_bs_incremental"></span>**VSS \_ BS \_ INCREMENTAL**
</dt> <dd>

Gibt unterstützung für inkrementelle Sicherungen an.

</dd> <dt>

<span id="VSS_BS_LOG"></span><span id="vss_bs_log"></span>**VSS \_ BS \_ LOG**
</dt> <dd>

Gibt die Unterstützung für Protokollsicherungen an.

</dd> <dt>

<span id="VSS_BS_COPY"></span><span id="vss_bs_copy"></span>**VSS \_ BS \_ COPY**
</dt> <dd>

Gibt die Unterstützung für Kopiersicherungen an.

</dd> <dt>

<span id="VSS_BS_EXCLUSIVE_INCREMENTAL_DIFFERENTIAL"></span><span id="vss_bs_exclusive_incremental_differential"></span>**VSS \_ BS \_ EXCLUSIVE \_ INCREMENTAL \_ DIFFERENTIAL**
</dt> <dd>

Gibt an, dass ein Writer das Kombinieren inkrementeller Sicherungen mit differenziellen Sicherungen nicht unterstützt.

</dd> </dl>

Der Writer kann bestimmen, welcher Sicherungstyp ausgeführt wird, indem [**er CVssWriter::GetBackupType**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getbackuptype)aufruft. Der früheste Zeitpunkt, zu dem dies ausgeführt werden kann, ist die Verarbeitung des PrepareForBackup-Ereignisses. **CVssWriter::GetBackupType** gibt einen Member der [**VSS \_ BACKUP \_ TYPE-Enumeration**](/windows/desktop/api/Vss/ne-vss-vss_backup_type) zurück. Wenn der Sicherungstyp vom Writer nicht unterstützt wird, sollte der Writer die Sicherung als vollständige Sicherung behandeln.

## <a name="backup-stamps"></a>Sicherungsstempel

Inkrementelle und differenzielle Sicherungen sind immer an eine vorherige Sicherung gebunden. Es gibt zwei Möglichkeiten, Sicherungen zu binden. Bei einfachen Datenspeichern kann der Anforderer die Korrelation zwischen Sicherungen nachverfolgen. Für komplexere Datenspeicher muss der Writer jedoch einen eigenen Zeitstempel mit der Sicherung beibehalten. dieser Zeitstempel kann die Protokollposition, Prüfpunktinformationen usw. nachverfolgen. Ein Writer gibt an, dass er seine eigenen Zeitstempel benötigt, indem er das **VSS \_ BS \_ TIMESTAMPED-Bit** beim Aufrufen von [**IVssCreateWriterMetadata::SetBackupSchema**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setbackupschema)festlegt.

Ein Writer kann einen Zeitstempel mit jeder Komponente speichern, die gesichert wird. Der Writer speichert den Zeitstempel, indem [**er IVssComponent::SetBackupStamp aufruft**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp)und eine Zeichenfolgendarstellung des Stempels für den *wszBackupStamp-Parameter* übergibt. Im Allgemeinen ruft ein Writer diese Methode während der Verarbeitung des [*PostSnapshot-Ereignisses*](vssgloss-p.md) auf. Für Sicherungen ohne Schattenkopie wird das PostSnapshot-Ereignis jedoch nicht gesendet. In diesem Fall muss **IVssComponent::SetBackupStamp** aufgerufen werden, während das [*PrepareForBackup-Ereignis*](vssgloss-p.md) verarbeitet wird.

Wenn eine inkrementelle oder differenzielle Sicherung ausgeführt wird, gibt der Anforderer dem Writer den Sicherungsstempel der vorherigen Sicherung an, die als Basis für diese Sicherung dient. Der Writer kann während der Verarbeitung des Ereignisses PrepareForBackup oder PostSnapshot auf diesen vorherigen Sicherungsstempel zugreifen, indem [**er IVssComponent::GetPreviousBackupStamp aufruft.**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpreviousbackupstamp) Der Writer kann den zurückgegebenen Stempel verwenden, um zu bestimmen, was gesichert werden muss.

## <a name="backup-strategies"></a>Sicherungsstrategien

### <a name="file-backup-files-strategies"></a>Strategien für Dateisicherungsdateien

Häufig müssen bestimmte Dateien, die in den Writermetadaten gemeldet werden, nur gesichert werden, wenn bestimmte Sicherungstypen ausgeführt werden. Einige Dateien sind möglicherweise nur erforderlich, wenn eine vollständige Sicherung ausgeführt wird. Andere Dateien sind möglicherweise nur erforderlich, wenn eine inkrementelle oder differenzielle Sicherung ausgeführt wird. VSS stellt eine Methode für die Writer bereit, um diese Informationen dem Anfordernden anzugeben. Beim Hinzufügen von Dateien zu Komponenten mit [**IVssCreateWriterMetadata::AddDatabaseFiles,**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles) [**IVssCreateWriterMetadata::AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)oder [**IVssCreateWriterMetadata::AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup)gibt der *dwBackupTypeMask-Parameter* an, für welche Sicherungstypen diese Dateien gesichert werden müssen. Die Maske kann einen oder mehrere der folgenden Werte enthalten:

<dl> <dt>

<span id="VSS_FSBT_FULL_BACKUP_REQUIRED"></span><span id="vss_fsbt_full_backup_required"></span>**VOLLSTÄNDIGE VSS \_ \_ \_ FSBT-SICHERUNG \_ ERFORDERLICH**
</dt> <dd>

Erforderlich für vollständige Sicherungen.

</dd> <dt>

<span id="VSS_FSBT_DIFFERENTIAL_BACKUP_REQUIRED"></span><span id="vss_fsbt_differential_backup_required"></span>**VSS \_ FSBT \_ DIFFERENTIAL BACKUP \_ \_ ERFORDERLICH**
</dt> <dd>

Erforderlich für differenzielle Sicherungen.

</dd> <dt>

<span id="VSS_FSBT_INCREMENTAL_BACKUP_REQUIRED"></span><span id="vss_fsbt_incremental_backup_required"></span>**INKREMENTELLE VSS \_ \_ \_ FSBT-SICHERUNG \_ ERFORDERLICH**
</dt> <dd>

Erforderlich für inkrementelle Sicherungen.

</dd> <dt>

<span id="VSS_FSBT_LOG_BACKUP_REQUIRED"></span><span id="vss_fsbt_log_backup_required"></span>**VSS \_ \_ FSBT-PROTOKOLLSICHERUNG \_ \_ ERFORDERLICH**
</dt> <dd>

Erforderlich für Protokollsicherungen.

</dd> <dt>

<span id="VSS_FSBT_ALL_BACKUP_REQUIRED"></span><span id="vss_fsbt_all_backup_required"></span>**VSS \_ FSBT \_ – ALLE \_ \_ SICHERUNGEN ERFORDERLICH**
</dt> <dd>

Für alle Sicherungstypen erforderlich. Dies ist die Standardeinstellung.

</dd> </dl>

Diese Spezifikation überschreibt die Selektivitätsspezifikation der Komponente. Betrachten Sie beispielsweise eine Komponente, deren Dateien alle mit **VSS \_ FSBT \_ LOG BACKUP \_ \_ REQUIRED,** aber nicht mit **VSS \_ FSBT FULL BACKUP \_ \_ \_ REQUIRED** gekennzeichnet sind. Angenommen, diese Komponente kann nicht für die Sicherung ausgewählt werden (*bSelectable* war false, als [**IVssCreateWriterMetadata::AddComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponent) aufgerufen wurde). Im Fall einer Protokollsicherung bedeutet dies, dass alle Dateien in dieser Komponente immer gesichert werden müssen. Bei einer vollständigen Sicherung muss jedoch keine der Dateien gesichert werden, obwohl die Selektivität der Komponente impliziert, dass sie gesichert werden sollte.

### <a name="backup-by-last-modify-time"></a>Sicherung nach zeitpunkt der letzten Änderung

Eine Möglichkeit, mit der ein Writer angeben kann, welche Dateien geändert wurden, ist die Verwendung des Differenzdateimechanismus. Ein Writer kann angeben, dass bestimmte Dateien in einer Komponente nur gesichert werden sollen, wenn sie seit einem bestimmten Zeitpunkt geändert wurden. Der Writer ruft [**IVssComponent::AddDifferencedFilesByLastModifyTime**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime) mit einer Dateispezifikation und einem Zeitpunkt der letzten Änderung auf. **IVssComponent::AddDifferencedFilesByLastModifyTime** wird in der Regel während der Verarbeitung des PostSnapshot-Ereignisses aufgerufen, obwohl es während der Verarbeitung des PrepareForBackup-Ereignisses aufgerufen werden kann. Der Anforderer muss dann alle Dateien sichern, die der Dateispezifikation entsprechen, die sich seit dem angegebenen Zeitpunkt geändert haben. Wenn der Writer den Sicherungsstempelmechanismus verwendet, wird dieser Zeitpunkt der letzten Änderung basierend auf dem vorherigen Sicherungsstempel im Sicherungsdokument bestimmt. Der Writer kann auch 0 (null) für den Zeitpunkt der letzten Änderung übergeben. Dies bedeutet, dass der Anforderer für die Bestimmung des Zeitpunkts der letzten Sicherung und der seit diesem Zeitpunkt geänderten Dateien verantwortlich ist.

### <a name="partial-file-backup"></a>Partielle Dateisicherung

Eine weitere Möglichkeit für einen Writer, Änderungen an der Anfordernden anzugeben, ist die Verwendung des Partiellen Dateimechanismus. Ein Writer kann Bytebereiche in Komponentendateien angeben, die gesichert werden müssen. Der Writer kann diese Dateibereiche während der Verarbeitung des PostSnapshot- oder PrepareForBackup-Ereignisses angeben. Der Writer ruft [**IVssComponent::AddPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile) auf, um der Sicherung partielle Dateispezifikationen hinzuzufügen. Eine partielle Dateispezifikation besteht aus einem Pfad und einem Dateinamen sowie Informationen darüber, welche Bereiche in der Datei gesichert werden müssen.

### <a name="file-specification-rules"></a>Dateispezifikationsregeln

[**IVssComponent::AddDifferencedFilesByLastModifyTime**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime) oder [**IVssComponent::AddPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile) können beide verwendet werden, um dateispezifikationen zu ändern, die während des Identify-Ereignisses angegeben wurden, oder um der Spezifikation vollständig neue Dateien hinzuzufügen. Wenn der Writer informationen ändert, die während des Identify-Ereignisses mit **IVssComponent::AddDifferencedFilesByLastModifyTime** festgelegt wurden, muss die Dateispezifikation genau mit einer der Dateispezifikationen in der aktuellen Komponente übereinstimmen. Die Dateispezifikation darf dateien in der aktuellen Komponente nicht teilweise überlappen und darf nicht mit Dateien in anderen Komponenten übereinstimmen. Dateien, die mithilfe von **IVssComponent::AddPartialFile** angegeben werden, können sich jedoch teilweise überlappen. Informationen, die von **IVssComponent::AddDifferencedFilesByLastModifyTime** oder **IVssComponent::AddPartialFile** festgelegt wurden, überschreiben die zuvor festgelegten Informationen mithilfe der [**IVssCreateWriterMetadata-Schnittstelle**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata) als Reaktion auf das Identify-Ereignis.

Allgemeine Dateispezifikationen können einen Wert für einen alternativen Speicherort aufweisen (festgelegt durch den *wszAlternateLocation-Parameter* von [**IVssCreateWriterMetadata::AddFilesToFileGroup),**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup)der einen alternativen Speicherort zum Abrufen der Datei zum Zeitpunkt der Sicherung angibt. Wenn die dateispezifikation, die über die Mechanismen differenced-file oder partial-file festgelegt wurde, mit einer vorhandenen Dateispezifikation übereinstimmt, die über einen alternativen Speicherort verfügt, ruft die Sicherungsanwendung die Daten von diesem alternativen Speicherort ab.

Wenn die dateispezifikation, die in [**IVssComponent::AddDifferencedFilesByLastModifyTime**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime) oder in [**IVssComponent::AddPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile) festgelegt ist, nicht mit den Dateien in der Komponente übereinstimmt, die gesichert werden, werden jetzt alle übereinstimmenden Dateien zur Sicherung hinzugefügt. Es muss darauf geachtet werden, dass der Writer nur Dateien hinzufügt, die auf einem Volume vorhanden sind, das bereits während dieser Arbeit schattenkopiert wird. Andernfalls kann der Anforderer diese Dateien möglicherweise nicht sichern. Wenn diese Funktionen während der Verarbeitung des PostSnapshot-Ereignisses aufgerufen werden, kann dies mithilfe der [**CVssWriter::IsPathAffected-Methode**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-ispathaffected) bestimmt werden. Wenn er während der Behandlung des PrepareForBackup-Ereignisses aufgerufen wird, muss der Writer diese Bestimmung mithilfe einer anderen Methode vornehmen.

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

Schattenkopie erforderlich für inkrementelle Sicherungen.

</dd> <dt>

<span id="VSS_FSBT_LOG_SNAPSHOT_REQUIRED"></span><span id="vss_fsbt_log_snapshot_required"></span>**VSS \_ \_ FSBT-PROTOKOLLMOMENTAUFNAHME \_ \_ ERFORDERLICH**
</dt> <dd>

Schattenkopie für Protokollsicherungen erforderlich.

</dd> <dt>

<span id="VSS_FSBT_ALL_SNAPSHOT_REQUIRED"></span><span id="vss_fsbt_all_snapshot_required"></span>**VSS \_ FSBT \_ – ALLE \_ MOMENTAUFNAHMEN \_ ERFORDERLICH**
</dt> <dd>

Schattenkopie ist für alle Sicherungstypen erforderlich. Dies ist die Standardeinstellung.

</dd> </dl>

Wenn ein bestimmtes Volume nur Komponenten enthält, für die für diese Sicherung keine Schattenkopie erforderlich ist, kann der Anforderer den Schritt zum Erstellen einer Schattenkopie für dieses Volume überspringen. Alle Daten auf diesem Volume können direkt vom ursprünglichen Volume auf das Sicherungsmedium kopiert werden.

## <a name="backup-cleanup"></a>Sicherungsbereinigung

Wenn der Writer eine Protokollkürzung oder eine andere Bereinigung nach der Sicherung durchführen muss, ist der richtige Ort hierfür die Verarbeitung des [*BackupComplete-Ereignisses.*](vssgloss-b.md) Das [*BackupShutdown-Ereignis*](vssgloss-b.md) wird einige Zeit nach BackupComplete gesendet, sodass einige Bereinigungen auch im BackupShutdown-Ereignishandler durchgeführt werden können.

Das BackupShutdown-Ereignis wird immer nach beendigung einer Sicherung gesendet. Wenn der Anforderer beim Ausführen einer Sicherung ungewöhnlich beendet wird, wird BackupShutdown sofort gesendet, ohne zuerst BackupComplete zu senden. Wenn der Writer einen Beliebigen Zustand bereinigen muss, kann dies hier erfolgen. In diesem Fall sollte die Protokollkürzung jedoch nicht erfolgen, da die Sicherung nicht notwendigerweise abgeschlossen wurde.

## <a name="restore-strategies"></a>Wiederherstellungsstrategien

Die grundlegenden Aufgaben von Writern bei der Wiederherstellung bestehen darin, zu überprüfen, ob die Wiederherstellung bei der Behandlung des PreRestore-Ereignisses erfolgen kann und ob die Wiederherstellung bei der Behandlung des PostRestore-Ereignisses erfolgt ist. Komplexere Speicher führen auch einen Wiederherstellungsprozess im PostRestore-Handler aus. Wenn die Wiederherstellung Teil einer inkrementellen oder differenziellen Wiederherstellung ist, möchte der Writer diesen Wiederherstellungsprozess in der Regel verzögern, bis alle inkrementellen oder differenziellen Wiederherstellungen abgeschlossen sind. [**IVssComponent::GetAdditionalRestores**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getadditionalrestores) gibt an, ob dies die endgültige Wiederherstellung dieser Komponente ist oder ob weitere Wiederherstellungen folgen. Wenn **IVssComponent::GetAdditionalRestores** **true** zurückgibt, sollte der Writer seine Wiederherstellungsprozedur für diese Komponente nicht ausführen.

## <a name="new-targets"></a>Neue Ziele

Wenn dies vom Writer unterstützt wird, kann der Anforderer Datendateien an einem anderen Speicherort als dem ursprünglichen Sicherungszeitspeicherort wiederherstellen. Ein Writer gibt Unterstützung für diesen Wiederherstellungsmodus an, indem das **VSS \_ BS \_ WRITER SUPPORTS \_ NEW \_ \_ TARGET-Bit** im *dsSchemaMask-Parameter* festgelegt wird, wenn [**IVssCreateWriterMetadata::SetBackupSchema**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setbackupschema)aufgerufen wird. Ein Writer ruft die neuen Speicherorte für Komponentendateien zur Wiederherstellungszeit ab, indem [**er IVssComponent::GetNewTargetCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtargetcount) und [**IVssComponent::GetNewTarget aufruft.**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtarget)

## <a name="directed-targets"></a>Directed Targets

Bei komplizierten Wiederherstellungsszenarien kann ein Writer Bereiche einer gesicherten Datei verschiedenen Bereichen derselben oder einer anderen Datei zuordnen. Dies kann mithilfe des Zielmechanismus erfolgen. Dazu muss ein Writer zuerst angeben, dass dies geschieht, indem [**er IVssComponent::SetRestoreTarget aufruft**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoretarget)und **VSS \_ RT \_ DIRECTED** für den *Zielparameter* übergibt. Anschließend ruft der Writer für jede Zuordnung [**IVssComponent::AddDirectedTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddirectedtarget)auf. Diese Methode verwendet einen vollständigen Pfad zu einer Quelldatei in der Sicherung und einen vollständigen Pfad zu einer Zieldatei, in der wiederhergestellt wird. Außerdem wird für jede dieser Dateien eine Bereichsliste verwendet. Der Writer ruft diese Funktionen während der Behandlung des PreRestore-Ereignisses auf, und der Anforderer ist dann für die Wiederherstellung der angegebenen Bereiche in der Quelldatei in den zugeordneten Bereichen in der Zieldatei verantwortlich. Das Format der Bereichszeichenfolge ist dasselbe wie in [ **IVssComponent::AddPartialFile.**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile)

## <a name="private-writer-metadata"></a>Private Writer-Metadaten

Es ist häufig nützlich, dass ein Writer private Metadaten mit einer Sicherung verwaltet, um eine inkrementelle oder differenzielle Wiederherstellung ordnungsgemäß durchzuführen. Ein Writer kann [**IVssComponent::SetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupmetadata) aufrufen, während er entweder PrepareForBackup oder PostSnapshot zum Speichern von Metadaten verarbeitet. Auf diese Metadaten kann der Writer während PreRestore oder PostRestore zugreifen, indem [**IVssComponent::GetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata)aufgerufen wird. Metadaten können auch mit partieller Dateispezifikation gespeichert werden, indem der *wszMetadata-Parameter* von [**IVssComponent::AddPartialFile verwendet wird.**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile) Auf diese Metadaten wird über den *pbstrMetadata-Parameter* von [**IVssComponent::GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile)zugegriffen. Der Writer kann auch Metadaten zwischen [**CVssWriter::OnPreRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onprerestore) und [**CVssWriter::OnPostRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostrestore)an sich selbst übergeben. In **CVssWriter::OnPreRestore** werden die Metadaten durch Aufrufen von [**IVssComponent::SetRestoreMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoremetadata)festgelegt. In **CVssWriter::OnPostRestore** werden die Metadaten durch Aufrufen von [**IVssComponent::GetRestoreMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoremetadata)abgerufen.

-   [Writer-Rolle in inkrementellen und differenziellen VSS-Sicherungen](writer-role-in-vss-incremental-and-differential-backups.md)
-   [Anfordererrolle in inkrementellen und differenziellen VSS-Sicherungen](requestor-role-in-vss-incremental-and-differential-backups.md)

 

 



