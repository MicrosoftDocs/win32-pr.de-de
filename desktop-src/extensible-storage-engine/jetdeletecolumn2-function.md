---
description: 'Weitere Informationen zu: JetDeleteColumn2-Funktion'
title: JetDeleteColumn2-Funktion
TOCTitle: JetDeleteColumn2 Function
ms:assetid: 840b5acd-8bbf-4524-9741-5d74e3427329
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269320(v=EXCHG.10)
ms:contentKeyID: 32765610
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDeleteColumn2
- JetDeleteColumn2A
- JetDeleteColumn2W
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 87e9506048094b77674e85f76f6c1718def44cae
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467167"
---
# <a name="jetdeletecolumn2-function"></a>JetDeleteColumn2-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetdeletecolumn2-function"></a>JetDeleteColumn2-Funktion

Die **JetDeleteColumn2-Funktion** löscht eine Spalte aus einer ESE-Datenbanktabelle und ermöglicht das Festlegen einer *grbit-Option.*

**Windows XP: JetDeleteColumn2** wird in Windows XP eingeführt.

```cpp
    JET_ERR JET_API JetDeleteColumn2(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          const tchar* szColumnName,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parameter

*sesid*

Der Datenbanksitzungskontext, der für den API-Aufruf verwendet werden soll.

*tableid*

Die Tabelle, die die zu löschende Spalte enthält.

*szColumnName*

Der Name der zu löschenden Spalte.

*grbit*

Eine Gruppe von Bits, die null oder mehr der folgenden Optionen angibt.


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_bitDeleteColumnIgnoreTemplateColumns</p> | <p>Wenn JET_bitDeleteColumIgnoreTemplateColumns festgelegt wird, versucht die API nur, Spalten in der abgeleiteten Tabelle zu löschen. Wenn eine Spalte mit diesem Namen in der Basistabelle vorhanden ist, wird sie ignoriert.</p> | 



### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errColumnInUse</p> | <p>Die Spalte wird derzeit verwendet. Sie kann derzeit von einem Index verwendet werden.</p> | 
| <p>JET_errFixedDDL</p> | <p>Es wurde versucht, die feste DDL zu ändern.</p> | 
| <p>JET_errFixedInheritedDDL</p> | <p>Die Spalte mit dem Namen <em>szColumnName</em> ist in der Vorlagentabelle vorhanden, und die DDL einer Vorlagentabelle kann nicht geändert werden.</p> | 
| <p>JET_errInvalidName</p> | <p>Dies kann zurückgegeben werden, wenn ein ungültiger Name für <em>szColumnName</em> angegeben wurde.</p> | 
| <p>JET_errPermissionDenied</p> | <p>Die Tabelle kann nicht geschrieben werden. Dies wird möglicherweise zurückgegeben, wenn die Datenbank im schreibgeschützten Modus geöffnet wurde.</p> | 
| <p>JET_errTransReadOnly</p> | <p>Die Transaktion ist eine schreibgeschützte Transaktion.</p> | 



#### <a name="remarks"></a>Hinweise

Das Aufrufen von [JetDeleteColumn](./jetdeletecolumn-function.md) ist identisch mit dem Aufrufen von **JetDeleteColumn2,** wobei *grbit* auf 0 (null) festgelegt ist.

#### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista oder Windows XP.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008 oder Windows Server 2003.</p> | | <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Implementiert als <strong>JetDeleteColumn2W</strong> (Unicode) und <strong>JetDeleteColumn2A</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetDeleteColumn](./jetdeletecolumn-function.md)
