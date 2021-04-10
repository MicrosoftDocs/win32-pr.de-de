---
description: Der gesteuerte Ziel Mechanismus ermöglicht Writer das Neuzuordnen von Dateien zum Zeitpunkt der Wiederherstellung.
ms.assetid: c0b4ab26-2bb6-4b0f-b837-01057983b49b
title: Arbeiten mit gerichteten Zielen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bd2e15ec873b87030a2d01be69d2c3e5f95a193
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041744"
---
# <a name="working-with-directed-targets"></a>Arbeiten mit gerichteten Zielen

Der [*gesteuerte Ziel*](vssgloss-d.md) Mechanismus ermöglicht Writer das Neuzuordnen von Dateien zum Zeitpunkt der Wiederherstellung. Dadurch können Writer folgende Aktionen ausführen:

-   Geben Sie neue Zielspeicher Orte an (analog zu [**IVssBackupComponents:: addnewtarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget)eines Anforderers).
-   Freigeben von Speicherplatz, indem nur benötigte Teile einer Datei auf dem Datenträger wieder hergestellt werden, insbesondere dann, wenn eine Datei mithilfe des [*partiellen Datei*](vssgloss-p.md) Mechanismus gesichert wurde.
-   Ändern Sie das Dateiformat, um die aktuellen Anforderungen zu erfüllen.

Für alle Dateien, die mit einem gerichteten Ziel Vorgang verwendet werden sollen, muss ein [*Wiederherstellungs Ziel*](vssgloss-r.md) von VSS \_ RT \_ angegeben werden.

Nachdem festgestellt wurde, dass ein Anforderer einen gerichteten Ziel Vorgang unterstützen kann, ein Writer (bei der Verarbeitung des [**PreRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) -Ereignisses) verwendet das [**IVssComponent:: adddirectedtarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddirectedtarget) -Element für die Instanz von [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) , das der Komponente entspricht, die die Datei verwaltet (bzw. die Komponente, die den Komponenten Satz definiert, der die Datei enthält), um zu definieren, wie die Datei bei der Wiederherstellung neu zugeordnet werden soll.

Bei Verwendung von [**IVssComponent:: adddirectedtarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddirectedtarget)geben Writer den Dateinamen und den Pfad zum Sichern der Datei an, den Dateinamen und den Pfad des Wiederherstellungs Ziels (diese Werte können mit dem ursprünglichen Dateinamen und Pfad übereinstimmen) sowie Quell-und Ziel Datei Bereiche.

Wie bei partiellen Datei Vorgängen sind Bereichs Listen Paare von Offsets in die zu sichernde Datei (in Bytes) und die Länge des wiederherzustellenden Abschnitts (in Byte), der Offset und die Länge, die durch einen Doppelpunkt getrennt werden, und jedes Paar durch ein Komma getrennt: *offset1 ***:**_Length1_*_,_* * Offset2 ***:**_Length2_. Jeder Wert ist eine 64-Bit-Ganzzahl im Hexadezimal-oder Dezimal Format.

Wenn ein Writer den gerichteten Ziel Mechanismus verwenden muss, damit der Anforderer eine Datei an einem neuen Speicherort wiederherstellen kann, hätte er [**IVssComponent:: adddirectedtarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddirectedtarget) mit dem ursprünglichen Dateinamen und Pfad sowie den neuen Dateinamen und Pfad und den Quell Zielbereich mit einem Offset von 0 (null) und einer Länge angeben, die der gesamten Dateigröße entspricht.

Wenn ein Writer beispielsweise über eine 200K-Datei verfügen muss, z. b \\ . "c: Write Data \\ Index. dat", die als "C: \\ Write Data \\ OldIndex. dat" wieder hergestellt wird, lautet die Zeichenfolge für Quell-und Zielbereich "**0:204880**."

Zum erneuten Zuordnen einer großen, teilweise gesicherten Datei verwendet der Anforderer den Quellbereich, der zum Sichern der Datei verwendet wird, und einen Zielbereich, der die Dateigröße reduziert. Die Informationen zum Quellbereich können mithilfe von [**IVssComponent:: GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile) für die Instanz von [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) abgerufen werden. Dies entspricht der Komponente, die die Datei verwaltet (oder der Komponente, die den Komponenten Satz definiert, der die Datei enthält).

Wenn die teilweise gesicherte Datei anfänglich eine große Datei war, deren Header Bytes 64-512, enthält eine Anzahl von Datensätzen und andere häufig aktualisierte Informationen, und die neuesten Daten befinden sich in den letzten 65536 Bytes der Datei – Bytes 0x1239e8577a bis 0x1239e7577a. ein Writer könnte eine Quell Bereichs Liste als Zeichenfolge "**64:448, 0x1239e8577a: 65536**" angeben.

Wenn der Writer die wiederhergestellte Datei neu zuordnen wollte, sodass Sie nur den Header und die neuesten Daten enthält, kann die Bereichs Liste die Zeichenfolge "**0:488488:65536**" lauten.

Vor dem eigentlichen Ausführen eines Wiederherstellungs Vorgangs sollte ein Anforderer überprüfen, ob Dateien Unterstützung für unterstützte Ziele erfordern.

Zu diesem Zweck durchläuft der Anforderer zuerst die Writer mit gespeicherten Komponenten in seinem Sicherungs Komponenten Dokument mithilfe von [**IVssBackupComponents:: getwritercomponentscount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponentscount) und [**IVssBackupComponents:: getwritercomponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents).

Die [**IVssBackupComponents:: getschreitercomponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents) -Schnittstelle wird dann verwendet, um Instanzen der [**ivssschreitercomponentset**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext) -Schnittstelle zurückzugeben, die die Methoden [**ivssschreitercomponentset XT:: getComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getcomponent) und [](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) [**ivssschreitercomponentset XT:: getcomponentcount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getcomponentcount) bereitstellt

Dadurch kann ein Anforderer die gerichteten Ziel Kandidaten mithilfe von [**IVssComponent:: getdirectedtargetcount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdirectedtargetcount) und [**IVssComponent:: getdirectedtarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdirectedtarget) für die Instanz von [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) abrufen. Dies entspricht der Komponente, die die Datei verwaltet (oder der Komponente, die den Komponenten Satz definiert, der die Datei enthält).

 

 
