---
description: 'Weitere Informationen zu: JetCloseTable-Funktion'
title: JetCloseTable-Funktion
TOCTitle: JetCloseTable Function
ms:assetid: c8975145-e48a-4029-9522-1509263019ae
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294087(v=EXCHG.10)
ms:contentKeyID: 32765702
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCloseTable
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fe7f3c084a52faa9b5f011474bd0b502aebd277b
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122989063"
---
# <a name="jetclosetable-function"></a>JetCloseTable-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetclosetable-function"></a>JetCloseTable-Funktion

Die **JetCloseTable-Funktion** schließt eine geöffnete Tabelle in einer Datenbank. Die Tabelle kann eine temporäre tabelle oder eine normale Tabelle sein.

```cpp
JET_ERR JET_API JetCloseTable(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid
);
```

### <a name="parameters"></a>Parameter

*sesid*

Identifiziert den Datenbanksitzungskontext, der für den API-Aufruf verwendet wird.

*tableid*

Identifiziert die zu schließende Tabelle.

Legen Sie *tableid* auf JET_tableidNil fest, um Arbeitsspeicher freizugeben.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 



#### <a name="remarks"></a>Bemerkungen

Diese Funktion muss für alle Tabellen aufgerufen werden, die mit [JetOpenTable](./jetopentable-function.md)geöffnet wurden.

Die Ausnahme von dieser Regel tritt auf, wenn [JetOpenTable](./jetopentable-function.md) in einer Transaktion aufgerufen wird und für die Transaktion ein Rollback ausgeführt wird (mit [JetRollback](./jetrollback-function.md)). Beim Rollback einer Transaktion wird die Tabelle automatisch geschlossen. In diesem Fall ist es ein Fehler, die Tabelle mit **JetCloseTable** zu schließen.

#### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | 
| <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetOpenTable](./jetopentable-function.md)  
[JetRollback](./jetrollback-function.md)
