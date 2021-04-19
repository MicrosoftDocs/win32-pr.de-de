---
title: Wiedergabeliste. BackgroundImage
description: Das BackgroundImage-Attribut gibt das Hintergrundbild an oder ruft es ab.
ms.assetid: d4efa774-d42e-4415-a487-1e858d984075
keywords:
- Wiedergabeliste. BackgroundImage Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.backgroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7eca04f47f6e157d5ede529c47fb6ae65b4333cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369125"
---
# <a name="playlistbackgroundimage"></a>Wiedergabeliste. BackgroundImage

Das **BackgroundImage** -Attribut gibt das Hintergrundbild an oder ruft es ab.

``` syntax
        elementID.backgroundImage
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Lese- **/schreibzeichenfolge** , die den Namen einer Bilddatei enthält. Er besitzt keinen Standardwert.

## <a name="remarks"></a>Bemerkungen

Wenn die Bildhöhe und-Breite kleiner als die Höhe und Breite des **Wiedergabe** Listen Elements sind, wird das Bild gekachelt. Die unterstützten Formate sind BMP, JPG, GIF und PNG.

Das Angeben des Werts "Gradient" für das Hintergrundbild bewirkt, dass der Hintergrund der Wiedergabeliste als Farbverlauf angezeigt wird. Dies bedeutet, dass die Hintergrundfarbe allmählich zwischen der [Wiedergabeliste. BackgroundColor](playlist-backgroundcolor.md) (am oberen Rand des Hintergrunds) und den [Wiedergabelisten. statusColor](playlist-statuscolor.md) -Werten übergeht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher, Windows Media Player 10 für das Farbverlaufs Feature<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Wiedergabelisten Element**](playlist-element.md)
</dt> </dl>

 

 





