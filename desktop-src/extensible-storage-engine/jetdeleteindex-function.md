---
description: Weitere Informationen finden Sie unter JetDeleteIndex-Funktion.
title: JetDeleteIndex-Funktion
TOCTitle: JetDeleteIndex Function
ms:assetid: c540503b-d5a6-47f2-9113-9650891c4b6d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294081(v=EXCHG.10)
ms:contentKeyID: 32765696
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDeleteIndexW
- JetDeleteIndexA
- JetDeleteIndex
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4170bd4def6ad60953189923252e2d775765b03d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478016"
---
# <a name="jetdeleteindex-function"></a>JetDeleteIndex-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetdeleteindex-function"></a>JetDeleteIndex-Funktion

Die **JetDeleteIndex-Funktion** löscht einen Index aus einer Tabelle.

```cpp
    JET_ERR JET_API JetDeleteIndex(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_PCSTR szIndexName
    );
```

### <a name="parameters"></a>Parameter

*sesid*

Der Datenbanksitzungskontext, der für den API-Aufruf verwendet werden soll.

*tableid*

Die Tabelle, die die zu löschende Spalte enthält.

*szIndexName*

Der Name des zu löschenden Indexes.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errFixedDDL</p> | <p>Es wurde versucht, einen Index aus einer festen Tabelle zu löschen (z. B. einen Index, der mit JET_bitTableCreateFixedDDL erstellt wurde).</p> | 
| <p>JET_errFixedInheritedDDL</p> | <p>Es wurde versucht, einen Index aus einer Vorlagentabelle zu löschen. Eine Vorlagentabelle verfügt über eine feste DDL.</p> | 
| <p>JET_errIndexNotFound</p> | <p>Der Index mit dem Namen in <em>szIndexName</em> wurde nicht gefunden.</p> | 
| <p>JET_errPermissionDenied</p> | <p>Die Tabelle kann nicht aktualisiert werden, da sie schreibgeschützt geöffnet wurde.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>Mehrere Threads haben versucht, dieselbe Datenbanksitzung zu verwenden.</p> | 
| <p>JET_errTransReadOnly</p> | <p>Die Transaktion wurde als schreibgeschützte Transaktion geöffnet.</p> | 



#### <a name="remarks"></a>Hinweise

Wenn der Index erfolgreich ist, wird er gelöscht und kann daher später nicht mehr verwendet werden. Es darf keine aktive Transaktion mit dem Index geben.

Bei Erfolg wird die Währung vor dem ersten Datensatz festgelegt.

#### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Implementiert als <strong>JetDeleteIndexW</strong> (Unicode) und <strong>JetDeleteIndexA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCreateIndex](./jetcreateindex-function.md)  
[JetCreateIndex2](./jetcreateindex2-function.md)
