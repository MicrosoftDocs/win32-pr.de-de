---
description: Zusätzlich zum Durchführen einer Sicherung oder Wiederherstellung sowie zum Überwachen von Schatten Kopien muss ein Anforderer Informationen zu den Komponenten der Writer verwalten, mit denen er interagiert.
ms.assetid: 641abfbe-fc72-4468-9ef6-69c452adb1b3
title: Verwendung von Komponenten durch den Anforderer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83efdb9e80ac0331289c3b611978e66a58098de6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526306"
---
# <a name="use-of-components-by-the-requester"></a>Verwendung von Komponenten durch den Anforderer

Zusätzlich zum Durchführen einer Sicherung oder Wiederherstellung sowie zum Überwachen von Schatten Kopien muss ein Anforderer Informationen zu den Komponenten der Writer verwalten, mit denen er interagiert. Die Komponentenauswahl und der logische Pfad werden verwendet, um Daten aus einer Sicherung einzubeziehen oder auszuschließen, und um zu entscheiden, welche Komponenten Informationen im Dokument mit den Sicherungs Komponenten enthalten sind.

## <a name="requester-component-selection-during-backup"></a>Auswahl der requestkomponente während der Sicherung

Während des Sicherungs Vorgangs importiert ein Anforderer mithilfe der Methoden [**IVssBackupComponents:: gatherschreitermetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) und [**IVssBackupComponents:: getschreitermetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata) (siehe [Übersicht über die Sicherungs Initialisierung](overview-of-backup-initialization.md) ).

Nach dem untersuchen von Writer-Informationen mit der [**ivssexaminewritermetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) -Schnittstelle entscheidet ein Anforderer, welche Writer er sichert und in begrenztem Umfang, welche der Komponenten eines bestimmten Writers wieder gesichert werden.

Beim Sichern eines Writers wird ein Anforderer:

-   Muss [*explizit*](vssgloss-e.md) alle nicht auswählbaren Writer für Sicherungs Komponenten einschließen, ohne für Sicherungs-Vorgänger verfügbar zu sein, indem [**IVssBackupComponents:: addComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) zum Hinzufügen der Komponente zum Sicherungs Komponenten Dokument verwendet wird.
-   Kann explizit beliebige für Sicherungs Komponenten auswählbare Writer einschließen, indem [**IVssBackupComponents:: addComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) verwendet wird, um die Komponente dem Dokument mit den Sicherungs Komponenten hinzuzufügen.
-   Wenn eine auswählbare for Backup-Komponente einen [*Komponenten Satz*](vssgloss-c.md)definiert, [*umfasst*](vssgloss-i.md) die explizite Einbindung implizit alle Mitglieder des Komponenten Satzes – ob für die Sicherung auswählbar. Diese Komponenten werden dem Dokument mit den Sicherungs Komponenten nicht hinzugefügt.

Beim Hinzufügen einer auswählbaren for Backup-Komponente oder einer nicht auswählbaren Sicherungs Komponente für Sicherungs Komponenten, die für die Sicherung von Vorgängerversionen in den Sicherungs Komponenten dokumentiert sind, gibt ein Anforderer Folgendes

-   Die Instanz des Writers, der die Komponente verwaltet.
-   Der Klassen Bezeichner des Writers.
-   Der [*logische Pfad*](vssgloss-l.md) der Komponente (die möglicherweise **null** ist).
-   Der Name der Komponente.

Wenn eine Komponente nicht mit der Spezifikation identisch ist, wird ein Fehler zurückgegeben.

Wenn eine solche Komponente vorhanden ist, erstellt VSS im Dokument mit den Sicherungs Komponenten eine [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) -Schnittstelle für die Komponente. Diese Informationen können vom Writer und der Anforderer aufgerufen und geändert werden. Für eine auswählbare Komponente, die einen [*Komponenten Satz*](vssgloss-c.md)definiert, werden nicht nur Eigenschaften der Komponente, sondern auch alle darin enthaltenen unter Komponenten beschrieben.

Informationen zu implizit hinzugefügten Komponenten sind im Dokument mit den Sicherungs Komponenten nicht verfügbar. Außerdem sind keine Dateiinformationen im Dokument mit den Sicherungs Komponenten verfügbar. Um diese Informationen zu erhalten, muss der Anforderer die Writer-Metadatendokumente (die bereits gelesen wurden) im Kontext der ausgewählten gespeicherten Komponenten im Dokument mit den Sicherungs Komponenten untersuchen.

## <a name="requester-component-selection-during-restore"></a>Auswahl der requestkomponente während der Wiederherstellung

Während des Wiederherstellungs Vorgangs sollte ein Anforderer keine Komponenten Informationen von den zurzeit im System aktiven Writern über [**IVssBackupComponents:: gatherwritermetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata)importieren, da der Status der derzeit ausgeführten Prozesse nicht notwendigerweise den Status der Prozesse widerspiegelt, wenn eine Sicherung erstellt wurde.

Es sollte immer noch ein [*identifiz-Ereignis*](vssgloss-i.md) über [**IVssBackupComponents:: gatherwritermetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata)generiert werden, um ein *identifizereignis* zu erstellen und um zu bestimmen, welche Writer aktuell im System und deren Status sind.

Der Anforderer Ruft das Dokument der gespeicherten Sicherungs Komponenten während der Initialisierung sowie gespeicherter Writer-Metadatendokumente ab (Weitere Informationen finden Sie unter [Übersicht über die Wiederherstellungs Initialisierung](overview-of-restore-initialization.md) ).

Die Einbindung von Komponenten während der Sicherung ist größtenteils identisch mit denen für die Wiederherstellung, mit der Ausnahme, dass Sie [*für die Wiederherstellung eine auswählbare*](vssgloss-s.md) Verbindung mit dem [*logischen Pfad*](vssgloss-l.md)– nicht [*für die Sicherung ausgewählt*](vssgloss-s.md)haben

Es gibt jedoch einige Unterschiede:

-   Wenn eine Komponente bei der Sicherung bereits explizit im Sicherungs Komponenten Dokument [*enthalten*](vssgloss-e.md) ist, wird [**IVssBackupComponents:: setselectedforrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore) verwendet, um Sie explizit zum Sicherungs Komponenten Dokument für die Wiederherstellung hinzuzufügen.
-   Wenn eine Komponente implizit in die Sicherung [*eingeschlossen*](vssgloss-i.md) wurde und für die Wiederherstellung nicht ausgewählt werden kann, ohne dass für die Wiederherstellung auswählbare Elemente vorhanden sind – was im Sicherungs Fall impliziert, dass eine explizite Einbindung erforderlich ist – ist die Komponente nicht explizit eingeschlossen (d. h., Sie wird nicht im Dokument mit den Sicherungs Komponenten mithilfe von [**IVssBackupComponents:**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore) Eine solche Komponente sollte als implizit für die Wiederherstellung ausgewählt werden.
-   Der Komponenten, die implizit für die Sicherung ausgewählt wurden (unabhängig davon, ob diese Komponente für die Sicherung ausgewählt wurde oder nicht), können nur diejenigen, die für die Wiederherstellung ausgewählt werden können, dem Dokument mit den Sicherungs Komponenten mithilfe von [**IVssBackupComponents:: adressstoresubcomponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent)hinzugefügt werden
-   Auswählbar für Wiederherstellungs Komponenten kann eine [*Komponentengruppe*](vssgloss-c.md) für die Wiederherstellung definieren – genau so, wie Sie für Sicherungs Komponenten ausgewählt ist. Diese Komponente für die Wiederherstellung ist dann für den Wiederherstellungs Vorgang definiert.

Ein Writer ohne explizit für die Wiederherstellung ausgewählte Komponenten vor der Generierung eines [*vorab*](vssgloss-p.md) Ereignisses werden keine VSS-Ereignisse empfangen.

Requester und Writer können mithilfe der [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) -Schnittstelle auf Informationen gespeicherter Komponenten zugreifen. Mithilfe der **IVssComponent** -Schnittstelle können Writer einige der Einstellungen der Komponenten, die im Dokument mit den Sicherungs Komponenten explizit enthalten sind, ändern, um eine Wiederherstellung zu unterstützen (z. b. das [*Wiederherstellungs Ziel*](vssgloss-r.md)). Wenn ein Komponenten Satz definiert wird, werden Writer-Änderungen einer explizit enthaltenen Komponente an die zugehörigen [*unter Komponenten*](vssgloss-s.md)weitergegeben. Außerdem bietet die-Schnittstelle einen Mechanismus zum Übergeben von Informationen über Erfolg und Fehler von Wiederherstellung zwischen Writer und Anforderer.

Wie bei der Sicherung sind im Dokument mit den Sicherungs Komponenten nicht genügend Informationen vorhanden, um die Wiederherstellung zu implementieren. Auch hier sind die Writer-Metadatendokumente erforderlich, um Informationen über die tatsächlichen Pfade der wiederherzustellenden Dateien bereitzustellen und um zu ermitteln, welche nicht auswählbaren Komponenten Teil des auswählbaren Komponenten Satzes sind und daher wieder hergestellt werden müssen.

Weitere Informationen zu den Arten der selekabilität und deren Verwendung finden Sie unter [Arbeiten mit selekabilität und logischen Pfaden](working-with-selectability-and-logical-paths.md) .

## <a name="use-of-writer-component-document-information-by-the-requester"></a>Verwendung von Dokument Informationen des Writer-Komponente durch den Anforderer

Jede Komponente wird eindeutig durch die [*Writer-Klassen-ID*](vssgloss-w.md) des übergeordneten Writers, den Namen und den [*logischen Pfad*](vssgloss-l.md)identifiziert.

Der Anforderer kann die von der [**IVssBackupComponents:: getschreitercomponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents) -Methode zurückgegebene [**ivssschreitercomponentset**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext) -Schnittstelle verwenden, um Informationen zu jeder gespeicherten Komponente abzurufen.

Der Name und der logische Pfad der Komponente (unter anderen Elementen) finden Sie über die von [**ivssschreitercomponentslog:: getComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getcomponent)zurückgegebene [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) -Schnittstelle.

> [!Note]  
> Während der Wiederherstellungs Phase sollte der Anforderer [**ivssschreitercomponentsext:: getComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getcomponent) oder [**ivssschreitercomponentsext:: getcomponentcount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getcomponentcount) nur aufrufen, nachdem der Aufruf von [**IVssBackupComponents::P**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) Realisierungs Vorgang zurückgegeben wurde, um dem Writer Zeit zu geben, das Dokument mit den Sicherungs Komponenten zu aktualisieren. Ein Beispiel für eine solche Aktualisierung wäre das Ändern des Wiederherstellungs Ziels.

 

Informationen zu den übergeordneten Writer der einzelnen gespeicherten auswählbaren Komponenten finden Sie unter Verwendung von [**ivssschreitercomponentsxt:: getschreiterinfo**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getwriterinfo).

Mit diesen Informationen können die Writer-Metadatendokumente abgefragt und das übereinstimmende Dokument identifiziert werden. Anschließend kann der Anforderer mit dem [*logischen Pfad*](vssgloss-l.md)die abhängigen, nicht auswählbaren Komponenten für jede auswählbare Komponente identifizieren, d. –. alle Elemente der [*Komponentengruppe*](vssgloss-c.md)der auswählbaren Komponente identifizieren.

Mithilfe der [**ivssexaminewrite Metadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) -Schnittstelle verfügt der Anforderer nun über vollständige Komponenten Informationen – einschließlich der Pfadspezifikation (von der [**ivsswmcomponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) -Schnittstelle) – sowohl für auswählbare als auch für nicht auswählbare Komponenten, die Sie sichern oder wiederherstellen müssen.

Dies ist ein Grund, warum es wichtig ist, dass ein Anforderer sowohl den Zustand seines eigenen Sicherungs Komponenten Dokuments als auch die Writer-Metadatendokumente der von ihm gesicherten Writer speichert.

Ausführlichere Informationen finden Sie [unter Arbeiten mit selekabilität und logischen Pfaden](working-with-selectability-and-logical-paths.md) .

 

 
