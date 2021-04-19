---
title: Ambientattribute. Visible
description: Das Visible-Attribut gibt die Sichtbarkeit für das Steuerelement an oder ruft Sie ab.
ms.assetid: 8347d42a-4af1-4ea1-b968-a2ae58278430
keywords:
- Ambientattribute. Visible Windows-Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.visible
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72794b7bbba0237a687dc70bda761c505b839e59
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369205"
---
# <a name="ambientattributesvisible"></a>Ambientattribute. Visible

Das **Visible** -Attribut gibt die Sichtbarkeit für das Steuerelement an oder ruft Sie ab.

``` syntax
        elementID.visible
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist ein **boolescher** Wert mit Lese-/Schreibzugriff.



| Wert | BESCHREIBUNG                      |
|-------|----------------------------------|
| true  | Standard. Das Steuerelement ist sichtbar. |
| false | Das Steuerelement ist nicht sichtbar.      |



 

## <a name="remarks"></a>Bemerkungen

Dieses Attribut ist nützlich zum Ausblenden von Steuerelementen, z. b. beim Austauschen einer Pause-Schaltfläche für eine Wiedergabe Schaltfläche.

Wenn der Wert false ist, ist das Steuerelement nicht sichtbar, und die Click-Ereignisse werden an das dahinter liegende Steuerelement übermittelt. Wenn der Wert true ist, ist das Steuerelement sichtbar und empfängt das Click-Ereignis selbst.

Der Standardwert für das **automenu** -Element ist false.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ambient-Attribute**](ambient-attributes.md)
</dt> </dl>

 

 





