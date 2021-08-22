---
description: Die NotifySample-Methode gibt alle Threads frei, die auf Beispiele warten.
ms.assetid: b09c48a0-9cd5-44a7-9267-d2a11e8cde4c
title: CBaseAllocator.NotifySample-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.NotifySample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b1b73a54ae9b5ccabacfbb1153c5d0d91f951e83082a1bdd3c7f7551ad813804
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017478"
---
# <a name="cbaseallocatornotifysample-method"></a>CBaseAllocator.NotifySample-Methode

Die `NotifySample` -Methode gibt alle Threads frei, die auf Beispiele warten.

## <a name="syntax"></a>Syntax


```C++
void NotifySample();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Wenn Threads auf Beispiele warten, ist der Wert von [**CBaseAllocator::m \_ lWaiting**](cbaseallocator-m-lwaiting.md) größer als 0 (null). Wenn *m \_ lWaiting* größer als 0 (null) ist, ruft diese Methode die **ReleaseSemaphore-Funktion** auf dem [**CBaseAllocator::m \_ hSem-Semaphor**](cbaseallocator-m-hsem.md) auf und aktiviert alle wartenden Threads. Außerdem wird *m \_ lWaiting* auf 0 (null) zurückgesetzt.

Diese Methode wird innerhalb der [**CBaseAllocator::ReleaseBuffer-Methode**](cbaseallocator-releasebuffer.md) aufgerufen, wenn ein Beispiel an die freie Liste zurückgegeben wird. und aus der [**CBaseAllocator::D ecommit-Methode,**](cbaseallocator-decommit.md) wenn der Zuweisungscommit aufgehoben wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseAllocator-Klasse**](cbaseallocator.md)
</dt> </dl>

 

 




