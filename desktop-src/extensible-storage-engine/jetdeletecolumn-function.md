---
description: Weitere Informationen finden Sie unter JetDeleteColumn-Funktion.
title: JetDeleteColumn-Funktion
TOCTitle: JetDeleteColumn Function
ms:assetid: b2f4be8c-7ea9-4f66-925b-4e9c14d9d475
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294062(v=EXCHG.10)
ms:contentKeyID: 32765677
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDeleteColumnA
- JetDeleteColumnW
- JetDeleteColumn
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fd20ba923157d50b3130250f4784ea9bfb19b9b1
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476446"
---
# <a name="jetdeletecolumn-function"></a>JetDeleteColumn-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetdeletecolumn-function"></a>JetDeleteColumn-Funktion

Die **JetDeleteColumn-Funktion** löscht eine Spalte aus einer ESE-Datenbanktabelle.

```cpp
JET_ERR JET_API JetDeleteColumn(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid,
  __in          const tchar* szColumnName
);
```

### <a name="parameters"></a>Parameter

*sesid*

Der Datenbanksitzungskontext, der für den API-Aufruf verwendet werden soll.

*tableid*

Die Tabelle, aus der die Spalte gelöscht werden soll.

*szColumnName*

Der Name der zu löschenden Spalte.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errColumnInUse</p> | <p>Die Spalte wird derzeit verwendet. Sie kann derzeit von einem Index verwendet werden.</p> | 
| <p>JET_errFixedDDL</p> | <p>Es wurde versucht, die feste DDL zu ändern.</p> | 
| <p>JET_errFixedInheritedDDL</p> | <p>Die Spalte mit dem Namen <em>in szColumnName</em> ist in der Vorlagentabelle vorhanden, und die DDL einer Vorlagentabelle kann nicht geändert werden.</p> | 
| <p>JET_errInvalidName</p> | <p>Dies kann zurückgegeben werden, wenn ein fehlerhafter Name für <em>szColumnName</em> angegeben wurde.</p> | 
| <p>JET_errPermissionDenied</p> | <p>Die Tabelle ist nicht beschreibbar. Dies wird möglicherweise zurückgegeben, wenn die Datenbank im schreibgeschützten Modus geöffnet wurde.</p> | 
| <p>JET_errTransReadOnly</p> | <p>Die Transaktion ist eine schreibgeschützte Transaktion.</p> | 



#### <a name="remarks"></a>Hinweise

Der **Aufruf von JetDeleteColumn** ist identisch mit dem Aufruf von [JetDeleteColumn2,](./jetdeletecolumn2-function.md) bei dem *grbit* auf 0 (null) festgelegt ist.

#### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Implementiert als <strong>JetDeleteColumnW</strong> (Unicode) und <strong>JetDeleteColumnA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetDeleteColumn2](./jetdeletecolumn2-function.md)
