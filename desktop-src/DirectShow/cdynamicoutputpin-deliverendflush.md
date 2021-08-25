---
description: 'CDynamicOutputPin.DeliverEndFlush-Methode: Die DeliverEndFlush-Methode fordert den verbundenen Eingabepin an, um einen Leerungsvorgang zu beenden.'
ms.assetid: e37bf06a-6cdc-4f14-bf2e-7a7d7004cff6
title: CDynamicOutputPin.DeliverEndFlush-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.DeliverEndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4cdd7e26b0c08b154c6cffd08066e8ae841a6aa849db4751ffa0cdf252848719
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055950"
---
# <a name="cdynamicoutputpindeliverendflush-method"></a>CDynamicOutputPin.DeliverEndFlush-Methode

Die `DeliverEndFlush` -Methode fordert den verbundenen Eingabepin an, um einen Leerungsvorgang zu beenden.

## <a name="syntax"></a>Syntax


```C++
HRESULT DeliverEndFlush();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg S \_ OK oder einen **HRESULT-Wert** zurück, der die Ursache des Fehlers angibt.

## <a name="remarks"></a>Hinweise

Diese Methode überschreibt die [**CBaseOutputPin::D eliverEndFlush-Methode.**](cbaseoutputpin-deliverendflush.md) Das Ereignis [**CDynamicOutputPin::m \_ hStopEvent**](cdynamicoutputpin-m-hstopevent.md) wird zurückgesetzt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CDynamicOutputPin-Klasse**](cdynamicoutputpin.md)
</dt> </dl>

 

 




