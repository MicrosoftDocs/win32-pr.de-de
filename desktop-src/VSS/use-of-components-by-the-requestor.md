---
description: Zusätzlich zum Durchführen einer Sicherung oder Wiederherstellung und zum Überwachen von Schattenkopien muss ein An anfordernde Benutzer Informationen zu den Komponenten der Writer verwalten, mit denen er interagiert.
ms.assetid: 641abfbe-fc72-4468-9ef6-69c452adb1b3
title: Verwendung von Komponenten durch den Anfordernden
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec3149800a3f8cb52afff044e593f6b01177b27054c64a2ee19c19cb570ed633
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998080"
---
# <a name="use-of-components-by-the-requester"></a>Verwendung von Komponenten durch den Anfordernden

Zusätzlich zum Durchführen einer Sicherung oder Wiederherstellung und zum Überwachen von Schattenkopien muss ein An anfordernde Benutzer Informationen zu den Komponenten der Writer verwalten, mit denen er interagiert. Die Komponentenauswahl und der logische Pfad werden verwendet, um Daten in eine Sicherung ein- oder auszuschließen und zu entscheiden, welche Komponenteninformationen im Dokument Sicherungskomponenten enthalten sind.

## <a name="requester-component-selection-during-backup"></a>Auswahl der An anfordernden Komponente während der Sicherung

Während Sicherungsvorgängen importiert eine Anfordernde Writer-Metadatenkomponentendaten mithilfe der [**Methoden IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) und [**IVssBackupComponents::GetWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata) (weitere Informationen finden Sie unter [Übersicht](overview-of-backup-initialization.md) über die Sicherungsin initialisierung).

Nachdem die Writerinformationen mit der [**IVssExwriterMetadata-Schnittstelle**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) untersucht wurden, entscheidet ein An anfordernde Benutzer, welche Writer es sichern soll, und in begrenztem Umfang, welche Komponenten eines bestimmten Writers er sichern wird.

Beim Sichern eines Writers:

-   Muss [](vssgloss-e.md) explizit alle nicht auswählbaren Komponenten eines Writers für Sicherungskomponenten enthalten, ohne für Sicherungsvorderer mithilfe von [**IVssBackupComponents::AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) ausgewählt werden zu können, um die Komponente zum Sicherungskomponentendokument hinzuzufügen.
-   Kann explizit eines writer-Element enthalten, das für Sicherungskomponenten ausgewählt werden kann, indem [**IVssBackupComponents::AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) verwendet wird, um die Komponente dem Sicherungskomponentendokument hinzuzufügen.
-   Wenn eine für die Sicherungskomponente auswählbare [](vssgloss-i.md) Komponente einen Komponentensatz [*definiert,*](vssgloss-c.md)schließt die explizite Einbeziehung implizit alle Elemente des Komponentensets ein – unabhängig davon, ob sie für die Sicherung ausgewählt werden können oder nicht. Diese Komponenten werden dem Sicherungskomponentendokument nicht hinzugefügt.

Beim Hinzufügen einer auswählbaren Sicherungskomponente oder einer nicht auswählbaren für Sicherungskomponenten, ohne dass sicherungserfahrene Elemente dem Sicherungskomponentendokument ausgewählt werden können, gibt ein An anfordernder Benutzer Folgendes an:

-   Die Instanz des Writer, der die Komponente verwalten soll.
-   Der Klassenbezeichner des Writers
-   Der [*logische Pfad*](vssgloss-l.md) der Komponente (kann NULL **sein)**
-   Name der Komponente

Wenn eine Komponente nicht der Spezifikation entspricht, wird ein Fehler zurückgegeben.

Wenn eine solche Komponente vorhanden ist, erstellt VSS eine [**IVssComponent-Schnittstelle**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) für die Komponente im Dokument Sicherungskomponenten. Diese Informationen sind für den Writer und die Anfordernde zugänglich und änderbar. Bei einer auswählbaren Komponente, die einen Komponentensatz [*definiert,*](vssgloss-c.md)werden nicht nur die Eigenschaften der Komponente, sondern auch alle in ihr enthaltenen Unterkomponenten beschrieben.

Informationen zu implizit hinzugefügten Komponenten sind im Dokument sicherungskomponenten nicht verfügbar. Darüber hinaus sind im Dokument Sicherungskomponenten keine Dateiinformationen verfügbar. Um diese Informationen zu erhalten, muss der Anfordernde die Writer-Metadatendokumente (die bereits gelesen wurden) im Kontext der ausgewählten gespeicherten Komponenten im Sicherungskomponentendokument untersuchen.

## <a name="requester-component-selection-during-restore"></a>Auswahl der anfordernden Komponente während der Wiederherstellung

Bei Wiederherstellungsvorgängen sollte ein An anfordernder Benutzer keine Komponenteninformationen von den Writern importieren, die derzeit im System über [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata)aktiv sind, da der Status der derzeit ausgeführten Prozesse nicht notwendigerweise den Zustand der Prozesse wiedergelangt, als eine Sicherung erstellt wurde.

Es sollte weiterhin ein [*Identify-Ereignis*](vssgloss-i.md) über [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata)generieren, um sowohl ein *Identify-Ereignis* zu erstellen als auch um zu bestimmen, welche Writer sich derzeit im System befinden und deren Status.

Der Anfordernde ruft das gespeicherte Sicherungskomponentendokument während seiner Initialisierung [](overview-of-restore-initialization.md) sowie gespeicherte Writer-Metadatendokumente ab (weitere Informationen finden Sie unter Übersicht über die Wiederherstellungsin initialisierung).

Die Einbeziehung von Komponenten während der Sicherung ist größtenteils [](vssgloss-s.md) identisch mit der [](vssgloss-l.md)für die Wiederherstellung, mit der Ausnahme, dass Sie die Wiederherstellung zusammen mit dem logischen Pfad in Betracht ziehen müssen – nicht für die Sicherung [*auswählbar.*](vssgloss-s.md)

Es gibt jedoch einige Unterschiede:

-   Wenn eine Komponente [](vssgloss-e.md) während der Sicherung bereits explizit in das Sicherungskomponentendokument eingeschlossen wurde und für die Wiederherstellung (explizit oder implizit) enthalten ist, wird [**IVssBackupComponents::SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore) verwendet, um sie explizit dem Sicherungskomponentendokument für die Wiederherstellung hinzuzufügen.
-   Wenn eine [](vssgloss-i.md) Komponente implizit in die Sicherung eingeschlossen wurde und für die Wiederherstellung nicht ausgewählt werden kann, ohne dass die Vorgängerelemente für die Wiederherstellung ausgewählt werden können – was im Fall der Sicherung die Notwendigkeit einer expliziten Einbeziehung bedeuten würde –, wird die Komponente nicht explizit eingeschlossen (d. h., sie wird dem Sicherungskomponentendokument nicht mithilfe von [**IVssBackupComponents::SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore)hinzugefügt). Eine solche Komponente sollte als implizit für die Wiederherstellung ausgewählt betrachtet werden.
-   Von den Komponenten, die implizit für die Sicherung ausgewählt wurden (unabhängig davon, ob diese Komponente für die Sicherung ausgewählt werden konnte) können nur die Komponenten, die für die Wiederherstellung ausgewählt werden können, dem Sicherungskomponentendokument mithilfe von [**IVssBackupComponents::AddRestoreSubcomponent hinzugefügt werden.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent)
-   Für Wiederherstellungskomponenten auswählbar kann ein [*Komponentensatz*](vssgloss-c.md) für die Wiederherstellung definiert werden – genau wie bei Sicherungskomponenten. Diese für die Wiederherstellungskomponente auswählbare Komponente definiert dann diesen Komponentensatz für den Wiederherstellungsvorgang.

Ein Writer ohne Komponenten, die vor der Generierung eines [*PreRestore-Ereignisses*](vssgloss-p.md) explizit für die Wiederherstellung ausgewählt wurden, erhält keine VSS-Ereignisse.

Anfordernde und Writer können über die [**IVssComponent-Schnittstelle auf gespeicherte Komponenteninformationen**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) zugreifen. Über die **IVssComponent-Schnittstelle** können Writer einige der Einstellungen ihrer Komponenten ändern, die explizit im Dokument sicherungskomponenten enthalten sind, um eine Wiederherstellung zu unterstützen (z. B. das Wiederherstellungsziel ). [](vssgloss-r.md) Wenn sie einen Komponentensatz definiert, werden Writeränderungen einer explizit eingeschlossenen Komponente an ihre Unterkomponenten [*weiterversetzt.*](vssgloss-s.md) Darüber hinaus bietet die -Schnittstelle einen Mechanismus zum Übergeben von Informationen zum Wiederherstellungserfolg und -fehler zwischen Writer und Anfordernde.

Wie bei der Sicherung sind im Sicherungskomponentendokument selbst nicht genügend Informationen enthalten, um die Wiederherstellung zu implementieren. Auch hier müssen die Writer-Metadatendokumente Informationen zu den tatsächlichen Pfaden der wiederherzustellenden Dateien bereitstellen und feststellen, welche nicht auswählbaren Komponenten Teil des Komponentensets der auswählbaren Komponenten sind und daher wiederhergestellt werden müssen.

Informationen zu den Auswählbarkeitstypen und deren Verwendung finden Sie unter Working [with Selectability](working-with-selectability-and-logical-paths.md) and Logical Paths (Arbeiten mit Auswählbarkeit und logischen Pfaden).

## <a name="use-of-writer-component-document-information-by-the-requester"></a>Verwenden von Dokumentinformationen der Writer-Komponente durch den Anfordernden

Jede Komponente wird eindeutig durch die [*Writer-Klassen-ID ihres*](vssgloss-w.md) übergeordneten Writers, ihren Namen und ihren [*logischen Pfad identifiziert.*](vssgloss-l.md)

Der Anfordernde kann die [**IVssWriterComponentsExt-Schnittstelle**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext) verwenden, die von der [**IVssBackupComponents::GetWriterComponents-Methode**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents) zurückgegeben wird, um Informationen zu jeder gespeicherten Komponente zu erhalten.

Der Name und logische Pfad der Komponente (unter anderem) finden Sie über die [**IVssComponent-Schnittstelle,**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) die von [**IVssWriterComponentsExt::GetComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getcomponent)zurückgegeben wird.

> [!Note]  
> Während der Wiederherstellungsphase sollte der Anfordernde [**IVssWriterComponentsExt::GetComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getcomponent) oder [**IVssWriterComponentsExt::GetComponentCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getcomponentcount) erst aufrufen, nachdem der Aufruf von [**IVssBackupComponents::P reRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) zurückgegeben wurde, um dem Writer Zeit zum Aktualisieren des Sicherungskomponentendokuments zu geben. Ein Beispiel für ein solches Update wäre das Ändern des Wiederherstellungsziels.

 

Informationen zum übergeordneten Writer jeder gespeicherten auswählbaren Komponente finden Sie mithilfe von [**IVssWriterComponentsExt::GetWriterInfo.**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getwriterinfo)

Mit diesen Informationen können die Writer-Metadatendokumente abgefragt und das übereinstimmende Dokument identifiziert werden. Anschließend kann der [](vssgloss-l.md)An anfordernde Benutzer mithilfe des logischen Pfads die abhängigen, nicht auswählbaren Komponenten für jede auswählbare Komponente identifizieren, d. b. alle Member des Komponentensets der auswählbaren Komponente [*identifizieren.*](vssgloss-c.md)

Mithilfe der [**IVssExerklärwriterMetadata-Schnittstelle**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) verfügt der Anfordernde jetzt über vollständige Komponenteninformationen – einschließlich pfadspezifikation (von der [**IVssWMComponent-Schnittstelle)**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) – sowohl für auswählbare als auch für nicht auswählbare Komponenten, die er sichern oder wiederherstellen muss.

Dies ist ein Grund, warum es für einen An anfordernden wichtig ist, sowohl den Zustand seines eigenen Sicherungskomponentendokuments als auch die Writer-Metadatendokumente der zu sichernden Writer zu speichern.

Ausführlichere Informationen finden Sie unter Working [with Selectability and Logical Paths](working-with-selectability-and-logical-paths.md) (Arbeiten mit Auswählbarkeit und logischen Pfaden).

 

 
