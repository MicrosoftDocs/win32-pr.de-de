---
description: Beim Initialisieren eines VSS-Wiederherstellungs Vorgangs muss ein Anforderer das Sicherungs Komponenten Dokument und jedes relevante Writer-Metadatendokument abrufen, das während des Sicherungs Vorgangs erstellt und gespeichert wird.
ms.assetid: 0a087125-c9d4-460a-8153-3e2e26633ac2
title: Übersicht über die Wiederherstellungs Initialisierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eb62e5282a74e38cd53d36c8ba004f4b8069746
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131269"
---
# <a name="overview-of-restore-initialization"></a>Übersicht über die Wiederherstellungs Initialisierung

Beim Initialisieren eines VSS-Wiederherstellungs Vorgangs muss ein Anforderer das Sicherungs Komponenten Dokument und jedes relevante Writer-Metadatendokument abrufen, das während des Sicherungs Vorgangs erstellt und gespeichert wird. Der aktuelle Zustand des Writers wird bei der Behandlung des vom Anforderer generierten [*identifizereignisses*](vssgloss-i.md) abgefragt. Weitere Informationen finden Sie [unter Übersicht über die Verarbeitung einer Wiederherstellung unter VSS](overview-of-processing-a-restore-under-vss.md).

In der folgenden Tabelle wird die Abfolge der Aktionen und Ereignisse angezeigt, die zum Initialisieren eines Wiederherstellungs Vorgangs erforderlich sind.



| Requestaktion                                                                                                                                                                                                                                                                                                       | Ereignis                                                     | Writer-Aktion                                                                                                                                                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Erstellen Sie eine [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) -Schnittstelle, initialisieren Sie Sie, um eine Wiederherstellung zu verwalten, und laden Sie gespeicherte requestmetadaten (siehe " [**foratevssbackupcomponents**](/windows/desktop/api/VsBackup/nf-vsbackup-createvssbackupcomponents)", [**IVssBackupComponents:: initializeforrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforrestore)). | Keine                                                      | Keine                                                                                                                                                                                                                                                                                                                      |
| Rufen Sie " [**kreatevssexaminewrite Metadata**](/windows/desktop/api/VsBackup/nf-vsbackup-createvssexaminewritermetadata) " auf, um [**ivssexaminewrite Metadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) -Schnittstellen zu erstellen und Sie mit gespeicherten Writer-Metadaten zu laden.                                                                                                           | Keine                                                      | Keine                                                                                                                                                                                                                                                                                                                      |
| Initiieren eines asynchronen Kontakts mit Writern (siehe [**IVssBackupComponents:: gatherwritermetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata).)                                                                                                                                                                      | [*Identifizieren*](vssgloss-i.md) | Der Writer startet die Ereignis Behandlung zur Unterstützung der Wiederherstellung. Erstellt das Writer-Metadatendokument (Weitere Informationen finden Sie unter [Arbeiten mit dem Writer-Metadatendokument](working-with-the-writer-metadata-document.md) [**CVssWriter:: OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify), [**ivsskreateschreitermetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata)). |
| Der Anforderer wartet darauf, dass Writer durch Aufrufen von [**IVssAsync**](/windows/desktop/api/Vss/nn-vss-ivssasync)initialisiert werden.                                                                                                                                                                                                                               | Keine                                                      | Keine                                                                                                                                                                                                                                                                                                                      |



 

## <a name="requester-actions-during-restore-initialization"></a>Requestaktionen während der Wiederherstellungs Initialisierung

Während der Initialisierungsphase einer Wiederherstellung benötigt der Anforderer Zugriff auf das Dokument mit den gespeicherten Sicherungs Komponenten und alle Writer-Metadatendokumente.

Abhängig von der Implementierung bedeutet dies entweder, dass die anfordernde Person erfordert, dass Sicherungsmedien bereitgestellt und lesbar sind, oder dass ein anderer Mechanismus für den Zugriff auf die gespeicherten Metadaten verfügbar ist.

Der Anforderer verwendet das gespeicherte XML-Dokument mit dem Sicherungs Komponenten Dokument der anfordernden Person, die die Sicherung ausgeführt hat, um das Dokument mit den Sicherungs Komponenten zu initialisieren, indem [**IVssBackupComponents:: initializeforrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforrestore) auf die Informationen zugreifen kann.

Wie im Fall der Sicherung, enthält das Dokument mit den Sicherungs Komponenten nicht genügend Informationen, um eine Wiederherstellung zu unterstützen. Daher benötigt der Anforderer Zugriff auf die während der Sicherung gespeicherten Writer-Metadatendokumente (siehe [Verwendung von Komponenten durch den Anforderer](use-of-components-by-the-requestor.md)).

Der Anforderer Ruft die gespeicherten Writer-Metadaten durch Aufrufen von [**createvssexaminewrite Metadata**](/windows/desktop/api/VsBackup/nf-vsbackup-createvssexaminewritermetadata) für jeden Writer ab, dessen Daten gesichert und nun wieder hergestellt werden müssen. Diese Funktion erstellt ein [**ivssexaminewrite Metadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) -Objekt für jeden Writer und lädt das Writer-Metadatendokument des Writers in das-Objekt.

Wie bei der Sicherung, um die Zusammenarbeit zwischen sich selbst und den Writern des Systems zu initiieren, muss ein Anforderer durch Aufrufen von [**IVssBackupComponents:: gatherwritermetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata)ein [*identifizereignis*](vssgloss-i.md) generieren. Es ist nicht erforderlich, [**IVssBackupComponents:: gatherschreiterstatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) nach dem Abschluss von [**gatherwrite Metadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata)aufzurufen. Writer, die das [*identifizereignis*](vssgloss-i.md) nicht verarbeiten können, sind nicht in der Liste der Writer enthalten, die die Metadaten bereitstellen, die von [**IVssBackupComponents:: GetWriterMetadataCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadatacount) und [**IVssBackupComponents:: getwritermetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata) zurückgegeben werden (siehe [Ermitteln des Writer-Status](determining-writer-status.md)).

Wie beim Sicherungs Vorgang muss ein Anforderer die Informationen im Dokument mit den Sicherungs Komponenten Abfragen und analysieren und mit den Daten in den Writer-Metadatendokumenten vergleichen, um zu bestimmen, welche Komponenten gesichert wurden und welche Komponenten wieder hergestellt werden sollen (Weitere Informationen finden Sie unter [Übersicht über die Vorbereitung der Wiederherstellung](overview-of-preparing-for-restore.md)). Außerdem muss die anfordernde Person eine detaillierte Liste mit Informationen zu den Dateien auf dem Sicherungsmedium generieren, das für die Wiederherstellung ausgewählt wurde, sowie darüber, wie und wo Sie wieder hergestellt werden sollen. (Siehe [Erstellen einer Wiederherstellungs Gruppe](generating-a-restore-set.md).)

Daher ist es bei einigen Sicherungs Anwendungen möglicherweise hilfreich, auf dem Sicherungsmedium eine eigene Liste (in Ihrem eigenen optimierten Format) der Dateien und deren zugeordneten Writer, Komponenten, Wiederherstellungs Prozeduren und Speicherort Informationen zu speichern. Diese Liste kann verwendet werden, um den Umfang der Verarbeitung und den Vergleich von Writer-Metadatendokumenten und den Sicherungs Komponenten Dokumenten zu minimieren, die zur Unterstützung einer Wiederherstellung erforderlich sind.

## <a name="writer-actions-during-restore-initialization"></a>Writer-Aktionen während der Wiederherstellungs Initialisierung

Wie bei einem Wiederherstellungs Vorgang durchgeführt, ruft VSS als Reaktion auf das identifizereignis die virtuelle Handlermethode " [**CVssWriter:: OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify)" für jeden Writer auf.

Beachten Sie, dass andere Anwendungen als der aktuelle Anforderer (z.b. Systemanwendungen) Identifikations Ereignisse generieren können, die vom Writer behandelt werden müssen. Außerdem kann ein Writer nicht innerhalb von [**CVssWriter:: OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) ermitteln, welche Anwendung das Identifikations Ereignis generiert hat.

Wenn ein Writer bei der Verarbeitung eines Wiederherstellungs Vorgangs mehrere identifizierungsereignisse erhalten kann, sollten die Writer niemals Zustandsinformationen im [**CVssWriter:: OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) -Handler festlegen. Stattdessen müssen Sie denselben Algorithmus zum Erstellen Ihres Writer-Metadatendokuments verwenden, wie es bei Sicherungs Vorgängen geschehen ist (Weitere Informationen finden Sie unter [Writer-Aktionen während der Initialisierung der Sicherung](overview-of-backup-initialization.md) ).

 

 



