---
description: Die ondirectrender-Methode sammelt Zeit Steuerungsinformationen, die die Synchronisierung und die Qualitätskontrolle steuern.
ms.assetid: ed617fac-b2c6-4a3a-ac91-77e2d7cce981
title: Cbasevideorenderer. ondirectrender-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnDirectRender
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7c117366590c96b63ff4595d4563e92aec542cfb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359298"
---
# <a name="cbasevideorendererondirectrender-method"></a>Cbasevideorenderer. ondirectrender-Methode

Die **ondirectrender** -Methode sammelt Zeit Steuerungsinformationen, die die Synchronisierung und die Qualitätskontrolle steuern.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT OnDirectRender(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pmediasample* 
</dt> <dd>

Zeiger auf die [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Schnittstelle des Mediums Sample.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Diese Methode anstelle von " [**onrenderstart**](cbasevideorenderer-onrenderstart.md) " und " [**onrenderend**](cbasevideorenderer-onrenderend.md)" aufzurufen. Diese Methode wird vom DirectDraw-Videorenderer verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasevideorenderer-Klasse**](cbasevideorenderer.md)
</dt> </dl>

 

 




