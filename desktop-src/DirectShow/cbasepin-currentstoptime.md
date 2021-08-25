---
description: Die CurrentStopTime-Methode ruft die Segmentstoppzeit ab, die von der CBasePin::NewSegment-Methode festgelegt wird.
ms.assetid: 2066c4a5-2d39-4a2e-b2d6-48c615862aec
title: CBasePin.CurrentStopTime-Methode (Amfilter.h)
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
ms.openlocfilehash: 2905913828c91fffde9fb474802c8dea0e0f83d59ccdb5408f846a1936071cf6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916700"
---
# <a name="cbasepincurrentstoptime-method"></a>CBasePin.CurrentStopTime-Methode

Die `CurrentStopTime` -Methode ruft die Segmentstoppzeit ab, die von der [**CBasePin::NewSegment-Methode**](cbasepin-newsegment.md) festgelegt wird.

## <a name="syntax"></a>Syntax


```C++
REFERENCE_TIME CurrentStopTime();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt den Wert von [**CBasePin::m \_ tStop**](cbasepin-m-tstop.md)zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBasePin-Klasse**](cbasepin.md)
</dt> </dl>

 

 




