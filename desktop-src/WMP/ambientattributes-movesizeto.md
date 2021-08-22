---
title: AmbientAttributes.moveSizeTo
description: Die moveSizeTo-Methode verschiebt das Steuerelement und gibt eine neue Größe für das Steuerelement an der neuen Position an. Das Steuerelement wird im angegebenen Zeitraum animiert bewegt und seine Größe geändert.
ms.assetid: 89e3bf16-a123-4fb1-8c24-bc22a978e7f6
keywords:
- AmbientAttributes.moveSizeTo Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.moveSizeTo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 936a6696dfcc99c5a181906eb970f84c7019af7905c466f09e820044f6220271
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119469950"
---
# <a name="ambientattributesmovesizeto"></a>AmbientAttributes.moveSizeTo

Die **moveSizeTo-Methode** verschiebt das Steuerelement und gibt eine neue Größe für das Steuerelement an der neuen Position an. Das Steuerelement wird im angegebenen Zeitraum animiert bewegt und seine Größe geändert.

``` syntax
        elementID.moveSizeTo(newX, newY, newWidth, newHeight, moveTime, fSlide)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="newX"></span><span id="newx"></span><span id="NEWX"></span>*newX*
</dt> <dd>

**Number** (**long**) gibt den neuen Wert für das **linke Attribut** des Steuerelements an.

</dd> <dt>

<span id="newY"></span><span id="newy"></span><span id="NEWY"></span>*newY*
</dt> <dd>

**Number** (**long**) gibt den neuen Wert für das **oberste Attribut** des Steuerelements an.

</dd> <dt>

<span id="newWidth"></span><span id="newwidth"></span><span id="NEWWIDTH"></span>*newWidth*
</dt> <dd>

**Number** (**long**), die den neuen Wert für das **Width-Attribut** des Steuerelements an gibt.

</dd> <dt>

<span id="newHeight"></span><span id="newheight"></span><span id="NEWHEIGHT"></span>*newHeight*
</dt> <dd>

**Zahl** (**long**), die den neuen Wert für das **Height-Attribut** des Steuerelements an gibt.

</dd> <dt>

<span id="moveTime"></span><span id="movetime"></span><span id="MOVETIME"></span>*moveTime*
</dt> <dd>

**Number** (**long**) gibt die Zeit in Millisekunden an, die das Steuerelement benötigt, um an seine neue Position zu wechseln.

</dd> <dt>

<span id="fSlide"></span><span id="fslide"></span><span id="FSLIDE"></span>*fSlide*
</dt> <dd>

**Boolescher Wert,** der den Typ der Bewegung an gibt, die beim Verschieben des Steuerelements erstellt wird.



| Wert | BESCHREIBUNG                                                             |
|-------|-------------------------------------------------------------------------|
| true  | Die Bewegung ist nicht linear (gleitende Bewegung, die beschleunigt und verlangsamt). |
| false | Die Bewegung ist linear.                                                       |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die Bewegung des Steuerelements kann linear oder nicht linear sein. Lineare Bewegung bedeutet, dass das Steuerelement mit konstanter Geschwindigkeit an seine neue Position bewegt wird und plötzlich startet und beendet wird. Wenn eine nicht lineare Bewegung angegeben wird, wird eine gleitende Bewegung erstellt, die von 0 (null) am Anfang der Bewegung beschleunigt und am Ende wieder auf 0 (null) zurückgesetzt wird, was zu einem reibungslosen Ende kommt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------|
| Version<br/> | Windows Media Player 11<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Ambient-Attribute**](ambient-attributes.md)
</dt> <dt>

[**AmbientAttributes.height**](ambientattributes-height.md)
</dt> <dt>

[**AmbientAttributes.left**](ambientattributes-left.md)
</dt> <dt>

[**AmbientAttributes.top**](ambientattributes-top.md)
</dt> <dt>

[**AmbientAttributes.width**](ambientattributes-width.md)
</dt> </dl>

 

 





