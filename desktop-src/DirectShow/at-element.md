---
description: Das at-Element definiert den Wert eines Param-Elements zu einem bestimmten Zeitpunkt relativ zum Anfang des Übergangs oder Effekts, der den Parameter enthält.
ms.assetid: 523aa25c-790b-4532-9c69-76544235bdfe
title: at-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cb539331519fb23b6b8aa45b374457229f807a5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747264"
---
# <a name="at-element"></a><span data-ttu-id="a577f-103">at-Element</span><span class="sxs-lookup"><span data-stu-id="a577f-103">at Element</span></span>

> [!Note]  
> <span data-ttu-id="a577f-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="a577f-104">\[Deprecated.</span></span> <span data-ttu-id="a577f-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="a577f-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="a577f-106">Das- `at` Element definiert den Wert eines [**param**](param-element.md) -Elements zu einem bestimmten Zeitpunkt relativ zum Anfang des Übergangs oder Effekts, der den Parameter enthält.</span><span class="sxs-lookup"><span data-stu-id="a577f-106">The `at` element defines the value of a [**param**](param-element.md) element at a particular time, relative to the start of the transition or effect that contains the parameter.</span></span> <span data-ttu-id="a577f-107">Das- `at` Element bewirkt, dass der-Parameter zum angegebenen Zeitpunkt abrupt zum neuen Wert springt.</span><span class="sxs-lookup"><span data-stu-id="a577f-107">The `at` element causes the parameter to jump abruptly to the new value at the given time.</span></span> <span data-ttu-id="a577f-108">Verwenden Sie das [**lineare**](linear-element.md) -Element, um einen reibungslosen Übergang zu einem neuen Wert zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="a577f-108">For a smooth progression to a new value, use the [**linear**](linear-element.md) element.</span></span>

## <a name="attributes"></a><span data-ttu-id="a577f-109">Attribute</span><span class="sxs-lookup"><span data-stu-id="a577f-109">Attributes</span></span>

<span data-ttu-id="a577f-110">[**Uhrzeit**](time-attribute.md), [ **Wert**](value-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="a577f-110">[**time**](time-attribute.md), [**value**](value-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="a577f-111">Über-/unterordnungsinformationen</span><span class="sxs-lookup"><span data-stu-id="a577f-111">Parent/Child Information</span></span>



|          |                                |
|----------|--------------------------------|
| <span data-ttu-id="a577f-112">Parent</span><span class="sxs-lookup"><span data-stu-id="a577f-112">Parent</span></span>   | [<span data-ttu-id="a577f-113">**param**</span><span class="sxs-lookup"><span data-stu-id="a577f-113">**param**</span></span>](param-element.md) |
| <span data-ttu-id="a577f-114">Children</span><span class="sxs-lookup"><span data-stu-id="a577f-114">Children</span></span> | <span data-ttu-id="a577f-115">Keine</span><span class="sxs-lookup"><span data-stu-id="a577f-115">None</span></span>                           |



 

## <a name="examples"></a><span data-ttu-id="a577f-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a577f-116">Examples</span></span>


```XML
<at time="1" value="0.5" />
```



## <a name="see-also"></a><span data-ttu-id="a577f-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a577f-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a577f-118">XTL-Elemente</span><span class="sxs-lookup"><span data-stu-id="a577f-118">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 



