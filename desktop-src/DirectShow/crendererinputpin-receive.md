---
description: 'Die Receive-Methode empfängt das nächste Medien Beispiel im Stream. Diese Methode überschreibt die cbasinput PIN:: Receive-Methode.'
ms.assetid: b09140f0-2e3a-47b1-ace7-954043dd62eb
title: Crendererinputpin. Receive-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d3ddac3f456e1ab24574a4743983d20a828896e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354816"
---
# <a name="crendererinputpinreceive-method"></a>Crendererinputpin. Receive-Methode

Die- `Receive` Methode empfängt das nächste Medien Beispiel im Stream. Diese Methode überschreibt die [**cbasinput PIN:: Receive**](cbaseinputpin-receive.md) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT Receive(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pmediasample* 
</dt> <dd>

Zeiger auf die [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Schnittstelle des Beispiels.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode ruft die [**cbaserenderer:: Receive**](cbaserenderer-receive.md) -Methode des Filters auf, die das Rendering behandelt. Wenn diese Methode fehlschlägt, sendet die PIN ein EC \_ errorabort-Ereignis.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Crendererinputpin-Klasse**](crendererinputpin.md)
</dt> </dl>

 

 




