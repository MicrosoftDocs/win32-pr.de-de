---
title: TEXT.disabledFontStyle
description: Das disabledFontStyle-Attribut gibt den für das Text-Steuerelement verwendeten Schriftschnitt an oder ruft ihn ab, wenn er deaktiviert ist.
ms.assetid: d0593fe0-f80d-44a3-b989-e85887465d8a
keywords:
- TEXT.disabledFontStyle Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.disabledFontStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0119139e481eee6673c61f95425eac0a3918d738c3d18278442ba7713718b7bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119507590"
---
# <a name="textdisabledfontstyle"></a>TEXT.disabledFontStyle

Das **disabledFontStyle-Attribut** gibt den für das Text-Steuerelement verwendeten Schriftschnitt an oder ruft ihn ab, wenn er deaktiviert ist.

``` syntax
        elementID.disabledFontStyle
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine  Zeichenfolge mit Lese-/Schreibzugriff, die mindestens einen der folgenden Werte enthält.



| Wert     | Beschreibung           |
|-----------|-----------------------|
| Fett      | Fett formatiert.      |
| Kursiv    | Italischer Schriftschnitt.    |
| Underline | Unterstreichung des Schriftschnitts. |
| Durchgestrichen | Durchstreichen des Schriftschnitts. |
| Normal    | Normaler Schriftschnitt.    |



 

## <a name="remarks"></a>Hinweise

Es kann eine beliebige Kombination der Werte verwendet werden, die durch Leerzeichen getrennt ist. Der Normal-Stil hat Vorrang vor allen anderen Werten, und alle anderen, die zusammen mit Normal angegeben werden, werden ignoriert.

Wenn **disabledFontStyle** nicht angegeben ist, **wird fontStyle** verwendet.

Ein [Beispiel, das](text-value.md) veranschaulicht, wie die Attribute des TEXT-Elements verwendet werden, finden Sie im **Value-Attribut.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**TEXT-Element**](text-element.md)
</dt> <dt>

[**TEXT.fontStyle**](text-fontstyle.md)
</dt> </dl>

 

 





