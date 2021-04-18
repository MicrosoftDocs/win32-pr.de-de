---
title: Text. BackgroundColor
description: Das BackgroundColor-Attribut gibt die Hintergrundfarbe für das Text Steuerelement an oder ruft diese ab.
ms.assetid: 0c16318f-bf57-4c5f-85c1-46641124d431
keywords:
- Text. BackgroundColor-Fenster Media Player
topic_type:
- apiref
api_name:
- TEXT.backgroundColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bff833fad0b5ad60b49479c57dc51cbe82f48dbd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358274"
---
# <a name="textbackgroundcolor"></a>Text. BackgroundColor

Das **BackgroundColor** -Attribut gibt die Hintergrundfarbe für das Text Steuerelement an oder ruft diese ab.

``` syntax
        elementID.backgroundColor
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Lese- **/schreibzeichenfolge** , die einen beliebigen Microsoft Internet Explorer-Farbwert oder den Wert "None" enthält. Der Standardwert ist "None". Dies bedeutet, dass der Hintergrund transparent ist.

## <a name="remarks"></a>Bemerkungen

Die Hintergrundfarbe wird für die Höhe und Breite des Steuer Elements festgelegt. Wenn Height und Width nicht festgelegt sind, wird die Hintergrundfarbe auf die Höhe und Breite des Texts festgelegt.

Wenn Sie **AlphaBlend** oder **alphablendto** mit einem **Text** Element verwenden, für das keine **BackgroundColor** angegeben ist, wird eine Hintergrundfarbe von Schwarz verwendet. Wenn die Vordergrundfarbe ebenfalls schwarz ist (Dies ist der Standardwert für das **ForegroundColor** -Attribut), wird der Text möglicherweise nicht lesbar. Um dies zu verhindern, geben Sie immer das **BackgroundColor** -Attribut an, oder legen Sie **ForegroundColor** auf eine andere Farbe als schwarz fest.

Im [value](text-value.md) -Attribut finden Sie ein Beispiel, das veranschaulicht, wie die Attribute des **Text** -Elements verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ambientattribute. AlphaBlend**](ambientattributes-alphablend.md)
</dt> <dt>

[**Ambientattribute. alphablendto**](ambientattributes-alphablendto.md)
</dt> <dt>

[**Farb Verweis**](color-reference.md)
</dt> <dt>

[**Text-Element**](text-element.md)
</dt> <dt>

[**Text. ForegroundColor**](text-foregroundcolor.md)
</dt> </dl>

 

 





