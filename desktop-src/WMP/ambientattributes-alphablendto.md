---
title: AmbientAttributes.alphaBlendTo
description: Die alphaBlendTo-Methode passt die alphaBlend-Eigenschaft über einen bestimmten Zeitraum an.
ms.assetid: 5cb259bd-3010-4086-be9d-65022be297b7
keywords:
- AmbientAttributes.alphaBlendTo-Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.alphaBlendTo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a8e0e29df897d070cd4d337e27a7f5f7f7e3a86c7f44a784afadb5bc203674ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055228"
---
# <a name="ambientattributesalphablendto"></a>AmbientAttributes.alphaBlendTo

Die **alphaBlendTo-Methode** passt die **alphaBlend-Eigenschaft** über einen bestimmten Zeitraum an.

``` syntax
        elementID.alphaBlendTo(newVal, alphaTime)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="newVal"></span><span id="newval"></span><span id="NEWVAL"></span>*newVal*
</dt> <dd>

**Number** (long) gibt den neuen Deckkraftwert an. Liegt zwischen 0 (keine Deckkraft) und 255 (vollständige Deckkraft).

</dd> <dt>

<span id="alphaTime"></span><span id="alphatime"></span><span id="ALPHATIME"></span>*alphaTime*
</dt> <dd>

**Number** (**long**) gibt die Zeit in Millisekunden an, die das Element benötigt, um die Deckkraft zu ändern.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Methode ist nützlich, um Elemente schrittweise erscheinen oder verschwinden zu lassen.

Wenn Sie **alphaBlendTo mit** einem **TEXT-Element** verwenden, für das **nicht backgroundColor** angegeben ist, wird die Hintergrundfarbe Schwarz verwendet. Wenn die Vordergrundfarbe ebenfalls schwarz ist (dies ist der Standardwert für *TEXT*).**foregroundColor**): Der Text kann möglicherweise nicht mehr gelesen werden. Um dies zu verhindern, geben Sie immer das **backgroundColor-Attribut** an, oder legen Sie **foregroundColor** auf eine andere Farbe als Schwarz fest.

> [!Note]  
> Dieses Attribut wird in Windows 98 nicht unterstützt.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------|
| Version<br/> | Windows Media Player 9-Serie oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ambient-Attribute**](ambient-attributes.md)
</dt> <dt>

[**AmbientAttributes.alphaBlend**](ambientattributes-alphablend.md)
</dt> <dt>

[**TEXT-Element**](text-element.md)
</dt> <dt>

[**TEXT.backgroundColor**](text-backgroundcolor.md)
</dt> <dt>

[**TEXT.foregroundColor**](text-foregroundcolor.md)
</dt> </dl>

 

 





