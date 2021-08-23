---
description: Die NewSegment-Methode benachrichtigt den Pin, dass medienbeispiele, die nach diesem Aufruf empfangen wurden, als Segment gruppiert werden. Diese Methode implementiert die IPin::NewSegment-Methode.
ms.assetid: 8925b8b5-13dd-4127-82d8-96525bd4d6fc
title: CTransformInputPin.NewSegment-Methode (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.NewSegment
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c522755fe898717f0c06af9698be07ab2ebca491666982d6ff62756ef48ae08f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907420"
---
# <a name="ctransforminputpinnewsegment-method"></a>CTransformInputPin.NewSegment-Methode

Die -Methode benachrichtigt den Pin, dass Medienbeispiele, die nach diesem Aufruf empfangen `NewSegment` wurden, als Segment gruppiert werden. Diese Methode implementiert die [**IPin::NewSegment-Methode.**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment)

## <a name="syntax"></a>Syntax


```C++
HRESULT NewSegment(
   REFERENCE_TIME tStart,
   REFERENCE_TIME tStop,
   double         dRate
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*tStart* 
</dt> <dd>

Startzeit des Segments.

</dd> <dt>

*tStop* 
</dt> <dd>

Die Stoppzeit des Segments.

</dd> <dt>

*dRate* 
</dt> <dd>

Rate des Segments.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK oder einen anderen **HRESULT-Wert** zurück.

## <a name="remarks"></a>Hinweise

Diese Methode überschreibt die [**CBasePin::NewSegment-Methode.**](cbasepin-newsegment.md) Sie ruft die [**CTransformFilter::NewSegment-Methode**](ctransformfilter-newsegment.md) des Filters auf, um den Aufruf nachgeschaltet zu liefern.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



 

 




