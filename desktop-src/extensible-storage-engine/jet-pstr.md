---
description: 'Weitere Informationen finden Sie hier: JET_PSTR'
title: JET_PSTR
TOCTitle: JET_PSTR
ms:assetid: acb1143f-a5ee-4088-9f05-cc2aeef23442
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294056(v=EXCHG.10)
ms:contentKeyID: 32765667
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
ms.openlocfilehash: 6bbed2cad9f9c7816d010a429b1db8eb5306fc1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353922"
---
# <a name="jet_pstr"></a>JET_PSTR


_**Gilt für:** Windows | Windows Server_

## <a name="jet_pstr"></a>JET_PSTR

Der JET_PSTR-Datentyp enthält eine NULL-terminierte ASCII-Zeichenfolge (Char \* ).

**Windows Vista: JET_PSTR** wird in Windows Vista eingeführt.

```cpp
    typedef __nullterminated char *  JET_PSTR;
```

### <a name="data-types"></a>Datentypen

JET_PSTR

Mit NULL endend, ASCII-Zeichenfolge (Char \* ).

### <a name="requirements"></a>Anforderungen

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Erfordert Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Erfordert Windows Server 2008.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>In "ESENT. h" deklariert.</p></td>
</tr>
</tbody>
</table>

