---
description: 'Die newsegment-Methode benachrichtigt die PIN, dass Medien Beispiele, die nach diesem-aufrufempfang empfangen werden, als Segment gruppiert werden. Diese Methode implementiert die IPin:: newsegment-Methode.'
ms.assetid: 8925b8b5-13dd-4127-82d8-96525bd4d6fc
title: Ctransforminputpin. newsegment-Methode (Transfrm. h)
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
ms.openlocfilehash: 25c455fe5ec6ddf9157e991b70b468ace653daa9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360908"
---
# <a name="ctransforminputpinnewsegment-method"></a>Ctransforminputpin. newsegment-Methode

Die- `NewSegment` Methode benachrichtigt die PIN, dass nach diesem-aufrufempfang empfangene Medien Beispiele als Segment gruppiert werden. Diese Methode implementiert die [**IPin:: newsegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) -Methode.

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

*tSTART* 
</dt> <dd>

Die Startzeit des Segments.

</dd> <dt>

*tstopps* 
</dt> <dd>

Die Endzeit des Segments.

</dd> <dt>

*drate* 
</dt> <dd>

Rate des Segments.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK oder einen anderen **HRESULT** -Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode überschreibt die [**cbasepin:: newsegment**](cbasepin-newsegment.md) -Methode. Die [**ctransformfilter:: newsegment**](ctransformfilter-newsegment.md) -Methode des Filters wird aufgerufen, um den Aufruf Downstream zu übermitteln.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



 

 




