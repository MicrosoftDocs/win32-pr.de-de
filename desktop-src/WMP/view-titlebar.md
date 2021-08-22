---
title: VIEW.titleBar
description: Das titleBar-Attribut ruft einen Wert ab, der angibt, ob die Fenstertitelleiste angezeigt wird.
ms.assetid: 996aa2e0-0313-4a48-adcb-b82f76f38b6a
keywords:
- VIEW.titleBar Windows Media Player
topic_type:
- apiref
api_name:
- VIEW.titleBar
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb05550c22c342d14690f24f42c62a3af328eae65201b8138e82a7a33bf99fb9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054068"
---
# <a name="viewtitlebar"></a>VIEW.titleBar

Das **titleBar-Attribut** ruft einen Wert ab, der angibt, ob die Fenstertitelleiste angezeigt wird.

``` syntax
        elementID.titleBar
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist ein schreibgeschützter **boolescher** Wert.



| Wert | BESCHREIBUNG                             |
|-------|-----------------------------------------|
| true  | Standard. Die Titelleiste des Fensters wird angezeigt. |
| false | Die Titelleiste des Fensters wird nicht angezeigt.      |



 

## <a name="remarks"></a>Hinweise

Wenn die Titelleiste angezeigt wird, werden die Schaltflächen "Steuerelement", "Minimieren" und "Schließen" angezeigt. Der Titel des Fensters ist der Titel des **VIEW-Elements.**

Wenn **titleBar** auf TRUE festgelegt ist und der Benutzer versucht, den Wert von **Video.zoom** zu ändern, erfolgt die Änderung nur dann, wenn die Skin den **Zoom** überwacht und die Größe selbst entsprechend ändert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**VIEW-Element**](view-element.md)
</dt> <dt>

[**VIEW.title**](view-title.md)
</dt> <dt>

[**VIDEO.zoom**](video-zoom.md)
</dt> </dl>

 

 





