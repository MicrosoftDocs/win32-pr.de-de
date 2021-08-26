---
description: Die CurrentStartTime-Methode ruft die Segmentstartzeit ab, die von der CBasePin::NewSegment-Methode festgelegt wird.
ms.assetid: 6bf7407e-0b23-47cf-925e-3fed183c76fa
title: CBasePin.CurrentStartTime-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CurrentStartTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c92355b397736b713fcf5fd09a61a130761a0cb954331b606ec1367fd65e6e20
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916740"
---
# <a name="cbasepincurrentstarttime-method"></a>CBasePin.CurrentStartTime-Methode

Die `CurrentStartTime` -Methode ruft die Segmentstartzeit ab, die von der [**CBasePin::NewSegment-Methode festgelegt**](cbasepin-newsegment.md) wird.

## <a name="syntax"></a>Syntax


```C++
REFERENCE_TIME CurrentStartTime();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt den Wert von [**CBasePin::m \_ tStart zurück.**](cbasepin-m-tstart.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBasePin-Klasse**](cbasepin.md)
</dt> </dl>

 

 




