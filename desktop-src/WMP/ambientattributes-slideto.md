---
title: Ambientattribute. slideto
description: Die Methode "diasto" verschiebt das Steuerelement an eine neue Position. Das-Steuerelement bewegt sich im angegebenen Zeitraum nicht linear.
ms.assetid: 06dd610b-cb58-4b60-9f4b-8929c54c3c33
keywords:
- Ambientattribute. slideto Windows-Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.slideTo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: deb214046ace59094b6bd5c362dfa716b9fceb57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371297"
---
# <a name="ambientattributesslideto"></a>Ambientattribute. slideto

Die Methode " **diasto** " verschiebt das Steuerelement an eine neue Position. Das-Steuerelement bewegt sich im angegebenen Zeitraum nicht linear.

``` syntax
        elementID.slideTo(newX, newY, moveTime)
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

<span id="moveTime"></span><span id="movetime"></span><span id="MOVETIME"></span>*-Zeit*
</dt> <dd>

**Number** (**Long**) gibt die Zeit in Millisekunden an, die das Steuerelement benötigt, um zum neuen Speicherort zu wechseln.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode unterscheidet sich von " **muveto**", wodurch beim Verschieben des Steuer Elements eine lineare Bewegung erstellt wird. Die nichtlineare Bewegung, die von dieser Methode erstellt wird, ist eine gleitende Bewegung, die sich am Anfang der Bewegung von einer Geschwindigkeit von NULL beschleunigt und am Ende wieder auf 0 (null) zurücksetzt, um einen Smooth-Vorgang zu beenden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------|
| Version<br/> | Windows Media Player 11<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ambient-Attribute**](ambient-attributes.md)
</dt> <dt>

[**Ambientattribute. Left**](ambientattributes-left.md)
</dt> <dt>

[**Ambientattribute. muveto**](ambientattributes-moveto.md)
</dt> <dt>

[**AmbientAttributes.top**](ambientattributes-top.md)
</dt> </dl>

 

 





