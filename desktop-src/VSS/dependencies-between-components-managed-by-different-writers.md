---
description: Es gibt Situationen, in denen Daten von einem Writer von Daten abhängig sind, die von einem anderen Writer verwaltet werden. In diesen Fällen sollten Sie Daten von beiden Writern sichern oder wiederherstellen.
ms.assetid: 0413c289-74b7-4e83-a227-00bfb264e56e
title: Abhängigkeiten zwischen Komponenten, die von verschiedenen Writern verwaltet werden
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82d50e88e13899951802b2ec3aa0bd9e651c16928b9f57409329035a28cfa1ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118122154"
---
# <a name="dependencies-between-components-managed-by-different-writers"></a>Abhängigkeiten zwischen Komponenten, die von verschiedenen Writern verwaltet werden

Es gibt Situationen, in denen Daten von einem Writer von Daten abhängig sind, die von einem anderen Writer verwaltet werden. In diesen Fällen sollten Sie Daten von beiden Writern sichern oder wiederherstellen.

VSS behandelt dieses Problem mithilfe einer expliziten Writer-Komponenten-Abhängigkeit und der [**IVssWMDependency-Schnittstelle.**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmdependency)

Ein Writer fügt beim Erstellen des Writer-Metadatendokuments mithilfe der [**IVssCreateWriterMetadata::AddComponentDependency-Methode**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponentdependency) eine oder mehrere Abhängigkeiten hinzu. Der Writer übergibt der Methode den Namen und logischen Pfad der abhängigen Komponente [](vssgloss-w.md) (die sie verwaltet) sowie den Namen und logischen Pfad sowie die Writerklassen-ID (die GUID, die die Klasse identifiziert) der Komponente, von der sie abhängt.

Nach dem Erstellen informiert diese Abhängigkeit den Anfordernden darüber, dass bei jedem Sicherungs- oder Wiederherstellungsvorgang sowohl die abhängige Komponente als auch die Ziele ihrer Abhängigkeiten beteiligt sein müssen.

Eine bestimmte Komponente kann mehrere Abhängigkeiten aufweisen, was erfordert, dass sie und alle ihre abhängigen Ziele gemeinsam an der Sicherung und Wiederherstellung beteiligt sind.

Die abhängige Komponente und/oder die Ziele ihrer Abhängigkeiten können entweder explizit oder implizit [*in*](vssgloss-i.md) Sicherungs- oder Wiederherstellungsvorgänge eingeschlossen werden. [](vssgloss-e.md)

Der Abhängigkeitsmechanismus für explizite Writerkomponenten sollte nicht verwendet werden, um eine Abhängigkeit zwischen zwei Komponenten für denselben Writer zu erstellen. Die Auswahlregeln können die gleiche Funktionalität effizienter bereitstellen, ohne das Risiko von zirkulären Abhängigkeiten zu vermeiden.

Beispielsweise kann [**IVssCreateWriterMetadata::AddComponentDependency**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponentdependency) verwendet werden, um die Abhängigkeit der Komponente writerData (mit dem logischen Pfad "") des Writers MyWriter in der Komponente internetData (mit dem logischen Pfad "Connections") eines Writers namens InternetConnector mit einer Writer-Klassen-ID X zu definieren. (Es ist zwar möglich, dass mehrere Writer mit derselben Klassen-ID gleichzeitig im System sind, verwirrung wird jedoch vermieden, da die Kombination aus logischem Pfad und Komponentenname im System unter VSS eindeutig ist.)

Ein Writer fügt einer bestimmten Komponente mehrere Abhängigkeiten hinzu, indem er [**einfach IVssCreateWriterMetadata::AddComponentDependency**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponentdependency) aufruft, die mit verschiedenen Komponenten von verschiedenen Writern wiederholt wird. Die Anzahl der anderen Komponenten, von der eine bestimmte Komponente abhängt, können Sie durch Untersuchen des **cDependencies-Members** der [**VSS \_ COMPONENTINFO-Struktur**](/windows/desktop/api/VsBackup/ns-vsbackup-vss_componentinfo) finden.

Ein Writer oder an anfordernde Benutzer ruft Instanzen der [**IVssWMDependency-Schnittstelle**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmdependency) mit [**IVssWMComponent::GetDependency ab.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdependency) Die **IVssWMDependency** gibt den Komponentennamen, den logischen Pfad und die Klassen-ID des Writer zurück, der die Komponente, die das Ziel der Abhängigkeit ist, verwalten.

Der Abhängigkeitsmechanismus schreibt keine bestimmte Reihenfolge der Präferenz zwischen der abhängigen Komponente und den Zielen ihrer Abhängigkeiten vor. Wie bereits erwähnt, deutet eine Abhängigkeit darauf hin, dass bei jedem Sichern oder Wiederherstellen einer bestimmten Komponente auch die Komponente bzw. die Komponenten, von denen sie abhängt, sicherungs- oder wiederhergestellt werden müssen. Die genaue Implementierung der Abhängigkeit liegt im Ermessen der Sicherungsanwendung.

Im obigen Fall ist beispielsweise die Komponente writerData (logischer Pfad "") von der Komponente InternetConnector (logischer Pfad "Verbindungen") abhängig. Ein An anfordernde Kann dies auf eine der folgenden Weisen interpretieren:

-   Wenn die abhängige Komponente writerData (implizit oder explizit) für die Sicherung oder Wiederherstellung ausgewählt ist, muss die anfordernde Komponente (implizit oder explizit) das Ziel der Abhängigkeit internetData auswählen.
-   Wenn das Ziel der Abhängigkeit internetData nicht für die Sicherung ausgewählt ist, sollte die abhängige Komponente writerData nicht ausgewählt werden.

Beim Entwickeln von Unterstützung für Abhängigkeiten sollten entwickler jedoch beachten, dass es keine Möglichkeit gibt, wie ein Writer bestimmen kann, ob eine seiner Komponenten ein Ziel einer Abhängigkeit ist.

## <a name="declaring-remote-dependencies"></a>Deklarieren von Remoteabhängigkeiten

Eine verteilte Anwendung ist eine Anwendung, die so konfiguriert werden kann, dass ein oder mehrere Computer gleichzeitig verwendet werden. In der Regel wird die Anwendung auf einem oder mehrere Anwendungsservercomputern ausgeführt und kommuniziert mit einem oder mehrere Datenbankservercomputern (kann aber auch nicht tatsächlich ausgeführt werden). Diese Konfiguration wird manchmal als Bereitstellung mit mehreren System bezeichnet. Häufig kann dieselbe Anwendung auch so konfiguriert werden, dass sie auf einem einzelnen Computer ausgeführt wird, auf dem sowohl ein Anwendungsserver als auch ein Datenbankserver ausgeführt wird. Eine solche Konfiguration wird als Einzelsystembereitstellung bezeichnet. In beiden Konfigurationen verfügen der Anwendungsserver und der Datenbankserver jeweils über eigene unabhängige VSS Writer.

Wenn eine vom Writer der Anwendung verwaltete Komponente in einer Bereitstellung mit mehreren System von einer Remotekomponente abhängt, die vom Writer des Datenbankservers verwaltet wird, wird dies als Remoteabhängigkeit bezeichnet. (Im Gegensatz dazu verfügt eine Einzelsystembereitstellung nur über lokale Abhängigkeiten.)

Ein Beispiel für eine Bereitstellung mit mehreren System ist ein Anwendungsserver, der einen SQL Server-Datenbankserver als Datenspeicher verwendet. Die anwendungsspezifischen Daten, einschließlich der Webparts, Webinhaltsdateien und der IIS-Metabasis, befinden sich auf einem oder mehrere Computer, die als Front-End-Webserver bezeichnet werden. Der tatsächliche SQL, der die Konfigurationsdatenbank und mehrere Inhaltsdatenbanken umfasst, befindet sich auf einem oder mehreren anderen Computern, die als Back-End-Datenbankserver bezeichnet werden. Jeder Front-End-Webserver enthält denselben anwendungsspezifischen Inhalt und dieselbe Konfiguration. Jeder Der Back-End-Datenbankserver kann alle Inhaltsdatenbanken oder die Konfigurationsdatenbank hosten. Die Anwendungssoftware wird nur auf den Front-End-Webservern ausgeführt, nicht auf den Datenbankservern. In dieser Konfiguration verfügt der VSS Writer der Anwendung über Remoteabhängigkeiten von den Komponenten, die vom SQL werden.

Ein Writer kann eine Remoteabhängigkeit deklarieren, indem er die [**AddComponentDependency-Methode**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponentdependency) aufruft, wobei "RemoteComputerName", wobei RemoteComputerName der Name des Computers ist, auf dem sich die Remotekomponente befindet, dem logischen Pfad im \\ \\  \\ *wszOnLogicalPath-Parameter* voraussetzt.  Der Wert von *RemoteComputerName kann* eine IP-Adresse oder ein Computername sein, der von der [**GetComputerNameEx-Funktion zurückgegeben**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) wird.

**Windows Server 2003:** Ein Writer kann Remoteabhängigkeiten erst deklarieren, Windows Server 2003 mit Service Pack 1 (SP1) installiert wurde.

Um eine Abhängigkeit zu identifizieren, ruft eine anfordernde Person die [**Methoden GetWriterId,**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmdependency-getwriterid) [**GetLogicalPath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getlogicalpath)und [**GetComponentName**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmdependency-getcomponentname) der [**IVssWMDependency-Schnittstelle**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmdependency) auf. Der Anfordernde muss den Komponentennamen untersuchen, den **GetComponentName** im *parameter pbstrComponentName zurückgibt.* Wenn der Komponentenname mit " " beginnt, muss der Anfordernde davon ausgehen, dass er eine Remoteabhängigkeit angibt und dass die erste Komponente nach " " der RemoteComputerName ist, der angegeben wurde, als der Writer \\ \\ \\ \\ [**AddComponentDependency aufgerufen hat.**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponentdependency)  Wenn der Komponentenname nicht mit " " beginnt, sollte der Anfordernde davon ausgehen, dass \\ \\ er eine lokale Abhängigkeit angibt.

Wenn eine Remoteabhängigkeit besteht, muss die anfordernde Komponente beim Sichern der lokalen Komponente sichern. Um die Remotekomponente zu sichern, muss der Anfordernde über einen Agent auf dem Remotecomputer verfügen und die Sicherung auf dem Remotecomputer initiieren.

## <a name="structuring-remote-dependencies"></a>Strukturieren von Remoteabhängigkeiten

Es ist wichtig zu verstehen, dass eine Abhängigkeit keine Komponente an sich selbst ist. Eine Komponente ist erforderlich, um die Abhängigkeit zu halten.

In den folgenden Beispielen werden zwei Möglichkeiten zum Strukturieren einer Reihe von Abhängigkeiten gezeigt.

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

In Beispiel 1 werden die Abhängigkeiten von Komponente A gehalten. Da nur Komponenten ausgewählt werden können, nicht einzelne Dateien, würde die Strukturierung der Abhängigkeiten von Komponente A auf diese Weise erfordern, dass die gesamte Komponente, sowohl die Dateien als auch die Abhängigkeiten, immer zusammen sichern und wiederhergestellt werden müssen. Sie können nicht einzeln sicherungs- oder wiederhergestellt werden.

In Beispiel 2 enthalten separate Komponenten (Komponenten A und B) jede der Abhängigkeiten. In diesem Fall können die beiden Komponenten unabhängig voneinander ausgewählt und daher unabhängig voneinander sicherungs- und wiederhergestellt werden. Die Strukturierung der Abhängigkeiten auf diese Weise bietet einer verteilten Anwendung viel mehr Flexibilität bei der Verwaltung ihrer Remoteabhängigkeiten.

## <a name="supporting-remote-dependencies"></a>Unterstützen von Remoteabhängigkeiten

Ein Anfordernde kann vollständige oder partielle Unterstützung für Remoteabhängigkeiten bereitstellen.

Um vollständigen Support zu bieten, sollte der Anfordernde folgende Schritte zur Sicherungs- und Wiederherstellungszeit durchführen.

Zur Sicherungszeit muss der Anfordernde die Sicherung auf dem (lokalen) Front-End-Computer starten, die abhängigkeiten ermitteln, die vorhanden sind, und zusätzliche Sicherungsaufträge spoolen, um die Back-End-Datenbanken zu erfassen. Der Anfordernde muss warten, bis die Back-End-Sicherungsaufträge auf dem Remotecomputer abgeschlossen sind, bevor er die [**Methoden IVssBackupComponents::SetBackupSucceeded und**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded) [**IVssBackupComponents::BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) aufruft. Wenn der Anfordernde wartet, bis die Sicherung der Back-End-Komponenten abgeschlossen ist, bevor **BackupComplete** aufruft, erzeugt dies eine einfacher wiederherstellbare Sicherung für einen Writer, der zusätzliche Verbesserungen implementiert, z. B. topologiebasierte Sperren, während der Sicherung. Im folgenden Verfahren wird beschrieben, was der Anfordernde tun sollte:

1.  Auf dem lokalen Computer ruft die Anfordernde die [**Methoden IVssBackupComponents::InitializeForBackup,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforbackup) [**IVssBackupComponents::GatherWriterMetadata,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) [**IVssBackupComponents::P repareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup)und [**IVssBackupComponents::D oSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) auf.
2.  Nachdem die lokale Schattenkopie abgeschlossen ist, aber bevor die Sicherung abgeschlossen ist, spoolt der Anfordernde zusätzliche Sicherungsaufträge, indem er eine Anforderung an den Agent auf dem Remotecomputer sendet.
3.  Auf dem Remotecomputer führt der Agent des Anfordernden die gepoolte Sicherungssequenz aus, indem er [**InitializeForBackup,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforbackup) [**GatherWriterMetadata,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) [**PrepareForBackup,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) [**DoSnapshotSet,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) [**SetBackupSucceeded**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded)und [**BackupComplete aufruft.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete)
4.  Wenn der Agent des Anfordernden die in einem Pool gespeicherten Aufträge auf dem Remotecomputer abgeschlossen hat, schließt der Anfordernde die Sicherungssequenz ab, indem er [**SetBackupSucceeded und**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded) [**BackupComplete aufruft.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete)

Zur Wiederherstellungszeit muss der Anfordernde die Wiederherstellung mit dem (lokalen) Front-End-Computer starten, die wiederherzustellenden Komponenten und ihre Abhängigkeiten auswählen und dann das [**PreRestore-Ereignis**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) senden, indem er die **IVssBackupComponents::P reRestore-Methode** aufruft. Der Anfordernde sollte dann die Back-End-Wiederherstellungsaufträge auf dem Remotecomputer spoolen und die [**IVssBackupComponents::P ostRestore-Methode**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore) aufrufen, wenn die Back-End-Wiederherstellungen abgeschlossen sind. Diese Anforderung bietet dem Front-End-Writer mehr Kontrolle über die Wiederherstellungserfahrung und eine insgesamt bessere Benutzererfahrung für Administratoren. Da die Sicherungen in den einzelnen Systemen nicht zum gleichen Zeitpunkt erfolgen, muss der Front-End-Writer eine Bereinigung der Back-End-Daten durchführen. In der beispielbasierten Anwendung, die im vorherigen "Deklarieren von Remoteabhängigkeiten" erläutert wurde, sollte der Writer eine Standortumstellung oder Neuindizierung initiieren, nachdem eine Wiederherstellung einer der Back-End-Datenbanken abgeschlossen wurde. Zu diesem Zweck muss der Writer Ereignisse auf dem Front-End-Server empfangen. Im folgenden Verfahren wird beschrieben, was der Anfordernde tun sollte:

1.  Auf dem lokalen Computer ruft die Anfordernde [**IVssBackupComponents::InitializeForRestore,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforrestore) [**GatherWriterMetadata,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) [**IVssBackupComponents::SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore) (oder [**IVssBackupComponentsEx::SetSelectedForRestoreEx)**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex-setselectedforrestoreex)und [**PreRestore auf.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore)
2.  Nachdem die [**PreRestore-Phase**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) abgeschlossen ist, aber bevor die [**PostRestore-Phase**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore) beginnt, spoolt der Anfordernde zusätzliche Wiederherstellungsaufträge, indem er eine Anforderung an seinen Agent auf dem Remotecomputer sendet.
3.  Auf dem Remotecomputer führt der Agent des Anfordernden die gepoolten Wiederherstellungsaufträge aus, indem er [**InitializeForRestore,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforrestore) [**GatherWriterMetadata,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) [**SetSelectedForRestore,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore) [**PreRestore,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) [**SetFileRestoreStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setfilerestorestatus) (oder [**SetSelectedForRestoreEx)**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex-setselectedforrestoreex)und [**PostRestore aufruft.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore)
4.  Wenn der Agent des Anfordernden die in einem Pool gespeicherten Aufträge auf dem Remotecomputer abgeschlossen hat, schließt der Anfordernde die Wiederherstellungssequenz ab, indem er [**IVssBackupComponents::SetFileRestoreStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setfilerestorestatus) und [**PostRestore aufruft.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore)

Um Teilunterstützung für Remoteabhängigkeiten zu bieten, muss der Anfordernde Remoteabhängigkeiten befolgen und diese als Teil der Sicherung enthalten, aber die Reihenfolge der Ereignisse auf Front-End- und Back-End-Systemen, wie in den vorherigen beiden Verfahren angegeben, wäre nicht erforderlich. Für einen Anfordernden, der nur teilweise Unterstützung implementiert, sollte der Anfordernde die Sicherungs-/Wiederherstellungsdokumentation der Writeranwendung lesen, um zu verstehen, welche Szenarien unterstützt werden können.

 

 
