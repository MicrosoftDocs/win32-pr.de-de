---
description: Mit dem gerichteten Zielmechanismus können Writer Dateien zum Zeitpunkt der Wiederherstellung neu zuordnen.
ms.assetid: c0b4ab26-2bb6-4b0f-b837-01057983b49b
title: Arbeiten mit gerichteten Zielen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e27c5fac6636e15498e79a5e51d6e921ac5465671b6e1a5c36ff9c2604d3fbcf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117937391"
---
# <a name="working-with-directed-targets"></a>Arbeiten mit gerichteten Zielen

Mit dem [*gerichteten Zielmechanismus*](vssgloss-d.md) können Writer Dateien zum Zeitpunkt der Wiederherstellung neu zuordnen. Dadurch können Writer folgende Schritte ausführen:

-   Geben Sie neue Zielspeicherorte an (analog zu [**den IVssBackupComponents::AddNewTarget des**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget)Anfordernden).
-   Freigeben von Speicherplatz, indem nur benötigte Teile einer Datei auf dem Datenträger wiederhergestellt werden, insbesondere dann, wenn eine Datei mit dem [*Partiellen Dateimechanismus*](vssgloss-p.md) gesichert wurde.
-   Ändern Sie das Dateiformat entsprechend den aktuellen Anforderungen.

Jede Datei, die mit einem gerichteten Zielvorgang verwendet werden soll, muss über das [*Wiederherstellungsziel*](vssgloss-r.md) VSS \_ RT DIRECTED \_ verfügen.

Nachdem festgestellt wurde, dass ein Anforderer einen gerichteten Zielvorgang unterstützen kann, verwendet ein Writer (während der Behandlung des [**PreRestore-Ereignisses)**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) die [**IVssComponent::AddDirectedTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddirectedtarget) für die Instanz von [**IVssComponent,**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) die der Komponente entspricht, die die Datei verwaltet (oder die Komponente, die den Komponentensatz definiert, der die Datei enthält), um zu definieren, wie die Datei bei der Wiederherstellung neu zugeordnet werden soll.

Bei Der Verwendung von [**IVssComponent::AddDirectedTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddirectedtarget)geben Writer den Dateinamen und pfad an, der zum Sichern der Datei verwendet wird, den Dateinamen und den Pfad des Wiederherstellungsziels (diese Werte können mit dem ursprünglichen Dateinamen und Pfad übereinstimmen) sowie Quell- und Zieldateibereiche.

Wie bei partiellen Dateivorgängen sind Bereichslisten Paare von Offsets in die zu sichernde Datei (in Bytes) und die Länge des wiederherzustellenden Abschnitts (in Bytes), der Offset und die Länge, die durch einen Doppelpunkt getrennt werden, und jedes Paar durch ein Komma getrennt: *Offset1***:**_Length1_*_,_* *Offset2***:**_Length2_. Jeder Wert ist eine 64-Bit-Ganzzahl im Hexadezimal- oder Dezimalformat.

Wenn ein Writer den gerichteten Zielmechanismus verwenden muss, damit der Anforderer eine Datei an einem neuen Speicherort wiederherstellen kann, hat er [**IVssComponent::AddDirectedTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddirectedtarget) mit dem ursprünglichen Dateinamen und Pfad sowie dem neuen Dateinamen und Pfad aufgerufen und Quellzielbereiche mit einem Nulloffset und einer Länge angegeben, die der gesamten Dateigröße entspricht.

Wenn ein Writer beispielsweise über eine 200.000-Datei (C: \\ WriterData \\ Index.dat) verfügen muss, die als C: \\ WriterData \\ OldIndex.dat wiederhergestellt wird, würde die Quell- und Zielbereichszeichenfolge **"0:204880**" lauten.

Zum erneuten Zuordnen einer großen, teilweise gesicherten Datei verwendet der Anforderer den Quellbereich, der zum Sichern der Datei verwendet wird, und einen Zielbereich, der die Dateigröße reduziert. Die Quellbereichsinformationen können mithilfe von [**IVssComponent::GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile) für die Instanz von [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) abgerufen werden, die der Komponente entspricht, die die Datei verwaltet (oder die Komponente, die den Komponentensatz definiert, der die Datei enthält).

Wenn es sich bei der teilweise gesicherten Datei zunächst um eine große Datei handelt, deren Header (Bytes 64–512) eine Anzahl von Datensätzen und andere häufig aktualisierte Informationen enthält und deren aktuelle Daten in den letzten 65536 Bytes der Datei zu finden sind – Bytes 0x1239E8577A 0x1239E7577A, könnte ein Writer eine Quellbereichsliste als Zeichenfolge **"64:448,0x1239E8577A:65536"** angeben.

Wenn der Writer die wiederhergestellte Datei neu zuordnen möchte, um nur den Header und die neuesten Daten zu enthalten, könnte die Bereichsliste die Zeichenfolge **"0:488,488:65536"** sein.

Vor dem tatsächlichen Ausführen eines Wiederherstellungsvorgangs sollte ein Anforderer überprüfen, ob Dateien eine gezielte Zielunterstützung erfordern.

Hierzu durchläuft der Anforderer zunächst die Writer mit gespeicherten Komponenten im Sicherungskomponentendokument mithilfe von [**IVssBackupComponents::GetWriterComponentsCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponentscount) und [**IVssBackupComponents::GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents).

Die [**IVssBackupComponents::GetWriterComponents-Schnittstelle**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents) wird dann verwendet, um Instanzen der [**IVssWriterComponentsExt-Schnittstelle**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext) zurückzugeben, die [**IVssWriterComponentsExt::GetComponent-**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getcomponent) und [**IVssWriterComponentsExt::GetComponentCount-Methoden**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getcomponentcount) bereitstellt, mit denen der Anforderer [**IVssComponent-Instanzen**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) abrufen kann.

Dadurch kann ein Anforderer gerichtete Zielkandidaten mithilfe von [**IVssComponent::GetDirectedTargetCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdirectedtargetcount) und [**IVssComponent::GetDirectedTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdirectedtarget) für die Instanz von [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) abrufen, die der Komponente entspricht, die die Datei verwaltet (oder die Komponente, die den Komponentensatz definiert, der die Datei enthält).

 

 
