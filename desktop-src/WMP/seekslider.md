---
title: SeekSlider
description: Dies ist ein vordefinierter Schieberegler mit den folgenden Standardwerten. | SeekSlider
ms.assetid: 9fdb0f70-e5ce-4dbc-aeba-44fa0e2c9b3c
keywords:
- SeekSlider-Fenster Media Player
topic_type:
- apiref
api_name:
- SEEKSLIDER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 59808fa7c41acfcc28b715362b8724c7f113faee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370598"
---
# <a name="seekslider"></a>SeekSlider

Dies ist ein vordefinierter **Schieberegler** mit den folgenden Standardwerten.

``` syntax
toolTip="Seek"
foregroundProgress="wmpprop:player.network.downloadProgress"
max="wmpprop:player.currentMedia.duration"
min="0"
value="wmpprop:player.controls.currentPosition"
onDragEnd="jscript:player.controls.currentPosition=value;"
useForegroundProgress="true"
```

## <a name="remarks"></a>Bemerkungen

Dadurch wird ein **Schieberegler** -Steuerelement erstellt, das die Mediendatei an einer beliebigen Position sucht. Die Quick Infos sind lokalisiert. Alle Eigenschaften dieses **Schiebereglers** können überschrieben werden, indem Sie explizit angegeben werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------|
| Version<br/> | Windows Media Player 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Slider-Element**](slider-element.md)
</dt> </dl>

 

 





