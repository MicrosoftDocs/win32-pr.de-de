---
description: Eine anfordernde Seite muss möglicherweise Dateien an einem Speicherort wiederherstellen, der durch einen anderen Speicherort als den Standardpfad eines Dateisets oder die Zuordnung des alternativen Speicherorts angegeben wird.
ms.assetid: ce11485c-da0e-4c16-962e-eeedc2da3de4
title: Arbeiten mit neuen Zielen während der Wiederherstellung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9f7b9a614b043a423dd90868b0a66b505ee194ef968daed4952b0ba60fec6b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118590464"
---
# <a name="working-with-new-targets-during-restore"></a>Arbeiten mit neuen Zielen während der Wiederherstellung

Eine anfordernde Seite muss möglicherweise Dateien an einem Speicherort wiederherstellen, der durch einen anderen Speicherort als den Standardpfad eines Dateisets oder die Zuordnung des alternativen [*Speicherorts angegeben wird.*](vssgloss-a.md) Es gibt viele Gründe, warum dies passieren kann. Beispielsweise war kein Wiederherstellungsziel zugänglich, oder ein anfordernde Benutzer fordert absichtlich an, dass Dateien an einem zuvor unbekannten Speicherort wiederhergestellt werden. In diesem Fall verwendet die anfordernde Seite den neuen Zielmechanismus, um Writern anzugeben, dass eine Datei in einem anderen Bereich auf dem Datenträger wiederhergestellt wurde.

Nicht alle Writer unterstützen eine Anfordernde beim Ändern des Wiederherstellungsziels einer Datei. Ein Anfordernde muss die Writer-Unterstützung überprüfen, indem er die Sicherungsschemamaske des Writers überprüft (von [**IVssExerklärwriterMetadata::GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema)zurückgegeben) und überprüft, ob sie das \_ VSS BS \_ WRITER SUPPORTS NEW TARGET-Flag \_ \_ \_ enthält.

Der Anfordernde gibt eine solche Wiederherstellung über die [**IVssBackupComponents::AddNewTarget-Methode**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget) an. Zusätzlich zur Angabe einer Dateispezifikation und eines ursprünglichen und eines neuen Wiederherstellungsziels gibt der Anfordernde Komponenteninformationen an– einen logischen Pfad und Komponentennamen.

Welche Komponenteninformationen verwendet werden, hängt davon ab, ob die Komponente, [](vssgloss-e.md) die die Datei mit einem neuen Ziel verwalten soll, explizit [*oder*](vssgloss-i.md) implizit in die Sicherung eingeschlossen wurde.

Wenn die verwaltende Komponente explizit eingeschlossen wurde, werden ihre Informationen verwendet. Wenn die verwaltende Komponente implizit eingeschlossen wurde, handelt es sich um eine Unterkomponente in einem Komponentensatz. In diesem Fall werden die definierenden Komponenteninformationen des Komponentensets verwendet.

Beim Behandeln des [**PostRestore-Ereignisses**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore) sollten Writer überprüfen, ob eine der Dateien an einem neuen Speicherort wiederhergestellt wurde. Dies kann mithilfe der [**Methoden IVssComponent::GetNewTargetCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtargetcount) und [**IVssComponent::GetNewTarget erfolgen.**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtarget)

Die Instanz der [**IVssComponent-Schnittstelle,**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) die verwendet wird, hängt davon ab, ob die Verwaltungskomponente der Datei der Sicherung explizit oder implizit hinzugefügt wurde.

 

 



