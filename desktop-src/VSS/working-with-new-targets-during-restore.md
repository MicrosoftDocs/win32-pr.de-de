---
description: Ein Anforderer muss möglicherweise Dateien an einem Speicherort wiederherstellen, der durch einen anderen als den Standardpfad eines Datei Satzes oder seine Alternative Speicherort Zuordnung angegeben wird.
ms.assetid: ce11485c-da0e-4c16-962e-eeedc2da3de4
title: Arbeiten mit neuen Zielen während der Wiederherstellung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31f20a6e8c27c186648d0f662921160ab5c76988
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359838"
---
# <a name="working-with-new-targets-during-restore"></a>Arbeiten mit neuen Zielen während der Wiederherstellung

Ein Anforderer muss möglicherweise Dateien an einem Speicherort wiederherstellen, der durch einen anderen als den Standardpfad eines Datei Satzes oder seine [*Alternative Speicherort Zuordnung*](vssgloss-a.md)angegeben wird. Es gibt viele Gründe, warum dies passieren kann – beispielsweise konnte nicht auf das Wiederherstellungs Ziel zugegriffen werden, oder ein Anforderer, der Benutzer absichtlich anfordert, dass Dateien an einem zuvor unbekannten Speicherort wieder hergestellt werden. In diesem Fall verwendet der Anforderer den neuen Ziel Mechanismus, um Writer anzuzeigen, dass eine Datei in einem anderen Bereich auf dem Datenträger wieder hergestellt wurde.

Nicht alle Writer unterstützen eine anfordernde Person, die das Wiederherstellungs Ziel einer Datei ändert. Ein Anforderer muss die Writer-Unterstützung überprüfen, indem er die Sicherungs Schema Maske des Writers prüft (von [**ivssexamineschreibmetadata:: getbackupschema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema)zurückgegeben) und sicherstellt, dass er den VSS- \_ \_ Writer-Writer \_ unterstützt das \_ neue \_ Zielflag enthält.

Der Anforderer gibt eine solche Wiederherstellung über die [**IVssBackupComponents:: addnewtarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget) -Methode an. Zusätzlich zur Angabe einer Datei Spezifikation und eines ursprünglichen und eines neuen Wiederherstellungs Ziels gibt der Anforderer die Komponenten Informationen an – einen logischen Pfad und einen Komponentennamen.

Welche Komponenten Informationen verwendet werden, hängt davon ab, ob die Komponente, die die Datei mit einem neuen Ziel verwaltet, [*explizit eingeschlossen*](vssgloss-e.md) oder implizit in die Sicherung [*eingeschlossen*](vssgloss-i.md) wurde.

Wenn die Verwaltungs Komponente explizit eingeschlossen wurde, werden die zugehörigen Informationen verwendet. Wenn die Verwaltungs Komponente implizit eingeschlossen wurde, handelt es sich um eine Unterkomponente in einem Komponenten Satz. In diesem Fall werden die Informationen des Komponenten Satzes der definierenden Komponente verwendet.

Während der Behandlung des [**postrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore) -Ereignisses sollten die Writer überprüfen, ob eine Ihrer Dateien an einem neuen Speicherort wieder hergestellt wurde. Dies kann mithilfe der [**IVssComponent:: getnewtargetcount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtargetcount) -Methode und der [**IVssComponent:: getnewtarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtarget) -Methode erfolgen.

Welche Instanz der [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) -Schnittstelle verwendet wird, hängt davon ab, ob die Verwaltungs Komponente der Datei der Sicherung explizit oder implizit hinzugefügt wurde.

 

 



