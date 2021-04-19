---
description: Der testwriter ist ein Hilfsprogramm, das Sie zum Testen von VSS-Anforderer-Anwendungen verwenden können.
ms.assetid: 02434cb9-390c-4cf0-9941-b833ace55685
title: VSS-testwriter-Tool
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61ffdbb513697a701866be5ceeb40168e8c28368
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359842"
---
# <a name="vss-test-writer-tool"></a>VSS-testwriter-Tool

Der testwriter ist ein Hilfsprogramm, das Sie zum Testen von VSS-Anforderer-Anwendungen verwenden können. Dieser Writer kann so konfiguriert werden, dass er fast alle Aktionen durchführt, die von einem VSS Writer durchgeführt werden können. Außerdem führt der testwriter umfassende Prüfungen durch, um sicherzustellen, dass die anfordernde Person diese Writer-Aktionen ordnungsgemäß verarbeitet hat.

Jede Instanz des Writers wird mit einer XML-Konfigurationsdatei initialisiert, die genau beschreibt, welche Komponenten der Writer meldet und wie sich der Writer verhält. Der Writer kann so konfiguriert werden, dass er über verschiedene Arten von Szenarien berichtet, einschließlich komplizierterer Szenarien mithilfe der inkrementellen und differenziellen Schnittstellen. Der Writer führt während des Prozesses Überprüfungen an verschiedenen Punkten durch, um sicherzustellen, dass sich der Anforderer ordnungsgemäß verhält. Nachdem die Wiederherstellung abgeschlossen ist, überprüft der Writer, ob alle erforderlichen Dateien ohne Beschädigung wieder hergestellt wurden. Der Writer kann auch konfiguriert werden, um andere Vorgänge auszuführen, z. b. fehlerhafte Ereignisse.

> [!Note]  
> Dieses Tool ist im Microsoft Windows Software Development Kit (SDK) für Windows Vista und höher enthalten. Sie können die Windows SDK von herunterladen [https://msdn.microsoft.com/windowsvista](https://msdn.microsoft.com/windows/default.aspx) .

 

In der Windows SDK-Installation befindet sich das Tool vsssampleprovider in `%Program Files(x86)%\Windows Kits\8.1\bin\x64` (für 64-Bit-Windows) und `%Program Files(x86)%\Windows Kits\8.1\bin\x86` .

## <a name="running-the-test-writer-tool"></a>Ausführen des testwriter-Tools

Um den testwriter zu starten, geben Sie Folgendes an der Eingabeaufforderung ein:

**vswriter.exe** *config-Datei*

Dabei ist *config-file* der Pfad zu einer Konfigurationsdatei, die das Verhalten dieses Writers angibt.

Drücken Sie STRG + C, um den testwriter anzuhalten.

Mehrere Instanzen des testwriters können gleichzeitig ausgeführt werden. Jede Instanz des Writers meldet jedoch dieselbe Writer-Klassen-ID (aber eine andere Writer-Instanz-ID), sodass logische Pfade und Komponentennamen für alle gleichzeitig auszulaufenden Instanzen des Writers eindeutig sein müssen.

Um sicherzustellen, dass der Writer ordnungsgemäß überprüfen kann, ob der Anforderer die Spezifikationen der Ausschluss Datei berücksichtigt hat, sollten alle Dateien, die gesichert wurden, aus dem ursprünglichen Volume gelöscht werden, bevor versucht wird, Sie wiederherzustellen. Es wird empfohlen, dass eine Vorlage für jedes Writer-Szenario gespeichert wird, damit das Szenario leicht neu erstellt werden kann.

## <a name="using-a-configuration-file"></a>Verwenden einer Konfigurationsdatei

Die folgende Beispielkonfigurationsdatei, vswriter \_ -config.xml, finden Sie unter `%ProgramFiles%\Microsoft SDKs\Windows\v7.0\bin\vsstools` auf x86-Plattformen und `%ProgramFiles%\Microsoft SDKs\Windows\v7.0\bin\x64\vsstools` auf x64-Plattformen.

``` syntax
<TestWriter usage="USER_DATA">

    <RestoreMethod method="RESTORE_IF_CAN_BE_REPLACED"
                   writerRestore="always"
                   rebootRequired="no" />

    <ExcludeFile path="c:\writerData\notTheseFiles" 
                 filespec="excludeThisFile.txt" 
                 recursive="no"/>

    <Component componentType="filegroup"
               componentName="TestFiles">
        <ComponentFile path="c:\writerData\myFilesHere" 
                       filespec="*"
                       recursive="no" />
    </Component>

</TestWriter>
```

Das Stamm Element in dieser Konfigurationsdatei hat den Namen testwriter. Alle anderen Elemente werden unter dem testwriter-Element angeordnet.

Eines der Attribute, das testwriter zugeordnet ist, ist das Usage-Attribut. Dieses Attribut gibt den Verwendungstyp an, der über [**ivssexamineschreibmetadata:: GetIdentity**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getidentity)gemeldet wird. Einer der möglichen Werte für dieses Attribut sind Benutzer \_ Daten.

Das erste untergeordnete Element des Root-Elements muss immer ein restoremethod-Element sein. Dieses Element gibt Folgendes an:

-   Die Restore-Methode (in diesem Fall Restore \_ , \_ Wenn \_ ersetzt werden kann \_ )
-   Gibt an, ob der Writer Wiederherstellungs Ereignisse erfordert (in diesem Fall immer).
-   Gibt an, ob ein Neustart erforderlich ist, nachdem der Writer wieder hergestellt wurde (in diesem Fall Nein).

Dieses Element kann optional eine Zuordnung alternativer Orte angeben. (In diesem Fall wird kein alternativer Speicherort angegeben.)

Das zweite untergeordnete Element ist ein EXCLUDEFILE-Element. Dieses Element bewirkt, dass der Writer eine Datei oder einen Satz von Dateien aus einer Sicherung ausschließt.

Das dritte untergeordnete Element ist ein Komponenten Element. Dieses Element bewirkt, dass der Writer seinen Metadaten eine Komponente hinzufügt. Ein Component-Element enthält Attribute, mit denen die Komponente und die untergeordneten Elemente beschrieben werden, um den Inhalt der Komponente zu beschreiben, wie z. b. Folgendes:

-   componentType, um anzugeben, ob es sich um eine Datei Gruppe oder eine Datenbank handelt
-   LogicalPath für den logischen Pfad der Komponente
-   componentname für den Namen der Komponente
-   auswählbar zum Angeben des Status für die auswählbare Sicherung

Das Component-Element weist auch ein untergeordnetes Element mit dem Namen "componentfile" auf, um dieser Komponente eine Datei Spezifikation hinzuzufügen. (Ein Komponenten Element kann eine beliebige Anzahl von componentfile-Elementen aufweisen, die für jede Komponente angegeben werden können.) Dieses componentfile-Element weist die folgenden Attribute auf:

-   Path = "c: \\ Schreibdaten \\ myfileshere"
-   file spec = " \* "
-   rekursiv = "Nein"

Obwohl der testwriter das requestverhalten überprüft, überprüft er nicht, ob die Konfigurationsdatei stets die dokumentierte Semantik für einen Writer verwaltet. Es gibt viele Vorgänge, die ein gut verhaltener Writer nicht ausführen sollte (z. b. die gleiche Datei in mehreren Komponenten melden), und es liegt an dem Autor der XML-Konfigurationsdatei, diese Semantik beizubehalten.

## <a name="configuring-writer-attributes"></a>Konfigurieren von Writer-Attributen

Das testwriter-Stamm Element enthält Attribute, die verschiedene Verhaltensweisen des Writers bestimmen. Einige der Verhaltensweisen, die geändert werden können, sind die folgenden:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Attribut</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="verbosity"></span><span id="VERBOSITY"></span>Ausführlichkeit<br/></td>
<td>Der Writer druckt den Status auf der Konsole, während er Ereignisse empfängt und verarbeitet. Die angezeigte ausführlichkeits Stufe wird durch das Ausführlichkeit-Attribut angegeben. Es gibt drei ausführlichkeits Grade, aus denen Sie auswählen können:<br/> <dl> <dt><span id="low"></span><span id="LOW"></span>Preis</dt> <dd> Nur Fehler im Writer oder falsches Verhalten der Anforderer werden gedruckt.<br/> </dd> <dt><span id="medium"></span><span id="MEDIUM"></span>Mittelalter</dt> <dd> Alle Elemente auf der Ebene mit niedriger Ausführlichkeit werden zusätzlich zu zusätzlichen Statusinformationen gedruckt, z. b. wenn Ereignisse empfangen werden. Dies ist der Standardebene.<br/> </dd> <dt><span id="high"></span><span id="HIGH"></span>hochrangiger</dt> <dd> Ausführliche Statusinformationen zum Vorgang des Writers werden gemeldet.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="deleteFiles"></span><span id="deletefiles"></span><span id="DELETEFILES"></span>DeleteFiles<br/></td>
<td>Wenn Sie eine zusätzliche Überprüfung ausführen möchten, legen Sie dieses Attribut auf Ja fest, damit &quot; &quot; der Writer alle seine Dateien sofort nach dem Erstellen der Volumeschattenkopie löscht. Der Anforderer muss dann die Dateien aus der Schatten Kopie kopieren, da Sie auf dem ursprünglichen Volume nicht mehr vorhanden sind. <br/>
<blockquote>
[!Note]<br />
Im Fall von spuckwritern werden die Dateien am ursprünglichen Speicherort nach dem Spit gelöscht, aber bevor die Schatten Kopie erstellt wird. Nachdem die Schatten Kopie erstellt wurde, werden die Dateien aus dem Verzeichnis "Spit" gelöscht.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="deletePartialFiles"></span><span id="deletepartialfiles"></span><span id="DELETEPARTIALFILES"></span>deletepartialfiles<br/></td>
<td>Zum Löschen von partiellen Dateien legen Sie dieses Attribut auf "Ja" fest &quot; &quot; .<br/></td>
</tr>
<tr class="even">
<td><span id="deleteDifferencedFiles"></span><span id="deletedifferencedfiles"></span><span id="DELETEDIFFERENCEDFILES"></span>deletedifferencedfiles<br/></td>
<td>Um differenzierte Dateien zu löschen, legen Sie dieses Attribut auf "Ja" fest &quot; &quot; .<br/></td>
</tr>
<tr class="odd">
<td><span id="checkIncludes"></span><span id="checkincludes"></span><span id="CHECKINCLUDES"></span>checkincludes<br/></td>
<td>Legen Sie dieses Attribut auf &quot; Ja fest &quot; , damit der Writer prüft, ob jede zu sichernde Datei an einem geeigneten Speicherort wieder hergestellt wurde und dass die Datei nicht beschädigt wurde. Teil Dateien und differenzierende Dateien werden ebenfalls ordnungsgemäß behandelt.<br/></td>
</tr>
<tr class="even">
<td><span id="checkExcludes"></span><span id="checkexcludes"></span><span id="CHECKEXCLUDES"></span>Check-Ausschlüsse<br/></td>
<td>Legen Sie dieses Attribut auf &quot; Ja fest &quot; , damit der Writer prüft, ob Dateien, die einer Datei Spezifikation in der Ausschlussliste entsprechen, nicht wieder hergestellt werden. Damit dies ordnungsgemäß funktioniert, müssen die Wiederherstellungs Verzeichnisse vor der Wiederherstellung geleert werden.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="specifying-alternate-location-mappings"></a>Angeben von alternativen Speicherort Zuordnungen

Eine Alternative Speicherort Zuordnung gibt einen Speicherort für die Wiederherstellung an, wenn die Wiederherstellungsmethode \_ \_ an einem \_ alternativen Speicherort wieder hergestellt wird \_ \_ oder wenn die normale Wiederherstellung einer Komponente fehlschlägt. Ein Writer kann seine alternativen Speicherort Zuordnungen mithilfe der [**ivssexaminewrite Metadata:: getalternatelocationmapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping) -Methode an den Anforderer melden. Sie können der Test-Writer-Konfigurationsdatei Alternative Speicherort Zuordnungen hinzufügen, indem Sie dem restoremethod-Element Alternative unter Elemente für die Zuordnung hinzufügen.

Das folgende restoremethod-Element enthält ein untergeordnetes Element von "Alternative".

``` syntax
<RestoreMethod method="RESTORE_IF_CAN_REPLACE"
              writerRestore="always"
              rebootRequired="no">
    <AlternateLocationMapping path="c:\files"
                              filespec="*.txt"
                              recursive="no"
                              alternatePath="c:\altfiles"/>
</RestoreMethod>
```

Dieses Beispiel gibt an, dass die anfordernde Person zuerst versuchen soll, alle Dateien, die mit "c: \\ Files. txt" übereinstimmen \\ \* , im Verzeichnis "c: Files" wiederherzustellen \\ . Wenn eine dieser Dateien nicht ersetzt werden kann, sollte der Anforderer stattdessen alle Dateien im Verzeichnis "c: altfiles" Wiederherstellen \\ . Der Anforderer sollte diese Alternative Speicherort Zuordnung mithilfe der [**IVssBackupComponents:: addalternativelocationmapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addalternativelocationmapping) -Methode speichern. Wenn der testwriter so konfiguriert ist, dass er überprüft, ob Dateien wieder hergestellt wurden, überprüft er auch, ob der Anforderer **addalternativelocationmapping** aufgerufen hat.

## <a name="specifying-files-to-be-excluded"></a>Angeben von auszuschließenden Dateien

Jeder Writer kann eine Liste mit Datei Spezifikationen angeben, die Dateien angeben, die der Anforderer von der Sicherung ausschließen soll. Sie können diese Datei Spezifikationen der Test-Writer-Konfigurationsdatei hinzufügen, indem Sie dem testwriter-Stamm Element die unter Elemente "EXCLUDEFILE" hinzufügen.

Im folgenden finden Sie ein Beispiel für ein EXCLUDEFILE-Unterelement, das alle Dateien im Verzeichnis "c: Files" ausschließt \\ , die mit "c: Temp" identisch sind. \\ \* \*

``` syntax
    <ExcludeFile path="c:\files" 
                 filespec="temp*.*" 
                 recursive="no"/>
```

## <a name="backing-up-spit-writers"></a>Sichern von spuckwritern

Viele Writer fungieren als "spuckwriter". Ein spuchwriter erstellt zwischen Dateien, die auf einem ursprünglichen Satz von Dateien basieren, oder "spuckt Dateien", und legt die spuatendateien zum Zeitpunkt der Sicherung an einem alternativen Speicherort ab. Der Writer verwendet die [**ivsswmfiledesc:: getalternateloations**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) -Methode, um den Anforderer zu benachrichtigen, dass er diese Dateien vom alternativen Speicherort aus sichern soll. Diese Dateien sollten jedoch weiterhin am aktiven Speicherort der ursprünglichen Dateien wieder hergestellt werden. Der testwriter kann so konfiguriert werden, dass er als spuckwriter für eine bestimmte Datei Spezifikation fungiert.

Das folgende componentfile-Element enthält ein "Alternative Path"-Attribut:

``` syntax
    <ComponentFile path="c:\files"
                   filespec="*.txt"
                   recursive="no"
                   alternatePath="c:\files\spit" />
```

In diesem Beispiel wird der Test-Writer so konfiguriert, dass alle Dateien, die mit "c: \\ Files. txt" übereinstimmen \\ \* , \\ \\ unmittelbar vor dem Erstellen der Volumeschattenkopie in das Verzeichnis "c: files Der Anforderer muss die Dateien aus dem Verzeichnis "c: \\ Files Spit" sichern \\ . Wenn der testwriter zum Löschen von Dateien konfiguriert ist, werden die ursprünglichen Dateien vor der Erstellung der Schatten Kopie gelöscht, sodass Sie nicht im Verzeichnis c: \\ Files auf dem schattenkopiespeichervolume angezeigt werden. In diesem Fall werden die Dateien in "c: Files"- \\ Dateien \\ nach dem Erstellen der Schatten Kopie gelöscht. Daher müssen Sie aus dem Verzeichnis "c \\ : Files \\ ..." auf dem schattenkopiespeichervolume gesichert werden.

## <a name="reporting-component-dependencies"></a>Abhängigkeiten der Berichtskomponente

Writer können eine Abhängigkeit zwischen einer lokalen Komponente und einer Komponente angeben, die in einem anderen Writer vorhanden ist. Diese Abhängigkeiten werden dem Anforderer mithilfe von [**ivsswmcomponent:: getdependengemeldet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdependency). Der testwriter kann so konfiguriert werden, dass diese Abhängigkeiten gemeldet werden, indem dem Component-Element mindestens ein Abhängigkeits Unterelement hinzugefügt wird.

Das folgende Component-Element enthält ein Abhängigkeits Unterelement:

``` syntax
    <Component componentType="filegroup"
               logicalPath=""
               componentName="WriterComponent"
               selectable="yes">
         <Dependency writerId="<GUID of target writer>"
                     logicalPath="ComponentPath"
                     componentName="Writer2Component" />
    </Component>
```

Die Abhängigkeit wird als Attribute des Abhängigkeits Elements angegeben. "Write ID" ist die Klassen-ID des Writers, der das Ziel der Abhängigkeit enthält. "LogicalPath" ist der logische Pfad zur Komponente in diesem Writer, und "componentname" ist der Name der Komponente. Wenn der Anforderer "Write Component" im aktuellen Writer sichert, sollte in diesem Fall auch die Komponente "componentpath \\ Writer2Component" im zielwriter gesichert werden.

> [!Note]  
> Der testwriter führt keine Überprüfung durch, um sicherzustellen, dass Abhängigkeiten berücksichtigt werden.

 

## <a name="failing-events"></a>Fehlerhafte Ereignisse

Der testwriter kann so konfiguriert werden, dass er die normalen Ereignisse, die ein Writer empfängt, fehlschlägt. Diese Ereignisse lauten wie folgt:



| Ereignis                                                                                                                                    | BESCHREIBUNG                                                                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Identify"></span><span id="identify"></span><span id="IDENTIFY"></span>Identifizieren<br/>                                     | Als Antwort auf einen [**IVssBackupComponents:: gatherschreibmetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) -Aufrufvorgang empfangen. Bei diesem Fehler wird der Writer nicht gemeldet.<br/>                                                                 |
| <span id="PrepareForBackup"></span><span id="prepareforbackup"></span><span id="PREPAREFORBACKUP"></span>PrepareForBackup<br/>     | Wird als Antwort an den Anforderer empfangen, der [**IVssBackupComponents::P Analyse forbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup)aufruft.<br/>                                                                                                                 |
| <span id="PrepareForSnapsot"></span><span id="prepareforsnapsot"></span><span id="PREPAREFORSNAPSOT"></span>Prepareforsnapsot<br/> | Wird empfangen, wenn der Anforderer [**IVssBackupComponents aufruft::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset), aber bevor die Schatten Kopie erstellt wird.<br/>                                                                                              |
| <span id="Freeze"></span><span id="freeze"></span><span id="FREEZE"></span>Ge<br/>                                             | Wird unmittelbar nach [*prepareforsnapshot*](vssgloss-p.md)empfangen, aber noch bevor die Schatten Kopie erstellt wird.<br/>                                                                                                      |
| <span id="Thaw"></span><span id="thaw"></span><span id="THAW"></span>Reaktivieren<br/>                                                     | Wird nach Abschluss der Erstellung der Schatten Kopie empfangen.<br/>                                                                                                                                                                                                     |
| <span id="PostSnapshot"></span><span id="postsnapshot"></span><span id="POSTSNAPSHOT"></span>PostSnapshot<br/>                     | Wird empfangen, nachdem das abaw abgeschlossen ist, aber vor [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) abgeschlossen ist.<br/>                                                                                                                   |
| <span id="Abort"></span><span id="abort"></span><span id="ABORT"></span>Abbruch<br/>                                                 | Wird empfangen, wenn zu viel Zeit zwischen [*Einfrieren*](vssgloss-f.md) und [*durch*](vssgloss-t.md) sucht wird, oder wenn der Anforderer [**IVssBackupComponents:: abortbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup)aufruft.<br/> |
| <span id="BackupComplete"></span><span id="backupcomplete"></span><span id="BACKUPCOMPLETE"></span>BackupComplete<br/>             | Wird empfangen, wenn der Anforderer beendet wird. Hier werden keine Fehler gemeldet.<br/>                                                                                                                                                                                 |
| <span id="PreRestore"></span><span id="prerestore"></span><span id="PRERESTORE"></span>Vorabversion<br/>                             | Wird empfangen, wenn der Anforderer [**IVssBackupComponents aufruft::P erneut**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore)ausgeführt.<br/>                                                                                                                                           |
| <span id="PostRestore"></span><span id="postrestore"></span><span id="POSTRESTORE"></span>Postrestore<br/>                         | Wird empfangen, wenn der Anforderer [**IVssBackupComponents aufruft::P ostrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore).<br/>                                                                                                                                         |



 

Diese Fehler werden durch Hinzufügen eines oder mehrerer failevent-unter Elemente zum testwriter-Stamm Element konfiguriert. Es gibt zwei Klassen von Fehlern, die festgelegt werden können: Wiederholungs fähig und nicht wiederholbar. Wiederholbare Fehler sind Fehler, die möglicherweise nicht mehr auftreten, wenn der gesamte Sicherungs Vorgang wiederholt wird, während nicht wiederholbare Fehler wahrscheinlich nicht verschwinden. Der Fehlertyp für das Ereignis wird basierend auf dem wiederholbaren Attribut ausgewählt.

Im folgenden finden Sie ein Beispiel für einen einfachen nicht wiederholbaren Fehler:

``` syntax
    <FailEvent writerEvent="Freeze"
               retryable="no" />
```

Dieses Beispiel führt dazu, dass der Writer während des [*Freeze*](vssgloss-f.md) -Ereignisses fehlschlägt. [**IVssBackupComponents:: gatherschreibstatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) meldet, dass der Writer fehlschlägt, wenn VSS \_ E \_ Beschreib tererror \_ nicht wiederholbar ist.

Im folgenden finden Sie ein Beispiel für einen einfachen Wiederholungs fähigen Fehler:

``` syntax
    <FailEvent writerEvent="Freeze"
               retryable="yes"
               numFailures="2"/>
```

Dieses Beispiel bewirkt, dass der Writer das erste Mal fehlschlägt, wenn er ein [*Freeze*](vssgloss-f.md) -Ereignis empfängt. Nach den ersten beiden vorkommen wird der Writer immer erfolgreich ausgeführt. Der von [**gatherschreiterstatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) gemeldete Writer-Fehler ist ein zufälliger Wiederholungs Fehlercode.

## <a name="declaring-supported-backup-types"></a>Deklarieren unterstützter Sicherungs Typen

Writer kommunizieren, welche Sicherungs Typen durch den Aufruf von [**ivssexaminewritermetadata:: getbackupschema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema)der Anforderer unterstützt werden. Das testwriter-Stamm Element enthält Attribute für jeden Sicherungstyp, um die Unterstützung anzugeben. Diese Attribute sind supportscopy, supportsdifferential, supportsinkremental und supportslog. Legen Sie das entsprechende Attribut auf "yes" fest, um die Unterstützung für einen bestimmten Sicherungstyp anzugeben.

Wenn der Anforderer den Sicherungstyp auf einen Sicherungstyp festlegt, der vom Writer nicht unterstützt wird, wird dieser Fakt während der [**Vorbereitung von PrepareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup)festgelegt, ansonsten aber ordnungsgemäß funktionieren.

## <a name="indicating-the-file-backup-type"></a>Angeben des Datei Sicherungs Typs

Die [**ivsswmfiledesc:: getbackuptypemask**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getbackuptypemask) -Methode gibt eine Bitmaske an den Anforderer zurück, die angibt, wie eine Datei gesichert werden soll. Dies gibt an, ob eine Datei für bestimmte Sicherungs Typen erforderlich oder nicht erforderlich ist und ob eine Schatten Kopie bei bestimmten Sicherungs Typen erforderlich ist. Die Sicherungs Typen in dieser Bitmaske werden in der [Rolle dokumentanforderer bei der Sicherung komplexer Filialen](requestor-role-in-backing-up-complex-stores.md)ausführlicher erläutert.

Im testwriter werden die Elemente dieser Bitmaske durch Festlegen von Attributen in jedem componentfile-Element angegeben. Die Attribute "fullbackuprequired", "diffbackuprequired", "incbackuprequired" und "logbackuprequired" geben an, wann eine Datei gesichert werden muss. Die Attribute "fullsnapshotrequired", "diffsnapshotrequired", "incsnapshotrequired" und "logsnapshotrequired" geben an, wann eine Datei von einer Schatten Kopie eines Volumes (und nie vom ursprünglichen Volume) gesichert werden muss. Der Standardwert für alle diese Werte ist "yes", was darauf hinweist, dass eine Datei immer gesichert werden muss und aus einer Schatten Kopie eines Volumes gesichert werden muss.

## <a name="adding-partial-files"></a>Hinzufügen von Teil Dateien

Während der Verarbeitung von [**DoSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)kann ein Writer jeder Komponente partielle Dateien hinzufügen. Diese partiellen Dateien werden mithilfe von [**IVssComponent:: GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile)gemeldet. Der testwriter kann so konfiguriert werden, dass partielle Dateien hinzugefügt werden, indem partialfile-unter Elemente in einem Component-Element angegeben werden.

Im folgenden finden Sie ein Beispiel für ein Komponenten Element mit zwei partialfile-unter Elementen:

``` syntax
    <Component componentType="filegroup"
               logicalPath=""
               componentName="WriterComponent"
               selectable="yes">
        <ComponentFile path="c:\files"
                       filespec="*.txt"
                       recursive="no"/>
        <PartialFile path="c:\files"
                     filespec="partial.txt"
                     ranges="0:5,100:20" />
        <PartialFile path="c:\files2"
                     filespec="partial.txt"
                     ranges="0:5,100:20" />
    </Component>
```

Nur partielle Dateien, die teilweise mit einer vorhandenen componentfile-Datei übereinstimmen (wie in der ersten partiellen Datei im Beispiel), oder neue Teil Dateien, die sich auf demselben Volume wie eine vorhandene componentfile-Datei (wie in der zweiten partiellen Datei) befinden, sollten auf diese Weise angegeben werden. Für diese Komponente muss die anfordernde Person vollständig alle Dateien, die mit "c: files. txt" übereinstimmen, vollständig sichern, \\ \\ \* außer partial.txt. Der Anforderer muss dann die angegebenen Bereiche (wobei ein Bereich eine Abweichung gefolgt von einer Länge ist) für die Dateien c: \\ Files \\partial.txt und c: \\ files2partial.txt sichern \\ .

Wenn der Writer zum Überprüfen von Datei Wiederherstellungen konfiguriert ist, werden nur die gesicherten Bereiche der partiellen Datei zur Wiederherstellungszeit überprüft. Änderungen an anderen Teilen der Datei werden unbemerkt bleiben. Wenn das deletepartialfiles-Attribut des testwriter-Stamm Elements festgelegt ist, werden die partiellen Dateien sofort nach der Erstellung der Schatten Kopie aus dem ursprünglichen Volume gelöscht.

## <a name="adding-differenced-files"></a>Hinzufügen differenzierter Dateien

Während der Verarbeitung von [**DoSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)kann ein Writer jeder Komponente differenzierte Dateien hinzufügen. Diese differenzierten Dateien werden mithilfe von [**IVssComponent:: getdifferencedfile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfile)gemeldet. Der testwriter kann so konfiguriert werden, dass differenzierte Dateien hinzugefügt werden, indem differencedfile-unter Elemente in einem Component-Element angegeben werden.

Im folgenden finden Sie ein Beispiel für ein Komponenten Element, das zwei differencedfile-unter Elemente aufweist:

``` syntax
    <Component componentType="filegroup"
               logicalPath=""
               componentName="WriterComponent"
               selectable="yes">
        <ComponentFile path="c:\files"
                       filespec="*.txt"
                       recursive="no"/>
        <DifferencedFile path="c:\files"
                         filespec="*.txt"
                         year="2007"
                         month="1"
                         day="22"
                         hour="12"
                         minute="44"
                         second="17" />
        <DifferencedFile path="c:\files2"
                         filespec="*.txt"
                         year="2007"
                         month="1"
                         day="22"
                         hour="12"
                         minute="44"
                         second="17" />
    </Component>
```

Anders als bei partiellen Dateien sollten differenzierte Dateien nie teilweise mit einer componentfile-Spezifikation identisch sein. Die Datei Spezifikation in einem differencedfile-Element muss entweder genau mit einer componentfile übereinstimmen (wie in der ersten differenzierten Datei im Beispiel), oder Sie sollte überhaupt nicht übereinstimmen, aber auf einem Volume, auf das in einer componentfile-Datei verwiesen wird (wie in der zweiten differenzierten Datei). Die Datums-und Uhrzeitwerte sollten relativ zur lokalen Zeitzone sein, Sie werden jedoch in GMT konvertiert, bevor Sie an den Anforderer gemeldet werden. Im Beispiel werden nur Dateien, die mit "c: \\ Files \\ \* . txt" oder "c: \\ files2. txt" übereinstimmen \\ \* , die seit 1/22/2003:12:44:17 geändert wurden, gesichert.

Wenn der testwriter zum Überprüfen von Datei Wiederherstellungen konfiguriert ist, werden nur die geänderten Dateien auf die Wiederherstellung überprüft. Wenn das deletedifferencedfiles-Attribut des testwriter-Stamm Elements festgelegt ist, werden die differenzierten Dateien sofort nach dem Erstellen der Schatten Kopie aus dem ursprünglichen Volume gelöscht.

## <a name="new-targets"></a>Neue Ziele

Bestimmte Writer gestatten dem Anforderer, ihn darüber zu informieren, dass ein neuer Speicherort zum Wiederherstellen bestimmter Dateien ausgewählt wurde. Der Writer weist darauf hin, dass dieser Modus als Teil der Bitmaske unterstützt wird, die von [**ivssexaminescriptermetadata:: getbackupschema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema)zurückgegeben wird. Standardmäßig unterstützt der testwriter immer neue Ziele. Diese Unterstützung kann deaktiviert werden, indem das supportsnewtarget-Attribut im testwriter-Stamm Element auf "No" festgelegt wird.

Wenn ein Writer neue Ziele unterstützt, kann der Antragsteller den Writer über neue Ziele informieren, indem [**IVssBackupComponents:: addnewtarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget)aufgerufen wird. Der Writer prüft dann den neuen Zielort, um die Wiederherstellung anstelle des ursprünglichen Speicher Orts zu überprüfen.

## <a name="more-information"></a>Weitere Informationen

Der testwriter unterstützt weitere Konfigurationsoptionen, die hier nicht beschrieben werden. Das vollständige Schema für alle Konfigurationsfunktionen des testwriters wird in swriter.xml in `%ProgramFiles%\Microsoft SDKs\Windows\v7.0\bin\x64\vsstools` (für 64-Bit-Windows) und `%ProgramFiles%\Microsoft SDKs\Windows\v7.0\bin\vsstools` (für 32-Bit-Windows) angegeben. Diese Datei enthält ein XML-Schema, in dem alle Elemente und Attribute, aus denen eine Konfigurationsdatei besteht, vollständig beschrieben werden. Jedes Element und jedes Attribut in dieser Datei wird mit einer Beschreibung kommentiert, die die Verwendung dieses Elements oder des Attributs dokumentiert.

 

 




