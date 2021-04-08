---
description: Das Group-Element definiert eine Gruppe, das Objekt der obersten Ebene in einer Zeitachse.
ms.assetid: db2f1fdd-bcb1-4401-91f4-5e167e4da215
title: Group-Element (DirectShow)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe0b8146586d93a53093a68bb1abc08e85c52f14
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103958068"
---
# <a name="group-element"></a><span data-ttu-id="6d2f8-103">Group-Element</span><span class="sxs-lookup"><span data-stu-id="6d2f8-103">group Element</span></span>

> [!Note]  
> <span data-ttu-id="6d2f8-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="6d2f8-104">\[Deprecated.</span></span> <span data-ttu-id="6d2f8-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="6d2f8-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="6d2f8-106">Das **Group** -Element definiert eine Gruppe, das Objekt der obersten Ebene in einer Zeitachse.</span><span class="sxs-lookup"><span data-stu-id="6d2f8-106">The **group** element defines a group, the top-level object in a timeline.</span></span>

## <a name="attributes"></a><span data-ttu-id="6d2f8-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="6d2f8-107">Attributes</span></span>

<span data-ttu-id="6d2f8-108">[**Bittiefe**](bitdepth-attribute.md), [**Pufferung**](buffering-attribute.md), [**Framerate**](framerate-attribute.md), [**height**](height-attribute.md), [**Lock**](lock-attribute.md), [**stumm**](mute-attribute.md), [**Name**](name-attribute.md), [**PreviewMode**](previewmode-attribute.md), [**Samplingrate**](samplingrate-attribute.md), [**Type**](type-attribute.md), [**UserData**](userdata-attribute.md), [**UserID**](userid-attribute.md), [**username**](username-attribute.md), [**Width**](width-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="6d2f8-108">[**bitdepth**](bitdepth-attribute.md), [**buffering**](buffering-attribute.md), [**framerate**](framerate-attribute.md), [**height**](height-attribute.md), [**lock**](lock-attribute.md), [**mute**](mute-attribute.md), [**name**](name-attribute.md), [**previewmode**](previewmode-attribute.md), [**samplingrate**](samplingrate-attribute.md), [**type**](type-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md), [**width**](width-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="6d2f8-109">Über-/unterordnungsinformationen</span><span class="sxs-lookup"><span data-stu-id="6d2f8-109">Parent/Child Information</span></span>



|          |                                                                                                          |
|----------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d2f8-110">Parent</span><span class="sxs-lookup"><span data-stu-id="6d2f8-110">Parent</span></span>   | [<span data-ttu-id="6d2f8-111">**Zeitplan**</span><span class="sxs-lookup"><span data-stu-id="6d2f8-111">**timeline**</span></span>](timeline-element.md)                                                                     |
| <span data-ttu-id="6d2f8-112">Children</span><span class="sxs-lookup"><span data-stu-id="6d2f8-112">Children</span></span> | <span data-ttu-id="6d2f8-113">zusammen [**gesetzte**](composite-element.md), [**Effekte**](effect-element.md), nach [**Verfolgung**](track-element.md)</span><span class="sxs-lookup"><span data-stu-id="6d2f8-113">[**composite**](composite-element.md), [**effect**](effect-element.md), [**track**](track-element.md)</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="6d2f8-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6d2f8-114">Remarks</span></span>

<span data-ttu-id="6d2f8-115">Innerhalb eines- `group` Elements wird die Priorität von geschachtelten Ebenen implizit durch die Reihenfolge bestimmt, in der Sie im-Element angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="6d2f8-115">Within a `group` element, the priority of nested layers is determined implicitly by the order they appear within the element.</span></span> <span data-ttu-id="6d2f8-116">Die erste Ebene hat Priorität 0, und nachfolgende Ebenen haben höhere Prioritätswerte.</span><span class="sxs-lookup"><span data-stu-id="6d2f8-116">The first layer has priority 0, and subsequent layers have increasing priority values.</span></span>

## <a name="examples"></a><span data-ttu-id="6d2f8-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6d2f8-117">Examples</span></span>


```XML
<group type="video" width="640" height="480" framerate="30"> </group>
```



## <a name="see-also"></a><span data-ttu-id="6d2f8-118">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6d2f8-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d2f8-119">XTL-Elemente</span><span class="sxs-lookup"><span data-stu-id="6d2f8-119">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 



