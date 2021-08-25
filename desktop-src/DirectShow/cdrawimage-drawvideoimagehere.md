---
description: Die DrawVideoImageHere-Methode zeichnet ein Bild aus einem Medienbeispiel in einen angegebenen Gerätekontext.
ms.assetid: b11e1c6b-5a29-444f-a0a9-049cd9d49b13
title: CDrawImage.DrawVideoImageHere-Methode (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.DrawVideoImageHere
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8137c4e18708ce6a0402d1d34caf9560054f267d8de0280a6efb5c3dd36e6517
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119909810"
---
# <a name="cdrawimagedrawvideoimagehere-method"></a>CDrawImage.DrawVideoImageHere-Methode

Die `DrawVideoImageHere` -Methode zeichnet ein Bild aus einem Medienbeispiel in einen angegebenen Gerätekontext.

## <a name="syntax"></a>Syntax


```C++
BOOL DrawVideoImageHere(
   HDC          hdc,
   IMediaSample *pMediaSample,
   RECT         *lprcSrc,
   RECT         *lprcDst
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Hdc* 
</dt> <dd>

Handle für einen Gerätekontext, in dem die Zeichnung ausgeführt wird.

</dd> <dt>

*pMediaSample* 
</dt> <dd>

Zeiger auf die [**IMediaSample-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-imediasample) des Beispiels, das das Bild enthält.

</dd> <dt>

*lprcSrc* 
</dt> <dd>

Zeiger auf ein Quellrechteck, das zum Zeichnen verwendet werden soll. Bei **NULL** wird das Rechteck in [**CDrawImage::m \_ SourceRect**](cdrawimage-m-sourcerect.md) verwendet.

</dd> <dt>

*lprcDst* 
</dt> <dd>

Zeiger auf ein Zielrechteck, das zum Zeichnen verwendet werden soll. Bei **NULL** wird das Rechteck in [**CDrawImage::m \_ TargetRect**](cdrawimage-m-targetrect.md) verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn erfolgreich.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CDrawImage-Klasse**](cdrawimage.md)
</dt> </dl>

 

 




