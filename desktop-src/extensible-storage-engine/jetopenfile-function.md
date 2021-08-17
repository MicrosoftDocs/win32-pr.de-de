---
description: Weitere Informationen finden Sie unter JetOpenFile-Funktion.
title: JetOpenFile-Funktion
TOCTitle: JetOpenFile Function
ms:assetid: 52f69050-ca1c-4a6b-a188-22bd7cb96bf5
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269249(v=EXCHG.10)
ms:contentKeyID: 32765551
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenFileW
- JetOpenFile
- JetOpenFileA
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b83f48f024ba79eaa55ad4ae333e8f093cd307e5508e0bb8338ce9bbc4a1bef7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119615060"
---
# <a name="jetopenfile-function"></a>JetOpenFile-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetopenfile-function"></a>JetOpenFile-Funktion

Die **JetOpenFile-Funktion** öffnet eine angefügte Datenbank, eine Datenbankpatchdatei oder eine Transaktionsprotokolldatei einer aktiven Instanz, um eine Streaming-Fuzzysicherung durchführen zu können. Die Daten aus diesen Dateien können anschließend mithilfe von [JetReadFile](./jetreadfile-function.md)über das zurückgegebene Handle gelesen werden. Das zurückgegebene Handle muss mit [JetCloseFile geschlossen werden.](./jetclosefile-function.md) Eine externe Sicherung der Instanz muss zuvor mit [JetBeginExternalBackup initiiert worden sein.](./jetbeginexternalbackup-function.md)

```cpp
    JET_ERR JET_API JetOpenFile(
      __in          const tchar* szFileName,
      __out         JET_HANDLE* phfFile,
      __out         unsigned long* pulFileSizeLow,
      __out         unsigned long* pulFileSizeHigh
    );
```

### <a name="parameters"></a>Parameter

*szFileName*

Der relative oder absolute Pfad zu einer angefügten Datenbank, Datenbankpatchdatei oder Transaktionsprotokolldatei, die von der Instanz verwaltet wird, die für die Sicherung gelesen wird.

*phfFile*

Der Ausgabepuffer, der ein Handle für die zu lesende Datei empfängt.

*pulFileSizeLow*

Der Ausgabepuffer, der die am wenigsten signifikanten 32 Bits der Größe der Datei empfängt.

*pulFileSizeHigh*

Der Ausgabepuffer, der die signifikantesten 32 Bits der Größe der Datei empfängt.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR-Datentyp](./jet-err.md) mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Rückgabecode</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>Der Vorgang wurde erfolgreich abgeschlossen.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBackupAbortByServer</p></td>
<td><p>Fehler beim Vorgang, weil die aktuelle externe Sicherung durch einen Aufruf von <a href="gg294067(v=exchg.10).md">JetStopBackup abgebrochen wurde.</a> Dieser Fehler wird nur von xp Windows und späteren Versionen zurückgegeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Es ist nicht möglich, den Vorgang abschließen, da alle Aktivitäten auf der -Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufs von <a href="gg269240(v=exchg.10).md">JetStopService beendet wurden.</a></p></td>
</tr>
<tr class="even">
<td><p>JET_errFileAccessDenied</p></td>
<td><p>Der Vorgang ist fehlgeschlagen, da die angeforderte Datei aufgrund einer Freigabeverletzung oder unzureichender Berechtigungen nicht geöffnet werden konnte.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFileNotFound</p></td>
<td><p>Fehler beim Vorgang, da die angeforderte Datei nicht geöffnet werden konnte, weil sie unter dem angegebenen Pfad nicht gefunden wurde. Dieser Fehler wird nur von Windows 2000 zurückgegeben.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da für die der Sitzung zugeordnete Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen. Dieser Fehler wird nur von xp Windows und späteren Versionen zurückgegeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidBackupSequence</p></td>
<td><p>Fehler beim Sicherungsvorgang, weil er nicht sequenziert aufgerufen wurde.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Einer der bereitgestellten Parameter enthielt einen unerwarteten Wert oder einen Wert, der in Kombination mit dem Wert eines anderen Parameters nicht sinnvoll war. Dies kann für <strong>JetOpenFile passieren,</strong> wenn:</p>
<ul>
<li><p>Das angegebene Instanzhand handle ist ungültig (Windows XP und spätere Versionen).</p></li>
<li><p>Der angegebene Dateinamenparameter ist NULL oder eine Zeichenfolge der Länge 0 (Windows XP und spätere Releases).</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidPath</p></td>
<td><p>Fehler beim Vorgang, weil der angegebene Pfad nicht gefunden werden konnte.</p></td>
</tr>
<tr class="even">
<td><p>JET_errMissingFileToBackup</p></td>
<td><p>Die angeforderte Datei konnte nicht für die Sicherung geöffnet werden, da sie nicht gefunden wurde. Dieser Fehler wird nur von xp Windows und späteren Versionen zurückgegeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoBackup</p></td>
<td><p>Der Vorgang ist fehlgeschlagen, da keine externe Sicherung durchgeführt wird.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz noch nicht initialisiert wurde.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfMemory</p></td>
<td><p>Fehler beim Vorgang, da nicht genügend Arbeitsspeicher zugeordnet werden konnte, um ihn abschließen zu können. <strong>JetOpenFile</strong> gibt JET_errOutOfMemory zurück, wenn versucht wird, eine andere Datei zu öffnen, bevor die vorherige Datei, die mit <strong>JetOpenFile</strong> geöffnet wurde, von <a href="gg294127(v=exchg.10).md">JetCloseFile geschlossen wurde.</a> Derzeit wird nur ein ausstehendes Dateihand handle unterstützt.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRunningInMultiInstanceMode</p></td>
<td><p>Der Vorgang ist fehlgeschlagen, weil versucht wurde, die Engine im Legacymodus (Windows 2000-Kompatibilitätsmodus) zu verwenden, bei dem nur eine Instanz unterstützt wird, wenn tatsächlich bereits mehrere Instanzen vorhanden sind.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz heruntergefahren wird. JET_errRestoreInProgress Der Vorgang kann nicht abgeschlossen werden, da ein Wiederherstellungsvorgang für die -Instanz durchgeführt wird, die der Sitzung zugeordnet ist.</p></td>
</tr>
</tbody>
</table>


Bei Erfolg wird ein Handle für die angeforderte Datei zurückgegeben. Wenn das Handle für eine Datenbankdatei gilt, wird diese Datenbankdatei für die Streamingsicherung vorbereitet, was zur Erstellung einer Datenbankpatchdatei am gleichen Speicherort wie die Datenbankdatei führen kann. Die Datenbankpatchdatei hat genau denselben Pfad und Dateinamen wie die Datenbankdatei, verfügt jedoch über einen . PAT-Erweiterung. Die Größe der Datei wird ebenfalls zurückgegeben.

Bei einem Fehler ist der Status der Ausgabepuffer nicht definiert. Eine Datenbankpatchdatei kann vorübergehend auf dem Datenträger erstellt werden, und alle vorhandenen Dateien am Speicherort der Patchdatei können gelöscht werden. Der Fehler führt zum Abbruch des gesamten Sicherungsprozesses für die Instanz. Bei Windows XP und späteren Versionen wird die Sicherung nicht abgebrochen, wenn versucht wurde, eine Datenbank zu sichern, die zum Zeitpunkt des Aufrufs nicht an die Instanz angefügt war.

**Warnung**  Aus Sicherheitsgründen ist es wichtig zu beachten, dass **JetOpenFile** nicht überprüft, ob der angeforderte Dateipfad dem Satz von Dateien zugeordnet ist, die für die Instanz sichern werden sollen. Daher ist es möglich, diese Funktion für den Zugriff auf jede Datei zu verwenden, die vom aktuellen Sicherheitskontext des Threads geöffnet werden kann. Es ist zwingend erforderlich, dass die Anwendung die pfade, die an diese Funktion übergeben werden, auf einen bekannten Satz guter Dateipfade beschränkt, oder es kann ein Angriff auf die Offenlegung von Informationen möglich gemacht werden.

#### <a name="remarks"></a>Hinweise

Die Ausgabepuffer für Handle und Dateigröße müssen vorhanden sein. Wenn sie nicht vorhanden sind, stürzt die Engine ab, da die Ausgabepufferparameter nicht überprüft werden.

Derzeit kann nur eine Datei gleichzeitig für die Sicherung geöffnet werden.

**JetOpenFile** übernimmt die Sicherungsberechtigung nicht, bevor die angeforderte Datei geöffnet wird.

Die Größe der Datei, die gelesen werden soll, wie von dieser Funktion gemeldet, ist möglicherweise nicht mit der Größe der Datei auf dem Datenträger übereinstimmen. In Windows XP und späteren Versionen können zusätzliche Informationen an eine Datenbankdatei angefügt werden, die von der Datenbank-Engine während eines Wiederherstellungsvorgang verwendet wird. Daher sollte sich die Anwendung nur auf die von **JetOpenFile** zurückgegebene Dateigröße oder auf die tatsächliche Anzahl von Datenbytes verlassen, die von [JetReadFile zurückgegeben werden.](./jetreadfile-function.md)

#### <a name="requirements"></a>Anforderungen

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Wird in Esent.h deklariert.</p></td>
</tr>
<tr class="even">
<td><p><strong>Bibliothek</strong></p></td>
<td><p>Verwenden Sie ESENT.lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Dll</strong></p></td>
<td><p>Erfordert ESENT.dll.</p></td>
</tr>
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Wird als <strong>JetOpenFileW</strong> (Unicode) und <strong>JetOpenFileA</strong> (ANSI) implementiert.</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_HANDLE](./jet-handle.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetBeginExternalBackup](./jetbeginexternalbackup-function.md)  
[JetCloseFile](./jetclosefile-function.md)  
[JetGetAttachInfo](./jetgetattachinfo-function.md)  
[JetGetLogInfo](./jetgetloginfo-function.md)  
[JetReadFile](./jetreadfile-function.md)  
[JetStopBackup](./jetstopbackup-function.md)  
[JetStopService](./jetstopservice-function.md)  
[JetTruncateLog](./jettruncatelog-function.md)
