---
description: Die ShouldDrawSampleNow-Methode bestimmt, ob das Video gezeichnet werden soll, ohne einen Timer-Advise-Link mit der Uhr zu setzen.
ms.assetid: 2cbefc66-0d99-4559-b210-3163cd413dbf
title: CBaseVideoRenderer.ShouldDrawSampleNow-Methode (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.ShouldDrawSampleNow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e3c0297ccf670de12380c5f02af2c67d6050bac29dd1fa7e7e89a6e6c7c20592
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074685"
---
# <a name="cbasevideorenderershoulddrawsamplenow-method"></a>CBaseVideoRenderer.ShouldDrawSampleNow-Methode

Die `ShouldDrawSampleNow` -Methode bestimmt, ob das Video gezeichnet werden soll, ohne einen Timer-Advise-Link mit der Uhr zu setzen.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT ShouldDrawSampleNow(
   IMediaSample   *pMediaSample,
   REFERENCE_TIME *ptrStart,
   REFERENCE_TIME *ptrEnd
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pMediaSample* 
</dt> <dd>

Zeiger auf die [**IMediaSample-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-imediasample) für das Beispiel.

</dd> <dt>

*ptrStart* 
</dt> <dd>

Zeiger auf die Zeit, zu der mit dem Rendern begonnen werden soll.

</dd> <dt>

*ptrEnd* 
</dt> <dd>

Zeiger auf die Zeit, zu der das Rendering nicht mehr möglich ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Gibt S OK zurück, um gleichzeitiges Zeichnen ohne Warten zu bedeuten, S FALSE bedeutet Zeichnen zum Zeitpunkt \_ \_ *ptrStart* oder einen Fehler, der bedeutet, dass das Beispiel nicht ge zeichnen soll. Das heißt, es zu überspringen, um Zeit zu sparen.

## <a name="remarks"></a>Hinweise

Diese Memberfunktion überschreibt [**CBaseRenderer::ShouldDrawSampleNow**](cbaserenderer-shoulddrawsamplenow.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseVideoRenderer-Klasse**](cbasevideorenderer.md)
</dt> </dl>

 

 




