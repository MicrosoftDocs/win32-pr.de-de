---
title: VIEW.backgroundImage
description: Das backgroundImage-Attribut gibt das Hintergrundbild der VIEW- oder SUBVIEW-Ansicht an oder ruft es ab.
ms.assetid: 60ffb257-2f43-4ae3-869d-3eb981ef4ae7
keywords:
- VIEW.backgroundImage-Windows Media Player
topic_type:
- apiref
api_name:
- VIEW.backgroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1de8bcbd0eb47f03aaff46b4292a8afe226ca8a221ec570537351af8e509801
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119761740"
---
# <a name="viewbackgroundimage"></a>VIEW.backgroundImage

Das **backgroundImage-Attribut** gibt das Hintergrundbild von **VIEW** oder SUBVIEW an oder ruft **es ab.**

``` syntax
        elementID.backgroundImage
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Zeichenfolge mit **Lese-/Schreibzugriff.**

## <a name="remarks"></a>Hinweise

Die unterstützten Formate sind BMP, JPG, GIF und PNG. Wenn es sich bei dem Bild um eine 8-Bit-BMP-Datei handelt, können die Farbton- und Sättigungswerte mithilfe der Attribute **backgroundImageHueShift** und **backgroundImageSaturation** dynamisch geändert werden.

Wenn Sie in Windows Mediendownloadpaket das **backgroundImage-Attribut** für ein **VIEW-Element** angeben, müssen Sie auch das **backgroundColor-Attribut** für dieses Element angeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**VIEW-Element**](view-element.md)
</dt> <dt>

[**VIEW.backgroundImageHueShift**](view-backgroundimagehueshift.md)
</dt> <dt>

[**VIEW.backgroundImageSaturation**](view-backgroundimagesaturation.md)
</dt> </dl>

 

 





