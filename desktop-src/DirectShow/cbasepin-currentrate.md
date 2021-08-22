---
description: Die CurrentRate-Methode ruft die Segmentrate ab, die von der CBasePin::NewSegment-Methode festgelegt wird.
ms.assetid: 19780dd2-2dcf-4e5d-8a70-a46be05e040c
title: CBasePin.CurrentRate-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CurrentRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8c522a76aebce39e4670d4d00b3344bf56d20172c2d54243322dd36a5d203226
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955199"
---
# <a name="cbasepincurrentrate-method"></a>CBasePin.CurrentRate-Methode

Die `CurrentRate` -Methode ruft die Segmentrate ab, die von der [**CBasePin::NewSegment-Methode festgelegt**](cbasepin-newsegment.md) wird.

## <a name="syntax"></a>Syntax


```C++
double CurrentRate();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt den Wert von [**CBasePin::m \_ dRate zurück.**](cbasepin-m-drate.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBasePin-Klasse**](cbasepin.md)
</dt> </dl>

 

 




