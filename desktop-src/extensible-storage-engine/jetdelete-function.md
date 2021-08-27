---
description: Weitere Informationen finden Sie unter JetDelete-Funktion.
title: JetDelete-Funktion
TOCTitle: JetDelete Function
ms:assetid: 807de5ba-2f4b-4779-ab29-a1f094beecc1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269315(v=EXCHG.10)
ms:contentKeyID: 32765605
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDelete
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1e5d8fe6cfc4e0521866a12383aa34f7858432d3
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477606"
---
# <a name="jetdelete-function"></a>JetDelete-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetdelete-function"></a>JetDelete-Funktion

Die **JetDelete-Funktion** löscht den aktuellen Datensatz in einer Datenbanktabelle.

```cpp
    JET_ERR JET_API JetDelete(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid
    );
```

### <a name="parameters"></a>Parameter

*sesid*

Der Datenbanksitzungskontext, der für den API-Aufruf verwendet wird.

*tableid*

Der Cursor in einer Datenbanktabelle. Die aktuelle Zeile wird gelöscht.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errCallbackFailed</p> | <p>Die Rückruffunktion ist in irgendeiner Weise fehlgeschlagen. Beispielsweise werden Zugriffsverletzungen in Rückruffunktionen erfasst und in JET_errCallbackFailed. Dieser Fehler wird nur von xp Windows und höher zurückgegeben.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Es ist nicht möglich, den Vorgang abschließen, da alle Aktivitäten auf der -Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufs von <a href="gg269240(v=exchg.10).md">JetStopService beendet wurden.</a></p> | 
| <p>JET_errIllegalOperation</p> | <p>Der durch <em>tableid angegebene Cursor</em> unterstützt das Löschen nicht. Weitere Informationen finden Sie im Abschnitt mit den Hinweisen.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da für die der Sitzung zugeordnete Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen. Dieser Fehler wird nur von xp Windows und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>Der durch <em>tableid angegebene Cursor</em> befindet sich nicht in einem Datensatz.</p> | 
| <p>JET_errNotInitialized</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz noch nicht initialisiert wurde.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da ein Wiederherstellungsvorgang für die -Instanz durchgeführt wird, die der Sitzung zugeordnet ist.</p> | 
| <p>JET_errPermissionDenied</p> | <p>Die Datenbank-Engine verfügt nicht über ausreichende Berechtigungen zum Löschen des Datensatzes. Dies kann passieren, wenn die Datenbankdatei mit schreibgeschützten Zugriff geöffnet wurde.</p> | 
| <p>JET_errRollbackError</p> | <p>Ein Updatepuffer (siehe <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a>) ist vorhanden, aber nicht für alle Änderungen, die an Spalten vom Typ JET_coltypLongText und/oder Spalten des Typs JET_coltypLongBinary vorgenommen wurden, kann ein Rollback ausgeführt werden.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>Es ist unzulässig, dieselbe Sitzung von mehr als einem Thread gleichzeitig zu verwenden. Dieser Fehler wird nur von xp Windows und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errTermInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz heruntergefahren wird.</p> | 
| <p>JET_errTransReadOnly</p> | <p>Die Transaktion ist eine schreibgeschützte Transaktion und unterstützt keine Löschungen.</p> | 
| <p>JET_errVersionStoreOutOfMemory</p> | <p>Fehler beim Vorgang, da nicht genügend Arbeitsspeicher vorhanden ist, um Transaktionsinformationen zum Update zu speichern.</p> | 
| <p>JET_errWriteConflict</p> | <p>Eine andere Sitzung hat den Datensatz zuvor für das Update gesperrt. Das von dieser Sitzung versuchte Update ist fehlgeschlagen.</p> | 



Bei Erfolg bleibt die Währung direkt vor dem nächsten Datensatz. Wenn der gelöschte Datensatz der letzte in der Tabelle war, bleibt die Währung am Ende der Tabelle (d. h. nach dem neuen letzten Datensatz). Wenn der gelöschte Datensatz der einzige Datensatz in der Tabelle war, wird die Währung auf den Anfang festgelegt.

Die entsprechenden Indizes werden automatisch aktualisiert.

Wenn ein Update vorbereitet wird [(mit JetPrepareUpdate),](./jetprepareupdate-function.md)wird es abgebrochen. Der Updatepuffer wird zurückgesetzt.

Bei einem Ausfall bleibt die Währung unverändert. Wenn ein Update vorbereitet ist (siehe [JetPrepareUpdate),](./jetprepareupdate-function.md)kann der Updatepuffer zurückgesetzt werden.

#### <a name="remarks"></a>Hinweise

Nicht alle Tabellen unterstützen das Löschen von Zeilen. Eine temporäre Tabelle unterstützt normalerweise nicht das Löschen von Zeilen. Das Löschen von Datensätzen kann für temporäre Tabellen aus vielen Gründen aktiviert werden. Einige davon sind:

  - JET_bitTTUpdatable wurde während der Erstellung angegeben.

  - Große temporäre Tabellen können das Löschen unterstützen, wenn sie mit einem JET_bitTTScrollable oder JET_bitTTIndexed. Der Schwellenwert, bei dem eine temporäre Tabelle "groß" wird, beträgt derzeit 64 KB, kann aber in zukünftigen Versionen geändert werden.

Windows XP und höher. Rückruffunktionen können von **JetDelete** aufgerufen werden, einschließlich JET_cbtypBeforeDelete und JET_cbtypAfterDelete.

Es ist wichtig, die Auswirkungen einer großen Anzahl von Aktualisierungsvorgängen innerhalb einer einzelnen Transaktion zu verstehen. Jedes Update der Datenbank muss von der Datenbank-Engine im Versionsspeicher nachverfolgt werden. Der Versionsspeicher enthält einen Livedatensatz aller verschiedenen Versionen jedes Datensatzes oder Indexeintrags in der Datenbank, die von allen aktiven Transaktionen angezeigt werden können. Diese Versionen werden verwendet, um die Parallelitätssteuerung mit mehreren Versionen zu unterstützen, die von der Datenbank-Engine verwendet wird, um Transaktionen mithilfe der Momentaufnahmeisolation zu unterstützen. Sobald die Datenbank-Engine die zum Speichern dieser Versionen verwendeten Ressourcen ausgeschöpft hat, kann sie keine weiteren Änderungen mehr akzeptieren, bis einige Transaktionen abgeschlossen sind, um das Wiederverlangen dieser Ressourcen zu ermöglichen. Wenn sich die Engine in diesem Zustand befindet, werden alle Updates mit JET_errVersionStoreOutOfMemory. Die für die Datenbank-Engine verfügbaren Ressourcen zum Speichern dieser Versionen können mit [JetSetSystemParameter mit](./jetsetsystemparameter-function.md) JET_paramMaxVerPages *und* *JET_paramGlobalMinVerPages.*

#### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetOpenTempTable](./jetopentemptable-function.md)  
[JetPrepareUpdate](./jetprepareupdate-function.md)  
[Systemparameter](./extensible-storage-engine-system-parameters.md)
