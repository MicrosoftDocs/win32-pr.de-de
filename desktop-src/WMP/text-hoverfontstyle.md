---
title: Text. hoverfontstyle
description: Das hoverfontstyle-Attribut gibt den Schriftart Stil an, der für das Text Steuerelement verwendet wird, wenn mit dem Mauszeiger darauf gezeigt wird, oder ruft ihn ab.
ms.assetid: 77ca8512-6150-4a75-8220-19de3fe9e719
keywords:
- Text. hoverfontstyle-Fenster Media Player
topic_type:
- apiref
api_name:
- TEXT.hoverFontStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebaeed6d9701b6e81ac91bc5292dc5b431aa70d7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369458"
---
# <a name="texthoverfontstyle"></a>Text. hoverfontstyle

Das **hoverfontstyle** -Attribut gibt den Schriftart Stil an, der für das Text Steuerelement verwendet wird, wenn mit dem Mauszeiger darauf gezeigt wird, oder ruft ihn ab.

``` syntax
        elementID.hoverFontStyle
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Lese- **/schreibzeichenfolge** , die einen oder mehrere der folgenden Werte enthält.



| Wert     | BESCHREIBUNG           |
|-----------|-----------------------|
| Fett      | Fett Schriftstil.      |
| Kursiv    | Kursiv Schriftstil.    |
| Underline | Unterstreichung der Schriftart. |
| Durchgestrichen | Stil der Strikeout-Schriftart. |
| Normal    | Normaler Schriftart Stil.    |



 

## <a name="remarks"></a>Bemerkungen

Eine beliebige Kombination der Werte kann mit Leerzeichen getrennt verwendet werden. Der normale Stil hat Vorrang vor allen anderen Werten, und alle anderen Werte, die zusammen mit normal angegeben werden, werden ignoriert.

Wenn **hoverfontstyle** nicht angegeben ist, wird **FontStyle** verwendet.

Im [value](text-value.md) -Attribut finden Sie ein Beispiel, das veranschaulicht, wie die Attribute des **Text** -Elements verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Text-Element**](text-element.md)
</dt> <dt>

[**Text. FontStyle**](text-fontstyle.md)
</dt> </dl>

 

 





