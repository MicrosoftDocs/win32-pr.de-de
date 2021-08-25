---
description: Weitere Informationen finden Sie unter JetSetSessionContext-Funktion.
title: JetSetSessionContext-Funktion
TOCTitle: JetSetSessionContext Function
ms:assetid: e44efadf-a5c7-408a-ad68-56646b6ea650
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294124(v=EXCHG.10)
ms:contentKeyID: 32765738
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetSessionContext
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 61df6b5396a5bffcef4f7e32e9a2c32477d019e0
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465287"
---
# <a name="jetsetsessioncontext-function"></a>JetSetSessionContext-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetsetsessioncontext-function"></a>JetSetSessionContext-Funktion

Die **JetSetSessionContext-Funktion** ordnet dem aktuellen Thread mithilfe des angegebenen Kontexthandvers eine Sitzung zu. Diese Zuordnung überschreibt die Standard-Engine-Anforderung, dass eine Transaktion für eine bestimmte Sitzung vollständig im selben Thread erfolgen muss.

```cpp
    JET_ERR JET_API JetSetSessionContext(
      __in          JET_SESID sesid,
      __in          JET_API_PTR ulContext
    );
```

### <a name="parameters"></a>Parameter

*sesid*

Die Sitzung, die für diesen Aufruf verwendet werden soll.

*ulContext*

Ein eindeutiger Bezeichner, dem diese Sitzung zugeordnet wird.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da alle Aktivitäten auf der -Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufs von <a href="gg269240(v=exchg.10).md">JetStopService beendet wurden.</a></p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da für die -Instanz, die der Sitzung zugeordnet ist, ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen.</p><p><strong>Windows XP:</strong>  Dieser Rückgabewert wird in xp Windows eingeführt.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Einer der bereitgestellten Parameter enthielt einen unerwarteten Wert, oder die Kombination mehrerer Parameterwerte führte zu einem unerwarteten Ergebnis. Dieser Fehler wird von <strong>JetSetSessionContext unter</strong> den folgenden Bedingungen zurückgegeben:</p><ul><li><p><em>ulContext</em> ist NULL</p></li><li><p><em>ulContext</em> ist -1</p></li></ul> | 
| <p>JET_errNotInitialized</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die -Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da ein Wiederherstellungsvorgang für die -Instanz durchgeführt wird, die der Sitzung zugeordnet ist.</p> | 
| <p>JET_errSessionContextAlreadySet</p> | <p>Die Sitzung konnte dem aktuellen Thread nicht zugeordnet werden, da sie bereits einem Thread zugeordnet wurde.</p> | 
| <p>JET_errTermInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die -Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</p> | 



Wenn diese Funktion erfolgreich ausgeführt wird, wird die Sitzung dem aktuellen Thread zugeordnet. Es erfolgt keine Änderung des Datenbankstatus.

Wenn diese Funktion fehlschlägt, bleibt der Sitzungszustand unverändert. Es erfolgt keine Änderung des Datenbankstatus.

#### <a name="remarks"></a>Hinweise

Eine Sitzung wird normalerweise für die Dauer einer Transaktion an einen bestimmten Thread gebunden. Dieses Verhalten soll Anwendungen dabei helfen, die konzeptionell nicht empfohlenen Freigaben einer einzelnen Sitzung für mehrere Threads zu erkennen und zu verhindern. Manchmal funktioniert diese einfache Überprüfung nicht mit der Architektur der Anwendung. Wenn die Anwendung beispielsweise serverseitige Objekte mithilfe eines Threadpools hosten und Transaktionen mehrere Serveraufrufe an ein bestimmtes Objekt umfassen, kann dieser Schutz dazu führen, dass einige dieser Aufrufe mit JET_errSessionSharingViolation fehlschlagen, obwohl das Verwendungsmuster korrekt ist. Diese Situation kommt bei COM-Objektservern häufig vor.

**JetSetSessionContext** und [JetResetSessionContext](./jetresetsessioncontext-function.md) lösen dieses Problem, indem sie diese Sitzungsfreigabeprüfung etwas flexibler gestalten. Wenn die Anwendung beginnt, eine Reihe von ESE-API-Aufrufen mithilfe einer bestimmten Sitzung zu tätigen, legt sie zuerst den Sitzungskontext auf einen bestimmten Wert fest. Diese Aktion ordnet die Sitzung dem aufrufenden Thread zu. Im angegebenen Beispiel könnte dieser Kontext die Adresse des Objekts sein, das das JET-Sitzungshand handle enthält. Nachdem die ESE-API-Aufrufe erfolgt sind, setzt die Anwendung den Sitzungskontext zurück. Durch diese Aktion wird die Sitzung vom aufrufenden Thread entfernt. Das -Objekt und seine Sitzung können dann auch dann von einem anderen Thread verwendet werden, wenn die Sitzung über eine aktive Transaktion verfügt.

Es ist wichtig zu beachten, **dass JetSetSessionContext** aufgerufen werden muss, bevor eine Transaktion für diese Sitzung geöffnet wird, da die Zuordnung nicht funktioniert.

**JetSetSessionContext** ist threadsicher. Mehrere Threads können versuchen, gleichzeitig einen Threadkontext für dieselbe Sitzung zu setzen, und nur einer gewinnt. Diese Tatsache kann von der Anwendung als Mittel zum Zuordnen einer Sitzung aus einem Pool verwendet werden, ohne den externen Zustand der Zuordnung zu speichern.

#### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_API_PTR](./jet-api-ptr.md)  
[JET_ERR](./jet-err.md)  
[JetResetSessionContext](./jetresetsessioncontext-function.md)  
[JET_SESID](./jet-sesid.md)  
[JetStopService](./jetstopservice-function.md)
