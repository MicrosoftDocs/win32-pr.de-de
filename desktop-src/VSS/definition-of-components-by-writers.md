---
description: Komponenten werden von Writern in ihrem Writer-Metadatendokument als Reaktion auf ein Identify-Ereignis zu Beginn eines Sicherungsvorgang (siehe Übersicht über die Sicherungsin initialisierung) definiert und instanziiert, wenn das Writer-Metadatendokument aufgefüllt wird.
ms.assetid: 5e1c3f9b-ca83-4e70-963b-0a237c6f4b0d
title: Definition von Komponenten nach Writern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82fa08acba3c49cd99e83a5dcc901d4a12108a9dc6dde9891add93bcc54e3566
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136381"
---
# <a name="definition-of-components-by-writers"></a>Definition von Komponenten nach Writern

Komponenten werden von Writern in ihrem Writer-Metadatendokument als Reaktion auf ein [*Identify-Ereignis*](vssgloss-i.md) zu Beginn eines Sicherungsvorgang definiert und instanziiert (siehe Übersicht über die Sicherungsin initialisierung), [](overview-of-backup-initialization.md)wenn das Writer-Metadatendokument aufgefüllt wird.

Beim Erstellen einer Komponente im Writer-Metadatendokument mithilfe von [**IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata) und [**IVssCreateWriterMetadata::AddComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponent)muss ein Writer Folgendes angeben:

-   Gibt an, ob die Komponente [ *für die Sicherung ausgewählt werden kann.*](vssgloss-s.md)
-   Ein Komponententyp
-   Ein Komponentenname (der nicht nur innerhalb [](vssgloss-w.md) einer bestimmten Writerinstanz, sondern über alle Writerinstanzen hinweg eindeutig sein muss)
-   Gibt an, ob der Komponente writerspezifische Metadaten zugeordnet sind
-   Ob der Writer nach einer erfolgreichen Sicherung eine Benachrichtigung erfordert

Writer können optional Folgendes angeben:

-   Der logische Pfad einer [*Komponente*](vssgloss-l.md) (der nicht nur innerhalb einer bestimmten Writerinstanz, sondern über alle Writerinstanzen hinweg eindeutig sein muss)
-   Eine Komponentenbeschreibung (oder Beschriftung)
-   Ein Symbol, das mit GUIs verwendet werden soll, um die Komponente anzugeben.

Es ist nicht erforderlich, dass eine Komponente tatsächlich Dateien enthält. Diese Art von leerer oder "Dummy"-Komponente kann beim Organisieren von Komponenten nützlich sein. Eine solche Komponente kann verwendet werden, um einen [*Komponentensatz*](vssgloss-c.md) und die Komponente eines Writers zu definieren (siehe [Logisches Pfading von Komponenten](logical-pathing-of-components.md)).

## <a name="setting-up-component-organization"></a>Einrichten der Komponentenorganisation

Das Festlegen der Auswählbarkeit [](vssgloss-s.md)einer Komponente [*(die*](vssgloss-s.md) Auswählbarkeit für [](vssgloss-l.md) die Sicherung und die Selektorierbarkeit für die Wiederherstellung) [](/windows)und der logischen [](vssgloss-c.md) Pfade ermöglicht es einem Writer, die Einbeziehung bestimmter Komponenten in einen Sicherungs- oder Wiederherstellungsvorgang zu erauftragen oder optional zu machen und Komponenten in Komponentensätzen zu gruppieren, die eine auswählbare Komponente als Einstiegspunkt für die gesamte Gruppe verwenden.

Die Mitgliedschaft in diesen Gruppierungen bestimmt, welche Komponenten bei Sicherungs- und Wiederherstellungsvorgängen verwendet werden. Wenn "auswählbar" verwendet wird, um für den Sicherungsvorgang wieder auswählbar und für den Wiederherstellungsvorgang zur Wiederherstellung auswählbar zu sein, sollten Entwickler dies verstehen:

-   Wenn komponenten, die von einem bestimmten Writer verwaltet werden, gesichert werden, [](vssgloss-c.md) muss ein An anfordernder [](vssgloss-l.md) Benutzer explizit alle nicht auswählbaren Komponenten ohne auswählbare Vorgänger in seinen logischen Pfad zum Sicherungskomponentendokument enthalten und diese Komponenten als Gruppe sichern und wiederherstellen. [](vssgloss-e.md)
-   Ein Anfordernde hat die Möglichkeit, dem Sicherungskomponentendokument während Sicherungs- und Wiederherstellungsvorgängen explizit auswählbare Komponenten hinzufügen. Nachdem die Komponente hinzugefügt wurde, muss sie sicherungs- oder wiederhergestellt werden.
-   Wenn eine Komponente ausgewählt werden kann, bilden die Komponente und alle ihre [*Unterkomponenten*](vssgloss-s.md) (wie durch logische Pfade definiert) einen Komponentensatz, der als einzelne Einheit behandelt werden kann, die optional an Sicherungs- und Wiederherstellungsvorgängen teilnehmen kann.
-   Ein Anfordernder fügt dem Sicherungskomponentendokument während Sicherungs- und Wiederherstellungsvorgängen nie explizit eine nicht auswählbare Komponente mit auswählbaren Vorgängern hinzu, eine Unterkomponente in einem Komponentensatz. Diese Komponenten [](/windows) müssen implizit eingeschlossen werden, wenn ihr auswählbarer Vorgänger explizit hinzugefügt wird. In diesem Fall müssen sie sichern oder wiederhergestellt werden (siehe Verwendung von Komponenten durch den Anfordernden [).](use-of-components-by-the-requestor.md)
-   Eine auswählbare Komponente mit einem auswählbaren Vorgänger ist immer noch eine Unterkomponente [*(ein*](vssgloss-s.md) Member eines Komponentensets) und kann implizit eingeschlossen werden, wenn der auswählbare Vorgänger explizit in den Vorgang eingeschlossen wird. In diesem Fall werden die Informationen nicht dem Sicherungskomponentendokument hinzugefügt. Wenn der auswählbare Vorgänger nicht im Vorgang enthalten ist, kann die Komponente explizit für die Aufnahme in den Vorgang ausgewählt werden. In diesem Fall sind die Informationen im Dokument sicherungskomponenten enthalten.
-   Eine implizit in einer Sicherung enthaltene Unterkomponenten kann explizit in einen Wiederherstellungsvorgang eingeschlossen werden, unabhängig vom Status eines auswählbaren Vorgängers, wenn sie für die Wiederherstellung ausgewählt werden kann. Alle während eines Wiederherstellungsvorgang für die Wiederherstellungsunterkomponenten auswählbaren Komponenten müssen dem Sicherungskomponentendokument hinzugefügt werden.
-   Ein Writer, dem vor der Generierung der [*Ereignisse PrepareForBackup*](vssgloss-p.md) und [*PreRestore*](vssgloss-p.md) keine Komponente explizit zum Sicherungskomponentendokument hinzugefügt wurde, erhält keine weiteren VSS-Ereignisse.

Weitere Informationen finden Sie unter [Arbeiten mit Auswählbarkeit und logischen Pfaden.](working-with-selectability-and-logical-paths.md)

## <a name="adding-files-to-a-component"></a>Hinzufügen von Dateien zu einer Komponente

Eine Komponente enthält Dateiinformationen in Form eines [*Dateisets, der:*](vssgloss-f.md)

-   Ein Stammverzeichnis der Dateien in der Komponente.
-   Eine Dateispezifikation für die Dateien in der Komponente.
-   Ein Flag, das angibt, ob die Spezifikation der Komponente rekursiv ist.

Je nach Komponententyp, bei dem es sich um eine Datenbank oder eine Dateigruppe handelt, und (im Fall von Datenbankkomponenten) und unabhängig davon, ob es sich bei den zu ladenden Dateien um Daten- oder Protokolldateien handelt, ruft ein Writer [**IVssCreateWriterMetadata::AddFilesToFileGroup,**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup) [**IVssCreateWriterMetadata::AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)oder [**IVssCreateWriterMetadata::AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) auf, um einen Dateisatz hinzuzufügen.

Wenn Sie diese Funktionen verwenden, sollten Sie die Dateien angeben, die dem Dateisatz wie folgt hinzugefügt werden sollen:

-   *wszPath:* Dies ist der Pfad zu dem Verzeichnis, das die Dateien enthält, die dem Dateisatz hinzugefügt werden sollen. Wenn *der bRecursive-Parameter* auf **TRUE** festgelegt ist, gibt der *wszPath-Parameter* eine Hierarchie von Verzeichnissen an, die rekursiv durchlaufen werden sollen, und alle Verzeichnisse sollten neu erstellt werden, einschließlich leerer Verzeichnisse.
-   *wszFilespec:* Diese Zeichenfolge gibt die Dateien in jedem Verzeichnis an, die dem Dateisatz hinzugefügt werden sollen.

Angenommen, die folgende Verzeichnisstruktur ist vorhanden:

<dl> C: \\ Directory1 \\File1.txt  
C: \\ Directory1 \\File2.txt  
C: \\ Directory1 \\ Directory2 \\File1.txt  
C: \\ Directory1 \\ Directory2 \\File2.txt  
C: \\ Directory1 \\ Directory3\\  
</dl>

Wenn der Writer "C: \\ Directory1" für *wszPath,*"File1. " für \* *wszFilespec* und **TRUE** für *bRecursive* angibt, sollte der An anfordernde Benutzer die folgenden Dateien enthalten:

<dl> C: \\ Directory1 \\File1.txt  
C: \\ Directory1 \\ Directory2 \\File1.txt  
</dl>

Wenn der Writer stattdessen "C: \\ Directory1" für *wszPath,*" \* " " für *wszFilespec* und **true** für *bRecursive* angibt, sollte der Anfordernde diese Dateien enthalten:

<dl> C: \\ Directory1 \\File1.txt  
C: \\ Directory1 \\File2.txt  
C: \\ Directory1 \\ Directory2 \\File1.txt  
C: \\ Directory1 \\ Directory2 \\File2.txt  
</dl>

Wenn der Writer "C: \\ Directory1" für *wszPath,*" \* " " für *wszFilespec* und **false** für *bRecursive* angibt, sollte der Anfordernde diese Dateien enthalten:

<dl> C: \\ Directory1 \\File1.txt  
C: \\ Directory1 \\File2.txt  
</dl>

In allen vorherigen Beispielen sollte das leere Verzeichnis C: Directory1 Directory3 neu erstellt werden, wenn der Writer **true** für *bRecursive* \\ \\ \\ angibt.

Für einen Dateisatz, der einer Dateigruppenkomponente hinzugefügt wurde, hat ein Writer die Möglichkeit, einen alternativen Pfad hinzufügen, wenn sich Dateien, die sich derzeit auf dem Datenträger befinden, nicht in dem befinden, was der Writer als geeigneten oder Standardspeicherort betrachten würde. In diesen Fällen enthält die Definition des Pfads des Dateisets den normalen Speicherort der Dateien und den Speicherort, an dem Dateien wiederhergestellt werden sollen, während der alternative Pfad den aktuellen Speicherort der zu sichernden Dateien enthält.

Alle Dateien im Dateisatz müssen zum Zeitpunkt der Sicherung vorhanden sein. An anfordernde Stellen müssen davon ausgehen, dass alle im Dateisatz aufgeführten Dateien für die Sicherung erforderlich sind und die Sicherung fehlschlägt, wenn Dateien fehlen. Beachten Sie, dass \* , wenn " " für den *wszFilespec-Parameter* angegeben wird, 0 (null) oder mehr Dateien übereinstimmen kann.

Beachten Sie, dass solche Writer Metadata Document-Attribute als alternative Speicherortzuordnungen, explizit eingeschlossene und ausgeschlossene Dateien und Wiederherstellungsmethoden auf Writerebene und nicht auf Komponentenebene festgelegt werden. (Weitere Informationen finden Sie unter [Working with the Writer Metadata Document](working-with-the-writer-metadata-document.md).)

## <a name="component-definition-for-backup-and-restore-operations"></a>Komponentendefinition für Sicherungs- und Wiederherstellungsvorgänge

Sowohl Wiederherstellungs- als [](vssgloss-i.md)auch Sicherungsvorgänge generieren notwendigerweise ein Identify-Ereignis, und sowohl für Sicherungen als auch für Wiederherstellungen wird es von derselben [**CVssWriter::OnIdentify-Methode**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) verarbeitet.

Während Sicherungsvorgängen verwenden an anfordernde Stellen die von den [**CVssWriter::OnIdentify-Methoden**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) eines Writers zurückgegebenen Informationen, um zu bestimmen, welche Writer im System vorhanden sind, und um dann zu bestimmen, welche ihrer Dateien gesichert werden sollen.

Bei Wiederherstellungsvorgängen werden die vom [**CVssWriter::OnIdentify-Ereignis**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) eines Writers zurückgegebenen Informationen nur verwendet, um die Identität und den Status von Writern zu erstellen, die derzeit im System vorhanden sind. Die während einer Wiederherstellung generierten Dateispezifikationsinformationen werden nicht verwendet. Stattdessen werden writer-Metadatendokumente, die zur Sicherungszeit gespeichert sind, verwendet, um diese Daten zu erhalten.

Nach dem Erstellen während eines Sicherungsvorganges werden die Informationen der Writerkomponente zusammen mit den restlichen Writerinformationen gespeichert, um zur Unterstützung von Wiederherstellungsvorgängen abgerufen zu werden. Es liegt in der Regel in der Verantwortung des Anfordernden, diese Informationen zu speichern.

 

 
