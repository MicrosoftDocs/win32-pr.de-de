---
description: Die SetAbortSignal-Methode legt ein Flag fest, das angibt, ob das Rendering beendet und weitere Stichproben abgelehnt werden sollen.
ms.assetid: 2dbf3b4d-e285-4d17-a77c-01a16c09d148
title: CBaseRenderer.SetAbortSignal-Methode (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SetAbortSignal
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 819f279d20192ff82d9021e03780713f714682abf47aaf854b4568312572e8d8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119526533"
---
# <a name="cbaserenderersetabortsignal-method"></a>CBaseRenderer.SetAbortSignal-Methode

Die `SetAbortSignal` -Methode legt ein Flag fest, das angibt, ob das Rendering beendet und weitere Stichproben abgelehnt werden sollen.

## <a name="syntax"></a>Syntax


```C++
void SetAbortSignal(
   BOOL bAbort
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bAbort* 
</dt> <dd>

Boolescher Wert, der angibt, ob das Rendering beendet werden soll. True gibt an, dass der Filter keine weiteren Stichproben rendert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Methode legt das [**CBaseRenderer::m \_ bAbort-Flag**](cbaserenderer-m-babort.md) fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseRenderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




