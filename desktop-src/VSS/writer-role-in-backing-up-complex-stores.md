---
description: Wie bei allen wichtigen Vorgängen unter VSS erfordern inkrementelle und differenzielle Sicherungen eine enge Zusammenarbeit zwischen Anforderern und Writern.
ms.assetid: 3cf5dd1f-dc58-42bc-925f-fee7d34053c5
title: Writer-Rolle beim Sichern komplexer Filialen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80864256b9a19c25a2f0dce0d0c929ed19fd7269
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129268"
---
# <a name="writer-role-in-backing-up-complex-stores"></a>Writer-Rolle beim Sichern komplexer Filialen

Wie bei allen wichtigen Vorgängen unter VSS erfordern [*inkrementelle*](vssgloss-i.md) und [*differenzielle*](vssgloss-d.md) Sicherungen eine enge Zusammenarbeit zwischen Anforderern und Writern.

## <a name="backup-types"></a>Sicherungs Typen

Die-Infrastruktur bietet spezielle Unterstützung für fünf Arten von Sicherungen. Die Schritte lassen sich wie folgt beschreiben:

-   Vollständig (**VSS \_ BT \_ vollständig**). Dateien werden unabhängig vom Zeitpunkt der letzten Sicherung gesichert. Der Sicherungs Verlauf der einzelnen Dateien wird aktualisiert, und dieser Sicherungstyp kann als Grundlage für eine inkrementelle oder differenzielle Sicherung verwendet werden. Wenn Protokolldateien vorhanden sind, werden Sie möglicherweise als Ergebnis dieser Sicherung abgeschnitten.

    Zum Wiederherstellen einer vollständigen Sicherung ist nur ein einzelnes Sicherungs Abbild erforderlich.

-   Differenziell (**VSS \_ BT- \_ differenziell**). Die VSS-API wird verwendet, um sicherzustellen, dass nur Dateien, die seit der letzten vollständigen Sicherung geändert oder hinzugefügt wurden, auf ein Speichermedium kopiert werden. alle Informationen zur zwischen Sicherung werden ignoriert. Dies kann ganze Dateien oder bestimmte Bereiche innerhalb von Dateien einschließen. Eine differenzielle Sicherung ist einer vollständigen Sicherung zugeordnet und kann im allgemeinen erst wieder hergestellt werden, wenn die vollständige Sicherung wieder hergestellt wurde. Wenn Protokolldateien vorhanden sind, werden Sie in der Regel nicht als Ergebnis dieser Sicherung abgeschnitten.

    Zum Wiederherstellen einer differenziellen Sicherung sind das ursprüngliche Sicherungs Image und das letzte differenzielle Sicherungs Abbild erforderlich, das seit der letzten vollständigen Sicherung erstellt wurde.

-   Inkrementell (**VSS \_ BT \_ inkrementell** Die VSS-API wird verwendet, um sicherzustellen, dass nur Dateien, die seit der letzten vollständigen oder inkrementellen Sicherung geändert oder hinzugefügt wurden, auf ein Speichermedium kopiert werden. Dies kann ganze Dateien oder bestimmte Bereiche innerhalb von Dateien einschließen. Einige Writer lassen nicht zu, dass inkrementelle Sicherungen mit differenziellen Sicherungen gemischt werden. Wenn Protokolldateien vorhanden sind, werden Sie möglicherweise als Ergebnis dieser Sicherung abgeschnitten.

    Zum Wiederherstellen einer inkrementellen Sicherung sind das ursprüngliche Sicherungs Abbild und alle inkrementellen Sicherungs Abbilder seit der ersten Sicherung

-   Protokoll Sicherung (**VSS \_ BT- \_ Protokoll**). Es werden nur die Protokolldateien eines Writers (Dateien, die einer Komponente mit der [**ivssdeateschreitermetadata:: adddatabaselogfiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) -Methode hinzugefügt und durch einen Aufrufen von [**ivsswmcomponent:: getdatabaselogfile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabaselogfile)abgerufen werden) gesichert. Dieser Sicherungstyp ist spezifisch für VSS. Protokoll Sicherungen werden in der Regel sehr häufig durchgeführt. In der Regel wird die Protokolldatei als Ergebnis dieser Sicherung abgeschnitten.
-   Kopier Sicherung (**VSS \_ BT- \_ Kopie**). Ebenso wie der \_ Vollständige VSS BT- \_ Sicherungstyp werden Dateien unabhängig vom Zeitpunkt der letzten Sicherung gesichert. Der Sicherungs Verlauf der einzelnen Dateien wird jedoch nicht aktualisiert, und dieser Sicherungstyp kann nicht als Grundlage für eine inkrementelle oder differenzielle Sicherung verwendet werden. Protokolldateien sollten aufgrund einer Kopiesicherung nie abgeschnitten werden.

<dl> <dt>

<span id="Partial_File_Support"></span><span id="partial_file_support"></span><span id="PARTIAL_FILE_SUPPORT"></span>Unterstützung für Teil Dateien
</dt> <dd>

Einige Writer unterstützen die Wiederherstellung von Dateien durch das Überschreiben von Teilen der Dateien, die Sie verwalten. Ein Anforderer kann diese Funktion nutzen, und wenn dies der Fall ist, wird er durch Festlegen der Informationen in [**IVssBackupComponents:: SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate)festgelegt.

</dd> </dl>

Die Writer geben an, welche Art von Sicherungen durch Aufrufen von [**ivsscreatewritermetadata:: setbackupschema**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setbackupschema) bei der Verarbeitung des [*identifizierungsereignisses*](vssgloss-i.md) unterstützt werden. Der *dsschemamask* -Parameter für die **ivsskreateschreitermetadata:: setbackupschema** -Methode ist eine Bitmaske, die angibt, welche Sicherungs Typen unterstützt werden. Alle Writer müssen vollständige Sicherungen unterstützen.

<dl> <dt>

<span id="VSS_BS_DIFFERENTIAL"></span><span id="vss_bs_differential"></span>**VSS- \_ SB- \_ differenziell**
</dt> <dd>

Gibt die Unterstützung für differenzielle Sicherungen an.

</dd> <dt>

<span id="VSS_BS_INCREMENTAL"></span><span id="vss_bs_incremental"></span>**\_ \_ inkrementelles VSS-**
</dt> <dd>

Gibt Unterstützung für inkrementelle Sicherungen an

</dd> <dt>

<span id="VSS_BS_LOG"></span><span id="vss_bs_log"></span>**VSS \_ - \_ Blog**
</dt> <dd>

Gibt die Unterstützung für Protokoll Sicherungen an.

</dd> <dt>

<span id="VSS_BS_COPY"></span><span id="vss_bs_copy"></span>**VSS- \_ SB- \_ Kopie**
</dt> <dd>

Gibt die Unterstützung für Kopier Sicherungen an.

</dd> <dt>

<span id="VSS_BS_EXCLUSIVE_INCREMENTAL_DIFFERENTIAL"></span><span id="vss_bs_exclusive_incremental_differential"></span>**\_ \_ exklusive \_ inkrementelle VSS-SB \_**
</dt> <dd>

Gibt an, dass ein Writer keine inkrementellen Sicherungen mit differenziellen Sicherungen unterstützt.

</dd> </dl>

Der Writer kann ermitteln, welche Art von Sicherung durchgeführt wird, indem [**CVssWriter:: getbackuptype**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getbackuptype)aufgerufen wird. Der früheste Zeitpunkt, an dem dieser Vorgang ausgeführt werden kann, ist die Verarbeitung des PrepareForBackup-Ereignisses. **CVssWriter:: getbackuptype** gibt einen Member der [**VSS- \_ \_ Sicherungstyp**](/windows/desktop/api/Vss/ne-vss-vss_backup_type) Enumeration zurück. Wenn der Sicherungstyp vom Writer nicht unterstützt wird, sollte der Writer die Sicherung als vollständige Sicherung behandeln.

## <a name="backup-stamps"></a>Sicherungs Stempel

Inkrementelle und differenzielle Sicherungen sind immer an eine vorherige Sicherung gebunden. Es gibt zwei Möglichkeiten, Sicherungen zu verknüpfen. Bei einfachen Daten speichern kann der Anforderer die Korrelation zwischen Sicherungen nachverfolgen. Bei komplexeren Daten speichern muss der Writer aber seinen eigenen Zeitstempel mit der Sicherung beibehalten. Dieser Zeitstempel kann die Protokoll Position, die Prüf Punkt Informationen usw. nachverfolgen. Ein Writer gibt an, dass er seine eigenen Zeitstempel benötigt, indem er das Zeitstempel Bit von **VSS- \_ SB \_** festlegt, wenn er [**ivsskreateschreitermetadata:: setbackupschema**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setbackupschema)aufruft.

Ein Writer kann einen Zeitstempel mit jeder zu sichernden Komponente speichern. Der Writer speichert den Zeitstempel, indem er [**IVssComponent:: setbackupstamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp)aufruft und eine Zeichen folgen Darstellung des Stempels für den Parameter *wszbackupstamp* übergibt. Im allgemeinen Ruft ein Writer diese Methode auf, während das [*PostSnapshot*](vssgloss-p.md) -Ereignis verarbeitet wird. Bei Sicherungen, die keine Schatten Kopie enthalten, wird das PostSnapshot-Ereignis jedoch nicht gesendet. In diesem Fall muss **IVssComponent:: setbackupstamp** aufgerufen werden, während das [*PrepareForBackup*](vssgloss-p.md) -Ereignis verarbeitet wird.

Wenn eine inkrementelle oder differenzielle Sicherung durchgeführt wird, gibt der Anforderer dem Writer den Sicherungs Stempel der vorherigen Sicherung an, der als Basis für diese Sicherung fungiert. Der Writer kann bei der Verarbeitung des PrepareForBackup-oder PostSnapshot-Ereignisses auf diesen vorherigen Sicherungs Stempel zugreifen, indem [**IVssComponent:: getpreviousbackupstamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpreviousbackupstamp)aufgerufen wird. Der Writer kann den zurückgegebenen Stempel verwenden, um zu bestimmen, was gesichert werden muss.

## <a name="backup-strategies"></a>Sicherungsstrategien

### <a name="file-backup-files-strategies"></a>Strategien für Datei Sicherungsdateien

Häufig müssen bestimmte in den Writer-Metadaten gemeldete Dateien nur gesichert werden, wenn bestimmte Sicherungs Arten durchgeführt werden. Einige Dateien sind möglicherweise nur erforderlich, wenn eine vollständige Sicherung durchgeführt wird. Andere Dateien sind möglicherweise nur beim Ausführen einer inkrementellen oder differenziellen Sicherung erforderlich. VSS stellt eine Methode bereit, mit der die Writer diese Informationen für den Anforderer angeben können. Beim Hinzufügen von Dateien zu Komponenten mithilfe von [**ivsskreateschreitermetadata:: adddatabasefiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles), [**ivsskreateschreitermetadata:: adddatabaselogfiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)oder [**ivsskreateschreitermetadata:: addfilestofilegroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup)gibt der Parameter *dwbackuptypemask* an, für welche Sicherungs Typen diese Dateien gesichert werden müssen. Die Maske kann einen oder mehrere der folgenden Werte enthalten:

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

Eine Möglichkeit, einen Writer anzugeben, welche Dateien geändert wurden, ist die Verwendung des differenzierten Datei Mechanismus. Ein Writer kann angeben, dass bestimmte Dateien in einer Komponente nur gesichert werden sollen, wenn Sie seit einer bestimmten Zeit geändert wurden. Der Writer ruft [**IVssComponent:: AddDifferencedFilesByLastModifyTime**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime) mit einer Datei Spezifikation und einem Zeitpunkt der letzten Änderung auf. **IVssComponent:: AddDifferencedFilesByLastModifyTime** wird in der Regel während der Verarbeitung des PostSnapshot-Ereignisses aufgerufen, obwohl es bei der Verarbeitung des PrepareForBackup-Ereignisses aufgerufen werden kann. Der Anforderer muss dann alle Dateien sichern, die der Datei Spezifikation entsprechen, die sich seit der angegebenen Zeit geändert haben. Wenn der Writer den Sicherungs Stempel Mechanismus verwendet, wird dieser Zeitpunkt der letzten Änderung basierend auf dem vorherigen Sicherungs Stempel im Sicherungs Dokument festgelegt. Der Writer kann auch für den Zeitpunkt der letzten Änderung den Wert 0 (null) übergeben, was darauf hinweist, dass die anfordernde Person für die Bestimmung der Uhrzeit der letzten Sicherung und der Änderung der Dateien seit diesem Zeitpunkt zuständig ist.

### <a name="partial-file-backup"></a>Teil Datei Sicherung

Eine andere Möglichkeit für einen Writer, Änderungen an der anfordernden Person anzugeben, ist die Verwendung des partiellen Datei Mechanismus. Ein Writer kann Byte Bereiche innerhalb von Komponenten Dateien angeben, die gesichert werden müssen. der Writer kann diese Datei Bereiche bei der Verarbeitung des PostSnapshot-oder PrepareForBackup-Ereignisses angeben. Der Writer ruft [**IVssComponent:: addpartialfile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile) auf, um der Sicherung partielle Datei Spezifikationen hinzuzufügen. Eine partielle Datei Spezifikation besteht aus einem Pfad und einem Dateinamen sowie Informationen dazu, welche Bereiche in der Datei gesichert werden müssen.

### <a name="file-specification-rules"></a>Regeln für die Datei Spezifikation

[**IVssComponent:: AddDifferencedFilesByLastModifyTime**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime) oder [**IVssComponent:: addpartialfile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile) kann verwendet werden, um die während des Identifizierungs Ereignisses angegebenen Datei Spezifikationen zu ändern oder um der Spezifikation vollständig neue Dateien hinzuzufügen. Wenn der Writer Informationen, die während des Identifizierungs Ereignisses mithilfe von **IVssComponent:: AddDifferencedFilesByLastModifyTime** festgelegt wurden, ändert, muss die Datei Spezifikation genau mit einer der Datei Spezifikationen in der aktuellen Komponente übereinstimmen. Die Datei Spezifikation darf Dateien in der aktuellen Komponente nicht teilweise überlappen, und Sie darf nicht mit Dateien in anderen Komponenten identisch sein. Mithilfe von **IVssComponent:: addpartialfile** angegebene Dateien können sich jedoch teilweise mit einer anderen Datei Spezifikation überlappen. Informationen, die von **IVssComponent:: AddDifferencedFilesByLastModifyTime** oder **IVssComponent:: addpartialfile** festgelegt werden, überschreiben die zuvor festgelegten Informationen mithilfe der [**ivsskreateschreitermetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata) -Schnittstelle als Reaktion auf das identifizeignis.

Allgemeine Datei Spezifikationen können einen alternativen Speicherort aufweisen (festgelegt durch den *wszalternate eloation* -Parameter von [**ivsscomateschreitermetadata:: addfilestofilegroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup)), der einen alternativen Speicherort zum Abrufen der Datei zum Zeitpunkt der Sicherung angibt. Wenn die Datei Spezifikation, die mithilfe der differenzierten Datei-oder partiellen Datei Mechanismen festgelegt wurde, mit einer vorhandenen Datei Spezifikation übereinstimmt, die einen alternativen Speicherort aufweist, ruft die Sicherungs Anwendung die Daten von diesem alternativen Speicherort ab.

Wenn die in [**IVssComponent:: AddDifferencedFilesByLastModifyTime**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime) oder in [**IVssComponent:: addpartialfile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile) festgelegte Datei Spezifikation nicht mit den Dateien in der zu sichernden Komponente übereinstimmt, werden der Sicherung jetzt alle übereinstimmenden Dateien hinzugefügt. Es muss darauf geachtet werden, dass der Writer nur Dateien hinzufügt, die auf einem Volume vorhanden sind, auf das bereits Schatten Kopien kopiert werden. Andernfalls kann der Anforderer die Dateien nicht sichern. Wenn diese Funktionen bei der Verarbeitung des PostSnapshot-Ereignisses aufgerufen werden, kann dies mithilfe der [**CVssWriter:: ispathbetroffenmethode**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-ispathaffected) bestimmt werden. Wenn beim Verarbeiten des PrepareForBackup-Ereignisses aufgerufen wird, muss der Writer diese Bestimmung mithilfe einer anderen Methode treffen.

### <a name="backup-without-a-shadow-copy"></a>Sicherung ohne Schatten Kopie

Bestimmte Dateitypen müssen möglicherweise nicht von einem Schattenkopievolume gesichert werden. Dies gilt z. b. häufig für Daten Bank Protokolldateien. Da Protokolldateien monoton vergrößert werden und ein Writer genau angeben kann, welche Teile der Datei mit partiellen Dateien gesichert werden sollen, ist es oft möglich, das Protokoll vom ursprünglichen Volume zu sichern. Als Optimierung ein Writer kann markieren, welche Dateien Schatten Kopien für verschiedene Sicherungs Typen erfordern, indem er die Flags verwendet, die im *dwbackuptypemask* -Parameter von [**ivsskreateschreitermetadata:: adddatabasefiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles), [**ivsskreateschreitermetadata:: adddatabaselogfiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)oder [**ivsskreateschreitermetadata:: addfilestofilegroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup)fest Folgende Flags werden unterstützt:

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

## <a name="backup-cleanup"></a>Sicherungscleanup

Wenn der Writer die Protokoll Verkürzung oder eine andere Bereinigung nach der Sicherung ausführen muss, ist dies der richtige Speicherort für die Verarbeitung des [*BackupComplete*](vssgloss-b.md) -Ereignisses. Das [*BackupShutdown*](vssgloss-b.md) -Ereignis wird nach dem Backup-Vorgang einige Zeit gesendet, sodass einige Bereinigungs Schritte auch im BackupShutdown-Ereignishandler ausgeführt werden können.

Das BackupShutdown-Ereignis wird immer nach Beendigung einer Sicherung gesendet. Wenn die anfordernde Person beim Ausführen einer Sicherung nicht ordnungsgemäß beendet wird, wird das BackupShutdown sofort gesendet, ohne dass zuvor BackupComplete gesendet wurde. Wenn der Writer einen Status bereinigen muss, kann dies hier geschehen. das Abschneiden von Protokollen sollte in diesem Fall jedoch nicht erfolgen, da die Sicherung nicht notwendigerweise beendet wurde.

## <a name="restore-strategies"></a>Wiederherstellungs Strategien

Bei der grundlegenden Aufgabe von Writern bei der Wiederherstellung muss überprüft werden, ob die Wiederherstellung bei der Verarbeitung des vorab Ereignisses stattfinden kann, und dass die Wiederherstellung bei der Behandlung des postrestore-Ereignisses stattgefunden hat. Komplexere Speicher führen außerdem einen Wiederherstellungsprozess im postrestore-Handler aus. Wenn die Wiederherstellung Teil einer inkrementellen oder differenziellen Wiederherstellung ist, möchte der Writer diesen Wiederherstellungsprozess im allgemeinen verzögern, bis alle inkrementellen oder differenziellen Wiederherstellungen abgeschlossen sind. [**IVssComponent:: getadditionalrestore**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getadditionalrestores) gibt an, ob dies die endgültige Wiederherstellung dieser Komponente ist oder ob weitere Wiederherstellungen vorhanden sind. Wenn **IVssComponent:: getadditionalrecovery** den Wert **true** zurückgibt, sollte der Writer seine Wiederherstellungs Prozedur nicht für diese Komponente ausführen.

## <a name="new-targets"></a>Neue Ziele

Wenn Sie vom Writer unterstützt wird, kann der Anforderer Datendateien an einem anderen Speicherort als dem ursprünglichen Speicherort wiederherstellen. Ein Writer gibt die Unterstützung für diesen Wiederherstellungs Modus an, indem er den **VSS- \_ \_ Writer \_ unterstützt das \_ neue \_ zielbit** im *dsschemamask* -Parameter beim Aufrufen von [**ivsscreateschreitermetadata:: setbackupschema**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setbackupschema)festlegt. Ein Writer ruft die neuen Speicherorte für Komponenten Dateien zum Zeitpunkt der Wiederherstellung ab, indem [**IVssComponent:: getnewtargetcount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtargetcount) und [**IVssComponent:: getnewtarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtarget)aufgerufen werden.

## <a name="directed-targets"></a>Gesteuerte Ziele

Bei komplizierten Wiederherstellungs Szenarien kann ein Writer Bereiche einer gesicherten Datei in verschiedenen Bereichen derselben oder einer anderen Datei zuordnen. Dies kann mithilfe des gerichteten Ziel Mechanismus erreicht werden. Zu diesem Zweck muss ein Writer zunächst angeben, dass dies geschieht, indem [**IVssComponent:: abtrestoretarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoretarget)aufgerufen wird, wobei **VSS RT an den \_ \_** *Ziel* Parameter weitergeleitet wird. Dann ruft der Writer für jede Zuordnung [**IVssComponent:: adddirectedtarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddirectedtarget)auf. Diese Methode nimmt einen vollständigen Pfad zu einer Quelldatei in der Sicherung und einen vollständigen Pfad zu einer Zieldatei an, die in wieder hergestellt wird. Außerdem wird eine Liste der Bereiche für jede dieser Dateien benötigt. Der Writer ruft diese Funktionen auf, während das PreRestore-Ereignis verarbeitet wird, und der Anforderer ist dann dafür verantwortlich, die angegebenen Bereiche in der Quelldatei in den zugeordneten Bereichen in der Zieldatei wiederherzustellen. Das Format der Bereichs Zeichenfolge ist mit dem Format in [ **IVssComponent:: addpartialfile** identisch.](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile)

## <a name="private-writer-metadata"></a>Private Writer-Metadaten

Es ist oft hilfreich, wenn ein Writer Private Metadaten mit einer Sicherung beibehält, um eine inkrementelle oder differenzielle Wiederherstellung ordnungsgemäß auszuführen. Ein Writer kann [**IVssComponent:: setbackupmetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupmetadata) aufrufen, während entweder PrepareForBackup oder PostSnapshot zum Speichern von Metadaten verarbeitet wird. Auf diese Metadaten kann der Writer während der Vorabversion oder im postrestore zugreifen, indem [**IVssComponent:: getbackupmetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata)aufgerufen wird. Metadaten können auch mit der partiellen Datei Spezifikation mithilfe des *wszmetadata* -Parameters von [**IVssComponent:: addpartialfile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile); gespeichert werden. der Zugriff auf diese Metadaten erfolgt über den *pbstraumetadata*-Parameter von [**IVssComponent:: GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile). Der Writer kann auch zwischen [**CVssWriter:: onprerestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onprerestore) und [**CVssWriter:: OnPostRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostrestore)Metadaten an sich selbst übergeben. In **CVssWriter:: onprerestore** werden die Metadaten durch den Aufruf von [**IVssComponent:: setrestoremetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoremetadata)festgelegt. In **CVssWriter:: OnPostRestore** werden die Metadaten durch Aufrufen von [**IVssComponent:: getrestoremetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoremetadata)abgerufen.

-   [Schreib Rolle in inkrementellen und differenziellen VSS-Sicherungen](writer-role-in-vss-incremental-and-differential-backups.md)
-   [Requestrolle in inkrementellen und differenziellen VSS-Sicherungen](requestor-role-in-vss-incremental-and-differential-backups.md)

 

 



