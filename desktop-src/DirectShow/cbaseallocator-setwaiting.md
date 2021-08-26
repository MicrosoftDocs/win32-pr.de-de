---
description: Die SetWaiting-Methode erhöht die Anzahl der wartenden Threads.
ms.assetid: 4aec6177-fb32-44be-a58e-41a4f4aaf4f2
title: CBaseAllocator.SetWaiting-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.SetWaiting
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 674528b6da53b7835e437afac9a0564f91785b2f9a13f132e87a6763b80881c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057460"
---
# <a name="cbaseallocatorsetwaiting-method"></a>CBaseAllocator.SetWaiting-Methode

Die `SetWaiting` -Methode erhöht die Anzahl der wartenden Threads.

## <a name="syntax"></a>Syntax


```C++
void SetWaiting();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Methode erhöht die [**Membervariable CBaseAllocator::m \_ lWaiting.**](cbaseallocator-m-lwaiting.md) Wenn ein Thread in der [**CBaseAllocator::GetBuffer-Methode**](cbaseallocator-getbuffer.md) blockiert wird, ruft die Zuweisung auf `SetWaiting` und wartet dann, bis das [**CBaseAllocator::m \_ hSem-Semaphor**](cbaseallocator-m-hsem.md) signalisiert wird. Die [**CBaseAllocator::ReleaseBuffer-Methode**](cbaseallocator-releasebuffer.md) signalisiert das Semaphor und legt *m \_ lWaiting* wieder auf 0 (null) fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseAllocator-Klasse**](cbaseallocator.md)
</dt> </dl>

 

 




