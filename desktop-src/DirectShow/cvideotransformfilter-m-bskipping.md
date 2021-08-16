---
description: Boolescher Wert, der angibt, ob der Filter derzeit Frames verwerfen soll. Wenn dieser Wert TRUE ist, wird der Filter weiterhin Frames löschen, bis er den nächsten Keyframe erreicht oder bis er 30 Deltaframes in einer Zeile ohne Keyframe empfängt.
ms.assetid: 1af22879-bf9b-4835-b3b5-06fb52b3140f
title: CVideoTransformFilter::m_bSkipping-Member (Vtrans.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bSkipping
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f865bdc707b206a8528413a357a4e14bcfe88fff813e1f62a44d30e6f4843ab4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117821915"
---
# <a name="cvideotransformfilterm_bskipping-member"></a>CVideoTransformFilter::m \_ bSkipping-Member

Boolescher Wert, der angibt, ob der Filter derzeit Frames verwerfen soll. Wenn dieser Wert **TRUE** ist, wird der Filter weiterhin Frames löschen, bis er den nächsten Keyframe erreicht oder bis er 30 Deltaframes in einer Zeile ohne Keyframe empfängt.

## <a name="syntax"></a>Syntax


```C++
BOOL m_bSkipping;
```



## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Vtrans.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CVideoTransformFilter-Klasse**](cvideotransformfilter.md)
</dt> </dl>

 

 




