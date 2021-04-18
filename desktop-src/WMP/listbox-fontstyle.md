---
title: ListBox. FontStyle
description: Das FontStyle-Attribut gibt den Schrift Schnitt für das Listenfeld-Steuerelement an oder ruft ihn ab.
ms.assetid: c42b80b6-0dea-4080-a06e-931fdc02fa55
keywords:
- ListBox. FontStyle-Fenster Media Player
topic_type:
- apiref
api_name:
- LISTBOX.fontStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0903ac77f1fa4307dfcabad6311eb556617d8153
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364947"
---
# <a name="listboxfontstyle"></a>ListBox. FontStyle

Das **FontStyle** -Attribut gibt den Schrift Schnitt für das Listenfeld-Steuerelement an oder ruft ihn ab.

``` syntax
        elementID.fontStyle
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

Zu Renderingzwecken ist normal der Standard Schriftart Stil. Der Standardwert, der von diesem Attribut abgerufen wird, ist "" (leere Zeichenfolge).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------|
| Version<br/> | Windows Media Player für Windows XP oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ListBox-Element**](listbox-element.md)
</dt> <dt>

[**ListBox. FontSize**](listbox-fontsize.md)
</dt> </dl>

 

 





