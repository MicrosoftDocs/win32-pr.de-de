---
description: Das Sicherungskomponentendokument wird von Instanzen der IVssBackupComponents-Schnittstelle verwaltet.
ms.assetid: 8c7ebba8-58c4-4733-ba59-802abf902c5e
title: Inhalt des Sicherungskomponentendokuments
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c844f2e9e106817c8201822d000c2f6cb94c0fa272bb5b165d98e4cc48b1c21
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119248340"
---
# <a name="backup-components-document-contents"></a>Inhalt des Sicherungskomponentendokuments

Das Sicherungskomponentendokument wird von Instanzen der [**IVssBackupComponents-Schnittstelle**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) verwaltet. Diese Schnittstelle enthält auch zahlreiche Methoden zum Steuern von Sicherungsvorgängen, Bearbeiten von Schattenkopien und Abfragen des Systemstatus. Nicht alle Informationen des Dokuments sind jedoch direkt über diese Schnittstelle zugänglich.

Das Sicherungskomponentendokument besteht aus mehreren Sätzen von Daten:

-   Informationen darüber, welche Komponenten explizit in einen Sicherungs- oder Wiederherstellungsvorgang eingeschlossen wurden
-   Eine Darstellung der gespeicherten Komponenten- und Writerinformationen
-   Zustandsinformationen zum Sicherungs-/Wiederherstellungsvorgang

Während die Komponenteninformationen sowohl für den Anforderer als auch für den Writer verfügbar sind, hat nur der Writer Zugriff auf die Zustandsinformationen.

## <a name="component-inclusion-information"></a>Komponenteneinschlussinformationen

Das Sicherungskomponentendokument enthält eine Liste dieser Komponenten, die explizit in die Sicherung und Wiederherstellung durch den Anfordernden eingeschlossen sind. Die Liste enthält Folgendes:

-   Explizit [*eingeschlossene auswählbare Komponenten.*](vssgloss-s.md)

    Die Einbeziehung dieser Dateien in Sicherungsvorgänge wird durch [**IVssBackupComponents::AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) und in Wiederherstellungsvorgängen von [**IVssBackupComponents::SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore)angegeben.

-   Für Sicherungsunterkomponenten kann nicht ausgewählt werden, ohne dass ein für den Vorgänger der Sicherungskomponente auswählbar ist.

    Alle diese Komponenten müssen eingeschlossen werden, wenn Komponenten des Writers in den Vorgang einbezogen werden sollen. Die Einbeziehung dieser Dateien in Sicherungsvorgänge wird durch [**IVssBackupComponents::AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) und in Wiederherstellungsvorgängen von [**IVssBackupComponents::SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore)angegeben.

-   Komponenten, die der Sicherung implizit hinzugefügt werden [*(Unterkomponenten),*](vssgloss-s.md)die für die [*Wiederherstellung ausgewählt*](vssgloss-s.md) werden können und der Wiederherstellung explizit hinzugefügt werden.

    Diese Komponenten können entweder auswählbar oder nicht auswählbar sein, verfügen aber über einen auswählbaren Vorgänger, der verwendet wurde, um sie implizit für die Sicherung auszuwählen. Sie werden dem Sicherungskomponentendokument von [**IVssBackupComponents::AddRestoreSubcomponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent)hinzugefügt.

Die Identitäten von Komponenten, die implizit in der Wiederherstellung enthalten sind, werden nicht im Dokument sicherungskomponenten gespeichert.

VSS hat Zugriff auf Informationen zum Einbeziehen von Komponenten: Writer ohne Komponenten, die explizit in einer Wiederherstellung oder Sicherung enthalten sind, empfangen nach der Generierung der Ereignisse [*PrepareForBackup*](vssgloss-p.md) oder [*PreRestore*](vssgloss-p.md) keine VSS-Ereignisse.

Writer können diese Informationen nicht direkt abfragen. Dies ist keine wesentliche Einschränkung, da einzelne VSS-Writer entwurfsbedingt keine detaillierten Informationen über den Status anderer Writer im System benötigen sollten, und wie oben erwähnt, müssen diejenigen ohne enthaltene Komponenten nicht am VSS-Vorgang teilnehmen.

Ein Anforderer kann bestimmen, welche Komponenten explizit in einen Vorgang eingeschlossen wurden.

Die [**IVssBackupComponents::GetWriterComponentsCount-Methode**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponentscount) gibt die Anzahl der Writer mit Komponenteninformationen zurück, die im Sicherungskomponentendokument gespeichert sind (und nicht die Anzahl der Komponenten im Dokument).

Der Anforderer indiziert die gespeicherten Writerinformationen mithilfe von [**IVssBackupComponents::GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents), die Instanzen der [**IVssWriterComponentsExt-Schnittstelle**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext) zurückgibt. Die **IVssWriterComponentsExt-Schnittstelle** ermöglicht dem Anforderer, die [*Writer-Klasse*](vssgloss-w.md) und [*die Writerinstanz*](vssgloss-w.md) der beteiligten Writer abzurufen sowie auf Informationen zu den Komponenten zuzugreifen, die im Sicherungskomponentendokument gespeichert sind.

## <a name="information-on-included-components"></a>Informationen zu eingeschlossenen Komponenten

Die Darstellung der Komponentendaten im Sicherungskomponentendokument (die keine Pfad- und Dateispezifikationsinformationen enthält), auf die über Instanzen der [**IVssComponent-Schnittstelle**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) zugegriffen wird.

Anforderer und Writer erhalten auf unterschiedliche Weise Zugriff auf Instanzen der [**IVssComponent-Schnittstelle.**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent)

Ein Anforderer untersucht Komponentendaten auf Writer-Basis anhand von Instanzen der [**IVssWriterComponentsExt-Schnittstelle,**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext) die von [**IVssBackupComponents::GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents)zurückgegeben wird.

Zusätzlich zu den Writer-Identifikationsinformationen stellt die [**IVssWriterComponentsExt-Schnittstelle**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext) ein Array von Instanzen der [**IVssComponent-Schnittstelle**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) bereit – eine für jeden der ausgewählten enthaltenen Writerkomponenten.

Wie unter Lebenszyklus von [Sicherungskomponentendokumenten](backup-components-document-life-cycle.md)erwähnt, können die Writer über die [**IVssWriterComponents-Schnittstelle**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswritercomponents) zugriff auf dieselben Informationen erhalten, wenn sie das Ereignis PrepareForBackup, PrepareForSnapshot, PostSnapshot, BackupComplete, PreRestore oder PostRestore behandeln.

[**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) ermöglicht sowohl Writern als auch Anforderern das Abrufen der folgenden Informationen:

-   Name, Typ und [*logischer Pfad*](vssgloss-l.md) einer Komponente ([**GetComponentName**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getcomponentname), [**GetComponentType**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getcomponenttype), [**GetLogicalPath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getlogicalpath))
-   Wie eine Komponente wiederhergestellt werden soll, wie durch das [*Wiederherstellungsziel*](vssgloss-r.md) angegeben ([**IVssComponent::GetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoretarget))
-   Wenn beim Wiederherstellen einer Datei ein alternativer Speicherort verwendet wurde ([**GetAlternateLocationMapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmapping), [**GetAlternateLocationMappingCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmappingcount))
-   Neue Zielinformationen, sofern vorhanden ([**GetNewTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtarget), [**GetNewTargetCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtargetcount))
-   Fehlermeldungen vor und nach der Wiederherstellung ([**GetPreRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getprerestorefailuremsg), [**GetPostRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpostrestorefailuremsg))
-   Wenn für die Wiederherstellung ein [*für die Sicherungskomponente auswählbarer*](vssgloss-s.md) Ausgewählter ausgewählt wurde, der einen Komponentensatz definiert ([**IsSelectedForRestore**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-isselectedforrestore))
-   Gibt an, ob eine Sicherung oder Wiederherstellung erfolgreich war ([**GetBackupSucceeded,**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupsucceeded) [**GetFileRestoreStatus**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getfilerestorestatus))
-   Alle writerspezifischen Sicherungs- oder Wiederherstellungsoptionen, die möglicherweise von [**IVssBackupComponents::SetBackupOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupoptions) oder [**IVssBackupComponents::SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) ([**GetBackupOptions**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupoptions), [**GetRestoreOptions**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoreoptions)) festgelegt wurden
-   Alle writerspezifischen Metadatensicherungs- oder Wiederherstellungsmetadaten ([**GetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata)), [**GetRestoreMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoremetadata))
-   Zeitstempelinformationen ([**GetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupstamp), [**GetPreviousBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpreviousbackupstamp))
-   Informationen zu Sicherungsunterkomponenten, die explizit in einer Wiederherstellung enthalten sind ([**GetRestoreSubcomponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoresubcomponent), [**GetRestoreSubcomponentCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoresubcomponentcount))

Im Gegensatz zu Anforderern können Writer bestimmte Informationen im Sicherungskomponentendokument über die [**IVssComponent-Schnittstelle**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) ändern:

-   Wie eine Komponente wiederhergestellt werden soll, wie durch das Wiederherstellungsziel angegeben ([**IVssComponent::SetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoretarget))
-   Writer-spezifische Sicherungs- und Wiederherstellungsmetadaten ([**IVssComponent::SetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupmetadata), [**IVssComponent::SetRestoreMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoremetadata))
-   Zeitstempelinformationen ([**SetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp))
-   Fehlermeldungen vor und nach der Wiederherstellung ([**SetPreRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setprerestorefailuremsg), [**SetPostRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setpostrestorefailuremsg))

## <a name="requester-state-information"></a>Zustandsinformationen des Anfordernden

Anforderer fügen Informationen zum Status eines Sicherungs- oder Wiederherstellungsvorgangs mithilfe der [**IVssBackupComponents-Schnittstelle**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) in das Sicherungskomponentendokument ein. Writer-Anwendungen können diese Informationen über die [**CVssWriter-Klasse**](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriter) abfragen.

Im Sicherungskomponentendokument gespeicherte Zustandsinformationen umfassen Folgendes:

Allgemeine Informationen zur Sicherung

-   Der gesamte Sicherungstyp (inkrementell, differenziell oder vollständig)<dl> <dt>

Festlegung durch Anforderer mithilfe von [ **IVssBackupComponents::SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate)
</dt> <dt>

Von Writern mit [ **CVssWriter::GetBackupType** abgerufen](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getbackuptype)
</dt> </dl>
-   Whether component operations are supported<dl> <dt>

Festlegung durch Anforderer mithilfe von [ **IVssBackupComponents::SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate)
</dt> <dt>

Von Writern mit [ **CVssWriter::AreComponentsSelected abgerufen**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-arecomponentsselected)
</dt> </dl>
-   Whether the bootable system state is backed up<dl> <dt>

Festlegung durch Anforderer mithilfe von [ **IVssBackupComponents::SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate)
</dt> <dt>

Von Writern mit [ **CVssWriter::IsBootableStateBackedUp** abgerufen](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-isbootablesystemstatebackedup)
</dt> </dl>
-   Whether partial file operations are supported<dl> <dt>

Festlegung durch Anforderer mithilfe von [ **IVssBackupComponents::SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate)
</dt> <dt>

Von Writern mit [ **CVssWriter::IsPartialFileSupportEnabled** abgerufen](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-ispartialfilesupportenabled)
</dt> </dl>

Allgemeine Informationen zur Wiederherstellung

-   Der gesamte Wiederherstellungstyp (unabhängig davon, ob die Wiederherstellung per Kopier- oder Importvorgang erfolgt)<dl> <dt>

Festlegung durch Anforderer mithilfe von [ **IVssBackupComponents::SetRestoreState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestorestate)
</dt> <dt>

Von Writern mit [ **CVssWriter::GetRestoreType** abgerufen](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getrestoretype)
</dt> </dl>

Informationen zu unterstützenden Dateien

-   Der Speicherort von Dateien, die von einer bestimmten Komponente in Teildateivorgängen verwendet werden<dl> <dt>

Festlegung durch Anforderer mithilfe von [ **IVssBackupComponents::SetRangesFilePath**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrangesfilepath)
</dt> <dt>

Von Writern (oder Anforderern) mithilfe von [ **IVssComponent::GetPartialFile** abgerufen](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile)
</dt> </dl>

Status der Informationen

-   Geben Sie an, ob eine der Komponenten eines bestimmten Writers erfolgreich gesichert wurde.<dl> <dt>

Festlegung durch Anforderer mithilfe von [ **IVssBackupComponents::SetBackupSucceeded**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded)
</dt> <dt>

Von Writern und Anforderern mithilfe von [ **IVssComponent::GetBackupSucceeded abgerufen**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupsucceeded)
</dt> </dl>
-   Indicate whether one of a given writer's components was successfully restored<dl> <dt>

Festlegung durch Anforderer mithilfe von [ **IVssBackupComponents::SetFileRestoreStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setfilerestorestatus)
</dt> <dt>

Von Writern und Anfordernden mithilfe von [ **IVssComponent::GetFileRestoreStatus** abgerufen](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getfilerestorestatus)
</dt> </dl>

Writer-Settable Informationen

-   Zusätzliche Sicherungsspezifikation für eine der Komponenten eines bestimmten Writers<dl> <dt>

Festlegung durch Writer mithilfe von [ **IVssComponent::SetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupmetadata)
</dt> <dt>

Von Writern und Anforderern mithilfe von [ **IVssComponent::GetBackupMetadata** abgerufen](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata)
</dt> </dl>
-   Additional restore specification for one of a given writer's components<dl> <dt>

Festlegung durch Writer mithilfe von [ **IVssComponent::SetRestoreMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoremetadata)
</dt> <dt>

Von Writern und Anforderern mithilfe von [ **IVssComponent::GetRestoreMetadata** abgerufen](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoremetadata)
</dt> </dl>
-   A backup stamp that indicates, in a writer's own specific format, the time of the current backup of one of its component's backups<dl> <dt>

Festlegung durch Writer mithilfe von [ **IVssComponent::SetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp)
</dt> <dt>

Von Writern und Anforderern mithilfe von [ **IVssComponent::GetBackupStamp** abgerufen](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupstamp)
</dt> </dl>
-   A backup stamp that indicates, in a writer's own specific format, the time of the last backup of one of its components' backups using a backup stamp initially set by <a href="/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp">IVssComponent::SetBackupStamp</a><dl> <dt>

Gespeichert und von Anforderern für eine bestimmte Komponente mit [ **IVssBackupComponents::SetPreviousBackupStamp**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setpreviousbackupstamp)
</dt> <dt>

Von Writern und Anforderern mithilfe von [ **IVssComponent::GetPreviousBackupStamp** abgerufen](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpreviousbackupstamp)
</dt> </dl>
-   Error messages for failure before and after restore operations<dl> <dt>

Festlegung durch Writer mit [**IVssComponent::SetPreRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setprerestorefailuremsg) oder [**IVssComponent::SetPostRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setpostrestorefailuremsg)
</dt> <dt>

Von Writern und Anforderern mit [**IVssComponent::GetPreRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getprerestorefailuremsg) oder [**IVssComponent::GetPostRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpostrestorefailuremsg) abgerufen
</dt> </dl>

 

 
