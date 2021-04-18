---
description: 'Die newsegment-Methode benachrichtigt die PIN, dass Medien Beispiele, die nach diesem-aufrufempfang empfangen werden, als Segment gruppiert werden. Implementiert die IPin:: newsegment-Methode.'
ms.assetid: e334d5a7-0398-496c-882c-bf73e6545867
title: Cbasepin. newsegment-Methode (amfilter. h)
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
ms.openlocfilehash: 1f128ce8cb2fee5479efeddd5932d0392b92a6fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365458"
---
# <a name="cbasepinnewsegment-method"></a>Cbasepin. newsegment-Methode

Die- `NewSegment` Methode benachrichtigt die PIN, dass nach diesem-aufrufempfang empfangene Medien Beispiele als Segment gruppiert werden. Implementiert die [**IPin:: newsegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) -Methode.

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

Start Medien Position des Segments in 100-Nanosecond-Einheiten.

</dd> <dt>

*tstopps* 
</dt> <dd>

Die endmedien Position des Segments in 100-Nanosecond-Einheiten.

</dd> <dt>

*drate* 
</dt> <dd>

Die Rate, mit der dieses Segment verarbeitet werden soll, als Prozentsatz der ursprünglichen Rate.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode legt die Element Variablen [**cbasepin:: m \_ tSTART**](cbasepin-m-tstart.md), [**cbasepin:: m \_ tstoppt**](cbasepin-m-tstop.md)und [**cbasepin:: m \_ drate**](cbasepin-m-drate.md) fest. Überschreiben Sie diese Methode in der abgeleiteten Klasse, um die Benachrichtigung zu übergeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasepin-Klasse**](cbasepin.md)
</dt> </dl>

 

 




