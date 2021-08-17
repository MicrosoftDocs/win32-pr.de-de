---
title: SLIDER.tiled
description: Das gekachelte Attribut gibt einen Wert an, der angibt, ob das Schiebereglerbild gekachelt wird, oder ruft einen Wert ab.
ms.assetid: 159a2972-a0eb-4e43-a083-e124e56782f5
keywords:
- SLIDER.tiled Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.tiled
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a97be7ee857574b24585ffd7ffd9b63acdfad0a37762445699daa3a06f94e97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118832536"
---
# <a name="slidertiled"></a>SLIDER.tiled

Das **gekachelte** Attribut gibt einen Wert an, der angibt, ob das Schiebereglerbild gekachelt wird, oder ruft einen Wert ab.

``` syntax
        elementID.tiled
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist ein boolescher Wert mit **Lese-/Schreibzugriff.**



| Wert | BESCHREIBUNG                                                                                 |
|-------|---------------------------------------------------------------------------------------------|
| true  | Standard. Die Bildbitmap wird wiederholt, bis sie den gesamten Bereich des Steuerelements ausfüllt. |
| false | Das Bild wird nicht gekachelt.                                                                |



 

## <a name="remarks"></a>Hinweise

Dieses Attribut gilt nur, wenn Sie Vordergrund- und Hintergrundbilder verwenden, um ein Schieberegler-Steuerelement zu definieren. Wenn die Bilder kleiner als der definierte Bereich  des Schiebereglers sind und das gekachelte Attribut auf TRUE festgelegt ist, werden die Bilder wiederholt, bis sie die gesamte Länge des Steuerelements ausfüllen.

Sie können dieses Attribut in Verbindung mit dem **borderSize-Attribut** verwenden. Mit **dem BorderSize-Attribut** können Sie einen Rahmen definieren, der während des Kachelns nicht wiederholt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**SLIDER-Element**](slider-element.md)
</dt> <dt>

[**SLIDER.backgroundImage**](slider-backgroundimage.md)
</dt> <dt>

[**SLIDER.borderSize**](slider-bordersize.md)
</dt> <dt>

[**SLIDER.foregroundImage**](slider-foregroundimage.md)
</dt> </dl>

 

 





