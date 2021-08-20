---
title: TEXT.toolTip
description: Das ToolTip-Attribut gibt den QuickInfo-Text für das Textsteuerfeld an oder ruft den Text ab.
ms.assetid: 3e275607-e7ff-4424-8310-c628ede22629
keywords:
- TEXT.toolTip-Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.toolTip
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 726337ffb31b86d4eaa3a20a1d922fc622110b647fe9be747e8ae239c4548276
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118831819"
---
# <a name="texttooltip"></a>TEXT.toolTip

Das **ToolTip-Attribut** gibt den QuickInfo-Text für das Textsteuerfeld an oder ruft den Text ab.

``` syntax
        elementID.toolTip
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine  Lese-/Schreibzeichenfolge mit einer maximalen Länge von 1.024 Zeichen. Er besitzt keinen Standardwert.

## <a name="remarks"></a>Hinweise

Wenn dieses Attribut nicht angegeben ist  und der Text im Value-Attribut im Text-Steuerelement abgeschnitten wird oder **wordWrap** auf TRUE  festgelegt ist, zeigt die QuickInfo den vollständigen Text des Wertattributs an.

Wenn dieses Attribut auf "" (leere Zeichenfolge) festgelegt ist, wird keine QuickInfo angezeigt.

Ein [Beispiel, das](text-value.md) veranschaulicht, wie die Attribute des TEXT-Elements verwendet werden, finden Sie im **Value-Attribut.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**TEXT-Element**](text-element.md)
</dt> <dt>

[**TEXT.value**](text-value.md)
</dt> <dt>

[**TEXT.wordWrap**](text-wordwrap.md)
</dt> </dl>

 

 





