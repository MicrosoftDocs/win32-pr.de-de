---
title: BUTTON.transparencyColor
description: Das transparencyColor-Attribut gibt die Farbe an oder ruft sie ab, die in den BUTTON-Bildern transparent ist.
ms.assetid: c22f9965-3118-4c96-8ff5-7fbaa28cbb57
keywords:
- BUTTON.transparencyColor-Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.transparencyColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d51e42b1636958edd772d27c4e5a29720fa0dd87a74784f28f3ffeb7891873c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118840463"
---
# <a name="buttontransparencycolor"></a>BUTTON.transparencyColor

Das **transparencyColor-Attribut** gibt die Farbe an oder ruft sie ab, die in den **BUTTON-Bildern transparent** ist.

``` syntax
        elementID.transparencyColor
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine  Zeichenfolge mit Lese-/Schreibzugriff ohne Standardwert, die einen der folgenden Werte enthält.



| Wert                                    | Beschreibung                                                                                               |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Automatisch                                     | Die Farbe des Pixels an position 0,0 im Bild wird zur transparenten Farbe.                        |
| Beliebiger Internet Explorer Farbformatwert | Ein Internet Explorer Farbformatwert wird zur transparenten Farbe (z. B. "red" oder " \# FF0000"). |
| Keine                                     | Keine Transparenz.                                                                                          |



 

## <a name="remarks"></a>Hinweise

Eine transparente Farbe in einem Bild ermöglicht, dass alles, was sich hinter dem Bild befindet, durch die transparenten Bereiche angezeigt wird. Die **SCHALTFLÄCHE** erhält weiterhin Klicks auf den transparenten Bereich.

Die transparente Farbe kann ein beliebiger Internet Explorer sein. Wenn der Wert des **transparencyColor-Attributs** auf "Auto" festgelegt ist, wird die Farbe des Pixels an position 0,0 im Bild verwendet.

Wenn die angegebene Farbe keine der gültigen IE-Farben ist, wird der vorherige Wert beibehalten.

Da JPGs verlustbeendet sind und daher unerwarteten Farbwechseln unterliegen, werden sie nicht empfohlen, wenn **transparencyColor** verwendet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**BUTTON-Element**](button-element.md)
</dt> <dt>

[**BUTTON.image**](button-image.md)
</dt> <dt>

[**Farbreferenz**](color-reference.md)
</dt> </dl>

 

 





