---
description: 'Weitere Informationen finden Sie unter: JET_LGPOS Struktur'
title: JET_LGPOS Struktur
TOCTitle: JET_LGPOS Structure
ms:assetid: dbce1a60-b32b-40c1-a215-e93bb77cd8c1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294113(v=EXCHG.10)
ms:contentKeyID: 32765727
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
ms.openlocfilehash: e3e83786236a95cf2b0c4d77e26e6987334a5b00
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122986153"
---
# <a name="jet_lgpos-structure"></a>JET_LGPOS Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_lgpos-structure"></a>JET_LGPOS Struktur

Die **JET_LGPOS-Struktur** enthält Daten, die für den Protokollierungsmechanismus der Datenbank-Engine intern sind. Diese Struktur wird als intern betrachtet.

```cpp
    typedef struct {
      unsigned short ib;
      unsigned short isec;
      long lGeneration;
    } JET_LGPOS;
```

### <a name="members"></a>Member

**Ib**

Unterstützt die ESE-Infrastruktur und kann nicht in Ihrem Code verwendet werden.

**isec**

Unterstützt die ESE-Infrastruktur und kann nicht in Ihrem Code verwendet werden.

**lGeneration**

Unterstützt die ESE-Infrastruktur und kann nicht in Ihrem Code verwendet werden.

### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | 



### <a name="see-also"></a>Weitere Informationen

[JET_BKINFO](./jet-bkinfo-structure.md)  
[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)
