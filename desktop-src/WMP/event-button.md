---
title: Ereignis. Schaltfläche
description: Mit dem Button-Attribut wird ein Wert abgerufen, der angibt, welche Maustasten beim Eintreten des Ereignisses nicht angezeigt wurden.
ms.assetid: 58fb1522-9946-4942-b4bf-4cff37f7dbaf
keywords:
- Ereignis. Button-Fenster Media Player
topic_type:
- apiref
api_name:
- event.button
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f218c0703bd2847cc0f3b7fb2091bbb02e7863e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365504"
---
# <a name="eventbutton"></a>Ereignis. Schaltfläche

Mit dem **Button** -Attribut wird ein Wert abgerufen, der angibt, welche Maustasten beim Eintreten des Ereignisses nicht angezeigt wurden.

``` syntax
event.button
```

## <a name="possible-values"></a>Mögliche Werte

Bei diesem Attribut handelt es sich um eine schreibgeschützte **Zahl** (**Long**).



| Wert | BESCHREIBUNG                      |
|-------|----------------------------------|
| 0     | Keine Maustasten.      |
| 1     | Die linke Maustaste ist nicht mehr vorhanden.  |
| 2     | Die Rechte Maustaste wurde gedrückt. |
| 3     | Beide Maustasten waren nicht angezeigt.    |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ambient-Ereignis Attribute**](ambient-event-attributes.md)
</dt> </dl>

 

 





