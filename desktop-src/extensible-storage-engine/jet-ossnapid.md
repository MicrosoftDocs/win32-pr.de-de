---
description: 'Weitere Informationen finden Sie hier: JET_OSSNAPID'
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
ms.openlocfilehash: b0ca1bb5e2e5a80c9166574708efc7875ed95446
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352250"
---
# <a name="jet_ossnapid"></a>JET_OSSNAPID


_**Gilt für:** Windows | Windows Server_

## <a name="jet_ossnapid"></a>JET_OSSNAPID

Der **JET_OSSNAPID** -Datentyp enthält ein Handle für eine Momentaufnahme der Datenbank.

```cpp
    typedef JET_API_PTR JET_OSSNAPID;
```

### <a name="data-types"></a>Datentypen

JET_OSSNAPID

Ein Handle für eine Momentaufnahme der Datenbank. Dieses Handle wird in Jet-API-Elementen verwendet, die bei der Momentaufnahme Sicherung beteiligt sind.

**Null** kann verwendet werden, um ein ungültiges Handle anzugeben.

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

