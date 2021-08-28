---
description: 'Weitere Informationen finden Sie unter: JetResetSessionContext-Funktion'
title: JetResetSessionContext-Funktion
TOCTitle: JetResetSessionContext Function
ms:assetid: 537a4753-b804-457a-9a13-53e8d1056eab
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269250(v=EXCHG.10)
ms:contentKeyID: 32765552
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetResetSessionContext
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3bf2c87c3021bffea259b5e94741f1e8846e7747
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481276"
---
# <a name="jetresetsessioncontext-function"></a>JetResetSessionContext-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetresetsessioncontext-function"></a>JetResetSessionContext-Funktion

Die **JetResetSessionContext-Funktion** disassoziiert eine Sitzung vom aktuellen Thread.

```cpp
    JET_ERR JET_API JetResetSessionContext(
      __in          JET_SESID sesid
    );
```

### <a name="parameters"></a>Parameter

*sesid*

Die Sitzung, die für diesen Aufruf verwendet werden soll.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da für die der Sitzung zugeordnete Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen.</p><p>Dieser Fehler wird nur von xp Windows und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errNotInitialized</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz noch nicht initialisiert wurde.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da ein Wiederherstellungsvorgang für die -Instanz durchgeführt wird, die der Sitzung zugeordnet ist.</p> | 
| <p>JET_errSessionContextNotSetByThisThread</p> | <p>Die Sitzung konnte nicht vom aktuellen Thread entfernt werden, da sie einem anderen Thread zugeordnet ist.</p> | 
| <p>JET_errTermInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz heruntergefahren wird.</p> | 



Bei Erfolg wird die Sitzung vom aktuellen Thread entfernt. Es erfolgt keine Änderung des Datenbankstatus.

Bei einem Fehler bleibt der Sitzungszustand unverändert. Es erfolgt keine Änderung des Datenbankstatus.

#### <a name="remarks"></a>Hinweise

**JetResetSessionContext** muss für denselben Thread aufgerufen werden, der [JetSetSessionContext für](./jetsetsessioncontext-function.md) eine bestimmte Sitzung aufgerufen hat.

#### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_API_PTR](./jet-api-ptr.md)  
[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JetSetSessionContext](./jetsetsessioncontext-function.md)
