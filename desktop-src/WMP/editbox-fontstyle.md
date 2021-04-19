---
title: EditBox. FontStyle
description: Das FontStyle-Attribut gibt den Schrift Schnitt für das Bearbeitungsfeld-Steuerelement an oder ruft ihn ab.
ms.assetid: bc71359d-2b75-4134-99e8-52b2ca48dcde
keywords:
- EditBox. FontStyle-Fenster Media Player
topic_type:
- apiref
api_name:
- EDITBOX.fontStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4249f6224099c3d2a36a3b26244c9b804be519c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356328"
---
# <a name="editboxfontstyle"></a>EditBox. FontStyle

Das **FontStyle** -Attribut gibt den Schrift Schnitt für das Bearbeitungsfeld-Steuerelement an oder ruft ihn ab.

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

[**EditBox-Element**](editbox-element.md)
</dt> <dt>

[**EditBox. fontface**](editbox-fontface.md)
</dt> <dt>

[**EditBox. FontSize**](editbox-fontsize.md)
</dt> </dl>

 

 





