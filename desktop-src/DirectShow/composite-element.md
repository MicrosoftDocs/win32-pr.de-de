---
description: Das zusammengesetzte Element definiert eine Komposition, ein Container Objekt für Spuren und andere zusammengesetzte kombinieren.
ms.assetid: 7551da3a-1da6-426a-ba9d-f715df53718f
title: Composite-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a1c81bf445769c049287bdfa7d23f4ab82bb0f8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106345580"
---
# <a name="composite-element"></a><span data-ttu-id="b25a4-103">Composite-Element</span><span class="sxs-lookup"><span data-stu-id="b25a4-103">composite Element</span></span>

> [!Note]  
> <span data-ttu-id="b25a4-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="b25a4-104">\[Deprecated.</span></span> <span data-ttu-id="b25a4-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="b25a4-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b25a4-106">Das `composite` -Element definiert eine Komposition, ein Container Objekt für Spuren und andere zusammengefügte Zeichen.</span><span class="sxs-lookup"><span data-stu-id="b25a4-106">The `composite` element defines a composition, a container object for tracks and other nested compositions.</span></span>

## <a name="attributes"></a><span data-ttu-id="b25a4-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="b25a4-107">Attributes</span></span>

<span data-ttu-id="b25a4-108">[**Lock**](lock-attribute.md), [**stumm**](mute-attribute.md), [**UserData**](userdata-attribute.md), [**UserID**](userid-attribute.md), [**username**](username-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="b25a4-108">[**lock**](lock-attribute.md), [**mute**](mute-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="b25a4-109">Über-/unterordnungsinformationen</span><span class="sxs-lookup"><span data-stu-id="b25a4-109">Parent/Child Information</span></span>



|          |                                                                                                                         |
|----------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b25a4-110">Parent</span><span class="sxs-lookup"><span data-stu-id="b25a4-110">Parent</span></span>   | <span data-ttu-id="b25a4-111">`composite`, [ **Gruppe**](group-element.md)</span><span class="sxs-lookup"><span data-stu-id="b25a4-111">`composite`, [**group**](group-element.md)</span></span>                                                                             |
| <span data-ttu-id="b25a4-112">Children</span><span class="sxs-lookup"><span data-stu-id="b25a4-112">Children</span></span> | <span data-ttu-id="b25a4-113">`composite`, [**Auswirkung**](effect-element.md), nach [**Verfolgung**](track-element.md), [**Übergang**](transition-element.md)</span><span class="sxs-lookup"><span data-stu-id="b25a4-113">`composite`, [**effect**](effect-element.md), [**track**](track-element.md), [**transition**](transition-element.md)</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="b25a4-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b25a4-114">Remarks</span></span>

<span data-ttu-id="b25a4-115">Innerhalb eines- `composite` Elements wird die Priorität von geschachtelten Ebenen implizit durch die Reihenfolge bestimmt, in der Sie innerhalb des-Elements angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="b25a4-115">Within a `composite` element, the priority of nested layers is determined implicitly by the order in which they appear within the element.</span></span> <span data-ttu-id="b25a4-116">Die erste Ebene hat Priorität 0, und nachfolgende Ebenen haben höhere Prioritätswerte.</span><span class="sxs-lookup"><span data-stu-id="b25a4-116">The first layer has priority 0, and subsequent layers have increasing priority values.</span></span>

## <a name="examples"></a><span data-ttu-id="b25a4-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b25a4-117">Examples</span></span>


```XML
<composite> </composite>
```



## <a name="see-also"></a><span data-ttu-id="b25a4-118">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b25a4-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b25a4-119">XTL-Elemente</span><span class="sxs-lookup"><span data-stu-id="b25a4-119">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 



