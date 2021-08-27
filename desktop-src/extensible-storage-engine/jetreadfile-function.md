---
description: 'Weitere Informationen zu: JetReadFile-Funktion'
title: JetReadFile-Funktion
TOCTitle: JetReadFile Function
ms:assetid: 59dc9e04-7e02-4835-9aed-95cfcf74d780
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269257(v=EXCHG.10)
ms:contentKeyID: 32765559
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetReadFile
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b7f089e87fad910232bae85e14f1d6d2ab6e00b0
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470277"
---
# <a name="jetreadfile-function"></a>JetReadFile-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetreadfile-function"></a>JetReadFile-Funktion

Die **JetReadFile-Funktion** ruft den Inhalt einer Datei ab, die mit [JetOpenFile](./jetopenfile-function.md)geöffnet wurde.

```cpp
    JET_ERR JET_API JetReadFile(
      __in          JET_HANDLE hfFile,
      __out         void* pv,
      __in          unsigned long cb,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a>Parameter

*hfFile*

Das Handle der zu lesenden Datei.

*Pv*

Ausgabepuffer, der die Dateidaten empfängt.

*Cb*

Die maximale Größe des Ausgabepuffers in Bytes.

*actual*

Empfängt die tatsächliche Menge der abgerufenen Dateidaten.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errBackupAbortByServer</p> | <p>Fehler beim Vorgang, weil die aktuelle externe Sicherung durch einen Aufruf von <a href="gg269240(v=exchg.10).md">JetStopService</a>abgebrochen wurde. Dieser Fehler wird nur von Windows XP und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, als Ergebnis eines Aufrufs von <a href="gg269240(v=exchg.10).md">JetStopService</a>aufgetreten sind.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da für die Instanz, die der Sitzung zugeordnet ist, ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen. Dieser Fehler wird nur von Windows XP und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Einer der bereitgestellten Parameter enthielt einen unerwarteten Wert oder einen Wert, der in Kombination mit dem Wert eines anderen Parameters nicht sinnvoll war. Dies kann für <strong>JetReadFile</strong> auftreten, wenn:</p><ul><li><p>Das angegebene Instanzhandle ist ungültig. Windows XP und höhere Versionen.</p></li><li><p>Die Größe des Ausgabepuffers ist kein Vielfaches der Datenbankseitengröße (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>). Windows XP und höhere Versionen.</p></li><li><p>Die Ausgabepuffergröße ist kleiner als drei Datenbankseiten<a href="gg269337(v=exchg.10).md">(JET_paramDatabasePageSize</a>), und dies ist der erste Aufruf von <strong>JetReadFile</strong> für das angegebene Handle. Windows XP und höhere Versionen.</p></li></ul> | 
| <p>JET_errNoBackup</p> | <p>Fehler beim Vorgang, weil keine externe Sicherung ausgeführt wird.</p> | 
| <p>JET_errNotInitialized</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da die der Sitzung zugeordnete Instanz noch nicht initialisiert wurde.</p> | 
| <p>JET_errReadVerifyFailure</p> | <p>Fehler beim Vorgang, weil beim Lesen einer Datenbankseite aus einer Datenbankdatei oder Einer Datenbankpatchdatei eine nicht wiederherstellbare Datenbeschädigung erkannt wurde.</p> | 
| <p>JET_errLogReadVerifyFailure</p> | <p>Fehler beim Vorgang, weil beim Lesen einer Transaktionsprotokolldatei eine nicht wiederherstellbare Datenbeschädigung erkannt wurde. Dieser Fehler wird nur von Windows XP und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da ein Wiederherstellungsvorgang für die Instanz ausgeführt wird, die der Sitzung zugeordnet ist.</p> | 
| <p>JET_errRunningInMultiInstanceMode</p> | <p>Fehler beim Vorgang, weil versucht wurde, die Engine im Legacymodus (Windows 2000-Kompatibilitätsmodus) zu verwenden, wobei nur eine Instanz unterstützt wird, wenn tatsächlich bereits mehrere Instanzen vorhanden sind.</p> | 
| <p>JET_errTermInProgress</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da die der Sitzung zugeordnete Instanz heruntergefahren wird.</p> | 



Bei Erfolg wird der nächste Datenabschnitt aus der Datei in den Ausgabepuffer eingelesen. Die tatsächliche Anzahl der abgerufenen Bytes wird ebenfalls zurückgegeben. Der Dateioffset, bei dem der nächste Leseschritt erfolgt, wird um diesen Betrag erweitert.

Bei einem Fehler ist der Status des Ausgabepuffers nicht definiert. Der Fehler führt zum Abbruch des gesamten Sicherungsprozesses für die Instanz. Bei Windows XP und späteren Releases wird die Sicherung nicht abgebrochen, wenn beim Lesen einer Datenbankdatei ein Fehler aufgetreten ist. Die Sicherung dieser Datenbankdatei wird jedoch weiterhin abgebrochen, und das entsprechende Handle wird automatisch geschlossen.

#### <a name="remarks"></a>Hinweise

Jeder Aufruf von **JetReadFile** mit einem Handle, das bereits alle Daten in der zugrunde liegenden Datei zurückgegeben hat (z. B. ein vorheriger Aufruf, der weniger Bytes als die Größe des Ausgabepuffers zurückgegeben hat), ist immer erfolgreich, gibt jedoch 0 Bytes an Daten zurück.

Ein großer Ausgabepuffer sollte verwendet werden, um die Sicherungsleistung zu maximieren. Möglicherweise sind einige Experimente erforderlich, um den richtigen Kompromiss zwischen Ressourcenverbrauch und Durchsatz für eine bestimmte Situation zu finden. Der Ausgabepuffer sollte in jedem Fall nicht kleiner als 64 KB sein.

Mehrere gleichzeitige Aufrufe von **JetReadFile** mit demselben Dateihandle werden nicht unterstützt. Dies bedeutet, dass es nicht möglich ist, mehrere Puffer für gleichzeitiges Lesen für dieselbe Datei in die Warteschlange zu stellen, um einen hohen sequenziellen Durchsatz zu erzielen. Stattdessen sollte ein einzelner großer Puffer verwendet werden.

Wenn die Instanz so konfiguriert ist, dass die Bereinigung von Datenbankseiten aktiviert ist (siehe JET_paramZeroDatabaseDuringBackup in Systemparametern), werden gelöschte Daten als Nebeneffekt eines Aufrufs von **JetReadFile** für die Datenbankdatei aus der Datenbank entfernt.

Es ist sehr wichtig zu verstehen, wie Sicherungen und Datenbeschädigungen interagieren. Wenn die Datenbank-Engine während einer Sicherung eine Datenbeschädigung erkennt, schlägt die Sicherung der betroffenen Datenbank oder der gesamten Instanz fehl. Dies ist eine bewusste Entwurfsentscheidung zum Schutz vor Datenverlusten. Wenn die Datenbank-Engine zulässt, dass eine Sicherung erfolgreich ist, wenn eine Datenbeschädigung vorhanden war, kann eine ältere, nicht beschädigten Sicherung als Ergebnis verworfen werden. Dies wäre leider möglich, da es möglich wäre, die Datenbeschädigung auf der Liveinstanz zu beheben, indem diese Sicherung wiederhergestellt und alle Transaktionsprotokolldateien für diese Datenbank wiedergegeben werden. In diesem Szenario ohne Datenverlust wird davon ausgegangen, dass die zirkuläre Protokollierung nicht aktiviert ist (siehe [JET_paramCircularLog](./transaction-log-parameters.md) unter [Systemparameter](./extensible-storage-engine-system-parameters.md)).

Es ist auch wichtig zu verstehen, dass die Streamingsicherung, wenn datenbeschädigung vorliegt, der wahrscheinlichste Ort ist, an dem sie zuerst erkannt wird. Dies ist der Fall, da die Streamingsicherung der einzige Prozess ist, der routinemäßig jede einzelne Seite der Datenbankdatei überprüft. Es ist auch wahrscheinlich, dass die Streamingsicherung der erste Prozess ist, um die frühen Anzeichen von Hardwarefehlern zu erkennen, die sich durch zeitweilige Datenbeschädigungsfehler manifestieren. Dies ist auf die Menge der von der Sicherung abgerufenen Daten sowie auf die Geschwindigkeit zurückzuführen, mit der sie abgerufen werden.

Datenbeschädigungen werden von der Datenbank-Engine mithilfe von Blockprüfsummen erkannt. Diese Prüfsummen werden unmittelbar vor dem Schreiben einer Datenbankseite festgelegt und auf einer gelesenen Datenbankseite überprüft. Dieses Schema ermöglicht es der Datenbank-Engine, zu bestimmen, dass Daten zu einem bestimmten Zeitpunkt beschädigt wurden, aber die Datenbank-Engine kann die Quelle dieser Beschädigung nicht ermitteln. In der Vergangenheit wurde festgestellt, dass die häufigste Ursache für eine solche Beschädigung andere Quellen als die Datenbank-Engine selbst sind.

#### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_HANDLE](./jet-handle.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetOpenFile](./jetopenfile-function.md)  
[JetStopService](./jetstopservice-function.md)  
[Systemparameter](./extensible-storage-engine-system-parameters.md)
