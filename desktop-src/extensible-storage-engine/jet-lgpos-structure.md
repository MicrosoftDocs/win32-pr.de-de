---
description: 'Weitere Informationen finden Sie hier: JET_LGPOS Struktur'
title: JET_LGPOS Struktur
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
ms.openlocfilehash: 25f00c73a4bb922a8152335babe222b539c70ade
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042665"
---
# <a name="jet_lgpos-structure"></a>JET_LGPOS Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_lgpos-structure"></a>JET_LGPOS Struktur

Die **JET_LGPOS** -Struktur enthält Daten, die für den Protokollierungs Mechanismus der Datenbank-Engine intern sind. Diese Struktur wird als intern betrachtet.

```cpp
    typedef struct {
      unsigned short ib;
      unsigned short isec;
      long lGeneration;
    } JET_LGPOS;
```

### <a name="members"></a>Member

**besiegt**

Unterstützt die ESE-Infrastruktur und kann nicht in Ihrem Code verwendet werden.

**ISEC**

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
<td><p>In "ESENT. h" deklariert.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Weitere Informationen

[JET_BKINFO](./jet-bkinfo-structure.md)  
[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)
