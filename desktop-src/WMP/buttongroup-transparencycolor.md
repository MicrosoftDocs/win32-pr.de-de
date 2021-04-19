---
title: ButtonGroup. TransparencyColor
description: Das TransparencyColor-Attribut gibt die transparente Farbe der ButtonGroup-Bilder an oder ruft diese ab.
ms.assetid: 604c5b29-50b9-4df6-9e48-488bf4fb7227
keywords:
- ButtonGroup. TransparencyColor-Fenster Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.transparencyColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbaf6fb70db7d2699a63eb7b4fd34009f7b8ba75
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373693"
---
# <a name="buttongrouptransparencycolor"></a>ButtonGroup. TransparencyColor

Das **TransparencyColor** -Attribut gibt die transparente Farbe der **ButtonGroup** -Bilder an oder ruft diese ab.

``` syntax
        elementID.transparencyColor
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Lese- **/schreibzeichenfolge** ohne Standardwert, der einen der folgenden Werte enthält.



| Wert                                       | BESCHREIBUNG                                                                                        |
|---------------------------------------------|----------------------------------------------------------------------------------------------------|
| Auto                                        | Das Pixel an Position 0, 0 im Bild wird zur transparenten Farbe.                              |
| Jeder Microsoft Internet Explorer-Farbwert | Ein Internet Explorer-Farbwert wird zur transparenten Farbe (z. b. "Red" oder " \# FF0000"). |
| Keine                                        | Standard. Keine Transparenz.                                                                          |



 

## <a name="remarks"></a>Bemerkungen

Eine transparente Farbe in einem Bild ermöglicht, dass alle hinter dem Bild liegenden Bereiche durch die Transparenz Bereiche angezeigt werden. Der transparente Bereich ist klickbar, es sei denn, er wurde durch das **clippingimage** -Tag abgeschnitten.

Die Farbe kann jeder beliebige Microsoft Internet Explorer-Farbwert sein. Wenn der Wert Auto ist, wird die Farbe des Pixels an Position 0, 0 im Bild verwendet.

Wenn es sich bei der angegebenen Farbe nicht um eine der gültigen Internet Explorer-Farben handelt, wird eine Warnung zurückgegeben, und der vorherige Wert wird beibehalten.

Da es sich bei den JPGs um Verlust Verluste handelt und daher unerwartete Farbänderungen unterliegen, werden Sie nicht empfohlen, wenn **transparendcolor** verwendet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ButtonGroup-Element**](buttongroup-element.md)
</dt> <dt>

[**Farb Verweis**](color-reference.md)
</dt> </dl>

 

 





