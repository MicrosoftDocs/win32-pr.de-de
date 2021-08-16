---
description: 'Weitere Informationen finden Sie unter: JET_BKINFO Struktur'
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
ms.openlocfilehash: 9f391d711c6d10c50cfdb26314be6ee709ff481bda0ce370faa28d514422444c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118487865"
---
# <a name="jet_bkinfo-structure"></a>JET_BKINFO Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_bkinfo-structure"></a>JET_BKINFO Struktur

Die **JET_BKINFO-Struktur** enthält eine Sammlung von Daten zu einem bestimmten Sicherungsereignis.

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

**lgposMark**

Die ID dieser Sicherung.

**logtimeMark**

Der Zeitpunkt dieses Sicherungsereignis.

**bklogtimeMark**

Der Zeitpunkt dieses Sicherungsereignis mit zusätzlichen Bits, um eine Momentaufnahmesicherung anzugeben.

**Windows Vista: bklogtimeMark** wird in Windows Vista eingeführt.

**genLow**

Die niedrige Protokollgenerierungsnummer, die diesem Sicherungsereignis zugeordnet ist.

**genHigh**

Die hohe Protokollgenerierungsnummer, die diesem Sicherungsereignis zugeordnet ist.

### <a name="remarks"></a>Hinweise

Diese Struktur wird innerhalb der JET_DBINFOMISC [verwendet,](./jet-dbinfomisc-structure.md) um Daten zum Datenbanksicherungsereignis zu darstellen.

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
<td><p>Wird in Esent.h deklariert.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Weitere Informationen

[JET_LGPOS](./jet-lgpos-structure.md)  
[JET_LOGTIME](./jet-logtime-structure.md)  
[JET_BKLOGTIME](./jet-bklogtime-structure.md)  
[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)
