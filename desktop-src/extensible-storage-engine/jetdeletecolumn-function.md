---
description: 'Weitere Informationen finden Sie unter: jetdeletecolumn-Funktion'
title: Jetdeletecolumn-Funktion
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
ms.openlocfilehash: d7d577447942e36cd49763727473d3f6ddc659b4
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "103961777"
---
# <a name="jetdeletecolumn-function"></a>Jetdeletecolumn-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetdeletecolumn-function"></a>Jetdeletecolumn-Funktion

Die **jetdeletecolumn** -Funktion löscht eine Spalte aus einer ESE-Datenbanktabelle.

```cpp
JET_ERR JET_API JetDeleteColumn(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid,
  __in          const tchar* szColumnName
);
```

### <a name="parameters"></a>Parameter

*-sid*

Der für den API-Befehl zu verwendende Daten Bank Sitzungs Kontext.

*TableID*

Die Tabelle, aus der die Spalte gelöscht werden soll.

*szcolumnname*

Der Name der zu löschenden Spalte.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Rückgabecode</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>Der Vorgang wurde erfolgreich abgeschlossen.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnInUse</p></td>
<td><p>Die Spalte wird derzeit verwendet. Sie kann derzeit von einem Index verwendet werden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFixedDDL</p></td>
<td><p>Es wurde versucht, die festgelegte DDL zu ändern.</p></td>
</tr>
<tr class="even">
<td><p>JET_errFixedInheritedDDL</p></td>
<td><p>Die in <em>szcolumnname</em> genannte Spalte ist in der Vorlagen Tabelle vorhanden, und die DDL einer Vorlagen Tabelle kann nicht geändert werden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidName</p></td>
<td><p>Dieser Fehler kann zurückgegeben werden, wenn ein ungültiger Name für <em>szcolumnname</em> angegeben wurde.</p></td>
</tr>
<tr class="even">
<td><p>JET_errPermissionDenied</p></td>
<td><p>Die Tabelle ist nicht beschreibbar. Dies kann zurückgegeben werden, wenn die Datenbank im schreibgeschützten Modus geöffnet wurde.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTransReadOnly</p></td>
<td><p>Bei der Transaktion handelt es sich um eine schreibgeschützte Transaktion.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Bemerkungen

Der Aufruf von **jetdeletecolumn** ist mit dem Aufrufen von [JetDeleteColumn2](./jetdeletecolumn2-function.md) identisch, wobei *grbit* auf NULL (0) festgelegt ist.

#### <a name="requirements"></a>Anforderungen

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>In "ESENT. h" deklariert.</p></td>
</tr>
<tr class="even">
<td><p><strong>Bibliothek</strong></p></td>
<td><p>Verwenden Sie ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Erfordert ESENT.dll.</p></td>
</tr>
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implementiert als <strong>jetdeletecolumnw</strong> (Unicode) und <strong>jetdeletecolumna</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetDeleteColumn2](./jetdeletecolumn2-function.md)
