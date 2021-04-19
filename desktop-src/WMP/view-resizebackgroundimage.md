---
title: View. resizebackgroundimage
description: Mit dem resizebackgroundimage-Attribut wird ein Wert angegeben oder abgerufen, der angibt, ob die Größe des Hintergrund Bilds geändert werden kann.
ms.assetid: d18f3def-777f-4a71-961e-73bae98a4c64
keywords:
- View. resizebackgroundimage-Fenster Media Player
topic_type:
- apiref
api_name:
- VIEW.resizeBackgroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 397929d69cc6ac6ad51c29883898c153218afdca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360254"
---
# <a name="viewresizebackgroundimage"></a>View. resizebackgroundimage

Mit dem **resizebackgroundimage** -Attribut wird ein Wert angegeben oder abgerufen, der angibt, ob die Größe des Hintergrund Bilds geändert werden kann.

``` syntax
        elementID.resizeBackgroundImage
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist ein **boolescher** Wert mit Lese-/Schreibzugriff.



| Werte | BESCHREIBUNG                                      |
|--------|--------------------------------------------------|
| true   | Die Größe des Hintergrund Bilds kann geändert werden.             |
| false  | Standard. Die Größe des Hintergrund Bilds kann nicht geändert werden. |



 

## <a name="remarks"></a>Bemerkungen

Wenn Sie dieses Attribut auf "true" festlegen, wird die Größe des Hintergrund Bilds an die aktuellen Werte der Attribute " **Width** " und " **height** " angepasst.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------|
| Version<br/> | Windows Media Player 9-Serie oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**View-Element**](view-element.md)
</dt> <dt>

[**View. BackgroundImage**](view-backgroundimage.md)
</dt> </dl>

 

 





