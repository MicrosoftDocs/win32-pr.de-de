---
title: Sekundäre Ereignisse
description: Sekundäre Ereignisse
ms.assetid: cc9eb382-82ca-4416-a04e-1572e4c69c90
keywords:
- Windows Media Player Skins, sekundäre Ereignisse
- Skins, sekundäre Ereignisse
- Ereignisse, Sekundär
- Schreiben von Code für Skins, sekundäre Ereignisse
- sekundäre Ereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e04785a7468353665083287ac1b74bce5cbf0f8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471596"
---
# <a name="secondary-events"></a><span data-ttu-id="422b1-108">Sekundäre Ereignisse</span><span class="sxs-lookup"><span data-stu-id="422b1-108">Secondary Events</span></span>

<span data-ttu-id="422b1-109">Sie können bestimmen, welche anderen Ereignisse stattfinden, wenn ein bestimmtes Ereignis ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="422b1-109">You can determine what other events are taking place when a specific event is triggered.</span></span> <span data-ttu-id="422b1-110">Wenn z. b. auf eine Maustaste geklickt wird, möchten Sie möglicherweise wissen, ob die Alt-Taste gleichzeitig gedrückt war.</span><span class="sxs-lookup"><span data-stu-id="422b1-110">For example, when a mouse button is clicked, you may want to know whether the ALT key was down at the same time.</span></span>

## <a name="event-attributes"></a><span data-ttu-id="422b1-111">Ereignisattribute</span><span class="sxs-lookup"><span data-stu-id="422b1-111">Event Attributes</span></span>

<span data-ttu-id="422b1-112">Die folgenden Ereignis Attribute werden für Skins unterstützt:</span><span class="sxs-lookup"><span data-stu-id="422b1-112">The following event attributes are supported for skins:</span></span>

-   <span data-ttu-id="422b1-113">**altKey**</span><span class="sxs-lookup"><span data-stu-id="422b1-113">**altKey**</span></span>
-   <span data-ttu-id="422b1-114">**gedrückt**</span><span class="sxs-lookup"><span data-stu-id="422b1-114">**button**</span></span>
-   <span data-ttu-id="422b1-115">**clientX**</span><span class="sxs-lookup"><span data-stu-id="422b1-115">**clientX**</span></span>
-   <span data-ttu-id="422b1-116">**clientY**</span><span class="sxs-lookup"><span data-stu-id="422b1-116">**clientY**</span></span>
-   <span data-ttu-id="422b1-117">**ctrlKey**</span><span class="sxs-lookup"><span data-stu-id="422b1-117">**ctrlKey**</span></span>
-   <span data-ttu-id="422b1-118">**fromelements**</span><span class="sxs-lookup"><span data-stu-id="422b1-118">**fromElement**</span></span>
-   <span data-ttu-id="422b1-119">**OffsetX**</span><span class="sxs-lookup"><span data-stu-id="422b1-119">**offsetX**</span></span>
-   <span data-ttu-id="422b1-120">**offität**</span><span class="sxs-lookup"><span data-stu-id="422b1-120">**offsetY**</span></span>
-   <span data-ttu-id="422b1-121">**screenX**</span><span class="sxs-lookup"><span data-stu-id="422b1-121">**screenX**</span></span>
-   <span data-ttu-id="422b1-122">**Screeny**</span><span class="sxs-lookup"><span data-stu-id="422b1-122">**screenY**</span></span>
-   <span data-ttu-id="422b1-123">**shiftKey**</span><span class="sxs-lookup"><span data-stu-id="422b1-123">**shiftKey**</span></span>
-   <span data-ttu-id="422b1-124">**srcelements**</span><span class="sxs-lookup"><span data-stu-id="422b1-124">**srcElement**</span></span>
-   <span data-ttu-id="422b1-125">**"Element"**</span><span class="sxs-lookup"><span data-stu-id="422b1-125">**toElement**</span></span>
-   <span data-ttu-id="422b1-126">**x**</span><span class="sxs-lookup"><span data-stu-id="422b1-126">**x**</span></span>
-   <span data-ttu-id="422b1-127">**y**</span><span class="sxs-lookup"><span data-stu-id="422b1-127">**y**</span></span>
-   <span data-ttu-id="422b1-128">**Keycode**</span><span class="sxs-lookup"><span data-stu-id="422b1-128">**keyCode**</span></span>

<span data-ttu-id="422b1-129">Weitere Informationen zu diesen Attributen finden Sie in der [Skin-Programmier Referenz](skin-programming-reference.md).</span><span class="sxs-lookup"><span data-stu-id="422b1-129">For more information about these attributes, see the [Skin Programming Reference](skin-programming-reference.md).</span></span>

## <a name="using-secondary-events"></a><span data-ttu-id="422b1-130">Verwenden sekundärer Ereignisse</span><span class="sxs-lookup"><span data-stu-id="422b1-130">Using Secondary Events</span></span>

<span data-ttu-id="422b1-131">Ereignis Attribute können nur in JScript-Code verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="422b1-131">You can only process event attributes in JScript code.</span></span> <span data-ttu-id="422b1-132">Sie müssen die folgende Syntax verwenden:</span><span class="sxs-lookup"><span data-stu-id="422b1-132">You must use the following syntax:</span></span>


```C++
event.eventattributename
```



<span data-ttu-id="422b1-133">*eventattributename* ist der Name des Ereignis Attributs.</span><span class="sxs-lookup"><span data-stu-id="422b1-133">*eventattributename* is the name of the event attribute.</span></span> <span data-ttu-id="422b1-134">Wenn Sie z. b. ermitteln möchten, ob die Alt-Taste während eines Click-Ereignisses gedrückt wurde, können Sie die folgenden Zeilen in Ihrem JScript-Code verwenden:</span><span class="sxs-lookup"><span data-stu-id="422b1-134">For example, to determine whether the ALT key was pressed during a click event, you could use the following lines in your JScript code:</span></span>


```C++
wasAlt = event.altKey ;
if (wasAlt = true)
{
   // Do something here.
}
```



## <a name="related-topics"></a><span data-ttu-id="422b1-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="422b1-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="422b1-136">**Behandeln von Ereignissen**</span><span class="sxs-lookup"><span data-stu-id="422b1-136">**Handling Events**</span></span>](handling-events.md)
</dt> </dl>

 

 




