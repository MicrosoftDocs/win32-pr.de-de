---
description: Komponenten werden von definiert und von Writern in Ihrem Writer-Metadatendokument als Reaktion auf ein identifizierungsereignis zu Beginn eines Sicherungs Vorgangs instanziiert (siehe Übersicht über die Sicherungs Initialisierung), wenn das Writer-Metadatendokument aufgefüllt wird.
ms.assetid: 5e1c3f9b-ca83-4e70-963b-0a237c6f4b0d
title: Definition von Komponenten durch Writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa5383e9bc87620f23bb2a3ab067c1913a323782
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868763"
---
# <a name="definition-of-components-by-writers"></a>Definition von Komponenten durch Writer

Komponenten werden von definiert und von Writern in Ihrem Writer-Metadatendokument als Reaktion auf ein [*identifizierungsereignis*](vssgloss-i.md) zu Beginn eines Sicherungs Vorgangs instanziiert (siehe [Übersicht über die Sicherungs Initialisierung](overview-of-backup-initialization.md)), wenn das Writer-Metadatendokument aufgefüllt wird.

Wenn Sie eine Komponente im Writer-Metadatendokument mithilfe von [**ivsskreateschreitermetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata) und [**ivsskreateschreitermetadata:: addComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponent)erstellen, muss ein Writer Folgendes angeben:

-   Gibt an, ob die Komponente [ *für die Sicherung ausgewählt* werden kann](vssgloss-s.md)
-   Komponententyp
-   Ein Komponenten Name (der nicht nur innerhalb einer bestimmten [*Writer-Instanz*](vssgloss-w.md) , sondern über alle Writer-Instanzen hinweg eindeutig sein muss)
-   Gibt an, ob der Komponente Writer-spezifische Metadaten zugeordnet sind.
-   Gibt an, ob der Writer nach einer erfolgreichen Sicherung eine Benachrichtigung erfordert

Writer können optional Folgendes angeben:

-   Der [*logische Pfad*](vssgloss-l.md) einer Komponente (der nicht nur innerhalb einer bestimmten Writer-Instanz, sondern über alle Writer-Instanzen hinweg eindeutig sein muss)
-   Eine Komponenten Beschreibung (oder Beschriftung)
-   Ein Symbol, das mit GUIs verwendet werden soll, um die Komponente anzugeben.

Es ist nicht erforderlich, dass eine Komponente tatsächlich Dateien enthält. Diese Art von leerer oder "Dummy"-Komponente kann beim Organisieren von-Komponenten nützlich sein. Eine solche Komponente kann verwendet werden, um einen [*Komponenten Satz*](vssgloss-c.md) und eine Writer-Komponente zu definieren (siehe [logische Komponente von Komponenten](logical-pathing-of-components.md)).

## <a name="setting-up-component-organization"></a>Einrichten der Komponenten Organisation

Das Festlegen der [*selekabilität*](vssgloss-s.md) einer Komponente (deren [*selekabilität für die Sicherung*](vssgloss-s.md)und deren [*selektionsfähigkeit für die Wiederherstellung*](/windows)) und der zugehörigen [*logischen Pfade*](vssgloss-l.md) ermöglicht es einem Writer, bestimmte Komponenten in einem Sicherungs-oder Wiederherstellungs Vorgang zu beauftragen oder optional zu gestalten und Komponenten in [*Komponenten*](vssgloss-c.md) Gruppen zu gruppieren. Dabei fungiert eine auswählbare Komponente, die als Einstiegspunkt für die gesamte Gruppe fungiert.

Die Mitgliedschaft in diesen Gruppierungen bestimmt, welche Komponenten während Sicherungs-und Wiederherstellungs Vorgängen verwendet werden. Wenn Sie "wählbar" verwenden, um für den Sicherungs Vorgang eine auswählbare Sicherung durchführen und für die Wiederherstellung für den Wiederherstellungs Vorgang ausgewählt werden zu können,

-   Wenn von einem bestimmten Writer verwaltete Komponenten gesichert werden, muss eine anfordernde Person explizit alle nicht auswählbaren [*Komponenten*](vssgloss-c.md) ohne auswählbare Vorgänger in Ihrem [*logischen Pfad*](vssgloss-l.md) zum Sicherungs Komponenten Dokument [*einschließen*](vssgloss-e.md) und diese Komponenten als Gruppe sichern und wiederherstellen.
-   Ein Anforderer hat die Möglichkeit, dem Sicherungs Komponenten Dokument während der Sicherungs-und Wiederherstellungs Vorgänge explizit auswählbare Komponenten hinzuzufügen. Nachdem die Komponente hinzugefügt wurde, muss Sie gesichert oder wieder hergestellt werden.
-   Wenn eine Komponente ausgewählt werden kann, bilden die Komponente und alle zugehörigen [*unter Komponenten*](vssgloss-s.md) (wie durch logische Pfade definiert) einen Komponenten Satz, der als eine Einheit behandelt werden kann, die optional an Sicherungs-und Wiederherstellungs Vorgängen beteiligt sein kann.
-   Ein Anforderer fügt bei Sicherungs-und Wiederherstellungs Vorgängen niemals explizit eine nicht auswählbare Komponente mit auswählbaren Vorgängern, einer Unterkomponente in einem Komponenten Satz, zu seinem Sicherungs Komponenten Dokument hinzu. Diese Komponenten müssen [*implizit eingeschlossen*](/windows) werden, wenn Ihr auswählbarer Vorgänger explizit hinzugefügt wird. in diesem Fall müssen Sie gesichert oder wieder hergestellt werden (siehe [Verwendung von Komponenten durch die](use-of-components-by-the-requestor.md)anfordernde Person).
-   Eine auswählbare Komponente mit einem auswählbaren Vorgänger ist immer noch eine [*Unterkomponente*](vssgloss-s.md) (ein Member eines Komponenten Satzes) und kann implizit eingeschlossen werden, wenn der auswählbare Vorgänger explizit in den Vorgang eingeschlossen wird. In diesem Fall werden die zugehörigen Informationen nicht zum Dokument mit den Sicherungs Komponenten hinzugefügt. Wenn der auswählbare Vorgänger nicht in den Vorgang eingeschlossen ist, kann die Komponente explizit für die Einbindung in den Vorgang ausgewählt werden. in diesem Fall sind die zugehörigen Informationen im Dokument mit den Sicherungs Komponenten enthalten.
-   Eine Unterkomponente, die implizit in einer Sicherung enthalten ist, kann explizit in einen Wiederherstellungs Vorgang eingeschlossen werden, unabhängig vom Status eines auswählbaren Vorgängers, wenn Sie für die Wiederherstellung ausgewählt werden kann. Bei allen auswählbaren unter Komponenten, die während eines Wiederherstellungs Vorgangs eingeschlossen werden, müssen die zugehörigen Informationen dem Dokument mit den Sicherungs Komponenten hinzugefügt werden
-   Ein Writer, dem vor der Generierung von [*PrepareForBackup*](vssgloss-p.md) -und [*PreRestore*](vssgloss-p.md) -Ereignissen keine Komponente explizit zum Sicherungs Komponenten Dokument hinzugefügt wurde, erhält keine weiteren VSS-Ereignisse.

Weitere Informationen finden Sie unter [Arbeiten mit selekabilität und logischen Pfaden](working-with-selectability-and-logical-paths.md).

## <a name="adding-files-to-a-component"></a>Hinzufügen von Dateien zu einer Komponente

Eine Komponente enthält Dateiinformationen in Form eines [*Datei Satzes*](vssgloss-f.md) , der Folgendes enthält:

-   Ein Stammverzeichnis der Dateien in der Komponente.
-   Eine Datei Spezifikation für die Dateien in der Komponente.
-   Ein Flag, das angibt, ob die Spezifikation der Komponente rekursiv ist.

Abhängig vom Komponententyp, bei dem es sich um eine Datenbank oder eine Datei Gruppe handeln kann, und (im Fall von Datenbankkomponenten), ob es sich bei den zu ladenden Dateien um Daten-oder Protokolldateien handelt, ein Writer ruft [**ivsskreateschreitermetadata:: addfilestofilegroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup), [**ivsskreateschreitermetadata:: adddatabasefiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)oder [**ivsskreateschreitermetadata:: adddatabaselogfiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) auf, um einen Datei Satz hinzuzufügen.

Wenn Sie diese Funktionen verwenden, sollten Sie die Dateien, die dem Datei Satz hinzugefügt werden sollen, wie folgt angeben:

-   *wszpath*: Dies ist der Pfad zu dem Verzeichnis, das die Dateien enthält, die dem Datei Satz hinzugefügt werden sollen. Wenn der *bRecursive* -Parameter auf **true** festgelegt ist, gibt der *wszpath* -Parameter eine Hierarchie von Verzeichnissen an, die rekursiv durchlaufen werden sollen. alle Verzeichnisse sollten neu erstellt werden, einschließlich leerer Verzeichnisse.
-   *wszfilespec*: diese Zeichenfolge gibt die Dateien in jedem Verzeichnis an, das dem Datei Satz hinzugefügt werden soll.

Nehmen wir beispielsweise an, dass die folgende Verzeichnisstruktur vorhanden ist:

<dl> C: \\ directory1 \\File1.txt  
C: \\ directory1 \\File2.txt  
C: \\ directory1 \\ directory2 \\File1.txt  
C: \\ directory1 \\ directory2 \\File2.txt  
C: \\ directory1 \\ Directory3\\  
</dl>

Wenn der Writer "C: \\ directory1" für *wszpath*, "file1. \* " für *wszfilespec* und **true** für *bRecursive* angibt, sollte der Anforderer diese Dateien einschließen:

<dl> C: \\ directory1 \\File1.txt  
C: \\ directory1 \\ directory2 \\File1.txt  
</dl>

Wenn der Writer stattdessen "C: \\ directory1" für *wszpath*, " \* " für *wszfilespec* und **true** für *bRecursive* angibt, sollte der Anforderer diese Dateien einschließen:

<dl> C: \\ directory1 \\File1.txt  
C: \\ directory1 \\File2.txt  
C: \\ directory1 \\ directory2 \\File1.txt  
C: \\ directory1 \\ directory2 \\File2.txt  
</dl>

Wenn der Writer "C: \\ directory1" für *wszpath*, " \* " für *wszfilespec* und " **false** " für *bRecursive* angibt, sollte der Anforderer diese Dateien einschließen:

<dl> C: \\ directory1 \\File1.txt  
C: \\ directory1 \\File2.txt  
</dl>

In allen vorherigen Beispielen sollte das leere Verzeichnis C: directory1  Directory3 neu erstellt werden, wenn der Writer für *bRecursive* true angibt \\ \\ \\ .

In Fällen, in denen sich Dateien, die sich aktuell auf dem Datenträger befinden, nicht in dem von der Datei Gruppe verwendeten Datei Satz als geeigneten oder Standard Speicherort ansehen, hat ein Writer die Möglichkeit, einen alternativen Pfad hinzuzufügen. In diesen Fällen enthält die Definition des Pfads des Datei Satzes den normalen Speicherort der Dateien und den Speicherort, an dem Dateien wieder hergestellt werden sollen, während der Alternative Pfad den aktuellen Speicherort der zu sichernden Dateien enthält.

Alle Dateien im Datei Satz müssen zum Zeitpunkt der Sicherung vorhanden sein. Anfordernde Personen müssen davon ausgehen, dass alle im Datei Satz aufgeführten Dateien für die Sicherung erforderlich sind, und die Sicherung schlägt fehl, wenn Dateien fehlen. Beachten Sie Folgendes: Wenn " \* " für den Parameter " *wszfilespec* " angegeben wird, kann er mit 0 (null) oder mehr Dateien vergleichen.

Beachten Sie, dass solche Writer-Metadaten-Attribute als Alternative Positions Zuordnungen, explizit enthaltene und ausgeschlossene Dateien und Wiederherstellungsmethoden auf Writer-Ebene und nicht auf Komponentenebene festgelegt werden. (Weitere Informationen finden Sie unter [Arbeiten mit dem Writer-Metadatendokument](working-with-the-writer-metadata-document.md).)

## <a name="component-definition-for-backup-and-restore-operations"></a>Komponenten Definition für Sicherungs-und Wiederherstellungs Vorgänge

Sowohl Restore-als auch Backup-Vorgänge generieren notwendigerweise ein [*identifizereignis*](vssgloss-i.md), und für beide Sicherungen und Wiederherstellungen wird Sie von der gleichen [**CVssWriter:: OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) -Methode behandelt.

Bei Sicherungs Vorgängen werden von anfordernden Personen die Informationen verwendet, die von den [**CVssWriter:: onidentifi-**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) Methoden eines Writers zurückgegeben werden, um zu bestimmen, welche Writer auf dem System vorhanden sind, und um zu bestimmen, welche Dateien gesichert werden sollen.

Während des Wiederherstellungs Vorgangs werden die Informationen, die vom [**CVssWriter:: OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) -Ereignis eines Writers zurückgegeben werden, nur zum Einrichten der Identität und des Status von Writern verwendet, die derzeit auf dem System vorhanden sind. die während einer Wiederherstellung generierten Datei Spezifikations Informationen werden nicht verwendet. Stattdessen werden die zum Zeitpunkt der Sicherung gespeicherten Writer-Metadatendokumente verwendet, um diese Daten abzurufen.

Nach der Generierung während eines Sicherungs Vorgangs werden die Informationen der Writer-Komponente zusammen mit den restlichen Writer-Informationen gespeichert, damit Sie wieder hergestellt werden können. Der Anforderer ist in der Regel dafür verantwortlich, diese Informationen zu speichern.

 

 
