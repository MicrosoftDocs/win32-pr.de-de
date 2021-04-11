---
description: 'Weitere Informationen finden Sie hier: JET_BKINFO Struktur'
title: JET_BKINFO Struktur
TOCTitle: JET_BKINFO Structure
ms:assetid: dfaf1d72-1d5f-4777-91c1-6affb735b092
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294120(v=EXCHG.10)
ms:contentKeyID: 32765734
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
ms.openlocfilehash: 6c4849c23e742657d8f5eaba8a030426f7a2a440
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217870"
---
# <a name="jet_bkinfo-structure"></a>JET_BKINFO Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_bkinfo-structure"></a>JET_BKINFO Struktur

Die **JET_BKINFO** -Struktur enthält eine Sammlung von Daten zu einem bestimmten Sicherungs Ereignis.

```cpp
    typedef struct {
      JET_LGPOS lgposMark;
      union {
        JET_LOGTIME logtimeMark;
        JET_BKLOGTIME bklogtimeMark;
      };
      unsigned long genLow;
      unsigned long genHigh;
    } JET_BKINFO;
```

### <a name="members"></a>Member

**lgposmark**

Die ID dieser Sicherung.

**logtimemark**

Der Zeitpunkt dieses Sicherungs Ereignisses.

**bklogtimemark**

Die Zeit dieses Sicherungs Ereignisses mit zusätzlichen Bits, die auf eine Momentaufnahme Sicherung hindeuten.

**Windows Vista: bklogtimemark** wird in Windows Vista eingeführt.

**genlow**

Die niedrige Protokoll Generierungs Nummer, die diesem Sicherungs Ereignis zugeordnet ist.

**genhoch**

Die hohe Protokoll Generierungs Nummer, die diesem Sicherungs Ereignis zugeordnet ist.

### <a name="remarks"></a>Bemerkungen

Diese Struktur wird in der [JET_DBINFOMISC](./jet-dbinfomisc-structure.md) -Struktur verwendet, um Daten zum Daten Bank Sicherungs Ereignis darzustellen.

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

[JET_LGPOS](./jet-lgpos-structure.md)  
[JET_LOGTIME](./jet-logtime-structure.md)  
[JET_BKLOGTIME](./jet-bklogtime-structure.md)  
[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)
