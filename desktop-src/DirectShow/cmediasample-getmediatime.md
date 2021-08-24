---
description: Die GetMediaTime-Methode ruft die Medienzeiten für dieses Beispiel ab. Diese Methode implementiert die IMediaSample::GetMediaTime-Methode.
ms.assetid: f58a2162-5764-48f2-8984-ee4bba1229ab
title: CMediaSample.GetMediaTime-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 901531b3aaff882700a6a6196330cc7b0823b8b0069024101953f5f79a54e17d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634680"
---
# <a name="cmediasamplegetmediatime-method"></a>CMediaSample.GetMediaTime-Methode

Die `GetMediaTime` -Methode ruft die Medienzeiten für dieses Beispiel ab. Diese Methode implementiert die [**IMediaSample::GetMediaTime-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatime)

## <a name="syntax"></a>Syntax


```C++
HRESULT GetMediaTime(
   LONGLONG *pStart,
   LONGLONG *pEnd
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pStart* 
</dt> <dd>

Zeiger auf eine Variable, die die Startzeit des Mediums empfängt.

</dd> <dt>

*Pend* 
</dt> <dd>

Zeiger auf eine Variable, die die Medienstoppzeit empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der in der folgenden Tabelle gezeigten **HRESULT-Werte** zurück.



| Rückgabecode                                                                                                  | Beschreibung                                         |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                         | Erfolg.<br/>                                 |
| <dl> <dt>**VFW \_ E \_ MEDIA \_ TIME \_ NOT \_ SET**</dt> </dl> | Für dieses Beispiel wurden keine Medienzeiten festgelegt.<br/> |



 

## <a name="remarks"></a>Hinweise

Die [**CMediaSample::m \_ MediaEnd-Elementvariable**](cmediasample-m-mediaend.md) gibt einen Offset von [**CMediaSample::m \_ MediaStart**](cmediasample-m-mediastart.md)an. Der vom *pEnd-Parameter* empfangene Wert ist jedoch eine absolute Medienzeit, die als **m \_ MediaStart**  +  **m \_ MediaEnd** berechnet wird.

Informationen zu Medienzeiten finden Sie unter [Uhrzeit und Uhren in DirectShow.](time-and-clocks-in-directshow.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CMediaSample-Klasse**](cmediasample.md)
</dt> </dl>

 

 




