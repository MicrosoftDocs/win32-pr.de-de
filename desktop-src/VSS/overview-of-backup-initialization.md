---
description: 'Diese Phase der Sicherung initialisiert sowohl den Writer als auch den Anforderer, füllt die internen Datenstrukturen auf, gibt die Sicherung an und richtet die Kommunikation von Writer/requster über den erforderlichen-Befehl an IVssBackupComponents:: gatherwrite Metadata ein. Weitere Informationen finden Sie unter Übersicht über die Verarbeitung einer Sicherung unter VSS.'
ms.assetid: 1fc46062-c4a0-4aa2-ae05-3d7cded18584
title: Übersicht über die Initialisierung der Sicherung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53fb97b43cf19ca60e3e4601899700e35bdad3aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360473"
---
# <a name="overview-of-backup-initialization"></a>Übersicht über die Initialisierung der Sicherung

Diese Phase der Sicherung initialisiert sowohl den Writer als auch den Anforderer, füllt die internen Datenstrukturen auf, gibt die Sicherung an und richtet die Kommunikation von Writer/requster über den erforderlichen-Befehl an [**IVssBackupComponents:: gatherwrite Metadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata)ein. Weitere Informationen finden Sie [unter Übersicht über die Verarbeitung einer Sicherung unter VSS](overview-of-processing-a-backup-under-vss.md).

In der folgenden Tabelle wird die Abfolge der Aktionen und Ereignisse angezeigt, die für die Initialisierung der Sicherung erforderlich sind.



| Requestaktion                                                                                                                                                                                                                                                                                                                            | Ereignis                                                     | Writer-Aktion                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Erstellt eine [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) -Schnittstelle und initialisiert Sie zum Verwalten einer Sicherung (siehe " [**kreatevssbackupcomponents**](/windows/desktop/api/VsBackup/nf-vsbackup-createvssbackupcomponents)", [**IVssBackupComponents:: initializeforbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforbackup)) und aktiviert oder deaktiviert die Writer auf dem System. | Keine                                                      | Keine                                                                                                                                                                                                                                                       |
| Legen Sie optional den Kontext für schattenkopievorgänge fest, und Fragen Sie optional das System nach den von ihm unterstützten Anbietern und Schatten Kopien ab (siehe [**IVssBackupComponents:: SetContext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext), [**IVssBackupComponents:: Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query)).                                               | Keine                                                      | Keine                                                                                                                                                                                                                                                       |
| Der Anforderer kann zusätzliche Informationen zur Behandlung von Sicherungs-und Wiederherstellungs Vorgängen bereitstellen (siehe [**IVssBackupComponents:: SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate)).                                                                                                                                                        | Keine                                                      | Keine                                                                                                                                                                                                                                                       |
| Initiiert einen asynchronen Kontakt mit Writern (siehe [**IVssBackupComponents:: gatherwritermetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata))                                                                                                                                                                                           | [*Identifizieren*](vssgloss-i.md) | Erstellt ein Writer-Metadatendokument (Weitere Informationen finden Sie unter [Arbeiten mit dem Writer-Metadatendokument](working-with-the-writer-metadata-document.md) [**CVssWriter:: OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify), [**ivsskreatewrite Metadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata)). |



 

## <a name="requester-actions-during-backup-initialization"></a>Requestaktionen während der Sicherungs Initialisierung

Ein [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) -Objekt kann nur für eine Sicherung verwendet werden. Daher muss ein Anforderer bis zum Ende der Sicherung fortfahren, einschließlich der Veröffentlichung der **IVssBackupComponents** -Schnittstelle. Wenn die Sicherung vorzeitig beendet werden muss, muss der Anforderer [**IVssBackupComponents:: abortbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup) aufzurufen und dann das **IVssBackupComponents** -Objekt freigeben (Weitere Informationen finden Sie unter [Abbrechen von VSS-Vorgängen](aborting-vss-operations.md) ). Versuchen Sie nicht, die **IVssBackupComponents** -Schnittstelle fortzusetzen.

In der Regel wird das Dokument mit den Sicherungs Komponenten eines Anforderers als leer initialisiert. Ein Dokument mit gespeicherten Sicherungs Komponenten kann geladen werden, wenn [**IVssBackupComponents:: initializeforbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforbackup) aufgerufen wird, in der Regel zur Unterstützung von austauschen-Schattenkopievolumes. In diesem Fall unterscheidet sich die Kommunikation zwischen Writer und requster etwas von dem unten beschriebenen. (Weitere Informationen finden Sie unter [Importieren von transportable-schattenkopierten Volumes](importing-transportable-shadow-copied-volumes.md) .)

Um dem Schattenkopiesatz Volumes hinzuzufügen, muss ein Anforderer zuerst den Kontext für den Schattenkopievorgang festlegen, indem [**IVssBackupComponents:: SetContext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext)aufgerufen wird. Wenn diese Methode nicht aufgerufen wird, wird der Standardkontext für Schatten Kopien, VSS- \_ ctx- \_ Sicherung, verwendet. Weitere Informationen zum Festlegen des schattenkopiekontexts finden Sie unter [Kontext Konfigurationen für Schatten Kopien](shadow-copy-context-configurations.md).

Um mit der Beendigung des Setups vor der Sicherung zu beginnen, muss ein Anforderer [**IVssBackupComponents:: SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate)aufrufen. Dadurch weist eine anfordernde Person den Writern Folgendes zu:

-   Der Typ der Sicherung (gemäß Definition im [**VSS \_ - \_ Sicherungstyp**](/windows/desktop/api/Vss/ne-vss-vss_backup_type))
-   Gibt an, ob die Sicherung einen Start fähigen Systemstatus enthält.
-   Gibt an, ob die anfordernde Person die Auswahl einzelner Komponenten unterstützt oder ganze Volumes sichert.

Alle Anforderer, die an Sicherungs-und Wiederherstellungs Vorgängen teilnehmen, müssen immer [**IVssBackupComponents:: gatherschreitermetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata)aufruft. Diese Methode initiiert die Kommunikation von Writer-requster, indem ein VSS- [*identifizereignis*](vssgloss-i.md) generiert wird, in dem ein Writer sein Metadatendokument erstellt.

Vor dem Aufrufen von [**IVssBackupComponents:: gatherwritermetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata), ein Anforderer, hat die Möglichkeit, bestimmte bestimmte Writer und Writer-Klassen mithilfe von [**IVssBackupComponents:: enablewriterclasses**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-enablewriterclasses), [**IVssBackupComponents::D isablewriterinstance**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-disablewriterinstances)und [**IVssBackupComponents::D isablewriterclasses**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-disablewriterclasses) explizit zu aktivieren bzw. zu deaktivieren (Standardmäßig sind alle Klassen aktiviert). Nach dem Aufruf von **IVssBackupComponents:: gatherschreitermetadata** haben diese Aufrufe keine Auswirkung.

Da es keine Möglichkeit gibt, vor dem Aufrufen von [**IVssBackupComponents:: gatherwritermetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata)eine Liste der Writer auf dem System abzurufen, können anfordernde Personen eine zweite Instanz von [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) erstellen und löschen, um die Liste zu erhalten.

Es ist nicht erforderlich, [**IVssBackupComponents:: gatherschreiterstatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) nach dem Abschluss von [**IVssBackupComponents:: gatherwrite Metadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata)aufzurufen. Writer, die das von den Aufrufen generierte [*identifizereignis*](vssgloss-i.md) nicht verarbeiten können, sind nicht Teil der Liste der Writer, die Metadaten bereitstellen, die von [**IVssBackupComponents:: GetWriterMetadataCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadatacount) und [**IVssBackupComponents:: getwritermetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata) gefunden werden (siehe [Ermitteln des Writer-Status](determining-writer-status.md)).

## <a name="writer-actions-during-backup-initialization"></a>Writer-Aktionen während der Sicherungs Initialisierung

Als Reaktion auf das identifizereignis ruft VSS die virtuelle Handlermethode jedes Writers auf, [**CVssWriter:: onidentifi.**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) Ein Writer erstellt sein Writer-Metadatendokument durch Überschreiben der Standard Implementierung von **CVssWriter:: OnIdentify** und mithilfe der [**ivsskreateschreitermetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata) -Schnittstelle.

Beachten Sie, dass andere Anwendungen als der aktuelle Anforderer (z.b. Systemanwendungen) identifizieren können, die vom Writer behandelt werden müssen. Außerdem kann ein Writer nicht innerhalb von [**CVssWriter:: OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) ermitteln, welche Anwendung das Identifikations Ereignis generiert hat.

Dies ist der Fall, wenn ein Writer bei der Verarbeitung eines Sicherungs Vorgangs mehrere identifizierungsereignisse empfangen kann, sollte ein Writer niemals Zustandsinformationen im [**CVssWriter:: OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) -Handler festlegen.

Stattdessen sollte [**CVssWriter:: OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) einen konsistenten Algorithmus zum Erstellen des Writer-Metadatendokuments ausführen. Dies gilt insbesondere, wenn ein Writer das Dokument erstellt hat, weder der Anforderer noch der Schreiber. Ab diesem Zeitpunkt ist es ein Schreib geschütztes Dokument.

Dies bedeutet, dass die Anzahl und der Typ von [*Komponenten*](vssgloss-c.md) , die einem Writer zugeordnet sind, welche Dateien Teil der einzelnen Komponenten sind, und der explizite Ausschluss von Dateien von Sicherungs-oder Wiederherstellungs Vorgängen nicht geändert werden kann, nachdem ein Writer die Verarbeitung des identifizierungsereignisses zurückgegeben hat.

Alle Writer, die an VSS teilnehmen, müssen folgende Aktionen ausführen:

1.  Geben Sie eine Restore-Methode für alle Komponenten an, die vom Writer mithilfe von [**ivsskreateschreitermetadata:: abtrestoremethod**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setrestoremethod)verwaltet werden.
2.  Fügen Sie mithilfe von [**ivsskreatewritermetadata:: addComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponent) mindestens eine Komponente hinzu (Weitere Informationen zur Komponenten Spezifikation finden Sie unter [Definition von Komponenten durch Writer](definition-of-components-by-writers.md) ).

Ein Writer zeigt die Dateien an, die an einem Sicherungs-oder Wiederherstellungs Vorgang beteiligt werden sollen, indem [*Datei Sätze*](vssgloss-f.md)hinzugefügt werden – eine Kombination aus Pfad, die Datei Spezifikation und ein Rekursions Flag – zu einer bestimmten Komponente mithilfe von [**ivsskreateschreitermetadata:: addfilestofilegroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup), [**ivsskreateschreitermetadata:: adddatabasefiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)oder [**ivsskreateschreitermetadata:: adddatabaselogfiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles), je nach Typ (siehe [Hinzufügen von Dateien zu Komponenten](definition-of-components-by-writers.md)).

Ein Writer kann auch über eine oder mehrere leere Komponenten, Komponenten verfügen, denen keine Dateien hinzugefügt wurden. Diese sind beim Organisieren der-Komponenten des Writers sehr nützlich. (Siehe [logische Komponente von Komponenten](logical-pathing-of-components.md).)

Ein Writer verwendet [**ivsskreateschreitermetadata:: addexcludefiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addexcludefiles) , um explizit zu verhindern, dass Dateien in der Sicherung enthalten sind. Dieser explizite Ausschluss ist nützlich, da Platzhalter Zeichen zum Angeben von Dateien für die Aufnahme verwendet werden können (siehe [Ausschluss der Dateilisten Spezifikation](writer-metadata-document-contents.md)). Beachten Sie, dass die Liste Datei ausschließen Vorrang vor Komponenten Dateilisten hat.

[**Ivsskreateschreitermetadata:: addalternate elocationmapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addalternatelocationmapping) wird verwendet, um [*Alternative Speicherort*](vssgloss-a.md) Zuordnungen für angegebene Datei Sätze zu erstellen, die zu einer der Komponenten des Writers hinzugefügt wurden. Diese Zuordnungen werden während der Dateiwiederherstellung verwendet, wenn die Wiederherstellung am ursprünglichen Speicherort einer Datei nicht möglich oder wünschenswert ist. (Weitere Informationen finden Sie [unter Übersicht über die tatsächliche Dateiwiederherstellung](overview-of-actual-file-restoration.md) und [nicht standardmäßige Sicherungs-und Wiederherstellungs Speicherorte](non-default-backup-and-restore-locations.md)

Da der Sicherungs Dateisatz im Writer-Metadatendokument angegeben ist, kann er später nicht geändert werden. Daher sollte ein Writer so codiert werden, dass die Definition des Datei Satzes alle Dateien enthält, die in der Sicherung benötigt werden, entweder anhand des Namens oder anhand von Platzhalter Zeichen. Möglicherweise enthält dies einige Dateien, die möglicherweise nach dem identificingereignis erstellt werden.

 

 



