---
description: Die streamtime-Methode ruft die aktuelle streamzeit ab.
ms.assetid: 88a2939d-fb51-49fd-af71-21c99511de43
title: Cbasefilter. streamtime-Methode (amfilter. h)
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
ms.openlocfilehash: f4370758eb4ab15a9e53a5157550ee2129783c7f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354735"
---
# <a name="cbasefilterstreamtime-method"></a>Cbasefilter. streamtime-Methode

Die **streamtime** -Methode ruft die aktuelle streamzeit ab.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT StreamTime(
  [ref] CRefTime &rtStream
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*rtstream* \[ atur\]
</dt> <dd>

Verweis auf ein-Objekt, das die aktuelle [**streamzeit empfängt**](creftime.md) .

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.



| Rückgabecode                                                                                      | Beschreibung                                 |
|--------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>             | Erfolg.<br/>                         |
| <dl> <dt>**VFW \_ E \_ No \_ Clock**</dt> </dl> | Es ist keine Referenzuhr verfügbar.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Die streamzeit wird als aktuelle Verweis Zeit (wie durch die verweisuhr angegeben) abzüglich der Startzeit (angegeben durch [**cbasefilter:: m \_ tSTART**](cbasefilter-m-tstart.md)) definiert. Der *Zeitstempel* eines Medien Beispiels gibt die streamzeit an, zu der er gerendert werden soll. Wenn eine Stichprobe mit einem Zeitstempel, der kleiner ist als die aktuelle streamzeit, noch nicht gerendert wurde, wird Sie später angezeigt.

Diese Methode ruft die streamzeit ab, indem [**IReferenceClock:: getTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) aufgerufen wird, um die aktuelle Verweis Zeit zu erhalten, und anschließend wird die anfängliche Startzeit subtrahieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Uhrzeit und Uhren in DirectShow](time-and-clocks-in-directshow.md)
</dt> <dt>

[**Cbasefilter-Klasse**](cbasefilter.md)
</dt> </dl>

 

 




