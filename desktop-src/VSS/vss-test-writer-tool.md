---
description: Der Testwriter ist ein Hilfsprogramm, das Sie zum Testen von VSS-Anfordereranwendungen verwenden können.
ms.assetid: 02434cb9-390c-4cf0-9941-b833ace55685
title: VSS-Testwritertool
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b93f0b81bd5e27db9fdfb70ca52e6f43bbb1e853af87bc12e1d76f01d7966ef3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118344233"
---
# <a name="vss-test-writer-tool"></a>VSS-Testwritertool

Der Testwriter ist ein Hilfsprogramm, das Sie zum Testen von VSS-Anfordereranwendungen verwenden können. Dieser Writer kann so konfiguriert werden, dass fast alle Aktionen ausgeführt werden, die ein VSS Writer ausführen kann. Darüber hinaus führt der Testwriter umfangreiche Überprüfungen durch, um sicherzustellen, dass der Anforderer diese Writeraktionen ordnungsgemäß verarbeitet hat.

Jede Instanz des Writers wird mit einer XML-Konfigurationsdatei initialisiert, die genau beschreibt, welche Komponenten der Writer meldet und wie sich der Writer verhält. Der Writer kann so konfiguriert werden, dass er über verschiedene Arten von Szenarien berichtet, einschließlich komplizierterer Szenarien mithilfe der inkrementellen und differenziellen Schnittstellen. Der Writer führt während des Prozesses Überprüfungen an verschiedenen Stellen durch, um sicherzustellen, dass sich der Anforderer ordnungsgemäß verhält. Nach Abschluss der Wiederherstellung überprüft der Writer, ob alle erforderlichen Dateien ohne Beschädigung wiederhergestellt wurden. Der Writer kann auch so konfiguriert werden, dass er andere Vorgänge ausführt, z. B. fehlerhafte bestimmte Ereignisse.

> [!Note]  
> Dieses Tool ist im Microsoft Windows Software Development Kit (SDK) für Windows Vista und höher enthalten. Sie können das Windows SDK von [https://msdn.microsoft.com/windowsvista](https://msdn.microsoft.com/windows/default.aspx) herunterladen.

 

In der Windows SDK-Installation finden Sie das VssSampleProvider-Tool unter `%Program Files(x86)%\Windows Kits\8.1\bin\x64` (für 64-Bit-Windows) und `%Program Files(x86)%\Windows Kits\8.1\bin\x86` .

## <a name="running-the-test-writer-tool"></a>Ausführen des Testwritertools

Geben Sie an der Eingabeaufforderung Folgendes ein, um den Testwriter zu starten:

 *vswriter.exe-Konfigurationsdatei*

dabei ist *config-file* der Pfad zu einer Konfigurationsdatei, die das Verhalten dieses Writers angibt.

Drücken Sie STRG+C, um den Testwriter zu beenden.

Mehrere Instanzen des Testwriters können gleichzeitig ausgeführt werden. Allerdings meldet jede Instanz des Writers die gleiche Writerklassen-ID (obwohl eine andere Writerinstanz-ID), sodass logische Pfade und Komponentennamen für alle gleichzeitig ausgeführten Instanzen des Writers eindeutig sein müssen.

Um sicherzustellen, dass der Writer ordnungsgemäß überprüfen kann, ob der Anforderer die Ausschlussdateispezifikationen berücksichtigt hat, sollten alle gesicherten Dateien vom ursprünglichen Volume gelöscht werden, bevor versucht wird, sie wiederherzustellen. Es wird empfohlen, eine Vorlage für jedes Writerszenario zu speichern, damit das Szenario problemlos neu erstellt werden kann.

## <a name="using-a-configuration-file"></a>Verwenden einer Konfigurationsdatei

Die folgende Beispielkonfigurationsdatei, vswriter \_config.xml, finden Sie unter `%ProgramFiles%\Microsoft SDKs\Windows\v7.0\bin\vsstools` auf x86-Plattformen und `%ProgramFiles%\Microsoft SDKs\Windows\v7.0\bin\x64\vsstools` auf x64-Plattformen.

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

Das Stammelement in dieser Konfigurationsdatei heißt TestWriter. Alle anderen Elemente werden unter dem TestWriter-Element angeordnet.

Eines der Attribute, das TestWriter zugeordnet ist, ist das Verwendungsattribut. Dieses Attribut gibt den Verwendungstyp an, der über [**IVssExwriterMetadata::GetIdentity**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getidentity)gemeldet wird. Einer der möglichen Werte für dieses Attribut ist USER \_ DATA.

Das erste untergeordnete Element des Stammelements muss immer ein RestoreMethod-Element sein. Dieses Element gibt Folgendes an:

-   Die Wiederherstellungsmethode (in diesem Fall RESTORE \_ IF \_ CAN BE \_ \_ REPLACED)
-   Gibt an, ob der Writer Wiederherstellungsereignisse erfordert (in diesem Fall immer).
-   Gibt an, ob nach der Wiederherstellung des Writers ein Neustart erforderlich ist (in diesem Fall nein).

Dieses Element kann optional eine Zuordnung alternativer Speicherorte angeben. (In diesem Fall wird kein alternativer Speicherort angegeben.)

Das zweite untergeordnete Element ist ein ExcludeFile-Element. Dieses Element bewirkt, dass der Writer eine Datei oder einen Satz von Dateien aus der Sicherung ausschließt.

Das dritte untergeordnete Element ist ein Component-Element. Dieses Element bewirkt, dass der Writer den Metadaten eine Komponente hinzufügt. Ein Component-Element enthält Attribute, um die Komponente und untergeordnete Elemente zu beschreiben, um den Inhalt der Komponente zu beschreiben, z. B.:

-   componentType, um anzugeben, ob es sich um eine Dateigruppe oder eine Datenbank handelt
-   logicalPath für den logischen Pfad der Komponente
-   componentName für den Namen der Komponente
-   Auswählbar, um den Sicherungsstatus anzugeben, der ausgewählt werden kann

Das Component-Element verfügt auch über ein untergeordnetes Element mit dem Namen ComponentFile, um dieser Komponente eine Dateispezifikation hinzuzufügen. (Ein Component-Element kann über eine beliebige Anzahl von ComponentFile-Elementen verfügen, die für jede Komponente angegeben werden können.) Dieses ComponentFile-Element weist die folgenden Attribute auf:

-   path="c: \\ writerData \\ myFilesHere"
-   filespec=" \* "
-   recursive="no"

Obwohl der Testwriter das Verhalten des Anforderers überprüft, wird nicht überprüft, ob die Konfigurationsdatei immer die dokumentierte Semantik für einen Writer beibehält. Es gibt viele Vorgänge, die ein gut verhaltener Writer nicht durchführen sollte (z. B. das Melden derselben Datei in mehreren Komponenten), und es liegt beim Autor der XML-Konfigurationsdatei, diese Semantik beizubehalten.

## <a name="configuring-writer-attributes"></a>Konfigurieren von Writerattributen

Das TestWriter-Stammelement enthält Attribute, die verschiedene Verhaltensweisen des Writers bestimmen. Folgende Verhaltensweisen können geändert werden:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>attribute</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="verbosity"></span><span id="VERBOSITY"></span>Ausführlichkeit<br/></td>
<td>Der Writer gibt den Status in der Konsole aus, während er Ereignisse empfängt und verarbeitet. Der angezeigte Ausführlichkeitsgrad wird durch das Ausführlichkeitsattribut angegeben. Es stehen drei Ausführlichkeitsebenen zur Auswahl:<br/> <dl> <dt><span id="low"></span><span id="LOW"></span>Niedrig</dt> <dd> Es werden nur Fehler im Writer oder falsches Verhalten des Anfordernden ausgegeben.<br/> </dd> <dt><span id="medium"></span><span id="MEDIUM"></span>Mittel</dt> <dd> Zusätzlich zu zusätzlichen Statusinformationen, z. B. beim Empfang von Ereignissen, wird alles auf niedriger Ausführlichkeitsebene ausgegeben. Dies ist der Standardebene.<br/> </dd> <dt><span id="high"></span><span id="HIGH"></span>Hoch</dt> <dd> Detaillierte Statusinformationen zum Vorgang des Writers werden gemeldet.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="deleteFiles"></span><span id="deletefiles"></span><span id="DELETEFILES"></span>deleteFiles<br/></td>
<td>Um eine zusätzliche Überprüfung durchzuführen, legen Sie dieses Attribut auf Ja fest, &quot; damit der Writer alle seine Dateien sofort nach dem Erstellen der &quot; Volumeschattenkopie löscht. Der Anforderer muss dann die Dateien aus der Schattenkopie kopieren, da sie auf dem ursprünglichen Volume nicht mehr vorhanden sind. <br/>
<blockquote>
[!Note]<br />
Im Fall von Spit Writern werden die Dateien nach der Spit, aber vor der Erstellung der Schattenkopie vom ursprünglichen Speicherort gelöscht. Nachdem die Schattenkopie erstellt wurde, werden die Dateien aus dem Spit-Verzeichnis gelöscht.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="deletePartialFiles"></span><span id="deletepartialfiles"></span><span id="DELETEPARTIALFILES"></span>deletePartialFiles<br/></td>
<td>Um Teildateien zu löschen, legen Sie dieses Attribut auf &quot; ja &quot; fest.<br/></td>
</tr>
<tr class="even">
<td><span id="deleteDifferencedFiles"></span><span id="deletedifferencedfiles"></span><span id="DELETEDIFFERENCEDFILES"></span>deleteDifferencedFiles<br/></td>
<td>Um differenzierte Dateien zu löschen, legen Sie dieses Attribut auf &quot; ja &quot; fest.<br/></td>
</tr>
<tr class="odd">
<td><span id="checkIncludes"></span><span id="checkincludes"></span><span id="CHECKINCLUDES"></span>checkIncludes<br/></td>
<td>Legen Sie dieses Attribut auf &quot; Ja &quot; fest, damit der Writer überprüft, ob alle gesicherten Dateien an einem geeigneten Speicherort wiederhergestellt wurden und dass die Datei nicht beschädigt wurde. Teildateien und differenzierte Dateien werden ebenfalls ordnungsgemäß verarbeitet.<br/></td>
</tr>
<tr class="even">
<td><span id="checkExcludes"></span><span id="checkexcludes"></span><span id="CHECKEXCLUDES"></span>checkExcludes<br/></td>
<td>Legen Sie dieses Attribut auf &quot; Ja &quot; fest, damit der Writer überprüft, ob Dateien, die einer Dateispezifikation in der Ausschlussliste entsprechen, nicht wiederhergestellt werden. Damit dies ordnungsgemäß funktioniert, müssen die Wiederherstellungsverzeichnisse vor der Wiederherstellung geleert werden.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="specifying-alternate-location-mappings"></a>Angeben alternativer Standortzuordnungen

Eine alternative Speicherortzuordnung gibt einen Wiederherstellungsspeicherort an, wenn die Wiederherstellungsmethode VSS WRE RESTORE TO ALTERNATE LOCATION ist oder wenn die \_ \_ normale \_ \_ \_ Wiederherstellung einer Komponente fehlschlägt. Ein Writer kann seine alternativen Speicherortzuordnungen an den Anforderer melden, indem er die [**IVssExwriterMetadata::GetAlternateLocationMapping-Methode**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping) verwendet. Sie können der TestWriter-Konfigurationsdatei alternative Speicherortzuordnungen hinzufügen, indem Sie dem RestoreMethod-Element AlternateLocationMapping-Unterelemente hinzufügen.

Das folgende RestoreMethod-Element enthält ein AlternateLocationMapping-Unterelement.

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

In diesem Beispiel wird angegeben, dass der Anforderer zunächst versuchen soll, alle Dateien wiederherzustellen, die mit c:-Dateien \\ \\ \* übereinstimmen,.txt im Verzeichnis c: \\ files. Wenn eine dieser Dateien nicht ersetzt werden kann, sollte der Anforderer stattdessen alle Dateien im Verzeichnis c: \\ altfiles wiederherstellen. Der Anforderer sollte diese alternative Standortzuordnung mithilfe der [**IVssBackupComponents::AddAlternativeLocationMapping-Methode**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addalternativelocationmapping) speichern. Wenn der Testwriter so konfiguriert ist, dass überprüft wird, ob Dateien wiederhergestellt wurden, überprüft er auch, ob der Anforderer **AddAlternativeLocationMapping** aufgerufen hat.

## <a name="specifying-files-to-be-excluded"></a>Angeben der auszuschließenden Dateien

Jeder Writer kann eine Liste von Dateispezifikationen angeben, die Dateien angeben, die der Anfordernde von der Sicherung ausschließen soll. Sie können diese Dateispezifikationen der Test Writer-Konfigurationsdatei hinzufügen, indem Sie excludeFile-Unterelemente zum TestWriter-Stammelement hinzufügen.

Hier ist ein Beispiel für ein ExcludeFile-Unterelement, das alle Dateien im Verzeichnis C: \\ files ausschließt, die mit C: temp \\ \* \* übereinstimmen.

``` syntax
    <ExcludeFile path="c:\files" 
                 filespec="temp*.*" 
                 recursive="no"/>
```

## <a name="backing-up-spit-writers"></a>Sichern von Spit Writers

Viele Writer fungieren als "Spit Writer". Ein Spit Writer erstellt Zwischendateien oder "Spit-Dateien" basierend auf einem ursprünglichen Satz von Dateien und legt die Spit-Dateien zur Sicherungszeit an einem alternativen Speicherort ab. Der Writer verwendet die [**IVssWMFiledesc::GetAlternateLocation-Methode,**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) um den Anfordernden zu benachrichtigen, dass diese Dateien vom alternativen Speicherort gesichert werden sollen. Diese Dateien sollten jedoch weiterhin am aktiven Speicherort der ursprünglichen Dateien wiederhergestellt werden. Der Testwriter kann so konfiguriert werden, dass er als Spit Writer für eine bestimmte Dateispezifikation fungiert.

Das folgende ComponentFile-Element enthält ein alternatePath-Attribut:

``` syntax
    <ComponentFile path="c:\files"
                   filespec="*.txt"
                   recursive="no"
                   alternatePath="c:\files\spit" />
```

In diesem Beispiel wird der Testwriter so konfiguriert, dass alle Dateien, die mit c: übereinstimmende \\ Dateien \\ \*.txt, \\ direkt vor dem Erstellen der \\ Volumeschattenkopie in das Verzeichnis c: files spit kopiert werden. Der Anforderer muss die Dateien aus dem Verzeichnis c: \\ files \\ spit sichern. Wenn der Testwriter zum Löschen von Dateien konfiguriert ist, werden die ursprünglichen Dateien gelöscht, bevor die Schattenkopie erstellt wird, sodass sie nicht im Verzeichnis c: \\ files auf dem Schattenkopievolume angezeigt werden. In diesem Fall werden die Dateien in c: \\ files \\ spit gelöscht, nachdem die Schattenkopie erstellt wurde, sodass sie aus dem Verzeichnis c: \\ files \\ spit auf dem Schattenkopievolume gesichert werden müssen.

## <a name="reporting-component-dependencies"></a>Berichtskomponentenabhängigkeiten

Writer können eine Abhängigkeit zwischen einer lokalen Komponente und einer Komponente angeben, die in einem anderen Writer vorhanden ist. Diese Abhängigkeiten werden dem Anfordernden mithilfe von [**IVssWMComponent::GetDependency**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdependency)gemeldet. Der Testwriter kann zum Melden dieser Abhängigkeiten konfiguriert werden, indem dem Component-Element ein oder mehrere Abhängigkeitsunterelemente hinzugefügt werden.

Das folgende Component-Element enthält ein Dependency-Unterelement:

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

Die Abhängigkeit wird als Attribute des Dependency-Elements angegeben. writerId ist die Klassen-ID des Writers, der das Ziel der Abhängigkeit enthält, logicalPath ist der logische Pfad zur Komponente in diesem Writer, und componentName ist der Name der Komponente. Wenn der Anforderer in diesem Fall "WriterComponent" im aktuellen Writer gesichert, sollte er auch die Komponente "ComponentPath \\ Writer2Component" im Zielwriter sichern.

> [!Note]  
> Der Testwriter führt keine Überprüfung durch, um sicherzustellen, dass Abhängigkeiten berücksichtigt werden.

 

## <a name="failing-events"></a>Fehlerhafte Ereignisse

Der Testwriter kann so konfiguriert werden, dass alle normalen Ereignisse, die ein Writer empfängt, fehlschlagen. Diese Ereignisse sind wie folgt:



| Ereignis                                                                                                                                    | BESCHREIBUNG                                                                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Identify"></span><span id="identify"></span><span id="IDENTIFY"></span>Identifizieren<br/>                                     | Wird als Antwort auf einen [**IVssBackupComponents::GatherWriterMetadata-Aufruf**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) empfangen. Ein Fehler hier führt dazu, dass der Writer nicht gemeldet wird.<br/>                                                                 |
| <span id="PrepareForBackup"></span><span id="prepareforbackup"></span><span id="PREPAREFORBACKUP"></span>PrepareForBackup<br/>     | Als Antwort an den Anfordernden empfangen, der [**IVssBackupComponents::P repareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup)aufruft.<br/>                                                                                                                 |
| <span id="PrepareForSnapsot"></span><span id="prepareforsnapsot"></span><span id="PREPAREFORSNAPSOT"></span>PrepareForSnapsot<br/> | Wird empfangen, wenn der Anfordernde [**IVssBackupComponents::D oSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)aufruft, aber bevor die Schattenkopie erstellt wird.<br/>                                                                                              |
| <span id="Freeze"></span><span id="freeze"></span><span id="FREEZE"></span>Einfrieren<br/>                                             | Wird unmittelbar nach [*PrepareForSnapshot*](vssgloss-p.md)empfangen, aber noch bevor die Schattenkopie erstellt wird.<br/>                                                                                                      |
| <span id="Thaw"></span><span id="thaw"></span><span id="THAW"></span>Tauwetter<br/>                                                     | Wird empfangen, nachdem die Erstellung der Schattenkopie abgeschlossen wurde.<br/>                                                                                                                                                                                                     |
| <span id="PostSnapshot"></span><span id="postsnapshot"></span><span id="POSTSNAPSHOT"></span>PostSnapshot<br/>                     | Wird nach Abschluss von Thaw, aber vor Abschluss von [**IVssBackupComponents::D oSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) empfangen.<br/>                                                                                                                   |
| <span id="Abort"></span><span id="abort"></span><span id="ABORT"></span>Abbrechen<br/>                                                 | Wird empfangen, wenn zu viel Zeit zwischen [*Freeze*](vssgloss-f.md) und [*Thaw*](vssgloss-t.md) vergeht oder wenn der Anfordernde [**IVssBackupComponents::AbortBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup)aufruft.<br/> |
| <span id="BackupComplete"></span><span id="backupcomplete"></span><span id="BACKUPCOMPLETE"></span>BackupComplete<br/>             | Wird empfangen, wenn der Anforderer beendet wird. Fehler werden hier nie gemeldet.<br/>                                                                                                                                                                                 |
| <span id="PreRestore"></span><span id="prerestore"></span><span id="PRERESTORE"></span>PreRestore<br/>                             | Wird empfangen, wenn der Anfordernde [**IVssBackupComponents::P reRestore aufruft.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore)<br/>                                                                                                                                           |
| <span id="PostRestore"></span><span id="postrestore"></span><span id="POSTRESTORE"></span>PostRestore<br/>                         | Wird empfangen, wenn der Anfordernde [**IVssBackupComponents::P ostRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore)aufruft.<br/>                                                                                                                                         |



 

Diese Fehler werden konfiguriert, indem dem Stammelement TestWriter mindestens ein FailEvent-Unterelement hinzugefügt wird. Es gibt zwei Klassen von Fehlern, die festgelegt werden können: wiederholbar und nicht wiederholbar. Wiederholbare Fehler sind Fehler, die verloren gehen können, wenn der gesamte Sicherungsvorgang wiederholt wird, während nicht wiederholbare Fehler wahrscheinlich nicht mehr auftreten. Der Fehlertyp für das Ereignis wird basierend auf dem wiederholbaren Attribut ausgewählt.

Hier sehen Sie ein Beispiel für einen grundlegenden, nicht wiederholbaren Fehler:

``` syntax
    <FailEvent writerEvent="Freeze"
               retryable="no" />
```

Dieses Beispiel führt dazu, dass der Writer während des [*Freeze-Ereignisses*](vssgloss-f.md) fehlschlägt. [**IVssBackupComponents::GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) meldet den Writerfehler als VSS \_ E \_ WRITERERROR \_ NONRETRYABLE.

Hier sehen Sie ein Beispiel für einen einfachen, wiederholbaren Fehler:

``` syntax
    <FailEvent writerEvent="Freeze"
               retryable="yes"
               numFailures="2"/>
```

Dieses Beispiel bewirkt, dass der Writer das erste Mal fehlschlägt, wenn er ein [*Freeze-Ereignis*](vssgloss-f.md) empfängt. Nach den ersten beiden Mal ist der Writer immer erfolgreich. Der über [**GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) gemeldete Writerfehler ist ein zufälliger, wiederholbarer Fehlercode.

## <a name="declaring-supported-backup-types"></a>Deklarieren unterstützter Sicherungstypen

Writer kommunizieren, welche Sicherungstypen durch den Aufruf von [**IVssExwriterMetadata::GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema)des Anfordernden unterstützt werden. Das TestWriter-Stammelement enthält Attribute für jeden Sicherungstyp, um Unterstützung anzugeben. Diese Attribute sind supportsCopy, supportsDifferential, supportsIncremental und supportsLog. Um die Unterstützung für einen bestimmten Sicherungstyp anzugeben, legen Sie das entsprechende Attribut auf "ja" fest.

Wenn der Anfordernde den Sicherungstyp auf einen Sicherungstyp festlegt, der vom Writer nicht unterstützt wird, notiert der Writer diese Tatsache während [**PrepareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup), funktioniert aber andernfalls ordnungsgemäß.

## <a name="indicating-the-file-backup-type"></a>Angeben des Dateisicherungstyps

Die [**IVssWMFiledesc::GetBackupTypeMask-Methode**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getbackuptypemask) gibt eine Bitmaske an den Anfordernden zurück, die angibt, wie eine Datei gesichert werden soll. Dadurch wird angegeben, ob eine Datei während bestimmter Sicherungstypen erforderlich oder nicht erforderlich ist und ob während bestimmter Sicherungstypen eine Schattenkopie erforderlich ist. Die Sicherungstypen in dieser Bitmaske werden ausführlicher im Dokument [Anfordernde Rolle unter Sichern komplexer Speicher](requestor-role-in-backing-up-complex-stores.md)erläutert.

Im TestWriter werden die Elemente dieser Bitmaske durch Festlegen von Attributen in jedem ComponentFile-Element angegeben. Die Attribute fullBackupRequired, diffBackupRequired, incBackupRequired und logBackupRequired geben an, wann eine Datei gesichert werden muss. Die Attribute fullSnapshotRequired, diffSnapshotRequired, incSnapshotRequired und logSnapshotRequired geben an, wann eine Datei aus einer Schattenkopie eines Volumes (und nie vom ursprünglichen Volume) gesichert werden muss. Der Standardwert für alle diese Werte ist "Ja", was angibt, dass eine Datei immer gesichert und aus einer Schattenkopie eines Volumes gesichert werden muss.

## <a name="adding-partial-files"></a>Hinzufügen von Teildateien

Während der Verarbeitung von [**DoSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)hat ein Writer die Möglichkeit, jeder Komponente Teildateien hinzuzufügen. Diese Teildateien werden mithilfe von [**IVssComponent::GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile)gemeldet. Der Testwriter kann so konfiguriert werden, dass Partielle Dateien hinzugefügt werden, indem PartialFile-Unterelemente in einem Component-Element angegeben werden.

Hier sehen Sie ein Beispiel für ein Component-Element, das über zwei PartialFile-Unterelemente verfügt:

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

Nur Teildateien, die teilweise mit einer vorhandenen ComponentFile übereinstimmen (wie in der ersten Teildatei im Beispiel), oder neue Teildateien, die sich auf demselben Volume wie eine vorhandene ComponentFile befinden (wie in der zweiten partiellen Datei), sollten auf diese Weise angegeben werden. Für diese Komponente muss der Anforderer alle Dateien, die mit c: übereinstimmen, vollständig \\ \\ \* sichern, mit Ausnahme von partial.txt.txt. Der Anforderer muss dann die angegebenen Bereiche (wobei ein Bereich ein Offset gefolgt von einer Länge ist) für die Dateien c: \\ dateien \\partial.txt und c: \\ files2partial.txt \\ sichern.

Wenn der Writer zum Überprüfen von Dateiwiederherstellungen konfiguriert ist, werden nur die gesicherten Bereiche der Teildatei zum Zeitpunkt der Wiederherstellung überprüft. Änderungen an anderen Teilen der Datei bleiben unbemerkt. Wenn das deletePartialFiles-Attribut des TestWriter-Stammelements festgelegt ist, werden die Teildateien unmittelbar nach dem Erstellen der Schattenkopie vom ursprünglichen Volume gelöscht.

## <a name="adding-differenced-files"></a>Hinzufügen differenzierter Dateien

Während der Verarbeitung von [**DoSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)kann ein Writer jeder Komponente differenzierte Dateien hinzufügen. Diese differenzierten Dateien werden mithilfe von [**IVssComponent::GetDifferencedFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfile)gemeldet. Der Testwriter kann so konfiguriert werden, dass differenzierte Dateien hinzugefügt werden, indem DifferencedFile-Unterelemente in einem Component-Element angegeben werden.

Hier sehen Sie ein Beispiel für ein Component-Element, das über zwei DifferencedFile-Unterelemente verfügt:

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

Im Gegensatz zu Teildateien sollten unterschiedliche Dateien niemals teilweise mit einer ComponentFile-Spezifikation übereinstimmen. Die Dateispezifikation in einem DifferencedFile-Element sollte entweder genau mit einer ComponentFile übereinstimmen (wie in der ersten Differenzdatei im Beispiel), oder sie sollte überhaupt nicht mit ihr übereinstimmen, sondern auf einem Volume, auf das in einer ComponentFile verwiesen wird (wie in der zweiten differenzierten Datei). Die Datums- und Uhrzeitwerte sollten relativ zur lokalen Zeitzone sein, aber sie werden in GMT konvertiert, bevor sie dem Anfordernden gemeldet werden. Im Beispiel werden nur Dateien gesichert, die mit c: \\ dateien \\ \*.txt oder c: \\ files2 \\ \* übereinstimmen,.txt, die seit dem 22.1.2003:12:44:17 geändert wurden.

Wenn der Testwriter zum Überprüfen von Dateiwiederherstellungen konfiguriert ist, werden nur die geänderten Dateien auf die Wiederherstellung überprüft. Wenn das deleteDifferencedFiles-Attribut des TestWriter-Stammelements festgelegt ist, werden die differenzierten Dateien unmittelbar nach dem Erstellen der Schattenkopie vom ursprünglichen Volume gelöscht.

## <a name="new-targets"></a>Neue Ziele

Bestimmte Writer erlauben dem Anforderer, sie darüber zu informieren, dass ein neuer Speicherort ausgewählt wurde, an dem bestimmte Dateien wiederhergestellt werden sollen. Der Writer gibt an, dass dieser Modus als Teil der Bitmaske unterstützt wird, die von [**IVssExwriterMetadata::GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema)zurückgegeben wird. Standardmäßig unterstützt der Testwriter immer neue Ziele. Diese Unterstützung kann deaktiviert werden, indem das supportsNewTarget-Attribut im TestWriter-Stammelement auf "no" festgelegt wird.

Wenn ein Writer neue Ziele unterstützt, kann der Anforderer den Writer über neue Ziele informieren, indem [**er IVssBackupComponents::AddNewTarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget)aufruft. Der Writer überprüft dann den neuen Zielspeicherort, um die Wiederherstellung anstelle des ursprünglichen Speicherorts zu überprüfen.

## <a name="more-information"></a>Weitere Informationen

Der Testwriter unterstützt weitere Konfigurationsoptionen, die hier nicht beschrieben werden. Das vollständige Schema für alle Konfigurationsfunktionen des Testwriters wird in swriter.xml in `%ProgramFiles%\Microsoft SDKs\Windows\v7.0\bin\x64\vsstools` (für 64-Bit-Windows) und `%ProgramFiles%\Microsoft SDKs\Windows\v7.0\bin\vsstools` (für 32-Bit-Windows) angegeben. Diese Datei enthält ein XML-Schema, das alle Elemente und Attribute einer Konfigurationsdatei vollständig beschreibt. Jedes Element und jedes Attribut in dieser Datei wird mit einer Beschreibung kommentiert, die die Verwendung dieses Elements oder Attributs dokumentiert.

 

 




