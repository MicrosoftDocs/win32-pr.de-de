---
title: PLAYLIST.dropDownImage
description: Das dropDownImage-Attribut gibt den Namen des Bilds an, das für die Dropdownlistenschaltfläche verwendet wird, die am rechten Rand der Dropdownliste angezeigt wird, oder ruft diesen ab.
ms.assetid: 92454a8a-1688-4b5d-887d-6847f4232d87
keywords:
- PLAYLIST.dropDownImage Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.dropDownImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3173462cc7b055639a685917b87f1560adf5eabc8d0d7678788fa6a6c72129d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054208"
---
# <a name="playlistdropdownimage"></a>PLAYLIST.dropDownImage

Das **dropDownImage-Attribut** gibt den Namen des Bilds an, das für die Dropdownlistenschaltfläche verwendet wird, die am rechten Rand der Dropdownliste angezeigt wird, oder ruft diesen ab.

``` syntax
        elementID.dropDownImage
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine **Zeichenfolge** mit Lese-/Schreibzugriff, die den Namen einer Bilddatei enthält. Er besitzt keinen Standardwert.

## <a name="remarks"></a>Hinweise

Dieses Attribut unterstützt PNG-, JPG-, BMP- und GIF-Dateien. Wenn es sich bei dem Bild um eine 8-Bit-BMP-Datei handelt, können die Farbton- und Sättigungswerte mithilfe der Attribute **hueShift** und **saturation** dynamisch geändert werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------|
| Version<br/> | Windows Media Player 9er Serie oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**PLAYLIST-Element**](playlist-element.md)
</dt> <dt>

[**PLAYLIST.dropDownBackgroundImage**](playlist-dropdownbackgroundimage.md)
</dt> <dt>

[**PLAYLIST.hueShift**](playlist-hueshift.md)
</dt> <dt>

[**PLAYLIST.saturation**](playlist-saturation.md)
</dt> </dl>

 

 





