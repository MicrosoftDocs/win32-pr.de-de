---
description: Das Ereignis, das signalisiert wird, wenn die Stecknadel erfolgreich blockiert wird oder der Benutzer einen ausstehenden Block abbricht.
ms.assetid: 699bb7f7-e4f7-47c3-bbb1-0bc6556651ae
title: CDynamicOutputPin::m_hNotifyCallerPinBlockedEvent Member (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_hNotifyCallerPinBlockedEvent
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cfea481a3f24aee808fffba9be91b1fecf63fce8a875dc056420a8f075b677d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118656405"
---
# <a name="cdynamicoutputpinm_hnotifycallerpinblockedevent-member"></a>CDynamicOutputPin::m \_ hNotifyCallerPinBlockedEvent-Member

Das Ereignis, das signalisiert wird, wenn die Stecknadel erfolgreich blockiert wird oder der Benutzer einen ausstehenden Block abbricht.

## <a name="syntax"></a>Syntax


```C++
HANDLE m_hNotifyCallerPinBlockedEvent;
```



## <a name="remarks"></a>Hinweise

Halten Sie vor dem Zugriff auf diese Variable den kritischen [**Abschnitt CDynamicOutputPin::m \_ BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) bei.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CDynamicOutputPin-Klasse**](cdynamicoutputpin.md)
</dt> </dl>

 

 




