---
description: 'Weitere Informationen finden Sie hier: JET_COLUMNID'
title: JET_COLUMNID
TOCTitle: JET_COLUMNID
ms:assetid: d6c74c5c-ba61-4e1c-a1b1-495e925b6b68
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294104(v=EXCHG.10)
ms:contentKeyID: 32765719
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
ms.openlocfilehash: be5b8bb64dc9e0fc42055cf5e4d4f67caa7654bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861963"
---
# <a name="jet_columnid"></a>JET_COLUMNID


_**Gilt für:** Windows | Windows Server_

## <a name="jet_columnid"></a>JET_COLUMNID

Der **JET_COLUMNID** -Datentyp identifiziert eine Spalte in einer Tabelle.

```cpp
    typedef unsigned long JET_COLUMNID;
```

### <a name="data-types"></a>Datentypen

JET_COLUMNID

Identifiziert eine Spalte in einer Tabelle.

### <a name="remarks"></a>Bemerkungen

Spalten-IDs sind innerhalb einer einzelnen Tabelle eindeutig. Wenn eine Spalte bekanntermaßen über eine bestimmte Spalten-ID verfügt, weist Sie immer diese Spalten-ID auf. Durch die Wiederherstellung aus einer Sicherung wird der Wert einer Spalten-ID nicht geändert. Wenn jedoch eine oder mehrere Tabellen Spalten, vor einer bestimmten Tabellenspalte, gelöscht werden, kann eine Compact-Datenbank den Wert einer Spalten-ID ändern.

In einigen Fällen sind Spalten-IDs die einzige Möglichkeit zum Identifizieren von Spalten. Wenn eine temporäre Tabelle erstellt wird, haben die Spalten keine Namen, aber ein Array von Spalten-IDs wird von der Create-Funktion zurückgegeben.

Spalten in verschiedenen Tabellen können dieselbe Spalten-ID aufweisen.

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

