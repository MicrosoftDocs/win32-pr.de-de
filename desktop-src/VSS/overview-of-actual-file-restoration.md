---
description: Nachdem Sie die unter Übersicht über die Wiederherstellungs Initialisierung und die Übersicht über die Vorbereitung der Wiederherstellung beschriebenen Aktionen durchgeführt haben, verfügt der Anforderer über ausreichend Informationen, um die Wiederherstellung
ms.assetid: 15df39fa-1eb1-4e96-9e26-14470f391de4
title: Übersicht über die tatsächliche Dateiwiederherstellung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6527a10d0880b1e599377abb797449816019ab89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345287"
---
# <a name="overview-of-actual-file-restoration"></a>Übersicht über die tatsächliche Dateiwiederherstellung

Nachdem Sie die unter [Übersicht über die Wiederherstellungs Initialisierung](overview-of-restore-initialization.md) und die Übersicht über die [Vorbereitung der Wiederherstellung](overview-of-preparing-for-restore.md)beschriebenen Aktionen durchgeführt haben, verfügt der Anforderer über ausreichend Informationen, um die Wiederherstellung Die Wiederherstellung von Dateien umfasst weder Writer-Interaktionen noch die Generierung von Ereignissen. Weitere Informationen finden Sie [unter Übersicht über die Verarbeitung einer Wiederherstellung unter VSS](overview-of-processing-a-restore-under-vss.md).

In der folgenden Tabelle wird die Abfolge der Aktionen und Ereignisse angezeigt, die zum Wiederherstellen von Dateien erforderlich sind.



| Requestaktion                                                                                                                                                                                                                                                                                                          | Ereignis | Writer-Aktion |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|---------------|
| Erstellen Sie eine Wiederherstellungs Gruppe für Dateien auf dem Sicherungsmedium.                                                                                                                                                                                                                                                                 | Keine  | Keine          |
| Behandeln von [*gerichteten Zielen*](vssgloss-d.md) oder der Wiederherstellung von [*Teil Dateien*](vssgloss-p.md) (siehe [**IVssComponent:: getdirectedtarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdirectedtarget), [**IVssComponent:: GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile)). | Keine  | Keine          |
| Ignorieren Sie ggf. alle angegebenen Wiederherstellungs Speicherorte, und stellen Sie Sie an einem neuen Speicherort wieder her, der in einem früheren Vorgang von [**IVssBackupComponents:: addnewtarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget)angegeben wurde                                                                                                                       | Keine  | Keine          |
| Wenn die Wiederherstellung inkrementell ist und weitere Wiederherstellungen erforderlich sind, geben Sie an (siehe [**IVssBackupComponents:: setadditionalrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setadditionalrestores) und [inkrementelle und differenzielle Sicherungen](incremental-and-differential-backups.md))                                                     | Keine  | Keine          |
| Um zu erfahren, ob ein Writer den Inhalt des Dokuments mit den Sicherungs Komponenten geändert hat, nennen Sie [**IVssBackupComponents:: getschreitercomponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents). Der Writer hat z. b. möglicherweise das Wiederherstellungs Ziel geändert.                                                                 | Keine  | Keine          |



 

## <a name="requester-actions-during-restoring-files"></a>Requestaktionen beim Wiederherstellen von Dateien

Bei den meisten Dateien auf dem Sicherungsmedium muss die anfordernde Person ihre ursprünglichen Speicherorte und alle neuen Speicherorte oder alternativen Speicherort Zuordnungen ermitteln, die für Sie gelten. (Weitere Informationen zu bewährten Methoden bei der Ermittlung der wiederherzustellenden Dateien und deren Wiederherstellung finden Sie unter [Erstellen einer Wiederherstellungs Gruppe](generating-a-restore-set.md) .)

Darüber hinaus können einige Dateien über [*gesteuerte Ziele*](vssgloss-d.md) verfügen oder die Wiederherstellung von [*Teil*](vssgloss-p.md) Dateien unterstützen. Die Anzahl dieser Dateien kann durch Aufrufen von [**IVssComponent:: getdirectedtargetcount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdirectedtargetcount) und [**IVssComponent:: GetPartialFileCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfilecount)gefunden werden. Informationen zu detaillierten Wiederherstellungs Anweisungen finden Sie unter " [**IVssComponent:: adddirectedtarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddirectedtarget) " und " [**IVssComponent:: GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile)". (Partielle und gesteuerte Dateien können Teil der Komponenten sein, die der ursprünglichen Sicherung implizit oder explizit hinzugefügt wurden. Weitere Informationen finden Sie unter [Arbeiten mit selekabilität für die Wiederherstellung und unter Komponenten](working-with-selectability-for-restore-and-subcomponents.md) .)

Der Erfolg oder das Fehlschlagen einer Wiederherstellung wird auf Komponentenbasis mithilfe von [**IVssBackupComponents:: setfilerestorestatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setfilerestorestatus)angegeben. Der Bedarf an weiteren Wiederherstellungs Vorgängen (im Fall von inkrementellen oder differenziellen Wiederherstellungen) wird auch auf Komponentenbasis mithilfe von [**IVssBackupComponents:: setadditionalrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setadditionalrestores)angegeben.

Im Allgemeinen gibt VSS keinen Mechanismus zum Abrufen von Daten von einem Speichermedium, eine Auswahl von Speichermedien oder die Art und Weise an, wie bestimmt werden soll, wo die Dateien wieder hergestellt werden sollen.

Für bestimmte Writer kann das Wiederherstellen von Dateien jedoch die Verwendung einer dokumentierten benutzerdefinierten Schnittstelle und Prozedur beinhalten. Windows-System Schreiber, die derzeit eine solche Unterstützung erfordern, sind in [speziellen VSS-Verwendungs Fällen](special-vss-usage-cases.md)dokumentiert.

Im Allgemeinen wird empfohlen, dass die Dateien der einzelnen Komponenten jeder Writer- [*Instanz*](vssgloss-w.md) als Einheit verarbeitet werden. Dafür ist Folgendes erforderlich:

-   Zuordnen der einzelnen wiederherzustellenden Dateien mit der verwalteten Komponente. Dies erfordert die Verwendung von Writer-Metadatendokumenten.
-   Abrufen der richtigen Wiederherstellungs Ziel Informationen. Hierfür sind Informationen aus dem Dokument mit den Sicherungs Komponenten erforderlich.

 

 



