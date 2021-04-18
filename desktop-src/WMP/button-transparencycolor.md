---
title: Button. transparendcolor
description: Das TransparencyColor-Attribut gibt die Farbe an, die in den Schaltflächen Bildern transparent sein wird, oder ruft Sie ab.
ms.assetid: c22f9965-3118-4c96-8ff5-7fbaa28cbb57
keywords:
- Button. transparendcycolor-Fenster Media Player
topic_type:
- apiref
api_name:
- BUTTON.transparencyColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 771249ddb070c596dc126b9b0c8c7d04a4b4268f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361032"
---
# <a name="buttontransparencycolor"></a>Button. transparendcolor

Das **TransparencyColor** -Attribut gibt die Farbe an, die in den **Schalt** Flächen Bildern transparent sein wird, oder ruft Sie ab.

``` syntax
        elementID.transparencyColor
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Lese- **/schreibzeichenfolge** ohne den Standardwert, der einen der folgenden Werte enthält.



| Wert                                    | BESCHREIBUNG                                                                                               |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Auto                                     | Die Farbe des Pixels an Position 0, 0 im Bild wird zur transparenten Farbe.                        |
| Ein beliebiger Internet Explorer-Farb Format Wert | Ein Wert für den Internet Explorer-Farb Format wird zur transparenten Farbe (z. b. "Red" oder " \# FF0000"). |
| Keine                                     | Keine Transparenz.                                                                                          |



 

## <a name="remarks"></a>Bemerkungen

Eine transparente Farbe in einem Bild ermöglicht das Anzeigen des Bilds, das über die transparenten Bereiche angezeigt werden soll. Die **Schaltfläche** erhält weiterhin Klicks auf den Bereich transparent.

Die transparente Farbe kann ein beliebiger Internet Explorer-Farbwert sein. Wenn der Wert des **TransparencyColor** -Attributs auf "Auto" festgelegt ist, wird die Farbe des Pixels an Position 0, 0 im Bild verwendet.

Wenn es sich bei der angegebenen Farbe nicht um eine der gültigen IE-Farben handelt, wird der vorherige Wert beibehalten.

Da es sich bei den JPGs um Verlust Verluste handelt und daher unerwartete Farbänderungen unterliegen, werden Sie nicht empfohlen, wenn **transparendcolor** verwendet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Button-Element**](button-element.md)
</dt> <dt>

[**Button. Bild**](button-image.md)
</dt> <dt>

[**Farb Verweis**](color-reference.md)
</dt> </dl>

 

 





