---
description: Flag, das angibt, ob ein Decommit-Vorgang ausgeführt wird.
ms.assetid: aa008be1-8faa-4dc1-9641-37dcc59ce6c7
title: CBaseAllocator::m_bDecommitInProgress-Member (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bDecommitInProgress
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d6d73514ffbe2b6e2430230e64ccfa9006809523a95cd3220ca078d4c4e40f41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017538"
---
# <a name="cbaseallocatorm_bdecommitinprogress-member"></a>CBaseAllocator::m \_ bDecommitInProgress-Member

Flag, das angibt, ob ein Decommit-Vorgang ausgeführt wird. Der Wert ist **TRUE,** nachdem die [**CBaseAllocator::D ecommit-Methode**](cbaseallocator-decommit.md) aufgerufen wurde, aber bevor alle Puffer freigegeben wurden. Wenn der Wert **TRUE** ist, schlägt die [**CBaseAllocator::GetBuffer-Methode**](cbaseallocator-getbuffer.md) fehl. Außerdem sollte die Zuweisung nicht selbst gelöscht werden, während der Wert **TRUE** ist.

## <a name="syntax"></a>Syntax


```C++
BOOL m_bDecommitInProgress;
```



## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseAllocator-Klasse**](cbaseallocator.md)
</dt> </dl>

 

 




