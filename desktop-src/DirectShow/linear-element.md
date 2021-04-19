---
description: Das lineare Element definiert den Wert eines Param-Elements zu einem bestimmten Zeitpunkt relativ zum Anfang des Übergangs oder Effekts, der das param-Element enthält.
ms.assetid: f6af4bf1-fc2d-439c-b1e3-8e095ecad503
title: Linear-Element (camerauicontrol. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27080d08a1bbec98d5fa34b2739c63958e5d170a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370521"
---
# <a name="linear-element"></a><span data-ttu-id="8adc6-103">lineares Element</span><span class="sxs-lookup"><span data-stu-id="8adc6-103">linear Element</span></span>

> [!Note]  
> <span data-ttu-id="8adc6-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="8adc6-104">\[Deprecated.</span></span> <span data-ttu-id="8adc6-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="8adc6-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="8adc6-106">Das lineare Element definiert den Wert eines [**param**](param-element.md) -Elements zu einem bestimmten Zeitpunkt relativ zum Anfang des Übergangs oder Effekts, der das **param** -Element enthält.</span><span class="sxs-lookup"><span data-stu-id="8adc6-106">The linear element defines the value of a [**param**](param-element.md) element at a particular time, relative to the start of the transition or effect that contains the **param** element.</span></span> <span data-ttu-id="8adc6-107">Das- `linear` Element bewirkt, dass der-Parameter einen reibungslosen Übergang vom vorherigen Wert zum neuen Wert vornimmt.</span><span class="sxs-lookup"><span data-stu-id="8adc6-107">The `linear` element causes the parameter to make a smooth transition from its previous value to the new value.</span></span> <span data-ttu-id="8adc6-108">Verwenden Sie das [**at**](at-element.md) -Element, um sofort zu einem neuen Wert zu springen.</span><span class="sxs-lookup"><span data-stu-id="8adc6-108">For an instantaneous jump to a new value, use the [**at**](at-element.md) element.</span></span>

## <a name="attributes"></a><span data-ttu-id="8adc6-109">Attribute</span><span class="sxs-lookup"><span data-stu-id="8adc6-109">Attributes</span></span>

<span data-ttu-id="8adc6-110">[**Uhrzeit**](time-attribute.md), [ **Wert**](value-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="8adc6-110">[**time**](time-attribute.md), [**value**](value-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="8adc6-111">Über-/unterordnungsinformationen</span><span class="sxs-lookup"><span data-stu-id="8adc6-111">Parent/Child Information</span></span>



|          |                                |
|----------|--------------------------------|
| <span data-ttu-id="8adc6-112">Parent</span><span class="sxs-lookup"><span data-stu-id="8adc6-112">Parent</span></span>   | [<span data-ttu-id="8adc6-113">**param**</span><span class="sxs-lookup"><span data-stu-id="8adc6-113">**param**</span></span>](param-element.md) |
| <span data-ttu-id="8adc6-114">Children</span><span class="sxs-lookup"><span data-stu-id="8adc6-114">Children</span></span> | <span data-ttu-id="8adc6-115">Keine</span><span class="sxs-lookup"><span data-stu-id="8adc6-115">None</span></span>                           |



 

## <a name="examples"></a><span data-ttu-id="8adc6-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8adc6-116">Examples</span></span>


```XML
<linear time="6" value="0.0" />
```



## <a name="requirements"></a><span data-ttu-id="8adc6-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8adc6-117">Requirements</span></span>



| <span data-ttu-id="8adc6-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8adc6-118">Requirement</span></span> | <span data-ttu-id="8adc6-119">Wert</span><span class="sxs-lookup"><span data-stu-id="8adc6-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8adc6-120">Header</span><span class="sxs-lookup"><span data-stu-id="8adc6-120">Header</span></span><br/> | <dl> <span data-ttu-id="8adc6-121"><dt>Camerauicontrol. h</dt></span><span class="sxs-lookup"><span data-stu-id="8adc6-121"><dt>Camerauicontrol.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8adc6-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8adc6-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8adc6-123">XTL-Elemente</span><span class="sxs-lookup"><span data-stu-id="8adc6-123">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 




