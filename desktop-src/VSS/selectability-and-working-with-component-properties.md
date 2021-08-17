---
description: Das Arbeiten mit implizit ausgewählten Komponenten erfordert Zugriff auf das Sicherungskomponentendokument und die WriterMetadatendokumente.
ms.assetid: ede51931-be50-4286-818b-0e6122247bdd
title: Auswählbarkeit und Arbeiten mit Komponenteneigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a735481d4bd0d7fdaa4102026b74ca78be947afbab24858d88d9210dd7bd4e6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117751652"
---
# <a name="selectability-and-working-with-component-properties"></a>Auswählbarkeit und Arbeiten mit Komponenteneigenschaften

Das Arbeiten mit implizit ausgewählten Komponenten erfordert Zugriff auf das Sicherungskomponentendokument und die WriterMetadatendokumente.

Hierfür gibt es zwei Gründe:

-   Die im Sicherungskomponentendokument gespeicherten Komponentendaten (dargestellt durch die [**IVssComponent-Schnittstelle)**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) haben keinen Zugriff auf Komponentendateisatzinformationen – Dateispezifikation, Pfad und Rekursionsflag. (Weitere Informationen finden Sie [unter Arbeiten mit dem Dokument "Sicherungskomponenten".)](working-with-the-backup-components-document.md)
-   Nur Komponenten, die während der Sicherung explizit im Sicherungskomponentendokument [*enthalten*](vssgloss-e.md) sind, haben ihre Informationen direkt im Sicherungskomponentendokument gespeichert. Anforderer und Writer müssen die über die [**IVssComponent-Schnittstelle verfügbaren**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) Informationen in Verbindung mit [*logischen Pfadinformationen*](vssgloss-l.md) und WriterMetadatendokumenten verwenden, um Informationen zu [*implizit eingeschlossenen*](vssgloss-i.md) Komponenten abzurufen und Deren Eigenschaften festzulegen.

Der unter [Logisches Pfading von Komponenten beschriebene](logical-pathing-of-components.md) Fall "MyWriter" kann verwendet werden, um die Auswählbarkeit für die Sicherung zu veranschaulichen.



| Komponentenname | Logischer Pfad            | Für die Sicherung auswählbar | Für die Wiederherstellung auswählbar | Explizit eingeschlossen |
|----------------|-------------------------|-----------------------|------------------------|---------------------|
| "Ausführbare Dateien"  | ""                      | N                     | N                      | J                   |
| "ConfigFiles"  | "Ausführbare Dateien"           | N                     | N                      | J                   |
| "LicenseInfo"  | ""                      | J                     | N                      | J                   |
| "Security"     | ""                      | J                     | N                      | J                   |
| "UserInfo"     | "Security"              | N                     | N                      | N                   |
| "Zertifikate" | "Security"              | N                     | N                      | N                   |
| "writerData"   | ""                      | J                     | J                      | J                   |
| "Set1"         | "writerData"            | N                     | J                      | N                   |
| "Jan"          | "writerData \\ Set1"      | N                     | N                      | N                   |
| "Dec"          | "writerData \\ Set1"      | N                     | N                      | N                   |
| "Set2"         | "writerData"            | N                     | J                      | N                   |
| "Jan"          | "writerData \\ Set2"      | N                     | N                      | N                   |
| "Dec"          | "writerData \\ Set2"      | N                     | N                      | N                   |
| "Abfrage"        | "writerData \\ QueryLogs" | N                     | N                      | N                   |
| "Nutzung"        | "writerData"            | J                     | J                      | N                   |
| "Jan"          | "writerData \\ Usage"     | N                     | N                      | N                   |
| "Dec"          | "writerData \\ Usage"     | N                     | N                      | N                   |



 

## <a name="implicitly-included-components-in-the-backup-set"></a>Implizit eingeschlossene Komponenten im Sicherungssatz

Beim Überprüfen des Writer-Metadatendokuments eines Writers (siehe [**IVssBackupComponents::GetWriterMetadata)**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata)während der Sicherung sollte ein Anforderer eine Liste aller Komponenten, ihrer [*logischen Pfade*](vssgloss-l.md)und ihrer Dateisatzinformationen speichern.

Dateisatz- und ausgeschlossene Dateiinformationen werden benötigt, um eine Liste von Dateien für jede (explizit oder implizit) enthaltene Komponente zu bestimmen.

Bei Sicherungskomponenten, die für Sicherungskomponenten nicht auswählbar und für Sicherungskomponenten, die keinen [*Komponentensatz*](vssgloss-c.md)definieren, auswählbar sind, werden nur Dateisatz- und ausgeschlossene Dateiinformationen benötigt, um alle Kandidaten der Komponente für die Sicherung zu identifizieren, da diese Komponenten keine Unterkomponenten definieren.

Für explizit eingeschlossene, für Sicherungskomponenten auswählbare Komponenten, die einen Komponentensatz definieren, müssen die Dateisätze und Dateiinformationen sowohl für die definierende Komponente als auch alle [*Unterkomponenten*](vssgloss-s.md) verwendet werden, um Dateien für die Sicherung auszuwählen.

Dies bedeutet, dass Sicherungssätze für die Komponenten "Executables", "ConfigFiles" und "LicenseInfo" nur gefunden werden können, indem die Writer-Metadaten nur für diese Komponenten mit ihren Instanzen der [**IVssWMComponent-Schnittstelle**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) untersucht werden.

Wenn writerData jedoch explizit in der Sicherung enthalten ist, müssen Sie die Instanz der [**IVssWMComponent-Schnittstelle**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) und die Instanzen für "Set1" überprüfen. "Jan" (mit logischem Pfad "writerData \\ Set1"), "Dec" (mit logischem Pfad "writerData \\ Set1"), "Set2", "Jan" (mit logischem Pfad "writerData \\ Set2"), "Dec" (mit logischem Pfad "writerData \\ Set2"), "Query", "Usage", "Jan" (mit logischem Pfad "writerData \\ Usage") und "Dec" (mit logischem Pfad "writerData \\ Usage").

Hierzu muss ein Anforderer zunächst identifizieren, dass die Komponente "writerData" (logischer Pfad "") auswählbar ist. Anschließend müssen alle anderen vom Writer verwalteten Komponenten überprüft werden, um zu bestimmen, ob das erste Element in ihrem logischen Pfad "writerData" ist. Die Komponenten, die "writerData" als führende Member ihres logischen Pfads aufweisen, werden als Unterkomponenten von "writerData" identifiziert und implizit ausgewählt, wenn sie explizit ausgewählt werden.

Tatsächlich muss eine ähnliche Überprüfung durchgeführt werden, um zu bestimmen, dass keine Komponente "LicenseInfo" als führendes Element ihres logischen Pfads hat und daher "LicenseInfo" über keine Unterkomponenten verfügt.

Aufgrund der Komplexität dieses Mechanismus in VSS kann es für viele Anfordernde Writer nützlich sein, eigene Strukturen zum Speichern von Komponenten- und Sicherungssatzinformationen für explizite und implizit hinzugefügte Komponenten zu erstellen.

## <a name="properties-of-implicitly-included-components"></a>Eigenschaften implizit eingeschlossener Komponenten

Bei Wiederherstellungs- und Sicherungsvorgängen werden Instanzen der [**Schnittstellen IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) und [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) sowohl zum Abrufen von Informationen über Komponenten als auch zum Festlegen oder Ändern von Komponenteneigenschaften verwendet. Allerdings verfügen nur explizit enthaltene Komponenten über Instanzen der **IVssComponent-Schnittstelle** oder sind für die **IVssBackupComponents-Schnittstelle** zugänglich.

Einige Eigenschaften sind komponentenweit im Bereich festgelegt. Diese Eigenschaften umfassen Folgendes:

-   Sicherungs- und Wiederherstellungsstatus: <dl>

[**IVssBackupComponents::SetBackupSucceeded**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded)  
    [**IVssComponent::GetBackupSucceeded**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupsucceeded)  
    [**IVssBackupComponents::SetFileRestoreStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setfilerestorestatus)  
    [**IVssComponent::GetFileRestoreStatus**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getfilerestorestatus)  
    </dl>
-   Sicherungs- und Wiederherstellungsoptionen: <dl>

[**IVssBackupComponents::SetBackupOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupoptions)  
    [**IVssComponent::GetBackupOptions**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupoptions)  
    [**IVssBackupComponents::SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions)  
    [**IVssComponent::GetRestoreOptions**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoreoptions)  
    </dl>
-   Fehlermeldungen: <dl>

[**IVssComponent::SetPostRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setpostrestorefailuremsg)  
    [**IVssComponent::SetPreRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setprerestorefailuremsg)  
    [**IVssComponent::SetPostRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setpostrestorefailuremsg)  
    [**IVssComponent::SetPreRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setprerestorefailuremsg)  
    </dl>
-   Wiederherstellungsziele: <dl>

[**IVssComponent::SetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoretarget)  
    [**IVssComponent::GetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoretarget)  
    </dl>
-   Sicherungsstempel: <dl>

[**IVssComponent::SetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp)  
    [**IVssComponent::GetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupstamp)  
    </dl>
-   Zusätzliche Metadaten: <dl>

[**IVssComponent::SetRestoreMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoremetadata)  
    [**IVssComponent::GetRestoreMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoremetadata)  
    [**IVssComponent::SetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupmetadata)  
    [**IVssComponent::GetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata)  
    </dl>

Daher verwenden Sie die Instanz der [**IVssComponent-Schnittstelle**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) des definierenden Members einer Komponentengruppe oder den Namen, typ und logischen Pfad des definierenden Members mit einer [**IVssBackupComponents-Methode,**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) um Eigenschaften für alle Member der Komponentengruppe festzulegen oder abzurufen.

Aus diesem Grund werden Komponentensätze als Einheiten behandelt. Beispielsweise ist eine Sicherung eines Komponentensatzes nur erfolgreich, wenn die Sicherung aller Dateisätze aller komponenten erfolgreich ist.

Nehmen wir im vorherigen Beispiel an, dass eine Datei in der Komponente "Jan" (mit dem logischen Pfad "writerData \\ Set2") ein Member der durch "writerData" definierten Komponentenmenge ist. Wenn eine der Dateien von "Jan" nicht gesichert werden konnte, verwendet ein Anforderer beim Festlegen von [**IVssBackupComponents::SetBackupSucceeded**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded) mit **false** die Informationen von "writerData" als Argumente, um den Fehler des Komponentensatzes anzugeben.

Auf ähnliche Weise gilt der von [**IVssComponent::GetBackupSucceededed**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupsucceeded) für die Instanz von "writerData" der [**IVssComponent-Schnittstelle**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) zurückgegebene Zustand nicht nur für "writerData", sondern auch für alle zugehörigen Unterkomponenten.

Wenn ein Writer das Wiederherstellungsziel mithilfe von [**IVssComponent::SetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoretarget) der Instanz von "writerData" von [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent)geändert hat, würde dies das Wiederherstellungsziel für alle Dateisätze aller Unterkomponenten von "writerData" ändern.

Die folgenden Eigenschaften gelten nicht komponentenweit, sondern für bestimmte Dateien oder Dateisätze:

-   Alternative Standortzuordnungen: <dl>

[**IVssBackupComponents::AddAlternativeLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addalternativelocationmapping)  
    [**IVssComponent::GetAlternateLocationMapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmapping)  
    [**IVssComponent::GetAlternateLocationMappingCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmappingcount)  
    </dl>
-   Differenzierte Dateien: <dl>

[**IVssComponent::AddDifferencedFilesByLastModifyTime**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime)  
    [**IVssComponent::GetDifferencedFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfile)  
    [**IVssComponent::GetDifferencedFilesCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfilescount)  
    </dl>
-   Teildateien: <dl>

[**IVssComponent::AddPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile)  
    [**IVssComponent::GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile)  
    [**IVssComponent::GetPartialFileCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfilecount)  
    </dl>
-   Gerichtete Ziele: <dl>

[**IVssComponent::AddDirectedTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddirectedtarget)  
    [**IVssComponent::GetDirectedTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdirectedtarget)  
    [**IVssComponent::GetDirectedTargetCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdirectedtargetcount)  
    </dl>
-   Neue Ziele: <dl>

[**IVssBackupComponents::AddNewTarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget)  
    [**IVssComponent::GetNewTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtarget)  
    [**IVssComponent::GetNewTargetCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtargetcount)  
    </dl>

Wenn ein Anforderer über die [**IVssBackupComponents-Schnittstelle**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) auf diese Features für eine Unterkomponente zugreift, verwendet er die Komponenteninformationen für die definierende Komponente des Komponentensatzes, aber die Datei- oder Dateisatzinformationen für die Unterkomponente.

Wenn auf die Eigenschaft über die [**IVssComponent-Schnittstelle**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) zugegriffen werden kann, wird auch die -Instanz verwendet, die der definierenden Unterkomponente entspricht, aber die Datei- oder Dateisatzargumente werden aus der Unterkomponente übernommen.

Angenommen, die Unterkomponente "Jan" (mit dem logischen Pfad "writerData \\ Set2") hat eine Datei mit dem Pfad "c: \\ fred", der Dateispezifikation \* ".dat" und dem rekursiven Flag **true** muss möglicherweise an einem alternativen Speicherort wiederhergestellt werden.

Wenn dies der Fall wäre, würde ein Anforderer [**IVssBackupComponents::AddAlternativeLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addalternativelocationmapping)aufrufen, wobei er die Informationen von "writerData" (Komponententyp, den Komponentennamen "writeData" und den logischen Pfad "") zusammen mit den Dateisatzinformationen von "Jan" (Pfad "c: \\ fly", Dateispezifikation \* ".dat" und Rekursion gleich **TRUE)** verwendet.

Beachten Sie, dass in diesem Fall die Dateisatzinformationen genau mit den Dateisatzinformationen übereinstimmen müssen, die von [**IVssCreateWriterMetadata::AddFilesToFileGroup,**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup) [**IVssCreateWriterMetadata::AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)oder [**IVssCreateWriterMetadata::AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) verwendet werden, um Dateien zu Jan hinzuzufügen.

Wenn ein Writer einer Datei mit dem Pfad "c: \\ ethel" und dem Von "Jan" verwalteten Namen "lucy.dat" (mit dem logischen Pfad "writerData Set2") ein gerichtetes Ziel hinzufügen \\ möchte, würde er die [**IVssComponent-Instanz**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) verwenden, die "writerData" entspricht, aber die Dateiinformationen von "Jan".

## <a name="implicitly-included-components-in-the-restore-set"></a>Implizit eingeschlossene Komponenten im Wiederherstellungssatz

Komponenten, die implizit in eine Sicherung eingeschlossen wurden, können explizit in eine Wiederherstellung eingeschlossen werden, wenn sie für die Wiederherstellung ausgewählt werden können. Wie unter [Working with Selectability for Restore and Subcomponents (Arbeiten mit Der Auswählbarkeit für Wiederherstellung und Unterkomponenten)](working-with-selectability-for-restore-and-subcomponents.md)erwähnt, werden diese Komponenten dem Dokument sicherungskomponenten mithilfe der [**IVssBackupComponents::AddRestoreSubcomponent-Methode**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent) hinzugefügt.

Dadurch wird jedoch weder eine neue Instanz der [**IVssComponent-Schnittstelle**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) erstellt, noch kann auf die Komponente direkt über die [**IVssBackupComponents-Schnittstelle**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) zugegriffen werden.

Stattdessen muss auf eine Komponente, die explizit für die Wiederherstellung, aber implizit für die Sicherung eingeschlossen ist, über eine Instanz der [**IVssComponent-Schnittstelle**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) zugegriffen werden, die der Komponente entspricht, die den Komponentensatz definiert hat, dessen Member sie bei der Sicherung war.

Wenn Sie beispielsweise explizit für die Wiederherstellung von "Set1" einschließen möchten, eine Unterkomponente der für die Sicherungskomponente "writerData" auswählbaren Komponente, rufen Sie die [**IVssComponent::GetRestoreSubcomponent-Methode**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoresubcomponent) der Instanz der [**IVssComponent-Schnittstelle**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) von "writerData" auf.

 

 



