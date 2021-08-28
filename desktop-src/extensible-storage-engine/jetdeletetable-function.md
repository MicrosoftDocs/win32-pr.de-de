---
description: Weitere Informationen finden Sie unter JetDeleteTable-Funktion.
title: JetDeleteTable-Funktion
TOCTitle: JetDeleteTable Function
ms:assetid: e8a4131f-a69b-41f3-94c6-a1607fc23c1f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294128(v=EXCHG.10)
ms:contentKeyID: 32765742
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDeleteTable
- JetDeleteTableA
- JetDeleteTableW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2cdac49d766835a0d26a3b9d474b8759a552ed1d
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984903"
---
# <a name="jetdeletetable-function"></a>JetDeleteTable-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetdeletetable-function"></a>JetDeleteTable-Funktion

Die **JetDeleteTable-Funktion** löscht eine Tabelle in einer ESE-Datenbank.

```cpp
    JET_ERR JET_API JetDeleteTable(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szTableName
    );
```

### <a name="parameters"></a>Parameter

*sesid*

Der Datenbanksitzungskontext, der für den API-Aufruf verwendet werden soll.

*Dbid*

Der Datenbankbezeichner, der für den API-Aufruf verwendet werden soll.

*szTableName*

Der Name der zu löschenden Tabelle.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errTableInUse</p> | <p>Es wurde versucht, eine Tabelle zu löschen, während eine andere Sitzung über eine geöffnete Tabellen-ID (<a href="gg269182(v=exchg.10).md">JET_TABLEID</a>) mit <a href="gg294118(v=exchg.10).md">JetOpenTable</a> oder <a href="gg269193(v=exchg.10).md">JetDupCursor verfügt.</a></p> | 
| <p>JET_errCannotDeletetemporary Tabelle</p> | <p>Es wurde versucht, eine temporäre Tabelle zu löschen. Eine temporäre Tabelle wird automatisch gelöscht, wenn sie mit <a href="gg294087(v=exchg.10).md">JetCloseTable geschlossen wird.</a></p> | 
| <p>JET_errCannotDeleteTemplateTable</p> | <p>Es wurde versucht, eine Vorlagentabelle zu löschen, d. b. eine Tabelle, von der DDL geerbt werden kann.</p> | 



#### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | 
| <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implementiert als <strong>JetDeleteTableW</strong> (Unicode) und <strong>JetDeleteTableA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_DBID](./jet-dbid.md)  
[JET_SESID](./jet-sesid.md)  
[JetCloseTable](./jetclosetable-function.md)
