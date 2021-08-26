---
description: Der Bezeichner des Indexes, auf den in einer Datenbank zugegriffen werden soll.
ms.assetid: 559e73bf-91c2-4dbf-a667-e5c0431aaffa
title: INDEXID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5711f2927462325b2a6479dd9506099da4bd50f9a9a99b68152e5c0030a47d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001890"
---
# <a name="indexid"></a>INDEXID

Der Bezeichner des Indexes, auf den in einer Datenbank zugegriffen werden soll.


```C++
typedef DWORD INDEXID;
```



## <a name="remarks"></a>Hinweise

Eine **INDEXID** kann ein ganzzahliger Wert sein, der den Index darstellt, oder der folgende Wert:

<dl> <dt>

<span id="INDEXID_NULL___INDEXID_-1_"></span><span id="indexid_null___indexid_-1_"></span>INDEXID \_ NULL ((INDEXID)-1)
</dt> <dd>

Eine ungültige **INDEXID.**

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**SdbDeclareIndex**](sdbdeclareindex.md)
</dt> <dt>

[**SdbStartIndexing**](sdbstartindexing.md)
</dt> <dt>

[**SdbStopIndexing**](sdbstopindexing.md)
</dt> </dl>

 

 




