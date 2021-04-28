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
ms.openlocfilehash: f3334ac273a733c3f0591b76af7e76460997a199
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108120068"
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



 

## <a name="remarks"></a>Bemerkungen

Die Streamzeit wird als die aktuelle Referenzzeit (wie durch die Verweisuhr angegeben) abzüglich der Startzeit (angegeben durch [**CBaseFilter::m \_ tStart)**](cbasefilter-m-tstart.md)definiert. Der *Zeitstempel* eines Medienbeispiels gibt die Streamzeit an, zu der es gerendert werden soll. Wenn ein Beispiel mit einem Zeitstempel kleiner als die aktuelle Streamzeit noch nicht gerendert wurde, kommt es zu einem späteren Zeitpunkt.

Diese Methode ruft die Streamzeit ab, indem [**sie IReferenceClock::GetTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) aufruft, um die aktuelle Verweiszeit abzurufen, und subtrahiert dann die anfängliche Startzeit.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (streams.h einschließen)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Uhrzeit und Uhren in DirectShow](time-and-clocks-in-directshow.md)
</dt> <dt>

[**CBaseFilter-Klasse**](cbasefilter.md)
</dt> </dl>

 

 




