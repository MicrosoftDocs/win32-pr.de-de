---
title: VIDEO.fullScreen
description: Das fullScreen-Attribut gibt einen Wert an, der angibt, ob das Video im Vollbildmodus angezeigt wird, oder ruft einen Wert ab.
ms.assetid: de74d95a-31a2-4f65-811c-4e8018ee484a
keywords:
- VIDEO.fullScreen-Windows Media Player
topic_type:
- apiref
api_name:
- VIDEO.fullScreen
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8150843ab14148d398b11cba82aa52711621c15962976ca37d5332a6ae58f24
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119465692"
---
# <a name="videofullscreen"></a>VIDEO.fullScreen

Das **fullScreen-Attribut** gibt einen Wert an, der angibt, ob das Video im Vollbildmodus angezeigt wird, oder ruft einen Wert ab.

``` syntax
        elementID.fullScreen
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist ein boolescher Wert mit **Lese-/Schreibzugriff.**



| Wert | BESCHREIBUNG                                          |
|-------|------------------------------------------------------|
| true  | Video wird im Vollbildmodus angezeigt.                  |
| false | Standard. Das Video wird nicht im Vollbildmodus angezeigt. |



 

## <a name="remarks"></a>Hinweise

Diese Eigenschaft kann nur zur Laufzeit angegeben werden, nachdem eine Datei geladen wurde. Sie muss daher innerhalb eines Skriptereignishandlers festgelegt werden. Die Escapeschaltfläche wird verwendet, um zur normalen Anzeige zurückzukehren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**VIDEO-Element**](video-element.md)
</dt> <dt>

[**VIDEO.maintainAspectRatio**](video-maintainaspectratio.md)
</dt> <dt>

[**VIDEO.shrinkToFit**](video-shrinktofit.md)
</dt> <dt>

[**VIDEO.stretchToFit**](video-stretchtofit.md)
</dt> </dl>

 

 





