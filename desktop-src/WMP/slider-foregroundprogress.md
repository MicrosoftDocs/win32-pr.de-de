---
title: Schieberegler. foregroundprogress
description: Das foregroundprogress-Attribut gibt die aktuelle Position der Statusanzeige im Vordergrund als Prozentsatz des Schieberegler-Bereichs an oder ruft diese ab.
ms.assetid: 1218ca5a-445c-441b-aa62-74a184a25c2d
keywords:
- Schieberegler. foregroundprogress Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.foregroundProgress
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4597630453444564411d0bcfad8dc6b39914d13
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373894"
---
# <a name="sliderforegroundprogress"></a>Schieberegler. foregroundprogress

Das **foregroundprogress** -Attribut gibt die aktuelle Position der Statusanzeige im Vordergrund als Prozentsatz des Schieberegler-Bereichs an oder ruft diese ab.

``` syntax
        elementID.foregroundProgress
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Lese-/schreibnummer (**float**) im Bereich von 0 bis 100. 

## <a name="remarks"></a>Bemerkungen

Dieses Attribut wird hauptsächlich verwendet, um den Download Fortschritt einer Mediendatei zu verfolgen, während gleichzeitig die aktuelle Wiedergabe Position der Datei mithilfe des **value** -Attributs nachverfolgt wird. Die Position des Zieh Punkts für den Schieberegler ist auf den Bereich des Vordergrund Fortschritts beschränkt. Dadurch wird die interaktive Suche nur innerhalb des verfügbaren Teils einer Downloaddatei ermöglicht.

Um diese Funktion verwenden zu können, muss das **useforegroundprogress** -Attribut auf "true" festgelegt werden.

## <a name="examples"></a>Beispiele


```C++
<SLIDER
  id="seek"
  backgroundColor="blue"
  foregroundColor="red"
  thumbImage="seekthumb.bmp"
  min="0"
  max="wmpprop:player.currentMedia.duration"
  value="wmpprop:player.controls.currentPosition"
  useForegroundProgress="true"
  foregroundProgress="wmpprop:player.network.downloadProgress"
  ondragend="player.controls.currentposition=value"
/>

```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Slider-Element**](slider-element.md)
</dt> <dt>

[**Schieberegler. min.**](slider-min.md)
</dt> <dt>

[**Schieberegler. Max**](slider-max.md)
</dt> <dt>

[**Schieberegler. useforegroundprogress**](slider-useforegroundprogress.md)
</dt> <dt>

[**Slider. Wert**](slider-value.md)
</dt> </dl>

 

 





