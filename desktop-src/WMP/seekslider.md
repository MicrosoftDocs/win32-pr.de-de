---
title: SEEKSLIDER
description: Dies ist ein vordefinierter SLIDER mit den folgenden Standardwerten. | SEEKSLIDER
ms.assetid: 9fdb0f70-e5ce-4dbc-aeba-44fa0e2c9b3c
keywords:
- SEEKSLIDER Windows Media Player
topic_type:
- apiref
api_name:
- SEEKSLIDER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a294eede05ec2b2f0f84e925aa299c9bcb2388ee2151385e48f2c68e6b4c1328
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118833339"
---
# <a name="seekslider"></a>SEEKSLIDER

Dies ist ein vordefinierter **SLIDER** mit den folgenden Standardwerten.

``` syntax
toolTip="Seek"
foregroundProgress="wmpprop:player.network.downloadProgress"
max="wmpprop:player.currentMedia.duration"
min="0"
value="wmpprop:player.controls.currentPosition"
onDragEnd="jscript:player.controls.currentPosition=value;"
useForegroundProgress="true"
```

## <a name="remarks"></a>Hinweise

Dadurch wird ein **SLIDER-Steuerelement** erstellt, das die Mediendatei an eine beliebige Position sucht. Die QuickInfos sind lokalisiert. Alle Eigenschaften dieses **SLIDER können** überschrieben werden, indem sie explizit angegeben werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------|
| Version<br/> | Windows Media Player 7.0 oder höher<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**SLIDER-Element**](slider-element.md)
</dt> </dl>

 

 





