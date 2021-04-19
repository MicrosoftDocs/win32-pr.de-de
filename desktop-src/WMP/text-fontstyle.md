---
title: Text. FontStyle
description: Das FontStyle-Attribut gibt den Schrift Schnitt für das Text Steuerelement an oder ruft ihn ab.
ms.assetid: 1bb99305-dccc-489d-9a02-7cb306f0d47d
keywords:
- Text. FontStyle-Fenster Media Player
topic_type:
- apiref
api_name:
- TEXT.fontStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ab6ddfb3ff31cba50027c010ed10c2129d45134
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369959"
---
# <a name="textfontstyle"></a>Text. FontStyle

Das **FontStyle** -Attribut gibt den Schrift Schnitt für das Text Steuerelement an oder ruft ihn ab.

``` syntax
        elementID.fontStyle
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Lese- **/schreibzeichenfolge** , die einen oder mehrere der folgenden Werte enthält.



| Wert     | BESCHREIBUNG                 |
|-----------|-----------------------------|
| Fett      | Fett Schriftstil.            |
| Kursiv    | Kursiv Schriftstil.          |
| Underline | Unterstreichung der Schriftart.       |
| Durchgestrichen | Stil der Strikeout-Schriftart.       |
| Normal    | Standard. Normaler Schriftart Stil. |



 

## <a name="remarks"></a>Bemerkungen

Eine beliebige Kombination der Werte kann mit Leerzeichen getrennt verwendet werden. Der normale Stil hat Vorrang vor allen anderen Werten, und alle anderen Werte, die zusammen mit normal angegeben werden, werden ignoriert.

Im [value](text-value.md) -Attribut finden Sie ein Beispiel, das veranschaulicht, wie die Attribute des **Text** -Elements verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Text-Element**](text-element.md)
</dt> </dl>

 

 





