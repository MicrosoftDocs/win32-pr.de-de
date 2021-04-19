---
title: View. TitleBar
description: Mit dem TitleBar-Attribut wird ein Wert abgerufen, der angibt, ob die Fenstertitelleiste angezeigt wird.
ms.assetid: 996aa2e0-0313-4a48-adcb-b82f76f38b6a
keywords:
- View. TitleBar-Fenster Media Player
topic_type:
- apiref
api_name:
- VIEW.titleBar
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dea225103913e3906cf6cd3b129943fbf9b9f165
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367638"
---
# <a name="viewtitlebar"></a>View. TitleBar

Mit dem **TitleBar** -Attribut wird ein Wert abgerufen, der angibt, ob die Fenstertitelleiste angezeigt wird.

``` syntax
        elementID.titleBar
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist ein Schreib geschützter **boolescher** Wert.



| Wert | BESCHREIBUNG                             |
|-------|-----------------------------------------|
| true  | Standard. Die Fenstertitelleiste wird angezeigt. |
| false | Die Fenstertitelleiste wird nicht angezeigt.      |



 

## <a name="remarks"></a>Bemerkungen

Wenn die Titelleiste angezeigt wird, werden die Schaltflächen "Kontrollkästchen", "minimieren" und "Schließen" angezeigt. Der Titel des Fensters ist der Titel des **Ansichts** Elements.

Wenn **TitleBar** auf true festgelegt ist und der Benutzer versucht, den Wert von " **Video. Zoom**" zu ändern, wird die Änderung nicht durchgeführt, es sei denn, die Skin überwacht den **Zoom** und führt die entsprechende Aktion aus, um die Größe zu ändern.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**View-Element**](view-element.md)
</dt> <dt>

[**View. Title**](view-title.md)
</dt> <dt>

[**Video. Zoom**](video-zoom.md)
</dt> </dl>

 

 





