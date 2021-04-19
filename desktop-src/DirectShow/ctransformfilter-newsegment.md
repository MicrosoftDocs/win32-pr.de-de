---
description: Die newsegment-Methode benachrichtigt den Filter, dass nach diesem-Befehl empfangene Medien Beispiele als Segment gruppiert werden.
ms.assetid: 78ddaac7-9c1f-47b6-835d-dd16b1f5b01f
title: Ctransformfilter. newsegment-Methode (Transfrm. h)
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
ms.openlocfilehash: 0fd046288886d3e7619419dd591dd94310f56020
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359705"
---
# <a name="ctransformfilternewsegment-method"></a>Ctransformfilter. newsegment-Methode

Die- `NewSegment` Methode benachrichtigt den Filter, dass nach diesem-Befehl empfangene Medien Beispiele als Segment gruppiert werden.

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

*tSTART* 
</dt> <dd>

Die Startzeit des Segments, relativ zur ursprünglichen Quelle.

</dd> <dt>

*tstopps* 
</dt> <dd>

Die Endzeit des Segments, relativ zur ursprünglichen Quelle.

</dd> <dt>

*drate* 
</dt> <dd>

Rate, mit der das Segment verarbeitet werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Bemerkungen

Die [**ctransforminputpin:: newsegment**](ctransforminputpin-newsegment.md) -Methode der Eingabe-PIN ruft diese Methode auf. Diese Methode stellt den-Befehl `NewSegment` an die downstreameingabepin bereit.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ctransformfilter-Klasse**](ctransformfilter.md)
</dt> </dl>

 

 




