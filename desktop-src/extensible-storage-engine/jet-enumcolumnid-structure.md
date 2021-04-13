---
description: 'Weitere Informationen finden Sie hier: JET_ENUMCOLUMNID Struktur'
title: JET_ENUMCOLUMNID Struktur
TOCTitle: JET_ENUMCOLUMNID Structure
ms:assetid: 5480ebf1-4fc9-49b5-bbb3-12542b86c8f1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269251(v=EXCHG.10)
ms:contentKeyID: 32765553
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 356b2a31c682a6ed0392a875c606cfaf20f1aeea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526084"
---
# <a name="jet_enumcolumnid-structure"></a>JET_ENUMCOLUMNID Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_enumcolumnid-structure"></a>JET_ENUMCOLUMNID Struktur

Die **JET_ENUMCOLUMNID** -Struktur listet eine bestimmte Gruppe von Spalten und optional einen bestimmten Satz von Werten für diese Spalten auf, wenn die [jetenumeratecolumns](./jetenumeratecolumns-function.md) -Funktion verwendet wird. [Jetenreeratecolenns](./jetenumeratecolumns-function.md) gibt ein Array von **JET_ENUMCOLUMNID** Strukturen zurück.

```cpp
    typedef struct {
      JET_COLUMNID columnid;
      unsigned long ctagSequence;
      unsigned long* rgtagSequence;
    } JET_ENUMCOLUMNID;
```

### <a name="members"></a>Member

**ColumnID**

Die aufzuzählenden Spalten-ID.

Wenn die Spalten-ID 0 (null) ist, wird die Enumeration dieser Spalte übersprungen und ein entsprechender Slot im Ausgabe Array von [JET_ENUMCOLUMN](./jet-enumcolumn-structure.md) Strukturen mit dem Spalten Status JET_wrnColumnSkipped generiert.

**ctagsequence**

Identifiziert optional ein Array von Spaltenwerten (durch einen 1-basierten Index), die für die angegebene Spalten-ID aufgelistet werden sollen.

Wenn **ctagsequence** gleich 0 (null) ist, wird **rgtagsequence** ignoriert, und alle Spaltenwerte für die angegebene Spalten-ID werden aufgelistet.

Wenn ein Element von **rgtagsequence** gleich 0 (null) ist, wird die Enumeration dieses Spaltenwerts (durch einen einbasierten Index) übersprungen. Ein entsprechender Slot im Ausgabe Array der **JET_ENUMCOLUMNID** Struktur wird mit einem Spalten Statuswert JET_wrnColumnSkipped generiert.

**rgtagsequence**

Ein Array von einbasierten Indizes in das Array von Spaltenwerten für eine angegebene Spalte. Bei einem einzelnen Element handelt es sich um eine in [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md)definierte **itagsequence** . Eine **itagsequence** -Wert von 0 (null) bedeutet "Skip". Eine **itagsequence** von 1 bedeutet, dass der erste Spaltenwert der Spalte zurückgegeben wird, der Wert 2 für den zweiten Wert usw.

### <a name="requirements"></a>Anforderungen

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
</tbody>
</table>


### <a name="see-also"></a>Weitere Informationen

[JET_COLUMNID](./jet-columnid.md)  
[JET_ENUMCOLUMN](./jet-enumcolumn-structure.md)  
[JET_ENUMCOLUMNID]()  
[JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md)  
[Jetenreeratecolumschlag](./jetenumeratecolumns-function.md)
