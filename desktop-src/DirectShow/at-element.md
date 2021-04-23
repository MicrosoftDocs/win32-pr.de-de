---
description: Das at-Element definiert den Wert eines Param-Elements zu einem bestimmten Zeitpunkt relativ zum Anfang des Übergangs oder Effekts, der den Parameter enthält.
ms.assetid: 523aa25c-790b-4532-9c69-76544235bdfe
title: at-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5822f82a349f31f0d4c8de3f522f7f4f3346a08
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909828"
---
# <a name="at-element"></a><span data-ttu-id="c4d83-103">at-Element</span><span class="sxs-lookup"><span data-stu-id="c4d83-103">at Element</span></span>

> [!Note]  
> <span data-ttu-id="c4d83-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="c4d83-104">\[Deprecated.</span></span> <span data-ttu-id="c4d83-105">Diese API wird möglicherweise aus zukünftigen Versionen von Windows entfernt.\]</span><span class="sxs-lookup"><span data-stu-id="c4d83-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="c4d83-106">Das `at` -Element definiert den Wert eines [**param-Elements**](param-element.md) zu einem bestimmten Zeitpunkt relativ zum Anfang des Übergangs oder Effekts, der den Parameter enthält.</span><span class="sxs-lookup"><span data-stu-id="c4d83-106">The `at` element defines the value of a [**param**](param-element.md) element at a particular time, relative to the start of the transition or effect that contains the parameter.</span></span> <span data-ttu-id="c4d83-107">Das -Element bewirkt, dass der -Parameter zum angegebenen Zeitpunkt plötzlich zum `at` neuen Wert springt.</span><span class="sxs-lookup"><span data-stu-id="c4d83-107">The `at` element causes the parameter to jump abruptly to the new value at the given time.</span></span> <span data-ttu-id="c4d83-108">Verwenden Sie das lineare Element, um einen reibungslosen Verlauf zu einem [**neuen Wert**](linear-element.md) zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c4d83-108">For a smooth progression to a new value, use the [**linear**](linear-element.md) element.</span></span>

## <a name="attributes"></a><span data-ttu-id="c4d83-109">Attributes</span><span class="sxs-lookup"><span data-stu-id="c4d83-109">Attributes</span></span>

<span data-ttu-id="c4d83-110">[**time,**](time-attribute.md) [ **value**](value-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="c4d83-110">[**time**](time-attribute.md), [**value**](value-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="c4d83-111">Informationen zu über- und untergeordneten Daten</span><span class="sxs-lookup"><span data-stu-id="c4d83-111">Parent/Child Information</span></span>



| <span data-ttu-id="c4d83-112">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="c4d83-112">Label</span></span> | <span data-ttu-id="c4d83-113">Wert</span><span class="sxs-lookup"><span data-stu-id="c4d83-113">Value</span></span> |
|----------|--------------------------------|
| <span data-ttu-id="c4d83-114">Parent</span><span class="sxs-lookup"><span data-stu-id="c4d83-114">Parent</span></span>   | [<span data-ttu-id="c4d83-115">**Parameter**</span><span class="sxs-lookup"><span data-stu-id="c4d83-115">**param**</span></span>](param-element.md) |
| <span data-ttu-id="c4d83-116">Children</span><span class="sxs-lookup"><span data-stu-id="c4d83-116">Children</span></span> | <span data-ttu-id="c4d83-117">Keine</span><span class="sxs-lookup"><span data-stu-id="c4d83-117">None</span></span>                           |



 

## <a name="examples"></a><span data-ttu-id="c4d83-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c4d83-118">Examples</span></span>


```XML
<at time="1" value="0.5" />
```



## <a name="see-also"></a><span data-ttu-id="c4d83-119">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c4d83-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4d83-120">XTL-Elemente</span><span class="sxs-lookup"><span data-stu-id="c4d83-120">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 



