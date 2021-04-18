---
description: 'Weitere Informationen finden Sie hier: JET_BKLOGTIME Struktur'
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
ms.openlocfilehash: 0b3ebfd1c0b807a491695ba18d6735e0230a16fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350834"
---
# <a name="jet_bklogtime-structure"></a>JET_BKLOGTIME Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_bklogtime-structure"></a>JET_BKLOGTIME Struktur

Die **JET_BKLOGTIME** -Struktur enthält die Datums-und Uhrzeit Elemente eines Ereignisses. Es handelt sich um eine Erweiterung von [JET_LOGTIME](./jet-logtime-structure.md).

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

**bseconds**

Die Uhrzeit des Ereignisses in Sekunden. Dies kann 0 (null) bis 60 sein. 0 (null) wird verwendet, wenn die **JET_BKLOGTIME** Struktur "Null" ist.

**bminuten**

Die Uhrzeit des Ereignisses (in Minuten). Dies kann 0 (null) bis 60 sein. 0 (null) wird verwendet, wenn die **JET_BKLOGTIME** Struktur "Null" ist.

**bhours**

Die Uhrzeit des Ereignisses (in Stunden). Dies kann 0 (null) bis 24 sein. 0 (null) wird verwendet, wenn die **JET_BKLOGTIME** Struktur "Null" ist.

**bday**

Der Tag des Monats des Ereignisses. Dies kann 0 (null) bis 31 sein. 0 (null) wird verwendet, wenn die **JET_BKLOGTIME** Struktur "Null" ist.

**bmonth**

Der Monat des Jahres des Ereignisses. Der Wert kann zwischen 0 (null) und 12 liegen. 0 (null) wird verwendet, wenn die **JET_BKLOGTIME** Struktur "Null" ist.

**byear**

Das Jahr (Offset um 1900) des Ereignisses. Um das tatsächliche Jahr zu erreichen, fügen Sie diesem Wert 1900 hinzu. 0 (null) wird verwendet, wenn die **JET_BKLOGTIME** Struktur "Null" ist.

**bFiller1**

Dieses Feld sollte ignoriert werden.

**"f"**

Die Uhrzeit liegt im UTC-Format vor.

**funused**

Dieses Feld sollte ignoriert werden.

**bFiller2**

Dieses Feld sollte ignoriert werden.

**fossnapshot**

Wenn dieses Ereignis eine Sicherung ist, enthält dieses Flag einen der folgenden möglichen Werte:

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
<td><p>0 (null)</p></td>
</tr>
<tr class="even">
<td><p>Momentaufnahme Sicherung</p></td>
<td><p>1</p></td>
</tr>
</tbody>
</table>


**frei bedient**

Dieses Feld sollte ignoriert werden.

### <a name="remarks"></a>Bemerkungen

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
<td><p>In "ESENT. h" deklariert.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Weitere Informationen

[JET_LOGTIME](./jet-logtime-structure.md)  
[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)
