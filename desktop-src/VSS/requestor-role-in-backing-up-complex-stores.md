---
description: Erfahren Sie mehr über die Rolle des Anforderers in inkrementellen und differenziellen Sicherungen, die eine enge Zusammenarbeit zwischen Anforderern und Writern erfordern.
ms.assetid: 00391a49-8c81-4518-88a2-741ad5ee4ac3
title: Anfordererrolle beim Sichern komplexer Speicher
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a84dfa1b0b1837bacc2488b6bd9e3ffdd51b92c0
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262182"
---
# <a name="requester-role-in-backing-up-complex-stores"></a>Anfordererrolle beim Sichern komplexer Speicher

Wie bei allen wichtigen Vorgängen unter VSS erfordern [*inkrementelle*](vssgloss-i.md) und [*differenzielle*](vssgloss-d.md) Sicherungen eine enge Zusammenarbeit zwischen Anforderern und Writern.

## <a name="backup-type"></a>Art der Sicherung

Die Infrastruktur bietet spezielle Unterstützung für fünf Sicherungstypen. Die Schritte lassen sich wie folgt beschreiben:

-   Full (**VSS \_ BT \_ FULL**). Dateien werden unabhängig vom datum der letzten Sicherung gesichert. Der Sicherungsverlauf jeder Datei wird aktualisiert, und dieser Sicherungstyp kann als Grundlage für eine inkrementelle oder differenzielle Sicherung verwendet werden. Wenn Protokolldateien vorhanden sind, werden sie möglicherweise aufgrund dieser Sicherung abgeschnitten.

    Zum Wiederherstellen einer vollständigen Sicherung ist nur ein einzelnes Sicherungsimage erforderlich.

-   Differenziell (**VSS \_ BT \_ DIFFERENTIAL**). Die VSS-API wird verwendet, um sicherzustellen, dass nur Dateien, die seit der letzten vollständigen Sicherung geändert oder hinzugefügt wurden, auf ein Speichermedium kopiert werden sollen. alle Zwischensicherungsinformationen werden ignoriert. Dies kann ganze Dateien oder bestimmte Bereiche innerhalb von Dateien umfassen. Eine differenzielle Sicherung ist einer vollständigen Sicherung zugeordnet und kann im Allgemeinen erst wiederhergestellt werden, nachdem die vollständige Sicherung wiederhergestellt wurde. Wenn Protokolldateien vorhanden sind, werden sie aufgrund dieser Sicherung in der Regel nicht abgeschnitten.

    Zum Wiederherstellen einer differenziellen Sicherung sind das ursprüngliche Sicherungsimage und das letzte differenzielle Sicherungsimage erforderlich, das seit der letzten vollständigen Sicherung erstellt wurde.

-   Inkrementell (**VSS \_ BT \_ INCREMENTAL**). Die VSS-API wird verwendet, um sicherzustellen, dass nur Dateien, die seit der letzten vollständigen oder inkrementellen Sicherung geändert oder hinzugefügt wurden, auf ein Speichermedium kopiert werden. Dies kann ganze Dateien oder bestimmte Bereiche innerhalb von Dateien umfassen. Einige Writer lassen nicht zu, dass inkrementelle Sicherungen mit differenziellen Sicherungen kombiniert werden. Wenn Protokolldateien vorhanden sind, werden sie möglicherweise aufgrund dieser Sicherung abgeschnitten.

    Zum Wiederherstellen einer inkrementellen Sicherung sind das ursprüngliche Sicherungsimage und alle inkrementellen Sicherungsimages erforderlich, die seit der ersten Sicherung erstellt wurden.

-   Protokollsicherung (**VSS \_ BT \_ LOG**). Nur die Protokolldateien eines Writers (Dateien, die einer Komponente mit der [**IVssCreateWriterMetadata::AddDataBaseLogFiles-Methode**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) hinzugefügt und durch einen Aufruf von [**IVssWMComponent::GetDatabaseLogFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabaselogfile)abgerufen werden) werden gesichert. Dieser Sicherungstyp ist spezifisch für VSS. Protokollsicherungen werden häufig durchgeführt. In der Regel wird die Protokolldatei aufgrund dieser Sicherung abgeschnitten.
-   Kopiesicherung (**VSS \_ BT \_ COPY**). Wie beim VSS \_ BT \_ FULL-Sicherungstyp werden Dateien unabhängig vom letzten Sicherungsdatum gesichert. Der Sicherungsverlauf jeder Datei wird jedoch nicht aktualisiert, und diese Art von Sicherung kann nicht als Grundlage für eine inkrementelle oder differenzielle Sicherung verwendet werden. Protokolldateien sollten nie als Ergebnis einer Kopiersicherung abgeschnitten werden.

<dl> <dt>

<span id="Partial_File_Support"></span><span id="partial_file_support"></span><span id="PARTIAL_FILE_SUPPORT"></span>Partielle Dateiunterstützung
</dt> <dd>

Einige Writer unterstützen die Dateiwiederherstellung durch das Überschreiben von Teilen der dateien, die sie verwalten. Ein Anforderer kann so entworfen werden, dass er dies nutzt. Wenn dies der Fall ist, wird dies durch Festlegen der Informationen in [**IVssBackupComponents::SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate)angegeben.

</dd> </dl>

Der Anfordernde gibt an, welcher Sicherungstyp über den *backupType-Parameter* von [**IVssBackupComponents::SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate)ausgeführt wird. Verschiedene Writer unterstützen verschiedene Sicherungstypen. Nachdem [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) aufgerufen wurde, kann der Anforderer ermitteln, welche Sicherungstypen ein bestimmter Writer unterstützt, indem [**er IVssExwriterMetadata::GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema)aufruft. Der zurückgegebene Wert ist eine Bitmaske, die die Unterstützung für verschiedene Sicherungstypen angibt. **VSS \_ BS \_ DIFFERENTIAL** gibt Unterstützung für differenzielle Sicherungen, **VSS \_ BS \_ INCREMENTAL** für inkrementelle Sicherungen, **VSS \_ BS \_ LOG** für Protokollsicherungen und **VSS \_ BS \_ COPY** für Kopiesicherungen an. Alle Writer müssen vollständige Sicherungen unterstützen. Wenn ein Writer das Kombinieren inkrementeller Sicherungen mit differenziellen Sicherungen nicht unterstützt, wird auch das **FLAG \_ VSS BS \_ EXCLUSIVE INCREMENTAL \_ \_ DIFFERENTIAL** hinzugefügt. Wenn der Anfordernde eine inkrementelle oder differenzielle Sicherung ausführt und ein angegebener Writer diesen Sicherungstyp nicht unterstützt, sollte eine vollständige Sicherung für diesen Writer ausgeführt werden.

## <a name="backup-stamps"></a>Sicherungsstempel

Inkrementelle und differenzielle Sicherungen sind immer an eine vorherige Sicherung gebunden. Es gibt zwei Möglichkeiten, Sicherungen zu verknüpfen. Bei einfachen Datenspeichern kann der Anforderer die Korrelation zwischen Sicherungen nachverfolgen. Für komplexere Datenspeicher muss der Writer jedoch einen eigenen Zeitstempel mit der Sicherung beibehalten. dieser Zeitstempel kann die Protokollposition, Prüfpunktinformationen usw. nachverfolgen. Der Anforderer kann ermitteln, ob ein angegebener Writer seinen eigenen Zeitstempel speichern muss, indem er das **\_ VSS BS \_ TIMESTAMPED-Bit** in dem wert überprüft, der von [**IVssExwriterMetadata::GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema)zurückgegeben wird.

Writer, die einen Zeitstempel in einer Sicherung speichern, fügen den Zeitstempel entweder während der Verarbeitung von [**IVssBackupComponents::P repareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) oder während der Verarbeitung von [**IVssBackupComponents::D oSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)hinzu. Der Anfordernde kann diesen Zeitstempel abrufen, indem [**er IVssComponent::GetBackupStamp aufruft.**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupstamp) Beim Ausführen einer inkrementellen oder differenziellen Sicherung muss der Anforderer die aktuelle Sicherung mit einer vorherigen Sicherung verknüpfen. Dies erfolgt durch Abrufen des Zeitstempels aus der vorherigen Sicherung einer bestimmten Komponente und Übergeben an die [**IVssBackupComponents::SetPreviousBackupStamp-Funktion.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setpreviousbackupstamp) Dies muss für jede Komponente erfolgen, die in der vorherigen Sicherung gesichert wurde.

## <a name="backing-up-files"></a>Sichern von Dateien

### <a name="backing-up-files-reported-by-writer"></a>Sichern von Dateien, die vom Writer gemeldet werden

Jede Dateispezifikation, die ein Writer den Metadaten während der GatherWriterMetadata-Phase hinzufügt, enthält eine Sicherungstypmaske, die angibt, wann die Datei gesichert werden soll. Der Anfordernde bestimmt, was diese Maske ist, indem [**er IVssWMFiledesc::GetBackupTypeMask**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getbackuptypemask)aufruft. Die Werte in dieser Maske werden verwendet, um zu bestimmen, für welche Sicherungstypen die Dateispezifikation gesichert werden muss. Die Maske kann einen oder mehrere der folgenden Bitwerte enthalten:

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

### <a name="backup-by-last-modify-time"></a>Sicherung nach Zeitpunkt der letzten Änderung

Die in der Phase [**IVssBackupComponents::GatherWriterMetadata angegebenen**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) Dateispezifikationsinformationen geben dem Anfordernden keine Informationen darüber, was sich seit der letzten Sicherung geändert hat. Eine Möglichkeit für einen Writer, Änderungen an dem Anforderer anzugeben, ist die Verwendung des Differenzdateimechanismus. Ein Writer kann angeben, dass bestimmte Dateien in einer Komponente nur dann gesichert werden sollen, wenn sie seit einem bestimmten Zeitpunkt geändert wurden. Der Writer kann diese Dateien entweder in [**IVssBackupComponents::P repareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) oder in [**IVssBackupComponents::D oSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)angeben. Ein Anforderer kann diese Dateien ermitteln, indem er [**IVssComponent::GetDifferencedFilesCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfilescount) und [**IVssComponent::GetDifferencedFile aufruft.**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfile) Wenn die Dateispezifikation mit einem Satz in **IVssBackupComponents::GatherWriterMetadata** übereinstimmt (der derzeit basierend auf der Sicherungstypmaske gültig ist), überschreiben die differenzierten Dateiinformationen die vorherigen Informationen. Das heißt, die Dateien, die dieser Dateispezifikation entsprechen, werden jetzt nur gesichert, wenn sie seit dem angegebenen Zeitpunkt geändert wurden. Der Zeitpunkt der letzten Änderung wird mithilfe einer [**FILETIME-Struktur**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) kommuniziert. Wenn der Wert dieser Struktur 0 (null) ist, bedeutet dies, dass der Zeitpunkt der letzten Änderung basierend auf dem Datensatz des Anfordernden zum Zeitpunkt der letzten Sicherung bestimmt werden sollte.

### <a name="partial-file-backup"></a>Partielle Dateisicherung

Eine weitere Möglichkeit für einen Writer, Änderungen an dem Anfordernden anzugeben, ist die Verwendung des Partiellen Dateimechanismus. Ein Writer kann Bytebereiche in Komponentendateien angeben, die gesichert werden müssen. Der Writer kann diese Dateibereiche entweder in [**IVssBackupComponents::P repareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) oder in [**IVssBackupComponents::D oSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)angeben. Ein Anfordernder kann diese Dateien ermitteln, indem [**er IVssComponent::GetPartialFileCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfilecount) und [**IVssComponent::GetPartialFile aufruft.**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile) **IVssComponent::GetPartialFile** gibt einen Pfad und einen Dateinamen zurück, die auf die Datei zeigen, sowie eine Bereichszeichenfolge, die angibt, was in der Datei gesichert werden muss. Wie bei differenzierten Dateien überschreiben die Partiellen Dateiinformationen die vorherige Einstellung, wenn der Pfad und der Dateiname mit einer Dateispezifikation übereinstimmen, die vom Writer in [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata)festgelegt wurde. Die Ranges-Zeichenfolge kann zwei Formate aufweisen: Sie kann entweder die Bereiche direkt oder eine Datei mit Bereichsinformationen angeben. Wenn Bereiche direkt angegeben werden, ist die Syntax eine durch Trennzeichen getrennte Liste der Form offset1:length1, offset2:length2, wobei jeder Offset und jede Länge eine 64-Bit-Ganzzahl ohne Vorzeichen ist. Wenn Sie eine Ranges-Datei angeben, sollte die Ranges-Zeichenfolge auf File= *filename* festgelegt werden, wobei *filename* der vollständige Pfad zur Ranges-Datei ist. Die Ranges-Datei selbst ist eine Binärdatei, die als Liste von 64-Bit-Ganzzahlen ohne Vorzeichen formatiert ist. Die erste ganze Zahl gibt an, wie viele Bereiche in der Datei dargestellt werden. Jedes nachfolgende Paar von ganzen Zahlen stellt den Offset und die Länge eines Bereichs dar. Der Anforderer muss auch diese Bereichsdatei sichern und wiederherstellen.

### <a name="file-specification-rules"></a>Dateispezifikationsregeln

Dateispezifikationen, die durch die Mechanismen differenced-file und partial-file hinzugefügt werden, ändern entweder die in [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) festgelegten Dateispezifikationen oder fügen völlig neue Dateien hinzu. Wenn Sie Dateispezifikationen ändern, die in **IVssBackupComponents::GatherWriterMetadata** mithilfe des Partiellen Dateimechanismus festgelegt sind, kann ein Anforderer erwarten, dass die Dateispezifikation genau mit einer der Dateispezifikationen übereinstimmt, die in der Komponente in **IVssBackupComponents::GatherWriterMetadata** festgelegt sind. Die Dateispezifikation überschneidet sich nicht teilweise mit einer anderen Dateispezifikation, und sie stimmt nicht mit dateispezifikationen in anderen Komponenten dieses Writers überein. Dateispezifikationen, die mithilfe des Partiellen Dateimechanismus hinzugefügt wurden, können sich jedoch teilweise überlappen. Wenn dies zutrifft, überschreibt die Spezifikation "differenced-file" oder "partial-file" den in **IVssBackupComponents::GatherWriterMetadata festgelegten Spezifikationssatz.** Allgemeine Dateispezifikationen können einen Wert für einen alternativen Speicherort (zurückgegeben von [**IVssWMFiledesc::GetAlternateLocation)**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation)haben, der einen alternativen Speicherort angibt, von dem die Datei zum Zeitpunkt der Sicherung erhalten werden kann. Wenn die durch die Differenzdatei oder partiellen Dateimechanismen festgelegten Dateispezifikationen mit einer vorhandenen Dateispezifikation übereinstimmen, die über einen alternativen Speicherort verfügt, sollten die Daten von diesem alternativen Speicherort aus verwendet werden. Wenn die dateispezifischen Spezifikationen, die über die Mechanismen "Differenced File" oder "partial-file" festgelegt werden, nicht mit vorhandenen Spezifikationen für die Komponente übereinstimmen, sollten diese Dateibereiche nun der Sicherung hinzugefügt werden. Der Anfordernde kann davon ausgehen, dass nur Dateien auf Volumes, die bereits im Schattenkopiesatz enthalten sind, mit einem dieser Mechanismen hinzugefügt werden.

### <a name="backup-without-a-shadow-copy"></a>Sicherung ohne Schattenkopie

Bestimmte Dateitypen müssen möglicherweise nicht von einem Schattenkopie-Volume abgeschattet werden. Dies gilt beispielsweise häufig für Datenbankprotokolldateien. Da Protokolldateien monoton wachsen und ein Writer genau angeben kann, welche Teile der Datei mithilfe von Teildateien gesichert werden sollen, ist es häufig möglich, das Protokoll vom ursprünglichen Volume zu sichern. Zur Optimierung kann ein Writer mithilfe der Sicherungstypmaske markieren, welche Dateien Schattenkopien für verschiedene Sicherungstypen erfordern. Der von [**IVssWMFiledesc::GetBackupTypeMask**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getbackuptypemask) zurückgegebene Wert kann einen oder mehrere der folgenden Bitwerte enthalten:

<dl> <dt>

<span id="VSS_FSBT_FULL_SNAPSHOT_REQUIRED"></span><span id="vss_fsbt_full_snapshot_required"></span>**VOLLSTÄNDIGE VSS \_ \_ \_ FSBT-MOMENTAUFNAHME \_ ERFORDERLICH**
</dt> <dd>

Schattenkopie für vollständige Sicherungen erforderlich.

</dd> <dt>

<span id="VSS_FSBT_DIFFERENTIAL_SNAPSHOT_REQUIRED"></span><span id="vss_fsbt_differential_snapshot_required"></span>**VSS FSBT DIFFERENTIAL SNAPSHOT REQUIRED (VSS \_ \_ FSBT-DIFFERENZIELLE \_ \_ MOMENTAUFNAHME ERFORDERLICH)**
</dt> <dd>

Schattenkopie für differenzielle Sicherungen erforderlich.

</dd> <dt>

<span id="VSS_FSBT_INCREMENTAL_SNAPSHOT_REQUIRED"></span><span id="vss_fsbt_incremental_snapshot_required"></span>**VSS \_ FSBT: \_ INKREMENTELLE \_ \_ MOMENTAUFNAHME ERFORDERLICH**
</dt> <dd>

Schattenkopie für inkrementelle Sicherungen erforderlich.

</dd> <dt>

<span id="VSS_FSBT_LOG_SNAPSHOT_REQUIRED"></span><span id="vss_fsbt_log_snapshot_required"></span>**VSS \_ \_ FSBT-PROTOKOLLMOMENTAUFNAHME \_ \_ ERFORDERLICH**
</dt> <dd>

Schattenkopie für Protokollsicherungen erforderlich.

</dd> <dt>

<span id="VSS_FSBT_ALL_SNAPSHOT_REQUIRED"></span><span id="vss_fsbt_all_snapshot_required"></span>**VSS \_ FSBT \_ ALLE \_ MOMENTAUFNAHMEN \_ ERFORDERLICH**
</dt> <dd>

Schattenkopie, die für alle Sicherungstypen erforderlich ist; dies ist die Standardeinstellung.

</dd> </dl>

Wenn ein bestimmtes Volume nur Komponenten enthält, für die keine Schattenkopie für diese Sicherung erforderlich ist, kann der Anfordernde den Schritt zum Erstellen einer Schattenkopie für dieses Volume überspringen. Alle Daten auf diesem Volume können direkt vom ursprünglichen Volume auf das Sicherungsmedium kopiert werden.

## <a name="restoring-files"></a>Wiederherstellen von Dateien

### <a name="sequential-restores"></a>Sequenzielle Wiederherstellungen

Nachdem der Anfordernde einen Wiederherstellungsvorgang durchgeführt hat, sendet er das PostRestore-Ereignis an alle Writer. Im Allgemeinen behandeln Writer dieses Ereignis, indem sie Wiederherstellungsvorgänge oder andere Vorgänge nach der Wiederherstellung ausführen. Die Wiederherstellung inkrementeller Sicherungen erfolgt jedoch in der Regel als Sequenz von Wiederherstellungsvorgängen, eine pro inkrementeller Sicherung. Der Anfordernde muss den Writer darüber informieren, dass eine solche Wiederherstellung durchgeführt wird, um die Wiederherstellung oder andere unerwünschte Vorgänge zu verhindern, bis die Wiederherstellung vollständig durchgeführt wird. Rufen Sie dazu [**IVssBackupComponents::SetAdditionalRestores auf.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setadditionalrestores) Diese Methode wird pro Komponente aufgerufen und gibt dem Writer an, dass weitere Wiederherstellungen für diese Komponente kommen. Für die endgültige Wiederherstellung in der Sequenz sollte das Flag additional-restores auf FALSE (Standardwert) festgelegt werden. Dies bedeutet, dass dies die letzte Wiederherstellung in der Sequenz für diese Komponente ist.

### <a name="new-targets"></a>Neue Ziele

Wenn dies vom Writer unterstützt wird, kann die anfordernde Person Datendateien an einem anderen Speicherort als dem ursprünglichen Sicherungszeitspeicherort wiederherstellen. Der Anfordernde kann diese Unterstützung überprüfen, indem er [**IVssExwriterMetadata::GetBackupSchema aufruft.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema) Das **VSS \_ BS \_ WRITER SUPPORTS \_ \_ NEW \_ TARGET-Bit** wird festgelegt, wenn der Writer dieses Verhalten unterstützt. Der Anfordernde informiert den Writer über den neuen Speicherort, indem er [**IVssBackupComponents::AddNewTarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget) für jede verschobene Dateispezifikation aufruft. Der Anfordernde kann auch entscheiden, eine bestimmte Bereichdatei an einem anderen Speicherort wiederherzustellen. Der Anfordernde informiert den Writer über diese Änderung, indem er [**IVssBackupComponents::SetRangesFilePath aufruft.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrangesfilepath)

### <a name="directed-targets"></a>Gerichtete Ziele

Bei komplizierten Wiederherstellungsszenarien kann ein Writer Bereiche einer sicherungsbasierten Datei verschiedenen Bereichen derselben oder einer anderen Datei zuordnen. Dies kann mithilfe des gerichteten Zielmechanismus erfolgen. Der Anfordernde kann nach der [**IVssBackupComponents::P reStore-Phase feststellen,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) dass dieser Mechanismus für eine Komponente verwendet wird, indem er [**IVssComponent::GetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoretarget) aufruft und nach einer Rückgabe von **VSS \_ RT DIRECTED \_ prüft.** Der Anfordernde kann alle diese umgeleiteten Wiederherstellungen durch Aufrufen von [**IVssComponent::GetDirectedTargetCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdirectedtargetcount) und [**IVssComponent::GetDirectedTarget abrufen.**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdirectedtarget) **IVssComponent::GetDirectedTarget** gibt einen vollständigen Pfad zu einer Quelldatei in der Sicherung und einen vollständigen Pfad zu einer Zieldatei zurück, in der wiederhergestellt wird. Außerdem wird eine Liste der Bereiche für jede dieser Dateien zurückgegeben. Der Anfordernde ist dann dafür verantwortlich, die angegebenen Bereiche in der Quelldatei in den zugeordneten Bereichen in der Zieldatei wiederherzustellen. Das Format der Ranges-Zeichenfolge ist mit dem in [**IVssComponent::GetPartialFile identisch.**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile)

-   [Rolle "Writer" in inkrementellen und differenziellen VSS-Sicherungen](writer-role-in-vss-incremental-and-differential-backups.md)
-   [An anfordernde Rolle in inkrementellen und differenziellen VSS-Sicherungen](requestor-role-in-vss-incremental-and-differential-backups.md)

 

 
