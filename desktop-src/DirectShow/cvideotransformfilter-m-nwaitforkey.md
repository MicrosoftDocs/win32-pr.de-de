---
description: Die aktuelle maximale Anzahl der zu verdringten Deltaframes.
ms.assetid: d14c594e-55ab-42c2-bdb0-6829f71d02dd
title: CVideoTransformFilter::m_nWaitForKey-Member (Vtrans.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_nWaitForKey
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 83cb78b233385e502d6508212492c54865aca28990ae079e4bf588776bd83fe5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998540"
---
# <a name="cvideotransformfilterm_nwaitforkey-member"></a>CVideoTransformFilter::m \_ nWaitForKey-Member

Die aktuelle maximale Anzahl der zu verdringten Deltaframes. Diese Variable ist zwar größer als 0 (null), der Filter verdrungen jedoch Frames, bis sie einen Keyframe erreicht. Für jeden gelöschten Frame dekrementiert der Filter diese Variable um 1, wodurch verhindert wird, dass der Filter eine übermäßige Anzahl von Frames verdrungen. Nach 30 Deltaframes in einer Zeile ohne Keyframes beginnt der Filter erneut mit der Bereitstellung von Frames.

## <a name="syntax"></a>Syntax


```C++
int m_nWaitForKey;
```



## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Vtrans.h (einschließlich Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CVideoTransformFilter-Klasse**](cvideotransformfilter.md)
</dt> </dl>

 

 




