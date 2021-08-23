---
description: 'CBaseFilter.StreamTime-Methode: Die StreamTime-Methode ruft die aktuelle Streamzeit ab.'
ms.assetid: 88a2939d-fb51-49fd-af71-21c99511de43
title: CBaseFilter.StreamTime-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.StreamTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: af266e22cb8ee5a2ff5d5d233dc6cfc623e37cd0d34c073db4dbab71d9c221ff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635480"
---
# <a name="cbasefilterstreamtime-method"></a>CBaseFilter.StreamTime-Methode

Die **StreamTime-Methode** ruft die aktuelle Streamzeit ab.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT StreamTime(
  [ref] CRefTime &rtStream
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*rtStream* \[ Ref\]
</dt> <dd>

Verweis auf ein [**CRefTime-Objekt,**](creftime.md) das die aktuelle Streamzeit empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.



| Rückgabecode                                                                                      | Beschreibung                                 |
|--------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>             | Erfolg.<br/>                         |
| <dl> <dt>**VFW \_ E \_ NO \_ CLOCK**</dt> </dl> | Es ist keine Referenzuhr verfügbar.<br/> |



 

## <a name="remarks"></a>Hinweise

Die Streamzeit wird als aktuelle Referenzzeit (wie von der Referenzuhr angegeben) abzüglich der Startzeit (angegeben durch [**CBaseFilter::m \_ tStart ) definiert.**](cbasefilter-m-tstart.md) Der Zeitstempel eines *Medienbeispiels* gibt die Streamzeit an, zu der es gerendert werden soll. Wenn ein Beispiel mit einem Zeitstempel, der kleiner als die aktuelle Streamzeit ist, noch nicht gerendert wurde, ist es zu spät.

Diese Methode ruft die Streamzeit ab, indem [**sie IReferenceClock::GetTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) aufruft, um die aktuelle Verweiszeit zu erhalten, und subtrahiert dann die anfängliche Startzeit.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Zeit und Uhren in DirectShow](time-and-clocks-in-directshow.md)
</dt> <dt>

[**CBaseFilter-Klasse**](cbasefilter.md)
</dt> </dl>

 

 




