---
description: 'Weitere Informationen zu: JET_BKLOGTIME-Struktur'
title: JET_BKLOGTIME-Struktur
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
ms.openlocfilehash: 2d6f8e3f77d905eb601441ad8ab3ca88bb08f59d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478526"
---
# <a name="jet_bklogtime-structure"></a>JET_BKLOGTIME-Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_bklogtime-structure"></a>JET_BKLOGTIME-Struktur

Die **JET_BKLOGTIME-Struktur** enthält die Datums- und Uhrzeitelemente eines Ereignisses. Es handelt sich um eine Erweiterung von [JET_LOGTIME](./jet-logtime-structure.md).

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

Die Zeit des Ereignisses in Sekunden. Dies kann 0 (null) bis 60 sein. 0 (null) wird verwendet, wenn die **JET_BKLOGTIME** -Struktur "NULL" ist.

**bMinutes**

Die Zeit des Ereignisses in Minuten. Dies kann 0 (null) bis 60 sein. 0 (null) wird verwendet, wenn die **JET_BKLOGTIME** -Struktur "NULL" ist.

**bHours**

Die Uhrzeit des Ereignisses in Stunden. Dies kann 0 (null) bis 24 sein. 0 (null) wird verwendet, wenn die **JET_BKLOGTIME** -Struktur "NULL" ist.

**Bday**

Der Tag des Monats des Ereignisses. Dies kann 0 (null) bis 31 sein. 0 (null) wird verwendet, wenn die **JET_BKLOGTIME** -Struktur "NULL" ist.

**bMonth**

Der Monat des Jahres des Ereignisses. Dies kann 0 (null) bis 12 sein. 0 (null) wird verwendet, wenn die **JET_BKLOGTIME** -Struktur "NULL" ist.

**bYear**

Das Jahr (Offset um 1900) des Ereignisses. Um das tatsächliche Jahr zu erreichen, fügen Sie diesem Wert 1900 hinzu. 0 (null) wird verwendet, wenn die **JET_BKLOGTIME** -Struktur "NULL" ist.

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


| <p>Name</p> | <p>Wert</p> | 
|-------------|--------------|
| <p>Streamingsicherung</p> | <p>0 (Null)</p> | 
| <p>Momentaufnahmesicherung</p> | <p>1</p> | 



**fReserved**

Dieses Feld sollte ignoriert werden.

### <a name="remarks"></a>Hinweise

Diese Struktur wird beim Debuggen verwendet.

### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008.</p> | | <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | 



### <a name="see-also"></a>Weitere Informationen

[JET_LOGTIME](./jet-logtime-structure.md)  
[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)
