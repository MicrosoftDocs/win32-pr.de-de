---
description: Das Übergangselement definiert ein Übergangsobjekt. Ein Übergang ist eine Transformation mit zwei Eingaben, die zu einem Übergang von einem Stream (z. B. einem zusammengesetzten Stream oder einer Spur) zu einem anderen führt.
ms.assetid: d344a29f-5b6d-44a3-b1d7-759442e229f5
title: transition-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60bf6b915a393ab153f0e94862cb5ed72dd3424c
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910038"
---
# <a name="transition-element"></a>transition-Element

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Das `transition` -Element definiert ein Übergangsobjekt. Ein Übergang ist eine Transformation mit zwei Eingaben, die zu einem Übergang von einem Stream (z. B. einem zusammengesetzten Stream oder einer Spur) zu einem anderen führt.

## <a name="attributes"></a>Attributes

[**clsid**](clsid-attribute.md), [**cutpoint**](cutpoint-attribute.md), [**cutsonly**](cutsonly-attribute.md), [**lock**](lock-attribute.md), [**mute**](mute-attribute.md), [**start**](start-attribute.md), [**stop**](stop-attribute.md), [**swapinputs**](swapinputs-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)

## <a name="parentchild-information"></a>Informationen zu über- und untergeordneten Daten



| Bezeichnung | Wert |
|----------|------------------------------------------------------------------------|
| Parent   | [**zusammengesetzte**](composite-element.md), [ **Track**](track-element.md) |
| Children | [**Parameter**](param-element.md)                                         |



 

## <a name="remarks"></a>Bemerkungen

Das **clsid-Attribut** gibt das Unterobjekt an, das den Übergang erstellt.

## <a name="examples"></a>Beispiele


```XML
<transition
    clsid="{2a54c913-07aa-11d2-8d6d-00c04f8ef8e0}"
    start="7"
    stop="10"
/>
```



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[XTL-Elemente](xtl-elements.md)
</dt> </dl>

 

 



