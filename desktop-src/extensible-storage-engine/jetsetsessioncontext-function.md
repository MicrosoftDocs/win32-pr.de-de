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
ms.openlocfilehash: 7ac368caaff5ec652a6dc7ad490e7418e62888b7
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122986633"
---
# <a name="jetsetsessioncontext-function"></a>JetSetSessionContext-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetsetsessioncontext-function"></a>JetSetSessionContext-Funktion

Die **JetSetSessionContext-Funktion** ordnet dem aktuellen Thread mithilfe des angegebenen Kontexthandle eine Sitzung zu. Diese Zuordnung überschreibt die Standard-Engine-Anforderung, dass eine Transaktion für eine bestimmte Sitzung vollständig im selben Thread erfolgen muss.

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

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufs von <a href="gg269240(v=exchg.10).md">JetStopService</a>beendet wurden.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da für die Instanz, die der Sitzung zugeordnet ist, ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen.</p><p><strong>Windows XP:</strong>  Dieser Rückgabewert wird in Windows XP eingeführt.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Einer der bereitgestellten Parameter enthielt einen unerwarteten Wert, oder die Kombination mehrerer Parameterwerte führte zu einem unerwarteten Ergebnis. Dieser Fehler wird von <strong>JetSetSessionContext</strong> unter den folgenden Bedingungen zurückgegeben:</p><ul><li><p><em>ulContext</em> ist NULL</p></li><li><p><em>ulContext</em> ist -1</p></li></ul> | 
| <p>JET_errNotInitialized</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da ein Wiederherstellungsvorgang für die Instanz ausgeführt wird, die der Sitzung zugeordnet ist.</p> | 
| <p>JET_errSessionContextAlreadySet</p> | <p>Die Sitzung konnte dem aktuellen Thread nicht zugeordnet werden, da sie bereits einem Thread zugeordnet wurde.</p> | 
| <p>JET_errTermInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</p> | 



Wenn diese Funktion erfolgreich ist, wird die Sitzung dem aktuellen Thread zugeordnet. Es wird keine Änderung am Datenbankzustand vorgenommen.

Wenn diese Funktion fehlschlägt, bleibt der Sitzungszustand unverändert. Es wird keine Änderung am Datenbankzustand vorgenommen.

#### <a name="remarks"></a>Bemerkungen

Eine Sitzung ist normalerweise für die Dauer einer Transaktion an einen bestimmten Thread gebunden. Dieses Verhalten soll Anwendungen dabei helfen, die konzeptionell falsch empfohlenen Freigaben einer einzelnen Sitzung zwischen mehreren Threads zu erkennen und zu verhindern. Manchmal funktioniert diese einfache Überprüfung nicht mit der Architektur der Anwendung. Wenn die Anwendung beispielsweise serverseitige Objekte mithilfe eines Threadpools hostet und Transaktionen mehrere Serveraufrufe an ein bestimmtes Objekt umfassen, kann dieser Schutz dazu führen, dass einige dieser Aufrufe mit JET_errSessionSharingViolation fehlschlagen, obwohl das Verwendungsmuster richtig ist. Diese Situation ist bei COM-Objektservern üblich.

**JetSetSessionContext** und [JetResetSessionContext](./jetresetsessioncontext-function.md) lösen dieses Problem, indem sie die Sitzungsfreigabeprüfung etwas flexibler gestalten. Wenn die Anwendung beginnt, eine Reihe von ESE-API-Aufrufen mit einer bestimmten Sitzung vorzunehmen, legt sie zuerst den Sitzungskontext auf einen bestimmten Wert fest. Diese Aktion ordnet die Sitzung dem aufrufenden Thread zu. Im angegebenen Beispiel kann dieser Kontext die Adresse des Objekts sein, das das JET-Sitzungshandle enthält. Sobald die ESE-API-Aufrufe durchgeführt wurden, setzt die Anwendung den Sitzungskontext zurück. Diese Aktion trennt die Zuordnung der Sitzung zum aufrufenden Thread. Das Objekt und seine Sitzung können dann auch dann von einem anderen Thread verwendet werden, wenn die Sitzung über eine aktive Transaktion verfügt.

Es ist wichtig zu beachten, dass **JetSetSessionContext** aufgerufen werden muss, bevor eine Transaktion für diese Sitzung geöffnet wird. Andernfalls funktioniert die Zuordnung nicht.

**JetSetSessionContext** ist threadsicher. Mehrere Threads können gleichzeitig versuchen, einen Threadkontext in derselben Sitzung festzulegen, und nur einer gewinnt. Diese Tatsache kann von der Anwendung verwendet werden, um eine Sitzung aus einem Pool zuzuordnen, ohne den externen Zustand der Zuordnung zu speichern.

#### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | 
| <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_API_PTR](./jet-api-ptr.md)  
[JET_ERR](./jet-err.md)  
[JetResetSessionContext](./jetresetsessioncontext-function.md)  
[JET_SESID](./jet-sesid.md)  
[JetStopService](./jetstopservice-function.md)
