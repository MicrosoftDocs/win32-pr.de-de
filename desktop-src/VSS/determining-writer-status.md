---
description: Ein Anforderer muss über ein klar definiertes Verständnis bezüglich des Status des Writers verfügen, der während der Erstellung der Schatten Kopie und während Sicherungs-und Wiederherstellungs Vorgängen an dieser teilnimmt.
ms.assetid: 676d5cff-bd28-43f0-a402-d184c96f0061
title: Ermitteln des Writer-Status
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 719322a18808748e92d412c48c7b7628fdac9d51
ms.sourcegitcommit: 70f39ec77d19d3c32c376ee2831753d2cafae41a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104219115"
---
# <a name="determining-writer-status"></a>Ermitteln des Writer-Status

Ein Anforderer muss über ein klar definiertes Verständnis bezüglich des Status des Writers verfügen, der während der Erstellung der Schatten Kopie und während Sicherungs-und Wiederherstellungs Vorgängen an dieser teilnimmt. Zu diesem Zweck wird Folgendes empfohlen:

-   Anforderer verwenden [**IVssBackupComponents:: gatherbeschreiterstatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus), [**IVssBackupComponents:: getschreiterstatuscount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatuscount)und [**IVssBackupComponents:: getschreiterstatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus).
-   Wie in Übersicht über die [Verarbeitung einer Sicherung unter VSS](overview-of-processing-a-backup-under-vss.md) und im Überblick über die [Verarbeitung einer Wiederherstellung unter VSS](overview-of-processing-a-restore-under-vss.md)beschrieben, sind diese Methoden besonders nützlich, wenn Sie in einer klar definierten Sicherungs-oder Wiederherstellungs Sequenz aufgerufen werden. In der Regel bedeutet dies, dass die Writer abgefragt werden sollten, nachdem ein Anforderer eine seiner Aufgaben abgeschlossen und ein VSS-Ereignis generiert hat.

    Wenn eine Sicherung verarbeitet wird, sollte ein Antragsteller einen Writer nach dem Abschluss der folgenden Methoden Abfragen. Anforderer muss [**gatherschreibstatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) nach dem Aufruf von [**BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) aufrufen, damit die Writer-Sitzung auf den Status abgeschlossen festgelegt wird.

    > [!Note]  
    > Dies ist nur auf Windows Server 2008 mit Service Pack 2 (SP2) und früher erforderlich.

     

    <dl> <dt>

[**IVssBackupComponents::P Analyse forbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup)
</dt> <dt>

[**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)
</dt> <dt>

[**IVssBackupComponents:: BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete)
</dt> </dl>

Während des Wiederherstellungs Vorgangs sollte ein Antragsteller einen Writer nach Abschluss dieser Methoden Abfragen:
<dl> <dt>

[**IVssBackupComponents::P erneut ausführen**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore)
</dt> <dt>

[**IVssBackupComponents::P ostrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore)
</dt> </dl>

-   Aufrufe von [**IVssBackupComponents:: gatherwrite Status**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) , die nicht Teil einer klar definierten Sicherungs-oder Wiederherstellungs Sequenz sind, bieten kein zuverlässiges Bild des Writer-Status, da Sie möglicherweise Bedingungen widerspiegeln, die im aktuellen Vorgang keinen Fehler angeben, z. b.:
    -   Fehler bei der Erstellung vorheriger Schatten Kopien.
    -   Ein Fehler in einem frühen Sicherungs-oder Wiederherstellungs Vorgang.
    -   Ein nicht reagierender Writer, der derzeit ein Ereignis verarbeitet

Daher sollten sich Entwickler nicht auf den Schreiber Status verlassen, der von anderen Prozessen als der Anforderer zurückgegeben wird, oder versuchen, den Fortschritt einer Instanz der [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) -Schnittstelle mit einer anderen (möglicherweise in einem separaten Thread) zu überwachen.

Beachten Sie, dass bei Sicherungs Vorgängen, bei denen es erforderlich ist, Writer-Metadatendokumente zu untersuchen, kein Anforderer-Befehl für [**IVssBackupComponents:: GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) und [**IVssBackupComponents:: getwriterstatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) nach der Generierung und [*Behandlung des von*](vssgloss-i.md) [**IVssBackupComponents:: gatherwritermetdata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata)verursachten Erstellungs Ereignisses ist.

[**IVssBackupComponents:: getwriterstatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) meldet nur den Status dieser Writer, deren Metadaten von Writern von Writer [*-Ereignis*](vssgloss-i.md) Handlern, [**CVssWriter:: onidentifi(**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) und zurückgegeben von [**IVssBackupComponents:: GetWriterMetadataCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadatacount) und [**IVssBackupComponents:: getwritermetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata)) für VSS bereitgestellt wurden.

Wenn die Implementierung von [**CVssWriter:: OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) eines Writers fehlschlägt, werden die Metadaten des Writers nicht in der Liste der für den VSS bereitgestellten Writer-Metadatendokumente angezeigt, es sind keine Statusinformationen verfügbar, und der-Befehl wäre redundant.

Bei Wiederherstellungs Vorgängen, bei denen der Anforderer keine Writer-Metadatendokumente zum Ausführen von Writern untersuchen muss, kann der Aufruf von [**IVssBackupComponents:: GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) und [**IVssBackupComponents:: getwriterstatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) eine effizientere Möglichkeit sein, um zu bestimmen, welche Writer ausgeführt werden.

 

 



