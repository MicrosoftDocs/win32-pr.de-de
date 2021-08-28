---
title: AmbientAttributes.visible
description: Das sichtbare Attribut gibt die Sichtbarkeit für das Steuerelement an oder ruft sie ab.
ms.assetid: 8347d42a-4af1-4ea1-b968-a2ae58278430
keywords:
- AmbientAttributes.visible-Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.visible
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6136bbdba7fe222c16e6185bc2ddfa243c5387443122fb93eb1d6564ad01c956
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124050"
---
# <a name="ambientattributesvisible"></a>AmbientAttributes.visible

Das **sichtbare** Attribut gibt die Sichtbarkeit für das Steuerelement an oder ruft sie ab.

``` syntax
        elementID.visible
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist ein **boolescher** Lese-/Schreib-Wert.



| Wert | BESCHREIBUNG                      |
|-------|----------------------------------|
| true  | Standard. Das Steuerelement ist sichtbar. |
| false | Das Steuerelement ist nicht sichtbar.      |



 

## <a name="remarks"></a>Hinweise

Dieses Attribut eignet sich zum Ausblenden von Steuerelementen, z. B. beim Austauschen einer Pausenschaltfläche für eine Wiedergabeschaltfläche.

Wenn der Wert FALSE ist, ist das Steuerelement nicht sichtbar, und Klickereignisse werden an das steuerelement hinter ihm übergeben. Wenn der Wert TRUE ist, ist das Steuerelement sichtbar und empfängt das Klickereignis selbst.

Der Standardwert für das **AUTOMENU-Element** ist false.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ambient-Attribute**](ambient-attributes.md)
</dt> </dl>

 

 





