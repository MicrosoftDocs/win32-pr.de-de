---
description: 'Weitere Informationen zu: JET_INDEXRANGE-Struktur'
title: JET_INDEXRANGE-Struktur
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
ms.openlocfilehash: b5b68e7ebf6df39757ab39947201b945e35a3ece85518a3cb202525033cdd214
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118485598"
---
# <a name="jet_indexrange-structure"></a>JET_INDEXRANGE-Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_indexrange-structure"></a>JET_INDEXRANGE-Struktur

Die **JET_INDEXRANGE-Struktur** identifiziert einen Indexbereich, wenn er mit der [JetIntersectIndexes-Funktion](./jetintersectindexes-function.md) verwendet wird.

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_TABLEID tableid;
      JET_GRBIT grbit;
    } JET_INDEXRANGE;
```

### <a name="members"></a>Member

**cbStruct**

Die Größe des **JET_INDEXRANGE** in Bytes.

**tableid**

Ein Cursor, für den zuvor ein Indexbereich mit [JetSetIndexRange](./jetsetindexrange-function.md)festgelegt wurde.

**grbit**

Eine Bitmaske, die aus genau einer der folgenden Besteht.

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
<td><p>Gibt an, dass der Indexbereich normal behandelt werden soll.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitRecordNotInIndex</p></td>
<td><p>Für die zukünftige Verwendung reserviert. Darf nicht verwendet werden.</p></td>
</tr>
</tbody>
</table>


### <a name="remarks"></a>Hinweise

Jede **JET_INDEXRANGE** Struktur, die an [JetIntersectIndexes](./jetintersectindexes-function.md) übergeben wird, stellt einen Indexbereich dar, der durch den API-Aufruf überschneidet wird. Für den Cursor, der in **JET_INDEXRANGE** angegeben wird, muss bereits ein gültiger Indexbereich mit einem erfolgreichen Aufruf von [JetSetIndexRange](./jetsetindexrange-function.md)festgelegt sein.

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
<td><p>Deklariert in Esent.h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Weitere Informationen

[JET_COLUMNID](./jet-columnid.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetIntersectIndexes](./jetintersectindexes-function.md)  
[JetSetIndexRange](./jetsetindexrange-function.md)
