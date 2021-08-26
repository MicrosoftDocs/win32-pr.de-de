---
description: Die DrawImage-Methode zeichnet einen Videorahmen im Videofenster.
ms.assetid: 22e7f59c-90f7-4e0c-8993-eea1eaf58fba
title: CDrawImage.DrawImage-Methode (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.DrawImage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c2791d20b906f2a2adce31ce99b9e7498854c8fca00ade4507db0207e04b2cde
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043605"
---
# <a name="cdrawimagedrawimage-method"></a>CDrawImage.DrawImage-Methode

Die `DrawImage` -Methode zeichnet einen Videorahmen im Videofenster.

## <a name="syntax"></a>Syntax


```C++
BOOL DrawImage(
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

Gibt **TRUE** zurück, wenn erfolgreich, **andernfalls FALSE.**

## <a name="remarks"></a>Hinweise

Diese Methode delegiert an [**CDrawImage::FastRender**](cdrawimage-fastrender.md) oder [**CDrawImage::SlowRender,**](cdrawimage-slowrender.md)je nachdem, ob der Filter die Zuweisung besitzt, die das Beispiel bereitgestellt hat. Wenn der Filter die Zuweisung besitzt, ist das Beispiel garantiert ein [**CImageSample-Objekt.**](cimagesample.md) In diesem Fall verwendet das Beispiel freigegebenen Arbeitsspeicher, der von GDI belegt wird, und das Bild kann entweder mit **BitBlt** oder **StretchBlt** gezeichnet werden. Andernfalls müssen die Bilder mithilfe der **langsameren Funktionen SetDIBitsToDevice** oder **StretchDIBits** gezeichnet werden.

In Debugbuilds ruft diese Methode **DisplaySampleTimes** auf, um die Zeitstempel des Beispiels über das Videobild zu zeichnen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CDrawImage-Klasse**](cdrawimage.md)
</dt> <dt>

[**CDrawImage::UsingImageAllocator**](cdrawimage-usingimageallocator.md)
</dt> </dl>

 

 




