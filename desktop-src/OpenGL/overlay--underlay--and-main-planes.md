---
title: Überlagerung, Unterebene und Hauptebenen
description: Sie können in Ihren Anwendungen Hardware Ebenen (Überlagerung und Unterebene) verwenden.
ms.assetid: fd9401b3-f2a8-4384-92e8-61b346216542
keywords:
- OpenGL unter Windows, Hardware Ebenen-Ebenen
- Hardware Schicht-Flächen OpenGL
- über Lagerungs Ebenen OpenGL
- unterliegende Flächen OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6fe68c4bb57d431151c4d879965fcf7496c8615
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338990"
---
# <a name="overlay-underlay-and-main-planes"></a><span data-ttu-id="d8186-107">Überlagerung, Unterebene und Hauptebenen</span><span class="sxs-lookup"><span data-stu-id="d8186-107">Overlay, Underlay, and Main Planes</span></span>

<span data-ttu-id="d8186-108">Sie können in Ihren Anwendungen Hardware Ebenen (Überlagerung und Unterebene) verwenden.</span><span class="sxs-lookup"><span data-stu-id="d8186-108">You can use hardware layer planes (overlay and underlay planes) in your applications.</span></span> <span data-ttu-id="d8186-109">Bei Windows beschreiben Pixel Formate die Pixel Konfigurationen eines Grafik Geräts.</span><span class="sxs-lookup"><span data-stu-id="d8186-109">With Windows, pixel formats describe the pixel configurations of a graphics device.</span></span> <span data-ttu-id="d8186-110">Jedes Pixel Format beschreibt die Tiefe und andere Merkmale der Haupt Farb Puffer und beschreibt zusätzliche Puffer (z. b. Tiefe, Kumulation, Schablone und Zusatz), die von der Hauptebene verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d8186-110">Each pixel format describes the depth and other characteristics of the main color buffers and describes additional buffers (such as depth, accumulation, stencil, and auxiliary) that the main plane uses.</span></span> <span data-ttu-id="d8186-111">Die Pixel Formate werden nun erweitert und umfassen Überlagerungs-und unterliegende Puffer.</span><span class="sxs-lookup"><span data-stu-id="d8186-111">Pixel formats are now extended to include overlay and underlay buffers.</span></span>

<span data-ttu-id="d8186-112">Ebenenebenen verfügen immer über einen Farben Puffer in der Vorderseite und können auch Front-und Hintergrundfarben enthalten.</span><span class="sxs-lookup"><span data-stu-id="d8186-112">Layer planes always have a front-left color buffer and also can include front-right and back color buffers.</span></span> <span data-ttu-id="d8186-113">Jede Ebenenebene verfügt über einen bestimmten renderingkontext zum Rendern in die ebenenpuffer.</span><span class="sxs-lookup"><span data-stu-id="d8186-113">Each layer plane has a specific rendering context to render into the layer buffers.</span></span> <span data-ttu-id="d8186-114">Sie können keine GDI-Zeichnungsfunktionen in ebenenebenen verwenden.</span><span class="sxs-lookup"><span data-stu-id="d8186-114">You cannot use GDI drawing functions in layer planes.</span></span>

<span data-ttu-id="d8186-115">Ein Fenster verwaltet die Farb Puffer von ebenenflächen ähnlich der Art und Weise, wie Sie die Farben Puffer der Hauptebene verwaltet.</span><span class="sxs-lookup"><span data-stu-id="d8186-115">A window manages the color buffers of layer planes similarly to the way it manages main-plane color buffers.</span></span> <span data-ttu-id="d8186-116">Sie können mehrere Fenster gleichzeitig mit überlagern und/oder Unterebenen anzeigen.</span><span class="sxs-lookup"><span data-stu-id="d8186-116">You can display multiple windows with overlay and/or underlay planes at the same time.</span></span> <span data-ttu-id="d8186-117">Sie können keine unverankerten über Lagerungs Fenster aufweisen, die über ein beliebiges Fenster in der hauptzeichnungs Ebene verschoben werden können.</span><span class="sxs-lookup"><span data-stu-id="d8186-117">You cannot have free-floating overlay windows that can move over any window in the main drawing plane.</span></span> <span data-ttu-id="d8186-118">Darüber hinaus können Sie keine Hardware-Popup Flächen verwenden, die keine transparente Farbe aufweisen, da die zugrunde liegenden Flächen in einem Fenster jederzeit überladen werden.</span><span class="sxs-lookup"><span data-stu-id="d8186-118">In addition, because it would obscure underlying planes in a window at all times, you cannot use hardware pop-up planes that have no transparent color.</span></span>

<span data-ttu-id="d8186-119">Jede Ebenenebene in einem Fenster verfügt über eine zugeordnete Palette.</span><span class="sxs-lookup"><span data-stu-id="d8186-119">Each layer plane in a window has an associated palette.</span></span> <span data-ttu-id="d8186-120">Sie können die Palette einer Farb Index Ebene festlegen, aber die Palette einer RGBA-Farbebene ist fest.</span><span class="sxs-lookup"><span data-stu-id="d8186-120">You can set the palette of a color-index layer plane, but the palette of an RGBA color plane is fixed.</span></span> <span data-ttu-id="d8186-121">Sie müssen die entsprechende Palette erkennen, wenn sich ein Fenster im Vordergrund befindet.</span><span class="sxs-lookup"><span data-stu-id="d8186-121">You must realize the appropriate palette when a window is in the foreground.</span></span> <span data-ttu-id="d8186-122">Ebenenebenen verfügen über eine transparente Pixelfarbe oder einen transparenten Index, mit dem alle zugrunde liegenden ebenenebenen durch angezeigt werden können.</span><span class="sxs-lookup"><span data-stu-id="d8186-122">Layer planes have a transparent pixel color or index that enables any underlying layer planes to show through.</span></span>

<span data-ttu-id="d8186-123">Sie können den Zustand eines renderingkontexts in einen anderen renderingkontext auf einer separaten Ebenenebene kopieren.</span><span class="sxs-lookup"><span data-stu-id="d8186-123">You can copy the state of a rendering context to another rendering context in a separate layer plane.</span></span> <span data-ttu-id="d8186-124">Sie können auch anzeigen Listen zwischen renderingkontexten in verschiedenen ebenenebenen freigeben.</span><span class="sxs-lookup"><span data-stu-id="d8186-124">You can also share display lists among rendering contexts in different layer planes.</span></span>

<span data-ttu-id="d8186-125">Die folgenden Funktionen werden mit ebenenebenen verwendet:</span><span class="sxs-lookup"><span data-stu-id="d8186-125">The following functions are used with layer planes:</span></span>

-   [<span data-ttu-id="d8186-126">**wglcopycontext**</span><span class="sxs-lookup"><span data-stu-id="d8186-126">**wglCopyContext**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglcopycontext)
-   [<span data-ttu-id="d8186-127">**wglkreatelayercontext**</span><span class="sxs-lookup"><span data-stu-id="d8186-127">**wglCreateLayerContext**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglcreatelayercontext)
-   [<span data-ttu-id="d8186-128">**wgldescribelayerplane**</span><span class="sxs-lookup"><span data-stu-id="d8186-128">**wglDescribeLayerPlane**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wgldescribelayerplane)
-   [<span data-ttu-id="d8186-129">**wglgetlayerpaletteentries**</span><span class="sxs-lookup"><span data-stu-id="d8186-129">**wglGetLayerPaletteEntries**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglgetlayerpaletteentries)
-   [<span data-ttu-id="d8186-130">**wglrealizelayerpalette**</span><span class="sxs-lookup"><span data-stu-id="d8186-130">**wglRealizeLayerPalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglrealizelayerpalette)
-   [<span data-ttu-id="d8186-131">**wglsetlayerpaletteentries**</span><span class="sxs-lookup"><span data-stu-id="d8186-131">**wglSetLayerPaletteEntries**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglsetlayerpaletteentries)
-   [<span data-ttu-id="d8186-132">**wglswaplayerbuffers**</span><span class="sxs-lookup"><span data-stu-id="d8186-132">**wglSwapLayerBuffers**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglswaplayerbuffers)

 

 




