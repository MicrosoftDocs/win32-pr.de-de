---
title: TEXT.fontStyle
description: Das fontStyle-Attribut gibt den Schriftschnitt für das Text-Steuerelement an oder ruft es ab.
ms.assetid: 1bb99305-dccc-489d-9a02-7cb306f0d47d
keywords:
- TEXT.fontStyle-Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.fontStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fbdbe021890b3a76fbae3838cbebe958956af82ff468f990fe6fd9e91345a48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119762900"
---
# <a name="textfontstyle"></a>TEXT.fontStyle

Das **fontStyle-Attribut** gibt den Schriftschnitt für das Text-Steuerelement an oder ruft es ab.

``` syntax
        elementID.fontStyle
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine **Zeichenfolge** mit Lese-/Schreibzugriff, die mindestens einen der folgenden Werte enthält.



| Wert     | Beschreibung                 |
|-----------|-----------------------------|
| Fett      | Fetter Schriftschnitt.            |
| Kursiv    | Italischer Schriftschnitt.          |
| Underline | Unterstrichen Sie den Schriftschnitt.       |
| Durchgestrichen | Schriftschnitt mit durchsaarten Zeichen.       |
| Normal    | Standard. Normaler Schriftschnitt. |



 

## <a name="remarks"></a>Hinweise

Jede Kombination der Werte kann verwendet werden, getrennt durch Leerzeichen. Der Normal-Stil hat Vorrang vor allen anderen Werten, und alle anderen werte, die zusammen mit Normal angegeben werden, werden ignoriert.

Ein Beispiel, das veranschaulicht, wie die Attribute des **TEXT-Elements** verwendet werden, finden Sie im [Value-Attribut.](text-value.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**TEXT-Element**](text-element.md)
</dt> </dl>

 

 





