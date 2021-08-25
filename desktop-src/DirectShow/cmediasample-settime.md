---
description: Die SetTime-Methode legt die Streamzeiten fest, zu denen dieses Beispiel beginnen und abgeschlossen werden soll. Diese Methode implementiert die IMediaSample::SetTime-Methode.
ms.assetid: cab4907f-eb6f-4444-9b41-1f95a6ecffed
title: CMediaSample.SetTime-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: be9028db35cb6d74623bde77fac21e32793de436ea2f80d2f513687c15d1b64c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118156512"
---
# <a name="cmediasamplesettime-method"></a>CMediaSample.SetTime-Methode

Die `SetTime` -Methode legt die Streamzeiten fest, zu denen dieses Beispiel beginnen und beenden soll. Diese Methode implementiert die [**IMediaSample::SetTime-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime)

## <a name="syntax"></a>Syntax


```C++
HRESULT SetTime(
   REFERENCE_TIME *pTimeStart,
   REFERENCE_TIME *pTimeEnd
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pTimeStart* 
</dt> <dd>

Zeiger auf die Streamzeit, zu der das Beispiel beginnt, in Einheiten von 100 Nanosekunden oder **NULL.**

</dd> <dt>

*pTimeEnd* 
</dt> <dd>

Zeiger auf die Streamzeit, zu der das Beispiel endet, in Einheiten von 100 Nanosekunden oder **NULL.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Hinweise

Diese Methode legt die Membervariablen [**CMediaSample::m \_ Start**](cmediasample-m-start.md) und [**CMediaSample::m \_ End**](cmediasample-m-end.md) fest, die die Zeitstempel angeben. Außerdem wird die [**Membervariable CMediaSample::m \_ dwFlags**](cmediasample-m-dwflags.md) aktualisiert, die angibt, ob die Zeitstempel gültig sind.

Informationen zu Zeitstempeln finden Sie unter [Zeit und Uhren in DirectShow.](time-and-clocks-in-directshow.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CMediaSample-Klasse**](cmediasample.md)
</dt> </dl>

 

 




