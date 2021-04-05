---
description: Nach einer Wiederherstellung überprüfen Writer den Status des Vorgangs, damit Sie die wiederhergestellten Daten verwenden und Fehler behandeln können.
ms.assetid: f9def67a-c4ea-4014-929f-51fbd10d770a
title: Übersicht über Wiederherstellungs Bereinigung und-Beendigung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 391e029cdb109589b42240b5482f6aba2ff43555
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042092"
---
# <a name="overview-of-restore-clean-up-and-termination"></a>Übersicht über Wiederherstellungs Bereinigung und-Beendigung

Nach einer Wiederherstellung überprüfen Writer den Status des Vorgangs, damit Sie die wiederhergestellten Daten verwenden und Fehler behandeln können. Der Anforderer muss auf den Abschluss dieser Aktivität warten. Weitere Informationen finden Sie [unter Übersicht über die Verarbeitung einer Wiederherstellung unter VSS](overview-of-processing-a-restore-under-vss.md).

In der folgenden Tabelle wird die Abfolge der Aktionen und Ereignisse aufgeführt, die nach dem Wiederherstellen eines Wiederherstellungs Vorgangs erforderlich sind.



| Requestaktion                                                                                                                                                                                                                                                                                                                                                              | Ereignis                                                           | Writer-Aktion                                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Der Anforderer gibt das Ende der Wiederherstellung an (siehe [**IVssBackupComponents::P ostrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore)).                                                                                                                                                                                                                                           | [*Postrestore*](vssgloss-p.md) | Der Writer führt die Bereinigung nach der Wiederherstellung durch und behandelt Wiederherstellungs Fehler und Dateien, die an nicht standardmäßigen Speicherorten wieder hergestellt wurden (siehe [**CVssWriter:: OnPostRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostrestore), [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent)). |
| Der Anforderer wartet darauf, dass Writer das [**postrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore) -Ereignis mit [**IVssAsync**](/windows/desktop/api/Vss/nn-vss-ivssasync)verarbeiten. Außerdem sollte der Writer-Status überprüft werden (siehe [**IVssBackupComponents:: gatherschreiterstatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus), [**IVssBackupComponents:: getschreiterstatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus)). | Keine                                                            | Keine                                                                                                                                                                                                                                               |
| Der Anforderer gibt die [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) -Schnittstelle frei.                                                                                                                                                                                                                                                                                    | Keine                                                            | Keine                                                                                                                                                                                                                                               |



 

## <a name="requester-actions-during-cleanup-and-termination"></a>Requestaktionen während der Bereinigung und Beendigung

An diesem Punkt gibt eine anfordernde Person das Ende der Datei Wiederherstellungs Aktivitäten an, indem ein [*postrestore*](vssgloss-p.md) -Ereignis durch Aufrufen von [**IVssBackupComponents::P ostrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore)erzeugt wird.

Die Aktionen der Anforderer sind darauf beschränkt, auf die Writer zu warten, die ggf. einige abschließende Bereinigungs-und Wiederherstellungs Fehler ausführen müssen, und die [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) -Schnittstelle freigeben, nachdem alle Writer das [*postrestore*](vssgloss-p.md) -Ereignis verarbeitet haben.

## <a name="writer-actions-during-cleanup-and-termination"></a>Writer-Aktionen während der Bereinigung und Beendigung

Das [*postrestore*](vssgloss-p.md) -Ereignis wird von der virtuellen Methode [**CVssWriter:: OnPostRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostrestore)behandelt. Die Standard Implementierung gibt nur **dann true** zurück, wenn keine Aktion ausgeführt wird. Wenn ein Writer eine bessere Kontrolle über die nach der Wiederherstellung benötigte Situation ausführen muss, kann er diese Methode überschreiben.

Zusätzlich zu den normalen Bereinigungs Vorgängen (z. b. das Entfernen temporärer Dateien), die ein Writer in [**CVssWriter:: OnPostRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostrestore)ausführen kann, kann er den Erfolg oder Misserfolg von Wiederherstellungs Vorgängen verarbeiten.

Die Behandlung von Wiederherstellungs Fehlern, Dateien, die an einem alternativen Speicherort wieder hergestellt wurden, und der Bedarf an zukünftigen Wiederherstellungen liegt vollständig im Ermessen des Writers. Typische Aktionen können das Vergleichen von Dateien an Alternativen oder neuen Speicherorten mit derzeit verwendeten Dateien, das Zusammenführen von Daten aus mehreren Dateien oder das Starten neuer Sitzungen, die mit den neuen Datendateien verbunden sind, umfassen. VSS bietet die folgenden Mechanismen, um dies Komponenten Weise zu unterstützen:

-   Erfolg oder Fehler beim Wiederherstellen von Komponenten finden Sie unter [**IVssComponent:: getfilerestorestatus**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getfilerestorestatus).
-   Die Verwendung alternativer Speicherort Zuordnungen beim Wiederherstellen von Dateien wird von [**IVssComponent:: getalternatelocationmapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmapping)angegeben.
-   Die Bestimmung, ob eine Wiederherstellung inkrementell ist und weitere Wiederherstellungen erfordert, wird durch Aufrufen von [**IVssComponent:: getadditionalrestore**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getadditionalrestores)erreicht. Writer, die eine komplette Wiederherstellung Ihrer Daten benötigen, sollten erst neu gestartet werden, wenn diese Methode false zurückgibt.
-   Writer können mithilfe von [**IVssComponent:: getnewtargetcount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtargetcount) und [**IVssComponent:: getnewtarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtarget) ermitteln, ob der Anforderer benötigt hat, um Dateien an einem zuvor nicht angegebenen Speicherort wiederherzustellen.

(Weitere Informationen zum Wiederherstellen von Dateien an nicht standardmäßigen Speicherorten finden Sie unter [nicht standardmäßige Sicherungs-und Wiederherstellungs Speicherorte](non-default-backup-and-restore-locations.md).)

Wie bei jeder [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) -Methode gelten die von einer bestimmten Instanz zurückgegebenen Informationen auch für die Komponenten, die explizit für die Sicherung [*eingeschlossen*](vssgloss-e.md) werden, [und für alle](working-with-selectability-for-restore-and-subcomponents.md) Komponenten, die [*implizit*](vssgloss-i.md) für die Sicherungs Subkomponenten eingeschlossen sind. Dies schließt auch die unter Komponenten ein, die explizit von der anfordernden Person mithilfe von [**IVssBackupComponents:: adressstoresubcomponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent) wieder hergestellt werden können.

Da die Writer auf das Dokument mit den Sicherungs Komponenten zugreifen müssen, ist es wichtig, dass der Anforderer die [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) -Schnittstelle erst freigibt, wenn die Verarbeitung der Writer abgeschlossen ist.

 

 



