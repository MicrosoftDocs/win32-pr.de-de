---
description: 'Weitere Informationen zu: JET_LGPOS-Struktur'
title: JET_LGPOS-Struktur
TOCTitle: JET_LGPOS Structure
ms:assetid: dbce1a60-b32b-40c1-a215-e93bb77cd8c1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294113(v=EXCHG.10)
ms:contentKeyID: 32765727
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
ms.openlocfilehash: abf3ca2996e75d2abfe6fc766ec6f5bbd30054eeb9dd8406fe2747307a00c4a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119109257"
---
# <a name="jet_lgpos-structure"></a>JET_LGPOS-Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_lgpos-structure"></a>JET_LGPOS-Struktur

Die **JET_LGPOS-Struktur** enthält Daten, die für den Protokollierungsmechanismus der Datenbank-Engine intern sind. Diese Struktur wird als intern betrachtet.

```cpp
    typedef struct {
      unsigned short ib;
      unsigned short isec;
      long lGeneration;
    } JET_LGPOS;
```

### <a name="members"></a>Member

**Ib**

Unterstützt die ESE-Infrastruktur und kann nicht in Ihrem Code verwendet werden.

**isec**

Unterstützt die ESE-Infrastruktur und kann nicht in Ihrem Code verwendet werden.

**lGeneration**

Unterstützt die ESE-Infrastruktur und kann nicht in Ihrem Code verwendet werden.

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

[JET_BKINFO](./jet-bkinfo-structure.md)  
[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)
