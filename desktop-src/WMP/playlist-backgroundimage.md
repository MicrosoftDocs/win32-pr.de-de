---
title: PLAYLIST.backgroundImage
description: Das backgroundImage-Attribut gibt das Hintergrundbild an oder ruft es ab.
ms.assetid: d4efa774-d42e-4415-a487-1e858d984075
keywords:
- PLAYLIST.backgroundImage-Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.backgroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b56ddcb42f118a5a672b6678079825b6cb3d6aba5fbdc54953fb566e4222f583
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054248"
---
# <a name="playlistbackgroundimage"></a>PLAYLIST.backgroundImage

Das **backgroundImage-Attribut** gibt das Hintergrundbild an oder ruft es ab.

``` syntax
        elementID.backgroundImage
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine  Zeichenfolge mit Lese-/Schreibzugriff, die den Namen einer Bilddatei enthält. Er besitzt keinen Standardwert.

## <a name="remarks"></a>Hinweise

Wenn die Höhe und Breite des Bilds kleiner als die Höhe und Breite des **PLAYLIST-Elements** ist, wird das Bild gekachelt. Die unterstützten Formate sind BMP, JPG, GIF und PNG.

Das Angeben des Werts "gradient" für das Hintergrundbild bewirkt, dass der Hintergrund der Wiedergabeliste als Farbverlauf angezeigt wird. Dies bedeutet, dass die Hintergrundfarbe allmählich zwischen den [Werten PLAYLIST.backgroundColor](playlist-backgroundcolor.md) (oben im Hintergrund) und [PLAYLIST.statusColor über geht.](playlist-statuscolor.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher Windows Media Player 10 für das Farbverlaufsfeature<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**PLAYLIST-Element**](playlist-element.md)
</dt> </dl>

 

 





