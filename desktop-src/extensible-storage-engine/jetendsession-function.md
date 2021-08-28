---
description: Weitere Informationen finden Sie unter JetEndSession-Funktion.
title: JetEndSession-Funktion
TOCTitle: JetEndSession Function
ms:assetid: a9a8f98a-258e-4fbb-bed0-657581984a07
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294054(v=EXCHG.10)
ms:contentKeyID: 32765660
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEndSession
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2b96ae49ef907cea158d1496339a740e1026ffea
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472566"
---
# <a name="jetendsession-function"></a>JetEndSession-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetendsession-function"></a>JetEndSession-Funktion

Die **JetEndSession-Funktion** beendet die Sitzung und bereinigt alle Ressourcen, die der angegebenen Sitzung zugeordnet sind, und gibt deren Verlagerung wieder auf.

```cpp
    JET_ERR JET_API JetEndSession(
      __in          JET_SESID sesid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parameter

*sesid*

Die zu beendende Sitzung. Zugeordnete Ressourcen werden freigegeben, wenn die Sitzung beendet wird.

*grbit*

Reserviert. Dieser Parameter kann das JET_bitForceSessionClosed enthalten, aber dieses Flag ist reserviert, und das Festlegen hat keine Auswirkungen.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Es ist nicht möglich, den Vorgang abschließen, da alle Aktivitäten auf der -Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufs von <a href="gg269240(v=exchg.10).md">JetStopService beendet wurden.</a></p> | 
| <p>JET_errInvalidParameter</p> | <p>Einer der bereitgestellten Parameter enthielt einen unerwarteten Wert, oder die Kombination mehrerer Parameterwerte führte zu einem unerwarteten Ergebnis.</p> | 
| <p>JET_errInvalidSesid</p> | <p>Die Sitzung war keine gültige JET-Sitzung.</p> | 
| <p>JET_errNotInitialized</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz noch nicht initialisiert wurde.</p> | 
| <p>JET_errOutOfMemory</p> | <p>Fehler beim Vorgang, weil der Arbeitsspeicher nicht zugeordnet werden konnte.</p> | 
| <p>JET_errSessionInUse</p> | <p>Dies bedeutet, dass die Sitzung in einem anderen Thread verwendet wurde oder die Sitzung nicht ordnungsgemäß festgelegt oder zurückgesetzt wurde.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da für die der Sitzung zugeordnete Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen.</p><p>Dieser Fehler wird nur von xp Windows und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errOutOfBuffers</p> | <p>Systemfehler, der angibt, dass keine Puffer mehr sind.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da ein Wiederherstellungsvorgang für die -Instanz durchgeführt wird, die der Sitzung zugeordnet ist.</p> | 
| <p>JET_errTermInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz heruntergefahren wird.</p> | 



Bei Erfolg wird das Sitzungshandy geschlossen und ist nicht verfügbar, und alle Ressourcen im Zusammenhang mit dieser Sitzung werden bereinigt.

Bei einem Fehler gibt es mehrere zusätzliche Fehler, die im Rahmen des Schließens der Sortiertabelle, des Schließens des Cursors und des Transaktionsrollbacks auftreten können. Diese Fehler sind ziemlich unwahrscheinlich und äußerst unwahrscheinlich, wenn Ihre Sitzungen vollständig nicht verwendet werden, wenn **JetEndSession** aufgerufen wird. Diese Fehler werden zurückgegeben, wenn ein Teil der Sitzung nicht ordnungsgemäß bereinigt werden konnte.

#### <a name="remarks"></a>Hinweise

Diese API gibt ein Rollback für alle offenen Transaktionen aus (kein Committed auf Ebene 0). Außerdem werden alle Cursor, die dieser Sitzung zugeordnet sind, und alle Sortiertabellen, die erstellt oder geöffnet wurden, bereinigt.

#### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JetBeginSession](./jetbeginsession-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[JetStopService](./jetstopservice-function.md)
