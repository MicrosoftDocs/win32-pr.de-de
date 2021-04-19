---
description: 'Weitere Informationen finden Sie hier: JET_ERR'
title: JET_ERR
TOCTitle: JET_ERR
ms:assetid: cd9cb876-251c-458d-a015-8e9045e77fc9
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294092(v=EXCHG.10)
ms:contentKeyID: 32765707
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 35120be9a26dcbdc8d012cd12c871ddcf8f71555
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "106363193"
---
# <a name="jet_err"></a>JET_ERR


_**Gilt für:** Windows | Windows Server_

## <a name="jet_err"></a>JET_ERR

Der **JET_ERR** -Datentyp enthält einen [Fehlercode für die erweiterbare Speicher-Engine](./extensible-storage-engine-error-codes.md).

```cpp
typedef long JET_ERR;
```

### <a name="data-types"></a>Datentypen

JET_ERR

Ein NULL-Wert (entspricht JET_errSuccess) gibt an, dass der-Befehl erfolgreich ausgeführt wurde. Ein positiver Wert warnt vor einer nicht schwerwiegenden Bedingung, die während eines anderweitig erfolgreichen Aufrufes aufgetreten ist. Ein negativer Wert gibt an, dass der-Befehl fehlgeschlagen ist.

### <a name="remarks"></a>Bemerkungen

Informationen zum Zurückgeben von Fehlern als HRESULTs finden Sie unter [Fehler des Extensible Storage Engine](./extensible-storage-engine-errors.md). Informationen zu Flags zum Konfigurieren der Datenbank für die Fehlerbehandlung finden Sie unter Parameter für die [Fehlerbehandlung](./error-handling-parameters.md).

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

[Erweiterbare Speicher-Engine-Fehler](./extensible-storage-engine-errors.md)  
[Fehler Codes für erweiterbare Speicher-Engine](./extensible-storage-engine-error-codes.md)  
[Fehler Behandlungsparameter](./error-handling-parameters.md)
