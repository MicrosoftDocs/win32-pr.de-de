---
description: Die drawvideoimagehere-Methode zeichnet ein Bild aus einem Medien Beispiel in einen angegebenen Gerätekontext.
ms.assetid: b11e1c6b-5a29-444f-a0a9-049cd9d49b13
title: Cdrawimage. drawvideoimagehere-Methode (winutil. h)
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
ms.openlocfilehash: 599dd82e282f2d14ac7e974363a62695e209c080
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352950"
---
# <a name="cdrawimagedrawvideoimagehere-method"></a>Cdrawimage. drawvideoimagehere-Methode

Die- `DrawVideoImageHere` Methode zeichnet ein Bild aus einem Medien Beispiel in einen angegebenen Gerätekontext.

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

*HDC* 
</dt> <dd>

Handle für einen Gerätekontext, in dem die Zeichnung stattfindet.

</dd> <dt>

*pmediasample* 
</dt> <dd>

Ein Zeiger auf die [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Schnittstelle des Beispiels, das das Bild enthält.

</dd> <dt>

*lprcsrc* 
</dt> <dd>

Zeiger auf ein Quell Rechteck, das zum Zeichnen verwendet werden soll. Wenn der Wert **null** ist, wird das Rechteck in [**cdrawimage:: m \_ SourceRect**](cdrawimage-m-sourcerect.md) verwendet.

</dd> <dt>

*lprcdst* 
</dt> <dd>

Zeiger auf ein Ziel Rechteck, das zum Zeichnen verwendet werden soll. Wenn der Wert **null** ist, wird das Rechteck in [**cdrawimage:: m \_ targetrect**](cdrawimage-m-targetrect.md) verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cdrawimage-Klasse**](cdrawimage.md)
</dt> </dl>

 

 




