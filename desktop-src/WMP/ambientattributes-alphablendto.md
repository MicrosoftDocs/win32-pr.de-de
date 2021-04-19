---
title: Ambientattribute. alphablendto
description: Die alphablendto-Methode passt die AlphaBlend-Eigenschaft über einen Zeitraum an.
ms.assetid: 5cb259bd-3010-4086-be9d-65022be297b7
keywords:
- Ambientattribute. alphablendto Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.alphaBlendTo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 16b21e78de3510e2e4a58c7214995f7888f778c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354103"
---
# <a name="ambientattributesalphablendto"></a>Ambientattribute. alphablendto

Die **alphablendto** -Methode passt die **AlphaBlend** -Eigenschaft über einen Zeitraum an.

``` syntax
        elementID.alphaBlendTo(newVal, alphaTime)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="newVal"></span><span id="newval"></span><span id="NEWVAL"></span>*NewVal*
</dt> <dd>

**Number** (Long), der den neuen Deckkraft Wert angibt. Liegt zwischen 0 (keine Deckkraft) und 255 (vollständige Deckkraft).

</dd> <dt>

<span id="alphaTime"></span><span id="alphatime"></span><span id="ALPHATIME"></span>*Alpha Ativ*
</dt> <dd>

**Number** (**Long**), der die Zeit in Millisekunden angibt, die das-Element zum Ändern der Deckkraft benötigt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode ist nützlich, wenn Elemente allmählich angezeigt oder ausgeblendet werden.

Wenn Sie **alphablendto** mit einem **Text** Element verwenden, für das die **BackgroundColor** nicht angegeben ist, wird eine Hintergrundfarbe von Schwarz verwendet. , Wenn die Vordergrundfarbe ebenfalls schwarz ist (Dies ist der Standardwert für *Text*).**ForegroundColor**), wird der Text möglicherweise nicht lesbar. Um dies zu verhindern, geben Sie immer das **BackgroundColor** -Attribut an, oder legen Sie **ForegroundColor** auf eine andere Farbe als schwarz fest.

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

[**Ambientattribute. AlphaBlend**](ambientattributes-alphablend.md)
</dt> <dt>

[**Text-Element**](text-element.md)
</dt> <dt>

[**Text. BackgroundColor**](text-backgroundcolor.md)
</dt> <dt>

[**Text. ForegroundColor**](text-foregroundcolor.md)
</dt> </dl>

 

 





