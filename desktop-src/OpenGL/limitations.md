---
title: Einschränkungen
description: Einschränkungen
ms.assetid: 5f41620d-dde0-4e82-92f0-ada9d4acf127
keywords:
- OpenGL unter Windows, Einschränkungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 478a139326f74c236ca0109fddbbc3d4ffb46e1a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709725"
---
# <a name="limitations"></a><span data-ttu-id="b1701-104">Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="b1701-104">Limitations</span></span>

<span data-ttu-id="b1701-105">Die generische Implementierung weist die folgenden Einschränkungen auf:</span><span class="sxs-lookup"><span data-stu-id="b1701-105">The generic implementation has the following limitations:</span></span>

-   <span data-ttu-id="b1701-106">Drucken.</span><span class="sxs-lookup"><span data-stu-id="b1701-106">Printing.</span></span>

    <span data-ttu-id="b1701-107">Sie können ein OpenGL-Bild direkt mit Metadateien an einen Drucker drucken.</span><span class="sxs-lookup"><span data-stu-id="b1701-107">You can print an OpenGL image directly to a printer using metafiles only.</span></span> <span data-ttu-id="b1701-108">Weitere Informationen finden Sie unter [Drucken eines OpenGL-Bilds](printing-an-opengl-image.md).</span><span class="sxs-lookup"><span data-stu-id="b1701-108">For more information, see [Printing an OpenGL Image](printing-an-opengl-image.md).</span></span>

-   <span data-ttu-id="b1701-109">OpenGL-und GDI-Grafiken können nicht in einem Fenster mit doppelter puffert gemischt werden.</span><span class="sxs-lookup"><span data-stu-id="b1701-109">OpenGL and GDI graphics cannot be mixed in a double-buffered window.</span></span>

    <span data-ttu-id="b1701-110">Eine Anwendung kann sowohl OpenGL-Grafiken als auch GDI-Grafiken direkt in ein nur-gepuffertes Fenster, aber nicht in ein Fenster mit doppelter puffert zeichnen.</span><span class="sxs-lookup"><span data-stu-id="b1701-110">An application can directly draw both OpenGL graphics and GDI graphics into a single-buffered window, but not into a double-buffered window.</span></span>

-   <span data-ttu-id="b1701-111">Es sind keine Hardware Farbpaletten pro Fenster vorhanden.</span><span class="sxs-lookup"><span data-stu-id="b1701-111">There are no per-window hardware color palettes.</span></span>

    <span data-ttu-id="b1701-112">Windows verfügt über eine einzelne System Hardware-Farbpalette, die für den gesamten Bildschirm gilt.</span><span class="sxs-lookup"><span data-stu-id="b1701-112">Windows has a single system hardware color palette, which applies to the whole screen.</span></span> <span data-ttu-id="b1701-113">Ein OpenGL-Fenster kann nicht über eine eigene Hardware Palette verfügen, kann aber über eine eigene logische Palette verfügen.</span><span class="sxs-lookup"><span data-stu-id="b1701-113">An OpenGL window cannot have its own hardware palette, but can have its own logical palette.</span></span> <span data-ttu-id="b1701-114">Zu diesem Zweck muss Sie zu einer palettenfähigen Anwendung werden.</span><span class="sxs-lookup"><span data-stu-id="b1701-114">To do so, it must become a palette-aware application.</span></span> <span data-ttu-id="b1701-115">Weitere Informationen finden Sie unter [OpenGL-Farbmodi und Windows-Palettenverwaltung](opengl-color-modes-and-windows-palette-management.md).</span><span class="sxs-lookup"><span data-stu-id="b1701-115">For more information, see [OpenGL Color Modes and Windows Palette Management](opengl-color-modes-and-windows-palette-management.md).</span></span>

-   <span data-ttu-id="b1701-116">Es gibt keine direkte Unterstützung für die Zwischenablage, den dynamischen Datenaustausch (DDE) oder OLE.</span><span class="sxs-lookup"><span data-stu-id="b1701-116">There is no direct support for the Clipboard, dynamic data exchange (DDE), or OLE.</span></span>

    <span data-ttu-id="b1701-117">Ein Fenster mit OpenGL-Grafiken unterstützt diese Windows-Funktionen nicht direkt.</span><span class="sxs-lookup"><span data-stu-id="b1701-117">A window with OpenGL graphics does not directly support these Windows capabilities.</span></span> <span data-ttu-id="b1701-118">Es gibt jedoch Problem Umgehungen für die Verwendung der Zwischenablage.</span><span class="sxs-lookup"><span data-stu-id="b1701-118">There are workarounds, however, for using the Clipboard.</span></span> <span data-ttu-id="b1701-119">Weitere Informationen finden Sie unter [Kopieren eines OpenGL-Bilds in die Zwischenablage](copying-an-opengl-image-to-the-clipboard.md).</span><span class="sxs-lookup"><span data-stu-id="b1701-119">For more information, see [Copying an OpenGL Image to the Clipboard](copying-an-opengl-image-to-the-clipboard.md).</span></span>

-   <span data-ttu-id="b1701-120">Die C++-Klassenbibliothek von Inventor 2,0 ist nicht enthalten.</span><span class="sxs-lookup"><span data-stu-id="b1701-120">The Inventor 2.0 C++ class library is not included.</span></span>

    <span data-ttu-id="b1701-121">Die Erfinder Klassenbibliothek, die auf OpenGL basiert, bietet Konstrukte höherer Ebene für die Programmierung von 3D-Grafiken.</span><span class="sxs-lookup"><span data-stu-id="b1701-121">The Inventor class library, built on top of OpenGL, provides higher-level constructs for programming 3-D graphics.</span></span> <span data-ttu-id="b1701-122">Sie ist nicht in der aktuellen Version der Microsoft-Implementierung von OpenGL für Windows enthalten.</span><span class="sxs-lookup"><span data-stu-id="b1701-122">It is not included in the current version of Microsoft's implementation of OpenGL for Windows.</span></span>

-   <span data-ttu-id="b1701-123">Es gibt keine Unterstützung für die folgenden Pixel Format Features: Stereotyp, Alpha bitplane und hilfspuffer.</span><span class="sxs-lookup"><span data-stu-id="b1701-123">There is no support for the following pixel format features: stereoscopic images, alpha bitplanes, and auxiliary buffers.</span></span>

    <span data-ttu-id="b1701-124">Es gibt jedoch Unterstützung für mehrere zusätzliche Puffer, einschließlich Schablonen Puffer, Akkumulations Puffer, Hintergrund Puffer (doppelte Pufferung), über Lagerungs-und unterebenenpuffer und tiefen Puffer (z-Achse).</span><span class="sxs-lookup"><span data-stu-id="b1701-124">There is, however, support for several ancillary buffers including: stencil buffer, accumulation buffer, back buffer (double buffering), overlay and underlay plane buffer, and depth (z-axis) buffer.</span></span>

 

 




