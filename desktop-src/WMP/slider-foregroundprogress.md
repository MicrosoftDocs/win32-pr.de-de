---
title: SLIDER.foregroundProgress
description: Das foregroundProgress-Attribut gibt die aktuelle Position der Vordergrund-Statusleiste als Prozentsatz des Schiebereglerbereichs an oder ruft sie ab.
ms.assetid: 1218ca5a-445c-441b-aa62-74a184a25c2d
keywords:
- SLIDER.foregroundProgress Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.foregroundProgress
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e48819a2b3245fc8a72d29e9a30135cc37702417ca498c88b8be01578b74988
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119646340"
---
# <a name="sliderforegroundprogress"></a>SLIDER.foregroundProgress

Das **foregroundProgress-Attribut** gibt die aktuelle Position der Vordergrund-Statusleiste als Prozentsatz des Schiebereglerbereichs an oder ruft sie ab.

``` syntax
        elementID.foregroundProgress
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine  Lese-/Schreibnummer **(float)** im Bereich von 0 bis 100.

## <a name="remarks"></a>Hinweise

Dieses Attribut wird hauptsächlich verwendet, um den Downloadfortschritt einer Mediendatei nachzuverfolgen  und gleichzeitig die aktuelle Wiedergabeposition der Datei mithilfe des Value-Attributs nachzuverfolgen. Die Position des Schiebereglers ist auf den Bereich des Vordergrundfortschritts beschränkt. Dies ermöglicht das interaktive Suchen nur innerhalb des verfügbaren Teils einer heruntergeladenen Datei.

Um diese Funktion verwenden zu können, muss das **useForegroundProgress-Attribut** auf TRUE festgelegt werden.

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
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**SLIDER-Element**](slider-element.md)
</dt> <dt>

[**SLIDER.min**](slider-min.md)
</dt> <dt>

[**SLIDER.max**](slider-max.md)
</dt> <dt>

[**SLIDER.useForegroundProgress**](slider-useforegroundprogress.md)
</dt> <dt>

[**SLIDER.value**](slider-value.md)
</dt> </dl>

 

 





