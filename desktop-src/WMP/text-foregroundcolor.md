---
title: TEXT.foregroundColor
description: Das foregroundColor-Attribut gibt die Textfarbe für das Text-Steuerelement an oder ruft sie ab.
ms.assetid: 1ddbad93-fbff-4be6-9797-6594b5f09a1e
keywords:
- TEXT.foregroundColor-Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.foregroundColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b134058fdc39b653982f752f2623c6cd69b192e24e417ac012a02813a38334a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119467070"
---
# <a name="textforegroundcolor"></a>TEXT.foregroundColor

Das **foregroundColor-Attribut** gibt die Textfarbe für das Text-Steuerelement an oder ruft sie ab.

``` syntax
        elementID.foregroundColor
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine **Zeichenfolge** mit Lese-/Schreibzugriff, die einen beliebigen Microsoft Internet Explorer Farbwert enthält. Der Standardwert ist "black".

Ein Beispiel, das veranschaulicht, wie die Attribute des **TEXT-Elements** verwendet werden, finden Sie im [Value-Attribut.](text-value.md)

Wenn Sie **alphaBlend** oder **alphaBlendTo** mit einem **TEXT-Element** verwenden, für das nicht **backgroundColor** angegeben ist, wird eine Hintergrundfarbe von Schwarz verwendet. Wenn die Vordergrundfarbe ebenfalls schwarz ist (der Standardwert für das **foregroundColor-Attribut),** kann ihr Text unlesbar werden. Um dies zu verhindern, geben Sie immer das **backgroundColor-Attribut** an, oder legen Sie **foregroundColor** auf eine andere Farbe als Schwarz fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**AmbientAttributes.alphaBlend**](ambientattributes-alphablend.md)
</dt> <dt>

[**AmbientAttributes.alphaBlendTo**](ambientattributes-alphablendto.md)
</dt> <dt>

[**Farbreferenz**](color-reference.md)
</dt> <dt>

[**TEXT-Element**](text-element.md)
</dt> <dt>

[**TEXT.backgroundColor**](text-backgroundcolor.md)
</dt> </dl>

 

 





