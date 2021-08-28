---
title: AmbientAttributes.moveTo
description: Die moveTo-Methode verschiebt das Steuerelement mit linearer Geschwindigkeit an eine neue Position.
ms.assetid: 8670aa7b-a5c1-4d93-9f48-452bc53e65e6
keywords:
- AmbientAttributes.moveTo Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.moveTo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf05beedad4fe4abb839e957519384b58102253cd0ab6a292d629df23a7bef98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055048"
---
# <a name="ambientattributesmoveto"></a>AmbientAttributes.moveTo

Die **moveTo-Methode** verschiebt das Steuerelement mit linearer Geschwindigkeit an eine neue Position.

``` syntax
        elementID.moveTo(newLeft, newTop, time)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="newLeft"></span><span id="newleft"></span><span id="NEWLEFT"></span>*newLeft*
</dt> <dd>

**Number** (**long**), die den neuen Wert für das **linke** Attribut des Steuerelements angibt.

</dd> <dt>

<span id="newTop"></span><span id="newtop"></span><span id="NEWTOP"></span>*newTop*
</dt> <dd>

**Number** (**long**), die den neuen Wert für das **oberste** Attribut des Steuerelements angibt.

</dd> <dt>

<span id="time"></span><span id="TIME"></span>*Zeit*
</dt> <dd>

**Number** (**long**), die die Zeit in Millisekunden angibt, die benötigt wird, bis das Steuerelement an seine neue Position verschoben wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Methode ist nützlich für animierte **SUBVIEW-Elemente** (z. B. wenn der Benutzer auf eine Taskleiste klickt und die Steuerelemente nach unten schieben).

Diese Methode erstellt eine lineare Bewegung, wenn das Steuerelement bewegt wird. Dies unterscheidet sich von **slideTo,** wodurch eine nicht lineare Bewegung erstellt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ambient-Attribute**](ambient-attributes.md)
</dt> <dt>

[**AmbientAttributes.left**](ambientattributes-left.md)
</dt> <dt>

[**AmbientAttributes.slideTo**](ambientattributes-slideto.md)
</dt> <dt>

[**AmbientAttributes.top**](ambientattributes-top.md)
</dt> </dl>

 

 





