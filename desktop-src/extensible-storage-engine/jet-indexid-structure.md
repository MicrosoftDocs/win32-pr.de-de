---
description: 'Weitere Informationen finden Sie hier: JET_INDEXID Struktur'
title: JET_INDEXID Struktur
TOCTitle: JET_INDEXID Structure
ms:assetid: 8b1d90f0-bc93-4b30-90d1-b9e93ad26654
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269327(v=EXCHG.10)
ms:contentKeyID: 32765617
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
ms.openlocfilehash: e1a9c6a971e44604240d750163f0570937f9d4db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364247"
---
# <a name="jet_indexid-structure"></a>JET_INDEXID Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_indexid-structure"></a>JET_INDEXID Struktur

Die **JET_INDEXID** -Struktur enthält eine Index-ID. Eine Index-ID ist ein Hinweis, der verwendet wird, um die Auswahl des aktuellen Indexes mithilfe von [jetsetcurrentindex](./jetsetcurrentindex-function.md)zu beschleunigen. Dies ist besonders nützlich, wenn eine Tabelle eine große Anzahl von Indizes enthält. Die Index-ID kann mit [jetgetindexinfo](./jetgetindexinfo-function.md) oder [jetgettableindexinfo](./jetgettableindexinfo-function.md)abgerufen werden.

```cpp
    typedef struct tagJET_INDEXID {
      unsigned long cbStruct;
      char rgbIndexId[sizeof(JET_API_PRT) + sizeof(unsigned long) + sizeof(unsigned long)];
    } JET_INDEXID;
```

### <a name="members"></a>Member

**cbStruct**

Die Größe (in Bytes) der Index-ID.

Dies ist die tatsächliche Größe der Index-ID, die im Ausgabepuffer von [jetgetindexinfo](./jetgetindexinfo-function.md) oder [jetgettableindexinfo](./jetgettableindexinfo-function.md)zurückgegeben wird.

**rgbindexid**

Ein undurchsichtiges BLOB von Informationen, die von der-Engine verwendet werden, um schnell einen Index im Schema Cache zu identifizieren.

Versuchen Sie nicht, das BLOB von Informationen zu interpretieren. Es handelt sich nicht um eine festgelegte Größe.

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

[Jetgetindexinfo](./jetgetindexinfo-function.md)  
[Jetgettableindexinfo](./jetgettableindexinfo-function.md)  
[Jetgettableinfo](./jetgettableinfo-function.md)  
[Jetsetcurrentindex](./jetsetcurrentindex-function.md)
