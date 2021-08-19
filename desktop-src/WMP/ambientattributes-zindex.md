---
title: AmbientAttributes.zIndex
description: Das zIndex-Attribut gibt die Reihenfolge an, in der das Steuerelement gerendert wird, oder ruft sie ab.
ms.assetid: b05c9efc-5d1d-4cba-89f4-b4200ce99e09
keywords:
- AmbientAttributes.zIndex-Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.zIndex
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c0ebccb050d80371b5865316dd341c8e371d3bfd399d14545b312cf8d265bac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124040"
---
# <a name="ambientattributeszindex"></a>AmbientAttributes.zIndex

Das **zIndex-Attribut** gibt die Reihenfolge an, in der das Steuerelement gerendert wird, oder ruft sie ab.

``` syntax
        elementID.zIndex
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Lese-/Schreibnummer (**long**) mit dem Standardwert 0 (null).  Der Bereich ist der einer langen ganzen Zahl mit Vorzeichen.

## <a name="remarks"></a>Hinweise

Die Hintergrundbitmap einer **VIEW- oder** **SUBVIEW-Ansicht** hat einen festen z-Index von null. Wenn ein Steuerelement hinter dem Hintergrund angezeigt werden soll, muss **zIndex** auf eine negative Zahl festgelegt werden.

Der z-Index einer **VIEW-** oder SUBVIEW-Ansicht ist ein absoluter Index, während der z-Index eines Steuerelements relativ zum z-Index der **VIEW-** oder **SUBVIEW-Ansicht** ist, in der es enthalten ist. 

Das **zIndex-Attribut** wird von den ELEMENTEN **BROWSER** und **PLAYLIST nicht** unterstützt. Es funktioniert nicht mit dem **VIDEO-Element,** wenn *VIDEO*. **windowless ist** auf FALSE festgelegt, und mit dem **EFFECTS-Element,** wenn **EFFECTS**. **windowed** ist auf TRUE festgelegt.

**BUTTONELEMENT-Elemente** verwenden **den zIndex** ihrer **BUTTONGROUP**.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ambient-Attribute**](ambient-attributes.md)
</dt> </dl>

 

 





