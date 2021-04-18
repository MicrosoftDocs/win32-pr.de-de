---
description: Mit der slowrendering-Methode wird das Video Bild mithilfe der Funktionen SetDIBitsToDevice oder StretchDIBits gezeichnet.
ms.assetid: e1d8b189-b588-48eb-988a-3e5dedb38dbd
title: Cdrawimage. slowrendering-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.SlowRender
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b736bf6c44d4ada6e0a28408c449c9f8b2f1e1cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358363"
---
# <a name="cdrawimageslowrender-method"></a>Cdrawimage. slowrendering-Methode

Mit der- `SlowRender` Methode wird das Video Bild mithilfe der Funktionen **SetDIBitsToDevice** oder **StretchDIBits** gezeichnet.

## <a name="syntax"></a>Syntax


```C++
void SlowRender(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pmediasample* 
</dt> <dd>

Ein Zeiger auf die [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Schnittstelle des Beispiels, das das Bild enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Wenn [**cdrawimage:: usingimagezuordcator**](cdrawimage-usingimageallocator.md) **false** zurückgibt, verwendet die [**cdrawimage::D rawImage**](cdrawimage-drawimage.md) -Methode `SlowRender` zum Zeichnen des Video Bilds. Andernfalls verwendet DrawImage die **fastrinender** -Methode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cdrawimage-Klasse**](cdrawimage.md)
</dt> <dt>

[**Cdrawimage:: fastrauender**](cdrawimage-fastrender.md)
</dt> </dl>

 

 




