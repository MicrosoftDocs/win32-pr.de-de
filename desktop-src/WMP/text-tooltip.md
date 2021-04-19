---
title: Text. ToolTip
description: Das ToolTip-Attribut gibt den QuickInfo-Text für das Text Steuerelement an oder ruft ihn ab.
ms.assetid: 3e275607-e7ff-4424-8310-c628ede22629
keywords:
- Text. QuickInfo-Fenster Media Player
topic_type:
- apiref
api_name:
- TEXT.toolTip
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b064f2abefd07ec65a82069196b1012561699b62
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372357"
---
# <a name="texttooltip"></a>Text. ToolTip

Das **ToolTip** -Attribut gibt den QuickInfo-Text für das Text Steuerelement an oder ruft ihn ab.

``` syntax
        elementID.toolTip
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Lese- **/schreibzeichenfolge** mit einer maximalen Länge von 1024 Zeichen. Er besitzt keinen Standardwert.

## <a name="remarks"></a>Bemerkungen

Wenn dieses Attribut nicht angegeben wird und der Text im **value** -Attribut im Text Steuerelement abgeschnitten wird, oder wenn **WordWrap** auf true festgelegt ist, wird in der QuickInfo der vollständige Text des **value** -Attributs angezeigt.

Wenn dieses Attribut auf "" (leere Zeichenfolge) festgelegt ist, wird keine QuickInfo angezeigt.

Im [value](text-value.md) -Attribut finden Sie ein Beispiel, das veranschaulicht, wie die Attribute des **Text** -Elements verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Text-Element**](text-element.md)
</dt> <dt>

[**Text. Value**](text-value.md)
</dt> <dt>

[**Text. WordWrap**](text-wordwrap.md)
</dt> </dl>

 

 





