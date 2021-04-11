---
description: Wie bei allen wichtigen Vorgängen unter VSS erfordern inkrementelle und differenzielle Sicherungen eine enge Zusammenarbeit zwischen Anforderern und Writern.
ms.assetid: 00391a49-8c81-4518-88a2-741ad5ee4ac3
title: Requestrolle beim Sichern komplexer Filialen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 197351e76b6861ee9b9d1e0589ef028c911430ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042090"
---
# <a name="requester-role-in-backing-up-complex-stores"></a>Requestrolle beim Sichern komplexer Filialen

Wie bei allen wichtigen Vorgängen unter VSS erfordern [*inkrementelle*](vssgloss-i.md) und [*differenzielle*](vssgloss-d.md) Sicherungen eine enge Zusammenarbeit zwischen Anforderern und Writern.

## <a name="backup-type"></a>Sicherungstyp

Die-Infrastruktur bietet spezielle Unterstützung für fünf Arten von Sicherungen. Die Schritte lassen sich wie folgt beschreiben:

-   Vollständig (**VSS \_ BT \_ vollständig**). Dateien werden unabhängig vom Zeitpunkt der letzten Sicherung gesichert. Der Sicherungs Verlauf der einzelnen Dateien wird aktualisiert, und dieser Sicherungstyp kann als Grundlage für eine inkrementelle oder differenzielle Sicherung verwendet werden. Wenn Protokolldateien vorhanden sind, werden Sie möglicherweise als Ergebnis dieser Sicherung abgeschnitten.

    Zum Wiederherstellen einer vollständigen Sicherung ist nur ein einzelnes Sicherungs Abbild erforderlich.

-   Differenziell (**VSS \_ BT- \_ differenziell**). Die VSS-API wird verwendet, um sicherzustellen, dass nur Dateien, die seit der letzten vollständigen Sicherung geändert oder hinzugefügt wurden, auf ein Speichermedium kopiert werden. alle Informationen zur zwischen Sicherung werden ignoriert. Dies kann ganze Dateien oder bestimmte Bereiche innerhalb von Dateien einschließen. Eine differenzielle Sicherung ist einer vollständigen Sicherung zugeordnet und kann im allgemeinen erst wieder hergestellt werden, wenn die vollständige Sicherung wieder hergestellt wurde. Wenn Protokolldateien vorhanden sind, werden Sie in der Regel nicht als Ergebnis dieser Sicherung abgeschnitten.

    Zum Wiederherstellen einer differenziellen Sicherung sind das ursprüngliche Sicherungs Image und das letzte differenzielle Sicherungs Abbild erforderlich, das seit der letzten vollständigen Sicherung erstellt wurde.

-   Inkrementell (**VSS \_ BT \_ inkrementell** Die VSS-API wird verwendet, um sicherzustellen, dass nur Dateien, die seit der letzten vollständigen oder inkrementellen Sicherung geändert oder hinzugefügt wurden, auf ein Speichermedium kopiert werden. Dies kann ganze Dateien oder bestimmte Bereiche innerhalb von Dateien einschließen. Einige Writer lassen nicht zu, dass inkrementelle Sicherungen mit differenziellen Sicherungen gemischt werden. Wenn Protokolldateien vorhanden sind, werden Sie möglicherweise als Ergebnis dieser Sicherung abgeschnitten.

    Zum Wiederherstellen einer inkrementellen Sicherung sind das ursprüngliche Sicherungs Abbild und alle inkrementellen Sicherungs Abbilder seit der ersten Sicherung

-   Protokoll Sicherung (**VSS \_ BT- \_ Protokoll**). Es werden nur die Protokolldateien eines Writers (Dateien, die einer Komponente mit der [**ivssdeateschreitermetadata:: adddatabaselogfiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) -Methode hinzugefügt und durch einen Aufrufen von [**ivsswmcomponent:: getdatabaselogfile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabaselogfile)abgerufen werden) gesichert. Dieser Sicherungstyp ist spezifisch für VSS. Protokoll Sicherungen werden in der Regel sehr häufig durchgeführt. In der Regel wird die Protokolldatei als Ergebnis dieser Sicherung abgeschnitten.
-   Kopier Sicherung (**VSS \_ BT- \_ Kopie**). Ebenso wie der \_ Vollständige VSS BT- \_ Sicherungstyp werden Dateien unabhängig vom Zeitpunkt der letzten Sicherung gesichert. Der Sicherungs Verlauf der einzelnen Dateien wird jedoch nicht aktualisiert, und diese Art der Sicherung kann nicht als Grundlage für eine inkrementelle oder differenzielle Sicherung verwendet werden. Protokolldateien sollten aufgrund einer Kopiesicherung nie abgeschnitten werden.

<dl> <dt>

<span id="Partial_File_Support"></span><span id="partial_file_support"></span><span id="PARTIAL_FILE_SUPPORT"></span>Unterstützung für Teil Dateien
</dt> <dd>

Einige Writer unterstützen die Wiederherstellung von Dateien durch das Überschreiben von Teilen der Dateien, die Sie verwalten. Ein Anforderer kann diese Funktion nutzen, und wenn dies der Fall ist, wird er durch Festlegen der Informationen in [**IVssBackupComponents:: SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate)festgelegt.

</dd> </dl>

Der Anforderer gibt an, welcher Sicherungstyp durch den *backuptype* -Parameter von [**IVssBackupComponents:: SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate)ausgeführt wird. Verschiedene Writer unterstützen verschiedene Arten der Sicherung. Nachdem [**IVssBackupComponents:: gatherwrite Metadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) aufgerufen wurde, kann die anfordernde Person ermitteln, welche Sicherungs Typen ein bestimmter Writer unterstützt, indem [**ivssexamineschreitermetadata:: getbackupschema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema)aufgerufen wird. Der zurückgegebene Wert ist eine Bitmaske, die die Unterstützung für unterschiedliche Sicherungs Typen angibt. **VSS \_ Die SB- \_ differenzielle** Sicherung zeigt die Unterstützung für differenzielle Sicherungen, die **\_ \_ inkrementelle VSS** -Dateien für inkrementelle Sicherungen, das **VSS- \_ \_ Protokoll** für Protokoll Sicherungen und die **VSS- \_ SB- \_ Kopie** für Kopier Sicherungen Wenn ein Writer das Mischen von inkrementellen Sicherungen mit differenziellen Sicherungen nicht unterstützt, wird auch das **VSS SB-Flag \_ \_ exklusive \_ inkrementelles \_ differenziell** hinzugefügt Wenn der Anforderer eine inkrementelle oder differenzielle Sicherung ausführt und ein bestimmter Writer diesen Sicherungstyp nicht unterstützt, sollte für diesen Writer eine vollständige Sicherung durchgeführt werden.

## <a name="backup-stamps"></a>Sicherungs Stempel

Inkrementelle und differenzielle Sicherungen sind immer an eine vorherige Sicherung gebunden. Es gibt zwei Möglichkeiten, Sicherungen zu verknüpfen. Bei einfachen Daten speichern kann der Anforderer die Korrelation zwischen Sicherungen nachverfolgen. Bei komplexeren Daten speichern muss der Writer aber seinen eigenen Zeitstempel mit der Sicherung beibehalten. Dieser Zeitstempel kann die Protokoll Position, die Prüf Punkt Informationen usw. nachverfolgen. Der Anforderer kann ermitteln, ob ein bestimmter Writer seinen eigenen Zeitstempel speichern muss, indem er in dem Wert, der von [**ivssexamineschreibmetadata:: getbackupschema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema)zurückgegeben wird, nach dem **VSS- \_ SB- \_ Zeit** Stempel-Bit sucht.

Writer, die einen Zeitstempel in einer Sicherung speichern, fügen den Zeitstempel entweder während der Verarbeitung von [**IVssBackupComponents::P Analyse forbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) oder während der Verarbeitung von [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)hinzu. Der Anforderer kann diesen Zeitstempel durch Aufrufen von [**IVssComponent:: getbackupstamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupstamp)abrufen. Beim Ausführen einer inkrementellen oder differenziellen Sicherung muss der Anforderer die aktuelle Sicherung mit einer vorherigen Sicherung verknüpfen. Hierzu erhalten Sie den Zeitstempel aus der vorherigen Sicherung einer bestimmten Komponente und übergeben ihn an die [**IVssBackupComponents:: setpreviousbackupstamp**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setpreviousbackupstamp) -Funktion. Dies muss für jede Komponente erfolgen, die in der vorherigen Sicherung gesichert wurde.

## <a name="backing-up-files"></a>Sichern von Dateien

### <a name="backing-up-files-reported-by-writer"></a>Sichern der vom Writer gemeldeten Dateien

Jede Datei Spezifikation, die ein Writer seinen Metadaten während der gatherwrite Metadata-Phase hinzufügt, enthält eine Sicherungstyp Maske, die angibt, wann die Datei gesichert werden soll. Der Anforderer bestimmt, was diese Maske ist, indem [**ivsswmfiledesc:: getbackuptypemask**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getbackuptypemask)aufgerufen wird. Die Werte in dieser Maske werden verwendet, um zu ermitteln, für welche Sicherungs Typen die Datei Spezifikation gesichert werden muss. Die Maske kann einen oder mehrere der folgenden Bitwerte enthalten:

<dl> <dt>

<span id="VSS_FSBT_FULL_BACKUP_REQUIRED"></span><span id="vss_fsbt_full_backup_required"></span>**Vollständige VSS- \_ fsbt- \_ \_ Sicherung \_ erforderlich**
</dt> <dd>

Erforderlich für vollständige Sicherungen.

</dd> <dt>

<span id="VSS_FSBT_DIFFERENTIAL_BACKUP_REQUIRED"></span><span id="vss_fsbt_differential_backup_required"></span>**VSS- \_ fsbt- \_ differenzielle \_ Sicherung \_ erforderlich**
</dt> <dd>

Erforderlich für differenzielle Sicherungen.

</dd> <dt>

<span id="VSS_FSBT_INCREMENTAL_BACKUP_REQUIRED"></span><span id="vss_fsbt_incremental_backup_required"></span>**\_ \_ inkrementelle Sicherung von VSS fsbt \_ \_ erforderlich**
</dt> <dd>

Erforderlich für inkrementelle Sicherungen.

</dd> <dt>

<span id="VSS_FSBT_LOG_BACKUP_REQUIRED"></span><span id="vss_fsbt_log_backup_required"></span>**VSS- \_ fsbt- \_ Protokoll \_ Sicherung \_ erforderlich**
</dt> <dd>

Für Protokoll Sicherungen erforderlich.

</dd> <dt>

<span id="VSS_FSBT_ALL_BACKUP_REQUIRED"></span><span id="vss_fsbt_all_backup_required"></span>**VSS \_ fsbt \_ alle \_ Sicherungen \_ erforderlich**
</dt> <dd>

Erforderlich für alle Sicherungs Typen; Dies ist die Standardeinstellung.

</dd> </dl>

Diese Spezifikation überschreibt die Selektivität der Komponente. Nehmen Sie beispielsweise an, eine Komponente, deren Dateien alle mit der **VSS- \_ fsbt- \_ Protokoll \_ Sicherung \_** gekennzeichnet sind, aber nicht mit der **\_ vollständigen VSS fsbt- \_ \_ Sicherung \_ erforderlich** sind. Angenommen, diese Komponente kann nicht für die Sicherung ausgewählt werden (*bwählwar* false, als [**ivsskreateschreitermetadata:: addComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponent) aufgerufen wurde). Bei einer Protokoll Sicherung bedeutet dies, dass alle Dateien in dieser Komponente immer gesichert werden müssen. Im Fall einer vollständigen Sicherung muss jedoch keine der Dateien gesichert werden, obwohl die Selektivität der Komponente impliziert, dass Sie gesichert werden soll.

### <a name="backup-by-last-modify-time"></a>Sicherung nach Zeitpunkt der letzten Änderung

Die Datei Spezifikations Informationen, die in der [**IVssBackupComponents:: gatherschreitermetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) -Phase angegeben sind, weisen nicht die Anforderer Informationen zu den Änderungen auf, die seit der letzten Sicherung geändert wurden. Eine Möglichkeit für einen Writer, Änderungen an der anfordernden Person anzugeben, ist die Verwendung des differenzierten Datei Mechanismus. Ein Writer kann angeben, dass bestimmte Dateien in einer Komponente nur gesichert werden sollen, wenn Sie seit einer bestimmten Zeit geändert wurden. der Writer kann diese Dateien entweder in [**IVssBackupComponents::P maeforbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) oder in [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)angeben. Ein Anforderer kann diese Dateien durch Aufrufen von [**IVssComponent:: getdifferencedfilescount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfilescount) und [**IVssComponent:: getdifferencedfile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfile)ermitteln. Wenn die Datei Spezifikation mit einem Satz in **IVssBackupComponents:: gatherschreitermetadata** übereinstimmt (der derzeit basierend auf der Sicherungstyp Maske gültig ist), überschreibt die differenzierten Dateiinformationen die vorherigen Informationen. Das heißt, die Dateien, die mit dieser Datei Spezifikation übereinstimmen, werden jetzt nur gesichert, wenn Sie seit der angegebenen Zeit geändert wurden. Die Uhrzeit der letzten Änderung wird über eine [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) -Struktur kommuniziert. Wenn der Wert dieser Struktur 0 (null) ist, bedeutet dies, dass der Zeitpunkt der letzten Änderung basierend auf dem Datensatz des Anforderers für den Zeitpunkt der letzten Sicherung bestimmt werden soll.

### <a name="partial-file-backup"></a>Teil Datei Sicherung

Eine andere Möglichkeit für einen Writer, Änderungen an der anfordernden Person anzugeben, ist die Verwendung des partiellen Datei Mechanismus. Ein Writer kann Byte Bereiche innerhalb von Komponenten Dateien angeben, die gesichert werden müssen. der Writer kann diese Datei Bereiche entweder in [**IVssBackupComponents::P Analyse forbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) oder in [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)angeben. Ein Anforderer kann diese Dateien durch Aufrufen von [**IVssComponent:: GetPartialFileCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfilecount) und [**IVssComponent:: GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile)ermitteln. **IVssComponent:: GetPartialFile** gibt einen Pfad und einen Dateinamen zurück, der auf die Datei verweist, und eine Bereichs Zeichenfolge, die angibt, welche Elemente in der Datei gesichert werden müssen. Wie bei differenzierten Dateien überschreiben die partiellen Dateiinformationen die vorherige Einstellung, wenn der Pfad und der Dateiname mit einer Datei Spezifikation übereinstimmen, die vom Writer in [**IVssBackupComponents:: gatherwrite Metadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata)festgelegt wurde. Die Bereichs Zeichenfolge kann zwei Formate aufweisen: Sie kann entweder die Bereiche direkt angeben, oder es kann eine Datei mit Bereichs Informationen angegeben werden. Wenn Sie Bereiche direkt angeben, ist die Syntax eine durch Trennzeichen getrennte Liste der Form offset1: length1, offset2: length2, wobei jeder Offset und jede Länge eine 64-Bit-Ganzzahl ohne Vorzeichen ist. Wenn Sie eine Bereichs Datei angeben, sollte die Bereichs Zeichenfolge auf File = *filename* festgelegt werden, wobei *filename* der vollständige Pfad zur Bereichs Datei ist. Die Bereichs Datei selbst ist eine Binärdatei, die als Liste von 64-Bit-Ganzzahlen ohne Vorzeichen formatiert ist. Die erste ganze Zahl gibt an, wie viele Bereiche in der Datei dargestellt werden. Jedes nachfolgende ganzzahlige paar stellt den Offset und die Länge eines Bereichs dar. Der Anforderer muss darauf achten, diese Bereichs Datei zu sichern und wiederherzustellen.

### <a name="file-specification-rules"></a>Regeln für die Datei Spezifikation

Die durch die differenzierten Dateien und die partiellen Datei Mechanismen hinzugefügten Datei Spezifikationen ändern entweder die in [**IVssBackupComponents:: gatherwrite Metadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) festgelegten Datei Spezifikationen oder fügen vollständig neue Dateien hinzu. Wenn Sie die in **IVssBackupComponents:: gatherwrite Metadata** festgelegten Datei Spezifikationen mithilfe des partiellen Datei Mechanismus ändern, kann ein Anforderer erwarten, dass die Datei Spezifikation genau mit einer der in der Komponente in **IVssBackupComponents:: gatherwrite Metadata** festgelegten Datei Spezifikationen übereinstimmt. Die Datei Spezifikation überschneidet sich nicht teilweise mit einer anderen Datei Spezifikation, und Sie entspricht nicht den Datei Spezifikationen in anderen Komponenten des Writers. Datei Spezifikationen, die mithilfe des partiellen Datei Mechanismus hinzugefügt wurden, können sich jedoch teilweise überschneiden. Wenn dies zutrifft, überschreibt die differenzierte Datei-oder partielle Datei Spezifikation den Spezifikations Satz in **IVssBackupComponents:: gatherschreibmetadata**. Allgemeine Datei Spezifikationen können einen alternativen Speicherort aufweisen (von [**ivsswmfiledesc:: getalternateloation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation)zurückgegeben), der einen alternativen Speicherort zum Abrufen der Datei zum Zeitpunkt der Sicherung angibt. Wenn die Datei Spezifikationen, die durch die differenzierten Dateien oder partiellen Datei Mechanismen festgelegt wurden, mit einer vorhandenen Datei Spezifikation mit einem alternativen Speicherort verglichen werden, sollten die Daten von diesem alternativen Speicherort übernommen werden. Wenn die Datei Spezifikationen, die durch die differenzierten Dateien oder partiellen Datei Mechanismen festgelegt wurden, mit den vorhandenen Spezifikationen für die Komponente nicht identisch sind, sollten diese Datei Bereiche nun der Sicherung hinzugefügt werden. Der Anforderer kann davon ausgehen, dass nur Dateien auf Volumes, die bereits im Schattenkopiesatz enthalten sind, mit einem dieser Mechanismen hinzugefügt werden.

### <a name="backup-without-a-shadow-copy"></a>Sicherung ohne Schatten Kopie

Bestimmte Dateitypen müssen möglicherweise nicht von einem Schattenkopievolume gesichert werden. Dies gilt z. b. häufig für Daten Bank Protokolldateien. Da Protokolldateien monoton vergrößert werden und ein Writer genau angeben kann, welche Teile der Datei mit partiellen Dateien gesichert werden sollen, ist es oft möglich, das Protokoll vom ursprünglichen Volume zu sichern. Als Optimierung kann ein Writer mithilfe der Sicherungstyp Maske markieren, welche Dateien Schatten Kopien für verschiedene Sicherungs Typen erfordern. Der von [**ivsswmfiledebug:: getbackuptypemask**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getbackuptypemask) zurückgegebene Wert kann einen oder mehrere der folgenden Bitwerte enthalten:

<dl> <dt>

<span id="VSS_FSBT_FULL_SNAPSHOT_REQUIRED"></span><span id="vss_fsbt_full_snapshot_required"></span>**Vollständige VSS- \_ fsbt- \_ \_ Momentaufnahme \_ erforderlich**
</dt> <dd>

Für vollständige Sicherungen ist eine Schatten Kopie erforderlich.

</dd> <dt>

<span id="VSS_FSBT_DIFFERENTIAL_SNAPSHOT_REQUIRED"></span><span id="vss_fsbt_differential_snapshot_required"></span>**VSS- \_ fsbt- \_ differenzielle \_ Momentaufnahme \_ erforderlich**
</dt> <dd>

Für differenzielle Sicherungen ist eine Schatten Kopie erforderlich.

</dd> <dt>

<span id="VSS_FSBT_INCREMENTAL_SNAPSHOT_REQUIRED"></span><span id="vss_fsbt_incremental_snapshot_required"></span>**VSS \_ fsbt- \_ inkrementelle \_ Momentaufnahme \_ erforderlich**
</dt> <dd>

Für inkrementelle Sicherungen ist eine Schatten Kopie erforderlich.

</dd> <dt>

<span id="VSS_FSBT_LOG_SNAPSHOT_REQUIRED"></span><span id="vss_fsbt_log_snapshot_required"></span>**VSS- \_ fsbt- \_ Protokoll \_ Momentaufnahme \_ erforderlich**
</dt> <dd>

Für Protokoll Sicherungen ist eine Schatten Kopie erforderlich.

</dd> <dt>

<span id="VSS_FSBT_ALL_SNAPSHOT_REQUIRED"></span><span id="vss_fsbt_all_snapshot_required"></span>**VSS \_ fsbt \_ alle \_ Momentaufnahmen \_ erforderlich**
</dt> <dd>

Für alle Sicherungs Typen ist eine Schatten Kopie erforderlich. Dies ist die Standardeinstellung.

</dd> </dl>

Wenn ein bestimmtes Volume nur Komponenten enthält, für die keine Schatten Kopie für diese Sicherung erforderlich ist, kann der Anforderer den Schritt der Erstellung einer Schatten Kopie für dieses Volume überspringen. Alle Daten auf diesem Volume können direkt vom ursprünglichen Volume auf die Sicherungsmedien kopiert werden.

## <a name="restoring-files"></a>Dateien werden wieder hergestellt

### <a name="sequential-restores"></a>Sequenzielle Wiederherstellung

Nachdem der Anforderer die Ausführung eines Wiederherstellungs Vorgangs abgeschlossen hat, sendet er das postrestore-Ereignis an alle Writer. Im allgemeinen behandeln Writer dieses Ereignis, indem Sie Wiederherstellungs Vorgänge oder andere Vorgänge nach der Wiederherstellung ausführen. Die Wiederherstellung von inkrementellen Sicherungen erfolgt jedoch normalerweise als Sequenz von Wiederherstellungs Vorgängen, eine pro inkrementeller Sicherung. Der Anforderer muss den Writer darüber informieren, dass eine solche Wiederherstellung durchgeführt wird, um zu verhindern, dass eine Wiederherstellung oder andere unerwünschte Vorgänge durchgeführt werden, bis die Wiederherstellung vollständig abgeschlossen ist. Dies wird durch Aufrufen von [**IVssBackupComponents:: setadditionalbackups**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setadditionalrestores)erreicht. Diese Methode wird pro Komponente aufgerufen und weist den Writer an, dass für diese Komponente weitere Wiederherstellungen durchlaufen werden. Für die endgültige Wiederherstellung in der Sequenz sollte das Flag für die zusätzliche Wiederherstellung auf false (der Standardwert) festgelegt werden, was darauf hinweist, dass dies die letzte Wiederherstellung in der Sequenz für diese Komponente ist.

### <a name="new-targets"></a>Neue Ziele

Wenn Sie vom Writer unterstützt wird, kann der Anforderer Datendateien an einem anderen Speicherort als dem ursprünglichen Speicherort wiederherstellen. Der Anforderer kann durch Aufrufen von [**ivssexamineschreitermetadata:: getbackupschema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema)diese Unterstützung überprüfen. Der **VSS \_ - \_ Writer-Writer \_ unterstützt das \_ neue \_ zielbit** , wenn der Writer dieses Verhalten unterstützt. Der Anforderer informiert den Writer über den neuen Speicherort, indem [**IVssBackupComponents:: addnewtarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget) für jede verschobene Datei Spezifikation aufgerufen wird. Der Anforderer kann auch festlegen, dass eine bestimmte Bereichs Datei an einem anderen Speicherort wieder hergestellt werden soll. Der Anforderer informiert den Writer über diese Änderung, indem er [**IVssBackupComponents:: Server File Path**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrangesfilepath)aufruft.

### <a name="directed-targets"></a>Gesteuerte Ziele

Bei komplizierten Wiederherstellungs Szenarien kann ein Writer Bereiche einer gesicherten Datei in verschiedenen Bereichen derselben oder einer anderen Datei zuordnen. Hierzu können Sie den gerichteten Ziel Mechanismus verwenden. Der Anforderer kann nach der [**IVssBackupComponents::P reitore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) -Phase ermitteln, dass dieser Mechanismus für eine Komponente verwendet wird, indem [**IVssComponent:: getrestoretarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoretarget) aufgerufen und eine Rückgabe des **\_ \_ gerichteten VSS RT**-Objekts überprüft wird. Der Anforderer kann alle umgeleiteten Wiederherstellungen abrufen, indem [**IVssComponent:: getdirectedtargetcount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdirectedtargetcount) und [**IVssComponent:: getdirectedtarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdirectedtarget)aufgerufen werden. **IVssComponent:: getdirectedtarget** gibt einen vollständigen Pfad zu einer Quelldatei in der Sicherung und einen vollständigen Pfad zu einer Zieldatei zurück, die in wieder hergestellt wird. Außerdem wird eine Liste der Bereiche für jede dieser Dateien zurückgegeben. Der Anforderer ist dann dafür verantwortlich, die angegebenen Bereiche in der Quelldatei in den zugeordneten Bereichen in der Zieldatei wiederherzustellen. Das Format der Bereichs Zeichenfolge entspricht dem Format in [**IVssComponent:: GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile).

-   [Schreib Rolle in inkrementellen und differenziellen VSS-Sicherungen](writer-role-in-vss-incremental-and-differential-backups.md)
-   [Requestrolle in inkrementellen und differenziellen VSS-Sicherungen](requestor-role-in-vss-incremental-and-differential-backups.md)

 

 
