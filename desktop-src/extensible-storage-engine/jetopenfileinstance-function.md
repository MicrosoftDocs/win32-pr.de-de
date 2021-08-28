---
description: Weitere Informationen finden Sie unter JetOpenFileInstance-Funktion.
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
ms.openlocfilehash: ba66545c65abcaa3d3969ec7c3d61d73c57be732
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983373"
---
# <a name="jetopenfileinstance-function"></a>JetOpenFileInstance-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetopenfileinstance-function"></a>JetOpenFileInstance-Funktion

Die **JetOpenFileInstance-Funktion** öffnet eine angefügte Datenbank, eine Datenbankpatchdatei oder eine Transaktionsprotokolldatei einer aktiven Instanz, um eine Streaming-Fuzzysicherung durchführen zu können. Die Daten aus diesen Dateien können anschließend mit [jetReadFileInstance](./jetreadfileinstance-function.md)über das zurückgegebene Handle gelesen werden. Das zurückgegebene Handle muss mit [JetCloseFileInstance geschlossen werden.](./jetclosefileinstance-function.md) Eine externe Sicherung der Instanz muss zuvor mit [JetBeginExternalBackupInstance initiiert worden sein.](./jetbeginexternalbackupinstance-function.md)

**Windows XP:****JetOpenFileInstance** wird in Windows XP eingeführt.  

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

Für Windows 2000 ist die API-Variante, die diesen Parameter akzeptiert, nicht verfügbar, da nur eine Instanz unterstützt wird. Die Verwendung dieser einen globalen Instanz wird in diesem Fall impliziert.

Für Windows XP und spätere Versionen kann die API-Variante, die diesen Parameter nicht akzeptiert, nur aufgerufen werden, wenn sich die Engine im Legacymodus (Windows 2000-Kompatibilitätsmodus) befindet, in dem nur eine Instanz unterstützt wird. Andernfalls wird der Vorgang mit einem JET_errRunningInMultiInstanceMode.

*szFileName*

Der relative oder absolute Pfad zu einer angefügten Datenbank, Datenbankpatchdatei oder Transaktionsprotokolldatei, die von der Instanz verwaltet wird, die für die Sicherung gelesen wird.

*phfFile*

Zeiger auf den Ausgabepuffer, der ein Handle für die zu lesende Datei empfängt.

*pulFileSizeLow*

Zeiger auf den Ausgabepuffer, der die am wenigsten signifikanten 32 Bits der Dateigröße empfängt.

*pulFileSizeHigh*

Zeiger auf den Ausgabepuffer, der die signifikantesten 32 Bits der Dateigröße empfängt.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errBackupAbortByServer</p> | <p>Fehler beim Vorgang, weil die aktuelle externe Sicherung durch einen Aufruf von <a href="gg269309(v=exchg.10).md">JetStopBackupInstance abgebrochen wurde.</a> Dieser Fehler wird nur von xp Windows und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Es ist nicht möglich, den Vorgang abschließen, da alle Aktivitäten auf der -Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufs von <a href="gg294108(v=exchg.10).md">JetStopServiceInstance beendet wurden.</a></p> | 
| <p>JET_errFileAccessDenied</p> | <p>Der Vorgang ist fehlgeschlagen, da die angeforderte Datei aufgrund einer Freigabeverletzung oder unzureichender Berechtigungen nicht geöffnet werden konnte.</p> | 
| <p>JET_errFileNotFound</p> | <p>Fehler beim Vorgang, da die angeforderte Datei nicht geöffnet werden konnte, weil sie unter dem angegebenen Pfad nicht gefunden wurde. Dieser Fehler wird nur von Windows 2000 zurückgegeben.</p> | 
| <p>JET_errInvalidBackupSequence</p> | <p>Fehler beim Sicherungsvorgang, weil er nicht sequenziert aufgerufen wurde.</p> | 
| <p>JET_errInvalidPath</p> | <p>Fehler beim Vorgang, weil der angegebene Pfad nicht gefunden werden konnte.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da für die der Sitzung zugeordnete Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen. Dieser Fehler wird nur von xp Windows und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Einer der bereitgestellten Parameter enthielt einen unerwarteten Wert oder einen Wert, der in Kombination mit dem Wert eines anderen Parameters nicht sinnvoll war. Dies kann für <strong>JetOpenFileInstance passieren, wenn:</strong></p><ul><li><p>Das angegebene Instanzhand handle ist ungültig (Windows XP und spätere Versionen).</p></li><li><p>Der angegebene Dateinamenparameter ist NULL oder eine Zeichenfolge der Länge 0 (Windows XP und spätere Releases).</p></li></ul> | 
| <p>JET_errMissingFileToBackup</p> | <p>Die angeforderte Datei konnte nicht für die Sicherung geöffnet werden, da sie nicht gefunden wurde. Dieser Fehler wird nur von xp Windows und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errNoBackup</p> | <p>Der Vorgang ist fehlgeschlagen, da keine externe Sicherung durchgeführt wird.</p> | 
| <p>JET_errNotInitialized</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz noch nicht initialisiert wurde.</p> | 
| <p>JET_errOutOfMemory</p> | <p>Fehler beim Vorgang, da nicht genügend Arbeitsspeicher zugeordnet werden konnte, um ihn abschließen zu können. <strong>JetOpenFileInstance</strong> gibt JET_errOutOfMemory zurück, wenn versucht wird, eine andere Datei zu öffnen, bevor die vorherige Datei, die mit <strong>JetOpenFileInstance</strong> geöffnet wurde, von <a href="gg269270(v=exchg.10).md">JetCloseFileInstance geschlossen wurde.</a> Derzeit wird nur ein ausstehendes Dateihand handle unterstützt.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da ein Wiederherstellungsvorgang für die -Instanz durchgeführt wird, die der Sitzung zugeordnet ist.</p> | 
| <p>JET_errRunningInMultiInstanceMode</p> | <p>Der Vorgang ist fehlgeschlagen, weil versucht wurde, die Engine im Legacymodus (Windows 2000-Kompatibilitätsmodus) zu verwenden, bei dem nur eine Instanz unterstützt wird, wenn tatsächlich bereits mehrere Instanzen vorhanden sind.</p> | 
| <p>JET_errTermInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz heruntergefahren wird.</p> | 



Bei Erfolg wird ein Handle für die angeforderte Datei zurückgegeben. Wenn das Handle für eine Datenbankdatei gilt, wird diese Datenbankdatei für eine Streamingsicherung vorbereitet, was zur Erstellung einer Datenbankpatchdatei am gleichen Speicherort wie die Datenbankdatei führen kann. Die Datenbankpatchdatei hat genau denselben Pfad und Dateinamen wie die Datenbankdatei, jedoch mit einem . PAT-Erweiterung. Die Größe der Datei wird ebenfalls zurückgegeben.

Bei einem Fehler ist der Status der Ausgabepuffer nicht definiert. Eine Datenbankpatchdatei kann vorübergehend auf dem Datenträger erstellt werden, und alle vorhandenen Dateien am Speicherort der Patchdatei können gelöscht werden. Der Fehler führt zum Abbruch des gesamten Sicherungsprozesses für die Instanz. Bei Windows XP und späteren Versionen wird die Sicherung nicht abgebrochen, wenn versucht wurde, eine Datenbank zu sichern, die zum Zeitpunkt des Aufrufs nicht an die Instanz angefügt war.

**Warnung**  Aus Sicherheitsgründen ist es wichtig zu beachten, dass **JetOpenFileInstance** nicht überprüft, ob der angeforderte Dateipfad dem Satz von Dateien zugeordnet ist, die für die Instanz sichern werden. Daher ist es möglich, diese Funktion für den Zugriff auf jede Datei zu verwenden, die vom aktuellen Sicherheitskontext des Threads geöffnet werden kann. Es ist zwingend erforderlich, dass die Anwendung die pfade, die an diese Funktion übergeben werden, auf einen bekannten Satz guter Dateipfade beschränkt, oder es kann ein Angriff auf die Offenlegung von Informationen möglich gemacht werden.

#### <a name="remarks"></a>Bemerkungen

Die Ausgabepuffer für Handle und Dateigröße müssen vorhanden sein. Wenn sie nicht vorhanden sind, stürzt die Engine ab, da die Ausgabepufferparameter nicht überprüft werden.

Derzeit kann nur eine Datei gleichzeitig für die Sicherung geöffnet werden.

**JetOpenFileInstance übernimmt** die Sicherungsberechtigung nicht, bevor die angeforderte Datei geöffnet wird.

Die Größe der Datei, die gelesen werden soll, wie von dieser Funktion gemeldet, ist möglicherweise nicht mit der Größe der Datei auf dem Datenträger übereinstimmen. In Windows XP und späteren Versionen können zusätzliche Informationen an eine Datenbankdatei angefügt werden, die von der Datenbank-Engine während eines Wiederherstellungsvorgang verwendet wird. Daher sollte sich die Anwendung nur auf die dateigröße verlassen, die von **JetOpenFileInstance** zurückgegeben wird, oder auf der tatsächlichen Anzahl von Bytes von Daten, die von [JetReadFileInstance zurückgegeben werden.](./jetreadfileinstance-function.md)

#### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista oder Windows XP.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008 oder Windows Server 2003.</p> | 
| <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | 
| <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implementiert als <strong>JetOpenFileInstanceW</strong> (Unicode) und <strong>JetOpenFileInstanceA</strong> (ANSI).</p> | 



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
