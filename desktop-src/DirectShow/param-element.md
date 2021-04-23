---
description: Das param-Element gibt den Wert einer Eigenschaft für einen Übergang, einen Effekt oder ein anderes Unterobjekt an.
ms.assetid: a727c47c-b925-436c-b1e8-d5f407120dc9
title: param-Element (DirectShow)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a10f902e85066f6cea14023e8cff9250126add0
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909038"
---
# <a name="param-element"></a><span data-ttu-id="68c56-103">param-Element</span><span class="sxs-lookup"><span data-stu-id="68c56-103">param Element</span></span>

> [!Note]  
> <span data-ttu-id="68c56-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="68c56-104">\[Deprecated.</span></span> <span data-ttu-id="68c56-105">Diese API wird möglicherweise aus zukünftigen Versionen von Windows entfernt.\]</span><span class="sxs-lookup"><span data-stu-id="68c56-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="68c56-106">Das `param` -Element gibt den Wert einer Eigenschaft für einen Übergang, einen Effekt oder ein anderes Unterobjekt an.</span><span class="sxs-lookup"><span data-stu-id="68c56-106">The `param` element specifies the value of a property on a transition, effect, or other subobject.</span></span>

## <a name="attributes"></a><span data-ttu-id="68c56-107">Attributes</span><span class="sxs-lookup"><span data-stu-id="68c56-107">Attributes</span></span>

<span data-ttu-id="68c56-108">[**name**](name-attribute.md), [ **value**](value-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="68c56-108">[**name**](name-attribute.md), [**value**](value-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="68c56-109">Informationen zu über- und untergeordneten Daten</span><span class="sxs-lookup"><span data-stu-id="68c56-109">Parent/Child Information</span></span>



| <span data-ttu-id="68c56-110">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="68c56-110">Label</span></span> | <span data-ttu-id="68c56-111">Wert</span><span class="sxs-lookup"><span data-stu-id="68c56-111">Value</span></span> |
|----------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68c56-112">Parent</span><span class="sxs-lookup"><span data-stu-id="68c56-112">Parent</span></span>   | <span data-ttu-id="68c56-113">[**clip**](clip-element.md), [**effect**](effect-element.md), [**transition**](transition-element.md)</span><span class="sxs-lookup"><span data-stu-id="68c56-113">[**clip**](clip-element.md), [**effect**](effect-element.md), [**transition**](transition-element.md)</span></span> |
| <span data-ttu-id="68c56-114">Children</span><span class="sxs-lookup"><span data-stu-id="68c56-114">Children</span></span> | <span data-ttu-id="68c56-115">[**bei**](at-element.md), [ **linear**](linear-element.md)</span><span class="sxs-lookup"><span data-stu-id="68c56-115">[**at**](at-element.md), [**linear**](linear-element.md)</span></span>                                               |



 

## <a name="remarks"></a><span data-ttu-id="68c56-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="68c56-116">Remarks</span></span>

<span data-ttu-id="68c56-117">Das **Value-Attribut** gibt den Wert der -Eigenschaft am Anfang des Übergangs oder Effekts an.</span><span class="sxs-lookup"><span data-stu-id="68c56-117">The **value** attribute specifies the value of the property at the start of the transition or effect.</span></span> <span data-ttu-id="68c56-118">Verwenden Sie das **at-** **oder lineare** -Element, um sich ändernde Werte anzugeben.</span><span class="sxs-lookup"><span data-stu-id="68c56-118">Use the **at** or **linear** element to specify changing values.</span></span> <span data-ttu-id="68c56-119">Wenn das **param-Element** keine **at-** oder **linearen** Elemente enthält, bleibt der Wert über die Dauer des Effekts oder Übergangs konstant.</span><span class="sxs-lookup"><span data-stu-id="68c56-119">If the **param** element contains no **at** or **linear** elements, the value remains constant over the duration of the effect or transition.</span></span>

> [!Note]  
> <span data-ttu-id="68c56-120">Ein **param-Element** innerhalb eines **Clipelements** darf keine **at- oder** **linearen Elemente** enthalten.</span><span class="sxs-lookup"><span data-stu-id="68c56-120">A **param** element inside a **clip** element cannot contain **at** or **linear** elements.</span></span>

 

<span data-ttu-id="68c56-121">Viele Übergänge unterstützen eine **Status-Standardeigenschaft,** die zwischen 0 und 1,0 liegt und angibt, welcher Prozentsatz des Übergangs in der Ausgabe widergespiegelt wird.</span><span class="sxs-lookup"><span data-stu-id="68c56-121">Many transitions support a standard **Progress** property that ranges from 0 to 1.0, indicating what percentage of the transition is reflected in the output.</span></span> <span data-ttu-id="68c56-122">Bei **Progress** = 0,0 befindet sich der Übergang am Anfang seiner Sequenz (vollständig das erste Videobild).</span><span class="sxs-lookup"><span data-stu-id="68c56-122">At **Progress** = 0.0, the transition is at the beginning of its sequence (entirely the first video image).</span></span> <span data-ttu-id="68c56-123">Bei **Progress** = 0,5 ist der Übergang halb abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="68c56-123">At **Progress** = 0.5, the transition is half complete.</span></span> <span data-ttu-id="68c56-124">(Beispielsweise befindet sich bei einer Zurücksetzung bei **Progress** = 0,5 die Übergangsgrenze in der Mitte des Bilds.) Bei **Progress** = 1.0 ist der Übergang abgeschlossen (vollständig das zweite Bild).</span><span class="sxs-lookup"><span data-stu-id="68c56-124">(For example, in a wipe, at **Progress** = 0.5 the transition boundary is in the center of the image) At **Progress** = 1.0, the transition is complete (entirely the second image).</span></span> <span data-ttu-id="68c56-125">Standardmäßig wechseln Übergänge von **Progress** = 0.0 am Anfang des Übergangs zu **Progress** = 1.0 am Ende.</span><span class="sxs-lookup"><span data-stu-id="68c56-125">By default, transitions go from **Progress** = 0.0 at the start of the transition to **Progress** = 1.0 at the end.</span></span>

<span data-ttu-id="68c56-126">Andere Eigenschaften sind in der Regel spezifisch für einen bestimmten Übergang oder Effekt.</span><span class="sxs-lookup"><span data-stu-id="68c56-126">Other properties are usually specific to one particular transition or effect.</span></span> <span data-ttu-id="68c56-127">Beispielsweise unterstützt der Zurücksetzenübergang eine **GradientSize-Eigenschaft,** die die Breite des Übergangsbereichs steuert.</span><span class="sxs-lookup"><span data-stu-id="68c56-127">For example, the wipe transition supports a **GradientSize** property that controls the width of the transition area.</span></span>

<span data-ttu-id="68c56-128">Um einen Übergang rückwärts auszuführen, legen Sie die **Progress-Eigenschaft** zu Beginn des Übergangs auf 1,0 fest, und verwenden Sie das **lineare** Element, um den Wert in 0,0 zu ändern, wie im folgenden Beispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="68c56-128">To run a transition backward, set the **Progress** property to 1.0 at the start of the transition, and use the **linear** element to change the value to 0.0, as shown in the following example:</span></span>


```
<transition clsid="{af279b30-86eb-11d1-81bf-0000f87557db}" start="0" stop="6">
    <param name="progress" value="1.0">
        <linear time="6" value="0.0" />
    </param>
</transition>
```



## <a name="examples"></a><span data-ttu-id="68c56-129">Beispiele</span><span class="sxs-lookup"><span data-stu-id="68c56-129">Examples</span></span>


```XML
<param name="progress" value="1.0" />
```



## <a name="see-also"></a><span data-ttu-id="68c56-130">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="68c56-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68c56-131">XTL-Elemente</span><span class="sxs-lookup"><span data-stu-id="68c56-131">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 



