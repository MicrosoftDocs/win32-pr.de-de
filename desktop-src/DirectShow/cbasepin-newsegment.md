---
description: Die NewSegment-Methode benachrichtigt den Pin, dass medienbeispiele, die nach diesem Aufruf empfangen wurden, als Segment gruppiert werden. Implementiert die IPin::NewSegment-Methode.
ms.assetid: e334d5a7-0398-496c-882c-bf73e6545867
title: CBasePin.NewSegment-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.NewSegment
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ed3ffc9cc0656509b29a6c32baeaf7311437a79e8402fbae0727cf9f93a30abe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119384550"
---
# <a name="cbasepinnewsegment-method"></a>CBasePin.NewSegment-Methode

Die -Methode benachrichtigt den Pin, dass Medienbeispiele, die nach diesem Aufruf empfangen `NewSegment` wurden, als Segment gruppiert werden. Implementiert die [**IPin::NewSegment-Methode.**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment)

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

Startmedienposition des Segments in Einheiten von 100 Nanosekunden.

</dd> <dt>

*tStop* 
</dt> <dd>

Endmedienposition des Segments in Einheiten von 100 Nanosekunden.

</dd> <dt>

*dRate* 
</dt> <dd>

Rate, mit der dieses Segment verarbeitet werden soll, als Prozentsatz der ursprünglichen Rate.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Hinweise

Diese Methode legt die [**Membervariablen CBasePin::m \_ tStart,**](cbasepin-m-tstart.md) [**CBasePin::m \_ tStop**](cbasepin-m-tstop.md)und [**CBasePin::m \_ dRate**](cbasepin-m-drate.md) fest. Überschreiben Sie in der abgeleiteten Klasse diese Methode, um die Benachrichtigung nachgelagert zu übergeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBasePin-Klasse**](cbasepin.md)
</dt> </dl>

 

 




