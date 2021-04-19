---
title: Externe Ereignisse
description: Externe Ereignisse
ms.assetid: d3fd8af6-8d7e-43b8-88fd-a59cf0cef609
keywords:
- Windows Media Player Skins, externe Ereignisse
- Skins, externe Ereignisse
- Ereignisse, extern
- Schreiben von Code für Skins, externe Ereignisse
- externe Ereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfa09a01b709f0da51d09fc2bec70cba0a1b07d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106342299"
---
# <a name="external-events"></a><span data-ttu-id="69317-108">Externe Ereignisse</span><span class="sxs-lookup"><span data-stu-id="69317-108">External Events</span></span>

<span data-ttu-id="69317-109">Wenn Benutzer auf eine Schaltfläche klicken oder eine Taste drücken, können Sie auf Ihre Eingabe mit Ereignis Handlern reagieren.</span><span class="sxs-lookup"><span data-stu-id="69317-109">When users click a button or press a key, you can respond to their input with event handlers.</span></span> <span data-ttu-id="69317-110">Ein Ereignishandler ist ein Code Abschnitt, der immer dann ausgeführt wird, wenn das Ereignis ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="69317-110">An event handler is a section of code that runs whenever the event is triggered.</span></span>

<span data-ttu-id="69317-111">Die folgenden Ereignisse werden von Skin-Elementen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="69317-111">The following events are supported by skin elements:</span></span>

-   <span data-ttu-id="69317-112">**Laden**</span><span class="sxs-lookup"><span data-stu-id="69317-112">**load**</span></span>
-   <span data-ttu-id="69317-113">**close**</span><span class="sxs-lookup"><span data-stu-id="69317-113">**close**</span></span>
-   <span data-ttu-id="69317-114">**Größe**</span><span class="sxs-lookup"><span data-stu-id="69317-114">**resize**</span></span>
-   <span data-ttu-id="69317-115">**Messer**</span><span class="sxs-lookup"><span data-stu-id="69317-115">**timer**</span></span>
-   <span data-ttu-id="69317-116">**Sie**</span><span class="sxs-lookup"><span data-stu-id="69317-116">**click**</span></span>
-   <span data-ttu-id="69317-117">**dblclick**</span><span class="sxs-lookup"><span data-stu-id="69317-117">**dblclick**</span></span>
-   <span data-ttu-id="69317-118">**error**</span><span class="sxs-lookup"><span data-stu-id="69317-118">**error**</span></span>
-   <span data-ttu-id="69317-119">**mousedown**</span><span class="sxs-lookup"><span data-stu-id="69317-119">**mousedown**</span></span>
-   <span data-ttu-id="69317-120">**mouseup**</span><span class="sxs-lookup"><span data-stu-id="69317-120">**mouseup**</span></span>
-   <span data-ttu-id="69317-121">**mousemove**</span><span class="sxs-lookup"><span data-stu-id="69317-121">**mousemove**</span></span>
-   <span data-ttu-id="69317-122">**Mouseover**</span><span class="sxs-lookup"><span data-stu-id="69317-122">**mouseover**</span></span>
-   <span data-ttu-id="69317-123">**mouseout**</span><span class="sxs-lookup"><span data-stu-id="69317-123">**mouseout**</span></span>
-   <span data-ttu-id="69317-124">**keypress**</span><span class="sxs-lookup"><span data-stu-id="69317-124">**keypress**</span></span>
-   <span data-ttu-id="69317-125">**keydown**</span><span class="sxs-lookup"><span data-stu-id="69317-125">**keydown**</span></span>
-   <span data-ttu-id="69317-126">**keyup**</span><span class="sxs-lookup"><span data-stu-id="69317-126">**keyup**</span></span>

<span data-ttu-id="69317-127">Weitere Informationen zu bestimmten Ereignissen finden Sie in der Design- [Programmier Referenz](skin-programming-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="69317-127">See the [Skin Programming Reference](skin-programming-reference.md) for more details about specific events.</span></span>

<span data-ttu-id="69317-128">Ein typischer externer Ereignishandler würde das Ereignis benennen und den Code definieren, der ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="69317-128">A typical external event handler would name the event and define the code that will run.</span></span> <span data-ttu-id="69317-129">Wenn Sie z. b. Code zum Starten von Windows Media Player erstellen möchten, wenn der Benutzer auf eine Schaltfläche klickt, würden Sie die folgende Zeile in den Schaltflächen Code einfügen.</span><span class="sxs-lookup"><span data-stu-id="69317-129">For example, if you want to create code to start Windows Media Player when the user clicks on a button, you would put the following line in your button code.</span></span>


```C++
onclick = "JScript: player.URL = 'https://proseware.com/laure.wma' ; "

```



<span data-ttu-id="69317-130">Dadurch wird die Datei mit dem Namen "Laure. wma" wiedergegeben.</span><span class="sxs-lookup"><span data-stu-id="69317-130">This will play the file named laure.wma.</span></span> <span data-ttu-id="69317-131">Beachten Sie, dass Sie das Wort "on" bestimmten Ereignissen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="69317-131">Note that you add the word "on" to specific events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="69317-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="69317-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="69317-133">**Behandeln von Ereignissen**</span><span class="sxs-lookup"><span data-stu-id="69317-133">**Handling Events**</span></span>](handling-events.md)
</dt> </dl>

 

 




