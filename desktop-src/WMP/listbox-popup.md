---
title: ListBox. popUp
description: Das Popup Attribut gibt einen Wert an, der angibt, ob das Element ein popUp-oder Listenfeld-Steuerelement darstellt.
ms.assetid: b0ade23a-6164-4dd4-b599-43ea1fcd44e4
keywords:
- ListBox. popUp-Fenster Media Player
topic_type:
- apiref
api_name:
- LISTBOX.popUp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43d197adbdf2ec27ea6ef7bf04c5c71d15ae923d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372365"
---
# <a name="listboxpopup"></a>ListBox. popUp

Das **Popup** Attribut gibt einen Wert an, der angibt, ob das Element ein popUp-oder Listenfeld-Steuerelement darstellt.

``` syntax
<ELEMENT popUp="value">
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist ein **boolescher** Wert, der nur zur Entwurfszeit angegeben wird.



| Wert | BESCHREIBUNG                                |
|-------|--------------------------------------------|
| true  | Das-Element stellt ein Popup-Steuerelement dar.    |
| false | Das-Element stellt ein Listenfeld-Steuerelement dar. |



 

## <a name="remarks"></a>Bemerkungen

Das **Popup** -Element stellt ein Listenfeld-Steuerelement dar, das nur bei Bedarf angezeigt wird. Sie ist mit dem **ListBox** -Element identisch, außer dem Standardwert dieses Attributs, das das Anzeigeverhalten ändert. Der Standardwert für **ListBox** -Elemente ist false. Für **Popup** Elemente ist der Standardwert true. Anstatt dieses Attribut anzugeben, sollte das **ListBox** -oder **Popup** Element entsprechend dem gewünschten Verhalten verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------|
| Version<br/> | Windows Media Player für Windows XP oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ListBox-Element**](listbox-element.md)
</dt> <dt>

[**Popup-Element**](popup-element.md)
</dt> </dl>

 

 





