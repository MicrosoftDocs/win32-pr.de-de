---
title: LISTBOX.fontStyle
description: Das attribut fontStyle gibt den Schriftschnitt für das Listenfeld-Steuerelement an oder ruft den Schriftschnitt ab.
ms.assetid: c42b80b6-0dea-4080-a06e-931fdc02fa55
keywords:
- LISTBOX.fontStyle-Windows Media Player
topic_type:
- apiref
api_name:
- LISTBOX.fontStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 258064ca4ee97fc33bb98bf64d8e3dcf305c5d7e045282a5218a060e904aff50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118575037"
---
# <a name="listboxfontstyle"></a>LISTBOX.fontStyle

Das **attribut fontStyle** gibt den Schriftschnitt für das Listenfeld-Steuerelement an oder ruft den Schriftschnitt ab.

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

[**LISTBOX-Element**](listbox-element.md)
</dt> <dt>

[**LISTBOX.fontSize**](listbox-fontsize.md)
</dt> </dl>

 

 





