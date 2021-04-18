---
title: Slider. thumbimage
description: Das Attribut "thumbimage" gibt das Bild an, das zum Darstellen der aktuellen Position des Schiebereglers verwendet wird, oder ruft es ab.
ms.assetid: 3aa69188-3443-483c-81a9-bf22832509d8
keywords:
- Slider. thumbimage-Fenster Media Player
topic_type:
- apiref
api_name:
- SLIDER.thumbImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b798dfbae24fe2cef3669d2fb372966e47254026
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371702"
---
# <a name="sliderthumbimage"></a>Slider. thumbimage

Das Attribut " **thumbimage** " gibt das Bild an, das zum Darstellen der aktuellen Position des Schiebereglers verwendet wird, oder ruft es ab.

``` syntax
        elementID.thumbImage
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Lese- **/schreibzeichenfolge** , die den Namen einer Bilddatei enthält.

## <a name="remarks"></a>Bemerkungen

Das **thumbimage** gibt das Bild an, das verwendet wird, um die aktuelle Position darzustellen, und zeigt an, dass der Benutzer mit dem Steuerelement Aktionen ausführen kann. Wenn kein Thumb-Bild angegeben wird, ist der Schieberegler nicht interaktiv.

Das Thumb-Bild wird in der schmalen Dimension des Schieberegler-Steuer Elements zentriert. Wenn das Thumb-Bild schmaler ist als das-Steuerelement, wird das Bild in der Mitte des Hintergrunds angezeigt. Wenn das Thumb-Bild größer als das-Steuerelement ist, werden die Enden des Bilds abgeschnitten.

Die Position des Schiebereglers wird durch die Mitte des Thumb-Bilds angegeben. Wenn **BorderSize** gleich 0 (null) ist, wird nur die Hälfte des Thumb-Bilds am Anfang und am Ende des Schiebereglers sichtbar. Um dies zu verhindern, legen Sie **BorderSize** auf einen Wert fest, der größer oder gleich der Hälfte der Breite des Thumb-Bilds ist (oder die halbe Höhe, wenn die **Richtung** auf "vertikal" festgelegt ist).

Die unterstützten Formate sind BMP, JPG, PNG und GIF (keine animierten GIFs).

Weitere Informationen finden Sie unter **customslider**. [positionImage](customslider-positionimage.md) -Attribut für ein Beispiel, das veranschaulicht, wie die Attribute des **Slider** -Elements verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Slider-Element**](slider-element.md)
</dt> <dt>

[**Slider. BorderSize**](slider-bordersize.md)
</dt> <dt>

[**Schieberegler. Richtung**](slider-direction.md)
</dt> </dl>

 

 





