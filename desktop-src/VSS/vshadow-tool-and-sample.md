---
description: Vshadow ist ein Befehlszeilen Tool, das Sie zum Erstellen und Verwalten von Volumeschattenkopien verwenden können.
ms.assetid: 19109f92-b9da-4df7-8628-374e37a3f624
title: Vshadow-Tool und-Beispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad7a9a697ecdf39f91d43fa0c66faebd37cfbfed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485027"
---
# <a name="vshadow-tool-and-sample"></a>Vshadow-Tool und-Beispiel

Vshadow ist ein Befehlszeilen Tool, das Sie zum Erstellen und Verwalten von Volumeschattenkopien verwenden können.

> [!Note]  
> Vshadow ist im Microsoft Windows Software Development Kit (SDK) für Windows Vista und höher enthalten. Das VSS 7,2 SDK enthält eine Version von vshadow, die nur unter Windows Server 2003 ausgeführt wird. Weitere Informationen zum Herunterladen der Windows SDK und des VSS 7,2 SDK finden Sie unter [Volumeschattenkopie-Dienst](volume-shadow-copy-service-portal.md).

 

Das vshadow-Tool verwendet Befehlszeilenoptionen und optionale Flags, um die auszuführenden Aufgaben zu identifizieren. Bei Verwendung ohne Befehlszeilenoptionen erstellt der vshadow-Befehl einen neuen Schattenkopiesatz.

Vshadow-Befehle führen die folgenden Vorgänge aus:

-   [Erstellen eines schattenkopiesatzes](#creating-a-shadow-copy-set)
-   [Importieren eines schattenkopiesatzes](#importing-a-shadow-copy-set)
-   [Abfragen von schattenkopieeigenschaften](#querying-shadow-copy-properties)
-   [Löschen von Schatten Kopien](#deleting-shadow-copies)
-   [Unterbrechen eines schattenkopiesatzes](#breaking-a-shadow-copy-set)
-   [Unterbrechen eines schattenkopiessets mithilfe der breaksnapshotsetex-Methode](#breaking-a-shadow-copy-set-using-the-breaksnapshotsetex-method)
-   [Lokales verfügbar machen einer Schatten Kopie](#exposing-a-shadow-copy-locally)
-   [Remote verfügbar machen einer Schatten Kopie](#exposing-a-shadow-copy-remotely)
-   [Auflisten des Writer-Status und der Metadaten](#listing-writer-status-and-metadata)
-   [Ausführen von Wiederherstellungsoperationen](#performing-restore-operations)
-   [Zurücksetzen auf eine vorherige Schatten Kopie](#reverting-to-a-previous-shadow-copy)
-   [Neusynchronisierung von LUNs](#resynchronizing-luns)

## <a name="creating-a-shadow-copy-set"></a>Erstellen eines schattenkopiesatzes

**vshadow** \[ Optionalflags \] *volumelist*

Dieser Befehl erstellt einen neuen Schattenkopiesatz.

*Volumelist* ist eine Liste von Volumenamen. Vshadow erstellt eine Schatten Kopie für jedes Volume in der Liste. Ein Volumename kann optional mit einem umgekehrten Schrägstrich ( \\ ) beendet werden. Beispielsweise sind "c:" und "c:" \\ gültige Volumenamen. Sie können auch bereitgestellte Ordner (z. b. C: \\ Directoren Name) oder VolumeGuid-Namen angeben (z. b. \\ \\ ? \\ Volume {edbed95e-7e8d-11d8-9d01-505054503030}).

*Optionalflags* ist eine Bitmaske Optionaler Flagwerte aus der folgenden Tabelle.



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
<td><span id="-ad"></span><span id="-AD"></span><strong>-AD</strong><br/></td>
<td>Dieses optionale Flag gibt differenzielle Hardware Schatten Kopien an. Dieses Flag und das <strong>-AP-</strong> Flag schließen sich gegenseitig aus.<br/>
<blockquote>
[!Note]<br />
Dieses Flag wird nur unter Windows Server-Betriebssystemen unterstützt.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="-ap"></span><span id="-AP"></span><strong>-AP</strong><br/></td>
<td>Dieses optionale Flag gibt Plex-Hardware Schatten Kopien an. Dieses Flag und das <strong>-AD-</strong> Flag schließen sich gegenseitig aus.<br/>
<blockquote>
[!Note]<br />
Dieses Flag wird nur unter Windows Server-Betriebssystemen unterstützt.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="_-bc_File.xml"></span><span id="_-bc_file.xml"></span><span id="_-BC_FILE.XML"></span><strong></strong> <strong>-BC =</strong><em>File</em><strong>. XML</strong><br/></td>
<td>Dieses optionale Flag gibt nicht transportable-Schatten Kopien an und speichert das Dokument mit den Sicherungs Komponenten in der angegebenen Datei. Diese Datei kann in einem nachfolgenden Wiederherstellungs Vorgang verwendet werden. Dieses Flag und das <strong>-t-</strong> Flag schließen sich gegenseitig aus.<br/>
<blockquote>
[!Note]<br />
Dieses Flag wird nur unter Windows Server-Betriebssystemen unterstützt.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="-exec_Command"></span><span id="-exec_command"></span><span id="-EXEC_COMMAND"></span><strong>-exec =</strong><em>Befehl</em><br/></td>
<td>Dieses optionale Flag führt einen Befehl oder ein Skript aus, nachdem die Schatten Kopien erstellt wurden, aber bevor das vshadow-Tool beendet wird. Der <em>Befehl</em> kann einen ausführbaren Shellbefehl oder eine cmd-Datei angeben. Wenn Sie einen Shellbefehl angibt, können keine Befehlsparameter angegeben werden.<br/>
<blockquote>
[!Note]<br />
Aus Sicherheitsgründen und um die Implementierung einfach zu halten, akzeptiert das optionale Flag <strong>-exec</strong> keine Parameter, die an den Befehl oder das Skript weitergegeben werden. Die gesamte Zeichenfolge, die an das optionale Flag <strong>-exec</strong> übergeben wird, wird als einzelne cmd-oder exe-Datei behandelt. Weitere Informationen zu dieser Einschränkung finden Sie im vshadow-Quellcode.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="-forcerevert"></span><span id="-FORCEREVERT"></span><strong>-forcerevert</strong><br/></td>
<td>Dieses optionale Flag gibt an, dass der Schattenkopievorgang nur dann abgeschlossen werden soll, wenn alle Datenträger Signaturen wieder hergestellt werden können.<br/>
<blockquote>
[!Note]<br />
Dieses Flag wird nur unter Windows Server-Betriebssystemen unterstützt.
</blockquote>
<br/> <strong>Windows Server 2003:</strong> Nicht unterstützt.<br/></td>
</tr>
<tr class="even">
<td><span id="-mask"></span><span id="-MASK"></span><strong>-Mask</strong><br/></td>
<td>Dieses optionale Flag gibt an, dass die schattenkopieluns vom Computer maskiert werden sollen, wenn der Schattenkopiesatz beschädigt ist.<br/>
<blockquote>
[!Note]<br />
Dieses Flag wird nur unter Windows Server-Betriebssystemen unterstützt.
</blockquote>
<br/> <strong>Windows Server 2003:</strong> Nicht unterstützt.<br/></td>
</tr>
<tr class="odd">
<td><span id="-nar"></span><span id="-NAR"></span><strong>-Nar</strong><br/></td>
<td>Dieses optionale Flag gibt Schatten Kopien ohne automatische Wiederherstellung an. Weitere Informationen zu dieser Option finden Sie in der Dokumentation für das VSS_VOLSNAP_ATTR_NO_AUTORECOVERY-Flag der <a href="/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes"><strong>_VSS_VOLUME_SNAPSHOT_ATTRIBUTES</strong></a> -Enumeration.<br/></td>
</tr>
<tr class="even">
<td><span id="-norevert"></span><span id="-NOREVERT"></span><strong>-norevert</strong><br/></td>
<td>Dieses optionale Flag gibt an, dass Datenträger Signaturen nicht rückgängig gemacht werden sollen.<br/>
<blockquote>
[!Note]<br />
Dieses Flag wird nur unter Windows Server-Betriebssystemen unterstützt.
</blockquote>
<br/> <strong>Windows Server 2003:</strong> Nicht unterstützt.<br/></td>
</tr>
<tr class="odd">
<td><span id="-nw"></span><span id="-NW"></span><strong>-NW</strong><br/></td>
<td>Dieses optionale Flag gibt Schatten Kopien an, ohne dass Writer einbezogen werden. Weitere Informationen zu Schatten Kopien ohne Writer-Beteiligung finden Sie unter <a href="shadow-copy-creation-details.md">Details zur Erstellung von Schatten</a>Kopien. Dieses Flag und die Flags " <strong>-Wi</strong> " und " <strong>-WX</strong> " schließen sich gegenseitig aus.<br/></td>
</tr>
<tr class="even">
<td><span id="-p"></span><span id="-P"></span><strong>-p</strong><br/></td>
<td>Dieses optionale Flag gibt <a href="vssgloss-p.md"><em>persistente Schatten Kopien</em></a>an.<br/>
<blockquote>
[!Note]<br />
Dieses Flag wird nur unter Windows Server-Betriebssystemen unterstützt.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="-rw"></span><span id="-RW"></span><strong>-RW</strong><br/></td>
<td>Dieses optionale Flag gibt an, dass die schattenkopieluns als Lese-/Schreibzugriff festgelegt werden, wenn der Schattenkopiesatz<br/>
<blockquote>
[!Note]<br />
Dieses Flag wird nur unter Windows Server-Betriebssystemen unterstützt.
</blockquote>
<br/> <strong>Windows Server 2003:</strong> Nicht unterstützt.<br/></td>
</tr>
<tr class="even">
<td><span id="-scsf"></span><span id="-SCSF"></span><strong>-SCSF</strong><br/></td>
<td>Dieses optionale Flag gibt die <a href="vssgloss-c.md"><em>Client zugänglichen Schatten Kopien</em></a>an.<br/>
<blockquote>
[!Note]<br />
Dieses Flag wird nur unter Windows Server-Betriebssystemen unterstützt.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="-script_File.cmd"></span><span id="-script_file.cmd"></span><span id="-SCRIPT_FILE.CMD"></span><strong>-Script =</strong><em>File</em><strong>. cmd</strong><br/></td>
<td>Dieses optionale Flag generiert eine cmd-Datei, die Umgebungsvariablen enthält, die sich auf die erstellten Schatten Kopien beziehen, z. b. schattenkopienids und IDs von Schatten Kopien<br/></td>
</tr>
<tr class="even">
<td><span id="-t_File.xml"></span><span id="-t_file.xml"></span><span id="-T_FILE.XML"></span><strong>-t =</strong><em>File</em><strong>. XML</strong><br/></td>
<td>Dieses optionale Flag gibt austauschen-Schatten Kopien an und speichert das Dokument mit den Sicherungs Komponenten in der Datei, die durch den <em>File.xml</em> -Parameter angegeben wird. Diese Datei kann in einem nachfolgenden Import-und/oder Wiederherstellungs Vorgang verwendet werden. Dieses Flag und das <strong>-BC-</strong> Flag schließen sich gegenseitig aus.<br/> <strong>Windows Server 2003, Standard Edition und Windows Server 2003, Web Edition:</strong> Transportable-Schatten Kopien werden nicht unterstützt. Alle Editionen von Windows Server 2003 mit Service Pack 1 (SP1) unterstützen austauschen-Schatten Kopien.<br/></td>
</tr>
<tr class="odd">
<td><span id="-tr"></span><span id="-TR"></span><strong>-TR</strong><br/></td>
<td>Dieses optionale Flag gibt an, dass die TxF-Wiederherstellung während der Erstellung von Schatten Kopien erzwungen werden soll.<br/>
<blockquote>
[!Note]<br />
Dieses Flag wird nur unter Windows Server-Betriebssystemen unterstützt.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="-tracing"></span><span id="-TRACING"></span><strong>-Ablauf Verfolgung</strong><br/></td>
<td>Dieses optionale Flag generiert eine ausführliche Ausgabe, die für die Problembehandlung verwendet werden kann.<br/></td>
</tr>
<tr class="odd">
<td><span id="-wait"></span><span id="-WAIT"></span><strong>-Wait</strong><br/></td>
<td>Dieses optionale Flag bewirkt, dass das vshadow-Tool vor dem Beenden auf eine Benutzer Bestätigung wartet.<br/></td>
</tr>
<tr class="even">
<td><span id="-wi_Writer"></span><span id="-wi_writer"></span><span id="-WI_WRITER"></span><strong>-Wi =</strong><em>Writer</em><br/></td>
<td>Dieses optionale Flag überprüft, ob der angegebene Writer oder die angegebene Komponente in der Schatten Kopie enthalten ist. Der <em>Writer</em> kann einen Komponenten Pfad, einen Writer-Namen, eine Writer-ID oder eine Writer-Instanz-ID angeben. Dieses Flag und das <strong>-NW-</strong> Flag schließen sich gegenseitig aus.<br/></td>
</tr>
<tr class="odd">
<td><span id="-wx_Writer"></span><span id="-wx_writer"></span><span id="-WX_WRITER"></span><strong>-WX =</strong><em>Writer</em><br/></td>
<td>Dieses optionale Flag überprüft, ob der angegebene Writer oder die Komponente von der Schatten Kopie ausgeschlossen ist. Der <em>Writer</em> kann einen Komponenten Pfad, einen Writer-Namen, eine Writer-ID oder eine Writer-Instanz-ID angeben. Dieses Flag und das <strong>-NW-</strong> Flag schließen sich gegenseitig aus.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="importing-a-shadow-copy-set"></a>Importieren eines schattenkopiesatzes

**vshadow** \[ Optionalflags \] **-i =**_File_*_. XML_*

Mit der Befehlszeilenoption **-i** wird ein austauschen-Schattenkopiesatz importiert.

> [!Note]  
> Diese Befehlszeilenoption wird nur unter Windows Server-Betriebssystemen unterstützt.

 

Bei der *File.xml* -Datei muss es sich um eine Sicherungs Komponenten-Dokument Datei für einen austauschen-Schatten Kopier Satz handeln, der mit dem optionalen **-t-** oder **-BC-** Flag erstellt wurde.

Ein Schattenkopiesatz ist eine [*persistente Schatten Kopie*](vssgloss-p.md) , wenn er mit dem optionalen **-p-** Flag erstellt wurde. Wenn der über austauschen Schattenkopiesatz nicht persistent ist, wird er für kurze Zeit angezeigt, während der Befehl zum Erstellen von Schatten Kopien ausgeführt wird, und wird automatisch gelöscht, wenn der Befehl zurückgegeben wird. Sie können nicht persistente Schatten Kopien nur während der Erstellung von Schatten Kopien importieren, indem Sie den Schattenkopiesatz erstellen, indem Sie das optionale Flag **-exec** zum Ausführen einer cmd-Datei verwenden, die vshadow **-i** aufruft.

Die Befehlszeilenoption " **-i** " kann nicht mit anderen Befehlszeilenoptionen kombiniert werden.

*Optionalflags* ist eine Bitmaske Optionaler Flagwerte aus der folgenden Tabelle.



| Optionaler Flagwert                                                                                                            | BESCHREIBUNG                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="-exec_Command"></span><span id="-exec_command"></span><span id="-EXEC_COMMAND"></span>**-exec =**_Befehl_<br/> | Dieses optionale Flag führt einen Befehl oder ein Skript aus, nachdem die Schatten Kopien importiert wurden, aber bevor das vshadow-Tool beendet wird. Der *Befehl* kann einen ausführbaren Shellbefehl oder eine cmd-Datei angeben. Wenn Sie einen Shellbefehl angibt, können keine Befehlsparameter angegeben werden.<br/> |
| <span id="-tracing"></span><span id="-TRACING"></span>**-Ablauf Verfolgung**<br/>                                                  | Dieses optionale Flag generiert eine ausführliche Ausgabe, die für die Problembehandlung verwendet werden kann.<br/>                                                                                                                                                                                 |
| <span id="-wait"></span><span id="-WAIT"></span>**-Wait**<br/>                                                           | Dieses optionale Flag bewirkt, dass das vshadow-Tool vor dem Beenden auf eine Benutzer Bestätigung wartet.<br/>                                                                                                                                                                          |



 

## <a name="querying-shadow-copy-properties"></a>Abfragen von schattenkopieeigenschaften

**vshadow** **-q**

**vshadow** **-qx =**_Shadowcopy* TID_

**vshadow** **-s =**_shadowcopyid_

Die Befehlszeilenoption **-q** listet die Eigenschaften aller Schatten Kopien auf dem Computer auf.

Die Befehlszeilenoption **-qx** listet die Eigenschaften aller Schatten Kopien im Schattenkopiesatz auf, deren ID von *shadowcopysetid* angegeben wird.

Die Befehlszeilenoption **-s** listet die Eigenschaften der Schatten Kopie auf, deren ID von *shadowcopyid* angegeben wird.

Diese Befehlszeilenoptionen verwenden eine Kombination aus [**IVssBackupComponents:: Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query) und [**IVssBackupComponents:: getionnapshotproperties**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties) , um die Eigenschaften des angegebenen Satzes von Schatten Kopien zu erhalten.

Die Befehlszeilenoptionen **-q**, **-qx** und **-s** schließen sich gegenseitig aus und können nicht mit anderen Befehlszeilenoptionen kombiniert werden.

## <a name="deleting-shadow-copies"></a>Löschen von Schatten Kopien

**vshadow** **-da**

**vshadow** **-do**

**vshadow** **-DX =**_Shadowcopy* TID_

**vshadow** **-DS =**_shadowcopyid_

Der **-da-** Befehl löscht alle Schatten Kopien auf dem Computer.

> [!Note]  
> Die Befehlszeilenoption " **-da** " erfordert eine Bestätigung des Benutzers.

 

Mit der Befehlszeilenoption **-DO** wird die älteste Schatten Kopie auf dem Computer gelöscht.

Mit der Befehlszeilenoption **-DX** werden alle Schatten Kopien im Schattenkopiesatz gelöscht, deren ID von *shadowcopysetid* angegeben wird.

Die Befehlszeilenoption **-DS** löscht die Schatten Kopie, deren ID von *shadowcopyid* angegeben wird.

Diese Befehlszeilenoptionen sind nur für die Verwendung mit [*permanenten Schatten Kopien*](vssgloss-p.md) vorgesehen. Nicht persistente Schatten Kopien müssen nicht explizit gelöscht werden, da Sie automatisch gelöscht werden, wenn der vshadow-Erstellungs Befehl beendet wird.

Die Befehlszeilenoptionen " **-da**", "- **do**", " **-DX**" und " **-DS** " schließen sich gegenseitig aus und können nicht mit anderen Befehlszeilenoptionen kombiniert werden.

## <a name="breaking-a-shadow-copy-set"></a>Unterbrechen eines schattenkopiesatzes

**vshadow** **-b =**_Shadowcopy* TID_

**vshadow** **-BW =**_Shadowcopy* TID_

Mit der Befehlszeilenoption **-b =**_shadowcopysetid_ wird jede Schatten Kopie im Schattenkopiesatz in ein eigenständiges Schreib geschütztes Volume konvertiert.

Die Befehlszeilenoption **-BW =**_shadowcopysetid_ konvertiert jede Schatten Kopie im Schattenkopiesatz in ein eigenständiges beschreibbares Volume.

> [!Note]  
> Die Befehlszeilenoptionen **-b** und **-BW** werden nur unter Windows Server-Betriebssystemen unterstützt.

 

Informationen zum Unterbrechen eines schattenkopiessets finden Sie unter [Breaking Shadow-Kopien](breaking-shadow-copies.md).

Nachdem der Schattenkopiesatz getrennt wurde, sind der Schattenkopiesatz und die einzelnen Schatten Kopien nicht mehr vorhanden und können nicht mithilfe von VSS-Befehlen verwaltet werden.

Ein Schattenkopiesatz ist persistent, wenn er mit dem optionalen **-p-** Flag erstellt wurde. Wenn der über austauschen Schattenkopiesatz nicht persistent ist, wird er für kurze Zeit angezeigt, während der Befehl zum Erstellen von Schatten Kopien ausgeführt wird, und wird automatisch gelöscht, wenn der Befehl zurückgegeben wird. Sie können nicht persistente Schatten Kopien nur während der Erstellung von Schatten Kopien unterbrechen, indem Sie den Schattenkopiesatz erstellen, indem Sie das optionale Flag **-exec** verwenden, um eine cmd-Datei auszuführen, die **vshadow** **-b** oder **vshadow** **-BW** aufruft.

Die Befehlszeilenoptionen " **-b** " und " **-BW** " schließen sich gegenseitig aus und können nicht mit anderen Befehlszeilenoptionen kombiniert werden.

## <a name="breaking-a-shadow-copy-set-using-the-breaksnapshotsetex-method"></a>Unterbrechen eines schattenkopiessets mithilfe der breaksnapshotsetex-Methode

**vshadow** **-BEx**

Die Befehlszeilenoption " **-BEx** " unterbricht einen Schattenkopiesatz gemäß den Optionen, die durch die optionalen **-Mask-**,- **RW**-, **-forcerevert**-und **-norevert** -Flags angegeben werden. Diese Befehlszeilenoption ähnelt den Befehlszeilenoptionen **-b** und **-BW** . Die Befehlszeilenoption **-BEx** verwendet die [**IVssBackupComponentsEx2:: breaksnapshotsetex**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-breaksnapshotsetex) -Methode, wohingegen die Befehlszeilenoptionen **-b** und **-BW** die [**IVssBackupComponents:: breaksnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset) -Methode verwenden.

Informationen zum Unterbrechen eines schattenkopiessets finden Sie unter [Breaking Shadow-Kopien](breaking-shadow-copies.md).

> [!Note]  
> Die Befehlszeilenoption **-BEx** wird nur unter Windows Server-Betriebssystemen unterstützt.

 

**vshadow** **-BEx** **-Mask**

Das Flag **-Mask** gibt an, dass die LUN der Schatten Kopie vom Host maskiert wird. Wenn das Flag " **-Mask** " angegeben ist, können die Flags " **-RW**", " **-forcerevert**" und " **-norevert** " nicht angegeben werden.

**vshadow** **-BEx** **-RW**

Das Flag **-RW** gibt an, dass die LUN der Schatten Kopie als Lese-/schreibvolume für den Host verfügbar gemacht wird.

**vshadow** **-BEx** **-forcerevert**

Das Flag " **-forcerevert** " gibt an, dass die Datenträger Bezeichner aller schattenkopieluns auf die der ursprünglichen LUNs zurückgesetzt werden. Wenn jedoch eine der ursprünglichen LUNs auf dem System vorhanden ist, schlägt der Vorgang fehl, und keiner der Bezeichner wird wieder hergestellt. Dieses Flag und das **-norevert-** Flag schließen sich gegenseitig aus.

**vshadow** **-BEx** **-norevert**

Das Flag " **-norevert** " gibt an, dass keine der Datenträger-IDs der schattenkopiedatenträger wieder hergestellt werden. Dieses Flag und das Flag " **-forcerevert** " schließen sich gegenseitig aus.

## <a name="exposing-a-shadow-copy-locally"></a>Lokales verfügbar machen einer Schatten Kopie

**vshadow** **-El =**_shadowcopyid_*_,_*_localemptydirectory_

 **vshadow** **-El =**_shadowcopyid_*_,_*_unuseddriveletter_

Mit der Befehlszeilenoption-El wird einem permanenten Schatten Kopiervorgang ein bereit **gestellter** Ordner oder ein Laufwerksbuchstabe zugewiesen. Beachten Sie, dass die volumeinhalte schreibgeschützt bleiben, es sei denn, Sie nennen anschließend **vshadow** **-BW** , um den Schattenkopiesatz zu unterbrechen

> [!Note]  
> Nicht persistente Schatten Kopien und [*Client barrierefreie Schatten Kopien*](vssgloss-c.md) können nicht lokal verfügbar gemacht werden.

 

Wenn {edbed95e-7e8d-11d8-9d01-505054503030} z. b. die GUID einer vorhandenen persistenten Schatten Kopie und X: ein nicht verwendeter Laufwerk Buchstabe ist, macht der folgende Befehl die Schatten Kopie unter X verfügbar:

**vshadow** **-El = {edbed95e-7e8d-11d8-9d01-505054503030}, x:**

Im folgenden Beispiel wird gezeigt, wie die gleiche Schatten Kopie unter dem bereitgestellten Ordner C: \\ Shadowcopy June23 verfügbar gemacht wird \\ :

**mkdir c: \\ shadowkopien \\ June23**

**vshadow** **-El = {edbed95e-7e8d-11d8-9d01-505054503030}, c: \\ shadowkopien \\ June23**

Die Befehlszeilenoption **-El** kann nicht mit anderen Befehlszeilenoptionen kombiniert werden.

## <a name="exposing-a-shadow-copy-remotely"></a>Remote verfügbar machen einer Schatten Kopie

**vshadow** **-er =**_shadowcopyid_*_,_*_unusedsharename_

 **vshadow** **-er =**_shadowcopyid_*_,_*_unusedsharename_*_,_*_pathfromrootonshadow_

Die Befehlszeilenoption **-er** weist der Schatten Kopie einen schreibgeschützten Freigabe Namen (oder ein Unterverzeichnis) dem Stammverzeichnis zu. Beachten Sie, dass der Inhalt der Freigabe weiterhin schreibgeschützt bleibt, es sei denn, Sie werden anschließend **vshadow** **-BW** aufgerufen, um den Schattenkopiesatz

> [!Note]  
> Die vom [*Client zugänglichen Schatten Kopien*](vssgloss-c.md) können nicht Remote verfügbar gemacht werden.

 

Wenn {edbed95e-7e8d-11d8-9d01-505054503030} z. b. die GUID einer vorhandenen persistenten Schatten Kopie und Share 123 ein nicht verwendeter \_ Freigabe Name ist, macht der folgende Befehl die Schatten Kopie unter Freigabe \_ 123 verfügbar:

**vshadow** **-er = {edbed95e-7e8d-11d8-9d01-505054503030}, Freigabe \_ 123**

Im folgenden Beispiel wird gezeigt, wie Sie nur eine Teilstruktur (mit dem Namen "" Ordner1 " \\ Folder2") derselben Schatten Kopie in derselben Freigabe verfügbar machen:

**vshadow** **-er = {edbed95e-7e8d-11d8-9d01-505054503030}, Freigabe \_ 123, "Ordner1" \\ Folder2**

Die Befehlszeilenoption **-er** kann nicht mit anderen Befehlszeilenoptionen kombiniert werden.

## <a name="listing-writer-status-and-metadata"></a>Auflisten des Writer-Status und der Metadaten

**vshadow** **-WS**

**vshadow** **-WM**

**vshadow** **-wm2**

**vshadow** **-WM3**

Mit der Befehlszeilenoption **-WS** werden die VSS-Writer aufgelistet, die derzeit auf dem Computer ausgeführt werden, und Ihr Status wird beschrieben. Dieser Befehl entspricht dem Befehl [vssadmin List Writers](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754968(v=ws.11)) . Es gibt sechs mögliche Zustands Werte: "stabil", "Fehler", "unbekannt", "warten auf Einfrieren", "fixiert" und "warten auf Abschluss

Die Befehlszeilenoption **-WM** listet eine Zusammenfassung der Writer-Metadaten auf, einschließlich der betroffenen Volumes.

Die Befehlszeilenoption **-wm2** listet alle Writer-Metadaten auf.

Die Befehlszeilenoption **-WM3** listet alle Writer-Metadaten im unformatierten XML-Format auf.

**Windows Vista und Windows Server 2003:** Die Befehlszeilenoption **-WM3** wird nicht unterstützt.

Sie können diese Informationen verwenden, um zu bestimmen, welche Volumes in den Volumeschattenkopie-Satz eingeschlossen werden sollen.

> [!Note]  
> Wenn der Writer-Zustand stabil ist oder auf den Abschluss wartet, kann der Writer als stabiler Zustand angesehen werden, der für die nächste Sicherung bereit ist.

 

Die Befehlszeilenoptionen **-WS**, **-WM**, **-wm2** und **-WM3** schließen sich gegenseitig aus und können nicht mit anderen Befehlszeilenoptionen kombiniert werden.

## <a name="performing-restore-operations"></a>Ausführen von Wiederherstellungsoperationen

**vshadow** \[ Optionalflags \] **-r =**_File_*_. XML_*

**vshadow** \[ Optionalflags \] **-RS =**_File_*_. XML_*

Die Befehlszeilenoption **-r** führt einen Wiederherstellungs Vorgang aus.

Die Befehlszeilenoption **-RS** führt einen simulierten Wiederherstellungs Vorgang aus.

Die *File.xml* Datei muss eine Sicherungs Komponenten-Dokument Datei für einen Schattenkopiesatz sein, der mit dem optionalen **-t-** oder **-BC-** Flag erstellt wurde.

Die Befehlszeilenoptionen " **-r** " und " **-RS** " schließen sich gegenseitig aus und können nicht mit anderen Befehlszeilenoptionen kombiniert werden.

*Optionalflags* ist eine Bitmaske Optionaler Flagwerte aus der folgenden Tabelle.



| Optionaler Flagwert                                                                                                            | BESCHREIBUNG                                                                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="-wi_Writer"></span><span id="-wi_writer"></span><span id="-WI_WRITER"></span>**-Wi =**_Writer_<br/>             | Dieses optionale Flag überprüft, ob der angegebene Writer oder die Komponente in die Wiederherstellung eingeschlossen ist. Der *Writer* kann einen Komponenten Pfad, einen Writer-Namen, eine Writer-ID oder eine Writer-Instanz-ID angeben.<br/>                                                                                    |
| <span id="-wx_Writer"></span><span id="-wx_writer"></span><span id="-WX_WRITER"></span>**-WX =**_Writer_<br/>             | Dieses optionale Flag überprüft, ob der angegebene Writer oder die Komponente von der Wiederherstellung ausgeschlossen ist. Der *Writer* kann einen Komponenten Pfad, einen Writer-Namen, eine Writer-ID oder eine Writer-Instanz-ID angeben.<br/>                                                                                  |
| <span id="-exec_Command"></span><span id="-exec_command"></span><span id="-EXEC_COMMAND"></span>**-exec =**_Befehl_<br/> | Dieses optionale Flag führt einen Befehl oder ein Skript zwischen den Ereignissen vor und nach der Wiederherstellung aus, die an die Writer gesendet werden. Der *Befehl* kann einen ausführbaren Shellbefehl oder eine cmd-Datei angeben. Wenn Sie einen Shellbefehl angibt, können keine Befehlsparameter angegeben werden.<br/> |
| <span id="-tracing"></span><span id="-TRACING"></span>**-Ablauf Verfolgung**<br/>                                                  | Dieses optionale Flag generiert eine ausführliche Ausgabe, die für die Problembehandlung verwendet werden kann.<br/>                                                                                                                                                                                       |



 

## <a name="reverting-to-a-previous-shadow-copy"></a>Zurücksetzen auf eine vorherige Schatten Kopie

**vshadow** **-Revert =**_shadowcopyid_

> [!Note]  
> Diese Befehlszeilenoption wird nur unter Windows Server-Betriebssystemen unterstützt.

 

**Windows Server 2008 und Windows Server 2003:** Nicht unterstützt.

Mit der Befehlszeilenoption **-Revert** wird ein Volume auf die vorherige Schatten Kopie zurückgesetzt, deren ID von *shadowcopyid* angegeben wird.

Die Befehlszeilenoption ' **-Revert** ' kann nicht mit anderen Befehlszeilenoptionen kombiniert werden.

## <a name="resynchronizing-luns"></a>Neusynchronisierung von LUNs

**vshadow** **-adresssync =**_shadowcopyid_ **-Resync =**_bcdfilename_ \[ optionalresyncflags\]

**vshadow** **-adresssync =**_shadowcopyid_*_,_* *targetvolumedriveletter* **-Resync =**_bcdfilename_ \[ optionalresyncflags\]

Mit der Befehlszeilenoption **-adresssync** werden die Volumes angegeben, die in einen LUN-Neusynchronisierungs Vorgang eingeschlossen werden sollen. Der *shadowcopyid* -Parameter gibt den Bezeichner der Schatten Kopie an. Der optionale Parameter *targetvolumedriveletter* gibt das Ziel Volume an, in das der Inhalt des schattenkopiespeichervolumes kopiert werden soll.

Mit der Befehlszeilenoption **-Resync** wird ein LUN-Vorgang für die erneute Synchronisierung initiiert. Nachdem der Vorgang beendet wurde, sollte die Signatur der einzelnen Ziel-LUN mit der Signatur der Ziel Volume-LUN identisch sein. Der *bcdfilename* -Parameter gibt den Namen der XML-Datei an, die das Sicherungs Komponenten Dokument enthält.

> [!Note]  
> Die Befehlszeilenoptionen **-adresssync** und **-Resync** werden nur unter Windows Server-Betriebssystemen unterstützt.

 

**Windows Server 2008 und Windows Server 2003:** Nicht unterstützt.

*Optionalresyncflags* ist eine Bitmaske Optionaler Flagwerte aus der folgenden Tabelle.



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
<td>Dieses optionale Flag gibt an, dass die Signatur der einzelnen Ziel-LUN nach Abschluss des Vorgangs mit der ursprünglichen LUN identisch sein sollte, mit der die Schatten Kopie erstellt wurde, nicht mit der Ziel Volume-LUN.<br/>
<blockquote>
[!Note]<br />
Das Flag " <strong>-revertsig</strong> " wird nur unter Windows Server-Betriebssystemen unterstützt.
</blockquote>
<br/> <strong>Windows Server 2008 und Windows Server 2003:</strong> Nicht unterstützt.<br/></td>
</tr>
<tr class="even">
<td><span id="-novolcheck"></span><span id="-NOVOLCHECK"></span><strong>-novolcheck</strong><br/></td>
<td>Dieses optionale Flag gibt an, dass der VSS-Dienst nicht nach nicht ausgewählten Volumes suchen soll, die durch den LUN-Vorgang zum erneuten Synchronisieren überschrieben werden.<br/>
<blockquote>
[!Note]<br />
Das Flag " <strong>-novolcheck</strong> " wird nur unter Windows Server-Betriebssystemen unterstützt.
</blockquote>
<br/> <strong>Windows Server 2008 und Windows Server 2003:</strong> Nicht unterstützt.<br/></td>
</tr>
</tbody>
</table>



 

 

 
