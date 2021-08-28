---
description: Weitere Informationen finden Sie unter JetReadFile-Funktion.
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
ms.openlocfilehash: 0c670a6ed5cdcbb4b0fa4ead2415a1e55121dfce
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985853"
---
# <a name="jetreadfile-function"></a>JetReadFile-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetreadfile-function"></a>JetReadFile-Funktion

Die **JetReadFile-Funktion** ruft den Inhalt einer Datei ab, die mit [JetOpenFile geöffnet wurde.](./jetopenfile-function.md)

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

Ausgabepuffer, der die Dateidaten erhält.

*Cb*

Die maximale Größe des Ausgabepuffers in Bytes.

*–actual*

Empfängt die tatsächliche Menge der abgerufenen Dateidaten.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errBackupAbortByServer</p> | <p>Fehler beim Vorgang, weil die aktuelle externe Sicherung durch einen Aufruf von <a href="gg269240(v=exchg.10).md">JetStopService abgebrochen wurde.</a> Dieser Fehler wird nur von xp Windows und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Es ist nicht möglich, den Vorgang abschließen, da alle Aktivitäten auf der -Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufs von <a href="gg269240(v=exchg.10).md">JetStopService beendet wurden.</a></p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da für die der Sitzung zugeordnete Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen. Dieser Fehler wird nur von xp Windows und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Einer der bereitgestellten Parameter enthielt einen unerwarteten Wert oder einen Wert, der in Kombination mit dem Wert eines anderen Parameters nicht sinnvoll war. Dies kann für <strong>JetReadFile passieren,</strong> wenn:</p><ul><li><p>Das angegebene Instanzhand handle ist ungültig. Windows XP und spätere Versionen.</p></li><li><p>Die Ausgabepuffergröße ist kein Vielfaches der Datenbankseitengröße (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>). Windows XP und spätere Versionen.</p></li><li><p>Die Ausgabepuffergröße ist kleiner als drei Datenbankseiten (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>), und dies ist der erste Aufruf von <strong>JetReadFile</strong> für das angegebene Handle. Windows XP und spätere Versionen.</p></li></ul> | 
| <p>JET_errNoBackup</p> | <p>Der Vorgang ist fehlgeschlagen, da keine externe Sicherung durchgeführt wird.</p> | 
| <p>JET_errNotInitialized</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz noch nicht initialisiert wurde.</p> | 
| <p>JET_errReadVerifyFailure</p> | <p>Fehler beim Vorgang, weil beim Lesen einer Datenbankseite aus einer Datenbankdatei oder einer Datenbankpatchdatei eine nicht wiederherstellbare Datenbeschädigung erkannt wurde.</p> | 
| <p>JET_errLogReadVerifyFailure</p> | <p>Fehler beim Vorgang, weil beim Lesen einer Transaktionsprotokolldatei eine nicht wiederherstellbare Datenbeschädigung erkannt wurde. Dieser Fehler wird nur von xp Windows und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da ein Wiederherstellungsvorgang für die -Instanz durchgeführt wird, die der Sitzung zugeordnet ist.</p> | 
| <p>JET_errRunningInMultiInstanceMode</p> | <p>Der Vorgang ist fehlgeschlagen, weil versucht wurde, die Engine im Legacymodus (Windows 2000-Kompatibilitätsmodus) zu verwenden, bei dem nur eine Instanz unterstützt wird, wenn tatsächlich bereits mehrere Instanzen vorhanden sind.</p> | 
| <p>JET_errTermInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz heruntergefahren wird.</p> | 



Bei Erfolg wird der nächste Daten chunk aus der Datei in den Ausgabepuffer eingelesen. Die tatsächliche Anzahl der abgerufenen Bytes wird ebenfalls zurückgegeben. Der Dateioffset, an dem der nächste Leseschritt erfolgt, wird um diesen Betrag erweitert.

Bei einem Fehler ist der Status des Ausgabepuffers nicht definiert. Der Fehler führt zum Abbruch des gesamten Sicherungsprozesses für die Instanz. Bei Windows XP und späteren Versionen wird die Sicherung nicht abgebrochen, wenn beim Lesen einer Datenbankdatei ein Fehler aufgetreten ist. Die Sicherung dieser Datenbankdatei wird jedoch weiterhin abgebrochen, und das entsprechende Handle wird automatisch geschlossen.

#### <a name="remarks"></a>Bemerkungen

Jeder Aufruf von **JetReadFile** mit einem Handle, das bereits alle Daten in der zugrunde liegenden Datei zurückgegeben hat (z. B. ein vorheriger Aufruf, der weniger Bytes als die Größe des Ausgabepuffers zurückgegeben hat), ist immer erfolgreich, gibt jedoch keine Bytes an Daten zurück.

Ein großer Ausgabepuffer sollte verwendet werden, um die Sicherungsleistung zu maximieren. Möglicherweise sind einige Experimente erforderlich, um den richtigen Kompromiss zwischen Ressourcenverbrauch und Durchsatz für eine bestimmte Situation zu finden. Der Ausgabepuffer sollte in jedem Fall nicht kleiner als 64 KB sein.

Mehrere gleichzeitige Aufrufe von **JetReadFile** mit demselben Dateihandles werden nicht unterstützt. Dies bedeutet, dass es nicht möglich ist, mehrere Puffer zum gleichzeitigen Lesen für dieselbe Datei in die Warteschlange zu stellen, um einen hohen sequenziellen Durchsatz zu erzielen. Stattdessen sollte ein einzelner großer Puffer verwendet werden.

Wenn die Instanz so konfiguriert ist, dass die Datenbankseitenbereinigung aktiviert ist (siehe JET_paramZeroDatabaseDuringBackup unter Systemparameter), werden gelöschte Daten als Nebeneffekt eines Aufrufs von **JetReadFile** für die Datenbankdatei aus der Datenbank entfernt.

Es ist sehr wichtig zu verstehen, wie Sicherungen und Datenbeschädigungen interagieren. Wenn die Datenbank-Engine während einer Sicherung eine Datenbeschädigung erkennt, kann die Sicherung der betroffenen Datenbank oder der gesamten Instanz nicht wiederhergestellt werden. Dies ist eine bewusste Entwurfsentscheidung zum Schutz vor Datenverlust. Wenn die Datenbank-Engine eine Sicherung erfolgreich durchführen konnte, wenn eine Datenbeschädigung vorhanden war, kann eine ältere, nicht korrupierte Sicherung als Ergebnis verworfen werden. Dies wäre unerfreulich, da es möglich wäre, die Datenbeschädigung auf der Liveinstanz zu beheben, indem diese Sicherung wiederhergestellt und alle Transaktionsprotokolldateien für diese Datenbank wieder angezeigt werden. In diesem Szenario ohne Datenverlust wird davon ausging, dass die zirkuläre Protokollierung nicht aktiviert ist (siehe [JET_paramCircularLog](./transaction-log-parameters.md) unter [Systemparameter](./extensible-storage-engine-system-parameters.md)).

Es ist auch wichtig zu verstehen, dass die Streamingsicherung am wahrscheinlichsten erkannt wird, wenn eine Datenbeschädigung vorhanden ist. Dies ist der Fall, da die Streamingsicherung der einzige Prozess ist, der routinemäßig jede einzelne Seite der Datenbankdatei überprüft. Es ist auch wahrscheinlich, dass die Streamingsicherung der erste Prozess ist, um die frühen Anzeichen von Hardwarefehlern zu erkennen, die sich durch zeitweilige Datenbeschädigungsfehler manifestieren. Dies liegt an der Menge der von der Sicherung abgerufenen Daten und der Geschwindigkeit, mit der sie abgerufen werden.

Datenbeschädigungen werden von der Datenbank-Engine mithilfe von Blocküberprüfungen erkannt. Diese Prüfsummen werden direkt vor dem Schreiben einer Datenbankseite festgelegt und auf einer gelesenen Datenbankseite überprüft. Mit diesem Schema kann die Datenbank-Engine feststellen, dass Daten zu einem bestimmten Zeitpunkt beschädigt wurden. Die Datenbank-Engine kann die Quelle der Beschädigung jedoch nicht ermitteln. In der Vergangenheit wurde festgestellt, dass die vorherrschende Ursache einer solchen Beschädigung aus anderen Quellen als der Datenbank-Engine selbst stammt.

#### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | 
| <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_HANDLE](./jet-handle.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetOpenFile](./jetopenfile-function.md)  
[JetStopService](./jetstopservice-function.md)  
[Systemparameter](./extensible-storage-engine-system-parameters.md)
