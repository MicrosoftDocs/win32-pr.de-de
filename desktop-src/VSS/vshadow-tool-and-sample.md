---
description: VShadow ist ein Befehlszeilentool, mit dem Sie Volumeschattenkopien erstellen und verwalten können.
ms.assetid: 19109f92-b9da-4df7-8628-374e37a3f624
title: VShadow-Tool und -Beispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 306d759d10875b03cb0d2e4e2064a85614400ff5240800da3fc4c1ce94add8c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998070"
---
# <a name="vshadow-tool-and-sample"></a>VShadow-Tool und -Beispiel

VShadow ist ein Befehlszeilentool, mit dem Sie Volumeschattenkopien erstellen und verwalten können.

> [!Note]  
> VShadow ist im Microsoft Windows Software Development Kit (SDK) für Windows Vista und höher enthalten. Das VSS 7.2 SDK enthält eine Version von VShadow, die nur auf Windows Server 2003 ausgeführt wird. Informationen zum Herunterladen des Windows SDK und des VSS 7.2 SDK finden Sie unter [Volumeschattenkopie-Dienst](volume-shadow-copy-service-portal.md).

 

Das VShadow-Tool verwendet Befehlszeilenoptionen und optionale Flags, um die auszuführende Arbeit zu identifizieren. Bei Verwendung ohne Befehlszeilenoptionen erstellt der VShadow-Befehl einen neuen Schattenkopiesatz.

VShadow-Befehle führen die folgenden Vorgänge aus:

-   [Erstellen eines Schattenkopiesatzes](#creating-a-shadow-copy-set)
-   [Importieren eines Schattenkopiesatzes](#importing-a-shadow-copy-set)
-   [Abfragen von Schattenkopieeigenschaften](#querying-shadow-copy-properties)
-   [Löschen von Schattenkopien](#deleting-shadow-copies)
-   [Breaking a Shadow Copy Set](#breaking-a-shadow-copy-set)
-   [Unterbrechen eines Schattenkopiesets mithilfe der BreakSnapshotSetEx-Methode](#breaking-a-shadow-copy-set-using-the-breaksnapshotsetex-method)
-   [Lokales Verfügbarmachen einer Schattenkopie](#exposing-a-shadow-copy-locally)
-   [Remote verfügbarmachen einer Schattenkopie](#exposing-a-shadow-copy-remotely)
-   [Auflisten des Writerstatus und der Metadaten](#listing-writer-status-and-metadata)
-   [Ausführen von Wiederherstellungsvorgängen](#performing-restore-operations)
-   [Kehren zu einer vorherigen Schattenkopie zurück](#reverting-to-a-previous-shadow-copy)
-   [Erneutes Synchronisieren von LUNs](#resynchronizing-luns)

## <a name="creating-a-shadow-copy-set"></a>Erstellen eines Schattenkopiesatzes

**vshadow** \[ OptionalFlags \] *VolumeList*

Dieser Befehl erstellt einen neuen Schattenkopiesatz.

*VolumeList* ist eine Liste von Volumenamen. VShadow erstellt eine Schattenkopie für jedes Volume in der Liste. Ein Volumename kann optional mit einem umgekehrten Schrägstrich () beendet \\ werden. Beispielsweise sind sowohl C: als auch C: \\ gültige Volumenamen. Sie können auch bereitgestellte Ordner (z. B. C: \\ DirectoryName) oder Volume-GUID-Namen (z. \\ \\ B. ? \\ Volume{edbed95e-7e8d-11d8-9d01-505054503030}).

*OptionalFlags* ist eine Bitmaske mit optionalen Flagwerten aus der folgenden Tabelle.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Optionaler Flagwert</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="-ad"></span><span id="-AD"></span><strong>-ad</strong><br/></td>
<td>Dieses optionale Flag gibt differenzielle Hardwareschattenkopien an. Dieses Flag und das <strong>-ap-Flag</strong> schließen sich gegenseitig aus.<br/>
<blockquote>
[!Note]<br />
Dieses Flag wird nur unter Windows Serverbetriebssystemen unterstützt.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="-ap"></span><span id="-AP"></span><strong>-ap</strong><br/></td>
<td>Dieses optionale Flag gibt plexe Hardwareschattenkopien an. Dieses Flag und das <strong>-ad-Flag</strong> schließen sich gegenseitig aus.<br/>
<blockquote>
[!Note]<br />
Dieses Flag wird nur unter Windows Serverbetriebssystemen unterstützt.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="_-bc_File.xml"></span><span id="_-bc_file.xml"></span><span id="_-BC_FILE.XML"></span><strong></strong> <strong>-bc=</strong><em>Datei</em> <strong>.xml</strong><br/></td>
<td>Dieses optionale Flag gibt nicht transportierbare Schattenkopien an und speichert das Sicherungskomponentendokument in der angegebenen Datei. Diese Datei kann in einem nachfolgenden Wiederherstellungsvorgang verwendet werden. Dieses Flag und das <strong>-t-Flag</strong> schließen sich gegenseitig aus.<br/>
<blockquote>
[!Note]<br />
Dieses Flag wird nur unter Windows Serverbetriebssystemen unterstützt.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="-exec_Command"></span><span id="-exec_command"></span><span id="-EXEC_COMMAND"></span><strong>-exec=</strong><em>Befehl</em><br/></td>
<td>Dieses optionale Flag führt einen Befehl oder ein Skript aus, nachdem die Schattenkopien erstellt wurden, aber bevor das VShadow-Tool beendet wird. <em>Command</em> kann einen ausführbaren Shellbefehl oder eine CMD-Datei angeben. Wenn ein Shellbefehl angegeben wird, können keine Befehlsparameter angegeben werden.<br/>
<blockquote>
[!Note]<br />
Aus Sicherheitsgründen und um die Implementierung einfach zu halten, akzeptiert das optionale Flag <strong>-exec</strong> keine Parameter, die an den Befehl oder das Skript übergeben werden sollen. Die gesamte Zeichenfolge, die an das optionale Flag <strong>-exec</strong> übergeben wird, wird als einzelne CMD- oder EXE-Datei behandelt. Weitere Informationen zu dieser Einschränkung finden Sie im Quellcode von VShadow.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="-forcerevert"></span><span id="-FORCEREVERT"></span><strong>-forcerevert</strong><br/></td>
<td>Dieses optionale Flag gibt an, dass der Schattenkopiervorgang nur abgeschlossen werden soll, wenn alle Datenträgersignaturen wiegt werden können.<br/>
<blockquote>
[!Note]<br />
Dieses Flag wird nur unter Windows Serverbetriebssystemen unterstützt.
</blockquote>
<br/> <strong>Windows Server 2003:</strong> Wird nicht unterstützt.<br/></td>
</tr>
<tr class="even">
<td><span id="-mask"></span><span id="-MASK"></span><strong>-mask</strong><br/></td>
<td>Dieses optionale Flag gibt an, dass die Schattenkopie-LUNs vom Computer maskiert werden sollen, wenn das Schattenkopieset beschädigt ist.<br/>
<blockquote>
[!Note]<br />
Dieses Flag wird nur unter Windows Serverbetriebssystemen unterstützt.
</blockquote>
<br/> <strong>Windows Server 2003:</strong> Wird nicht unterstützt.<br/></td>
</tr>
<tr class="odd">
<td><span id="-nar"></span><span id="-NAR"></span><strong>-nar</strong><br/></td>
<td>Dieses optionale Flag gibt Schattenkopien ohne automatische Wiederherstellung an. Weitere Informationen zu dieser Option finden Sie in der <a href="/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes"><strong></strong></a> Dokumentation zum VSS_VOLSNAP_ATTR_NO_AUTORECOVERY-Flag der _VSS_VOLUME_SNAPSHOT_ATTRIBUTES-Enumeration.<br/></td>
</tr>
<tr class="even">
<td><span id="-norevert"></span><span id="-NOREVERT"></span><strong>-norevert</strong><br/></td>
<td>Dieses optionale Flag gibt an, dass Datenträgersignaturen nicht wiegt werden sollen.<br/>
<blockquote>
[!Note]<br />
Dieses Flag wird nur unter Windows Serverbetriebssystemen unterstützt.
</blockquote>
<br/> <strong>Windows Server 2003:</strong> Wird nicht unterstützt.<br/></td>
</tr>
<tr class="odd">
<td><span id="-nw"></span><span id="-NW"></span><strong>-nw</strong><br/></td>
<td>Dieses optionale Flag gibt Schattenkopien ohne Einbeziehung von Writern an. Weitere Informationen zu Schattenkopien ohne Beteiligung des Autors finden Sie unter <a href="shadow-copy-creation-details.md">Details zur Erstellung von Schattenkopien.</a> Dieses Flag und die Flags <strong>-wi</strong> und <strong>-wx</strong> schließen sich gegenseitig aus.<br/></td>
</tr>
<tr class="even">
<td><span id="-p"></span><span id="-P"></span><strong>-p</strong><br/></td>
<td>Dieses optionale Flag gibt <a href="vssgloss-p.md"><em>persistente Schattenkopien</em></a>an.<br/>
<blockquote>
[!Note]<br />
Dieses Flag wird nur unter Windows Serverbetriebssystemen unterstützt.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="-rw"></span><span id="-RW"></span><strong>-rw</strong><br/></td>
<td>Dieses optionale Flag gibt an, dass die Schattenkopie-LUNs gelesen/geschrieben werden sollen, wenn der Schattenkopiesatz fehlerhaft ist.<br/>
<blockquote>
[!Note]<br />
Dieses Flag wird nur unter Windows Serverbetriebssystemen unterstützt.
</blockquote>
<br/> <strong>Windows Server 2003:</strong> Wird nicht unterstützt.<br/></td>
</tr>
<tr class="even">
<td><span id="-scsf"></span><span id="-SCSF"></span><strong>-scsf</strong><br/></td>
<td>Dieses optionale Flag gibt <a href="vssgloss-c.md"><em>für den Client zugängliche Schattenkopien an.</em></a><br/>
<blockquote>
[!Note]<br />
Dieses Flag wird nur unter Windows Serverbetriebssystemen unterstützt.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="-script_File.cmd"></span><span id="-script_file.cmd"></span><span id="-SCRIPT_FILE.CMD"></span><strong>-script=</strong><em>Datei</em><strong>.cmd</strong><br/></td>
<td>Dieses optionale Flag generiert eine CMD-Datei mit Umgebungsvariablen im Zusammenhang mit den erstellten Schattenkopien, z. B. Schattenkopie-IDs und Schattenkopiesatz-IDs.<br/></td>
</tr>
<tr class="even">
<td><span id="-t_File.xml"></span><span id="-t_file.xml"></span><span id="-T_FILE.XML"></span><strong>-t=</strong><em>Datei</em> <strong>.xml</strong><br/></td>
<td>Dieses optionale Flag gibt transportierbare Schattenkopien an und speichert das Sicherungskomponentendokument in der Datei, die vom <em> parameterFile.xml</em> angegeben wird. Diese Datei kann in einem nachfolgenden Import- und/oder Wiederherstellungsvorgang verwendet werden. Dieses Flag und das <strong>Flag -bc</strong> schließen sich gegenseitig aus.<br/> <strong>Windows Server 2003, Standard Edition und Windows Server 2003, Web Edition:</strong> Transportierbare Schattenkopien werden nicht unterstützt. Alle Editionen von Windows Server 2003 mit Service Pack 1 (SP1) unterstützen transportierbare Schattenkopien.<br/></td>
</tr>
<tr class="odd">
<td><span id="-tr"></span><span id="-TR"></span><strong>-tr</strong><br/></td>
<td>Dieses optionale Flag gibt an, dass die TxF-Wiederherstellung während der Erstellung von Schattenkopien erzwungen werden soll.<br/>
<blockquote>
[!Note]<br />
Dieses Flag wird nur unter Windows Serverbetriebssystemen unterstützt.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="-tracing"></span><span id="-TRACING"></span><strong>-tracing</strong><br/></td>
<td>Dieses optionale Flag generiert eine ausführliche Ausgabe, die für die Problembehandlung verwendet werden kann.<br/></td>
</tr>
<tr class="odd">
<td><span id="-wait"></span><span id="-WAIT"></span><strong>-wait</strong><br/></td>
<td>Dieses optionale Flag bewirkt, dass das VShadow-Tool auf die Bestätigung des Benutzers wartet, bevor es beendet wird.<br/></td>
</tr>
<tr class="even">
<td><span id="-wi_Writer"></span><span id="-wi_writer"></span><span id="-WI_WRITER"></span><strong>-wi=</strong><em>Writer</em><br/></td>
<td>Dieses optionale Flag überprüft, ob der angegebene Writer oder die angegebene Komponente in der Schattenkopie enthalten ist. <em>Writer</em> kann einen Komponentenpfad, einen Writernamen, eine Writer-ID oder eine Writerinstanz-ID angeben. Dieses Flag und das <strong>Flag -nw</strong> schließen sich gegenseitig aus.<br/></td>
</tr>
<tr class="odd">
<td><span id="-wx_Writer"></span><span id="-wx_writer"></span><span id="-WX_WRITER"></span><strong>-wx=</strong><em>Writer</em><br/></td>
<td>Dieses optionale Flag überprüft, ob der angegebene Writer oder die angegebene Komponente aus der Schattenkopie ausgeschlossen ist. <em>Writer</em> kann einen Komponentenpfad, einen Writernamen, eine Writer-ID oder eine Writerinstanz-ID angeben. Dieses Flag und das <strong>Flag -nw</strong> schließen sich gegenseitig aus.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="importing-a-shadow-copy-set"></a>Importieren eines Schattenkopiesets

**vshadow** \[ OptionalFlags \] **-i=**_Datei.xml_ *__*

Die **Befehlszeilenoption -i** importiert einen transportierbaren Schattenkopiesatz.

> [!Note]  
> Diese Befehlszeilenoption wird nur auf Windows Serverbetriebssystemen unterstützt.

 

Die *File.xml-Datei* muss eine Sicherungskomponenten-Dokumentdatei für einen transportierbaren Schattenkopiesatz sein, der mit dem optionalen **Flag -t** oder **-bc** erstellt wurde.

Ein Schattenkopiesatz ist eine [*persistente Schattenkopie,*](vssgloss-p.md) wenn er mit dem optionalen **Flag -p** erstellt wurde. Wenn der transportierbare Schattenkopiesatz nicht vorhanden ist, wird er für kurze Zeit angezeigt, während der Befehl zum Erstellen von Schattenkopien ausgeführt wird, und wird automatisch gelöscht, wenn der Befehl zurückgegeben wird. Sie können nichtpersistente Schattenkopien nur während der Erstellung von Schattenkopien importieren, indem Sie den Schattenkopiesatz mit dem optionalen **Flag -exec** erstellen, um eine CMD-Datei auszuführen, die VShadow **-i aufruft.**

Die **Befehlszeilenoption -i** kann nicht mit anderen Befehlszeilenoptionen kombiniert werden.

*OptionalFlags* ist eine Bitmaske optionaler Flagwerte aus der folgenden Tabelle.



| Optionaler Flagwert                                                                                                            | BESCHREIBUNG                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="-exec_Command"></span><span id="-exec_command"></span><span id="-EXEC_COMMAND"></span>**-exec=**_Befehl_<br/> | Dieses optionale Flag führt einen Befehl oder ein Skript aus, nachdem die Schattenkopien importiert wurden, aber bevor das VShadow-Tool beendet wird. *Der Befehl* kann einen ausführbaren Shellbefehl oder eine CMD-Datei angeben. Wenn ein Shellbefehl angegeben wird, können keine Befehlsparameter angegeben werden.<br/> |
| <span id="-tracing"></span><span id="-TRACING"></span>**-tracing**<br/>                                                  | Dieses optionale Flag generiert eine ausführliche Ausgabe, die für die Problembehandlung verwendet werden kann.<br/>                                                                                                                                                                                 |
| <span id="-wait"></span><span id="-WAIT"></span>**-wait**<br/>                                                           | Dieses optionale Flag bewirkt, dass das VShadow-Tool auf die Benutzerbestätigung wartet, bevor es beendet wird.<br/>                                                                                                                                                                          |



 

## <a name="querying-shadow-copy-properties"></a>Abfragen von Schattenkopieeigenschaften

**vshadow** **-q**

**vshadow** **-qx=**_ShadowCopySetId_

**vshadow** **-s=**_ShadowCopyId_

Die **Befehlszeilenoption -q** listet die Eigenschaften aller Schattenkopien auf dem Computer auf.

Die **Befehlszeilenoption -qx** listet die Eigenschaften aller Schattenkopien im Schattenkopiesatz auf, deren ID durch *ShadowCopySetId angegeben wird.*

Die **Befehlszeilenoption -s** listet die Eigenschaften der Schattenkopie auf, deren ID durch *ShadowCopyId angegeben wird.*

Diese Befehlszeilenoptionen verwenden eine Kombination aus [**IVssBackupComponents::Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query) und [**IVssBackupComponents::GetSnapshotProperties,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties) um die Eigenschaften der angegebenen Gruppe von Schattenkopien zu erhalten.

Die **Befehlszeilenoptionen -q,** **-qx** und **-s** schließen sich gegenseitig aus und können nicht mit anderen Befehlszeilenoptionen kombiniert werden.

## <a name="deleting-shadow-copies"></a>Löschen von Schattenkopien

**vshadow** **-da**

**vshadow** **-do**

**vshadow** **-dx=**_ShadowCopySetId_

**vshadow** **-ds=**_ShadowCopyId_

Der **Befehl -da** löscht alle Schattenkopien auf dem Computer.

> [!Note]  
> Für **die Befehlszeilenoption -da** ist eine Benutzerbestätigung erforderlich.

 

Mit **der Befehlszeilenoption -do** wird die älteste Schattenkopie auf dem Computer gelöscht.

Mit **der Befehlszeilenoption -dx** werden alle Schattenkopien im Schattenkopiesatz gelöscht, deren ID von *ShadowCopySetId angegeben wird.*

Die **Befehlszeilenoption -ds** löscht die Schattenkopie, deren ID durch *ShadowCopyId angegeben wird.*

Diese Befehlszeilenoptionen sind nur für die Verwendung mit [*persistenten Schattenkopien*](vssgloss-p.md) verfügbar. Nichtpersistente Schattenkopien müssen nicht explizit gelöscht werden, da sie automatisch gelöscht werden, wenn der VShadow-Erstellungsbefehl beendet wird.

Die **Befehlszeilenoptionen -da,** **-do,** **-dx** und **-ds** schließen sich gegenseitig aus und können nicht mit anderen Befehlszeilenoptionen kombiniert werden.

## <a name="breaking-a-shadow-copy-set"></a>Breaking a Shadow Copy Set

**vshadow** **-b=**_ShadowCopySetId_

**vshadow** **-bw=**_ShadowCopySetId_

Die **Befehlszeilenoption -b=**_ShadowCopySetId_ konvertiert jede Schattenkopie im Schattenkopiesatz in ein eigenständiges schreibgeschütztes Volume.

Die **Befehlszeilenoption -bw=**_ShadowCopySetId_ konvertiert jede Schattenkopie im Schattenkopiesatz in ein eigenständiges beschreibbares Volume.

> [!Note]  
> Die **Befehlszeilenoptionen -b** und **-bw** werden nur auf Windows Serverbetriebssystemen unterstützt.

 

Informationen zum Aufbrechen eines Schattenkopiesets finden Sie unter [Breaking Shadow Copies](breaking-shadow-copies.md).

Nachdem der Schattenkopiesatz unterbrochen wurde, sind der Schattenkopiesatz und die einzelnen Schattenkopien nicht mehr vorhanden und können nicht mehr mit VSS-Befehlen verwaltet werden.

Ein Schattenkopiesatz ist persistent, wenn er mit dem optionalen **Flag -p** erstellt wurde. Wenn der transportierbare Schattenkopiesatz nicht vorhanden ist, wird er für kurze Zeit angezeigt, während der Befehl zum Erstellen von Schattenkopien ausgeführt wird, und wird automatisch gelöscht, wenn der Befehl zurückgegeben wird. Sie können nicht vorhandene Schattenkopiesätze nur während der Erstellung von Schattenkopien durch Erstellen des Schattenkopiesets mithilfe des optionalen **Flags -exec** zum Ausführen einer CMD-Datei, die **vshadow** **-b** oder **vshadow** **-bw** aufruft, unterbricht.

Die **Befehlszeilenoptionen -b** und **-bw** schließen sich gegenseitig aus und können nicht mit anderen Befehlszeilenoptionen kombiniert werden.

## <a name="breaking-a-shadow-copy-set-using-the-breaksnapshotsetex-method"></a>Breaking a Shadow Copy Set Using the BreakSnapshotSetEx Method

**vshadow** **-bex**

Die **Befehlszeilenoption -bex** unterbricht einen Schattenkopiesatz gemäß den Optionen, die von den optionalen Flags **-mask,** **-rw,** **-forcerevert** und **-norevert angegeben** werden. Diese Befehlszeilenoption ähnelt den Befehlszeilenoptionen **-b** und **-bw.** Die **Befehlszeilenoption -bex** verwendet die [**IVssBackupComponentsEx2::BreakSnapshotSetEx-Methode,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-breaksnapshotsetex) während die Befehlszeilenoptionen **-b** und **-bw** die [**IVssBackupComponents::BreakSnapshotSet-Methode**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset) verwenden.

Informationen zum Aufbrechen eines Schattenkopiesets finden Sie unter [Breaking Shadow Copies](breaking-shadow-copies.md).

> [!Note]  
> Die **Befehlszeilenoption -bex** wird nur auf Windows Serverbetriebssystemen unterstützt.

 

**vshadow** **-bex** **-mask**

Das **Flag -mask** gibt an, dass die Schattenkopie-LUN vom Host maskiert wird. Wenn das **Flag -mask** angegeben wird, können die **Flags -rw,** **-forcerevert** und **-norevert** nicht angegeben werden.

**vshadow** **-bex** **-rw**

Das **Flag -rw** gibt an, dass die Schattenkopie-LUN für den Host als Lese-/Schreibvolumen verfügbar gemacht wird.

**vshadow** **-bex** **-forcerevert**

Das **Flag -forcerevert** gibt an, dass die Datenträgerbezeichner aller Schattenkopie-LUNs auf die der ursprünglichen LUNs zurückverwendet werden. Wenn jedoch eine der ursprünglichen LUNs auf dem System vorhanden ist, kann der Vorgang nicht durchgeführt werden, und keiner der Bezeichner wird zurückgewollt. Dieses Flag und das **Flag -norevert** schließen sich gegenseitig aus.

**vshadow** **-bex** **-norevert**

Das **Flag -norevert** gibt an, dass keiner der Schattenkopie-LUN-Datenträgerbezeichner zurückgewollt wird. Dieses Flag und das **Flag -forcerevert** schließen sich gegenseitig aus.

## <a name="exposing-a-shadow-copy-locally"></a>Lokales Verfügbarstellen einer Schattenkopie

**vshadow** **-el=**_ShadowCopyId_*_,_*_LocalEmptyDirectory_

 **vshadow** **-el=**_ShadowCopyId_*_,_*_UnusedDriveLetter_

Mit **der Befehlszeilenoption -el** wird einer persistenten Schattenkopie ein bereitgestellter Ordner oder ein Laufwerkbuchstaben zugewiesen. Beachten Sie, dass der Volumeinhalt schreibgeschützt bleibt, es sei denn, Sie rufen **anschließend vshadow** **-bw** auf, um den Schattenkopiesatz zu unterbricht.

> [!Note]  
> Nichtpersistente Schattenkopien und [*über den Client zugängliche Schattenkopien*](vssgloss-c.md) können nicht lokal verfügbar gemacht werden.

 

Wenn beispielsweise {edbed95e-7e8d-11d8-9d01-505054503030} die GUID einer vorhandenen persistenten Schattenkopie ist und X: ein nicht verwendeter Laufwerkbuchstaben ist, macht der folgende Befehl die Schattenkopie unter X verfügbar:

**vshadow** **-el={edbed95e-7e8d-11d8-9d01-505054503030},x:**

Das folgende Beispiel zeigt, wie sie dieselbe Schattenkopie unter dem bereitgestellten Ordner C verfügbar macht: \\ ShadowCopies \\ June23:

**mkdir c: \\ ShadowCopies \\ June23**

**vshadow** **-el={edbed95e-7e8d-11d8-9d01-505054503030},c: \\ ShadowCopies \\ June23**

Die **Befehlszeilenoption -el** kann nicht mit anderen Befehlszeilenoptionen kombiniert werden.

## <a name="exposing-a-shadow-copy-remotely"></a>Remote verfügbar machen einer Schattenkopie

**vshadow** **-er=**_ShadowCopyId_*_,_*_UnusedShareName_

 **vshadow** **-er=**_ShadowCopyId_*_,_*_UnusedShareName_*_,_*_PathFromRootOnShadow_

Mit **der Befehlszeilenoption -er** wird dem Stammverzeichnis (oder einem Unterverzeichnis) aus der Schattenkopie ein schreibgeschützter Freigabename zugewiesen. Beachten Sie, dass der Inhalt der Freigabe schreibgeschützt bleibt, es sei denn, Sie rufen **anschließend vshadow** **-bw** auf, um den Schattenkopiesatz zu unterbricht.

> [!Note]  
> [*Auf den Client zugängliche Schattenkopien*](vssgloss-c.md) können nicht remote verfügbar gemacht werden.

 

Wenn beispielsweise {edbed95e-7e8d-11d8-9d01-505054503030} die GUID einer vorhandenen persistenten Schattenkopie ist und freigabe 123 ein nicht verwendeter Freigabename ist, macht der folgende Befehl die Schattenkopie unter Freigabe \_ \_ 123 verfügbar:

**vshadow** **-er={edbed95e-7e8d-11d8-9d01-505054503030},share \_ 123**

Das folgende Beispiel zeigt, wie Sie nur eine Teilstruktur (mit dem Namen "Ordner1 Ordner2") derselben Schattenkopie unter \\ derselben Freigabe verfügbar machen:

**vshadow** **-er={edbed95e-7e8d-11d8-9d01-505054503030},share \_ 123,Folder1 \\ Folder2**

Die Befehlszeilenoption **-er** kann nicht mit anderen Befehlszeilenoptionen kombiniert werden.

## <a name="listing-writer-status-and-metadata"></a>Auflisten des Writerstatus und der Metadaten

**vshadow** **-ws**

**vshadow** **-wm**

**vshadow** **-wm2**

**vshadow** **-wm3**

Die **Befehlszeilenoption -ws** listet die VSS Writer auf, die derzeit auf dem Computer ausgeführt werden, und beschreibt deren Status. Dieser Befehl entspricht dem [Befehl Vssadmin list writers.](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754968(v=ws.11)) Es gibt sechs mögliche Statuswerte: Stabil, Fehler, Unbekannt, Warten auf Einfrieren, Fixiert und Warten auf Abschluss.

Die Befehlszeilenoption **-wm** listet eine Zusammenfassung der Writer-Metadaten auf, einschließlich der betroffenen Volumes.

Die Befehlszeilenoption **-wm2** listet alle Writermetadaten auf.

Die Befehlszeilenoption **-wm3** listet alle Writer-Metadaten im unformatierten XML-Format auf.

**Windows Vista und Windows Server 2003:** Die Befehlszeilenoption **-wm3** wird nicht unterstützt.

Anhand dieser Informationen können Sie bestimmen, welche Volumes in den Volumeschattenkopiesatz aufgenommen werden sollen.

> [!Note]  
> Wenn der Writerstatus Stabil oder Auf Abschluss wartet, kann der Writer als stabil betrachtet werden und für die nächste Sicherung bereit sein.

 

Die **Befehlszeilenoptionen -ws,** **-wm,** **-wm2** und **-wm3** schließen sich gegenseitig aus und können nicht mit anderen Befehlszeilenoptionen kombiniert werden.

## <a name="performing-restore-operations"></a>Ausführen von Wiederherstellungsvorgängen

**vshadow** \[ OptionalFlags \] **-r=**_Datei_ *_.xml_*

**vshadow** \[ OptionalFlags \] **-rs=**_Datei_ *_.xml_*

Die **Befehlszeilenoption -r** führt einen Wiederherstellungsvorgang aus.

Die Befehlszeilenoption **-rs** führt einen simulierten Wiederherstellungsvorgang aus.

Die *File.xml-Datei* muss eine Sicherungskomponentendokumentdatei für einen Schattenkopiesatz sein, der mit dem optionalen Flag **-t** oder **-bc** erstellt wurde.

Die Befehlszeilenoptionen **-r** und **-rs** schließen sich gegenseitig aus und können nicht mit anderen Befehlszeilenoptionen kombiniert werden.

*OptionalFlags* ist eine Bitmaske mit optionalen Flagwerten aus der folgenden Tabelle.



| Optionaler Flagwert                                                                                                            | BESCHREIBUNG                                                                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="-wi_Writer"></span><span id="-wi_writer"></span><span id="-WI_WRITER"></span>**-wi=**_Writer_<br/>             | Dieses optionale Flag überprüft, ob der angegebene Writer oder die angegebene Komponente in der Wiederherstellung enthalten ist. *Writer* kann einen Komponentenpfad, einen Writernamen, eine Writer-ID oder eine Writerinstanz-ID angeben.<br/>                                                                                    |
| <span id="-wx_Writer"></span><span id="-wx_writer"></span><span id="-WX_WRITER"></span>**-wx=**_Writer_<br/>             | Dieses optionale Flag überprüft, ob der angegebene Writer oder die angegebene Komponente von der Wiederherstellung ausgeschlossen ist. *Writer* kann einen Komponentenpfad, einen Writernamen, eine Writer-ID oder eine Writerinstanz-ID angeben.<br/>                                                                                  |
| <span id="-exec_Command"></span><span id="-exec_command"></span><span id="-EXEC_COMMAND"></span>**-exec=**_Befehl_<br/> | Dieses optionale Flag führt einen Befehl oder ein Skript zwischen den Ereignissen vor und nach der Wiederherstellung aus, die an die Writer gesendet werden. *Command* kann einen ausführbaren Shellbefehl oder eine CMD-Datei angeben. Wenn ein Shellbefehl angegeben wird, können keine Befehlsparameter angegeben werden.<br/> |
| <span id="-tracing"></span><span id="-TRACING"></span>**-tracing**<br/>                                                  | Dieses optionale Flag generiert eine ausführliche Ausgabe, die für die Problembehandlung verwendet werden kann.<br/>                                                                                                                                                                                       |



 

## <a name="reverting-to-a-previous-shadow-copy"></a>Kehren zu einer vorherigen Schattenkopie zurück

**vshadow** **-revert=**_ShadowCopyId_

> [!Note]  
> Diese Befehlszeilenoption wird nur unter Windows Serverbetriebssystemen unterstützt.

 

**Windows Server 2008 und Windows Server 2003:** Wird nicht unterstützt.

Mit der Befehlszeilenoption **-revert** wird ein Volume auf die vorherige Schattenkopie zurückgesetzt, deren ID von *ShadowCopyId* angegeben wird.

Die Befehlszeilenoption **-revert** kann nicht mit anderen Befehlszeilenoptionen kombiniert werden.

## <a name="resynchronizing-luns"></a>Erneutes Synchronisieren von LUNs

**vshadow** **-addresync=**_ShadowCopyId_ **-resync=**_BCDFileName_ \[ OptionalResyncFlags\]

**vshadow** **-addresync=**_ShadowCopyId_*_,_* *TargetVolumeDriveLetter* **-resync=**_BCDFileName_ \[ OptionalResyncFlags\]

Die Befehlszeilenoption **-addresync** gibt die Volumes an, die in einen LUN-Neusynchronisierungsvorgang eingeschlossen werden sollen. Der *ShadowCopyId-Parameter* gibt den Bezeichner der Schattenkopie an. Der optionale *TargetVolumeDriveLetter-Parameter* gibt das Zielvolume an, auf das der Inhalt des Schattenkopievolumes kopiert werden soll.

Die Befehlszeilenoption **-resync** initiiert einen LUN-Neusynchronisierungsvorgang. Nach Abschluss des Vorgangs sollte die Signatur jeder Ziel-LUN mit der Signatur der Zielvolume-LUN identisch sein. Der *BCDFileName-Parameter* gibt den Namen der XML-Datei an, die das Sicherungskomponentendokument enthält.

> [!Note]  
> Die Befehlszeilenoptionen **-addresync** und **-resync** werden nur auf Windows Serverbetriebssystemen unterstützt.

 

**Windows Server 2008 und Windows Server 2003:** Wird nicht unterstützt.

*OptionalResyncFlags* ist eine Bitmaske mit optionalen Flagwerten aus der folgenden Tabelle.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Optionaler Flagwert</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="-revertsig"></span><span id="-REVERTSIG"></span><strong>-revertsig</strong><br/></td>
<td>Dieses optionale Flag gibt an, dass die Signatur jeder Ziel-LUN nach Abschluss des Vorgangs mit der Signatur der ursprünglichen LUN identisch sein sollte, die zum Erstellen der Schattenkopie verwendet wurde, nicht der Zielvolume-LUN.<br/>
<blockquote>
[!Note]<br />
Das Flag <strong>-revertsig</strong> wird nur auf Windows Serverbetriebssystemen unterstützt.
</blockquote>
<br/> <strong>Windows Server 2008 und Windows Server 2003:</strong> Wird nicht unterstützt.<br/></td>
</tr>
<tr class="even">
<td><span id="-novolcheck"></span><span id="-NOVOLCHECK"></span><strong>-novolcheck</strong><br/></td>
<td>Dieses optionale Flag gibt an, dass der VSS-Dienst nicht auf nicht ausgewählte Volumes prüfen soll, die durch den LUN-Neusynchronisierungsvorgang überschrieben werden.<br/>
<blockquote>
[!Note]<br />
Das Flag <strong>-novolcheck</strong> wird nur auf Windows Serverbetriebssystemen unterstützt.
</blockquote>
<br/> <strong>Windows Server 2008 und Windows Server 2003:</strong> Wird nicht unterstützt.<br/></td>
</tr>
</tbody>
</table>



 

 

 
