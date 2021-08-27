---
description: 'Weitere Informationen finden Sie unter: JET_LOGTIME Struktur'
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
ms.openlocfilehash: 9cb6fac65451518e20dd64ee223638165ac5c752
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470475"
---
# <a name="jet_logtime-structure"></a>JET_LOGTIME Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_logtime-structure"></a>JET_LOGTIME Struktur

Die **JET_LOGTIME-Struktur** enthält Elemente des Datums und der Uhrzeit eines Ereignisses.

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

**bSeconds**

Die Zeit des Ereignisses in Sekunden. Dieser Wert kann 0 bis 59 sein. 0 wird verwendet, wenn die -Struktur NULL ist.

**bMinutes**

Die Zeit des Ereignisses in Minuten. Dieser Wert kann 0 bis 59 sein. 0 wird verwendet, wenn die -Struktur NULL ist.

**bHours**

Die Zeit des Ereignisses in Stunden. Dieser Wert kann 0 bis 23 sein. 0 wird verwendet, wenn die -Struktur NULL ist.

**Bday**

Der Tag des Monats des Ereignisses. Dieser Wert kann 0 bis 31 sein. 0 wird verwendet, wenn die -Struktur NULL ist.

**bMonth**

Der Monat des Jahres des Ereignisses. Dieser Wert kann 0 bis 12 sein. 0 wird verwendet, wenn die -Struktur NULL ist.

**bYear**

Das Jahr des Ereignisses (Offset um 1900). Um das tatsächliche Jahr zu erreichen, fügen Sie diesem Wert 1900 hinzu. 0 wird verwendet, wenn die -Struktur NULL ist.

**bFiller1**

Dieses Feld sollte ignoriert werden.

**fTimeIsUTC**

Die Zeit liegt im UTC-Format vor.

**fUnused**

Dieses Feld sollte ignoriert werden.

**bFiller2**

Dieses Feld sollte ignoriert werden.

### <a name="remarks"></a>Hinweise

Diese Struktur ist in erster Linie für die Verwendung beim Debuggen gedacht.

### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | 



### <a name="see-also"></a>Weitere Informationen

[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)
