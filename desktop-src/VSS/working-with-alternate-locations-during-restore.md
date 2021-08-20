---
description: Es gibt viele Gründe, warum ein Anfordernde Dateien von Sicherungsmedien an ihrem ursprünglichen Speicherort nicht wiederherstellen sollte oder nicht.
ms.assetid: 2a9cfd99-5a2c-4c0c-98ff-11c745298cda
title: Arbeiten mit alternativen Speicherorten während der Wiederherstellung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 907732c7b4b97668f1a317f9e03c3ea35bdec9618ff0e3e3c1a2f1e319eb19fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056148"
---
# <a name="working-with-alternate-locations-during-restore"></a>Arbeiten mit alternativen Speicherorten während der Wiederherstellung

Es gibt viele Gründe, warum ein Anfordernde Dateien von Sicherungsmedien an ihrem ursprünglichen Speicherort nicht wiederherstellen sollte oder nicht. Beispielsweise kann eine Wiederherstellungsmethode oder ein Wiederherstellungsziel eine solche Wiederherstellung erfordern, oder der aktuelle Wiederherstellungsort ist belegt und nicht beschreibbar.

Um solche Fälle zu behandeln, hat ein Writer möglicherweise eine alternative Speicherortzuordnung [*definiert,*](vssgloss-a.md)ein nicht standardmäßiges Wiederherstellungsziel, das für besondere Umstände verwendet werden soll.

Der Begriff alternative Standortzuordnung, wie er mit VSS verwendet wird, sollte nicht mit dem Begriff alternativer Pfad [*verwechselt werden.*](vssgloss-a.md) Alternative Speicherortzuordnungen werden nur bei Wiederherstellungsvorgängen verwendet und verweisen auf ein alternatives Ziel für Wiederherstellungsvorgänge. Alternative Pfade werden nur während Sicherungsvorgängen verwendet und verweisen auf eine alternative Quelle, aus der gesichert werden soll.

Um während der Wiederherstellung alternative Speicherortzuordnungen zu verwenden, würde ein An anfordernder Benutzer folgende Schritte (in der Regel nach der Generierung eines [**PreRestore-Ereignisses)**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) tun:

1.  Mithilfe einer Instanz der [**IVssExerklärwriterMetadata-Schnittstelle,**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) die durch Abrufen eines gespeicherten Writers abgerufen wird, verwendet ein Anmeldedienst die [**IVssExwordWriterMetadata::GetAlternateLocationMapping-Methode,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping) um die alternativen Speicherortzuordnungen eines Writers als Instanzen der [**IVssWMFiledesc-Schnittstelle**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) zu erhalten.

    > [!Note]  
    > Der Anfordernde verwendet [**IVssExumaWriterMetadata::GetAlternateLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping)und nicht [**IVssComponent::GetAlternateLocationMapping.**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmapping) Erstere gibt diese alternativen Standortzuordnungen zurück, die von einem Anfordernden verwendet werden können. Letzteres wird verwendet, um die alternativen Standortzuordnungen anzugeben, die tatsächlich von einem Anfordernden verwendet werden.

     

2.  Der Aufruf von [**IVssExwriterMetadata::GetAlternateLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping) gibt eine Instanz der [**IVssWMFiledesc-Schnittstelle**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) zurück. Diese Instanz enthält Dateisatzinformationen – einen pfad, der von [**IVssWMFiledesc::GetPath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getpath)angegeben wird, eine Dateispezifikation, die über [**IVssWMFiledesc::GetFilespec**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getfilespec)zurückgegeben wird, und ein Rekursionsflag, das von [**IVssWMFiledesc::GetRecursive**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getrecursive)ermittelt wurde – übereinstimmend. der Dateisätze, die (mithilfe von [**IVssCreateWriterMetadata::AddDatabaseFiles,**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles) [**IVssCreateWriterMetadata::AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)oder [**IVssCreateWriterMetadata::AddFilesToFileGroup)**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup)einer der vom Writer verwalteten Komponenten hinzugefügt wurden.

    Der von [**IVssWMFiledesc::GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) zurückgegebene Wert ist die alternative Speicherortzuordnung für diesen Dateisatz.

3.  Alternative Speicherortzuordnungen enthalten keine Komponenteninformationen. Daher müssen die Dateisatzinformationen (Pfad, Dateispezifikation und Rekursionsflag), die durch Aufrufen von [**IVssExwordWriterMetadata::GetAlternateLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping) ermittelt wurden, mit denen verglichen werden, die in den Komponenten des Writers enthalten sind.

    Diese Informationen finden Sie, indem Sie die Komponenten des Writers iterieren und [**IVssExwriterMetadata::GetComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getcomponent) aufrufen, um eine Instanz der [**IVssWMComponent-Schnittstelle**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) zu erhalten und [**IVssWMComponent::GetFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getfile) zu verwenden, um eine [**IVssWMFiledesc-Instanz**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) mit den Komponentendateisatzinformationen zu erhalten.

    Wenn die von der Instanz von [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) zurückgegebenen Dateisatzinformationen, die von [**IVssExwordWriterMetadata::GetComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getcomponent) und [**IVssWMComponent::GetFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getfile) ermittelt wurden, mit denen aus der **IVssWMFiledesc-Instanz,** die von [**IVssWMFiledesc::GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation)abgeleitet wurde, gefunden wurde, wurde die Komponente gefunden, die die Dateien mit der spezifischen alternativen Speicherortzuordnung verwalten.

4.  Nachdem die Komponente gefunden wurde, kann der Anfordernde die Bedingungen bestimmen, unter denen eine alternative Standortzuordnung verwendet werden soll, indem er folgende Schritte vorn hat:

    -   Untersuchen sie die Wiederherstellungsmethode der Komponente, die durch Aufrufen von [**IVssExoloWriterMetadata::GetRestoreMethod ermittelt wird.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getrestoremethod)
    -   Überprüfen Sie, ob ein Wiederherstellungsziel die Wiederherstellungsmethode überschreibt, indem [**Sie IVssComponent::GetRestoreTarget aufrufen.**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoretarget)

        Wenn die im Writer-Metadatendokument gefundene Komponente explizit [*in*](vssgloss-e.md) die Sicherung eingeschlossen wurde, entspricht die Instanz der [**IVssComponent-Schnittstelle**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) dieser Komponente. Wenn die Komponente implizit [*in*](vssgloss-i.md) die Sicherung eingeschlossen wurde, entspricht die Instanz von **IVssComponent** der Komponente, die den Komponentensatz definiert, dessen Komponente im Writer-Metadatendokument eine Unterkomponente ist.

5.  Mit diesen Informationen kann der Anfordernde komponentenweise bestimmen, ob er einen bestimmten Dateisatz einer bestimmten Komponente auf einem Ziel wiederherstellen muss, das durch die Zuordnung des alternativen Speicherorts definiert ist.

6.  Bei Verwendung einer alternativen Speicherortzuordnung beachtet der Anfordernde den Dateideskriptor und das rekursive Flag des Dateisets und verwendet den Pfad, der von der alternativen Speicherortzuordnung bereitgestellt wird.

    Der Anfordernde gibt an, dass er während eines Wiederherstellungsvorgang eine alternative Speicherortzuordnung verwendet hat, indem er [**IVssBackupComponents::AddAlternativeLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addalternativelocationmapping) mit den Standardspeicherortinformationen des Dateisets, dem verwendeten alternativen Wiederherstellungsziel und einem Komponentennamen aufruft.

    Wenn der Dateisatz von einer Komponente verwaltet wurde, die explizit in der Sicherung enthalten war, wird dieser Komponentenname verwendet. Wenn der Dateisatz von einer Komponente verwaltet wurde, die implizit in der Sicherung enthalten war, wird der Name der Komponente verwendet, die den Komponentensatz definiert, dessen Komponente, die den Dateisatz verwaltet, eine Unterkomponente ist.

Writer überprüfen durch Aufrufen von [**IVssComponent::GetAlternateLocationMapping,**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmapping)ob Dateisätze aus einer ihrer Komponenten an einer alternativen Speicherortzuordnung wiederhergestellt wurden.

 

 



