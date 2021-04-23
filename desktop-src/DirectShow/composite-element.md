---
description: Das zusammengesetzte Element definiert eine Komposition, ein Containerobjekt für Spuren und andere geschachtelte Kompositionen.
ms.assetid: 7551da3a-1da6-426a-ba9d-f715df53718f
title: composite-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5eff3e0c16040f837e4c8a792ebac3124d723d1
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908838"
---
# <a name="composite-element"></a><span data-ttu-id="5a619-103">composite-Element</span><span class="sxs-lookup"><span data-stu-id="5a619-103">composite Element</span></span>

> [!Note]  
> <span data-ttu-id="5a619-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="5a619-104">\[Deprecated.</span></span> <span data-ttu-id="5a619-105">Diese API wird möglicherweise aus zukünftigen Versionen von Windows entfernt.\]</span><span class="sxs-lookup"><span data-stu-id="5a619-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="5a619-106">Das `composite` -Element definiert eine Komposition, ein Containerobjekt für Spuren und andere geschachtelte Kompositionen.</span><span class="sxs-lookup"><span data-stu-id="5a619-106">The `composite` element defines a composition, a container object for tracks and other nested compositions.</span></span>

## <a name="attributes"></a><span data-ttu-id="5a619-107">Attributes</span><span class="sxs-lookup"><span data-stu-id="5a619-107">Attributes</span></span>

<span data-ttu-id="5a619-108">[**lock**](lock-attribute.md), [**mute**](mute-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="5a619-108">[**lock**](lock-attribute.md), [**mute**](mute-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="5a619-109">Informationen zu über- und untergeordneten Daten</span><span class="sxs-lookup"><span data-stu-id="5a619-109">Parent/Child Information</span></span>



| <span data-ttu-id="5a619-110">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="5a619-110">Label</span></span> | <span data-ttu-id="5a619-111">Wert</span><span class="sxs-lookup"><span data-stu-id="5a619-111">Value</span></span> |
|----------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a619-112">Parent</span><span class="sxs-lookup"><span data-stu-id="5a619-112">Parent</span></span>   | <span data-ttu-id="5a619-113">`composite`, [ **Gruppe**](group-element.md)</span><span class="sxs-lookup"><span data-stu-id="5a619-113">`composite`, [**group**](group-element.md)</span></span>                                                                             |
| <span data-ttu-id="5a619-114">Children</span><span class="sxs-lookup"><span data-stu-id="5a619-114">Children</span></span> | <span data-ttu-id="5a619-115">`composite`, [**effect**](effect-element.md), [**track**](track-element.md), [**transition**](transition-element.md)</span><span class="sxs-lookup"><span data-stu-id="5a619-115">`composite`, [**effect**](effect-element.md), [**track**](track-element.md), [**transition**](transition-element.md)</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="5a619-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5a619-116">Remarks</span></span>

<span data-ttu-id="5a619-117">Innerhalb eines Elements wird die Priorität geschachtelter Ebenen implizit durch die Reihenfolge bestimmt, in der `composite` sie innerhalb des Elements angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="5a619-117">Within a `composite` element, the priority of nested layers is determined implicitly by the order in which they appear within the element.</span></span> <span data-ttu-id="5a619-118">Die erste Ebene hat Priorität 0, und nachfolgende Ebenen haben höhere Prioritätswerte.</span><span class="sxs-lookup"><span data-stu-id="5a619-118">The first layer has priority 0, and subsequent layers have increasing priority values.</span></span>

## <a name="examples"></a><span data-ttu-id="5a619-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5a619-119">Examples</span></span>


```XML
<composite> </composite>
```



## <a name="see-also"></a><span data-ttu-id="5a619-120">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5a619-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a619-121">XTL-Elemente</span><span class="sxs-lookup"><span data-stu-id="5a619-121">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 



