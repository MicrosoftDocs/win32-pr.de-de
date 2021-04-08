---
description: Das param-Element gibt den Wert einer Eigenschaft eines Übergangs, eines Effekts oder eines anderen unter Objekts an.
ms.assetid: a727c47c-b925-436c-b1e8-d5f407120dc9
title: param-Element (DirectShow)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb1d007a7f3e2dcffaa7b9163c76be604fed7a9a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860387"
---
# <a name="param-element"></a><span data-ttu-id="b9b39-103">param-Element</span><span class="sxs-lookup"><span data-stu-id="b9b39-103">param Element</span></span>

> [!Note]  
> <span data-ttu-id="b9b39-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="b9b39-104">\[Deprecated.</span></span> <span data-ttu-id="b9b39-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="b9b39-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b9b39-106">Das- `param` Element gibt den Wert einer Eigenschaft eines Übergangs, eines Effekts oder eines anderen unter Objekts an.</span><span class="sxs-lookup"><span data-stu-id="b9b39-106">The `param` element specifies the value of a property on a transition, effect, or other subobject.</span></span>

## <a name="attributes"></a><span data-ttu-id="b9b39-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="b9b39-107">Attributes</span></span>

<span data-ttu-id="b9b39-108">[**Name**](name-attribute.md), [ **Wert**](value-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="b9b39-108">[**name**](name-attribute.md), [**value**](value-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="b9b39-109">Über-/unterordnungsinformationen</span><span class="sxs-lookup"><span data-stu-id="b9b39-109">Parent/Child Information</span></span>



|          |                                                                                                          |
|----------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9b39-110">Parent</span><span class="sxs-lookup"><span data-stu-id="b9b39-110">Parent</span></span>   | <span data-ttu-id="b9b39-111">[**Clip**](clip-element.md), [**Effekt**](effect-element.md), [**Übergang**](transition-element.md)</span><span class="sxs-lookup"><span data-stu-id="b9b39-111">[**clip**](clip-element.md), [**effect**](effect-element.md), [**transition**](transition-element.md)</span></span> |
| <span data-ttu-id="b9b39-112">Children</span><span class="sxs-lookup"><span data-stu-id="b9b39-112">Children</span></span> | <span data-ttu-id="b9b39-113">[**bei**](at-element.md), [ **linear**](linear-element.md)</span><span class="sxs-lookup"><span data-stu-id="b9b39-113">[**at**](at-element.md), [**linear**](linear-element.md)</span></span>                                               |



 

## <a name="remarks"></a><span data-ttu-id="b9b39-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b9b39-114">Remarks</span></span>

<span data-ttu-id="b9b39-115">Das **value** -Attribut gibt den Wert der-Eigenschaft am Anfang des Übergangs oder Effekts an.</span><span class="sxs-lookup"><span data-stu-id="b9b39-115">The **value** attribute specifies the value of the property at the start of the transition or effect.</span></span> <span data-ttu-id="b9b39-116">Verwenden Sie das **at** -oder **lineare** -Element, um veränderliche Werte anzugeben.</span><span class="sxs-lookup"><span data-stu-id="b9b39-116">Use the **at** or **linear** element to specify changing values.</span></span> <span data-ttu-id="b9b39-117">Wenn das **param** -Element keine oder **lineare** Elemente enthält, bleibt der Wert während der Dauer des **Effekts oder Übergangs** konstant.</span><span class="sxs-lookup"><span data-stu-id="b9b39-117">If the **param** element contains no **at** or **linear** elements, the value remains constant over the duration of the effect or transition.</span></span>

> [!Note]  
> <span data-ttu-id="b9b39-118">Ein **param** -Element innerhalb eines **Clip** -Elements darf **keine oder** **lineare** Elemente enthalten.</span><span class="sxs-lookup"><span data-stu-id="b9b39-118">A **param** element inside a **clip** element cannot contain **at** or **linear** elements.</span></span>

 

<span data-ttu-id="b9b39-119">Viele Übergänge unterstützen eine **Standardstatus** Eigenschaft, die zwischen 0 und 1,0 liegt und angibt, welcher Prozentsatz des Übergangs in der Ausgabe reflektiert wird.</span><span class="sxs-lookup"><span data-stu-id="b9b39-119">Many transitions support a standard **Progress** property that ranges from 0 to 1.0, indicating what percentage of the transition is reflected in the output.</span></span> <span data-ttu-id="b9b39-120">Bei **Progress** = 0,0 erfolgt der Übergang am Anfang seiner Sequenz (vollständig das erste Video Bild).</span><span class="sxs-lookup"><span data-stu-id="b9b39-120">At **Progress** = 0.0, the transition is at the beginning of its sequence (entirely the first video image).</span></span> <span data-ttu-id="b9b39-121">Bei **Progress** = 0,5 ist der Übergang halb abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="b9b39-121">At **Progress** = 0.5, the transition is half complete.</span></span> <span data-ttu-id="b9b39-122">(Beispielsweise wird bei einer Löschung, bei **Progress** = 0,5, die Übergangsgrenze in der Mitte des Bilds angezeigt.) Bei **Progress** = 1,0 ist der Übergang abgeschlossen (vollständig das zweite Bild).</span><span class="sxs-lookup"><span data-stu-id="b9b39-122">(For example, in a wipe, at **Progress** = 0.5 the transition boundary is in the center of the image) At **Progress** = 1.0, the transition is complete (entirely the second image).</span></span> <span data-ttu-id="b9b39-123">Standardmäßig gehen Übergänge von **Progress** = 0,0 zu Beginn des Übergangs in **Progress** = 1,0 am Ende über.</span><span class="sxs-lookup"><span data-stu-id="b9b39-123">By default, transitions go from **Progress** = 0.0 at the start of the transition to **Progress** = 1.0 at the end.</span></span>

<span data-ttu-id="b9b39-124">Andere Eigenschaften sind normalerweise spezifisch für einen bestimmten Übergang oder einen bestimmten Effekt.</span><span class="sxs-lookup"><span data-stu-id="b9b39-124">Other properties are usually specific to one particular transition or effect.</span></span> <span data-ttu-id="b9b39-125">Beispielsweise unterstützt der Übergangs Übergang eine **gradientsize** -Eigenschaft, die die Breite des Übergangsbereichs steuert.</span><span class="sxs-lookup"><span data-stu-id="b9b39-125">For example, the wipe transition supports a **GradientSize** property that controls the width of the transition area.</span></span>

<span data-ttu-id="b9b39-126">Legen Sie zum Ausführen eines Übergangs rückwärts die Status **-Eigenschaft am** Anfang des Übergangs auf 1,0 fest, und verwenden Sie das **lineare** -Element, um den Wert in 0,0 zu ändern, wie im folgenden Beispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="b9b39-126">To run a transition backward, set the **Progress** property to 1.0 at the start of the transition, and use the **linear** element to change the value to 0.0, as shown in the following example:</span></span>


```
<transition clsid="{af279b30-86eb-11d1-81bf-0000f87557db}" start="0" stop="6">
    <param name="progress" value="1.0">
        <linear time="6" value="0.0" />
    </param>
</transition>
```



## <a name="examples"></a><span data-ttu-id="b9b39-127">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b9b39-127">Examples</span></span>


```XML
<param name="progress" value="1.0" />
```



## <a name="see-also"></a><span data-ttu-id="b9b39-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b9b39-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9b39-129">XTL-Elemente</span><span class="sxs-lookup"><span data-stu-id="b9b39-129">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 



