---
description: 'Weitere Informationen finden Sie unter: JET_BKLOGTIME Struktur'
title: JET_BKLOGTIME Struktur
TOCTitle: JET_BKLOGTIME Structure
ms:assetid: 31460079-7c5b-4145-837d-b112ba0117d6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269219(v=EXCHG.10)
ms:contentKeyID: 32765522
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
ms.openlocfilehash: b34740d582e341cce3b2fd0b28203b7346a4de1d94a8586289be8ab252247943
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118487722"
---
# <a name="jet_bklogtime-structure"></a>JET_BKLOGTIME Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_bklogtime-structure"></a>JET_BKLOGTIME Struktur

Die **JET_BKLOGTIME-Struktur** enthält die Datums- und Uhrzeitelemente eines Ereignisses. Es ist eine Erweiterung von [JET_LOGTIME.](./jet-logtime-structure.md)

**Windows Vista: JET_BKLOGTIME** wird in Windows Vista eingeführt.

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
      union {
        char bFiller2;
        struct {
          unsigned char fOSSnapshot  :1;
          unsigned char fReserved  :7;
        };
      };
    } JET_BKLOGTIME;
```

### <a name="members"></a>Member

**bSeconds**

Die Zeit des Ereignisses in Sekunden. Dies kann 0 (null) bis 60 sein. 0 (null) wird verwendet, wenn die **JET_BKLOGTIME** "NULL" ist.

**bMinutes**

Die Zeit des Ereignisses in Minuten. Dies kann 0 (null) bis 60 sein. 0 (null) wird verwendet, wenn die **JET_BKLOGTIME** "NULL" ist.

**bHours**

Die Zeit des Ereignisses in Stunden. Dies kann 0 (null) bis 24 sein. 0 (null) wird verwendet, wenn die **JET_BKLOGTIME** "NULL" ist.

**Bday**

Der Tag des Monats des Ereignisses. Dies kann 0 (null) bis 31 sein. 0 (null) wird verwendet, wenn die **JET_BKLOGTIME** "NULL" ist.

**bMonth**

Der Monat des Jahres des Ereignisses. Dies kann 0 (null) bis 12 sein. 0 (null) wird verwendet, wenn die **JET_BKLOGTIME** "NULL" ist.

**bYear**

Das Jahr (Offset um 1900) des Ereignisses. Um das tatsächliche Jahr zu erreichen, fügen Sie diesem Wert 1900 hinzu. 0 (null) wird verwendet, wenn die **JET_BKLOGTIME** "NULL" ist.

**bFiller1**

Dieses Feld sollte ignoriert werden.

**fTimeIsUTC**

Die Zeit liegt im UTC-Format vor.

**fUnused**

Dieses Feld sollte ignoriert werden.

**bFiller2**

Dieses Feld sollte ignoriert werden.

**fOSSnapshot**

Wenn es sich bei diesem Ereignis um eine Sicherung handelt, enthält dieses Flag einen der folgenden möglichen Werte:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Name</p></th>
<th><p>Wert</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Streamingsicherung</p></td>
<td><p>0 (Null)</p></td>
</tr>
<tr class="even">
<td><p>Momentaufnahmesicherung</p></td>
<td><p>1</p></td>
</tr>
</tbody>
</table>


**fReserved**

Dieses Feld sollte ignoriert werden.

### <a name="remarks"></a>Hinweise

Diese Struktur wird beim Debuggen verwendet.

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


### <a name="see-also"></a>Weitere Informationen

[JET_LOGTIME](./jet-logtime-structure.md)  
[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)
