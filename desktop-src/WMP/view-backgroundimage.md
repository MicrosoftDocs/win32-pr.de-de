---
title: View. BackgroundImage
description: Das BackgroundImage-Attribut gibt das Hintergrundbild der Ansicht oder unter Ansicht an oder ruft es ab.
ms.assetid: 60ffb257-2f43-4ae3-869d-3eb981ef4ae7
keywords:
- Anzeigen von BackgroundImage-Windows-Media Player
topic_type:
- apiref
api_name:
- VIEW.backgroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e96f4a93882e02589d7f15b74ba5cb225f506d69
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352891"
---
# <a name="viewbackgroundimage"></a>View. BackgroundImage

Das **BackgroundImage** -Attribut gibt das Hintergrundbild der **Ansicht** oder **unter Ansicht** an oder ruft es ab.

``` syntax
        elementID.backgroundImage
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Lese- **/schreibzeichenfolge**.

## <a name="remarks"></a>Bemerkungen

Die unterstützten Formate sind BMP, JPG, GIF und PNG. Wenn es sich bei dem Bild um eine 8-Bit-BMP-Datei handelt, können seine Farbton-und Sättigungswerte mithilfe der **backgroundimagehueshift** -und **backgroundimagesationtribute** -Attribute dynamisch geändert werden.

Wenn Sie in einem Windows Media-Download Paket das **BackgroundImage** -Attribut für ein **Ansichts** Element angeben, müssen Sie auch das **BackgroundColor** -Attribut für dieses Element angeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**View-Element**](view-element.md)
</dt> <dt>

[**View. backgroundimagehueshift**](view-backgroundimagehueshift.md)
</dt> <dt>

[**View. backgroundimagesationations**](view-backgroundimagesaturation.md)
</dt> </dl>

 

 





