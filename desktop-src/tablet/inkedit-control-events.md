---
description: 'In der folgenden Tabelle wird beschrieben, in welchen Threads die Ereignisse des InkEdit-Steuer Elements ausgelöst werden können. Eventthreadschangetriggers auf der Benutzeroberfläche der Anwendung (UI) threadclicktrigger auf der Benutzeroberfläche von Thread der Anwendung threaddblclickauslöst auf der Benutzeroberfläche threadkeydowntriggers der Anwendung auf der UI threadkeydowntriggers der Anwendung auf der UI threadkeyuptriggers der Anwendung auf der UI threadmousedowntriggers der Anwendung auf der Benutzeroberfläche threadmousetreveauslöst der Anwendung auf der UI threadmouseupfires der Anwendung auf der UI threadrecognition der Anwendung (nur verwaltete Bibliothek). Wird auf der UI threaderkentionresulttriggers der Anwendung auf der Benutzeroberfläche von threadselchangetriggers der Anwendung auf der UI threadstroketriggers der Anwendung auf dem UI-Thread der Anwendung ausgelöst. '
ms.assetid: 8554a1ab-3288-4bdd-866b-dd2c25842b1f
title: Ereignisse des InkEdit-Steuer Elements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b1547df05b438e6ade49663f5095dfd6674dbe4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960504"
---
# <a name="inkedit-control-events"></a><span data-ttu-id="ef4b1-103">Ereignisse des InkEdit-Steuer Elements</span><span class="sxs-lookup"><span data-stu-id="ef4b1-103">InkEdit Control Events</span></span>

<span data-ttu-id="ef4b1-104">In der folgenden Tabelle wird beschrieben, in welchen Threads die Ereignisse des [InkEdit](inkedit-control-reference.md) -Steuer Elements ausgelöst werden können.</span><span class="sxs-lookup"><span data-stu-id="ef4b1-104">The following table describes which threads the [InkEdit](inkedit-control-reference.md) control events can fire on.</span></span>



| <span data-ttu-id="ef4b1-105">Ereignis</span><span class="sxs-lookup"><span data-stu-id="ef4b1-105">Event</span></span>                                                                          | <span data-ttu-id="ef4b1-106">Threads</span><span class="sxs-lookup"><span data-stu-id="ef4b1-106">Threads</span></span>                                                          |
|--------------------------------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="ef4b1-107">**Klima**</span><span class="sxs-lookup"><span data-stu-id="ef4b1-107">**Change**</span></span>](inkedit-change.md)                                               | <span data-ttu-id="ef4b1-108">Wird auf dem Benutzeroberflächen Thread der Anwendung ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="ef4b1-108">Fires on the application's user interface (UI) thread</span></span><br/> |
| [<span data-ttu-id="ef4b1-109">**Sie**</span><span class="sxs-lookup"><span data-stu-id="ef4b1-109">**Click**</span></span>](inkedit-click.md)                                                 | <span data-ttu-id="ef4b1-110">Wird im UI-Thread der Anwendung ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="ef4b1-110">Fires on the application's UI thread</span></span><br/>                  |
| [<span data-ttu-id="ef4b1-111">**DblClick**</span><span class="sxs-lookup"><span data-stu-id="ef4b1-111">**DblClick**</span></span>](inkedit-dblclick.md)                                           | <span data-ttu-id="ef4b1-112">Wird im UI-Thread der Anwendung ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="ef4b1-112">Fires on the application's UI thread</span></span><br/>                  |
| [<span data-ttu-id="ef4b1-113">**Geste**</span><span class="sxs-lookup"><span data-stu-id="ef4b1-113">**Gesture**</span></span>](inkedit-gesture.md)                                             | <span data-ttu-id="ef4b1-114">Wird im UI-Thread der Anwendung ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="ef4b1-114">Fires on the application's UI thread</span></span><br/>                  |
| [<span data-ttu-id="ef4b1-115">**KeyDown**</span><span class="sxs-lookup"><span data-stu-id="ef4b1-115">**KeyDown**</span></span>](inkedit-keydown.md)                                             | <span data-ttu-id="ef4b1-116">Wird im UI-Thread der Anwendung ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="ef4b1-116">Fires on the application's UI thread</span></span><br/>                  |
| [<span data-ttu-id="ef4b1-117">**KeyPress**</span><span class="sxs-lookup"><span data-stu-id="ef4b1-117">**KeyPress**</span></span>](inkedit-keypress.md)                                           | <span data-ttu-id="ef4b1-118">Wird im UI-Thread der Anwendung ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="ef4b1-118">Fires on the application's UI thread</span></span><br/>                  |
| [<span data-ttu-id="ef4b1-119">**KeyUp**</span><span class="sxs-lookup"><span data-stu-id="ef4b1-119">**KeyUp**</span></span>](inkedit-keyup.md)                                                 | <span data-ttu-id="ef4b1-120">Wird im UI-Thread der Anwendung ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="ef4b1-120">Fires on the application's UI thread</span></span><br/>                  |
| [<span data-ttu-id="ef4b1-121">**MouseDown**</span><span class="sxs-lookup"><span data-stu-id="ef4b1-121">**MouseDown**</span></span>](inkedit-mousedown.md)                                         | <span data-ttu-id="ef4b1-122">Wird im UI-Thread der Anwendung ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="ef4b1-122">Fires on the application's UI thread</span></span><br/>                  |
| [<span data-ttu-id="ef4b1-123">**MouseMove**</span><span class="sxs-lookup"><span data-stu-id="ef4b1-123">**MouseMove**</span></span>](inkedit-mousemove.md)                                         | <span data-ttu-id="ef4b1-124">Wird im UI-Thread der Anwendung ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="ef4b1-124">Fires on the application's UI thread</span></span><br/>                  |
| [<span data-ttu-id="ef4b1-125">**MouseUp**</span><span class="sxs-lookup"><span data-stu-id="ef4b1-125">**MouseUp**</span></span>](inkedit-mouseup.md)                                             | <span data-ttu-id="ef4b1-126">Wird im UI-Thread der Anwendung ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="ef4b1-126">Fires on the application's UI thread</span></span><br/>                  |
| <span data-ttu-id="ef4b1-127">[**Erkennung**](/previous-versions/ms567627(v=vs.100)) (nur verwaltete Bibliothek).</span><span class="sxs-lookup"><span data-stu-id="ef4b1-127">[**Recognition**](/previous-versions/ms567627(v=vs.100)) (Managed Library only).</span></span> | <span data-ttu-id="ef4b1-128">Wird im UI-Thread der Anwendung ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="ef4b1-128">Fires on the application's UI thread</span></span><br/>                  |
| [<span data-ttu-id="ef4b1-129">**Erkennungs Ergebnis**</span><span class="sxs-lookup"><span data-stu-id="ef4b1-129">**RecognitionResult**</span></span>](inkedit-recognitionresult.md)                         | <span data-ttu-id="ef4b1-130">Wird im UI-Thread der Anwendung ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="ef4b1-130">Fires on the application's UI thread</span></span><br/>                  |
| [<span data-ttu-id="ef4b1-131">**SelChange**</span><span class="sxs-lookup"><span data-stu-id="ef4b1-131">**SelChange**</span></span>](inkedit-selchange.md)                                         | <span data-ttu-id="ef4b1-132">Wird im UI-Thread der Anwendung ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="ef4b1-132">Fires on the application's UI thread</span></span><br/>                  |
| [<span data-ttu-id="ef4b1-133">**Stellung**</span><span class="sxs-lookup"><span data-stu-id="ef4b1-133">**Stroke**</span></span>](inkedit-stroke.md)                                               | <span data-ttu-id="ef4b1-134">Wird im UI-Thread der Anwendung ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="ef4b1-134">Fires on the application's UI thread</span></span><br/>                  |



 

 

