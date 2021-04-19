---
description: 'Weitere Informationen finden Sie hier: JET_INDEXRANGE Struktur'
title: JET_INDEXRANGE Struktur
TOCTitle: JET_INDEXRANGE Structure
ms:assetid: 8e437f7d-1e21-4a0b-a5a5-1c78235a4f80
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269335(v=EXCHG.10)
ms:contentKeyID: 32765624
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
ms.openlocfilehash: ecbd8151be8ef278fc1bddc12323f41abd05b09e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363608"
---
# <a name="jet_indexrange-structure"></a>JET_INDEXRANGE Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_indexrange-structure"></a>JET_INDEXRANGE Struktur

Die **JET_INDEXRANGE** -Struktur identifiziert einen Index Bereich, wenn er mit der [jetintersectindexes](./jetintersectindexes-function.md) -Funktion verwendet wird.

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_TABLEID tableid;
      JET_GRBIT grbit;
    } JET_INDEXRANGE;
```

### <a name="members"></a>Member

**cbStruct**

Die Größe (in Bytes) der **JET_INDEXRANGE**.

**TableID**

Ein Cursor, für den zuvor ein Index Bereich mit [jetsetindexrange](./jetsetindexrange-function.md)festgelegt wurde.

**grbit**

Eine Bitmaske, die aus genau einer der folgenden Elemente besteht.

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
<td><p>JET_bitRecordInIndex</p></td>
<td><p>Gibt an, dass der Index Bereich normal behandelt werden soll.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitRecordNotInIndex</p></td>
<td><p>Für die zukünftige Verwendung reserviert. Darf nicht verwendet werden.</p></td>
</tr>
</tbody>
</table>


### <a name="remarks"></a>Bemerkungen

Jede **JET_INDEXRANGE** Struktur, die an [jetintersectindexes](./jetintersectindexes-function.md) übermittelt wird, stellt einen Index Bereich dar, der durch den API--Befehl interdiert wird. Der Cursor, der in **JET_INDEXRANGE** angegeben ist, muss bereits über einen gültigen Index Bereich verfügen, wobei [jetsetindexrange](./jetsetindexrange-function.md)erfolgreich aufgerufen werden kann.

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
[JET_GRBIT](./jet-grbit.md)  
[JET_TABLEID](./jet-tableid.md)  
[Jetclosetable](./jetclosetable-function.md)  
[Jetintersectindexes](./jetintersectindexes-function.md)  
[Jetsetindexrange](./jetsetindexrange-function.md)
