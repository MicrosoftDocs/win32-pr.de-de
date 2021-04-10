---
description: Zum Arbeiten mit implizit ausgewählten Komponenten ist sowohl der Zugriff auf das Dokument mit den Sicherungs Komponenten als auch auf das Schreiben von Dokumenten erforderlich
ms.assetid: ede51931-be50-4286-818b-0e6122247bdd
title: Selekabilität und arbeiten mit Komponenteneigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83d06683bafb02802d84f152f1ceb662eb7491f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131257"
---
# <a name="selectability-and-working-with-component-properties"></a>Selekabilität und arbeiten mit Komponenteneigenschaften

Zum Arbeiten mit implizit ausgewählten Komponenten ist sowohl der Zugriff auf das Dokument mit den Sicherungs Komponenten als auch auf das Schreiben von Dokumenten erforderlich

Hierfür gibt es zwei Gründe:

-   Die Komponenten Daten, die im Dokument mit den Sicherungs Komponenten (dargestellt durch die [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) -Schnittstelle) gespeichert werden, haben keinen Zugriff auf Komponenten Datei Satz Informationen – Datei Angabe, Pfad und Rekursions Flag. (Weitere Informationen finden Sie [unter Arbeiten mit dem Sicherungs Komponenten Dokument](working-with-the-backup-components-document.md).)
-   Nur Komponenten, die während der Sicherung explizit im Sicherungs Komponenten Dokument [*enthalten*](vssgloss-e.md) sind, werden direkt im Dokument mit den Sicherungs Komponenten gespeichert. Anforderer und Writer müssen die Informationen, die über die [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) -Schnittstelle verfügbar sind, zusammen mit [*logischen Pfad*](vssgloss-l.md) Informationen und Writer-Metadatendokumenten verwenden, um Informationen zu erhalten und die Eigenschaften von [*implizit*](vssgloss-i.md) eingeschlossenen Komponenten festzulegen.

Der Fall "myWriter", der in [logischen Komponenten von Komponenten](logical-pathing-of-components.md) erläutert wird, kann verwendet werden, um die Auswahlmöglichkeiten für die Sicherung zu veranschaulichen.



| Komponentenname | Logischer Pfad            | Für Sicherung auswählbar | Zur Wiederherstellung ausgewählt | Explizit eingeschlossen |
|----------------|-------------------------|-----------------------|------------------------|---------------------|
| Ausführbare Dateien  | ""                      | N                     | N                      | J                   |
| "Configfiles"  | Ausführbare Dateien           | N                     | N                      | J                   |
| "Licenseingefo"  | ""                      | J                     | N                      | J                   |
| "Security"     | ""                      | J                     | N                      | J                   |
| UserInfo     | "Security"              | N                     | N                      | N                   |
| Abschluss | "Security"              | N                     | N                      | N                   |
| "beschreibdaten"   | ""                      | J                     | J                      | J                   |
| Set1         | "beschreibdaten"            | N                     | J                      | N                   |
| Jan          | "Schreibdaten \\ set1"      | N                     | N                      | N                   |
| 31.12.2012          | "Schreibdaten \\ set1"      | N                     | N                      | N                   |
| Set2         | "beschreibdaten"            | N                     | J                      | N                   |
| Jan          | "Schreibdaten \\ set2"      | N                     | N                      | N                   |
| 31.12.2012          | "Schreibdaten \\ set2"      | N                     | N                      | N                   |
| Such        | "Write Data \\ querylogs" | N                     | N                      | N                   |
| Ungs        | "beschreibdaten"            | J                     | J                      | N                   |
| Jan          | "Verwendung von" Schreib Daten \\ "     | N                     | N                      | N                   |
| 31.12.2012          | "Verwendung von" Schreib Daten \\ "     | N                     | N                      | N                   |



 

## <a name="implicitly-included-components-in-the-backup-set"></a>Implizit enthaltene Komponenten in den Sicherungs Satz

Bei der Untersuchung eines Writer-Metadatendokuments (siehe [**IVssBackupComponents:: getschreitermetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata)) während der Sicherung sollte ein Anforderer eine Liste aller Komponenten, der [*logischen Pfade*](vssgloss-l.md)und der zugehörigen Datei Satz Informationen speichern.

Informationen zu Datei Satz und ausgeschlossenen Dateien sind erforderlich, um eine Liste der Dateien für jede (explizit oder implizit) enthaltene Komponente zu ermitteln.

Für nicht auswählbare Sicherungs Komponenten ohne auswählbare Sicherungs-und auswählbare Sicherungs Komponenten, die keinen [*Komponenten Satz*](vssgloss-c.md)definieren, werden nur Datei Satz-und ausgeschlossene Dateiinformationen benötigt, um alle Kandidaten für die Sicherung zu identifizieren, da diese Komponenten keine unter Komponenten definieren.

Um explizit für Sicherungs Komponenten ausgewählt zu werden, die einen Komponenten Satz definieren, legt die Dateiinformationen sowohl für die definierende Komponente als auch für alle [*unter Komponenten*](vssgloss-s.md) fest, die zum Auswählen von Dateien für die Sicherung verwendet werden müssen.

Dies bedeutet, dass Sicherungs Sätze für die Komponenten "Executables", "configfiles" und "LicenseInfo" nur gefunden werden können, indem die Writer-Metadaten nur für diese Komponenten mithilfe ihrer Instanzen der [**ivsswmcomponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) -Schnittstelle überprüft werden.

Wenn "Write Data" jedoch explizit in der Sicherung enthalten ist, müssen Sie die zugehörige Instanz der [**ivsswmcomponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) -Schnittstelle und die für "set1", "Jan" (mit dem logischen Pfad "schreiterdata \\ set1"), "Dec" (mit dem logischen Pfad "beschreiterdaten set1") "untersuchen. \\ set2", "Jan" (mit dem logischen Pfad "Write Data \\ set2"), "Dec" (mit dem logischen Pfad "beschreiterdaten \\ set2"), "Query", "Usage", "Jan" (mit dem logischen Pfad "Schreib Daten \\ Verwendung") und "Dec" (mit dem logischen Pfad "Schreib Daten \\ Verwendung").

Zu diesem Zweck muss eine anfordernde Person zunächst feststellen, dass die Komponente "Write Data" (logischer Pfad "") ausgewählt werden kann. Anschließend muss er alle anderen vom Writer verwalteten Komponenten scannen, um zu bestimmen, ob das erste Element im logischen Pfad "Schreib Daten" ist. Die Komponenten, die "Write Data" als führende Member Ihres logischen Pfades aufweisen, werden als unter Komponenten von "beschreiterdaten" identifiziert und werden implizit ausgewählt, wenn Sie explizit ausgewählt werden.

Tatsächlich muss eine ähnliche Überprüfung durchgeführt werden, um zu bestimmen, dass keine Komponente "LicenseInfo" als führender Member Ihres logischen Pfads aufweist und dass "LicenseInfo" keine unter Komponenten aufweist.

Aufgrund der Komplexität dieses Mechanismus in VSS finden viele Anforderer Writer möglicherweise die Möglichkeit, eigene Strukturen zum Speichern von Komponenten-und Sicherungs Satz Informationen für explizit und implizit hinzugefügte Komponenten zu erstellen.

## <a name="properties-of-implicitly-included-components"></a>Eigenschaften von implizit enthaltenen Komponenten

Während der Wiederherstellungs-und Sicherungs Vorgänge werden Instanzen der [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) -Schnittstelle und der [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) -Schnittstelle verwendet, um Informationen zu Komponenten abzurufen und Komponenteneigenschaften festzulegen oder zu ändern. Allerdings verfügen nur Komponenten, die explizit eingeschlossen werden, über Instanzen der **IVssComponent** -Schnittstelle oder über die **IVssBackupComponents** -Schnittstelle.

Einige Eigenschaften sind im Gültigkeitsbereich Komponenten Satz weit. Diese Eigenschaften umfassen Folgendes:

-   Sicherungs-und Wiederherstellungs Status: <dl>

[**IVssBackupComponents:: setbackupwar**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded)  
    [**IVssComponent:: getbackupwar**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupsucceeded)  
    [**IVssBackupComponents:: setfilerestorestatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setfilerestorestatus)  
    [**IVssComponent:: getfilerestorestatus**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getfilerestorestatus)  
    </dl>
-   Sicherungs-und Wiederherstellungsoptionen: <dl>

[**IVssBackupComponents:: setbackupoptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupoptions)  
    [**IVssComponent:: getbackupoptions**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupoptions)  
    [**IVssBackupComponents:: abtrestoreoptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions)  
    [**IVssComponent:: getrestoreoptions**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoreoptions)  
    </dl>
-   Fehlermeldungen: <dl>

[**IVssComponent:: setpostrestorefailuremsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setpostrestorefailuremsg)  
    [**IVssComponent:: setprerestorefailuremsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setprerestorefailuremsg)  
    [**IVssComponent:: setpostrestorefailuremsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setpostrestorefailuremsg)  
    [**IVssComponent:: setprerestorefailuremsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setprerestorefailuremsg)  
    </dl>
-   Wiederherstellungs Ziele: <dl>

[**IVssComponent:: abtrestoretarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoretarget)  
    [**IVssComponent:: getrestoretarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoretarget)  
    </dl>
-   Sicherungs Stempel: <dl>

[**IVssComponent:: setbackupstamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp)  
    [**IVssComponent:: getbackupstamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupstamp)  
    </dl>
-   Zusätzliche Metadaten: <dl>

[**IVssComponent:: abtrestoremetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoremetadata)  
    [**IVssComponent:: getrestoremetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoremetadata)  
    [**IVssComponent:: setbackupmetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupmetadata)  
    [**IVssComponent:: getbackupmetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata)  
    </dl>

Daher verwenden Sie die Instanz der [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) -Schnittstelle des definierenden Members eines Komponentensets, oder verwenden Sie den Namen, den Typ und den logischen Pfad des definierenden Members mit einer [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) -Methode, um Eigenschaften für alle Member des Komponenten Satzes festzulegen oder abzurufen.

Aus diesem Grund werden Komponenten Sätze als Einheiten behandelt. Beispielsweise ist eine Sicherung eines Komponenten Satzes nur erfolgreich, wenn die Sicherung aller Datei Sätze aller zugehörigen Komponenten erfolgreich ist.

Im vorherigen Beispiel wird angenommen, dass eine Datei in der Komponente "Jan" (mit dem logischen Pfad "Write Data \\ set2") ein Member des durch "Write Data" definierten Komponenten Satzes ist. Wenn eine der Dateien des "Jan"-Datentyps nicht gesichert werden konnte, verwendet eine anfordernde Person beim Festlegen von [**IVssBackupComponents:: setbackupall**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded) mit **false** die Informationen von "Write Data" (der Name "schreiterdata", den Pfad "" und den Komponententyp) als Argumente, um den Fehler des Komponenten Satzes anzugeben.

Ebenso gilt der von [**IVssComponent:: getbackupwar**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupsucceeded) für die Instanz der [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) -Schnittstelle zurückgegebene Status nicht nur für "Write Data", sondern auch für alle seine unter Komponenten.

Wenn ein Writer das Wiederherstellungs Ziel mithilfe von [**IVssComponent:: setrestoretarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoretarget) der "schreiterdata"-Instanz von [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent)geändert hat, ändert sich außerdem das Wiederherstellungs Ziel für alle Datei Sätze aller "beschreiterdata"-unter Komponenten.

Die folgenden Eigenschaften gelten nicht für Komponenten, sondern für bestimmte Dateien oder Dateigruppen:

-   Alternativen Speicherort Zuordnungen: <dl>

[**IVssBackupComponents:: addalternativelocationmapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addalternativelocationmapping)  
    [**IVssComponent:: getalternatelocationmapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmapping)  
    [**IVssComponent:: getalternatelocationmappingcount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmappingcount)  
    </dl>
-   Differenzierte Dateien: <dl>

[**IVssComponent:: AddDifferencedFilesByLastModifyTime**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime)  
    [**IVssComponent:: getdifferencedfile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfile)  
    [**IVssComponent:: getdifferencedfilescount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfilescount)  
    </dl>
-   Partielle Dateien: <dl>

[**IVssComponent:: addpartialfile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile)  
    [**IVssComponent:: GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile)  
    [**IVssComponent:: GetPartialFileCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfilecount)  
    </dl>
-   Gesteuerte Ziele: <dl>

[**IVssComponent:: adddirectedtarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddirectedtarget)  
    [**IVssComponent:: getdirectedtarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdirectedtarget)  
    [**IVssComponent:: getdirectedtargetcount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdirectedtargetcount)  
    </dl>
-   Neue Ziele: <dl>

[**IVssBackupComponents:: addnewtarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget)  
    [**IVssComponent:: getnewtarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtarget)  
    [**IVssComponent:: getnewtargetcount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtargetcount)  
    </dl>

Wenn ein Anforderer mithilfe der [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) -Schnittstelle auf diese Funktionen für eine Unterkomponente zugreift, verwendet er die Komponenten Informationen für die definierende Komponente des Komponenten Satzes, aber die Datei-oder Datei Satz Informationen für die Unterkomponente.

Ebenso gilt: Wenn auf die Eigenschaft über die [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) -Schnittstelle zugegriffen werden kann, wird die Instanz verwendet, die der definierenden Unterkomponente entspricht, aber die Datei-oder Datei Satz Argumente werden von der Unterkomponente entnommen.

Nehmen wir beispielsweise an, dass für die Teilkomponente "Jan" (mit dem logischen Pfad "Beschreibungsdaten \\ set2") ein Dateisatz mit dem Pfad "c: \\ Fred", die Datei Spezifikation " \* . dat" und das rekursive Flag **true** an einem alternativen Speicherort wieder hergestellt werden müssen.

Wenn dies der Fall wäre, würde ein Anforderer [**IVssBackupComponents:: addalternativelocationmapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addalternativelocationmapping). dabei werden die Informationen zu "beschreibenden Daten" (Komponententyp, Komponenten Name "beschreibenden Daten" und der logische Pfad "") zusammen mit den Datei Satz Informationen von "Jan" (Pfad "c: \\ Fred", Datei Spezifikation " \* . dat" und Rekursion gleich " **true**") verwendet.

Beachten Sie, dass die Datei Satz Informationen in diesem Fall genau mit den Datei Satz Informationen übereinstimmen müssen, die von [**ivsskreateschreitermetadata:: addfilestofilegroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup), [**ivsskreateschreitermetadata:: adddatabasefiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)oder [**ivsskreateschreitermetadata:: adddatabaselogfiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) zum Hinzufügen von Dateien zu Jan verwendet werden

Ebenso gilt: Wenn ein Writer ein gerichtetes Ziel zu einer Datei mit dem Pfad "c: \\ Ethel" und dem Namen "Lucy. dat", die von "Jan" verwaltet wird (mit dem logischen Pfad "beschreiterdata \\ set2"), verwenden würde, würde er die [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) -Instanz verwenden, die "Write Data" entspricht, aber die Dateiinformationen von "Jan"

## <a name="implicitly-included-components-in-the-restore-set"></a>Implizit enthaltene Komponenten in den Wiederherstellungs Satz

Komponenten, die implizit in einer Sicherung enthalten waren, können explizit in eine Wiederherstellung eingeschlossen werden, wenn Sie für die Wiederherstellung ausgewählt werden können. Wie bereits in [Arbeiten mit selektselabilität für Wiederherstellung und unter Komponenten](working-with-selectability-for-restore-and-subcomponents.md)erläutert, werden diese Komponenten dem Dokument mit den Sicherungs Komponenten mithilfe der [**IVssBackupComponents:: adressstoresubcomponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent) -Methode hinzugefügt.

Dadurch wird jedoch keine neue Instanz der [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) -Schnittstelle erstellt, und die Komponente ist nicht direkt über die [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) -Schnittstelle zugänglich.

Stattdessen muss eine Komponente, die explizit für die Wiederherstellung eingeschlossen ist, aber implizit für die Sicherung eingeschlossen wird, über eine Instanz der [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) -Schnittstelle aufgerufen werden, die der Komponente entspricht, von der der Komponenten Satz definiert wurde, von dem Sie bei der Sicherung Mitglied war.

Wenn Sie z. b. explizit for Restore "set1" einschließen möchten, eine Unterkomponente der auswählbaren for Backup-Komponente "beschreiterdata", erhalten Sie Informationen dazu, indem Sie die [**IVssComponent:: getrestoresubcomponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoresubcomponent) -Methode der Instanz "" von "beschreiterdata" der [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) -Schnittstelle aufrufen.

 

 



