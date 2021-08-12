---
description: Flag, das angibt, ob der Filter eine End-of-Stream-Benachrichtigung gesendet hat.
ms.assetid: 93f897de-04bb-4de4-a612-39b27c7d6f6c
title: CTransformFilter::m_bEOSDelivered-Member (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bEOSDelivered
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 38d27fabb9dd3ed2a37ed5d836bfdfb1036f4255e6af48580ab6e0678abad74b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118655104"
---
# <a name="ctransformfilterm_beosdelivered-member"></a>CTransformFilter::m \_ bEOSDelivered-Member

Flag, das angibt, ob der Filter eine End-of-Stream-Benachrichtigung gesendet hat.

## <a name="syntax"></a>Syntax


```C++
BOOL m_bEOSDelivered;
```



## <a name="remarks"></a>Hinweise

Wenn der Filter angehalten wird, wenn er über keine Eingabeverbindung verfügt, sendet er eine End-of-Stream-Benachrichtigung downstream und legt dieses Flag auf **TRUE** fest. Die Benachrichtigung zum Ende des Streams stellt sicher, dass der Downstreamfilter nicht auf Stichproben wartet. Beachten Sie, dass die [**EndOfStream-Methode**](ctransformfilter-endofstream.md) des Filters dieses Flag nicht festgelegt hat.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CTransformFilter-Klasse**](ctransformfilter.md)
</dt> </dl>

 

 




