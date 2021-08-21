---
description: Ein Wiederherstellungssatz ist eine Liste aller wiederherzustellenden Dateien und der Speicherorte, an denen sie wiederhergestellt werden.
ms.assetid: 3196c26c-3407-4c00-a800-c3497df583e5
title: Generieren eines Wiederherstellungssatzes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b85dd620869614420e5073f47ef4ac8732b1e2c0d0d218ea0e94ae690cb9f773
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119958450"
---
# <a name="generating-a-restore-set"></a>Generieren eines Wiederherstellungssatzes

Ein Wiederherstellungssatz ist eine Liste aller wiederherzustellenden Dateien und der Speicherorte, an denen sie wiederhergestellt werden.

Wie beim Generieren der Sicherungsdateiliste (siehe [Generieren eines Sicherungssatzes)](generating-a-backup-set.md)muss ein Algorithmus, mit dem bestimmt wird, welche Dateien wiederhergestellt werden sollen und wo sie wiederhergestellt werden sollen, [*die Writerinstanz*](vssgloss-w.md) nach Writerinstanz und komponentenweise für jede Writerinstanz fortsetzen.

Es ist erforderlich, jede Datei auf dem Sicherungsmedium der Komponente zuzuordnen, die sie verwaltet hat. Es ist auch erforderlich, die [*Wiederherstellungsmethode*](vssgloss-r.md)der Verwaltungskomponente sowie die [*Wiederherstellungszielinformationen*](vssgloss-r.md) der Datei sowie die [*alternativen Speicherortzuordnungen*](vssgloss-a.md) (falls vorhanden) abzurufen.

Einige Dateien erfordern möglicherweise auch [*Teildateienvorgänge*](vssgloss-p.md) oder [*gerichtete Ziele*](vssgloss-d.md) für die Wiederherstellung.

Durch Untersuchen der [*Selektivität*](vssgloss-s.md) der Komponenten für Sicherungen und [*logische Pfade*](vssgloss-l.md) (siehe Arbeiten [mit Selektorierbarkeit und logischen Pfaden)](working-with-selectability-and-logical-paths.md)kann ein Anforderer die Komponentenstruktur des Sicherungsvorgangs bestimmen, den er wiederherstellen wird.

Wenn die Komponentenstruktur der Sicherung eingerichtet ist, kann der Anforderer die [*Dateisatzinformationen*](vssgloss-f.md) jeder Komponente abrufen (Dateispezifikation, Pfad und Rekursionsflag). Ein Anforderer kann dann einen Wiederherstellungssatz generieren.

Dateien, die [*Teildateien*](vssgloss-p.md)oder [*gerichtete Ziele*](vssgloss-d.md) erfordern, bieten eigene detaillierte Wiederherstellungsanweisungen (siehe [Nicht standardmäßige Sicherungs- und Wiederherstellungsspeicherorte),](non-default-backup-and-restore-locations.md)die dann dem Wiederherstellungssatz hinzugefügt werden können.

Ein typischer Mechanismus zum Generieren eines Wiederherstellungssatzes für Dateien, die nicht an Teildateienvorgängen oder [*gerichteten Zielen*](vssgloss-d.md) beteiligt sind, kann wie folgt vorgehen:

1.  Rufen Sie eine Liste der Dateien auf dem Sicherungsmedium ab, einschließlich ihrer ursprünglichen Pfade.

2.  Identifizieren Sie die [*Writer-Klasse*](vssgloss-w.md) und -Komponente für jede Datei auf dem Sicherungsmedium wie folgt:

    -   Rufen Sie für jeden Writer Komponenteninformationen [**(IVssWMComponent)**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent)ab, indem [**Sie IVssEx csvWriterMetadata::GetComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getcomponent) für alle zugehörigen Komponenten aufrufen.
    -   Rufen Sie für jede Komponente Dateideskriptorinformationen [**(IVssWMFiledesc)**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc)für jeden Satz von Dateien ab, die die Komponente enthält (abhängig von den Datentypen, die die Komponente enthält, indem [**Sie IVssWMComponent::GetFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getfile), [**IVssWMComponent::GetDatabaseFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabasefile)und [**IVssWMComponent::GetDatabaseLogFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabaselogfile)aufrufen.
    -   Vergleichen Sie den Namen und die Pfadinformationen der Datei mit den Pfadinformationen, die im Dateideskriptor für jeden Satz von Dateien in einer Komponente zurückgegeben werden (zurückgegeben von [**IVssWMFiledesc::GetPath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getpath), [**IVssWMFiledesc::GetFilespec**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getfilespec)und [**IVssWMFiledesc::GetRecursive),**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getrecursive)um zu bestimmen, ob die Datei Teil der Komponente ist.
        > [!Note]  
        > Sie sollten alle alternativen Speicherortinformationen im Dateideskriptor ignorieren, die aus einer Komponente in einem gespeicherten Writer-Metadatendokument abgerufen wurden (d.h. [**IVssWMFiledesc::GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) gibt nicht **NULL** zurück). Dieser alternative Speicherort ist der [*alternative Pfad,*](vssgloss-a.md)der nur während der Sicherung verwendet wird.

         

3.  Rufen Sie alternative Zuordnungsinformationen für jede Datei auf dem Sicherungsmedium ab:

    -   Alternative Dateizuordnungen werden auf Writer- und nicht auf Komponentenebene gespeichert und aus dem Objekt [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) abgerufen, das von [**IVssExwriterMetadata::GetAlternateLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping)zurückgegeben wird.
    -   Sie können ermitteln, ob eine bestimmte Datei über eine alternative Speicherortzuordnung verfügt, indem Sie den Pfad und den Namen der Datei anhand des Pfads und der Dateispezifikation überprüfen, die in der alternativen Speicherortzuordnung enthalten sind, die von [**IVssExgineWriterMetadata::GetAlternateLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping)zurückgegeben wird, über [**IVssWMFiledesc::GetPath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getpath), [**IVssWMFiledesc::GetFiledesc::GetFilespec**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getfilespec)und [**IVssWMFiledesc::GetRecursive**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getrecursive). (Wenn während der Sicherung ein alternativer Pfad verwendet wurde, sollten diese Informationen während dieser Überprüfung bei der Verarbeitung einer Wiederherstellung ignoriert werden.)
    -   Wenn eine Datei und eine alternative Speicherortzuordnungsdatei-Deskriptoren übereinstimmen, verwenden Sie die [**IVssWMFiledesc::GetAlternateLocation-Methode**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) des [**IVssWMFiledesc-Objekts,**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) das von [**IVssExmobileWriterMetadata::GetAlternateLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping) zurückgegeben wird, um den alternativen Speicherort zu finden, an dem Sie die Datei wiederherstellen können.
    -   Die auf diese Weise abgerufene alternative Standortzuordnung stimmt nicht unbedingt mit der zuordnung überein, die vom Sicherungskomponentendokument von [**IVssComponent::GetAlternateLocationMapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmapping)zurückgegeben wird. Der [**IVssWMFiledesc::GetAlternateLocation-Wert**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) ist nur dann nicht leer, wenn die alternative Speicherortzuordnung für eine Datei verwendet wird.

4.  Mit diesen Datei- und Komponenteninformationen kann das Sicherungskomponentendokument abgefragt werden, um Informationen zu Wiederherstellungszielen, Optionen und neuen Wiederherstellungsspeicherorten für jede Datei abzurufen. Diese Informationen können mit der Liste der Dateien, Komponenten und alternativen Speicherorte kombiniert werden.

5.  Dateien, die nicht durch Writer geschützt sind, können in Übereinstimmung mit herkömmlichen Wiederherstellungsvorgängen ausgewählt werden.

An diesem Punkt sollte ein Anforderer über eine Liste aller Dateien verfügen, die er wiederherstellen muss, zusammen mit Anweisungen zum Wiederherstellen dieser Dateien, und kann mit der Wiederherstellung von Dateien auf der Grundlage von folgendem Grund beginnen:

-   Ob alternative Speicherortzuordnungen oder der ursprüngliche Dateispeicherort als Ziel für die Wiederherstellung verwendet werden soll, hängt vom Vorhandensein oder Fehlen einer Datei an diesem Zielspeicherort und den Komponenteneinstellungen von [**VSS \_ RESTORE \_ TARGET**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restore_target) und [**VSS \_ RESTOREMETHOD \_ ENUM**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) ab (siehe [Nicht standardmäßige Sicherungs- und Wiederherstellungsspeicherorte).](non-default-backup-and-restore-locations.md)
-   Ob ein Wiederherstellungsversuch erfolgreich ist, hängt von Problemen wie den Zugriffsberechtigungen des Ziels, dem Sperren von Zieldateien und anderen herkömmlichen Problemen bei der Dateiwiederherstellung ab.
-   Der Erfolg oder Fehler beim Wiederherstellen einer bestimmten Komponente für eine bestimmte Writerinstanz sollte im Sicherungskomponentendokument beibehalten werden, indem [**IVssBackupComponents::SetFileRestoreStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setfilerestorestatus)aufgerufen wird. Dadurch können Writer auf die Informationen zugreifen, wenn sie das PostRestore-Ereignis verarbeiten.
-   Wenn eine Datei an einer alternativen Speicherortzuordnung wiederhergestellt wird, muss der Anforderer [**IVssBackupComponents::AddAlternativeLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addalternativelocationmapping)aufrufen. Dadurch können Writer ermitteln, ob ihre Dateien über [**IVssComponent::GetAlternateLocationMapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmapping)an alternativen Speicherorten wiederhergestellt wurden.
-   Anforderer finden es möglicherweise wünschenswert, Dateien an völlig neuen Speicherorten wiederherzustellen. Dies ist akzeptabel, aber der Anforderer muss dies dem Writer mithilfe der [**IVssBackupComponents::AddNewTarget-Methode**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget) angeben.

 

 



