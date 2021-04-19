---
description: Das Übergangs Element definiert ein Übergangs Objekt. Ein Übergang ist eine Transformation mit zwei Eingaben, die zu einem Übergang von einem Stream (z. b. einer zusammengesetzten oder einer Spur) zu einem anderen führt.
ms.assetid: d344a29f-5b6d-44a3-b1d7-759442e229f5
title: Transition-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b7663785c641252609366c8bfd6044582829e82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368812"
---
# <a name="transition-element"></a>Transition-Element

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Das- `transition` Element definiert ein Übergangs Objekt. Ein Übergang ist eine Transformation mit zwei Eingaben, die zu einem Übergang von einem Stream (z. b. einer zusammengesetzten oder einer Spur) zu einem anderen führt.

## <a name="attributes"></a>Attribute

[**CLSID**](clsid-attribute.md), [**cutpoint**](cutpoint-attribute.md), [**cutsonly**](cutsonly-attribute.md), [**Lock**](lock-attribute.md), [**stumm**](mute-attribute.md), [**Start**](start-attribute.md), [**Stopps**](stop-attribute.md), [**Swap**](swapinputs-attribute.md), [**UserData**](userdata-attribute.md), [**UserID**](userid-attribute.md), [**username**](username-attribute.md)

## <a name="parentchild-information"></a>Über-/unterordnungsinformationen



|          |                                                                        |
|----------|------------------------------------------------------------------------|
| Parent   | [**Composite**](composite-element.md), [ **Track**](track-element.md) |
| Children | [**param**](param-element.md)                                         |



 

## <a name="remarks"></a>Bemerkungen

Das **CLSID** -Attribut gibt das untergeordnete Objekt an, das den Übergang erstellt.

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

 

 



