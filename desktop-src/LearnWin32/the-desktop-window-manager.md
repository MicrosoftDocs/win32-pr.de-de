---
title: Die Desktopfenster-Manager
description: Die Desktopfenster-Manager
ms.assetid: 79250d49-dad5-46c6-892d-b92dac14b417
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fca8550134ba0c1cdafe0bd5c349061ef900a9e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103898"
---
# <a name="the-desktop-window-manager"></a><span data-ttu-id="4a77f-103">Die Desktopfenster-Manager</span><span class="sxs-lookup"><span data-stu-id="4a77f-103">The Desktop Window Manager</span></span>

<span data-ttu-id="4a77f-104">Vor Windows Vista zeichnete ein Windows-Programm direkt auf den Bildschirm.</span><span class="sxs-lookup"><span data-stu-id="4a77f-104">Before Windows Vista, a Windows program would draw directly to the screen.</span></span> <span data-ttu-id="4a77f-105">Anders ausgedrückt: Das Programm würde direkt in den Speicherpuffer schreiben, der von der Grafikkarte angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="4a77f-105">In other words, the program would write directly to the memory buffer shown by the video card.</span></span> <span data-ttu-id="4a77f-106">Dieser Ansatz kann visuelle Artefakte verursachen, wenn sich ein Fenster nicht ordnungsgemäß neu malt.</span><span class="sxs-lookup"><span data-stu-id="4a77f-106">This approach can cause visual artifacts if a window does not repaint itself correctly.</span></span> <span data-ttu-id="4a77f-107">Wenn der Benutzer beispielsweise ein Fenster über ein anderes Fenster zieht und sich das darunter liegende Fenster nicht schnell genug neu malt, kann das oberste Fenster einen Trail verlassen:</span><span class="sxs-lookup"><span data-stu-id="4a77f-107">For example, if the user drags one window over another window, and the window underneath does not repaint itself quickly enough, the top-most window can leave a trail:</span></span>

![Screenshot: Neupaintieren von Artefakten](images/graphics04.png)

<span data-ttu-id="4a77f-109">Der Trail wird verursacht, weil beide Fenster in den gleichen Speicherbereich zeichnen.</span><span class="sxs-lookup"><span data-stu-id="4a77f-109">The trail is caused because both windows paint to the same area of memory.</span></span> <span data-ttu-id="4a77f-110">Wenn das oberste Fenster gezogen wird, muss das Fenster darunter neu strichen werden.</span><span class="sxs-lookup"><span data-stu-id="4a77f-110">As the top-most window is dragged, the window below it must be repainted.</span></span> <span data-ttu-id="4a77f-111">Wenn das erneute Anstrichen zu langsam ist, führt dies zu den Artefakten, die in der vorherigen Abbildung gezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="4a77f-111">If the repainting is too slow, it causes the artifacts shown in the previous image.</span></span>

<span data-ttu-id="4a77f-112">Windows Vista hat durch die Einführung des Desktopfenster-Manager (DWM) die Art und Weise, wie Fenster gezeichnet werden, grundlegend geändert.</span><span class="sxs-lookup"><span data-stu-id="4a77f-112">Windows Vista fundamentally changed how windows are drawn, by introducing the Desktop Window Manager (DWM).</span></span> <span data-ttu-id="4a77f-113">Wenn dwm aktiviert ist, wird ein Fenster nicht mehr direkt in den Anzeigepuffer geschaltet.</span><span class="sxs-lookup"><span data-stu-id="4a77f-113">When the DWM is enabled, a window no longer draws directly to the display buffer.</span></span> <span data-ttu-id="4a77f-114">Stattdessen zeichnet jedes Fenster zu einem Offscreen-Speicherpuffer, der auch als *Offscreenoberfläche* bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="4a77f-114">Instead, each window draws to an offscreen memory buffer, also called an *offscreen surface*.</span></span> <span data-ttu-id="4a77f-115">Der DWM kombiniert diese Oberflächen dann mit dem Bildschirm.</span><span class="sxs-lookup"><span data-stu-id="4a77f-115">The DWM then composites these surfaces to the screen.</span></span>

![Ein Diagramm, das zeigt, wie dwm den Desktop zusammengesetzt.](images/graphics05.png)

<span data-ttu-id="4a77f-117">Dwm bietet gegenüber der alten Grafikarchitektur mehrere Vorteile.</span><span class="sxs-lookup"><span data-stu-id="4a77f-117">The DWM provides several advantages over the old graphics architecture.</span></span>

-   <span data-ttu-id="4a77f-118">Weniger neu malte Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="4a77f-118">Fewer repaint messages.</span></span> <span data-ttu-id="4a77f-119">Wenn ein Fenster durch ein anderes Fenster blockiert wird, muss sich das verdeckte Fenster nicht selbst neu malen.</span><span class="sxs-lookup"><span data-stu-id="4a77f-119">When a window is obstructed by another window, the obstructed window does not need to repaint itself.</span></span>
-   <span data-ttu-id="4a77f-120">Reduzierte Artefakte.</span><span class="sxs-lookup"><span data-stu-id="4a77f-120">Reduced artifacts.</span></span> <span data-ttu-id="4a77f-121">Zuvor konnten durch Ziehen eines Fensters visuelle Artefakte erstellt werden, wie beschrieben.</span><span class="sxs-lookup"><span data-stu-id="4a77f-121">Previously, dragging a window could create visual artifacts, as described.</span></span>
-   <span data-ttu-id="4a77f-122">Visuelle Effekte.</span><span class="sxs-lookup"><span data-stu-id="4a77f-122">Visual effects.</span></span> <span data-ttu-id="4a77f-123">Da der DWM für das Zusammenstellen des Bildschirms zuständig ist, kann er durchscheinende und unscharfe Bereiche des Fensters rendern.</span><span class="sxs-lookup"><span data-stu-id="4a77f-123">Because the DWM is in charge of compositing the screen, it can render translucent and blurred areas of the window.</span></span>
-   <span data-ttu-id="4a77f-124">Automatische Skalierung für hohe DPI-Daten.</span><span class="sxs-lookup"><span data-stu-id="4a77f-124">Automatic scaling for high DPI.</span></span> <span data-ttu-id="4a77f-125">Obwohl die Skalierung nicht die ideale Methode zum Verarbeiten von hohen DPI-Daten ist, ist sie ein sinnvoller Fallback für ältere Anwendungen, die nicht für hohe DPI-Einstellungen konzipiert wurden.</span><span class="sxs-lookup"><span data-stu-id="4a77f-125">Although scaling is not the ideal way to handle high DPI, it is a viable fallback for older applications that were not designed for high DPI settings.</span></span> <span data-ttu-id="4a77f-126">(Wir kehren später im Abschnitt [DPI und Device-Independent Pixels](dpi-and-device-independent-pixels.md)zu diesem Thema zurück.)</span><span class="sxs-lookup"><span data-stu-id="4a77f-126">(We will return to this topic later, in the section [DPI and Device-Independent Pixels](dpi-and-device-independent-pixels.md).)</span></span>
-   <span data-ttu-id="4a77f-127">Alternative Ansichten.</span><span class="sxs-lookup"><span data-stu-id="4a77f-127">Alternative views.</span></span> <span data-ttu-id="4a77f-128">Der DWM kann die Offscreenoberflächen auf verschiedene interessante Weise verwenden.</span><span class="sxs-lookup"><span data-stu-id="4a77f-128">The DWM can use the offscreen surfaces in various interesting ways.</span></span> <span data-ttu-id="4a77f-129">Der DWM ist beispielsweise die Technologie hinter Windows-Flip-3D, Miniaturansichten und animierten Übergängen.</span><span class="sxs-lookup"><span data-stu-id="4a77f-129">For example, the DWM is the technology behind Windows Flip 3D, thumbnails, and animated transitions.</span></span>

<span data-ttu-id="4a77f-130">Beachten Sie jedoch, dass die Aktivierung des DWM nicht garantiert ist.</span><span class="sxs-lookup"><span data-stu-id="4a77f-130">Note, however, that the DWM is not guaranteed to be enabled.</span></span> <span data-ttu-id="4a77f-131">Die Grafikkarte unterstützt möglicherweise nicht die DWM-Systemanforderungen, und Benutzer können den DWM über die **Systemeigenschaften-Systemsteuerung** deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="4a77f-131">The graphics card might not support the DWM system requirements, and users can disable the DWM through the **System Properties** control panel.</span></span> <span data-ttu-id="4a77f-132">Das bedeutet, dass sich Ihr Programm nicht auf das Neumalverhalten des DWM verlassen sollte.</span><span class="sxs-lookup"><span data-stu-id="4a77f-132">That means your program should not rely on the repainting behavior of the DWM.</span></span> <span data-ttu-id="4a77f-133">Testen Sie ihr Programm mit deaktivierter DWM, um sicherzustellen, dass es ordnungsgemäß neu malt.</span><span class="sxs-lookup"><span data-stu-id="4a77f-133">Test your program with DWM disabled to make sure that it repaints correctly.</span></span>

## <a name="next"></a><span data-ttu-id="4a77f-134">Nächste</span><span class="sxs-lookup"><span data-stu-id="4a77f-134">Next</span></span>

[<span data-ttu-id="4a77f-135">Beibehaltener Modus im Vergleich zum unmittelbaren Modus</span><span class="sxs-lookup"><span data-stu-id="4a77f-135">Retained Mode Versus Immediate Mode</span></span>](retained-mode-versus-immediate-mode.md)

 

 




