---
title: Text. scrollingamount
description: Das scrollingamount-Attribut gibt die Anzahl der Pixel an, die der Text während jeder scrollbewegung bewegt, oder ruft diese ab.
ms.assetid: 46f74531-69dd-4505-8937-5b48b6e9be7b
keywords:
- Text. scrollingamount-Media Player
topic_type:
- apiref
api_name:
- TEXT.scrollingAmount
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66de7bfc6001f10c429d05c480dc315edfe72f76
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356500"
---
# <a name="textscrollingamount"></a>Text. scrollingamount

Das **scrollingamount** -Attribut gibt die Anzahl der Pixel an, die der Text während jeder scrollbewegung bewegt, oder ruft diese ab.

``` syntax
        elementID.scrollingAmount
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine positive Lese-/schreibzahl (**int**) mit einem Standardwert von 6. 

## <a name="remarks"></a>Bemerkungen

Für einen reibungslosen Bildlauf sollte " **scrollingamount** " klein sein. Für schnelles zeichnen mit großen Lücken sollte das **scrollingamount** größer sein. Wenn **Scroll** = "false", wird **scrollingamount** ignoriert.

Im [value](text-value.md) -Attribut finden Sie ein Beispiel, das veranschaulicht, wie die Attribute des **Text** -Elements verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Text-Element**](text-element.md)
</dt> <dt>

[**Text. Scroll**](text-scrolling.md)
</dt> </dl>

 

 





