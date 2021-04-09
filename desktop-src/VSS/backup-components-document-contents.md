---
description: Das Dokument mit den Sicherungs Komponenten wird von Instanzen der IVssBackupComponents-Schnittstelle verwaltet.
ms.assetid: 8c7ebba8-58c4-4733-ba59-802abf902c5e
title: Dokumentinhalte der Sicherungs Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e12c88ebffa0037702e1f30dd818d4fd23fe4e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868771"
---
# <a name="backup-components-document-contents"></a>Dokumentinhalte der Sicherungs Komponenten

Das Dokument mit den Sicherungs Komponenten wird von Instanzen der [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) -Schnittstelle verwaltet. Diese Schnittstelle enthält auch zahlreiche Methoden zum Steuern von Sicherungs Vorgängen, zum Bearbeiten von Schatten Kopien und zum Abfragen des Systemstatus. Allerdings sind nicht alle Dokument Informationen direkt über diese Schnittstelle zugänglich.

Das Dokument mit den Sicherungs Komponenten besteht aus mehreren Datensätzen:

-   Informationen zu den Komponenten, die explizit in einem Sicherungs-oder Wiederherstellungs Vorgang enthalten waren
-   Eine Darstellung der gespeicherten Komponenten-und Writer-Informationen
-   Zustandsinformationen zum Sicherungs-/Wiederherstellungs Vorgang

Obwohl die Komponenten Informationen sowohl für den Anforderer als auch für den Writer verfügbar sind, hat nur der Writer Zugriff auf die Statusinformationen.

## <a name="component-inclusion-information"></a>Informationen zur Komponenten Einbindung

Das Dokument mit den Sicherungs Komponenten enthält eine Liste der Komponenten, die von der anfordernden Person explizit in die Sicherung und Wiederherstellung eingeschlossen werden. Die Liste enthält Folgendes:

-   Explizit [*einwählbare Komponenten*](vssgloss-s.md).

    Die Aufnahme dieser Dateien in Sicherungs Vorgänge wird durch [**IVssBackupComponents:: addComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) und in Restore- [**Vorgängen durch IVssBackupComponents:: setselectedforrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore)angegeben.

-   Nicht auswählbar für Sicherungs Subkomponenten ohne auswählbare für Sicherungs Komponenten Vorgänger.

    Alle diese Komponenten müssen eingeschlossen werden, wenn alle Komponenten des Writers in den Vorgang eingeschlossen werden sollen. Die Aufnahme dieser Dateien in Sicherungs Vorgänge wird durch [**IVssBackupComponents:: addComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) und in Restore- [**Vorgängen durch IVssBackupComponents:: setselectedforrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore)angegeben.

-   Komponenten, die der Sicherung ([*unter Komponenten*](vssgloss-s.md)) implizit hinzugefügt wurden und [*für die Wiederherstellung ausgewählt*](vssgloss-s.md) sind und der Wiederherstellung explizit hinzugefügt werden.

    Diese Komponenten können wählbar oder nicht auswählbar sein, Sie verfügen jedoch über einen auswählbaren Vorgänger, der verwendet wurde, um Sie implizit für die Sicherung auszuwählen. Sie werden dem Dokument mit den Sicherungs Komponenten von [**IVssBackupComponents:: adressstoresubcomponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent)hinzugefügt.

Die Identitäten von Komponenten, die implizit in die Wiederherstellung einbezogen werden, werden nicht im Dokument mit den Sicherungs Komponenten gespeichert.

VSS hat Zugriff auf Informationen zur Einbindung von Komponenten: Writer ohne explizit in eine Wiederherstellung oder eine Sicherung enthaltene Komponenten empfangen keine VSS-Ereignisse nach der Generierung der [*PrepareForBackup*](vssgloss-p.md) -oder [*vorab*](vssgloss-p.md) Version-Ereignisse.

Writer können diese Informationen nicht direkt abfragen. Dies ist keine wesentliche Einschränkung, da einzelne VSS-Writer Entwurfs bedingt keine detaillierten Informationen über den Status anderer Writer auf dem System benötigen. wie bereits erwähnt, müssen diejenigen ohne enthaltene Komponenten nicht an dem VSS-Vorgang teilnehmen.

Ein Anforderer kann ermitteln, welche Komponenten explizit in einen Vorgang eingeschlossen wurden.

Die [**IVssBackupComponents:: getwritercomponentscount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponentscount) -Methode gibt die Anzahl der Writer mit Komponenten Informationen zurück, die im Dokument mit den Sicherungs Komponenten gespeichert sind (und nicht die Anzahl der Komponenten im Dokument).

Der Anforderer indiziert durch die gespeicherten Writer-Informationen mithilfe von [**IVssBackupComponents:: getschreitercomponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents), der Instanzen der [**ivssschreitercomponentlxt**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext) -Schnittstelle zurückgibt. Die **ivsswritercomponentlxt** -Schnittstelle ermöglicht es der anfordernden Person, die [*Writer-Klasse*](vssgloss-w.md) und die [*Writer-Instanz*](vssgloss-w.md) der beteiligten Writer abzurufen und auf Informationen über die im Sicherungs Komponenten Dokument gespeicherten Komponenten zuzugreifen.

## <a name="information-on-included-components"></a>Informationen zu enthaltenen Komponenten

Die Darstellung der Komponenten Daten in der Sicherungs Komponenten (die keine Informationen zu Pfad-und Datei Spezifikationen enthalten), auf die über Instanzen der [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) -Schnittstelle zugegriffen wird.

Anforderer und Writer erhalten auf unterschiedliche Weise Zugriff auf Instanzen der [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) -Schnittstelle.

Ein Anforderer überprüft die Komponenten Daten eines Writers von Writer, indem er Instanzen der von [**IVssBackupComponents:: getschreitercomponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents)zurückgegebenen [**ivssschreitercomponentlxt**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext) -Schnittstelle verwendet.

Zusätzlich zu den Writer-Identifikationsinformationen stellt die [**ivsswritercomponentlxt**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext) -Schnittstelle ein Array von Instanzen der [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) -Schnittstelle bereit – eines für jeden der ausgewählten Writer, die Komponenten enthalten.

Wie bereits im [Dokument Lebenszyklus der Sicherungs Komponenten](backup-components-document-life-cycle.md)erwähnt, können die Writer [**bei der Verarbeitung**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswritercomponents) von PrepareForBackup, prepareforsnapshot, PostSnapshot, BackupComplete, PreRestore oder postrestore-Ereignis auf die gleichen Informationen zugreifen.

[**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) ermöglicht es Writer und Anforderern, die folgenden Informationen zu erhalten:

-   Name, Typ und [*logischer Pfad*](vssgloss-l.md) einer Komponente ([**GetComponentName**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getcomponentname), [**getcomponenttype**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getcomponenttype), [**getlogicalpath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getlogicalpath))
-   Wie eine Komponente wieder hergestellt werden soll, wie durch das [*Wiederherstellungs Ziel*](vssgloss-r.md) angegeben ([**IVssComponent:: getrestoretarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoretarget))
-   Wenn ein alternativer Speicherort zum Wiederherstellen einer Datei verwendet wurde ([**getalternatelocationmapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmapping), [**getalternatelocationmappingcount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmappingcount))
-   Neue Ziel Informationen, sofern vorhanden ([**getnewtarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtarget), [**getnewtargetcount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtargetcount))
-   Fehlermeldungen vor und nach der Wiederherstellung ([**getprerestorefailuremsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getprerestorefailuremsg), [**getpostrestorefailuremsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpostrestorefailuremsg))
-   Wenn eine [*auswählbare for Backup*](vssgloss-s.md) -Komponente, die einen Komponenten Satz definiert, für die Wiederherstellung ausgewählt wurde ([**isselectedforrestore**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-isselectedforrestore))
-   Ob eine Sicherung oder Wiederherstellung erfolgreich war ([**getbackupwar**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupsucceeded), [**getfilerestorestatus**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getfilerestorestatus))
-   Alle Writer-spezifischen Sicherungs-oder Wiederherstellungsoptionen, die möglicherweise von [**IVssBackupComponents:: setbackupoptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupoptions) oder [**IVssBackupComponents:: setrestoreoptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) ([**getbackupoptions**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupoptions), [**getrestoreoptions**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoreoptions)) festgelegt wurden.
-   Alle Writer-spezifischen Metadaten zum Sichern oder Wiederherstellen von Metadaten ([**getbackupmetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata)), [**getrestoremetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoremetadata))
-   Zeitstempel Informationen ([**getbackupstamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupstamp), [**getpreviousbackupstamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpreviousbackupstamp))
-   Informationen zu Sicherungs Subkomponenten, die explizit in einer Wiederherstellung enthalten sind ([**getrestoresubcomponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoresubcomponent), [**getrestoresubcomponentcount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoresubcomponentcount))

Anders als bei Anforderern können Writer bestimmte Informationen im Dokument mit den Sicherungs Komponenten über die [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) -Schnittstelle ändern:

-   Wie eine Komponente wieder hergestellt werden soll, wie vom Wiederherstellungs Ziel angegeben ([**IVssComponent:: abtrestoretarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoretarget))
-   Writer-spezifische Sicherungs-und Wiederherstellungs Metadaten ([**IVssComponent:: setbackupmetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupmetadata), [**IVssComponent:: setrestoremetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoremetadata))
-   Zeitstempel Informationen ([**setbackupstamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp))
-   Fehlermeldungen vor und nach der Wiederherstellung ([**setprerestorefailuremsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setprerestorefailuremsg), [**setpostrestorefailuremsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setpostrestorefailuremsg))

## <a name="requester-state-information"></a>Zustandsinformationen des Anforderers

Anforderer fügt Informationen über den Status eines Sicherungs-oder Wiederherstellungs Vorgangs mithilfe der [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) -Schnittstelle in das Dokument mit den Sicherungs Komponenten ein. Writer-Anwendungen können diese Informationen über die [**CVssWriter**](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriter) -Klasse Abfragen.

Die im Dokument mit den Sicherungs Komponenten gespeicherten Zustandsinformationen umfassen Folgendes:

Allgemeine Informationen zur Sicherung

-   Der Gesamt Sicherungstyp (inkrementell, Differenziell oder vollständig)<dl> <dt>

Wird von Anforderern mithilfe von [ **IVssBackupComponents:: SetBackupState** festgelegt.](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate)
</dt> <dt>

Von Writern mithilfe von [ **CVssWriter:: getbackuptype** abgerufen](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getbackuptype)
</dt> </dl>
-   Whether component operations are supported<dl> <dt>

Wird von Anforderern mithilfe von [ **IVssBackupComponents:: SetBackupState** festgelegt.](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate)
</dt> <dt>

Von Writern mithilfe von [ **CVssWriter:: arecomponentssgewählt** abgerufen](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-arecomponentsselected)
</dt> </dl>
-   Whether the bootable system state is backed up<dl> <dt>

Wird von Anforderern mithilfe von [ **IVssBackupComponents:: SetBackupState** festgelegt.](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate)
</dt> <dt>

Von Writern mithilfe von [ **CVssWriter:: isbootablestatebackedup** abgerufen](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-isbootablesystemstatebackedup)
</dt> </dl>
-   Whether partial file operations are supported<dl> <dt>

Wird von Anforderern mithilfe von [ **IVssBackupComponents:: SetBackupState** festgelegt.](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate)
</dt> <dt>

Von Writern mithilfe von [ **CVssWriter:: ispartialfilesupportenabled** abgerufen](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-ispartialfilesupportenabled)
</dt> </dl>

Allgemeine Informationen zur Wiederherstellung

-   Der Gesamt Wiederherstellungstyp (unabhängig davon, ob Restore durch Kopieren oder importieren erfolgt)<dl> <dt>

Festlegen durch requestals mithilfe von [ **IVssBackupComponents:: setrestorestate**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestorestate)
</dt> <dt>

Von Writern mithilfe von [ **CVssWriter:: getrestoretype** abgerufen](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getrestoretype)
</dt> </dl>

Informationen zu unterstützenden Dateien

-   Der Speicherort der Bereichs Dateien, die von einer bestimmten Komponente in partiellen Datei Vorgängen verwendet werden<dl> <dt>

Von Anforderern mithilfe von [ **IVssBackupComponents:: setrangesfilepath** festgelegt](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrangesfilepath)
</dt> <dt>

Abgerufen von Writern (oder Anforderern) mithilfe von [ **IVssComponent:: GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile)
</dt> </dl>

Status der Informationen

-   Geben Sie an, ob eine der Komponenten eines bestimmten Writers erfolgreich gesichert wurde.<dl> <dt>

Von Anforderern mithilfe von [ **IVssBackupComponents:: setbackupwar** festgelegt](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded)
</dt> <dt>

Wird von Writern und Anforderern mithilfe von [ **IVssComponent:: getbackupwar** abgerufen.](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupsucceeded)
</dt> </dl>
-   Indicate whether one of a given writer's components was successfully restored<dl> <dt>

Festlegen durch [ **anfordernde Personen mit IVssBackupComponents:: setfilerestorestatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setfilerestorestatus)
</dt> <dt>

Von Writern und Anforderer mithilfe von [ **IVssComponent:: getfilerestorestatus** abgerufen](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getfilerestorestatus)
</dt> </dl>

Writer-Settable Informationen

-   Zusätzliche Sicherungs Spezifikation für eine der Komponenten eines bestimmten Writers<dl> <dt>

Festlegung durch Writer mithilfe von [ **IVssComponent:: setbackupmetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupmetadata)
</dt> <dt>

Wird von Writern und Anforderern mithilfe von [ **IVssComponent:: getbackupmetadata** abgerufen.](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata)
</dt> </dl>
-   Additional restore specification for one of a given writer's components<dl> <dt>

Festlegung durch Writer mithilfe von [ **IVssComponent:: setrestoremetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoremetadata)
</dt> <dt>

Von Writern und Anforderern mithilfe von [ **IVssComponent:: getrestoremetadata** abgerufen](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoremetadata)
</dt> </dl>
-   A backup stamp that indicates, in a writer's own specific format, the time of the current backup of one of its component's backups<dl> <dt>

Festlegung durch Writer mithilfe von [ **IVssComponent:: setbackupstamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp)
</dt> <dt>

Wird von Writern und Anforderern mithilfe von [ **IVssComponent:: getbackupstamp** abgerufen.](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupstamp)
</dt> </dl>
-   A backup stamp that indicates, in a writer's own specific format, the time of the last backup of one of its components' backups using a backup stamp initially set by <a href="/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp">IVssComponent:: setbackupstamp</a><dl> <dt>

Wird von Anforderern für eine bestimmte Komponente mithilfe von [ **IVssBackupComponents:: setpreviousbackupstamp** gespeichert und festgelegt.](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setpreviousbackupstamp)
</dt> <dt>

Wird von Writern und Anforderern mithilfe von [ **IVssComponent:: getpreviousbackupstamp** abgerufen.](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpreviousbackupstamp)
</dt> </dl>
-   Error messages for failure before and after restore operations<dl> <dt>

Wird von Writern mithilfe von [**IVssComponent:: setprerestorefailuremsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setprerestorefailuremsg) oder [**IVssComponent:: setpostrestorefailuremsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setpostrestorefailuremsg) festgelegt.
</dt> <dt>

Wird von Writern und Anforderern mithilfe von [**IVssComponent:: getprerestorefailuremsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getprerestorefailuremsg) oder [**IVssComponent:: getpostrestorefailuremsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpostrestorefailuremsg) abgerufen.
</dt> </dl>

 

 
