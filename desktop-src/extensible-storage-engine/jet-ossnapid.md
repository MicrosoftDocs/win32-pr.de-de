---
description: 'Weitere Informationen finden Sie unter: JET_OSSNAPID'
title: JET_OSSNAPID
TOCTitle: JET_OSSNAPID
ms:assetid: 89b15492-674a-46e4-8aea-991df4f22a6f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269325(v=EXCHG.10)
ms:contentKeyID: 32765615
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
ms.openlocfilehash: 2dac261072ac9a5ce5a845ff046628cf348cd5815c34e16fccb575c2c0da3095
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118765076"
---
# <a name="jet_ossnapid"></a>JET_OSSNAPID


_**Gilt für:** Windows | Windows Server_

## <a name="jet_ossnapid"></a>JET_OSSNAPID

Der **JET_OSSNAPID** datentyp enthält ein Handle für eine Momentaufnahme der Datenbank.

```cpp
    typedef JET_API_PTR JET_OSSNAPID;
```

### <a name="data-types"></a>Datentypen

JET_OSSNAPID

Ein Handle für eine Momentaufnahme der Datenbank. Dieses Handle wird in JET-API-Elementen verwendet, die an der Momentaufnahmesicherung beteiligt sind.

**NULL** kann verwendet werden, um ein ungültiges Handle anzugeben.

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
<td><p>In Esent.h deklariert.</p></td>
</tr>
</tbody>
</table>

