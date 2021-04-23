---
description: Das Effect-Element definiert ein Audio- oder Videoeffektobjekt. Ein Effekt wird auf einen einzelnen Stream angewendet (z. B. eine Komposition, ein Titel oder eine Quelle).
ms.assetid: aedb4491-f1f0-44b3-ad88-3fac8c90144d
title: effect-Element (Gdipluseffects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4c925e61578857415bb22248a9ad2b1df27cdac
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908658"
---
# <a name="effect-element"></a>effect-Element

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Das `effect` -Element definiert ein Audio- oder Videoeffektobjekt. Ein Effekt wird auf einen einzelnen Stream angewendet (z. B. eine Komposition, ein Titel oder eine Quelle).

## <a name="attributes"></a>Attributes

[**clsid**](clsid-attribute.md), [**lock**](lock-attribute.md), [**mute**](mute-attribute.md), [**start**](start-attribute.md), [**stop**](stop-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)

## <a name="parentchild-information"></a>Informationen zu über- und untergeordneten Daten



| Bezeichnung | Wert |
|----------|--------------------------------------------------------------------------------------------------------------------------------------|
| Parent   | [**Zusammengesetzt,**](composite-element.md) [**Gruppe,**](group-element.md) [**Clip,**](clip-element.md) [**Track**](track-element.md) |
| Children | [**Parameter**](param-element.md)                                                                                                       |



 

## <a name="remarks"></a>Bemerkungen

Das **clsid-Attribut** gibt das Unterobjekt an, das den Effekt erstellt.

## <a name="examples"></a>Beispiele


```XML
<effect clsid="{b05a941c-3ce1-11d2-952a-00c04fa34f05}" start="0" stop="32.0" />
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Gdipluseffects.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[XTL-Elemente](xtl-elements.md)
</dt> </dl>

 

 




