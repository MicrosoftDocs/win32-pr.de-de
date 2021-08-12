---
title: EDITBOX.fontStyle
description: Das attribut fontStyle gibt den Schriftschnitt für das Bearbeitungsfeld-Steuerelement an oder ruft den Schriftschnitt ab.
ms.assetid: bc71359d-2b75-4134-99e8-52b2ca48dcde
keywords:
- EDITBOX.fontStyle-Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.fontStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65d9dc5ac5fe3750fb3a6af8658a5ddb30274764cc891438162434a44651322a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118578846"
---
# <a name="editboxfontstyle"></a>EDITBOX.fontStyle

Das **attribut fontStyle** gibt den Schriftschnitt für das Bearbeitungsfeld-Steuerelement an oder ruft den Schriftschnitt ab.

``` syntax
        elementID.fontStyle
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine **Zeichenfolge** mit Lese-/Schreibzugriff, die mindestens einen der folgenden Werte enthält.



| Wert     | Beschreibung           |
|-----------|-----------------------|
| Fett      | Fetter Schriftschnitt.      |
| Kursiv    | Italischer Schriftschnitt.    |
| Underline | Unterstrichen Sie den Schriftschnitt. |
| Durchgestrichen | Schriftschnitt mit durchsaarten Zeichen. |
| Normal    | Normaler Schriftschnitt.    |



 

## <a name="remarks"></a>Hinweise

Jede Kombination der Werte kann verwendet werden, getrennt durch Leerzeichen. Der Normal-Stil hat Vorrang vor allen anderen Werten, und alle anderen werte, die zusammen mit Normal angegeben werden, werden ignoriert.

Zu Renderingzwecken ist Normal der Standardschriftstil. Der Standardwert, der von diesem Attribut abgerufen wird, ist "" (leere Zeichenfolge).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------|
| Version<br/> | Windows Media Player für Windows XP oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EDITBOX-Element**](editbox-element.md)
</dt> <dt>

[**EDITBOX.fontFace**](editbox-fontface.md)
</dt> <dt>

[**EDITBOX.fontSize**](editbox-fontsize.md)
</dt> </dl>

 

 





