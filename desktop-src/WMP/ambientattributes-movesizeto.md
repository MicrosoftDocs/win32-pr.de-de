---
title: Ambientattribute. muvesizeto
description: Die Methode "muvesizeto" verschiebt das Steuerelement und gibt eine neue Größe für das Steuerelement am neuen Speicherort an. Das-Steuerelement verschiebt und ändert seine Größe im Verlauf des angegebenen Zeitraums auf animierte Weise.
ms.assetid: 89e3bf16-a123-4fb1-8c24-bc22a978e7f6
keywords:
- Media Player "ambientattribute. muvesizeto"
topic_type:
- apiref
api_name:
- AmbientAttributes.moveSizeTo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 406d48772e85a55ab82241518d499182931cc2fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366941"
---
# <a name="ambientattributesmovesizeto"></a>Ambientattribute. muvesizeto

Die Methode " **muvesizeto** " verschiebt das Steuerelement und gibt eine neue Größe für das Steuerelement am neuen Speicherort an. Das-Steuerelement verschiebt und ändert seine Größe im Verlauf des angegebenen Zeitraums auf animierte Weise.

``` syntax
        elementID.moveSizeTo(newX, newY, newWidth, newHeight, moveTime, fSlide)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="newX"></span><span id="newx"></span><span id="NEWX"></span>*newx*
</dt> <dd>

**Number** (**Long**) gibt den neuen Wert für das **linke** Attribut des Steuer Elements an.

</dd> <dt>

<span id="newY"></span><span id="newy"></span><span id="NEWY"></span>*Newy*
</dt> <dd>

**Number** (**Long**) gibt den neuen Wert für das **Top** -Attribut des Steuer Elements an.

</dd> <dt>

<span id="newWidth"></span><span id="newwidth"></span><span id="NEWWIDTH"></span>*neubreite*
</dt> <dd>

**Number** (**Long**) gibt den neuen Wert für das **Width** -Attribut des Steuer Elements an.

</dd> <dt>

<span id="newHeight"></span><span id="newheight"></span><span id="NEWHEIGHT"></span>*netwheight*
</dt> <dd>

**Number** (**Long**) gibt den neuen Wert für das **height** -Attribut des Steuer Elements an.

</dd> <dt>

<span id="moveTime"></span><span id="movetime"></span><span id="MOVETIME"></span>*-Zeit*
</dt> <dd>

**Number** (**Long**) gibt die Zeit in Millisekunden an, die das Steuerelement benötigt, um zum neuen Speicherort zu wechseln.

</dd> <dt>

<span id="fSlide"></span><span id="fslide"></span><span id="FSLIDE"></span>*Folie*
</dt> <dd>

**Boolescher** Wert, der den Typ der beim Verschieben des Steuer Elements erstellten Bewegung angibt.



| Wert | BESCHREIBUNG                                                             |
|-------|-------------------------------------------------------------------------|
| true  | Bewegung ist nicht linear (gleitende Bewegung, die beschleunigt und verlangsamt). |
| false | Bewegung ist linear.                                                       |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die Bewegung des Steuer Elements kann linear oder nicht linear sein. Lineare Bewegung bedeutet, dass das Steuerelement mit konstanter Geschwindigkeit an die neue Position bewegt wird, wobei der Start und das Beenden plötzlich beendet werden. Wenn eine nichtlineare Bewegung angegeben wird, wird eine gleitende Bewegung erstellt, die zu Beginn der Bewegung von NULL beschleunigt und am Ende wieder auf 0 (null) zurückgesetzt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------|
| Version<br/> | Windows Media Player 11<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ambient-Attribute**](ambient-attributes.md)
</dt> <dt>

[**Ambientattribute. Height**](ambientattributes-height.md)
</dt> <dt>

[**Ambientattribute. Left**](ambientattributes-left.md)
</dt> <dt>

[**AmbientAttributes.top**](ambientattributes-top.md)
</dt> <dt>

[**Ambientattribute. Width**](ambientattributes-width.md)
</dt> </dl>

 

 





