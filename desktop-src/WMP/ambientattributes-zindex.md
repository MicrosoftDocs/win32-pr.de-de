---
title: Ambientattribute. ZIndex
description: Das ZIndex-Attribut gibt die Reihenfolge an, in der das Steuerelement gerendert wird.
ms.assetid: b05c9efc-5d1d-4cba-89f4-b4200ce99e09
keywords:
- Fenster Media Player "ambientattribute. ZIndex"
topic_type:
- apiref
api_name:
- AmbientAttributes.zIndex
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52480cc387c0a9e5e45c4b8e8fd2dae4199dbd16
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372671"
---
# <a name="ambientattributeszindex"></a>Ambientattribute. ZIndex

Das **ZIndex** -Attribut gibt die Reihenfolge an, in der das Steuerelement gerendert wird.

``` syntax
        elementID.zIndex
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Lese-/schreibzahl (**Long**) mit einem Standardwert von 0 (null).  Der Bereich entspricht dem Wert einer langen ganzen Zahl mit Vorzeichen.

## <a name="remarks"></a>Bemerkungen

Die Hintergrund Bitmap einer **Sicht** oder **unter Ansicht** hat einen Fixed z-Index von 0 (null). Wenn Sie möchten, dass ein Steuerelement hinter dem Hintergrund steht, muss der **ZIndex** auf eine negative Zahl festgelegt werden.

Der z-Index einer **Sicht** oder **unter Ansicht** ist ein absoluter Index, während der z-Index eines Steuer Elements relativ zum z-Index der **Sicht** oder **unter Ansicht** ist, in der es enthalten ist.

Das **ZIndex** -Attribut wird vom **Browser** -und **Wiedergabe** Listenelement nicht unterstützt. Es funktioniert nicht mit dem **Video** -Element, wenn es sich um *Video* handelt. **Windows less** ist auf false festgelegt, ebenso wie das **Effects** -Element bei **Effekten**. " **Fenster** " ist auf "true" festgelegt.

**ButtonElement** -Elemente verwenden den **ZIndex** Ihrer **ButtonGroup**.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ambient-Attribute**](ambient-attributes.md)
</dt> </dl>

 

 





