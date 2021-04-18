---
title: Text. Scroll
description: Mit dem Scroll-Attribut wird ein Wert angegeben oder abgerufen, der angibt, ob der Text durch einen Bildlauf
ms.assetid: 1cd5cb4e-673f-4273-91ff-50165c2b08fa
keywords:
- Text. Scrollfenster Media Player
topic_type:
- apiref
api_name:
- TEXT.scrolling
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fdbb80b2033d542da4894172d58451ed5da224f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368555"
---
# <a name="textscrolling"></a>Text. Scroll

Mit dem **Scroll** -Attribut wird ein Wert angegeben oder abgerufen, der angibt, ob der Text durch einen Bildlauf

``` syntax
        elementID.scrolling
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist ein **boolescher** Wert mit Lese-/Schreibzugriff.



| Wert | BESCHREIBUNG                     |
|-------|---------------------------------|
| true  | Scrollen ist aktiviert.           |
| false | Standard. Der Bildlauf ist deaktiviert. |



 

## <a name="remarks"></a>Bemerkungen

Die Scrollfunktion stellt einen Puffer mit zwei Leerzeichen zwischen dem Ende des Texts und dem Anfang der wiederholten Zeile bereit.

Das Attribut " **Begründung** " gibt an, wo der Text zuerst vor dem Scrollen angezeigt wird.

Im [value](text-value.md) -Attribut finden Sie ein Beispiel, das veranschaulicht, wie die Attribute des **Text** -Elements verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Text-Element**](text-element.md)
</dt> <dt>

[**Text. Begründung**](text-justification.md)
</dt> <dt>

[**Text. scrollingamount**](text-scrollingamount.md)
</dt> <dt>

[**Text. scrollingdelay**](text-scrollingdelay.md)
</dt> <dt>

[**Text. scrollingdirection**](text-scrollingdirection.md)
</dt> </dl>

 

 





