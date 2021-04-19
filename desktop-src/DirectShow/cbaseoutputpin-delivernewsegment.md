---
description: Die delivernewsegment-Methode übergibt eine Benachrichtigung über einen neuen Segment an die verbundene Eingabe-PIN.
ms.assetid: 304f0267-88e0-4642-98a2-68ce973bdeab
title: Cbaseoutputpin. delivernewsegment-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.DeliverNewSegment
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3eb6d31a50095affdf38d44b69040304674ec6fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361448"
---
# <a name="cbaseoutputpindelivernewsegment-method"></a>Cbaseoutputpin. delivernewsegment-Methode

Die `DeliverNewSegment` -Methode übergibt eine Benachrichtigung über einen neuen Segment an die verbundene Eingabe-PIN.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT DeliverNewSegment(
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

Gibt einen **HRESULT** -Wert zurück. Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.



| Rückgabecode                                                                                           | Beschreibung                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Erfolg.<br/>              |
| <dl> <dt>**VFW \_ E \_ nicht \_ verbunden**</dt> </dl> | Die PIN ist nicht verbunden.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode ruft die [**IPin:: newsegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) -Methode für die Eingabe-PIN auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaseoutputpin-Klasse**](cbaseoutputpin.md)
</dt> </dl>

 

 




