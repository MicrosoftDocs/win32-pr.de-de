---
title: Video. Fullscreen
description: Mit dem Fullscreen-Attribut wird ein Wert angegeben oder abgerufen, der angibt, ob das Video im Vollbildmodus angezeigt wird.
ms.assetid: de74d95a-31a2-4f65-811c-4e8018ee484a
keywords:
- Video. Fullscreen-Fenster Media Player
topic_type:
- apiref
api_name:
- VIDEO.fullScreen
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c27fa1bde6437b55689494751410145995862d8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368634"
---
# <a name="videofullscreen"></a>Video. Fullscreen

Mit dem **Fullscreen** -Attribut wird ein Wert angegeben oder abgerufen, der angibt, ob das Video im Vollbildmodus angezeigt wird.

``` syntax
        elementID.fullScreen
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist ein **boolescher** Wert mit Lese-/Schreibzugriff.



| Wert | BESCHREIBUNG                                          |
|-------|------------------------------------------------------|
| true  | Video wird im Vollbildmodus angezeigt.                  |
| false | Standard. Video wird nicht im Vollbildmodus angezeigt. |



 

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft kann nur zur Laufzeit angegeben werden, nachdem eine Datei geladen wurde. Daher muss Sie in einem Skript Ereignishandler festgelegt werden. Die Schaltfläche "Escape" wird verwendet, um zur normalen Anzeige zurückzukehren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Video-Element**](video-element.md)
</dt> <dt>

[**Video. wart AspectRatio**](video-maintainaspectratio.md)
</dt> <dt>

[**Video. ShrinkToFit**](video-shrinktofit.md)
</dt> <dt>

[**Video. stretchdefit**](video-stretchtofit.md)
</dt> </dl>

 

 





