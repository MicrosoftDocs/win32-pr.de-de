---
description: Das Effect-Element definiert ein audiobild oder Videoeffekt Objekt. Ein Effekt wird auf einen einzelnen Stream (z. b. eine Komposition, eine Spur oder eine Quelle) angewendet.
ms.assetid: aedb4491-f1f0-44b3-ad88-3fac8c90144d
title: Effect-Element (gdipluseffects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9dd31e85407b99c3dffd4417a051be168f7c6d3a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371292"
---
# <a name="effect-element"></a>Effect-Element

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Das `effect` -Element definiert ein audiobild oder Videoeffekt Objekt. Ein Effekt wird auf einen einzelnen Stream (z. b. eine Komposition, eine Spur oder eine Quelle) angewendet.

## <a name="attributes"></a>Attribute

[**CLSID**](clsid-attribute.md), [**Lock**](lock-attribute.md), [**stumm**](mute-attribute.md), [**Start**](start-attribute.md), [**Ende**](stop-attribute.md), [**UserData**](userdata-attribute.md), [**UserID**](userid-attribute.md), [**username**](username-attribute.md)

## <a name="parentchild-information"></a>Über-/unterordnungsinformationen



|          |                                                                                                                                      |
|----------|--------------------------------------------------------------------------------------------------------------------------------------|
| Parent   | [**Composite**](composite-element.md), [**Group**](group-element.md), [**Clip**](clip-element.md), [**Track**](track-element.md) |
| Children | [**param**](param-element.md)                                                                                                       |



 

## <a name="remarks"></a>Bemerkungen

Das **CLSID** -Attribut gibt das untergeordnete Objekt an, das den Effekt erzeugt.

## <a name="examples"></a>Beispiele


```XML
<effect clsid="{b05a941c-3ce1-11d2-952a-00c04fa34f05}" start="0" stop="32.0" />
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Gdipluseffects. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[XTL-Elemente](xtl-elements.md)
</dt> </dl>

 

 




