---
description: Ein Wiederherstellungs Satz ist eine Liste aller wiederherzustellenden Dateien und der Speicherorte, an denen Sie wieder hergestellt werden.
ms.assetid: 3196c26c-3407-4c00-a800-c3497df583e5
title: Erstellen eines Wiederherstellungs Satzes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db3447ba6d258a5f22fff958761abc7ac0e4f27f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358835"
---
# <a name="generating-a-restore-set"></a>Erstellen eines Wiederherstellungs Satzes

Ein Wiederherstellungs Satz ist eine Liste aller wiederherzustellenden Dateien und der Speicherorte, an denen Sie wieder hergestellt werden.

Wie beim Erstellen der Sicherungsdatei Liste (siehe [Erstellen eines Sicherungs Satzes](generating-a-backup-set.md)), ist ein Algorithmus zum bestimmen, welche Dateien wieder hergestellt werden müssen und wo Sie wieder hergestellt werden müssen, die [*Writer-Instanz*](vssgloss-w.md) nach Writer-Instanz und Komponenten Weise für jede Writer-Instanz fortgesetzt.

Es ist notwendig, jede Datei auf dem Sicherungsmedium der Komponente zuzuordnen, von der Sie verwaltet wird. Außerdem ist es erforderlich, die [*Wiederherstellungsmethode*](vssgloss-r.md)der Verwaltungs Komponente und die [*Wiederherstellungs Ziel*](vssgloss-r.md) Informationen der Datei sowie die Zuordnungen für den [*alternativen Speicherort*](vssgloss-a.md) (sofern vorhanden) abzurufen.

Für einige Dateien sind möglicherweise auch [*partielle Datei*](vssgloss-p.md) Vorgänge oder [*gesteuerte Ziele*](vssgloss-d.md) für die Wiederherstellung erforderlich.

Durch Untersuchen der [*selekabilität der Komponenten für Sicherungs*](vssgloss-s.md) -und [*logische Pfade*](vssgloss-l.md) (siehe [Arbeiten mit selectbarkeit und logischen Pfaden](working-with-selectability-and-logical-paths.md)) kann ein Anforderer die Komponenten Struktur des Sicherungs Vorgangs ermitteln, der wieder hergestellt werden soll.

Wenn die Komponenten Struktur der Sicherung hergestellt ist, kann der Anforderer die [*Datei Satz*](vssgloss-f.md) Informationen jeder Komponente (Datei Angabe, Pfad und Rekursions Flag) erhalten. Ein Anforderer kann dann einen Wiederherstellungs Satz generieren.

Dateien, die [*partielle Dateien*](vssgloss-p.md)oder [*gesteuerte Ziele*](vssgloss-d.md) erfordern, bieten ihre eigenen detaillierten Wiederherstellungs Anweisungen (siehe [nicht standardmäßige Sicherungs-und Wiederherstellungs](non-default-backup-and-restore-locations.md)Pfade), die dem Wiederherstellungs Satz hinzugefügt werden können.

Ein typischer Mechanismus zum Erstellen eines Wiederherstellungs Satzes für Dateien, die nicht an Teil Dateien Vorgängen beteiligt sind, oder an [*gesteuerte Ziele*](vssgloss-d.md) kann wie folgt fortgesetzt werden:

1.  Rufen Sie eine Liste der Dateien auf dem Sicherungsmedium ab, einschließlich ihrer ursprünglichen Pfade.

2.  Identifizieren Sie die [*Writer-Klasse*](vssgloss-w.md) und die-Komponente für jede Datei auf dem Sicherungsmedium, indem Sie die folgenden Schritte ausführen:

    -   Rufen Sie für jeden Writer Komponenten Informationen ([**ivsswmcomponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent)) ab, indem Sie [**ivssexaminebeschreitermetadata:: getComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getcomponent) für alle zugehörigen Komponenten aufrufen.
    -   Rufen Sie für jede Komponente Dateideskriptoren ([**ivsswmfiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc)) für jede Gruppe von Dateien ab, die die Komponente enthält (abhängig von den Datentypen, die die Komponente enthält, indem Sie [**ivsswmcomponent:: GetFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getfile), [**ivsswmcomponent:: getdatabasefile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabasefile)und [**ivsswmcomponent:: getdatabaselogfile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabaselogfile)aufrufen.
    -   Vergleichen Sie den Namen und die Pfadinformationen der Datei mit der, die von den im Dateideskriptor enthaltenen Pfadinformationen für jeden Satz von Dateien in einer Komponente zurückgegeben wird (von [**ivsswmfiledesc**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getpath)zurückgegeben:). GetPath, [**ivsswmfiledesc:: GetFileSpec**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getfilespec)und [**ivsswmfiledesc:: getrecursive**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getrecursive)) für gespeicherte Datei Pfadinformationen, um zu bestimmen, ob die Datei Teil der Komponente ist.
        > [!Note]  
        > Sie sollten alle alternativen Speicherort Informationen im Dateideskriptor ignorieren, die von einer Komponente abgerufen wurden, die in einem gespeicherten Writer-Metadatendokument gefunden wurde (das heißt, [**ivsswmfiledesc:: getalternateloationgibt**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) nicht **null** zurück). Bei diesem alternativen Speicherort handelt es sich um den [*alternativen Pfad*](vssgloss-a.md), der nur während der Sicherung verwendet wird.

         

3.  Abrufen alternativer Mapping-Informationen für jede Datei auf dem Sicherungsmedium:

    -   Alternative Dateizuordnungen werden auf dem Writer gespeichert, nicht auf der Komponentenebene. Sie werden vom Objekt [**ivsswmfiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) abgerufen, das von [**ivssexamineschreibmetadata:: getalternatelocationmapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping)zurückgegeben wurde.
    -   Sie können feststellen, ob eine bestimmte Datei über eine Alternative Speicherort Zuordnung verfügt, indem Sie den Pfad und den Namen der Datei mit dem Pfad und der Datei Spezifikation überprüfen, die in der von ivssexaminescriptermetadata zurückgegebenen Zuordnung des alternativen Speicher Orts enthalten sind [**getalternatelocationmapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping), über [**ivsswmfiledebug:: getpath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getpath), [**ivsswmfiledebug:: GetFileSpec**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getfilespec)und [**ivsswmfiledebug:: getrecursive**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getrecursive). (Wenn während der Sicherung ein alternativer Pfad verwendet wurde, sollten diese Informationen während der Überprüfung bei der Verarbeitung einer Wiederherstellung ignoriert werden.)
    -   Wenn die Dateideskriptoren für eine Datei und Alternative Speicherort Zuordnungen übereinstimmen, verwenden Sie die [**ivsswmfiledesc:: getalternateloation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) -Methode des [**ivsswmfiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) -Objekts, das von [**ivssexaminebeschreib termetadata:: getalternatelocationmapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping) zurückgegeben wird, um den alternativen Speicherort zu ermitteln
    -   Die Alternative Speicherort Zuordnung, die auf diese Weise abgerufen wird, stimmt nicht notwendigerweise mit der überein, die vom Dokument mit den Sicherungs Komponenten von [**IVssComponent:: getalternatelocationmapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmapping)zurückgegeben wurde. Der [**ivsswmfiledesc:: getalternateloationwert**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) ist nur dann nicht leer, wenn die Alternative Speicherort Zuordnung für eine Datei verwendet wird.

4.  Mit dieser Datei und diesen Komponenten Informationen kann das Dokument "Sicherungs Komponenten" abgefragt werden, um Informationen zu Wiederherstellungs Zielen, Optionen und neuen Wiederherstellungs Speicherorten für jede Datei abzurufen. Diese Informationen können mit der Liste der Dateien, Komponenten und alternativen Speicherorte kombiniert werden.

5.  Dateien, die nicht durch Writer geschützt sind, können in Übereinstimmung mit herkömmlichen Wiederherstellungs Vorgängen ausgewählt werden.

An diesem Punkt sollte eine anfordernde Person über eine Liste aller Dateien verfügen, die für die Wiederherstellung erforderlich sind, sowie Anweisungen zum Wiederherstellen der Dateien. Außerdem können Sie mit der Wiederherstellung von Dateien beginnen:

-   Ob alternative Speicherort Zuordnungen oder der ursprüngliche Datei Speicherort als Ziel für die Wiederherstellung verwendet werden soll, hängt davon ab, ob eine Datei am Ziel Speicherort vorhanden ist und ob eine Datei am Ziel Speicherort und die Komponenten Einstellungen des [**VSS- \_ Wiederherstellungs \_ Ziels**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restore_target) und der [**VSS \_ restoremethod- \_ enum**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) (siehe [nicht standardmäßige Sicherungs-und Wiederherstellungs Speicherorte](non-default-backup-and-restore-locations.md))
-   Ob der Wiederherstellungs Versuch erfolgreich ist, hängt von Problemen wie den Zugriffsberechtigungen des Ziels, von der Sperrung der Zieldateien und von anderen konventionellen Problemen bei der Dateiwiederherstellung ab.
-   Der Erfolg oder das Fehlschlagen der Wiederherstellung einer bestimmten Komponente für eine bestimmte Writer-Instanz sollte im Dokument mit den Sicherungs Komponenten durch Aufrufen von [**IVssBackupComponents:: setfilerestorestatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setfilerestorestatus)beibehalten werden. Dadurch können die Informationen für Writer zugänglich gemacht werden, wenn Sie das postrestore-Ereignis verarbeiten.
-   Wenn eine Datei an einer alternativen Speicherort Zuordnung wieder hergestellt wird, muss der Anforderer [**IVssBackupComponents:: addalternativelocationmapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addalternativelocationmapping)aufruft. Dadurch können Writer ermitteln, ob Ihre Dateien an anderen Speicherorten über [**IVssComponent:: getalternatelocationmapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmapping)wieder hergestellt wurden.
-   Anforderer ist möglicherweise wünschenswert, Dateien an vollständig neuen Speicherorten wiederherzustellen. Dies ist akzeptabel, aber der Anforderer muss den Writer mithilfe der [**IVssBackupComponents:: addnewtarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget) -Methode angeben.

 

 



