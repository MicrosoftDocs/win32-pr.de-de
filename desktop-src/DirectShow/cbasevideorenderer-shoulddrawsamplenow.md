---
description: Die Methode "schulddrawsamplenow" bestimmt, ob das Video gezeichnet werden soll, ohne einen Zeit Geber-anweichung-Link mit der Uhr festzulegen
ms.assetid: 2cbefc66-0d99-4559-b210-3163cd413dbf
title: Cbasevideorenderer. schulddrawsamplenow-Methode (renbase. h)
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
ms.openlocfilehash: 8c96b7453eb6009121fd6782030f7988663f5e8f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367578"
---
# <a name="cbasevideorenderershoulddrawsamplenow-method"></a>Cbasevideorenderer. schulddrawsamplenow-Methode

Die- `ShouldDrawSampleNow` Methode bestimmt, ob das Video gezeichnet werden soll, ohne eine Zeit Geber Empfehlung mit der Uhr festzulegen.

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

*pmediasample* 
</dt> <dd>

Zeiger auf die [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Schnittstelle für das Beispiel.

</dd> <dt>

*ptrstart* 
</dt> <dd>

Zeiger auf den Zeitpunkt, zu dem das Rendering begonnen wird.

</dd> <dt>

*ptrend* 
</dt> <dd>

Zeiger auf die Zeit zum Abbrechen des Renderings.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Gibt den Wert "s OK" zurück, \_ um gleichzeitig zu zeichnen, ohne zu warten, "s false", um zum \_ Zeitpunkt " *ptrstart*" zu zeichnen, oder ein Fehler, der bedeutet, dass das Beispiel nicht gezeichnet wird

## <a name="remarks"></a>Bemerkungen

Diese Member-Funktion überschreibt [**cbaserenderer:: schulddrawsamplenow**](cbaserenderer-shoulddrawsamplenow.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasevideorenderer-Klasse**](cbasevideorenderer.md)
</dt> </dl>

 

 




