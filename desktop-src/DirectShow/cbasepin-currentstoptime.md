---
description: 'Die currentstoptime-Methode ruft die Endzeit des Segments ab, die von der cbasepin:: newsegment-Methode festgelegt wird.'
ms.assetid: 2066c4a5-2d39-4a2e-b2d6-48c615862aec
title: Cbasepin. currentstoptime-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CurrentStopTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 74fb25184bbcd0778268f74a4c40ccfb0722287f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370698"
---
# <a name="cbasepincurrentstoptime-method"></a>Cbasepin. currentstoptime-Methode

Die- `CurrentStopTime` Methode ruft die Endzeit des Segments ab, die von der [**cbasepin:: newsegment**](cbasepin-newsegment.md) -Methode festgelegt wird.

## <a name="syntax"></a>Syntax


```C++
REFERENCE_TIME CurrentStopTime();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt den Wert von [**cbasepin:: m \_ thalte**](cbasepin-m-tstop.md)zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasepin-Klasse**](cbasepin.md)
</dt> </dl>

 

 




