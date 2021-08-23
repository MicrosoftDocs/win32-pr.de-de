---
description: Während eines Sicherungsvorgang verwendet der Anfordernde IVssBackupComponents::SetBackupState, um den Typ des vorgangs in Bearbeitung zu definieren.
ms.assetid: 43dcdac7-ed8e-4150-83eb-585e0e92f13c
title: VSS-Sicherungsstatus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35701e1b576d9ea2e5464516589ae419dc73b74898768af06e974da05afffa8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056218"
---
# <a name="vss-backup-state"></a>VSS-Sicherungsstatus

Während eines Sicherungsvorgang verwendet der Anfordernde [**IVssBackupComponents::SetBackupState,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate) um den Typ des vorgangs in Bearbeitung zu definieren.

Diese Informationen sind nicht in einer leicht abrufbaren Form im Sicherungskomponentendokument enthalten, sodass anfordernde Entwickler diese Informationen unabhängig auf allen Sicherungsmedien speichern sollten.

Der Sicherungsstatus enthält Folgendes:

<dl> <dt>

<span id="Backup_Type"></span><span id="backup_type"></span><span id="BACKUP_TYPE"></span>Sicherungstyp
</dt> <dd>

Der Sicherungstyp gibt Kriterien zum Identifizieren der zu sichernden Dateien an. Die Auswertung dieser Kriterien muss mithilfe der VSS-API vorgenommen werden.

Bei der Entscheidung, welche Art von Sicherung verwendet werden soll und mit welchen Writern sie arbeiten sollen, sollten an anfordernde Stellen die Arten von Sicherungsvorgängen (bzw. Schemas– siehe [Unterstützung](writer-backup-schema-support.md)des Writersicherungsschemas) untersuchen, die von den einzelnen Writern des Systems unterstützt werden. Sicherungen unter VSS können die folgenden Typen haben:

-   Vollständig (VSS BT FULL): Dateien werden unabhängig vom letzten Sicherungsdatum \_ \_ gesichert. Der Sicherungsverlauf jeder Datei wird aktualisiert, und dieser Sicherungstyp kann als Grundlage für eine inkrementelle oder differenzielle Sicherung verwendet werden. Zum Wiederherstellen einer vollständigen Sicherung ist nur ein einzelnes Sicherungsimage erforderlich.
-   Kopiesicherung (VSS BT COPY) – wie beim VSS BT FULL-Sicherungstyp werden Dateien unabhängig vom letzten \_ \_ \_ \_ Sicherungsdatum gesichert. Der Sicherungsverlauf jeder Datei wird jedoch nicht aktualisiert, und diese Art von Sicherung kann nicht als Grundlage für eine inkrementelle oder differenzielle Sicherung verwendet werden.
-   Inkrementell (VSS BT INCREMENTAL): Die \_ VSS-API wird verwendet, um sicherzustellen, dass nur Dateien, die seit der letzten vollständigen oder inkrementellen Sicherung geändert oder hinzugefügt wurden, auf ein Speichermedium kopiert \_ werden. Das Wiederherstellen einer inkrementellen Sicherung erfordert das ursprüngliche Sicherungsimage und alle inkrementellen Sicherungsimages, die seit der ersten Sicherung erstellt wurden.
-   Differenziell (VSS BT DIFFERENTIAL): Mit der \_ VSS-API wird sichergestellt, dass nur Dateien, die seit der letzten vollständigen Sicherung geändert oder hinzugefügt wurden, auf ein Speichermedium kopiert werden. Alle Zwischensicherungsinformationen werden \_ ignoriert. Das Wiederherstellen einer differenziellen Sicherung erfordert das ursprüngliche Sicherungsimage und das letzte differenzielle Sicherungsimage, das seit der letzten vollständigen Sicherung erstellt wurde.
-   Protokolldatei (VSS BT LOG): Nur die Protokolldateien eines Writers (Dateien, die einer Komponente mit der \_ \_ [**IVssCreateWriterMetadata::AddDataBaseLogFiles-Methode**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) hinzugefügt und durch einen Aufruf von [**IVssWMComponent::GetDatabaseLogFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabaselogfile)abgerufen werden) werden sichern. Dieser Sicherungstyp ist für VSS spezifisch.

Anfordernde Können diese Sicherungen mithilfe von Informationen und Methoden außerhalb von VSS implementieren. Nur wenn eine Anfordernde eine Sicherung mithilfe der VSS-API implementiert, sollte sie einen der aufgeführten Sicherungstypen haben. Beispielsweise nimmt ein Anfordernder nur dann an einem VSS BT LOG-Sicherungstyp teil, wenn er die von \_ \_ [**IVssWMComponent::GetDatabaseLogFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabaselogfile) zurückgegebenen Informationen verwendet hat, um Protokolldateien zu identifizieren. Analog dazu gelten die VSS-Typen BT INCREMENTAL und VSS BT DIFFERENTIAL nur für inkrementelle oder differenzielle Vorgänge, wie \_ \_ unter \_ \_ Inkrementelle und [differenzielle Sicherungen beschrieben.](incremental-and-differential-backups.md)

</dd> <dt>

<span id="Specification_about_Selectability"></span><span id="specification_about_selectability"></span><span id="SPECIFICATION_ABOUT_SELECTABILITY"></span>Spezifikation zur Auswählbarkeit
</dt> <dd>

Eine VSS-Sicherung kann die VSS-Konzepte der Komponentenauswahl (dies [](vssgloss-c.md)wird als Ausführung im Komponentenmodus bezeichnet) oder ignorieren.

Ein Beispiel dafür, dass nicht im Komponentenmodus ausgeführt wird, wäre die Durchführung einer Systemimagesicherung, bei der die Sicherungsanwendung eine Zusammenarbeit mit dem Writer benötigt, um die Datenstabilität sicherzustellen, die Auswahl der Komponenten jedoch irrelevant wäre.

</dd> <dt>

<span id="Saving_Bootable_State"></span><span id="saving_bootable_state"></span><span id="SAVING_BOOTABLE_STATE"></span>Speichern des startbaren Zustands
</dt> <dd>

VSS unterstützt das Speichern des ausgeführten Systemstatus in einer vollständig startbaren Konfiguration. Dies ist jedoch nicht immer erforderlich, und die Vorbereitung des Writers zum Speichern eines startbaren Zustands kann manchmal die Echtzeitleistung eines ausgeführten Systems beeinträchtigen.

Daher geben Anfordernde an, ob eine Sicherung einen startbaren Systemstatus als Argument für [**IVssBackupComponents::SetBackupState enthält.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate) Writer bestimmen, ob sie das Speichern des startbaren Systemstatus unterstützen müssen, indem sie [**CVssWriter::IsBootableStateBackedUp aufrufen.**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-isbootablesystemstatebackedup)

Auch wenn der Systemstatus "Startbar" nicht ausgewählt ist, werden Schattenkopien der Systemdateien vorgenommen, und die Dateien können sicherungsfähig sein.

Bei der Wiederherstellung von Systemdateien sollte jedoch mit großer Sorgfalt vor worden sein, wenn der startbare Systemstatus durch die Sicherung nicht gespeichert wurde (siehe Sichern und Wiederherstellen des [Systemstatus in Windows Server 2003 R2 und Windows Server 2003 SP1).](backing-up-and-restoring-system-state-under-vss.md)

Es ist nicht möglich, diese Informationen aus einem abgerufenen Sicherungskomponentendokument wiederherzustellen. Daher sollten an anfordernde Autoren speichern, ob das System mit einem startbaren Systemstatus gesichert wurde oder nicht.

</dd> <dt>

<span id="Partial_File_Support"></span><span id="partial_file_support"></span><span id="PARTIAL_FILE_SUPPORT"></span>Teilweise Dateiunterstützung
</dt> <dd>

Einige Writer unterstützen die Dateiwiederherstellung durch das Überschreiben von Teilen der Dateien, die sie verwalten. Ein Anfordernder kann so entworfen werden, dass er dies nutzt. Wenn dies der Fall ist, wird dies durch Festlegen der Informationen in [**IVssBackupComponents::SetBackupState angegeben.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate)

</dd> </dl>

 

 



