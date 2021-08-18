---
title: TEXT.hoverFontStyle
description: Das hoverFontStyle-Attribut gibt den für das Text-Steuerelement verwendeten Schriftschnitt an oder ruft ihn ab, wenn der Mauszeiger darüber bewegt wird.
ms.assetid: 77ca8512-6150-4a75-8220-19de3fe9e719
keywords:
- TEXT.hoverFontStyle Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.hoverFontStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d04f2ae8e4231ca89f37a65e591271f2536679da649d1efd22ffc1063c89d17d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134623"
---
# <a name="texthoverfontstyle"></a>TEXT.hoverFontStyle

Das **hoverFontStyle-Attribut** gibt den für das Text-Steuerelement verwendeten Schriftschnitt an oder ruft ihn ab, wenn der Mauszeiger darüber bewegt wird.

``` syntax
        elementID.hoverFontStyle
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

Wenn **hoverFontStyle** nicht angegeben ist, **wird fontStyle** verwendet.

Ein [Beispiel, das](text-value.md) veranschaulicht, wie die Attribute des TEXT-Elements verwendet werden, finden Sie im **Value-Attribut.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**TEXT-Element**](text-element.md)
</dt> <dt>

[**TEXT.fontStyle**](text-fontstyle.md)
</dt> </dl>

 

 





