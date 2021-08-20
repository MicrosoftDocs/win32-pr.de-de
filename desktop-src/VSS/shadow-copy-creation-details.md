---
description: Im Allgemeinen hängt die Art und Weise, wie eine Schattenkopie erstellt wird, vom Typ der zu erstellenden Schattenkopie, ihrem Kontext und der Rolle ab, die Writern im Schattenkopievorgang gewährt wird.
ms.assetid: eab3b39b-dfa7-43ea-adba-cd0b495c373f
title: Details zur Erstellung von Schattenkopien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b8d8f506ef8d5c7acff86cb6a2fa890b3773423fddf339ea4911a0299963224
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998130"
---
# <a name="shadow-copy-creation-details"></a>Details zur Erstellung von Schattenkopien

Im Allgemeinen hängt die Art und Weise, wie eine Schattenkopie erstellt wird, vom Typ der zu erstellenden Schattenkopie, ihrem Kontext und der Rolle ab, die Writern im Schattenkopievorgang gewährt wird. (Weitere Informationen [finden Sie unter Shadow Copy Context Configurations](shadow-copy-context-configurations.md) (Konfigurationen des Schattenkopiekontexts).)

Der Schattenkopiekontext wird durch Aufrufen der [**IVssBackupComponents::SetContext-Methode**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext) festgelegt. Vor dem Aufrufen der [**IVssBackupComponents::D oSnapshotSet-Methode**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) zum Erstellen einer Schattenkopie müssen an anfordernde Benutzer die [**IVssBackupComponents-Methoden**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) in der in den folgenden Abschnitten angegebenen Reihenfolge aufrufen.

## <a name="prerequisites-for-all-shadow-copies"></a>Voraussetzungen für alle Schattenkopien

Unabhängig von der Ebene der Writer-Beteiligung erfordert die Erstellung einer Schattenkopie immer, dass der An anfordernde mit Aufrufen von [**IVssBackupComponents::InitializeForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforbackup) und [**IVssBackupComponents::StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset)initialisiert wird.

Wenn dieser Aufruf nicht erfolgt, gibt die [**IVssBackupComponents::D oSnapshotSet-Methode**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) einen Fehler zurück.

## <a name="shadow-copies-with-writer-participation"></a>Schattenkopien mit Writer-Beteiligung

Wenn der Schattenkopiekontext die Teilnahme des Writers angibt (d. h. [**IVssBackupComponents::SetContext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext) wird mit **VSS \_ CTX \_ BACKUP** oder **VSS \_ CTX \_ APP \_ ROLLBACK aufgerufen):**

-   Anfordernde müssen [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) immer aufrufen, wenn der Schattenkopiekontext die Teilnahme am Writer unterstützt. Wenn der Schattenkopiekontext writer-Teilnahme unterstützt und **IVssBackupComponents::GatherWriterMetadata** vor [**IVssBackupComponents::D oSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)nicht aufgerufen wird, wird ein Fehler zurückgegeben.
-   Wenn eine Anfordernde bestimmte Writerkomponenten auswählen möchte, muss sie [**IVssBackupComponents::AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) aufrufen, bevor [**sie StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) aufruft, um den Schattenkopiesatz zu erstellen.
-   [**StartSnapshotSet muss**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) aufgerufen werden, um den Schattenkopiesatz zu erstellen.
-   An anfordernde Benutzer können dem Schattenkopiesatz ein oder mehrere Volumes hinzufügen, indem sie [**AddToSnapshotSet aufrufen.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset) Einige Writerkomponenten geben möglicherweise keine betroffenen Volumes an. In diesem Fall ist es akzeptabel, dass ein Momentaufnahmesatz leer ist (d. h. keine Volumes enthält).
-   Um die Konsistenz von Writer-Metadaten zu gewährleisten, sollte ein An anfordernder Benutzer immer [**IVssBackupComponents::P repareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) aufrufen, auch wenn keine Komponenten ausgewählt sind. Dadurch generiert VSS ein **PrepareForBackup-Ereignis,** bei dem VSS die [**CVssWriter::OnPrepareBackup-Methode**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpreparebackup) für jeden beteiligten Writer aufruft.
-   VSS generiert [*PrepareForSnapshot-*](vssgloss-p.md) und [*Freeze-Ereignisse,*](vssgloss-f.md) bevor die Schattenkopie als Reaktion auf [**IVssBackupComponents::D oSnapshotSet erstellt wird.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) Writer behandeln die Ereignisse mit [**CVssWriter::OnPrepareSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpreparesnapshot) und [**CVssWriter::OnFreeze**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onfreeze).
-   VSS generiert [*Thaw-Ereignisse*](vssgloss-t.md) und [*PostSnapshot-Ereignisse*](vssgloss-p.md) nach dem Erstellen einer Schattenkopie als Antwort auf [**IVssBackupComponents::D oSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset). Writer behandeln die Ereignisse mit [**CVssWriter::OnThaw**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onthaw) und [**CVssWriter::OnPostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot).

## <a name="shadow-copies-without-writer-participation"></a>Schattenkopien ohne Writer-Beteiligung

Das Erstellen von Schattenkopien ohne Writer-Beteiligung wird für Standardsicherungsanwendungen nicht abgeraten (siehe [Sicherungen ohne Writer-Beteiligung).](backups-without-writer-participation.md)

Es gibt Verwendungsmöglichkeiten, z. B. schnelle Sicherungen eines Datenträgers, um ein Sicherheitsnetz gegen versehentliche Dateibeschädigungen zu bieten, die ohne explizite Beteiligung des Autors durchgeführt werden können. Eine solche Schattenkopie würde entweder den Kontext **VSS \_ CTX \_ FILE SHARE \_ \_ BACKUP** oder **VSS \_ CTX NAS \_ \_ ROLLBACK haben.**

Beachten Sie bei dieser Art von Schattenkopie Folgendes:

-   Anfordernde müssen weiterhin die erforderlichen Methoden aufrufen, die unter [Voraussetzungen für alle Schattenkopien aufgeführt sind.](#prerequisites-for-all-shadow-copies)
-   Anfordernde können [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata)aufrufen, dies ist jedoch nicht erforderlich.
-   Wenn Anfordernde [**IVssBackupComponents::AddComponent,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) [**IVssBackupComponents::P repareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup)oder [**IVssBackupComponents::BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete)aufrufen, wird ein Fehler zurückgegeben.
-   Anbieter generieren keine [*PrepareForSnapshot-,*](vssgloss-p.md) [*Freeze-,*](vssgloss-f.md) [*Thaw-*](vssgloss-t.md)oder [*PostSnapshot-Ereignisse*](vssgloss-p.md) für diese Art von Schattenkopie.

 

 



