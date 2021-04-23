---
description: Das lineare Element definiert den Wert eines Param-Elements zu einem bestimmten Zeitpunkt relativ zum Anfang des Übergangs oder Effekts, der das param-Element enthält.
ms.assetid: f6af4bf1-fc2d-439c-b1e3-8e095ecad503
title: lineares Element (Camerauicontrol.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e722dcbc68d24d76f34c80bdd17a91ad44423aa
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910088"
---
# <a name="linear-element"></a><span data-ttu-id="d48d1-103">lineares Element</span><span class="sxs-lookup"><span data-stu-id="d48d1-103">linear Element</span></span>

> [!Note]  
> <span data-ttu-id="d48d1-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="d48d1-104">\[Deprecated.</span></span> <span data-ttu-id="d48d1-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="d48d1-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d48d1-106">Das lineare Element definiert den Wert eines [**Param-Elements**](param-element.md) zu einem bestimmten Zeitpunkt relativ zum Anfang des Übergangs oder Effekts, der das **param-Element** enthält.</span><span class="sxs-lookup"><span data-stu-id="d48d1-106">The linear element defines the value of a [**param**](param-element.md) element at a particular time, relative to the start of the transition or effect that contains the **param** element.</span></span> <span data-ttu-id="d48d1-107">Das `linear` -Element bewirkt, dass der -Parameter einen reibungslosen Übergang von seinem vorherigen Wert zum neuen Wert bewirkt.</span><span class="sxs-lookup"><span data-stu-id="d48d1-107">The `linear` element causes the parameter to make a smooth transition from its previous value to the new value.</span></span> <span data-ttu-id="d48d1-108">Verwenden Sie das at-Element, um [](at-element.md) sofort zu einem neuen Wert zu springen.</span><span class="sxs-lookup"><span data-stu-id="d48d1-108">For an instantaneous jump to a new value, use the [**at**](at-element.md) element.</span></span>

## <a name="attributes"></a><span data-ttu-id="d48d1-109">Attributes</span><span class="sxs-lookup"><span data-stu-id="d48d1-109">Attributes</span></span>

<span data-ttu-id="d48d1-110">[**time**](time-attribute.md), [ **value**](value-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="d48d1-110">[**time**](time-attribute.md), [**value**](value-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="d48d1-111">Informationen zu über- und untergeordneten Daten</span><span class="sxs-lookup"><span data-stu-id="d48d1-111">Parent/Child Information</span></span>



| <span data-ttu-id="d48d1-112">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="d48d1-112">Label</span></span> | <span data-ttu-id="d48d1-113">Wert</span><span class="sxs-lookup"><span data-stu-id="d48d1-113">Value</span></span> |
|----------|--------------------------------|
| <span data-ttu-id="d48d1-114">Parent</span><span class="sxs-lookup"><span data-stu-id="d48d1-114">Parent</span></span>   | [<span data-ttu-id="d48d1-115">**Parameter**</span><span class="sxs-lookup"><span data-stu-id="d48d1-115">**param**</span></span>](param-element.md) |
| <span data-ttu-id="d48d1-116">Children</span><span class="sxs-lookup"><span data-stu-id="d48d1-116">Children</span></span> | <span data-ttu-id="d48d1-117">Keine</span><span class="sxs-lookup"><span data-stu-id="d48d1-117">None</span></span>                           |



 

## <a name="examples"></a><span data-ttu-id="d48d1-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d48d1-118">Examples</span></span>


```XML
<linear time="6" value="0.0" />
```



## <a name="requirements"></a><span data-ttu-id="d48d1-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d48d1-119">Requirements</span></span>



| <span data-ttu-id="d48d1-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d48d1-120">Requirement</span></span> | <span data-ttu-id="d48d1-121">Wert</span><span class="sxs-lookup"><span data-stu-id="d48d1-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d48d1-122">Header</span><span class="sxs-lookup"><span data-stu-id="d48d1-122">Header</span></span><br/> | <dl> <span data-ttu-id="d48d1-123"><dt>Camerauicontrol.h</dt></span><span class="sxs-lookup"><span data-stu-id="d48d1-123"><dt>Camerauicontrol.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d48d1-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d48d1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d48d1-125">XTL-Elemente</span><span class="sxs-lookup"><span data-stu-id="d48d1-125">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 




