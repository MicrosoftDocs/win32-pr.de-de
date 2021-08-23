---
description: Die SetMediaTime-Methode legt die Medienzeiten für dieses Beispiel fest. Diese Methode implementiert die IMediaSample::SetMediaTime-Methode.
ms.assetid: 768812f8-c044-4499-9149-7c334c51e539
title: CMediaSample.SetMediaTime-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3709a5f487855148b8ad4042f61b74fbe6029ef64e00b751672bf478f1da866e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016368"
---
# <a name="cmediasamplesetmediatime-method"></a>CMediaSample.SetMediaTime-Methode

Die `SetMediaTime` -Methode legt die Medienzeiten für dieses Beispiel fest. Diese Methode implementiert die [**IMediaSample::SetMediaTime-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatime)

## <a name="syntax"></a>Syntax


```C++
HRESULT SetMediaTime(
   LONGLONG *pStart,
   LONGLONG *pEnd
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pStart* 
</dt> <dd>

Zeiger auf die Startzeit des Mediums oder **NULL.**

</dd> <dt>

*Pend* 
</dt> <dd>

Zeiger auf die Medienstoppzeit oder **NULL.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Hinweise

Die Medienstoppzeit muss größer als die Startzeit des Mediums sein. Verwenden **Sie NULL,** um die Medienzeiten für ungültig zu erklären.

Der *pEnd-Parameter* gibt eine absolute Medienzeit an, aber die [**CMediaSample::m \_ MediaEnd-Membervariable**](cmediasample-m-mediaend.md) wird als Offset von *pStart berechnet.* Mit anderen Worten: **m \_ MediaEnd**  =  \* *pTimeEnd* \* *pTimeStart*.  

Informationen zu Medienzeiten finden Sie unter [Uhrzeit und Uhren in DirectShow.](time-and-clocks-in-directshow.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CMediaSample-Klasse**](cmediasample.md)
</dt> </dl>

 

 




