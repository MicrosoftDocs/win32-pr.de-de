---
title: AmbientAttributes.slideTo
description: Die slideTo-Methode verschiebt das Steuerelement an eine neue Position. Das Steuerelement wird im angegebenen Zeitraum nicht linear bewegt.
ms.assetid: 06dd610b-cb58-4b60-9f4b-8929c54c3c33
keywords:
- AmbientAttributes.slideTo Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.slideTo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3f199a2786adbd63313c3f500d589f9f51e2b8ca2fa8120a8fdf75021041115
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119469910"
---
# <a name="ambientattributesslideto"></a>AmbientAttributes.slideTo

Die **slideTo-Methode** verschiebt das Steuerelement an eine neue Position. Das Steuerelement wird im angegebenen Zeitraum nicht linear bewegt.

``` syntax
        elementID.slideTo(newX, newY, moveTime)
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

<span id="moveTime"></span><span id="movetime"></span><span id="MOVETIME"></span>*moveTime*
</dt> <dd>

**Number** (**long**) gibt die Zeit in Millisekunden an, die das Steuerelement benötigt, um an seine neue Position zu wechseln.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Methode ist anders als **moveTo,** das beim Verschieben des Steuerelements eine lineare Bewegung erstellt. Die nicht lineare Bewegung, die von dieser Methode erstellt wird, ist eine gleitende Bewegung, die von einer Geschwindigkeit von 0 (null) am Anfang der Bewegung beschleunigt und am Ende wieder auf 0 (null) zurückgesetzt wird und zu einem reibungslosen Ende kommt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------|
| Version<br/> | Windows Media Player 11<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Ambient-Attribute**](ambient-attributes.md)
</dt> <dt>

[**AmbientAttributes.left**](ambientattributes-left.md)
</dt> <dt>

[**AmbientAttributes.moveTo**](ambientattributes-moveto.md)
</dt> <dt>

[**AmbientAttributes.top**](ambientattributes-top.md)
</dt> </dl>

 

 





