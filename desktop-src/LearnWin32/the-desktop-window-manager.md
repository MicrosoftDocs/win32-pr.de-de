---
title: Der Desktopfenster-Manager
description: .
ms.assetid: 79250d49-dad5-46c6-892d-b92dac14b417
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73167b762a9952eb508f09e70f3d4183b3b7a018
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309936"
---
# <a name="the-desktop-window-manager"></a><span data-ttu-id="8a291-103">Der Desktopfenster-Manager</span><span class="sxs-lookup"><span data-stu-id="8a291-103">The Desktop Window Manager</span></span>

<span data-ttu-id="8a291-104">Vor Windows Vista würde ein Windows-Programm direkt auf den Bildschirm gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="8a291-104">Before Windows Vista, a Windows program would draw directly to the screen.</span></span> <span data-ttu-id="8a291-105">Das Programm würde also direkt in den Speicherpuffer schreiben, der von der Grafikkarte angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="8a291-105">In other words, the program would write directly to the memory buffer shown by the video card.</span></span> <span data-ttu-id="8a291-106">Diese Vorgehensweise kann visuelle Artefakte verursachen, wenn sich ein Fenster nicht selbst ordnungsgemäß neu zeichnet.</span><span class="sxs-lookup"><span data-stu-id="8a291-106">This approach can cause visual artifacts if a window does not repaint itself correctly.</span></span> <span data-ttu-id="8a291-107">Wenn der Benutzer z. b. ein Fenster über ein anderes Fenster zieht und sich das Fenster unterhalb nicht schnell genug neu zeichnet, kann das oberste Fenster eine Spur hinterlassen:</span><span class="sxs-lookup"><span data-stu-id="8a291-107">For example, if the user drags one window over another window, and the window underneath does not repaint itself quickly enough, the top-most window can leave a trail:</span></span>

![ein Screenshot mit repaint-Artefakten.](images/graphics04.png)

<span data-ttu-id="8a291-109">Der Pfad ist darauf zurückzuführen, dass beide Fenster in denselben Bereich des Arbeitsspeichers zeichnen.</span><span class="sxs-lookup"><span data-stu-id="8a291-109">The trail is caused because both windows paint to the same area of memory.</span></span> <span data-ttu-id="8a291-110">Wenn das oberste Fenster gezogen wird, muss das Fenster unterhalb des Fensters neu gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="8a291-110">As the top-most window is dragged, the window below it must be repainted.</span></span> <span data-ttu-id="8a291-111">Wenn das erneute zeichnen zu langsam ist, werden die in der vorherigen Abbildung gezeigten Artefakte verursacht.</span><span class="sxs-lookup"><span data-stu-id="8a291-111">If the repainting is too slow, it causes the artifacts shown in the previous image.</span></span>

<span data-ttu-id="8a291-112">Windows Vista hat grundlegend geändert, wie Windows gezeichnet wird, indem die Desktopfenster-Manager (DWM) eingeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8a291-112">Windows Vista fundamentally changed how windows are drawn, by introducing the Desktop Window Manager (DWM).</span></span> <span data-ttu-id="8a291-113">Wenn die DWM aktiviert ist, wird ein Fenster nicht mehr direkt in den Anzeige Puffer gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="8a291-113">When the DWM is enabled, a window no longer draws directly to the display buffer.</span></span> <span data-ttu-id="8a291-114">Stattdessen zeichnet jedes Fenster einen Offscreen-Speicherpuffer, auch als *Offscreen-Oberfläche* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="8a291-114">Instead, each window draws to an offscreen memory buffer, also called an *offscreen surface*.</span></span> <span data-ttu-id="8a291-115">Anschließend werden diese Oberflächen vom DWM auf den Bildschirm integriert.</span><span class="sxs-lookup"><span data-stu-id="8a291-115">The DWM then composites these surfaces to the screen.</span></span>

![ein Diagramm, das zeigt, wie die DWM den Desktop integriert.](images/graphics05.png)

<span data-ttu-id="8a291-117">Die DWM bietet mehrere Vorteile gegenüber der alten Grafik Architektur.</span><span class="sxs-lookup"><span data-stu-id="8a291-117">The DWM provides several advantages over the old graphics architecture.</span></span>

-   <span data-ttu-id="8a291-118">Weniger Repaint-Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="8a291-118">Fewer repaint messages.</span></span> <span data-ttu-id="8a291-119">Wenn ein Fenster von einem anderen Fenster behindert wird, muss sich das versperrte Fenster nicht selbst neu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="8a291-119">When a window is obstructed by another window, the obstructed window does not need to repaint itself.</span></span>
-   <span data-ttu-id="8a291-120">Reduzierte Artefakte.</span><span class="sxs-lookup"><span data-stu-id="8a291-120">Reduced artifacts.</span></span> <span data-ttu-id="8a291-121">Zuvor konnte das Ziehen eines Fensters wie beschrieben visuelle Artefakte erstellen.</span><span class="sxs-lookup"><span data-stu-id="8a291-121">Previously, dragging a window could create visual artifacts, as described.</span></span>
-   <span data-ttu-id="8a291-122">Visuelle Effekte.</span><span class="sxs-lookup"><span data-stu-id="8a291-122">Visual effects.</span></span> <span data-ttu-id="8a291-123">Da die DWM für die Zusammensetzung des Bildschirms zuständig ist, kann Sie überflüssig und unscharfe Bereiche des Fensters darstellen.</span><span class="sxs-lookup"><span data-stu-id="8a291-123">Because the DWM is in charge of compositing the screen, it can render translucent and blurred areas of the window.</span></span>
-   <span data-ttu-id="8a291-124">Automatische Skalierung für hohe dpi-Informationen.</span><span class="sxs-lookup"><span data-stu-id="8a291-124">Automatic scaling for high DPI.</span></span> <span data-ttu-id="8a291-125">Obwohl die Skalierung nicht die ideale Methode zur Verarbeitung von hohem dpi-Wert ist, ist Sie ein funktionierender Fall Back für ältere Anwendungen, die nicht für hohe DPI-Einstellungen entwickelt wurden.</span><span class="sxs-lookup"><span data-stu-id="8a291-125">Although scaling is not the ideal way to handle high DPI, it is a viable fallback for older applications that were not designed for high DPI settings.</span></span> <span data-ttu-id="8a291-126">(Dieses Thema wird später im Abschnitt [dpi und Device-Independent Pixel](dpi-and-device-independent-pixels.md)zurückgegeben.)</span><span class="sxs-lookup"><span data-stu-id="8a291-126">(We will return to this topic later, in the section [DPI and Device-Independent Pixels](dpi-and-device-independent-pixels.md).)</span></span>
-   <span data-ttu-id="8a291-127">Alternative Ansichten.</span><span class="sxs-lookup"><span data-stu-id="8a291-127">Alternative views.</span></span> <span data-ttu-id="8a291-128">Die DWM kann die Offscreen-Oberflächen auf verschiedene interessante Arten verwenden.</span><span class="sxs-lookup"><span data-stu-id="8a291-128">The DWM can use the offscreen surfaces in various interesting ways.</span></span> <span data-ttu-id="8a291-129">Die DWM ist beispielsweise die Technologie hinter Windows Flip 3D, Miniaturansichten und animierten Übergänge.</span><span class="sxs-lookup"><span data-stu-id="8a291-129">For example, the DWM is the technology behind Windows Flip 3D, thumbnails, and animated transitions.</span></span>

<span data-ttu-id="8a291-130">Beachten Sie jedoch, dass die DWM nicht garantiert aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="8a291-130">Note, however, that the DWM is not guaranteed to be enabled.</span></span> <span data-ttu-id="8a291-131">Die Grafikkarte unterstützt die Systemanforderungen des DWM-Systems möglicherweise nicht, und Benutzer können die DWM über die **System** Steuerung deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="8a291-131">The graphics card might not support the DWM system requirements, and users can disable the DWM through the **System Properties** control panel.</span></span> <span data-ttu-id="8a291-132">Dies bedeutet, dass sich das Programm nicht auf das neuzeichnungs Verhalten der DWM verlassen sollte.</span><span class="sxs-lookup"><span data-stu-id="8a291-132">That means your program should not rely on the repainting behavior of the DWM.</span></span> <span data-ttu-id="8a291-133">Testen Sie das Programm mit deaktiviertem DWM, um sicherzustellen, dass es ordnungsgemäß neu zeichnet.</span><span class="sxs-lookup"><span data-stu-id="8a291-133">Test your program with DWM disabled to make sure that it repaints correctly.</span></span>

## <a name="next"></a><span data-ttu-id="8a291-134">Nächste</span><span class="sxs-lookup"><span data-stu-id="8a291-134">Next</span></span>

[<span data-ttu-id="8a291-135">Modus für beibehaltene Modus und unmittelbarer</span><span class="sxs-lookup"><span data-stu-id="8a291-135">Retained Mode Versus Immediate Mode</span></span>](retained-mode-versus-immediate-mode.md)

 

 




