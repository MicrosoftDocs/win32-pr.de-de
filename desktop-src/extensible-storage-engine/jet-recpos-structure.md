---
description: 'Weitere Informationen finden Sie hier: JET_RECPOS Struktur'
title: JET_RECPOS Struktur
TOCTitle: JET_RECPOS Structure
ms:assetid: 7c335120-4b84-4095-8f13-e5315d4996b1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269308(v=EXCHG.10)
ms:contentKeyID: 32765598
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
ms.openlocfilehash: e24e16aaac4228f35350f55f57a14f2820add0cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364081"
---
# <a name="jet_recpos-structure"></a>JET_RECPOS Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_recpos-structure"></a>JET_RECPOS Struktur

Die **JET_RECPOS** -Struktur enthält eine Auflistung von ganzen Zahlen, die eine Bruch Position innerhalb eines Indexes darstellen. **centrieslt** ist die Anzahl der Indexeinträge, die kleiner sind als der aktuelle Index Schlüssel. **centriesinrange** ist die Anzahl der Indexeinträge, die dem aktuellen Schlüssel entsprechen. **centriesinrange** wird nicht unterstützt und wird immer als 1 zurückgegeben. " **zentriestotal** " ist die Anzahl der Indexeinträge im Index. Alle Werte sind Näherungen, ohne die Genauigkeit zu gewährleisten.

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long centriesLT;
      unsigned long centriesInRange;
      unsigned long centriesTotal;
    } JET_RECPOS;
```

### <a name="members"></a>Member

**cbStruct**

Die Größe der [JET_RETINFO](./jet-retinfo-structure.md) Struktur in Bytes. Dieser Wert bestätigt, dass die folgenden Felder vorhanden sind.

**centrieslt**

Die ungefähre Anzahl der Indexeinträge, die kleiner als der aktuelle Schlüssel sind.

**centriesinrange**

Die ungefähre Anzahl der Indexeinträge, die dem aktuellen Schlüssel entsprechen. Dieses Feld wird immer auf 1 festgelegt, unabhängig von der Anzahl der Indexeinträge, die tatsächlich dem aktuellen Schlüssel entsprechen.

**zentriestotal**

Die ungefähre Anzahl von Einträgen im Index.

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

[JET_RETINFO](./jet-retinfo-structure.md)  
[Jetgetrecordposition](./jetgetrecordposition-function.md)
