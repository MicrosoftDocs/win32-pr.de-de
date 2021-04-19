---
title: Text. ForegroundColor
description: Das ForegroundColor-Attribut gibt die Textfarbe für das Text Steuerelement an oder ruft diese ab.
ms.assetid: 1ddbad93-fbff-4be6-9797-6594b5f09a1e
keywords:
- Text. ForegroundColor-Fenster Media Player
topic_type:
- apiref
api_name:
- TEXT.foregroundColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e452a18a085337e8cbf0ec88567d6a57a0a498a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356371"
---
# <a name="textforegroundcolor"></a>Text. ForegroundColor

Das **ForegroundColor** -Attribut gibt die Textfarbe für das Text Steuerelement an oder ruft diese ab.

``` syntax
        elementID.foregroundColor
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Lese- **/schreibzeichenfolge** mit einem beliebigen Microsoft Internet Explorer-Farbwert. Der Standardwert ist "schwarz".

Im [value](text-value.md) -Attribut finden Sie ein Beispiel, das veranschaulicht, wie die Attribute des **Text** -Elements verwendet werden.

Wenn Sie **AlphaBlend** oder **alphablendto** mit einem **Text** Element verwenden, für das keine **BackgroundColor** angegeben ist, wird eine Hintergrundfarbe von Schwarz verwendet. Wenn die Vordergrundfarbe ebenfalls schwarz ist (Dies ist der Standardwert für das **ForegroundColor** -Attribut), wird der Text möglicherweise nicht lesbar. Um dies zu verhindern, geben Sie immer das **BackgroundColor** -Attribut an, oder legen Sie **ForegroundColor** auf eine andere Farbe als schwarz fest.

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

[**Text. BackgroundColor**](text-backgroundcolor.md)
</dt> </dl>

 

 





