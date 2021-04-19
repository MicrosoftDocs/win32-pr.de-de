---
description: Die fastrauender-Methode zeichnet das Video Bild mithilfe der Funktionen BitBLT oder StretchBlt.
ms.assetid: 8bbc96ce-393f-46fb-bf90-61d3ce0ef0d6
title: Cdrawimage. fastrauender-Methode (winutil. h)
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
ms.openlocfilehash: 823583beed6696d40803ccc098410dac053b8948
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373730"
---
# <a name="cdrawimagefastrender-method"></a>Cdrawimage. fastrauender-Methode

Die- `FastRender` Methode zeichnet das Video Bild mithilfe der Funktionen **BitBLT** oder **StretchBlt** .

## <a name="syntax"></a>Syntax


```C++
void FastRender(
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

Die [**cdrawimage::D rawImage**](cdrawimage-drawimage.md) -Methode ruft diese Methode auf, aber nur, wenn die Zuweisung für die Verbindung ein [**cimagezuordcator**](cimageallocator.md) -Objekt ist. In diesem Fall ist das Medien Beispiel garantiert ein [**cimagesample**](cimagesample.md) -Objekt. Das **cimagesample** -Objekt verwendet die Funktion " **kreatedibsection** ", um den gemeinsamen Speicher für die Bitmap zuzuordnen, sodass das Bild entweder mithilfe von **BitBLT** oder **StretchBlt** gezeichnet werden kann.

Diese Methode ruft **BitBLT** auf, wenn die Quell-und ungültige Ziel-Rechtecke genau übereinstimmen oder andernfalls **StretchBlt** .

Wenn der Filter nicht Besitzer der Zuweisung ist, verwendet die **DrawImage** -Methode [**cdrawimage:: slowrendering**](cdrawimage-slowrender.md) zum Zeichnen des Bilds.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cdrawimage-Klasse**](cdrawimage.md)
</dt> </dl>

 

 




