---
description: Dauer des Streams. Standardmäßig wird der Wert auf den Wert der Membervariablen CSourceSeeking::m \_ rtStop festgelegt.
ms.assetid: a87b321e-3179-4485-969b-bf12cb634b43
title: CSourceSeeking::m_rtDuration Member (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_rtDuration
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6aa62a3cdf906a4e9666b7786c08e49fca250ef042d187902132410cc2f0abaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053970"
---
# <a name="csourceseekingm_rtduration-member"></a>CSourceSeeking::m \_ rtDuration-Member

Dauer des Streams. Standardmäßig wird der Wert auf den Wert der [**Membervariablen CSourceSeeking::m \_ rtStop**](csourceseeking-m-rtstop.md) festgelegt.

## <a name="syntax"></a>Syntax


```C++
CRefTime m_rtDuration;
```



## <a name="remarks"></a>Hinweise

Halten Sie den **Abschnitt "m \_ pLock** critical" vor dem Zugriff auf diese Variable.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CSourceSeeking-Klasse**](csourceseeking.md)
</dt> </dl>

 

 




