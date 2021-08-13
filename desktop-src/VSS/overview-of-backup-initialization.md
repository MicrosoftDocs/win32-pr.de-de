---
description: Diese Phase der Sicherung initialisiert sowohl den Writer als auch den Anforderer, füllt seine internen Datenstrukturen auf, gibt die Sicherung an und richtet die Kommunikation zwischen Writer und Anforderer über den erforderlichen Aufruf von IVssBackupComponents::GatherWriterMetadata ein. Weitere Informationen finden Sie unter Übersicht über die Verarbeitung einer Sicherung unter VSS.
ms.assetid: 1fc46062-c4a0-4aa2-ae05-3d7cded18584
title: Übersicht über die Sicherungsinitialisierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4054dc644056100a4db28ea11b6dcaf9c358084a1b01b9ad28c13e14133fc5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118591354"
---
# <a name="overview-of-backup-initialization"></a>Übersicht über die Sicherungsinitialisierung

Diese Phase der Sicherung initialisiert sowohl den Writer als auch den Anforderer, füllt seine internen Datenstrukturen auf, gibt die Sicherung an und stellt die Kommunikation zwischen Writer und Anforderer über den erforderlichen Aufruf von [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata)her. Weitere Informationen finden Sie unter [Übersicht über die Verarbeitung einer Sicherung unter VSS.](overview-of-processing-a-backup-under-vss.md)

Die folgende Tabelle zeigt die Abfolge der Aktionen und Ereignisse, die für die Sicherungsinitialisierung erforderlich sind.



| Anfordereraktion                                                                                                                                                                                                                                                                                                                            | Ereignis                                                     | Writer-Aktion                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Erstellt eine [**IVssBackupComponents-Schnittstelle**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) und initialisiert sie, um eine Sicherung zu verwalten (siehe [**CreateVssBackupComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-createvssbackupcomponents), [**IVssBackupComponents::InitializeForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforbackup)) und optional Writer auf dem System zu aktivieren oder zu deaktivieren. | Keine                                                      | Keine                                                                                                                                                                                                                                                       |
| Legen Sie optional den Kontext für Schattenkopievorgänge fest, und fragen Sie optional das System nach den unterstützten Anbietern und Schattenkopien ab (siehe [**IVssBackupComponents::SetContext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext), [**IVssBackupComponents::Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query)).                                               | Keine                                                      | Keine                                                                                                                                                                                                                                                       |
| Der Anforderer kann zusätzliche Informationen zur Verarbeitung von Sicherungs- und Wiederherstellungsvorgängen bereitstellen (siehe [**IVssBackupComponents::SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate)).                                                                                                                                                        | Keine                                                      | Keine                                                                                                                                                                                                                                                       |
| Initiiert den asynchronen Kontakt mit Writern (siehe [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata)).                                                                                                                                                                                           | [*Identifizieren*](vssgloss-i.md) | Erstellt ein WriterMetadatendokument (siehe [Arbeiten mit dem Writer Metadata Document](working-with-the-writer-metadata-document.md), [**CVssWriter::OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify), [**IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata)) |



 

## <a name="requester-actions-during-backup-initialization"></a>Anfordereraktionen während der Sicherungsinitialisierung

Ein [**IVssBackupComponents-Objekt**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) kann nur für eine Sicherung verwendet werden. Daher muss ein Anforderer bis zum Ende der Sicherung fortfahren, einschließlich der Freigabe der **IVssBackupComponents-Schnittstelle.** Wenn die Sicherung vorzeitig beendet werden muss, muss der Anforderer [**IVssBackupComponents::AbortBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup) aufrufen und dann das **IVssBackupComponents-Objekt** freigeben (weitere Informationen finden Sie unter [Abbrechen von VSS-Vorgängen).](aborting-vss-operations.md) Versuchen Sie nicht, die **IVssBackupComponents-Schnittstelle fortzusetzen.**

In der Regel wird das Sicherungskomponentendokument eines Anfordernden als leer initialisiert. Ein gespeichertes Sicherungskomponentendokument kann geladen werden, wenn [**IVssBackupComponents::InitializeForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforbackup) aufgerufen wird, in der Regel zur Unterstützung transportierbarer Schattenkopievolumes. In diesem Fall unterscheidet sich die Kommunikation zwischen Writer und Anforderer etwas von der unten beschriebenen. (Weitere Informationen finden Sie unter [Importing Transportable Shadow Copied Volumes.)](importing-transportable-shadow-copied-volumes.md)

Um dem Schattenkopiesatz Volumes hinzuzufügen, muss ein Anforderer zuerst den Kontext für den Schattenkopievorgang festlegen, indem [**er IVssBackupComponents::SetContext aufruft.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext) Wenn diese Methode nicht aufgerufen wird, wird der Standardkontext für Schattenkopien, VSS \_ CTX \_ BACKUP, verwendet. Informationen zum Festlegen des Schattenkopiekontexts finden Sie unter [Kontextkonfigurationen für Schattenkopien.](shadow-copy-context-configurations.md)

Um mit dem Abschluss des Setups vor der Sicherung zu beginnen, muss ein Anforderer [**IVssBackupComponents::SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate)aufrufen. Dadurch gibt ein Anforderer den Writern Folgendes an:

-   Der Sicherungstyp (wie in [**VSS \_ BACKUP \_ TYPE**](/windows/desktop/api/Vss/ne-vss-vss_backup_type)definiert)
-   Ob die Sicherung einen startbaren Systemstatus enthält
-   Gibt an, ob der Anforderer die Auswahl einzelner Komponenten unterstützt oder ganze Volumes gesichert.

Alle Anforderer, die an Sicherungs- und Wiederherstellungsvorgängen teilnehmen, müssen immer [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata)aufrufen. Diese Methode initiiert die Kommunikation zwischen Writer und Anforderer, indem ein VSS [*Identify-Ereignis*](vssgloss-i.md) generiert wird, als Reaktion darauf, auf das ein Writer sein Metadatendokument erstellt.

Vor dem Aufrufen von [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata)hat ein Anforderer die Möglichkeit, bestimmte Writer- und Writerklassen mithilfe von [**IVssBackupComponents::EnableWriterClasses,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-enablewriterclasses) [**IVssBackupComponents::D isableWriterInstances**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-disablewriterinstances)und [**IVssBackupComponents::D isableWriterClasses**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-disablewriterclasses) explizit zu aktivieren oder zu deaktivieren (standardmäßig sind alle Klassen aktiviert). Nachdem **IVssBackupComponents::GatherWriterMetadata** aufgerufen wurde, haben diese Aufrufe keine Auswirkungen.

Da es keine Möglichkeit gibt, vor dem Aufrufen von [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata)eine Liste von Writern auf dem System abzurufen, können Anfordernde erwägen, eine zweite Instanz von [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) zu erstellen und dann zu löschen, um die Liste abzurufen.

Es ist nicht erforderlich, [**IVssBackupComponents::GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) nach dem Abschluss von [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata)aufzurufen. Writer, die das von den Aufrufen generierte [*Identify-Ereignis*](vssgloss-i.md) nicht verarbeiten können, sind nicht Teil der Liste der Writer, die Metadaten bereitstellen, die von [**IVssBackupComponents::GetWriterMetadataCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadatacount) und [**IVssBackupComponents::GetWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata) gefunden wurden (siehe [Bestimmen des Writerstatus](determining-writer-status.md)).

## <a name="writer-actions-during-backup-initialization"></a>Writeraktionen während der Sicherungsinitialisierung

Als Reaktion auf das Identify-Ereignis ruft VSS die virtuelle Handlermethode jedes [**Writers auf, CVssWriter::OnIdentify.**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) Ein Writer erstellt sein Writer-Metadatendokument, indem er die Standardimplementierungen von **CVssWriter::OnIdentify** überschreibt und die [**IVssCreateWriterMetadata-Schnittstelle**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata) verwendet.

Beachten Sie, dass andere Anwendungen als der aktuelle Anforderer (z. B. Systemanwendungen) Identify-Ereignisse generieren können, die vom Writer behandelt werden müssen. Darüber hinaus gibt es für einen Writer keine Möglichkeit, innerhalb von [**CVssWriter::OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) zu bestimmen, welche Anwendung das Identify-Ereignis generiert hat.

Dies ist der Fall, da ein Writer während der Verarbeitung eines Sicherungsvorgangs mehrere Identify-Ereignisse empfangen kann, sollte ein Writer niemals [**Zustandsinformationen im CVssWriter::OnIdentify-Handler**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) festlegen.

Stattdessen sollte [**CVssWriter::OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) einen konsistenten Algorithmus ausführen, um das Writer Metadata Document des Writers zu erstellen. Dies liegt insbesondere daran, dass weder der Anforderer noch der Writer das Dokument ändern können, nachdem ein Writer das Dokument erstellt hat. Ab diesem Zeitpunkt handelt es sich um ein schreibgeschütztes Dokument.

Dies bedeutet, dass die Anzahl und der Typ der [*Komponenten,*](vssgloss-c.md) die einem Writer zugeordnet sind, welche Dateien Teil jeder Komponente sind, und der explizite Ausschluss von Dateien aus Sicherungs- oder Wiederherstellungsvorgängen nicht geändert werden kann, nachdem ein Writer das Identify-Ereignis verarbeitet hat.

Alle Writer, die an VSS teilnehmen, müssen folgende Schritte ausführen:

1.  Geben Sie eine Wiederherstellungsmethode für alle Komponenten an, die vom Writer mithilfe von [**IVssCreateWriterMetadata::SetRestoreMethod**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setrestoremethod)verwaltet werden.
2.  Fügen Sie mindestens eine Komponente mithilfe von [**IVssCreateWriterMetadata::AddComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponent) hinzu (weitere Informationen zur Komponentenspezifikation finden Sie unter Definition of Components by Writers ( [Definition of Components by Writers).](definition-of-components-by-writers.md)

Ein Writer gibt die Dateien an, die an einem Sicherungs- oder Wiederherstellungsvorgang teilnehmen sollen, indem [*dateisätze*](vssgloss-f.md)– eine Kombination aus Pfad, Dateispezifikation und Rekursionsflag – einer bestimmten Komponente mithilfe von [**IVssCreateWriterMetadata::AddFilesToFileGroup,**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup) [**IVssCreateWriterMetadata::AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)oder [**IVssCreateWriterMetadata::AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)je nach Typ hinzugefügt werden (siehe [Hinzufügen von Dateien zu Komponenten).](definition-of-components-by-writers.md)

Ein Writer kann auch über eine oder mehrere leere Komponenten verfügen, denen keine Dateien hinzugefügt wurden. Diese sind sehr nützlich, um die Komponenten des Writers zu organisieren. (Weitere Informationen finden Sie unter [Logisches Pfading von Komponenten.)](logical-pathing-of-components.md)

Ein Writer verwendet [**IVssCreateWriterMetadata::AddExcludeFiles,**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addexcludefiles) um explizit zu verhindern, dass Dateien in die Sicherung eingeschlossen werden. Dieser explizite Ausschluss ist nützlich, da Platzhalterzeichen verwendet werden können, um Dateien für die Aufnahme anzugeben (siehe [Exclude File List Specification](writer-metadata-document-contents.md)). Beachten Sie, dass die Ausschlussdateiliste Vorrang vor Komponentendateienlisten hat.

[**IVssCreateWriterMetadata::AddAlternateLocationMapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addalternatelocationmapping) wird verwendet, um [*alternative Speicherortzuordnungen*](vssgloss-a.md) für angegebene Dateisätze zu erstellen, die einer der Writerkomponenten hinzugefügt wurden. Diese Zuordnungen werden während der Dateiwiederherstellung verwendet, wenn die Wiederherstellung am ursprünglichen Speicherort einer Datei nicht möglich oder wünschenswert ist. (Siehe [Übersicht über die tatsächliche Dateiwiederherstellung](overview-of-actual-file-restoration.md) und nicht [standardmäßige Sicherungs- und Wiederherstellungsspeicherorte.)](non-default-backup-and-restore-locations.md)

Da der Sicherungsdateisatz im Writer Metadata Document angegeben ist, kann er später nicht mehr geändert werden. Daher sollte ein Writer so codiert werden, dass die Definition des Dateisatzes alle dateien enthält, die in der Sicherung benötigt werden, entweder anhand des Namens oder durch Platzhalterzeichen. Dies kann einige Dateien umfassen, die nach dem Identify-Ereignis erstellt werden können.

 

 



