---
description: 'Weitere Informationen zu: JET_BKINFO-Struktur'
title: JET_BKINFO-Struktur
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
ms.openlocfilehash: 477c84ee0b466fb43ee0bb06ef14a2a1be6dd00e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472186"
---
# <a name="jet_bkinfo-structure"></a>JET_BKINFO-Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_bkinfo-structure"></a>JET_BKINFO-Struktur

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

Der Zeitpunkt dieses Sicherungsereignisses.

**bklogtimeMark**

Der Zeitpunkt dieses Sicherungsereignisses mit zusätzlichen Bits, um eine Momentaufnahmesicherung anzugeben.

**Windows Vista: bklogtimeMark** wird in Windows Vista eingeführt.

**genLow**

Die niedrige Protokollgenerierungsnummer, die diesem Sicherungsereignis zugeordnet ist.

**genHigh**

Die hohe Protokollgenerierungsnummer, die diesem Sicherungsereignis zugeordnet ist.

### <a name="remarks"></a>Hinweise

Diese Struktur wird innerhalb der [JET_DBINFOMISC](./jet-dbinfomisc-structure.md) Struktur verwendet, um Daten über das Datenbanksicherungsereignis darzustellen.

### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | 



### <a name="see-also"></a>Weitere Informationen

[JET_LGPOS](./jet-lgpos-structure.md)  
[JET_LOGTIME](./jet-logtime-structure.md)  
[JET_BKLOGTIME](./jet-bklogtime-structure.md)  
[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)
