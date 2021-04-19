---
description: 'Weitere Informationen finden Sie hier: JetDeleteColumn2-Funktion'
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
ms.openlocfilehash: 35e19eb7ac7b133bb690b268426fec9822efefea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366507"
---
# <a name="jetdeletecolumn2-function"></a>JetDeleteColumn2-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetdeletecolumn2-function"></a>JetDeleteColumn2-Funktion

Die **JetDeleteColumn2** -Funktion löscht eine Spalte aus einer ESE-Datenbanktabelle und ermöglicht die Festlegung einer *grbit* -Option.

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

*-sid*

Der für den API-Befehl zu verwendende Daten Bank Sitzungs Kontext.

*TableID*

Die Tabelle, die die zu löschende Spalte enthält.

*szcolumnname*

Der Name der zu löschenden Spalte.

*grbit*

Eine Gruppe von Bits, die NULL oder mehr der folgenden Optionen angibt.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Wert</p></th>
<th><p>Bedeutung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitDeleteColumnIgnoreTemplateColumns</p></td>
<td><p>Das Festlegen von JET_bitDeleteColumIgnoreTemplateColumns bewirkt, dass die API nur versucht, Spalten in der abgeleiteten Tabelle zu löschen. Wenn eine Spalte mit diesem Namen in der Basistabelle vorhanden ist, wird Sie ignoriert.</p></td>
</tr>
</tbody>
</table>


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

Der Aufruf von [jetdeletecolumn](./jetdeletecolumn-function.md) ist mit dem Aufrufen von **JetDeleteColumn2** identisch, wobei *grbit* auf NULL (0) festgelegt ist.

#### <a name="requirements"></a>Anforderungen

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Erfordert Windows Vista oder Windows XP.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Erfordert Windows Server 2008 oder Windows Server 2003.</p></td>
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
<td><p>Implementiert als <strong>JetDeleteColumn2W</strong> (Unicode) und <strong>JetDeleteColumn2A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[Jetdeletecolumn](./jetdeletecolumn-function.md)
