---
description: 'Weitere Informationen finden Sie unter: JET_OSSNAPID'
title: JET_OSSNAPID
TOCTitle: JET_OSSNAPID
ms:assetid: 89b15492-674a-46e4-8aea-991df4f22a6f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269325(v=EXCHG.10)
ms:contentKeyID: 32765615
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
ms.openlocfilehash: d6185f17c16cbdb2a45e172a14af346c3519aa12
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468367"
---
# <a name="jet_ossnapid"></a>JET_OSSNAPID


_**Gilt für:** Windows | Windows Server_

## <a name="jet_ossnapid"></a>JET_OSSNAPID

Der **JET_OSSNAPID-Datentyp** enthält ein Handle für eine Momentaufnahme der Datenbank.

```cpp
    typedef JET_API_PTR JET_OSSNAPID;
```

### <a name="data-types"></a>Datentypen

JET_OSSNAPID

Ein Handle für eine Momentaufnahme der Datenbank. Dieses Handle wird in JET-API-Elementen verwendet, die an der Momentaufnahmesicherung beteiligt sind.

**NULL** kann verwendet werden, um ein ungültiges Handle anzugeben.

### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | 


