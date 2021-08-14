---
title: BUTTONGROUP.transparencyColor
description: Das transparencyColor-Attribut gibt die transparente Farbe der BUTTONGROUP-Bilder an oder ruft sie ab.
ms.assetid: 604c5b29-50b9-4df6-9e48-488bf4fb7227
keywords:
- BUTTONGROUP.transparencyColor-Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.transparencyColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf97a25081e3f5c5729721bd675d9c59be1a4d52adc86acf6b9b75a0ee86dbac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118342663"
---
# <a name="buttongrouptransparencycolor"></a>BUTTONGROUP.transparencyColor

Das **transparencyColor-Attribut** gibt die transparente Farbe der **BUTTONGROUP-Bilder** an oder ruft sie ab.

``` syntax
        elementID.transparencyColor
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine  Zeichenfolge mit Lese-/Schreibzugriff ohne Standardwert, die einen der folgenden Werte enthält.



| Wert                                       | BESCHREIBUNG                                                                                        |
|---------------------------------------------|----------------------------------------------------------------------------------------------------|
| Automatisch                                        | Das Pixel an position 0,0 im Bild wird zur transparenten Farbe.                              |
| einen beliebigen Microsoft Internet Explorer-Farbwert | Ein Internet Explorer-Farbwert wird zur transparenten Farbe (z. B. "red" oder " \# FF0000"). |
| Keine                                        | Standard. Keine Transparenz.                                                                          |



 

## <a name="remarks"></a>Hinweise

Eine transparente Farbe in einem Bild ermöglicht, dass alles, was sich hinter dem Bild befindet, durch die Bereiche der Transparenz angezeigt wird. Der transparente Bereich kann angeklickt werden, es sei denn, er wird vom **ClippingImage-Tag** abgeschnitten.

Die Farbe kann ein beliebiger Microsoft Internet Explorer-Farbwert sein. Wenn der Wert Auto ist, wird die Farbe des Pixels an position 0,0 im Bild verwendet.

Wenn die angegebene Farbe keine der gültigen Farben Internet Explorer ist, wird eine Warnung zurückgegeben, und der vorherige Wert wird beibehalten.

Da JPGs verlustbeendet sind und daher unerwarteten Farbwechseln unterliegen, werden sie nicht empfohlen, wenn **transparencyColor** verwendet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**BUTTONGROUP-Element**](buttongroup-element.md)
</dt> <dt>

[**Farbreferenz**](color-reference.md)
</dt> </dl>

 

 





