---
title: Ambientattribute. muveto
description: Die Methode "muveto" verschiebt das Steuerelement mit einer linearen Geschwindigkeit an einen neuen Speicherort.
ms.assetid: 8670aa7b-a5c1-4d93-9f48-452bc53e65e6
keywords:
- Ambientattribute. muveto-Fenster Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.moveTo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af481526c0923c527bb14aa4700a6c6fe5ea3613
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358362"
---
# <a name="ambientattributesmoveto"></a>Ambientattribute. muveto

Die Methode " **muveto** " verschiebt das Steuerelement mit einer linearen Geschwindigkeit an einen neuen Speicherort.

``` syntax
        elementID.moveTo(newLeft, newTop, time)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="newLeft"></span><span id="newleft"></span><span id="NEWLEFT"></span>*newleft*
</dt> <dd>

**Number** (**Long**) gibt den neuen Wert für das **linke** Attribut des Steuer Elements an.

</dd> <dt>

<span id="newTop"></span><span id="newtop"></span><span id="NEWTOP"></span>*newtop*
</dt> <dd>

**Number** (**Long**) gibt den neuen Wert für das **Top** -Attribut des Steuer Elements an.

</dd> <dt>

<span id="time"></span><span id="TIME"></span>*Zeit*
</dt> <dd>

**Number** (**Long**) gibt die Zeit in Millisekunden an, die das Steuerelement benötigt, um zum neuen Speicherort zu wechseln.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode ist hilfreich für animierte **unter Ansicht** -Elemente (z. b. wenn der Benutzer auf eine Leiste klickt und die Steuerelemente auf die Folie nach unten klicken).

Diese Methode erstellt eine lineare Bewegung, wenn das Steuerelement verschoben wird. Dies unterscheidet sich von " **diasto**", wodurch eine nichtlineare Bewegung erstellt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ambient-Attribute**](ambient-attributes.md)
</dt> <dt>

[**Ambientattribute. Left**](ambientattributes-left.md)
</dt> <dt>

[**Ambientattribute. slideto**](ambientattributes-slideto.md)
</dt> <dt>

[**AmbientAttributes.top**](ambientattributes-top.md)
</dt> </dl>

 

 





