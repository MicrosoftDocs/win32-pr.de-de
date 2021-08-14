---
description: 'Weitere Informationen zu: JetOpenFileInstance-Funktion'
title: JetOpenFileInstance-Funktion
TOCTitle: JetOpenFileInstance Function
ms:assetid: 44af9549-77ef-48f4-8580-507f7199f281
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269238(v=EXCHG.10)
ms:contentKeyID: 32765540
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenFileInstanceA
- JetOpenFileInstanceW
- JetOpenFileInstance
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 86d7aa4a1e927c94996f6c6b2a2a0b6e3ab5cecf08f17569bfd8a4e2144032bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117704108"
---
# <a name="jetopenfileinstance-function"></a>JetOpenFileInstance-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetopenfileinstance-function"></a>JetOpenFileInstance-Funktion

Die **JetOpenFileInstance-Funktion** öffnet eine angefügte Datenbank, eine Datenbankpatchdatei oder eine Transaktionsprotokolldatei einer aktiven Instanz, um eine Streaming-Fuzzysicherung durchzuführen. Die Daten aus diesen Dateien können anschließend mithilfe von [JetReadFileInstance](./jetreadfileinstance-function.md)über das zurückgegebene Handle gelesen werden. Das zurückgegebene Handle muss mit [jetCloseFileInstance](./jetclosefileinstance-function.md)geschlossen werden. Eine externe Sicherung der -Instanz muss zuvor mit [JetBeginExternalBackupInstance](./jetbeginexternalbackupinstance-function.md)initiiert worden sein.

**Windows XP:****JetOpenFileInstance** wurde in Windows XP eingeführt.  

```cpp
    JET_ERR JET_API JetOpenFileInstance(
      __in          JET_INSTANCE instance,
      __in          JET_PCSTR szFileName,
      __out         JET_HANDLE* phfFile,
      __out         unsigned long* pulFileSizeLow,
      __out         unsigned long* pulFileSizeHigh
    );
```

### <a name="parameters"></a>Parameter

*Instanz*

Die -Instanz, die für diesen Aufruf verwendet werden soll.

Für Windows 2000 ist die API-Variante, die diesen Parameter akzeptiert, nicht verfügbar, da nur eine Instanz unterstützt wird. Die Verwendung dieser globalen Instanz wird in diesem Fall impliziert.

Für Windows XP und höhere Versionen kann die API-Variante, die diesen Parameter nicht akzeptiert, nur aufgerufen werden, wenn sich die Engine im Legacymodus befindet (Windows Kompatibilitätsmodus 2000), in dem nur eine Instanz unterstützt wird. Andernfalls schlägt der Vorgang mit JET_errRunningInMultiInstanceMode fehl.

*szFileName*

Der relative oder absolute Pfad zu einer angefügten Datenbank, Datenbankpatchdatei oder Transaktionsprotokolldatei, die von der -Instanz verwaltet wird, die für die Sicherung gelesen wird.

*phfFile*

Zeiger auf den Ausgabepuffer, der ein Handle für die zu lesende Datei empfängt.

*pulFileSizeLow*

Zeiger auf den Ausgabepuffer, der die am wenigsten signifikanten 32 Bits der Dateigröße empfängt.

*pulFileSizeHigh*

Zeiger auf den Ausgabepuffer, der die wichtigsten 32 Bits der Dateigröße empfängt.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).

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
<td><p>Fehler beim Vorgang, weil die aktuelle externe Sicherung durch einen Aufruf von <a href="gg269309(v=exchg.10).md">JetStopBackupInstance</a>abgebrochen wurde. Dieser Fehler wird nur von Windows XP und späteren Versionen zurückgegeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Es ist nicht möglich, den Vorgang abzuschließen, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, als Ergebnis eines Aufrufs von <a href="gg294108(v=exchg.10).md">JetStopServiceInstance</a>aufgetreten sind.</p></td>
</tr>
<tr class="even">
<td><p>JET_errFileAccessDenied</p></td>
<td><p>Fehler beim Vorgang, weil die angeforderte Datei aufgrund einer Freigabeverletzung oder unzureichender Berechtigungen nicht geöffnet werden konnte.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFileNotFound</p></td>
<td><p>Fehler beim Vorgang, weil die angeforderte Datei nicht geöffnet werden konnte, weil sie nicht unter dem angegebenen Pfad gefunden werden konnte. Dieser Fehler wird nur von Windows 2000 zurückgegeben.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidBackupSequence</p></td>
<td><p>Der Sicherungsvorgang ist fehlgeschlagen, da er außerhalb der Sequenz aufgerufen wurde.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidPath</p></td>
<td><p>Fehler beim Vorgang, weil der angegebene Pfad nicht gefunden werden konnte.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Es ist nicht möglich, den Vorgang abzuschließen, da für die instanz, die der Sitzung zugeordnet ist, ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen. Dieser Fehler wird nur von Windows XP und späteren Versionen zurückgegeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Einer der bereitgestellten Parameter enthielt einen unerwarteten Wert oder einen Wert, der in Kombination mit dem Wert eines anderen Parameters nicht sinnvoll war. Dies kann für <strong>JetOpenFileInstance</strong> passieren, wenn:</p>
<ul>
<li><p>Das angegebene Instanzhandle ist ungültig (Windows XP und höhere Versionen).</p></li>
<li><p>Der angegebene Filename-Parameter ist NULL oder eine Zeichenfolge der Länge 0 (Windows XP und höhere Versionen).</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errMissingFileToBackup</p></td>
<td><p>Die angeforderte Datei konnte nicht für die Sicherung geöffnet werden, da sie nicht gefunden wurde. Dieser Fehler wird nur von Windows XP und späteren Versionen zurückgegeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoBackup</p></td>
<td><p>Fehler beim Vorgang, weil keine externe Sicherung ausgeführt wird.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>Es ist nicht möglich, den Vorgang abzuschließen, da die der Sitzung zugeordnete Instanz noch nicht initialisiert wurde.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfMemory</p></td>
<td><p>Fehler beim Vorgang, weil nicht genügend Arbeitsspeicher zugeordnet werden konnte, um ihn abzuschließen. <strong>JetOpenFileInstance</strong> gibt JET_errOutOfMemory zurück, wenn versucht wird, eine andere Datei zu öffnen, bevor die zuvor mit <strong>JetOpenFileInstance</strong> geöffnete Datei von <a href="gg269270(v=exchg.10).md">JetCloseFileInstance</a>geschlossen wurde. Derzeit wird nur ein ausstehendes Dateihandle unterstützt.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Es ist nicht möglich, den Vorgang abzuschließen, da ein Wiederherstellungsvorgang für die Instanz ausgeführt wird, die der Sitzung zugeordnet ist.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRunningInMultiInstanceMode</p></td>
<td><p>Der Vorgang ist fehlgeschlagen, weil versucht wurde, die Engine im Legacymodus (Windows 2000-Kompatibilitätsmodus) zu verwenden, wobei nur eine Instanz unterstützt wird, wenn tatsächlich bereits mehrere Instanzen vorhanden sind.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Es ist nicht möglich, den Vorgang abzuschließen, da die der Sitzung zugeordnete Instanz heruntergefahren wird.</p></td>
</tr>
</tbody>
</table>


Bei Erfolg wird ein Handle für die angeforderte Datei zurückgegeben. Wenn das Handle für eine Datenbankdatei verwendet wird, wird diese Datenbankdatei für eine Streamingsicherung vorbereitet. Dies kann zur Erstellung einer Datenbankpatchdatei am gleichen Speicherort wie die Datenbankdatei führen. Die Datenbankpatchdatei hat genau denselben Pfad und Dateinamen wie die Datenbankdatei, jedoch mit einem . PAT-Erweiterung. Die Größe der Datei wird ebenfalls zurückgegeben.

Bei einem Fehler ist der Status der Ausgabepuffer nicht definiert. Eine Datenbankpatchdatei kann vorübergehend auf dem Datenträger erstellt werden, und alle vorhandenen Dateien am Speicherort der Patchdatei können gelöscht werden. Der Fehler führt zum Abbruch des gesamten Sicherungsprozesses für die Instanz. Bei Windows XP und späteren Releases wird die Sicherung nicht abgebrochen, wenn versucht wurde, eine Datenbank zu sichern, die zum Zeitpunkt des Aufrufs nicht an die Instanz angefügt war.

**Warnung**  Aus Sicherheitsgründen ist es wichtig zu beachten, dass **JetOpenFileInstance** nicht überprüft, ob der angeforderte Dateipfad dem Satz von Dateien zugeordnet ist, die für die Instanz gesichert werden. Daher ist es möglich, diese Funktion zu verwenden, um auf jede Datei zuzugreifen, die vom aktuellen Sicherheitskontext des Threads geöffnet werden kann. Es ist zwingend erforderlich, dass die Anwendung die an diese Funktion übergebenen Pfade auf einen bekannten Satz guter Dateipfade einschränkt, oder dass ein Angriff auf die Offenlegung von Informationen möglich ist.

#### <a name="remarks"></a>Hinweise

Die Ausgabepuffer für Handle und Dateigröße müssen vorhanden sein. Wenn sie nicht vorhanden sind, stürzt die Engine ab, da die Ausgabepufferparameter nicht überprüft werden.

Derzeit kann nur eine Datei gleichzeitig für die Sicherung geöffnet werden.

**JetOpenFileInstance** bestätigt die Sicherungsberechtigung vor dem Öffnen der angeforderten Datei nicht.

Die Größe der Datei, die wie von dieser Funktion gemeldet gelesen werden soll, stimmt möglicherweise nicht mit der Größe der Datei auf dem Datenträger überein. Bei Windows XP und späteren Releases können zusätzliche Informationen an eine Datenbankdatei angefügt werden, die von der Datenbank-Engine während eines Wiederherstellungsvorgangs verwendet wird. Daher sollte sich die Anwendung nur auf die von **JetOpenFileInstance** zurückgegebene Dateigröße oder auf die tatsächliche Anzahl von Datenbytes verlassen, die von [JetReadFileInstance](./jetreadfileinstance-function.md)zurückgegeben werden.

#### <a name="requirements"></a>Anforderungen

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Erfordert Windows Vista oder Windows XP.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Erfordert Windows Server 2008 oder Windows Server 2003.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Deklariert in Esent.h.</p></td>
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
<td><p>Implementiert als <strong>JetOpenFileInstanceW</strong> (Unicode) und <strong>JetOpenFileInstanceA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_HANDLE](./jet-handle.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetBeginExternalBackupInstance](./jetbeginexternalbackupinstance-function.md)  
[JetCloseFileInstance](./jetclosefileinstance-function.md)  
[JetGetAttachInfoInstance](./jetgetattachinfoinstance-function.md)  
[JetGetLogInfoInstance](./jetgetloginfoinstance-function.md)  
[JetReadFileInstance](./jetreadfileinstance-function.md)  
[JetStopBackupInstance](./jetstopbackupinstance-function.md)  
[JetTruncateLogInstance](./jettruncateloginstance-function.md)
