---
description: 'Während eines Sicherungs Vorgangs verwendet der Anforderer IVssBackupComponents:: SetBackupState, um den Typ des laufenden Vorgangs zu definieren.'
ms.assetid: 43dcdac7-ed8e-4150-83eb-585e0e92f13c
title: VSS-Sicherungs Status
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9aa9250139aee9f48f9880fd4a657fa7c6c4991
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751568"
---
# <a name="vss-backup-state"></a>VSS-Sicherungs Status

Während eines Sicherungs Vorgangs verwendet der Anforderer [**IVssBackupComponents:: SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate) , um den Typ des laufenden Vorgangs zu definieren.

Diese Informationen sind nicht in einem leicht abrufbaren Formular im Dokument mit den Sicherungs Komponenten enthalten, sodass Entwickler diese Informationen unabhängig von allen Sicherungsmedien speichern sollten.

Der Sicherungs Status enthält Folgendes:

<dl> <dt>

<span id="Backup_Type"></span><span id="backup_type"></span><span id="BACKUP_TYPE"></span>Sicherungstyp
</dt> <dd>

Der Sicherungstyp gibt Kriterien für die Identifizierung von Dateien an, die gesichert werden sollen. Die Auswertung dieser Kriterien muss mithilfe der VSS-API erfolgen.

Wenn Sie entscheiden, welche Art von Sicherung Sie verfolgen und welche Writer verwendet werden sollen, sollten die Anforderer die Arten (oder Schemas – siehe [Unterstützung des Writer-Sicherungs Schemas](writer-backup-schema-support.md)) von Sicherungs Vorgängen untersuchen, die von den einzelnen Writer des Systems unterstützt werden. Sicherungen unter VSS können folgende Typen aufweisen:

-   Vollständig (VSS \_ BT \_ Full) – Dateien werden unabhängig vom Zeitpunkt der letzten Sicherung gesichert. Der Sicherungs Verlauf der einzelnen Dateien wird aktualisiert, und dieser Sicherungstyp kann als Grundlage für eine inkrementelle oder differenzielle Sicherung verwendet werden. Zum Wiederherstellen einer vollständigen Sicherung ist nur ein einzelnes Sicherungs Abbild erforderlich.
-   Kopier Sicherung (VSS \_ BT- \_ Kopie) – wie der \_ Vollständige VSS BT- \_ Sicherungstyp werden Dateien unabhängig vom Zeitpunkt der letzten Sicherung gesichert. Der Sicherungs Verlauf der einzelnen Dateien wird jedoch nicht aktualisiert, und diese Art der Sicherung kann nicht als Grundlage für eine inkrementelle oder differenzielle Sicherung verwendet werden.
-   Inkrementell (VSS \_ BT \_ inkrementell) – mit der VSS-API wird sichergestellt, dass nur Dateien, die seit der letzten vollständigen oder inkrementellen Sicherung geändert oder hinzugefügt wurden, auf ein Speichermedium kopiert werden. Zum Wiederherstellen einer inkrementellen Sicherung sind das ursprüngliche Sicherungs Abbild und alle inkrementellen Sicherungs Abbilder seit der ersten Sicherung
-   Differenziell (VSS \_ BT \_ differenziell) – die VSS-API wird verwendet, um sicherzustellen, dass nur Dateien, die seit der letzten vollständigen Sicherung geändert oder hinzugefügt wurden, auf ein Speichermedium kopiert werden. alle zwischen Sicherungs Informationen werden ignoriert. Zum Wiederherstellen einer differenziellen Sicherung sind das ursprüngliche Sicherungs Image und das letzte differenzielle Sicherungs Abbild erforderlich, das seit der letzten vollständigen Sicherung erstellt wurde.
-   Protokolldatei (VSS \_ BT \_ -Protokoll) – nur die Protokolldateien eines Writers (Dateien, die zu einer Komponente mit der [**ivsskreateschreitermetadata:: adddatabaselogfiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) -Methode hinzugefügt und durch einen Aufrufen von [**ivsswmcomponent:: getdatabaselogfile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabaselogfile)abgerufen wurden) werden gesichert. Dieser Sicherungstyp ist spezifisch für VSS.

Es ist möglich, dass Anforderer diese Sicherungen mithilfe von Informationen und Methoden außerhalb von VSS implementieren kann. Nur wenn ein Anforderer eine Sicherung mithilfe der VSS-API implementiert, sollte er einen der aufgelisteten Sicherungs Typen aufweisen. Beispielsweise nimmt ein Anforderer an einem VSS \_ BT- \_ Protokolltyp "Backup" nur dann Teil, wenn er die von [**ivsswmcomponent:: getdatabaselogfile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabaselogfile) zurückgegebenen Informationen verwendet hat, um Protokolldateien zu identifizieren. Entsprechend \_ \_ gelten die differenziellen Typen VSS BT und VSS \_ BT \_ nur für inkrementelle oder differenzielle Vorgänge, wie in [inkrementellen und differenziellen Sicherungen](incremental-and-differential-backups.md)beschrieben.

</dd> <dt>

<span id="Specification_about_Selectability"></span><span id="specification_about_selectability"></span><span id="SPECIFICATION_ABOUT_SELECTABILITY"></span>Spezifikation zur selekabilität
</dt> <dd>

Bei einer VSS-Sicherung können VSS-Konzepte der Komponentenauswahl berücksichtigt werden – dies wird als Ausführung im [*Komponenten Modus*](vssgloss-c.md)bezeichnet – oder, um Sie zu ignorieren.

Ein Beispiel für die Nichtausführung von im Komponenten Modus wäre die Durchführung einer System Abbild Sicherung, bei der die Sicherungs Anwendung eine Writer-Zusammenarbeit benötigt, um die Daten Stabilität sicherzustellen, wobei die Auswahl von Komponenten irrelevant wäre.

</dd> <dt>

<span id="Saving_Bootable_State"></span><span id="saving_bootable_state"></span><span id="SAVING_BOOTABLE_STATE"></span>Start barer Zustand wird gespeichert.
</dt> <dd>

VSS unterstützt das Speichern des Betriebssystem Zustands in einer vollständig Start baren Konfiguration. Dies ist jedoch nicht immer erforderlich, und die Schreib Vorbereitung zum Speichern eines Start baren Zustands kann mitunter die Echtzeitleistung eines laufenden Systems beeinträchtigen.

Daher geben Anforderer an, ob eine Sicherung einen Start fähigen Systemstatus als Argument für [**IVssBackupComponents:: SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate)enthält. Writer bestimmen, ob das Speichern des Start baren Systemzustands durch Aufrufen von [**CVssWriter:: isbootablestatebackedup**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-isbootablesystemstatebackedup)unterstützt werden muss.

Selbst wenn der Start Bare Systemstatus nicht ausgewählt ist, werden Schatten Kopien der Systemdateien erstellt, und die Dateien können gesichert werden.

Beim Wiederherstellen von Systemdateien sollte jedoch sehr sorgfältig vorgegangen werden, wenn die Sicherung den Start baren Systemstatus nicht gespeichert hat (siehe [Sichern und Wiederherstellen des Systemstatus in Windows Server 2003 R2 und Windows Server 2003 SP1](backing-up-and-restoring-system-state-under-vss.md)).

Es ist nicht möglich, diese Informationen aus einem abgerufenen Sicherungs Komponenten Dokument wiederherzustellen, sodass die Autoren von Anforderern speichern können, ob das System mit einem Start baren Systemstatus gesichert wurde.

</dd> <dt>

<span id="Partial_File_Support"></span><span id="partial_file_support"></span><span id="PARTIAL_FILE_SUPPORT"></span>Unterstützung für Teil Dateien
</dt> <dd>

Einige Writer unterstützen die Wiederherstellung von Dateien durch das Überschreiben von Teilen der Dateien, die Sie verwalten. Ein Anforderer kann diese Funktion nutzen, und wenn dies der Fall ist, wird er durch Festlegen der Informationen in [**IVssBackupComponents:: SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate)festgelegt.

</dd> </dl>

 

 



