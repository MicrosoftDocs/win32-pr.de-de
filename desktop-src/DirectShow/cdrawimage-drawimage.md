---
description: Mit der DrawImage-Methode wird ein Videorahmen im Videofenster gezeichnet.
ms.assetid: 22e7f59c-90f7-4e0c-8993-eea1eaf58fba
title: Cdrawimage. DrawImage-Methode (winutil. h)
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
ms.openlocfilehash: d219eb82ab2cf1929605eee4045c2f278022ad98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357645"
---
# <a name="cdrawimagedrawimage-method"></a>Cdrawimage. DrawImage-Methode

Die- `DrawImage` Methode zeichnet einen Videoframe im Videofenster.

## <a name="syntax"></a>Syntax


```C++
BOOL DrawImage(
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

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

Diese Methode delegiert an [**cdrawimage:: fastrinender**](cdrawimage-fastrender.md) oder [**cdrawimage:: slowrendering**](cdrawimage-slowrender.md), je nachdem, ob der Filter die Zuweisung besitzt, die das Beispiel bereitgestellt hat. Wenn der Filter die Zuweisung besitzt, ist das Beispiel garantiert ein [**cimagesample**](cimagesample.md) -Objekt. In diesem Fall verwendet das Beispiel den gemeinsam genutzten Speicher, der von GDI zugeordnet wird, und das Image kann entweder mithilfe von **BitBLT** oder **StretchBlt** gezeichnet werden. Andernfalls müssen die Bilder mithilfe der langsameren Funktionen **SetDIBitsToDevice** oder **StretchDIBits** gezeichnet werden.

In Debugbuilds ruft diese Methode **displaysampletimes** auf, um die Zeitstempel des Beispiels über das Video Bild zu zeichnen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cdrawimage-Klasse**](cdrawimage.md)
</dt> <dt>

[**Cdrawimage:: usingimagezuordcator**](cdrawimage-usingimageallocator.md)
</dt> </dl>

 

 




