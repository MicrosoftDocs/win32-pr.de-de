---
description: 'Weitere Informationen finden Sie hier: JET_LS'
title: JET_LS
TOCTitle: JET_LS
ms:assetid: 8e4e7902-84b1-404b-8654-bb430a0952aa
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269336(v=EXCHG.10)
ms:contentKeyID: 32765625
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
ms.openlocfilehash: 3300fd88c0dd1e1fca55722bf58350e28f3c3b08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364082"
---
# <a name="jet_ls"></a>JET_LS


_**Gilt für:** Windows | Windows Server_

## <a name="jet_ls"></a>JET_LS

Der **JET_LS** -Datentyp enthält ein Kontext Handle für den lokalen Speicher (LS). Dieses Handle kann einem Cursor oder einer Tabelle zugeordnet werden und verweist möglicherweise auf dynamisch zugeordnete Ressourcen.

**Windows XP: JET_LS** wird in Windows XP eingeführt.

```cpp
    typedef JET_API_PTR JET_LS;
```

### <a name="data-types"></a>Datentypen

JET_LS

Der Wert JET_LSNil gibt ein ungültiges Kontext Handle an.

### <a name="remarks"></a>Bemerkungen

Ein Kontext Handle ist anfänglich mit dem **JET_LS** -Datentyp verknüpft, wobei [jetsetls](./jetsetls-function.md)verwendet wird. Das Kontext Handle kann mithilfe von [jetgetls](./jetgetls-function.md)aus dem **JET_LS** -Datentyp abgerufen werden.

Das Kontext Handle kann explizit vom **JET_LS** -Datentyp mithilfe von [jetgetls](./jetgetls-function.md) mit JET_bitLSReset getrennt werden. Alternativ kann das Kontext Handle implizit vom **JET_LS** Datentyp getrennt werden, wenn das zugrunde liegende Objekt von der Datenbank-Engine als Ergebnis einer direkten oder indirekten Aktion durch die Anwendung freigegeben wird. Im impliziten Fall wird ein Lauf Zeit Rückruf für die Anwendung ausgegeben, sodass er das Kontext Handle bereinigen kann. Weitere Informationen zum impliziten Aufheben der Zuordnung des Datentyps **JET_LS** finden Sie unter [jetsetls](./jetsetls-function.md).

Die folgenden Flags sind dem JET_LS-Datentyp zugeordnet.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Begriff</p></th>
<th><p>BESCHREIBUNG</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitLSReset</p></td>
<td><p>Der Kontext Handle wird vom-Objekt getrennt.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitLSCursor</p></td>
<td><p>Legen Sie den einem Tabellen Cursor zugeordneten lokalen Speicher fest, oder rufen Sie ihn ab.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitLSTable</p></td>
<td><p>Festlegen oder Abrufen des lokalen Speichers, der einer Tabelle zugeordnet ist.</p></td>
</tr>
<tr class="even">
<td><p>JET_LSNil</p></td>
<td><p>Das Kontext Handle ist ungültig.</p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a>Anforderungen

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Erfordert Windows Vista oder Windows XP.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Erfordert Windows Server 2008 oder Windows Server 2003.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>In "ESENT. h" deklariert.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Weitere Informationen

[Jetsetls](./jetsetls-function.md)  
[Jetgetls](./jetgetls-function.md)
