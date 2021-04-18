---
title: Video. Zoom
description: Das Zoom Attribut gibt den Prozentsatz an, um den das Video skaliert werden soll.
ms.assetid: 71c0e5a6-f7c4-46cf-a180-083d2926ba20
keywords:
- Video. Zoom-Fenster Media Player
topic_type:
- apiref
api_name:
- VIDEO.zoom
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b989cabcf84244976bda728d12c97697338f742
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354438"
---
# <a name="videozoom"></a>Video. Zoom

Das **Zoom** Attribut gibt den Prozentsatz an, um den das Video skaliert werden soll.

``` syntax
        elementID.zoom
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Lese-/schreibzahl (**Long**), die zwischen 1 und der maximalen Größe liegt, die von der Breite und Höhe des Video Steuer Elements untergebracht wird.  Der Standardwert ist 100.

## <a name="remarks"></a>Bemerkungen

Dieses Attribut kann nicht in Verbindung mit dem **Fullscreen** -Attribut verwendet werden.

Wenn " **Width** " und " **height** " angegeben sind und das resultierende Videofenster größer als das Video ist, das abgespielt wird, kann das Video durch zentrales hochskalieren auf die maximale Größe des Fensters vergrößert werden. Wenn " **Width** " und " **height** " nicht angegeben sind, ist " **Zoom** " auf Werte von 100 oder weniger beschränkt.

Wenn die Eigenschaft **ShrinkToFit** den Wert false hat, ändert sich das Video proportional beim Zoomen, um sich an den verfügbaren Platz anzupassen. Wenn **ShrinkToFit** den Wert true hat, wird das Video verkleinert, damit es in die restriktivste Dimension passt, wobei die ursprünglichen Proportionen beibehalten werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Video-Element**](video-element.md)
</dt> <dt>

[**Video. Fullscreen**](video-fullscreen.md)
</dt> <dt>

[**Video. ShrinkToFit**](video-shrinktofit.md)
</dt> </dl>

 

 





