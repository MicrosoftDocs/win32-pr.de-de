---
description: Nach einer Wiederherstellung überprüfen Writer den Status des Vorgangs, damit sie die wiederhergestellten Daten verwenden und Fehler behandeln können.
ms.assetid: f9def67a-c4ea-4014-929f-51fbd10d770a
title: Übersicht über die Bereinigung und Beendigung der Wiederherstellung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e8ad0b7d40f3c0e5322810f96bb120f28effe4ec3f0d4e278af924962713b2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118122032"
---
# <a name="overview-of-restore-clean-up-and-termination"></a>Übersicht über die Bereinigung und Beendigung der Wiederherstellung

Nach einer Wiederherstellung überprüfen Writer den Status des Vorgangs, damit sie die wiederhergestellten Daten verwenden und Fehler behandeln können. Der Anfordernde muss auf den Abschluss dieser Aktivität warten. Weitere Informationen finden Sie unter [Übersicht über die Verarbeitung einer Wiederherstellung unter VSS.](overview-of-processing-a-restore-under-vss.md)

Die folgende Tabelle zeigt die Abfolge der Aktionen und Ereignisse, die nach einem Wiederherstellungsvorgang erforderlich sind.



| Aktion des Anfordernden                                                                                                                                                                                                                                                                                                                                                              | Ereignis                                                           | Writer-Aktion                                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Der Anfordernde gibt das Ende der Wiederherstellung an (siehe [**IVssBackupComponents::P ostRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore)).                                                                                                                                                                                                                                           | [*PostRestore*](vssgloss-p.md) | Der Writer führt eine Bereinigung nach der Wiederherstellung durch und behandelt Wiederherstellungsfehler und Dateien, die an nicht standardmäßigen Speicherorten wiederhergestellt wurden (siehe [**CVssWriter::OnPostRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostrestore), [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent)). |
| Der Anfordernde wartet auf Writer, um das [**PostRestore-Ereignis**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore) mit [**IVssAsync zu behandeln.**](/windows/desktop/api/Vss/nn-vss-ivssasync) Außerdem sollte der Writerstatus überprüft werden (siehe [**IVssBackupComponents::GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus), [**IVssBackupComponents::GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus)). | Keine                                                            | Keine                                                                                                                                                                                                                                               |
| Der Anfordernde gibt die [**IVssBackupComponents-Schnittstelle**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) frei.                                                                                                                                                                                                                                                                                    | Keine                                                            | Keine                                                                                                                                                                                                                                               |



 

## <a name="requester-actions-during-cleanup-and-termination"></a>An anfordernde Aktionen während der Bereinigung und Beendigung

An diesem Punkt gibt ein Ansucher das Ende seiner Dateiwiederherstellungsaktivitäten an, indem er ein [*PostRestore-Ereignis*](vssgloss-p.md) generiert, indem er [**IVssBackupComponents::P ostRestore aufruft.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore)

Die Aktionen des Anfordernden sind auf das Warten auf die Writer beschränkt, die möglicherweise einige abschließende Bereinigungs- und Wiederherstellungsfehler ausführen und die [**IVssBackupComponents-Schnittstelle**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) freigeben müssen, nachdem alle Writer von der Behandlung des [*PostRestore-Ereignisses*](vssgloss-p.md) zurückgegeben wurden.

## <a name="writer-actions-during-cleanup-and-termination"></a>Writeraktionen während der Bereinigung und Beendigung

Das [*PostRestore-Ereignis*](vssgloss-p.md) wird von der virtuellen [**Methode CVssWriter::OnPostRestore behandelt.**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostrestore) Die Standardimplementierung gibt **einfach TRUE zurück,** ohne eine Aktion zu ergreifen. Wenn ein Writer mehr Kontrolle über die Situation nach der Wiederherstellung haben muss, kann er diese Methode überschreiben.

Zusätzlich zu allen normalen Bereinigungen (z. B. entfernen temporäre Dateien), die ein Writer in [**CVssWriter::OnPostRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostrestore)ausführen kann, kann er den Erfolg oder Fehler von Wiederherstellungsvorgängen behandeln.

Wie Wiederherstellungsfehler, Dateien, die an einem anderen Speicherort wiederhergestellt werden, und die Notwendigkeit zukünftiger Wiederherstellungen behandelt werden, liegt vollständig im Ermessen des Schreibers. Typische Aktionen können das Vergleichen von Dateien an alternativen oder neuen Speicherorten mit dateien sein, die derzeit verwendet werden, das Zusammenführen von Daten aus mehreren Dateien oder das Starten neuer Sitzungen, die mit den neuen Datendateien verbunden sind. VSS bietet die folgenden Mechanismen, um dies komponentenbasierte Unterstützung zu bieten:

-   Erfolg oder Fehler beim Wiederherstellen einer Komponente finden Sie unter [**IVssComponent::GetFileRestoreStatus**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getfilerestorestatus).
-   Die Verwendung alternativer Speicherortzuordnungen beim Wiederherstellen von Dateien wird durch [**IVssComponent::GetAlternateLocationMapping angegeben.**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmapping)
-   Die Ermittlung, ob eine Wiederherstellung inkrementell ist und weitere Wiederherstellungen erfordert, erfolgt durch Aufrufen von [**IVssComponent::GetAdditionalRestores.**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getadditionalrestores) Writer, die eine vollständige Wiederherstellung ihrer Daten benötigen, sollten erst neu gestartet werden, wenn diese Methode FALSE zurückgibt.
-   Writer können mithilfe von [**IVssComponent::GetNewTargetCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtargetcount) und [**IVssComponent::GetNewTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtarget) ermitteln, ob der An anfordernde Benutzer Dateien an einem zuvor nicht angegebenen Speicherort wiederherstellen muss.

(Weitere Informationen zum Wiederherstellen von Dateien an nicht standardmäßigen Speicherorten finden Sie unter [Nicht standardmäßige Sicherungs- und Wiederherstellungsspeicherorte.)](non-default-backup-and-restore-locations.md)

Wie bei jeder [**IVssComponent-Methode**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) gelten die von einer [](vssgloss-e.md) bestimmten Instanz zurückgegebenen [](vssgloss-i.md) Informationen für die Komponenten, die explizit für die Sicherung enthalten sind, und für alle implizit für Sicherungsunterkomponenten enthaltenen Komponenten, einschließlich der Unterkomponenten, die explizit für die Wiederherstellung durch den Anfordernden mithilfe von [**IVssBackupComponents enthalten sind::AddRestoreSubcomponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent) (weitere Informationen finden Sie unter Working with Selectability For Restore and [Subcomponents](working-with-selectability-for-restore-and-subcomponents.md) (Arbeiten mit Auswahlbarkeit für Wiederherstellung und Unterkomponenten).

Da die Writer Zugriff auf das Sicherungskomponentendokument benötigen, ist es wichtig, dass der Anfordernde die [**IVssBackupComponents-Schnittstelle**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) erst frei gibt, wenn writer die Verarbeitung abgeschlossen haben.

 

 



