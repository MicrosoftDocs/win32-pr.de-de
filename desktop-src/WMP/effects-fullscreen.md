---
title: Effekte. Fullscreen
description: Das Fullscreen-Attribut gibt einen Wert an, der angibt, ob die aktuelle Visualisierung voll Bildschirm angezeigt wird, oder ruft diesen ab. Dieses Attribut kann nur zur Laufzeit festgelegt werden.
ms.assetid: 319b46a4-b6c2-4dda-8285-f12af6836b25
keywords:
- Effekte. Fullscreen-Fenster Media Player
topic_type:
- apiref
api_name:
- EFFECTS.fullScreen
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64e1824e35793a083eb88ea42de0eb8858a4b76f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362102"
---
# <a name="effectsfullscreen"></a>Effekte. Fullscreen

Das **Fullscreen** -Attribut gibt einen Wert an, der angibt, ob die aktuelle Visualisierung voll Bildschirm angezeigt wird, oder ruft diesen ab. Dieses Attribut kann nur zur Laufzeit festgelegt werden.

``` syntax
        elementID.fullScreen
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist ein **boolescher** Wert mit Lese-/Schreibzugriff.



| Wert | BESCHREIBUNG                                          |
|-------|------------------------------------------------------|
| true  | Die Visualisierung wird voll Bildschirm angezeigt.              |
| false | Standard. Die Visualisierung wird nicht im Vollbildmodus angezeigt. |



 

## <a name="remarks"></a>Bemerkungen

Eine Visualisierung kann nur dann in den Vollbildmodus versetzt werden, wenn Medien wiedergegeben oder angehalten werden. Wenn *Player*. **currentMedia** ist ein Video, ein Video-Plug-in muss vorhanden sein. Wenn es sich um Audiodaten handelt, muss ein Visualisierungs-Plug-in vorhanden sein, das die voll Bild Anzeige unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Effects-Element**](effects-element.md)
</dt> </dl>

 

 





