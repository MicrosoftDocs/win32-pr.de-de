---
description: 'Nach dem Aufrufen von IVssBackupComponents:: gatherwritermetadata verwendet eine anfordernde Person die Instanz der IVssAsync-Schnittstelle, die von diesem Aufruf zurückgegeben wird, um zu bestimmen, wann alle Writer im System die Erstellung Ihrer Writer-Metadatendokumente abgeschlossen haben.'
ms.assetid: 04658d50-04f0-4189-8b88-ff152f1bf482
title: Übersicht über die Sicherungs Ermittlungs Phase
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d2d2a2d05220ecf3e25c77c18cc62b07726964f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106351625"
---
# <a name="overview-of-the-backup-discovery-phase"></a>Übersicht über die Sicherungs Ermittlungs Phase

Nach dem Aufrufen von [**IVssBackupComponents:: gatherwritermetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata)verwendet eine anfordernde Person die Instanz der [**IVssAsync**](/windows/desktop/api/Vss/nn-vss-ivssasync) -Schnittstelle, die von diesem Aufruf zurückgegeben wird, um zu bestimmen, wann alle Writer im System die Erstellung Ihrer Writer-Metadatendokumente abgeschlossen haben. Weitere Informationen finden Sie [unter Übersicht über die Verarbeitung einer Sicherung unter VSS](overview-of-processing-a-backup-under-vss.md).

An diesem Punkt kann der Anforderer eine Ermittlungsphase starten und die Metadaten überprüfen, um zu bestimmen, welche Anwendungen ausgeführt werden und welche Volumes mit Schatten Kopien kopiert werden müssen, um eine komplette Sicherung zu erhalten. In der folgenden Tabelle wird die Abfolge der Aktionen und Ereignisse angezeigt, die für die Sicherungs Ermittlungsphase erforderlich sind.



| Requestaktion                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | Ereignis | Writer-Aktion                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|-----------------------------------------------------------------------------------|
| Abrufen von Writer-Metadatendokumenten (siehe [**IVssBackupComponents:: getschreitermetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata), [**ivssexaminewrite Metadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata)).                                                                                                                                                                                                                                                                                                                                                 | Keine  | Während dieses Zeitraums können Writer mit ihren normalen Vorgängen fortfahren. |
| Verwenden Sie die Liste der Komponenten und der zugehörigen [*Datei Sätze*](vssgloss-f.md)sowie ausgeschlossene Dateien, um eine Liste der an der Sicherung beteiligten Volumes und Dateien zu erhalten (siehe [**ivsswmcomponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent), [**ivsswmfiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc)).                                                                                                                                                                                                                                                                      | Keine  | Keine                                                                              |
| Wählen Sie aus, welche Komponenten im Writer-Metadatendokument für die Sicherungskopie ausgewählt werden sollen. Nennen Sie [**IVssBackupComponents:: addComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) für jede Komponente, um Sie dem Dokument mit den Sicherungs Komponenten hinzuzufügen. (Weitere Informationen finden Sie unter [Arbeiten mit selectlichkeit für die Sicherung](working-with-selectability-for-backup.md) und [Arbeiten mit dem Sicherungs Komponenten Dokument](working-with-the-backup-components-document.md).)                                                                                                                      | Keine  | Keine                                                                              |
| Initialisieren Sie den Schattenkopiesatz, den Kontext und die Überprüfung auf unterstützte Volumes (siehe [**IVssBackupComponents:: startnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset), [**IVssBackupComponents:: isvolumesupportiert**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-isvolumesupported)).                                                                                                                                                                                                                                                                                   | Keine  | Keine                                                                              |
| Wenn Sie eine Sicherung außerhalb der Komponenten durchführen, fügen Sie die gewünschten Zielvolumes aus dem Writer-Metadatendokument dem Schattenkopiesatz hinzu, indem Sie [**IVssBackupComponents:: addtosnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset) für jedes Volume aufrufen. Andernfalls muss die anfordernde Person für die Komponenten im Writer-Metadatendokument, die bereits zum Sicherungs Komponenten Dokument hinzugefügt wurden (durch Aufrufen von [**addComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent)), auch **IVssBackupComponents:: addtosnapshotset** für jedes betroffene Volume aufrufen. | Keine  | Keine                                                                              |



 

## <a name="writer-actions-during-the-discovery-phase"></a>Writer-Aktionen während der Ermittlungs Phase

Da es sich bei der Ermittlungsphase einer Sicherung hauptsächlich um eine anfordernde Person handelt, die die aus Writer-Metadatendokumenten abgerufenen Informationen verarbeitet, gibt es nur wenige Anforderungen an einen Writer.

Theoretisch kann ein Writer an dieser Stelle weiterhin normal ausgeführt werden. Es kann jedoch wünschenswert sein, dass Writer Vorbereitungen für die bevorstehenden schattenkopievorgänge und Sicherungs Vorgänge beginnen.

## <a name="requester-actions-during-the-discovery-phase"></a>Requestaktionen während der Ermittlungs Phase

Ein Anforderer verwendet die [**ivssexaminewritermetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) -Objekte, die über [**IVssBackupComponents:: getwritermetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata) abgerufen wurden, um alle Writer-Metadaten zu durchlaufen und die Writer auszuwählen, deren Daten gesichert werden sollen.

An diesem Punkt muss die anfordernde Person eine anfängliche Liste der Sicherungs Kandidaten jedes Writers generieren, indem die Writer-Komponenten mithilfe von [**ivssexamineschreitermetadata:: getComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getcomponent)durchlaufen werden. Dadurch wird der Anforderer mit [**ivsswmcomponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) -Objekten bereitgestellt, über die Sie die Spezifikationen für die zu sichernden Dateien mithilfe von [**ivsswmcomponent:: GetFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getfile), [**ivsswmcomponent:: getdatabasefile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabasefile)und [**ivsswmcomponent:: getdatabaselogfile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabaselogfile)erhalten können.

Da das [**ivsswmfiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) -Objekt Platzhalter Zeichen verwenden kann, um Datei Speicherort Informationen zu speichern, kann es erforderlich sein, Funktionen wie " [**FindFirstFile**](/windows/win32/api/fileapi/nf-fileapi-findfirstfilea)", " [**findfirstfileex**](/windows/win32/api/fileapi/nf-fileapi-findfirstfileexa)" und " [**FindNextFile**](/windows/win32/api/fileapi/nf-fileapi-findnextfilea)" zu verwenden.

Bis die Schatten Kopie abgeschlossen ist, können Writer im normalen Verlauf der Arbeit weiterhin Dateien auf dem Datenträger hinzufügen oder daraus entfernen. Daher sollten Sie die tatsächliche Liste der zu sichernden Dateien nicht generieren.

Stattdessen wird die anfängliche Liste der zu sichernden Dateien und Volumes zu diesem Zeitpunkt wie folgt gefunden:

1.  Untersuchen aller auswählbaren für Sicherungs-und nicht auswählbaren Komponenten in den Writer-Metadatendokumenten der einzelnen Writer (mithilfe von [**ivssexaminewrite Metadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata)) und organisieren in Komponenten [*Gruppen*](vssgloss-c.md) verwenden den [*logischen Pfad*](vssgloss-l.md) (Weitere Informationen finden Sie [unter Arbeiten mit Auswahlmöglichkeiten und logischen Pfaden](working-with-selectability-and-logical-paths.md))
2.  [*Einschließen explizit*](vssgloss-e.md) aller erforderlichen Komponenten (nicht auswählbar für Sicherungs Komponenten ohne auswählbare für Sicherungs Vorgänger) im Dokument mit den Sicherungs Komponenten mithilfe von [ **IVssBackupComponents:: addComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent)
3.  Explizites einschließen Optionaler auswählbarer für Sicherungs Komponenten, die keine Komponenten Sätze definieren (mithilfe von [**IVssBackupComponents:: addComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent))
4.  Auswählen von [*Komponenten Sätzen*](vssgloss-c.md) für die Teilnahme an einer Sicherung durch explizites Hinzufügen Ihrer definierenden auswählbaren for Backup-Komponente (mithilfe von [**IVssBackupComponents:: addComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent)), die implizit die [*unter Komponenten*](vssgloss-s.md)des Komponenten Satzes [*einschließt*](vssgloss-i.md) .
5.  Durch die Verwendung von [*Datei Satz*](vssgloss-f.md) Informationen im Writer-Metadatendokument und in den Volumen Verwaltungsfunktionen der ausgewählten Writer bestimmt ein Anforderer die Pfade der zu sichernden Dateien und die Volumes, die als Schatten kopiert werden müssen.

Beachten Sie, dass nur die Komponenten, die in der Sicherung und im Sicherungs Komponenten Dokument explizit (mithilfe von [**IVssBackupComponents:: addComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent)) enthalten sind, dem Dokument Instanzen der [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) -Schnittstelle hinzugefügt werden. Diese Instanzen werden zum Überprüfen und Ändern von Komponenten Einstellungen sowohl für explizit enthaltene Komponenten als auch für deren implizit enthaltene unter Komponenten verwendet (siehe [selectlichkeit und arbeiten mit Komponenteneigenschaften](selectability-and-working-with-component-properties.md)).

Wenn ein Writer eine der Komponenten eines Writers enthält, muss er alle erforderlichen Komponenten hinzufügen. Ein Anforderer kann jedoch auch vollständig alle Komponenten Sätze eines Writers überspringen. Wenn keine der Komponenten eines Writers explizit ausgewählt ist, wird der Writer nicht ausgewählt, und VSS hindert den Writer daran, an dem Rest des Sicherungs Vorgangs teilzunehmen.

Der Anforderer initiiert den Schattenkopiesatz, der die ausgewählten Volumes enthält, indem [**IVssBackupComponents:: startnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset)aufgerufen wird.

Wenn das Volume an einer Schatten Kopie teilnehmen kann (die mit [**IVssBackupComponents:: isvolumesupportiert**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-isvolumesupported)werden kann), kann der Anforderer dieses Volume mithilfe von [**IVssBackupComponents:: addtosnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset)dem Schattenkopiesatz hinzufügen.

Obwohl es in der Regel nicht sinnvoll ist, kann ein Anforderer manchmal auch auswählen, welcher [*Anbieter*](vssgloss-p.md) die Schatten Kopie für ein bestimmtes Volume beibehält (Weitere Informationen finden Sie unter [Auswählen von Anbietern](selecting-providers.md) ).

Der Umgang mit einem Volume, das eingebundene Ordner oder Analyse Punkte enthält, sollte Vorsicht geboten werden. Ein bereitgestellter Ordner oder Analyse Punkt kann in einer Schatten Kopie angezeigt werden und kann gesichert werden. Ein bereitgestellter Ordner oder Analyse Punkt kann jedoch nicht auf dem schattenkopierten Volume durchsucht werden (siehe [Arbeiten mit bereitgestellten Ordnern und Analyse Punkten](working-with-reparse-and-mount-points.md)).

An dieser Stelle der Sicherung wird das Dokument mit den Sicherungs Komponenten initialisiert und ausgefüllt. In zukünftigen Vorgängen können Writer und Anforderer die [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) -Schnittstelle verwenden, um miteinander zu kommunizieren.

Writer erhalten bei der Behandlung von [*PrepareForBackup*](vssgloss-p.md)-, [*PostSnapshot*](vssgloss-p.md)-und [*BackupComplete*](vssgloss-b.md) -Ereignissen Zugriff auf die [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) -Schnittstelle.

 

 
