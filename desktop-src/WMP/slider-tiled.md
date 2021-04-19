---
title: Schieberegler. Kachel
description: Mit dem gekachelten Attribut wird ein Wert angegeben oder abgerufen, der angibt, ob das Schieberegler-Bild angezeigt wird.
ms.assetid: 159a2972-a0eb-4e43-a083-e124e56782f5
keywords:
- Schieberegler. gekachelte Fenster Media Player
topic_type:
- apiref
api_name:
- SLIDER.tiled
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b1448f496ee45d6c8b01356499b9628c745d69f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369707"
---
# <a name="slidertiled"></a>Schieberegler. Kachel

Mit dem **gekachelten** Attribut wird ein Wert angegeben oder abgerufen, der angibt, ob das Schieberegler-Bild angezeigt wird.

``` syntax
        elementID.tiled
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist ein **boolescher** Wert mit Lese-/Schreibzugriff.



| Wert | BESCHREIBUNG                                                                                 |
|-------|---------------------------------------------------------------------------------------------|
| true  | Standard. Die Bild Bitmap wird wiederholt, bis Sie den gesamten Bereich des Steuer Elements füllt. |
| false | Das Bild wird nicht gekachelt.                                                                |



 

## <a name="remarks"></a>Bemerkungen

Dieses Attribut gilt nur, wenn Sie Vordergrund-und Hintergrundbilder zum Definieren eines Schieberegler-Steuer Elements verwenden. Wenn die Bilder kleiner als der definierte Bereich des Schiebereglers sind und das **Kachel** Attribut auf true festgelegt ist, werden die Bilder so lange wiederholt, bis Sie die gesamte Länge des Steuer Elements auffüllen.

Möglicherweise möchten Sie dieses Attribut zusammen mit dem **BorderSize** -Attribut verwenden. Das **BorderSize** -Attribut ermöglicht es Ihnen, einen Rahmen zu definieren, der während der tiult nicht wiederholt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Slider-Element**](slider-element.md)
</dt> <dt>

[**Slider. BackgroundImage**](slider-backgroundimage.md)
</dt> <dt>

[**Slider. BorderSize**](slider-bordersize.md)
</dt> <dt>

[**Slider. foregroundimage**](slider-foregroundimage.md)
</dt> </dl>

 

 





