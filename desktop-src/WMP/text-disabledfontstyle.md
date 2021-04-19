---
title: Text. disabledfontstyle
description: Das disabledfontstyle-Attribut gibt den Schriftart Stil an, der für das Text Steuerelement verwendet wird, wenn er deaktiviert ist, oder ruft ihn ab.
ms.assetid: d0593fe0-f80d-44a3-b989-e85887465d8a
keywords:
- Text. disabledfontstyle-Fenster Media Player
topic_type:
- apiref
api_name:
- TEXT.disabledFontStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 563ab039a5eae00324f3a810c7d32f08729629b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372576"
---
# <a name="textdisabledfontstyle"></a>Text. disabledfontstyle

Das **disabledfontstyle** -Attribut gibt den Schriftart Stil an, der für das Text Steuerelement verwendet wird, wenn er deaktiviert ist, oder ruft ihn ab.

``` syntax
        elementID.disabledFontStyle
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

Wenn **disabledfontstyle** nicht angegeben wird, wird **FontStyle** verwendet.

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

 

 





