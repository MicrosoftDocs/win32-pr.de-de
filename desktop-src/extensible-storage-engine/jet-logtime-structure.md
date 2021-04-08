---
description: 'Weitere Informationen finden Sie hier: JET_LOGTIME Struktur'
title: JET_LOGTIME Struktur
TOCTitle: JET_LOGTIME Structure
ms:assetid: cb7c0b74-db7a-4e48-80b8-37b3fdf6d088
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294089(v=EXCHG.10)
ms:contentKeyID: 32765704
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
ms.openlocfilehash: 9c99e2c1f77a01c33a75d3e5d16c4fe58c122a4e
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "103762426"
---
# <a name="jet_logtime-structure"></a>JET_LOGTIME Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_logtime-structure"></a>JET_LOGTIME Struktur

Die **JET_LOGTIME** -Struktur enthält Elemente des Datums und der Uhrzeit eines Ereignisses.

```cpp
typedef struct {
  char bSeconds;
  char bMinutes;
  char bHours;
  char bDay;
  char bMonth;
  char bYear;
  union {
    char bFiller1;
    struct {
        unsigned char fTimeIsUTC: 1;
        unsigned char fUnused: 7;
    };
  };
  char bFiller2;
} JET_LOGTIME;
```

### <a name="members"></a>Member

**bseconds**

Die Uhrzeit des Ereignisses in Sekunden. Dieser Wert kann zwischen 0 und 59 liegen. 0 wird verwendet, wenn die-Struktur NULL ist.

**bminuten**

Die Uhrzeit des Ereignisses (in Minuten). Dieser Wert kann zwischen 0 und 59 liegen. 0 wird verwendet, wenn die-Struktur NULL ist.

**bhours**

Die Uhrzeit des Ereignisses (in Stunden). Dieser Wert kann zwischen 0 und 23 liegen. 0 wird verwendet, wenn die-Struktur NULL ist.

**bday**

Der Tag des Monats des Ereignisses. Dieser Wert kann zwischen 0 und 31 liegen. 0 wird verwendet, wenn die-Struktur NULL ist.

**bmonth**

Der Monat des Jahres des Ereignisses. Dieser Wert kann zwischen 0 und 12 liegen. 0 wird verwendet, wenn die-Struktur NULL ist.

**byear**

Das Jahr des Ereignisses (Offset um 1900). Um das tatsächliche Jahr zu erreichen, fügen Sie diesem Wert 1900 hinzu. 0 wird verwendet, wenn die-Struktur NULL ist.

**bFiller1**

Dieses Feld sollte ignoriert werden.

**"f"**

Die Uhrzeit liegt im UTC-Format vor.

**funused**

Dieses Feld sollte ignoriert werden.

**bFiller2**

Dieses Feld sollte ignoriert werden.

### <a name="remarks"></a>Bemerkungen

Diese Struktur ist hauptsächlich für die Verwendung beim Debuggen vorgesehen.

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

[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)
