---
description: Suchen nach Funktionen.
ms.assetid: c849db20-7567-41e0-9a57-85070a6e6a3a
title: CSourceSeeking::m_dwSeekingCaps Member (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_dwSeekingCaps
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 98044f8a05c22022f66e6014be591d99ec57451e33e8f2d7d464e6793bec19e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054030"
---
# <a name="csourceseekingm_dwseekingcaps-member"></a>CSourceSeeking::m \_ dwSeekingCaps-Member

Suchen nach Funktionen.

## <a name="syntax"></a>Syntax


```C++
DWORD m_dwSeekingCaps;
```



## <a name="remarks"></a>Hinweise

Standardmäßig wird der Wert auf die bitweise Kombination der folgenden Flags festgelegt:

-   AM \_ SEEKING \_ CanSeekForwards
-   AM \_ SEEKING \_ CanSeekBackwards
-   AM \_ SEEKING \_ CanSeekAbsolute
-   AM \_ SEEKING \_ CanGetStopPos
-   AM \_ SEEKING \_ CanGetDuration

Wenn der Filter einen anderen Satz von Funktionen unterstützt, überschreiben Sie diesen Wert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CSourceSeeking-Klasse**](csourceseeking.md)
</dt> </dl>

 

 




