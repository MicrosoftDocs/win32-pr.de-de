---
description: Es gibt Situationen, in denen Daten von einem Writer von Daten abhängen, die von einem anderen Writer verwaltet werden. In diesen Fällen sollten Sie Daten von beiden Writern sichern oder wiederherstellen.
ms.assetid: 0413c289-74b7-4e83-a227-00bfb264e56e
title: Abhängigkeiten zwischen Komponenten, die von unterschiedlichen Writern verwaltet werden
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91ba3be6a2c2f0a722c4c5f06ca95351e004e1cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349269"
---
# <a name="dependencies-between-components-managed-by-different-writers"></a>Abhängigkeiten zwischen Komponenten, die von unterschiedlichen Writern verwaltet werden

Es gibt Situationen, in denen Daten von einem Writer von Daten abhängen, die von einem anderen Writer verwaltet werden. In diesen Fällen sollten Sie Daten von beiden Writern sichern oder wiederherstellen.

VSS behandelt dieses Problem durch das Konzept einer expliziten Writer-Component-Abhängigkeit und der [**ivsswmabhängigkeits**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmdependency) -Schnittstelle.

Ein Writer Fügt beim Erstellen des Writer-Metadatendokuments mithilfe der [**ivsskreateschreitermetadata:: AddComponentDependency**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponentdependency) -Methode eine oder mehrere Abhängigkeiten hinzu. Der Writer übergibt der Methode den Namen und den logischen Pfad der abhängigen Komponente (die er verwaltet) sowie den Namen und den logischen Pfad sowie die Writer- [*Klassen-ID*](vssgloss-w.md) (die GUID, die die Klasse identifiziert) der Komponente, von der er abhängt.

Nach der Einrichtung informiert diese Abhängigkeit die Anforderer darüber, dass während eines Sicherungs-oder Wiederherstellungs Vorgangs sowohl die abhängige Komponente als auch die Ziele ihrer Abhängigkeiten teilnehmen müssen.

Eine bestimmte Komponente kann mehrere Abhängigkeiten aufweisen. Dies erfordert, dass Sie und alle abhängigen Ziele an der Sicherung und Wiederherstellung beteiligt sind.

Die abhängige Komponente und/oder die Ziel (n) ihrer Abhängigkeiten können entweder [*explizit*](vssgloss-e.md) oder [*implizit*](vssgloss-i.md) in einem Sicherungs-oder Wiederherstellungs Vorgang eingeschlossen werden.

Der explizite Writer-Komponenten Abhängigkeits Mechanismus sollte nicht verwendet werden, um eine Abhängigkeit zwischen zwei Komponenten auf demselben Writer zu erstellen. Die Auswahlregeln können die gleichen Funktionen effizienter und ohne das Risiko von zirkulären Abhängigkeiten bereitstellen.

Beispielsweise könnte [**ivssupateschreitermetadata:: AddComponentDependency**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponentdependency) verwendet werden, um die Abhängigkeit der Komponente "Write Data" (mit dem logischen Pfad "") des Writers "myWriter" in der Komponente "internetdata" (mit dem logischen Pfad "Connections") eines Writers namens "Internetconnector" mit der Writer-Klassen-ID X zu definieren. (obwohl es möglich ist, dass mehrere Writer mit derselben Klassen-ID gleichzeitig auf dem System ausgeführt werden, wird die Verwirrung vermieden, da die Kombination aus logischem Pfad und Komponenten Name auf dem System unter VSS eindeutig ist.)

Ein Writer fügt eine bestimmte Komponente durch Aufrufen von [**ivsscreatewritermetadata:: AddComponentDependency**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponentdependency) , die mit verschiedenen Komponenten von unterschiedlichen Writern wiederholt wird, mehrere Abhängigkeiten hinzu. Die Anzahl anderer Komponenten, von denen eine bestimmte Komponente abhängt, finden Sie unter Untersuchen des **cdependen-** Members der [**VSS \_ ComponentInfo**](/windows/desktop/api/VsBackup/ns-vsbackup-vss_componentinfo) -Struktur.

Ein Writer oder eine Anforderer Ruft Instanzen der [**ivsswmdepencenschnittstelle**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmdependency) mit [**ivsswmcomponent:: getabhängigkeiten**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdependency)ab. **Ivsswmdepend** gibt den Komponentennamen, den logischen Pfad und die Klassen-ID des Writers zurück, der die Komponente verwaltet, die das Ziel der Abhängigkeit ist.

Der Abhängigkeits Mechanismus schreibt keine bestimmte bevorzugte Reihenfolge zwischen der abhängigen Komponente und den Zielen ihrer Abhängigkeiten vor. Wie bereits erwähnt, müssen alle Abhängigkeiten darauf hindeuten, dass die Komponente oder Komponenten, von denen Sie abhängig ist, ebenfalls gesichert oder wieder hergestellt werden muss, wenn eine bestimmte Komponente gesichert oder wieder hergestellt wird. Die genaue Implementierung der Abhängigkeit liegt im Ermessen der Sicherungs Anwendung.

Im obigen Fall ist beispielsweise die Komponente "Write Data" (logischer Pfad "") von der Komponente Internetconnector (logischer Pfad "Connections") abhängig. Ein Anforderer kann dies auf eine der folgenden Arten interpretieren:

-   Wenn die abhängige Komponente "Write Data" (implizit oder explizit) für die Sicherung oder Wiederherstellung ausgewählt wird, muss der Anforderer (entweder implizit oder explizit) das Ziel seiner Abhängigkeit (internetdata) auswählen.
-   Wenn das Ziel seiner Abhängigkeit, internetdata, nicht für die Sicherung ausgewählt ist, sollte die abhängige Komponente "Write Data" nicht ausgewählt werden.

Wenn jedoch die Unterstützung für Abhängigkeiten entwickelt wird, sollten sich Entwickler von Anforderer bewusst sein, dass es keine Möglichkeit gibt, dass ein Writer feststellen kann, ob eine seiner Komponenten ein Ziel einer Abhängigkeit ist.

## <a name="declaring-remote-dependencies"></a>Deklarieren von Remote Abhängigkeiten

Eine verteilte Anwendung ist eine Anwendung, die so konfiguriert werden kann, dass ein oder mehrere Computer gleichzeitig verwendet werden. In der Regel wird die Anwendung auf einem oder mehreren Anwendungsserver Computern ausgeführt, und es wird eine Verbindung mit einem oder mehreren Datenbankserver Computern hergestellt (die aber möglicherweise tatsächlich auf diesem ausgeführt wird). Diese Konfiguration wird manchmal als Bereitstellung mit mehreren Systemen bezeichnet. Häufig kann dieselbe Anwendung auch für die Ausführung auf einem einzelnen Computer konfiguriert werden, auf dem ein Anwendungsserver und ein Datenbankserver ausgeführt werden. Eine solche Konfiguration wird als Bereitstellung mit nur einem System bezeichnet. In beiden Konfigurationen verfügen Anwendungsserver und Datenbankserver jeweils über eigene unabhängige VSS-Writer.

Wenn in einer Bereitstellung mit mehreren Systemen eine Komponente, die vom Writer der Anwendung verwaltet wird, von einer Remote Komponente abhängig ist, die vom Writer des Datenbankservers verwaltet wird, wird dies als Remote Abhängigkeit bezeichnet. (Eine Bereitstellung mit einem einzelnen System hat dagegen nur lokale Abhängigkeiten.)

Als Beispiel für eine Bereitstellung mit mehreren Systemen sollten Sie einen Anwendungsserver in Erwägung nehmen, der einen SQL Server Datenbankserver als Datenspeicher verwendet. Die anwendungsspezifischen Daten, die die Webparts, die Webinhalts Dateien und die IIS-Metabase enthalten, befinden sich auf einem oder mehreren Computern, die als Front-End-Webserver bezeichnet werden. Der tatsächliche SQL-Datenspeicher, der die Konfigurations Datenbank und mehrere Inhalts Datenbanken umfasst, befindet sich auf einem oder mehreren anderen Computern, die als Back-End-Datenbankserver bezeichnet werden. Alle Front-End-Webserver enthalten denselben anwendungsspezifischen Inhalt und dieselbe Konfiguration. Alle Back-End-Datenbankserver können beliebige Inhalts Datenbanken oder die Konfigurations Datenbank hosten. Die Anwendungssoftware wird nur auf den Front-End-Webservern ausgeführt, nicht auf den Datenbankservern. In dieser Konfiguration hat der VSS Writer der Anwendung Remote Abhängigkeiten von den Komponenten, die vom SQL Writer verwaltet werden.

Ein Writer kann eine Remote Abhängigkeit deklarieren, indem die [**AddComponentDependency**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponentdependency) -Methode aufgerufen wird, der " \\ \\ *Remotecomputername*" vorangestellt ist \\ , wobei " *Remotecomputername* " der Name des Computers ist, auf dem sich die Remote Komponente befindet, und der logische Pfad im *wszonlogicalpath* -Parameter. Der Wert von *Remotecomputername* kann eine IP-Adresse oder ein Computername sein, der von der [**GetComputerNameEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) -Funktion zurückgegeben wird.

**Windows Server 2003:** Ein Writer kann bis Windows Server 2003 mit Service Pack 1 (SP1) keine Remote Abhängigkeiten deklarieren.

Zum Identifizieren einer Abhängigkeit Ruft eine Anforderer die Methoden [**getschreiterid**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmdependency-getwriterid), [**getlogicalpath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getlogicalpath)und [**GetComponentName**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmdependency-getcomponentname) der [**ivsswmdepen-Schnitt**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmdependency) Stelle auf. Der Anforderer muss den Komponentennamen untersuchen, den **GetComponentName** im *pbstrincomponentname* -Parameter zurückgibt. Wenn der Komponenten Name mit " \\ \\ " beginnt, muss der Anforderer davon ausgehen, dass er eine Remote Abhängigkeit angibt und dass die erste Komponente, die auf "" folgt, \\ \\ der Remote *Computername* ist, der beim Aufrufen von [**AddComponentDependency**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponentdependency)angegeben wurde. Wenn der Komponenten Name nicht mit "" beginnt \\ \\ , sollte der Anforderer davon ausgehen, dass er eine lokale Abhängigkeit angibt.

Wenn eine Remote Abhängigkeit vorhanden ist, muss der Anforderer die Remote Komponente sichern, wenn er die lokale Komponente sichert. Zum Sichern der Remote Komponente sollte der Anforderer über einen Agent auf dem Remote Computer verfügen und die Sicherung auf dem Remote Computer initiieren.

## <a name="structuring-remote-dependencies"></a>Strukturieren von Remote Abhängigkeiten

Es ist wichtig zu verstehen, dass eine Abhängigkeit keine Komponente in und von sich selbst ist. Eine Komponente ist erforderlich, um die Abhängigkeit zu speichern.

Die folgenden Beispiele zeigen zwei Möglichkeiten, einen Satz von Abhängigkeiten zu strukturieren.

``` syntax
Example 1:
    Writer 1
        Component A
            File A
            File B
            Dependency (SQL/MSDE Writer, Component X, "\")
            Dependency (SQL/MSDE Writer, Component Y, "\")

Example 2:
    Writer 2
        Component A
            File A
            File B
        Component B
            Dependency (SQL/MSDE Writer, Component X, "\")
            Dependency (SQL/MSDE Writer, Component Y, "\")
```

In Beispiel 1 werden die Abhängigkeiten von Komponente A gespeichert. Da nur Komponenten ausgewählt werden können, nicht einzelne Dateien, müssen die Abhängigkeiten von Component A auf diese Weise so strukturiert werden, dass die gesamte Komponente, sowohl die Dateien als auch die Abhängigkeiten, immer gleich gesichert und wieder hergestellt werden müssen. Sie können nicht einzeln gesichert oder wieder hergestellt werden.

In Beispiel 2 enthalten separate Komponenten (Komponenten A und B) jede der Abhängigkeiten. In diesem Fall können die beiden Komponenten unabhängig voneinander ausgewählt und daher unabhängig voneinander gesichert und wieder hergestellt werden. Wenn Sie die Abhängigkeiten auf diese Weise strukturieren, wird eine verteilte Anwendung viel flexibler bei der Verwaltung Ihrer Remote Abhängigkeiten.

## <a name="supporting-remote-dependencies"></a>Unterstützen von Remote Abhängigkeiten

Ein Anforderer kann vollständige oder partielle Unterstützung für Remote Abhängigkeiten bereitstellen.

Um vollständige Unterstützung zu bieten, sollte der Anforderer zum Zeitpunkt der Sicherung und Wiederherstellung Folgendes ausführen.

Zum Zeitpunkt der Sicherung muss der Anforderer die Sicherung auf dem Front-End-Computer (lokal) starten, die vorhandenen Abhängigkeiten ermitteln und zusätzliche Sicherungsaufträge für die Erfassung der Back-End-Datenbanken erstellen. Der Anforderer muss warten, bis die Back-End-Sicherungsaufträge auf dem Remote Computer abgeschlossen sind, bevor die [**IVssBackupComponents:: setbackupcomplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded) -und [**IVssBackupComponents:: BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) -Methode aufgerufen werden. Wenn die anfordernde Person wartet, bis die Sicherung der Back-End-Komponenten abgeschlossen ist, bevor **BackupComplete** aufgerufen wird, führt dies zu einer leichter BEHEB baren Sicherung für einen Writer, der zusätzliche Verbesserungen implementiert – z. b. eine topologiesperre, beispielsweise – während der Sicherung. Im folgenden Verfahren wird erläutert, was der Anforderer tun sollte:

1.  Auf dem lokalen Computer ruft der Anforderer die Methoden [**IVssBackupComponents:: initializeforbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforbackup), [**IVssBackupComponents:: gatherschreitermetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata), [**IVssBackupComponents::P eneforbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup)und [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) auf.
2.  Nachdem die lokale Schatten Kopie abgeschlossen ist, aber bevor die Sicherung abgeschlossen ist, Spool der Anforderer zusätzliche Sicherungsaufträge, indem er eine Anforderung an den Agent auf dem Remote Computer sendet.
3.  Auf dem Remote Computer führt der Agent der Anforderer die gespoolte Sicherungs Sequenz durch Aufrufen von [**initializeforbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforbackup), [**gatherwrite-Metadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata), [**PrepareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup), [**DoSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset), [**setbackupwar**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded)und [**BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete)aus.
4.  Wenn der Agent der Anforderer die Spoolaufträge auf dem Remote Computer abgeschlossen hat, schließt der Anforderer die Sicherungs Sequenz ab, indem er [**setbackuperfolg**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded) und [**Backup Complete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete)aufruft.

Zum Zeitpunkt der Wiederherstellung muss der Anforderer die Wiederherstellung mit dem Front-End-Computer (lokaler Computer) starten, die Komponenten und deren Abhängigkeiten auswählen, die wieder hergestellt werden sollen, und dann das [**PreRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) -Ereignis durch Aufrufen der **IVssBackupComponents::P reitore** -Methode senden. Der Anforderer sollte dann die Back-End-Wiederherstellungs Aufträge auf dem Remote Computer spound die [**IVssBackupComponents::P ostrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore) -Methode aufruft, wenn die Back-End-Wiederherstellungen abgeschlossen sind. Durch diese Anforderung erhält der Front-End-Writer mehr Kontrolle über die Wiederherstellungs Funktion und eine bessere Administrator Benutzer Leistung. Da die Sicherungen auf den einzelnen Systemen nicht zu demselben Zeitpunkt erfolgen, muss der Front-End-Writer einen Bereinigung der Back-End-Daten ausführen. In der Beispielanwendung, die im vorherigen Abschnitt "Deklarieren von Remote Abhängigkeiten" erläutert wurde, sollte der Writer eine Neuzuordnung oder Neuindizierung initiieren, nachdem eine Wiederherstellung einer der Back-End-Datenbanken abgeschlossen wurde. Zu diesem Zweck muss der Writer Ereignisse auf dem Front-End-Server empfangen. Im folgenden Verfahren wird erläutert, was der Anforderer tun sollte:

1.  Auf dem lokalen Computer ruft der Anforderer [**IVssBackupComponents:: initializeforrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforrestore), [**gatherwrite Metadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata), [**IVssBackupComponents:: setselectedforrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore) (oder [**ivssbackupcomponentsex:: setselectedforrestoreex**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex-setselectedforrestoreex)) und [**PreRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore)auf.
2.  Nachdem die [**vorab**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) Version abgeschlossen ist, aber bevor die [**postrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore) -Phase beginnt, werden zusätzliche Wiederherstellungs Aufträge von der anfordernden Person Spool, indem eine Anforderung an den Agent auf dem Remote Computer gesendet wird.
3.  Auf dem Remote Computer führt der Agent der Anforderer die gespoolten Wiederherstellungs Aufträge durch Aufrufen von [**initializeforrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforrestore), [**gatherscriptermetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata), [**setselectedforrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore), [**PreRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore), [**setfilerestorestatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setfilerestorestatus) (oder [**setselectedforrestoreex**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex-setselectedforrestoreex)) und [**postrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore)aus.
4.  Wenn der Agent der Anforderer die Spoolaufträge auf dem Remote Computer abgeschlossen hat, schließt der Anforderer die Wiederherstellungs Sequenz ab, indem [**IVssBackupComponents:: setfilerestorestatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setfilerestorestatus) und [**postrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore)aufgerufen werden.

Um eine partielle Unterstützung für Remote Abhängigkeiten bereitzustellen, muss die anfordernde Person Remote Abhängigkeiten befolgen und Sie als Teil der Sicherung einschließen, aber die Reihenfolge von Ereignissen auf Front-End-und Back-End-Systemen, wie in den vorherigen beiden Verfahren erläutert, wäre nicht erforderlich. Für einen Anforderer, der nur partielle Unterstützung implementiert, sollte der Anforderer die Sicherungs-/Wiederherstellungs Dokumentation der Writer-Anwendung entnehmen, um zu verstehen, welche Szenarien unterstützt werden können.

 

 
