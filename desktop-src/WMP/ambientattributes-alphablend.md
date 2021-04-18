---
title: Ambientattribute. AlphaBlend
description: Das AlphaBlend-Attribut gibt einen Wert an, der eine beliebige Ansicht, unter Ansicht oder ein UI-Widget kombiniert, oder ruft diesen ab.
ms.assetid: a6c47d32-a497-4bfa-8fa3-ef94e267d94b
keywords:
- Ambientattribute. AlphaBlend-Fenster Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.alphaBlend
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8c0f0cb9d885f643b39acfbc5148403a5c8b788
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371479"
---
# <a name="ambientattributesalphablend"></a>Ambientattribute. AlphaBlend

Das **AlphaBlend** -Attribut gibt einen Wert an, der eine beliebige **Ansicht**, **unter Ansicht** oder ein UI-Widget kombiniert, oder ruft diesen ab.

``` syntax
        elementID.alphaBlend
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Lese-/schreibzahl (**Long**) mit einem Wert zwischen 0 (keine Deckkraft) und 255 (vollständige Deckkraft) und dem Standardwert 255. 

## <a name="remarks"></a>Bemerkungen

Dieses Attribut ermöglicht, dass ein Element semitransparent angezeigt wird, abhängig von der Menge der festgelegten Deckkraft. Die geringere Deckkraft, desto transparenter wird das Element angezeigt. Jedes Element in der Skin kann über einen separaten Deckkraft Wert verfügen, mit Ausnahme der Schaltflächen Elemente in einem **ButtonGroup** -Steuerelement. Wenn **AlphaBlend** in der **Ansicht** festgelegt ist, wird die Deckkraft der gesamten Skin festgelegt. Alpha Blend funktioniert nicht für Fenster Steuerelemente, einschließlich **Wiedergabeliste**, **Effekten**, **ListBox**, **Popup**, **EditBox** und **Video** (wenn **Windows less** auf false festgelegt ist). Wenn **AlphaBlend** auf **Ansicht** festgelegt wird, wird die gesamte Skin transparent. Die von mehreren Elementen verwendeten **TransparencyColor** -Attribute werden bei **AlphaBlend** nicht unterstützt.

Wenn Sie **AlphaBlend** mit einem **Text** Element verwenden, für das die **BackgroundColor** nicht angegeben ist, wird eine Hintergrundfarbe von Schwarz verwendet. , Wenn die Vordergrundfarbe ebenfalls schwarz ist (Dies ist der Standardwert für *Text*).**ForegroundColor**), wird der Text möglicherweise nicht lesbar. Um dies zu verhindern, geben Sie immer das **BackgroundColor** -Attribut an, oder legen Sie **ForegroundColor** auf eine andere Farbe als schwarz fest.

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

[**Ambientattribute. alphablendto**](ambientattributes-alphablendto.md)
</dt> <dt>

[**Text-Element**](text-element.md)
</dt> <dt>

[**Text. BackgroundColor**](text-backgroundcolor.md)
</dt> <dt>

[**Text. ForegroundColor**](text-foregroundcolor.md)
</dt> </dl>

 

 





