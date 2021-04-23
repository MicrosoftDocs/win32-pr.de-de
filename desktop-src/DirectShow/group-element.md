---
description: Das Group-Element definiert eine Gruppe, das Objekt der obersten Ebene in einer Zeitachse.
ms.assetid: db2f1fdd-bcb1-4401-91f4-5e167e4da215
title: group-Element (DirectShow)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31502cef89c8383e935f409d76b9e31ca53a2da1
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909248"
---
# <a name="group-element"></a><span data-ttu-id="f9bbf-103">group-Element</span><span class="sxs-lookup"><span data-stu-id="f9bbf-103">group Element</span></span>

> [!Note]  
> <span data-ttu-id="f9bbf-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="f9bbf-104">\[Deprecated.</span></span> <span data-ttu-id="f9bbf-105">Diese API wird möglicherweise aus zukünftigen Versionen von Windows entfernt.\]</span><span class="sxs-lookup"><span data-stu-id="f9bbf-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f9bbf-106">Das **Group-Element** definiert eine Gruppe, das Objekt der obersten Ebene in einer Zeitachse.</span><span class="sxs-lookup"><span data-stu-id="f9bbf-106">The **group** element defines a group, the top-level object in a timeline.</span></span>

## <a name="attributes"></a><span data-ttu-id="f9bbf-107">Attributes</span><span class="sxs-lookup"><span data-stu-id="f9bbf-107">Attributes</span></span>

<span data-ttu-id="f9bbf-108">[**bitdepth**](bitdepth-attribute.md), [**buffering**](buffering-attribute.md), [**framerate**](framerate-attribute.md), [**height**](height-attribute.md), [**lock**](lock-attribute.md), [**mute**](mute-attribute.md), [**name**](name-attribute.md), [**previewmode**](previewmode-attribute.md), [**samplingrate**](samplingrate-attribute.md), [**type**](type-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md), [**width**](width-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="f9bbf-108">[**bitdepth**](bitdepth-attribute.md), [**buffering**](buffering-attribute.md), [**framerate**](framerate-attribute.md), [**height**](height-attribute.md), [**lock**](lock-attribute.md), [**mute**](mute-attribute.md), [**name**](name-attribute.md), [**previewmode**](previewmode-attribute.md), [**samplingrate**](samplingrate-attribute.md), [**type**](type-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md), [**width**](width-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="f9bbf-109">Informationen zu über- und untergeordneten Daten</span><span class="sxs-lookup"><span data-stu-id="f9bbf-109">Parent/Child Information</span></span>



| <span data-ttu-id="f9bbf-110">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="f9bbf-110">Label</span></span> | <span data-ttu-id="f9bbf-111">Wert</span><span class="sxs-lookup"><span data-stu-id="f9bbf-111">Value</span></span> |
|----------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9bbf-112">Parent</span><span class="sxs-lookup"><span data-stu-id="f9bbf-112">Parent</span></span>   | [<span data-ttu-id="f9bbf-113">**Zeitachse**</span><span class="sxs-lookup"><span data-stu-id="f9bbf-113">**timeline**</span></span>](timeline-element.md)                                                                     |
| <span data-ttu-id="f9bbf-114">Children</span><span class="sxs-lookup"><span data-stu-id="f9bbf-114">Children</span></span> | <span data-ttu-id="f9bbf-115">[**composite**](composite-element.md), [**effect**](effect-element.md), [**track**](track-element.md)</span><span class="sxs-lookup"><span data-stu-id="f9bbf-115">[**composite**](composite-element.md), [**effect**](effect-element.md), [**track**](track-element.md)</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="f9bbf-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f9bbf-116">Remarks</span></span>

<span data-ttu-id="f9bbf-117">Innerhalb eines Elements wird die Priorität geschachtelter Ebenen implizit durch die Reihenfolge `group` bestimmt, in der sie im Element angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="f9bbf-117">Within a `group` element, the priority of nested layers is determined implicitly by the order they appear within the element.</span></span> <span data-ttu-id="f9bbf-118">Die erste Ebene hat Priorität 0, und nachfolgende Ebenen haben höhere Prioritätswerte.</span><span class="sxs-lookup"><span data-stu-id="f9bbf-118">The first layer has priority 0, and subsequent layers have increasing priority values.</span></span>

## <a name="examples"></a><span data-ttu-id="f9bbf-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f9bbf-119">Examples</span></span>


```XML
<group type="video" width="640" height="480" framerate="30"> </group>
```



## <a name="see-also"></a><span data-ttu-id="f9bbf-120">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f9bbf-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9bbf-121">XTL-Elemente</span><span class="sxs-lookup"><span data-stu-id="f9bbf-121">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 



