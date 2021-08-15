---
description: Die NewSegment-Methode benachrichtigt den Filter, dass medienbeispiele, die nach diesem Aufruf empfangen wurden, als Segment gruppiert werden.
ms.assetid: 78ddaac7-9c1f-47b6-835d-dd16b1f5b01f
title: CTransformFilter.NewSegment-Methode (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.NewSegment
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a2cb83c376b012ae3474f87b0f8d26c7fb5560812c1d8ddcbb3ea62293797bb9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953549"
---
# <a name="ctransformfilternewsegment-method"></a>CTransformFilter.NewSegment-Methode

Die -Methode benachrichtigt den Filter, dass medienbeispiele, die nach diesem Aufruf empfangen `NewSegment` wurden, als Segment gruppiert werden.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT NewSegment(
   REFERENCE_TIME tStart,
   REFERENCE_TIME tStop,
   double         dRate
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*tStart* 
</dt> <dd>

Startzeit des Segments relativ zur ursprünglichen Quelle.

</dd> <dt>

*tStop* 
</dt> <dd>

Die Stoppzeit des Segments relativ zur ursprünglichen Quelle.

</dd> <dt>

*dRate* 
</dt> <dd>

Rate, mit der das Segment verarbeitet werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Hinweise

Die [**CTransformInputPin::NewSegment-Methode**](ctransforminputpin-newsegment.md) des Eingabepins ruft diese Methode auf. Diese Methode übergibt den `NewSegment` Aufruf an den Downstreameingabepin.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CTransformFilter-Klasse**](ctransformfilter.md)
</dt> </dl>

 

 




