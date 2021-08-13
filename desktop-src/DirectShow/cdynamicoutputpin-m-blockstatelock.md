---
description: Kritischer Abschnitt, der den Blockierungszustand schützt.
ms.assetid: 6d20cf4c-2c27-41e6-8d01-6cb5e3876a38
title: CDynamicOutputPin::m_BlockStateLock Member (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_BlockStateLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fa5382a30dcd434965c53e893d6818ab0f08a84c19ea0ddec53846c0c01c80f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118656680"
---
# <a name="cdynamicoutputpinm_blockstatelock-member"></a>CDynamicOutputPin::m \_ BlockStateLock-Member

Kritischer Abschnitt, der den Blockierungszustand schützt.

## <a name="syntax"></a>Syntax


```C++
CCritSec m_BlockStateLock;
```



## <a name="remarks"></a>Hinweise

Halten Sie diesen kritischen Abschnitt bei, bevor Sie eine der folgenden Membervariablen verwenden:

-   [**CDynamicOutputPin::m \_ BlockState**](cdynamicoutputpin-m-blockstate.md)
-   [**CDynamicOutputPin::m \_ dwBlockCallerThreadID**](cdynamicoutputpin-m-dwblockcallerthreadid.md)
-   [**CDynamicOutputPin::m \_ dwNumOutstandingOutputPinUsers**](cdynamicoutputpin-m-dwnumoutstandingoutputpinusers.md)
-   [**CDynamicOutputPin::m \_ hNotifyCallerPinBlockedEvent**](cdynamicoutputpin-m-hnotifycallerpinblockedevent.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CDynamicOutputPin-Klasse**](cdynamicoutputpin.md)
</dt> </dl>

 

 




