---
title: LISTBOX.popUp
description: Das popUp-Attribut gibt einen Wert an, der angibt, ob das Element ein Popup- oder Listenfeld-Steuerelement darstellt.
ms.assetid: b0ade23a-6164-4dd4-b599-43ea1fcd44e4
keywords:
- LISTBOX.popUp-Windows Media Player
topic_type:
- apiref
api_name:
- LISTBOX.popUp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a755a4fc8f5e1451ee118f718a9b6618e75875789faef7318164f7f2add2069
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996440"
---
# <a name="listboxpopup"></a>LISTBOX.popUp

Das **popUp-Attribut** gibt einen Wert an, der angibt, ob das Element ein Popup- oder Listenfeld-Steuerelement darstellt.

``` syntax
<ELEMENT popUp="value">
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist ein **boolescher Wert,** der nur zur Entwurfszeit angegeben wird.



| Wert | BESCHREIBUNG                                |
|-------|--------------------------------------------|
| true  | Das -Element stellt ein Popupsteuerelement dar.    |
| false | Das -Element stellt ein Listenfeld-Steuerelement dar. |



 

## <a name="remarks"></a>Hinweise

Das **POPUP-Element** stellt ein Listenfeld-Steuerelement dar, das nur bei Bedarf angezeigt wird. Sie ist mit dem **LISTBOX-Element** identisch, mit Ausnahme des Standardwerts dieses Attributs, das das Anzeigeverhalten ändert. Für **LISTBOX-Elemente** ist der Standardwert FALSE. Für **POPUP-Elemente** ist der Standardwert TRUE. Anstatt dieses Attribut anzugeben, sollte das **LISTBOX-** oder **POPUP-Element** gemäß dem gewünschten Verhalten für verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------|
| Version<br/> | Windows Media Player für Windows XP oder höher<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**LISTBOX-Element**](listbox-element.md)
</dt> <dt>

[**POPUP-Element**](popup-element.md)
</dt> </dl>

 

 





