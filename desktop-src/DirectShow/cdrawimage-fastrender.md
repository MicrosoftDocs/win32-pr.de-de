---
description: Die FastRender-Methode zeichnet das Videobild mithilfe der Funktionen BitBlt oder StretchBlt.
ms.assetid: 8bbc96ce-393f-46fb-bf90-61d3ce0ef0d6
title: CDrawImage.FastRender-Methode (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.FastRender
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 146c3736f7aaa89fc9a724d9dd7e4bfb58160e21e2de57f40a8e855c8a3c1446
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043604"
---
# <a name="cdrawimagefastrender-method"></a>CDrawImage.FastRender-Methode

Die `FastRender` -Methode zeichnet das Videobild mithilfe der **Funktionen BitBlt** oder **StretchBlt.**

## <a name="syntax"></a>Syntax


```C++
void FastRender(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pMediaSample* 
</dt> <dd>

Zeiger auf die [**IMediaSample-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-imediasample) des Beispiels, das das Bild enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die [**CDrawImage::D rawImage-Methode**](cdrawimage-drawimage.md) ruft diese Methode auf, jedoch nur, wenn die Zuweisung für die Verbindung ein [**CImageAllocator-Objekt**](cimageallocator.md) ist. In diesem Fall ist das Medienbeispiel garantiert ein [**CImageSample-Objekt.**](cimagesample.md) Das **CImageSample-Objekt** verwendet die **CreateDIBSection-Funktion,** um freigegebenen Arbeitsspeicher für die Bitmap zu reservieren. Dadurch kann das Bild mit **BitBlt** oder **StretchBlt ge zeichnen.**

Diese Methode ruft **BitBlt auf,** wenn die Quell- und Targerrechtecke genau übereinstimmen, **andernfalls StretchBlt.**

Wenn der Filter die Zuweisung nicht besitzt, verwendet die **DrawImage-Methode** [**CDrawImage::SlowRender,**](cdrawimage-slowrender.md) um das Bild zu zeichnen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CDrawImage-Klasse**](cdrawimage.md)
</dt> </dl>

 

 




