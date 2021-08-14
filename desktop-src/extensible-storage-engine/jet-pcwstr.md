---
description: 'Weitere Informationen finden Sie unter: JET_PCWSTR'
title: JET_PCWSTR
TOCTitle: JET_PCWSTR
ms:assetid: fef64bb9-c2e0-4cfb-8138-c98ae6f50952
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294145(v=EXCHG.10)
ms:contentKeyID: 32765759
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
ms.openlocfilehash: 3958baa23228bdf32807cc4fdc07a471e625d553f57672e318a062038923b5af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119473890"
---
# <a name="jet_pcwstr"></a>JET_PCWSTR


_**Gilt für:** Windows | Windows Server_

## <a name="jet_pcwstr"></a>JET_PCWSTR

Der **JET_PCWSTR** Datentyp enthält eine mit NULL beendete, konstante **Unicode-Zeichenfolge** (char). \*

**Windows Vista: JET_PCWSTR** wird in Windows Vista eingeführt.

```cpp
    typedef __nullterminated const WCHAR * JET_PCWSTR;
```

### <a name="data-types"></a>Datentypen

JET_PCWSTR

Mit NULL beendete, konstante Unicode-Zeichenfolge (char \* ).

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
<td><p>In Esent.h deklariert.</p></td>
</tr>
</tbody>
</table>

