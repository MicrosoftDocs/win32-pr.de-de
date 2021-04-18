---
description: Im Allgemeinen ist das Erstellen einer Schatten Kopie abhängig vom Typ der zu erstellenden Schatten Kopie, vom Kontext und von der Rolle, die den Writern im Schattenkopievorgang zugewiesen wird.
ms.assetid: eab3b39b-dfa7-43ea-adba-cd0b495c373f
title: Details zur Erstellung von Schatten Kopien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b9281b899593ca0751f1d549aed60305041b18c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106351624"
---
# <a name="shadow-copy-creation-details"></a>Details zur Erstellung von Schatten Kopien

Im Allgemeinen ist das Erstellen einer Schatten Kopie abhängig vom Typ der zu erstellenden Schatten Kopie, vom Kontext und von der Rolle, die den Writern im Schattenkopievorgang zugewiesen wird. (Weitere Informationen finden Sie unter [Kontext Konfigurationen für Schatten Kopien](shadow-copy-context-configurations.md) .)

Der Kontext der Schatten Kopie wird durch Aufrufen der [**IVssBackupComponents:: SetContext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext) -Methode festgelegt. Vor dem Aufrufen der [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) -Methode zum Erstellen einer Schatten Kopie müssen anfordernde Personen die [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) -Methoden in der Reihenfolge aufrufen, die in den folgenden Abschnitten angegeben ist.

## <a name="prerequisites-for-all-shadow-copies"></a>Voraussetzungen für alle Schatten Kopien

Unabhängig von der Ebene der Schreib Beteiligung erfordert die Erstellung einer beliebigen Schatten Kopie immer, dass der Anforderer mit Aufrufen von [**IVssBackupComponents:: initializeforbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforbackup) und [**IVssBackupComponents:: startnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset)initialisiert wird.

Wenn dieser-Befehl nicht durchgeführt wird, gibt die [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) -Methode einen Fehler zurück.

## <a name="shadow-copies-with-writer-participation"></a>Schatten Kopien mit Writer-Beteiligung

Wenn der schattenkopieskontext die Writer-Teilnahme angibt (d. h. [**IVssBackupComponents:: SetContext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext) wird mit **VSS \_ ctx- \_ Sicherung** oder **VSS \_ ctx- \_ App- \_ Rollback** aufgerufen):

-   Anforderer muss immer [**IVssBackupComponents:: gatherschreitermetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) aufruft, wenn der schattenkopieskontext die Writer-Teilnahme unterstützt. Wenn der schattenkopieskontext die Writer-Teilnahme unterstützt und **IVssBackupComponents:: gatherschreitermetadata** nicht vor [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)aufgerufen wird, wird ein Fehler zurückgegeben.
-   Wenn ein Anforderer bestimmte Writer-Komponenten auswählen möchte, muss er [**IVssBackupComponents:: addComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) aufrufen, bevor [**startnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) aufgerufen wird, um den Schattenkopiesatz zu erstellen.
-   [**Startnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) muss aufgerufen werden, um den Schattenkopiesatz zu erstellen.
-   Anforderer können dem Schattenkopiesatz durch Aufrufen von [**addtosnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset)ein oder mehrere Volumes hinzufügen. Einige Writer-Komponenten geben möglicherweise keine betroffenen Volumes an. In diesem Fall ist es akzeptabel, dass eine Momentaufnahme als leer festgelegt ist (d. h., Sie enthält keine Volumes).
-   Um die Konsistenz von Writer-Metadaten zu gewährleisten, sollte ein Anforderer immer [**IVssBackupComponents::P Analyse forbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) aufruft, auch wenn keine Komponenten ausgewählt sind. Dies bewirkt, dass VSS ein **PrepareForBackup** -Ereignis generiert, in dem VSS die [**CVssWriter:: onpreparebackup**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpreparebackup) -Methode für jeden Beteiligten Writer aufruft.
-   VSS generiert [*prepareforsnapshot*](vssgloss-p.md) -und [*Freeze*](vssgloss-f.md) -Ereignisse, bevor die Schatten Kopie als Antwort auf [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)erstellt wird. Writer behandeln die Ereignisse mit [**CVssWriter:: OnPrepareSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpreparesnapshot) und [**CVssWriter:: OnFreeze**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onfreeze).
-   VSS generiert nach dem Erstellen einer Schatten Kopie als Antwort auf [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) [*Thaw*](vssgloss-t.md) -Ereignisse und [*PostSnapshot*](vssgloss-p.md) -Ereignisse. Writer behandeln die Ereignisse mit [**CVssWriter:: OnThaw**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onthaw) und [**CVssWriter:: OnPostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot).

## <a name="shadow-copies-without-writer-participation"></a>Schatten Kopien ohne Writer-Teilnahme

Das Erstellen von Schatten Kopien ohne Writer-Beteiligung wird bei Standard Sicherungs Anwendungen empfohlen (siehe [Sicherungen ohne Writer-Teilnahme](backups-without-writer-participation.md)).

Es gibt Verwendungsmöglichkeiten, wie z. b. schnelle Sicherungen eines Datenträgers zur Bereitstellung eines Sicherheitsnetzes vor versehentlicher Beschädigung von Dateien, die ohne explizite Writer-Teilnahme durchgeführt werden können. Eine solche Schatten Kopie hätte entweder den Kontext der **VSS \_ ctx- \_ Datei \_ Freigabe \_ Sicherung** oder des **VSS \_ ctx \_ NAS- \_ Rollbacks**.

Beachten Sie für diese Art der Schatten Kopie Folgendes:

-   Anfordernde Personen müssen weiterhin die erforderlichen Methoden abrufen, die unter [Voraussetzungen für alle Schatten Kopien](#prerequisites-for-all-shadow-copies)aufgeführt sind.
-   Anfordernde Personen können [**IVssBackupComponents:: gatherschreitermetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata)aufzurufen, dies ist jedoch nicht erforderlich.
-   Wenn Requester [**IVssBackupComponents:: addComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent), [**IVssBackupComponents::P Analyse forbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup)oder [**IVssBackupComponents:: BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete)aufruft, wird ein Fehler zurückgegeben.
-   Anbieter generieren für diese Art von Schatten Kopie keine [*prepareforsnapshot*](vssgloss-p.md)-, [*Freeze*](vssgloss-f.md)-, [*Thaw*](vssgloss-t.md)-oder [*PostSnapshot*](vssgloss-p.md) -Ereignisse.

 

 



