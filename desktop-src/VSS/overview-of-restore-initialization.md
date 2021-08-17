---
description: Beim Initialisieren eines VSS-Wiederherstellungsvorgang muss ein An anfordernde Benutzer das Sicherungskomponentendokument und jedes relevante Writer-Metadatendokument abrufen, das während des Sicherungsvorgang erstellt und gespeichert wurde.
ms.assetid: 0a087125-c9d4-460a-8153-3e2e26633ac2
title: Übersicht über die Wiederherstellungsin initialisierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c531e4b47c49e5bd5538ea30583a31273bb6645a445ef1b1ea851bac539411c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117751689"
---
# <a name="overview-of-restore-initialization"></a>Übersicht über die Wiederherstellungsin initialisierung

Beim Initialisieren eines VSS-Wiederherstellungsvorgang muss ein An anfordernde Benutzer das Sicherungskomponentendokument und jedes relevante Writer-Metadatendokument abrufen, das während des Sicherungsvorgang erstellt und gespeichert wurde. Der aktuelle Zustand des Writers wird bei der Behandlung des [*Vom*](vssgloss-i.md) Anfordernden generierten Identify-Ereignisses abgefragt. Weitere Informationen finden Sie unter [Übersicht über die Verarbeitung einer Wiederherstellung unter VSS.](overview-of-processing-a-restore-under-vss.md)

Die folgende Tabelle zeigt die Abfolge der Aktionen und Ereignisse, die zum Initialisieren eines Wiederherstellungsvorgang erforderlich sind.



| Aktion des Anfordernden                                                                                                                                                                                                                                                                                                       | Ereignis                                                     | Writer-Aktion                                                                                                                                                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Erstellen Sie eine [**IVssBackupComponents-Schnittstelle,**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) initialisieren Sie sie, um eine Wiederherstellung zu verwalten, und laden Sie gespeicherte Anfingermetadaten (siehe [**CreateVssBackupComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-createvssbackupcomponents), [**IVssBackupComponents::InitializeForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforrestore)). | Keine                                                      | Keine                                                                                                                                                                                                                                                                                                                      |
| Rufen [**Sie CreateVssExwriterMetadata auf,**](/windows/desktop/api/VsBackup/nf-vsbackup-createvssexaminewritermetadata) um [**IVssExerklärerMetadata-Schnittstellen**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) zu erstellen und sie mit gespeicherten Writer-Metadaten zu laden.                                                                                                           | Keine                                                      | Keine                                                                                                                                                                                                                                                                                                                      |
| Initiieren Eines asynchronen Kontakts mit Writern (siehe [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata).)                                                                                                                                                                      | [*Identifizieren*](vssgloss-i.md) | Der Writer beginnt mit der Ereignisbehandlung zur Unterstützung der Wiederherstellung. Erstellt das Writer-Metadatendokument (siehe [Working with the Writer Metadata Document](working-with-the-writer-metadata-document.md), [**CVssWriter::OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify), [**IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata)). |
| Der Anfordernde wartet darauf, dass Writer initialisiert werden, indem er [**IVssAsync aufruft.**](/windows/desktop/api/Vss/nn-vss-ivssasync)                                                                                                                                                                                                                               | Keine                                                      | Keine                                                                                                                                                                                                                                                                                                                      |



 

## <a name="requester-actions-during-restore-initialization"></a>An anfordernde Aktionen während der Wiederherstellungsin initialisierung

Während der Initialisierungsphase einer Wiederherstellung muss der Anfordernde Zugriff auf das gespeicherte Sicherungskomponentendokument und alle Writer-Metadatendokumente haben.

Abhängig von der Implementierung bedeutet dies, dass der An anfordernde Benutzer entweder verlangt, dass Sicherungsmedien bereitgestellt und lesbar sind, oder dass ein anderer Mechanismus für den Zugriff auf die gespeicherten Metadaten verfügbar ist.

Der An anfordernde Benutzer verwendet das gespeicherte XML-Dokument, das das Sicherungskomponentendokument des Anfordernden enthält, der die Sicherung ausgeführt hat, um das [**Sicherungskomponentendokument mithilfe von IVssBackupComponents::InitializeForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforrestore) zu initialisieren.

Wie bei der Sicherung enthält das Sicherungskomponentendokument nicht genügend Informationen, um eine Wiederherstellung zu unterstützen. Daher benötigt der Anfordernde Zugriff auf diese Writer-Metadatendokumente, die während der Sicherung gespeichert sind (siehe [Verwenden von Komponenten durch den An anfordernden Benutzer).](use-of-components-by-the-requestor.md)

Der Anfordernde ruft die gespeicherten Writermetadaten ab, indem er [**CreateVssExerklärerMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-createvssexaminewritermetadata) für jeden Writer aufruft, dessen Daten sichern wurden und nun wiederhergestellt werden sollen. Diese Funktion erstellt ein [**IVssExerklärwriterMetadata-Objekt**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) für jeden Writer und lädt das Writer Metadata Document des Writer in das -Objekt.

Wie bei der Sicherung muss ein An anfordernder Benutzer ein [*Identify-Ereignis*](vssgloss-i.md) generieren, indem er [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata)aufruft, um die Zusammenarbeit zwischen sich selbst und den Writern des Systems zu initiieren. [**IVssBackupComponents::GatherWriterStatus muss**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) nach Abschluss von [**GatherWriterMetadata nicht aufgerufen werden.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) Writer, die das [*Identify-Ereignis*](vssgloss-i.md) nicht verarbeiten können, werden nicht in die Liste der Writer aufgenommen, die die Metadaten bereitstellen, die von [**IVssBackupComponents::GetWriterMetadataCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadatacount) und [**IVssBackupComponents::GetWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata) zurückgegeben werden sollen (siehe [Determining Writer Status](determining-writer-status.md)).

Wie beim Sicherungsvorgang muss ein Anfrager die Informationen im Sicherungskomponentendokument abfragen und analysieren und mit Daten in den Writer-Metadatendokumenten vergleichen, um zu ermitteln, welche Komponenten gesichert wurden und welche wiederhergestellt werden sollen (siehe [Übersicht](overview-of-preparing-for-restore.md)über die Vorbereitung auf die Wiederherstellung). Darüber hinaus muss der Anfordernde eine detaillierte Liste generieren, die Informationen zu den Dateien auf den für die Wiederherstellung ausgewählten Sicherungsmedien sowie dazu enthält, wie und wo sie wiederhergestellt werden sollen. (Siehe [Generieren eines Wiederherstellungssets](generating-a-restore-set.md).)

Daher kann es für einige Sicherungsanwendungen nützlich sein, auf dem Sicherungsmedium eine eigene Liste (in einem eigenen optimierten Format) der Dateien und der zugehörigen Writer, Komponente, Wiederherstellungsprozedur und Speicherortinformationen zu speichern. Diese Liste kann verwendet werden, um die Menge an Analyse und Vergleich von Writer-Metadatendokumenten und den Sicherungskomponentendokumenten zu minimieren, die zur Unterstützung einer Wiederherstellung erforderlich sind.

## <a name="writer-actions-during-restore-initialization"></a>Writeraktionen während der Wiederherstellungsin initialisierung

Genau wie bei einem Wiederherstellungsvorgang ruft VSS als Reaktion auf das Identify-Ereignis die virtuelle Handlermethode [**CVssWriter::OnIdentify jedes Writers auf.**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify)

Beachten Sie, dass andere Anwendungen als die aktuelle Anfordernde (z. B. Systemanwendungen) Identify-Ereignisse generieren können, die vom Writer verarbeitet werden müssen. Darüber hinaus gibt es keine Möglichkeit für einen Writer, innerhalb von [**CVssWriter::OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) zu bestimmen, welche Anwendung das Identify-Ereignis generiert hat.

Da ein Writer während der Verarbeitung eines Wiederherstellungsvorgang mehrere Identify-Ereignisse empfangen kann, sollten Writer niemals [**Zustandsinformationen im CVssWriter::OnIdentify-Handler**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) festlegen. Stattdessen müssen sie denselben Algorithmus zum Erstellen ihres Writer-Metadatendokuments wie bei Sicherungsvorgängen verwenden (weitere Informationen finden Sie unter [Writer actions during Backup Initialization](overview-of-backup-initialization.md) (Schreibaktionen während der Sicherungsin initialisierung).

 

 



