---
description: 'Weitere Informationen zu: JetOpenFile-Funktion'
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
ms.openlocfilehash: ffe4527390e21e86ed46820125eb2a422367d8ec
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480376"
---
# <a name="jetopenfile-function"></a>JetOpenFile-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetopenfile-function"></a>JetOpenFile-Funktion

Die **JetOpenFile-Funktion** öffnet eine angefügte Datenbank, eine Datenbankpatchdatei oder eine Transaktionsprotokolldatei einer aktiven Instanz, um eine Streaming-Fuzzysicherung durchzuführen. Die Daten aus diesen Dateien können anschließend mithilfe von [JetReadFile](./jetreadfile-function.md)über das zurückgegebene Handle gelesen werden. Das zurückgegebene Handle muss mit [jetCloseFile](./jetclosefile-function.md)geschlossen werden. Eine externe Sicherung der -Instanz muss zuvor mit [JetBeginExternalBackup](./jetbeginexternalbackup-function.md)initiiert worden sein.

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

Der relative oder absolute Pfad zu einer angefügten Datenbank, Datenbankpatchdatei oder Transaktionsprotokolldatei, die von der -Instanz verwaltet wird, die für die Sicherung gelesen wird.

*phfFile*

Der Ausgabepuffer, der ein Handle für die zu lesende Datei empfängt.

*pulFileSizeLow*

Der Ausgabepuffer, der die am wenigsten signifikanten 32 Bits der Dateigröße empfängt.

*pulFileSizeHigh*

Der Ausgabepuffer, der die wichtigsten 32 Bits der Dateigröße empfängt.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errBackupAbortByServer</p> | <p>Fehler beim Vorgang, weil die aktuelle externe Sicherung durch einen Aufruf von <a href="gg294067(v=exchg.10).md">JetStopBackup</a>abgebrochen wurde. Dieser Fehler wird nur von Windows XP und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, als Ergebnis eines Aufrufs von <a href="gg269240(v=exchg.10).md">JetStopService</a>aufgetreten sind.</p> | 
| <p>JET_errFileAccessDenied</p> | <p>Fehler beim Vorgang, weil die angeforderte Datei aufgrund einer Freigabeverletzung oder unzureichender Berechtigungen nicht geöffnet werden konnte.</p> | 
| <p>JET_errFileNotFound</p> | <p>Fehler beim Vorgang, weil die angeforderte Datei nicht geöffnet werden konnte, weil sie nicht unter dem angegebenen Pfad gefunden werden konnte. Dieser Fehler wird nur von Windows 2000 zurückgegeben.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da für die instanz, die der Sitzung zugeordnet ist, ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen. Dieser Fehler wird nur von Windows XP und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errInvalidBackupSequence</p> | <p>Der Sicherungsvorgang ist fehlgeschlagen, weil er außerhalb der Sequenz aufgerufen wurde.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Einer der bereitgestellten Parameter enthielt einen unerwarteten Wert oder einen Wert, der in Kombination mit dem Wert eines anderen Parameters nicht sinnvoll war. Dies kann für <strong>JetOpenFile</strong> passieren, wenn:</p><ul><li><p>Das angegebene Instanzhandle ist ungültig (Windows XP und höhere Versionen).</p></li><li><p>Der angegebene Filename-Parameter ist NULL oder eine Zeichenfolge der Länge 0 (Windows XP und spätere Releases).</p></li></ul> | 
| <p>JET_errInvalidPath</p> | <p>Fehler beim Vorgang, weil der angegebene Pfad nicht gefunden werden konnte.</p> | 
| <p>JET_errMissingFileToBackup</p> | <p>Die angeforderte Datei konnte nicht für die Sicherung geöffnet werden, da sie nicht gefunden wurde. Dieser Fehler wird nur von Windows XP und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errNoBackup</p> | <p>Fehler beim Vorgang, weil keine externe Sicherung ausgeführt wird.</p> | 
| <p>JET_errNotInitialized</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da die der Sitzung zugeordnete Instanz noch nicht initialisiert wurde.</p> | 
| <p>JET_errOutOfMemory</p> | <p>Fehler beim Vorgang, weil nicht genügend Arbeitsspeicher zugeordnet werden konnte, um den Vorgang abzuschließen. <strong>JetOpenFile</strong> gibt JET_errOutOfMemory zurück, wenn versucht wird, eine andere Datei zu öffnen, bevor die zuvor mit <strong>JetOpenFile</strong> geöffnete Datei von <a href="gg294127(v=exchg.10).md">JetCloseFile</a>geschlossen wurde. Derzeit wird nur ein ausstehendes Dateihandle unterstützt.</p> | 
| <p>JET_errRunningInMultiInstanceMode</p> | <p>Fehler beim Vorgang, weil versucht wurde, die Engine im Legacymodus (Windows 2000-Kompatibilitätsmodus) zu verwenden, wobei nur eine Instanz unterstützt wird, wenn tatsächlich mehrere Instanzen bereits vorhanden sind.</p> | 
| <p>JET_errTermInProgress</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da die der Sitzung zugeordnete Instanz heruntergefahren wird. JET_errRestoreInProgress Es ist nicht möglich, den Vorgang abzuschließen, da ein Wiederherstellungsvorgang für die Instanz ausgeführt wird, die der Sitzung zugeordnet ist.</p> | 



Bei Erfolg wird ein Handle für die angeforderte Datei zurückgegeben. Wenn das Handle für eine Datenbankdatei gilt, wird diese Datenbankdatei für die Streamingsicherung vorbereitet, was zur Erstellung einer Datenbankpatchdatei am gleichen Speicherort wie die Datenbankdatei führen kann. Die Datenbankpatchdatei weist genau denselben Pfad und Dateinamen wie die Datenbankdatei auf, verfügt jedoch über einen . PAT-Erweiterung. Die Größe der Datei wird ebenfalls zurückgegeben.

Bei einem Fehler ist der Status der Ausgabepuffer nicht definiert. Eine Datenbankpatchdatei kann vorübergehend auf dem Datenträger erstellt werden, und alle vorhandenen Dateien am Speicherort der Patchdatei können gelöscht werden. Der Fehler führt zum Abbruch des gesamten Sicherungsprozesses für die Instanz. Bei Windows XP und späteren Releases wird die Sicherung nicht abgebrochen, wenn versucht wurde, eine Datenbank zu sichern, die zum Zeitpunkt des Aufrufs nicht an die Instanz angefügt war.

**Warnung**  Aus Sicherheitsgründen ist es wichtig zu beachten, dass **JetOpenFile** nicht überprüft, ob der angeforderte Dateipfad dem Satz von Dateien zugeordnet ist, die für die Instanz gesichert werden sollen. Daher ist es möglich, diese Funktion zu verwenden, um auf jede Datei zuzugreifen, die vom aktuellen Sicherheitskontext des Threads geöffnet werden kann. Es ist zwingend erforderlich, dass die Anwendung die an diese Funktion übergebenen Pfade auf einen bekannten Satz guter Dateipfade einschränkt, oder dass ein Angriff auf die Offenlegung von Informationen möglich ist.

#### <a name="remarks"></a>Hinweise

Die Ausgabepuffer für Handle und Dateigröße müssen vorhanden sein. Wenn sie nicht vorhanden sind, stürzt die Engine ab, da die Ausgabepufferparameter nicht überprüft werden.

Derzeit kann nur eine Datei gleichzeitig für die Sicherung geöffnet werden.

**JetOpenFile** bestätigt die Sicherungsberechtigung vor dem Öffnen der angeforderten Datei nicht.

Die Größe der Datei, die wie von dieser Funktion gemeldet gelesen werden soll, stimmt möglicherweise nicht mit der Größe der Datei auf dem Datenträger überein. Bei Windows XP und späteren Releases können zusätzliche Informationen an eine Datenbankdatei angefügt werden, die von der Datenbank-Engine während eines Wiederherstellungsvorgangs verwendet wird. Daher sollte sich die Anwendung nur auf die von **JetOpenFile** zurückgegebene Dateigröße oder auf die tatsächliche Anzahl der von [JetReadFile](./jetreadfile-function.md)zurückgegebenen Datenbytes verlassen.

#### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Implementiert als <strong>JetOpenFileW</strong> (Unicode) und <strong>JetOpenFileA</strong> (ANSI).</p> | 



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
