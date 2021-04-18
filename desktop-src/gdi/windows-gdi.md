---
description: Die Microsoft Windows Graphics Device Interface (GDI) ermöglicht Anwendungen die Verwendung von Grafiken und formatiertem Text sowohl auf der Videoanzeige als auch auf dem Drucker.
ms.assetid: b58ab70a-2071-4264-9d20-c0b0aaf8dc5c
title: Windows GDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41f5fc6ba9f4eb99786b21daeff2e1c48b9ce09d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979360"
---
# <a name="windows-gdi"></a><span data-ttu-id="b2533-103">Windows GDI</span><span class="sxs-lookup"><span data-stu-id="b2533-103">Windows GDI</span></span>

## <a name="purpose"></a><span data-ttu-id="b2533-104">Zweck</span><span class="sxs-lookup"><span data-stu-id="b2533-104">Purpose</span></span>

<span data-ttu-id="b2533-105">Die Microsoft Windows Graphics Device Interface (GDI) ermöglicht Anwendungen die Verwendung von Grafiken und formatiertem Text sowohl auf der Videoanzeige als auch auf dem Drucker.</span><span class="sxs-lookup"><span data-stu-id="b2533-105">The Microsoft Windows graphics device interface (GDI) enables applications to use graphics and formatted text on both the video display and the printer.</span></span> <span data-ttu-id="b2533-106">Windows-basierte Anwendungen greifen nicht direkt auf die Grafikhardware zu.</span><span class="sxs-lookup"><span data-stu-id="b2533-106">Windows-based applications do not access the graphics hardware directly.</span></span> <span data-ttu-id="b2533-107">Stattdessen interagiert GDI im Auftrag von Anwendungen mit Gerätetreibern.</span><span class="sxs-lookup"><span data-stu-id="b2533-107">Instead, GDI interacts with device drivers on behalf of applications.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="b2533-108">Anwendungsbereich</span><span class="sxs-lookup"><span data-stu-id="b2533-108">Where applicable</span></span>

<span data-ttu-id="b2533-109">GDI kann in allen Windows-basierten Anwendungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b2533-109">GDI can be used in all Windows-based applications.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="b2533-110">Entwicklergruppe</span><span class="sxs-lookup"><span data-stu-id="b2533-110">Developer audience</span></span>

<span data-ttu-id="b2533-111">Diese API ist für die Verwendung durch C/C++-Programmierer konzipiert.</span><span class="sxs-lookup"><span data-stu-id="b2533-111">This API is designed for use by C/C++ programmers.</span></span> <span data-ttu-id="b2533-112">Es ist eine Vertrautheit mit der [Nachrichten gesteuerten Windows-Architektur](../learnwin32/window-messages.md) erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b2533-112">Familiarity with the Windows [message-driven architecture](../learnwin32/window-messages.md) is required.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="b2533-113">Laufzeitanforderungen</span><span class="sxs-lookup"><span data-stu-id="b2533-113">Run-time requirements</span></span>

<span data-ttu-id="b2533-114">Informationen dazu, welche Betriebssysteme für die Verwendung einer bestimmten Funktion erforderlich sind, finden Sie im Abschnitt "Anforderungen" in der Dokumentation für die Funktion.</span><span class="sxs-lookup"><span data-stu-id="b2533-114">For information on which operating systems are required to use a particular function, see the Requirements section of the documentation for the function.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b2533-115">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="b2533-115">In this section</span></span>

-   [<span data-ttu-id="b2533-116">Bitmaps</span><span class="sxs-lookup"><span data-stu-id="b2533-116">Bitmaps</span></span>](bitmaps.md)
-   [<span data-ttu-id="b2533-117">Pinsel</span><span class="sxs-lookup"><span data-stu-id="b2533-117">Brushes</span></span>](brushes.md)
-   [<span data-ttu-id="b2533-118">Freistellen</span><span class="sxs-lookup"><span data-stu-id="b2533-118">Clipping</span></span>](clipping.md)
-   [<span data-ttu-id="b2533-119">Farben</span><span class="sxs-lookup"><span data-stu-id="b2533-119">Colors</span></span>](colors.md)
-   [<span data-ttu-id="b2533-120">Koordinaten Bereiche und Transformationen</span><span class="sxs-lookup"><span data-stu-id="b2533-120">Coordinate Spaces and Transformations</span></span>](coordinate-spaces-and-transformations.md)
-   [<span data-ttu-id="b2533-121">Geräte Kontexte</span><span class="sxs-lookup"><span data-stu-id="b2533-121">Device Contexts</span></span>](device-contexts.md)
-   [<span data-ttu-id="b2533-122">Gefüllte Formen</span><span class="sxs-lookup"><span data-stu-id="b2533-122">Filled Shapes</span></span>](filled-shapes.md)
-   [<span data-ttu-id="b2533-123">Schriftarten und Text</span><span class="sxs-lookup"><span data-stu-id="b2533-123">Fonts and Text</span></span>](fonts-and-text.md)
-   [<span data-ttu-id="b2533-124">Linien und Kurven</span><span class="sxs-lookup"><span data-stu-id="b2533-124">Lines and Curves</span></span>](lines-and-curves.md)
-   [<span data-ttu-id="b2533-125">Metadateien</span><span class="sxs-lookup"><span data-stu-id="b2533-125">Metafiles</span></span>](metafiles.md)
-   [<span data-ttu-id="b2533-126">Mehrere Anzeige Monitore</span><span class="sxs-lookup"><span data-stu-id="b2533-126">Multiple Display Monitors</span></span>](multiple-display-monitors.md)
-   [<span data-ttu-id="b2533-127">Zeichnen und zeichnen</span><span class="sxs-lookup"><span data-stu-id="b2533-127">Painting and Drawing</span></span>](painting-and-drawing.md)
-   [<span data-ttu-id="b2533-128">Paths</span><span class="sxs-lookup"><span data-stu-id="b2533-128">Paths</span></span>](paths.md)
-   [<span data-ttu-id="b2533-129">Stifte</span><span class="sxs-lookup"><span data-stu-id="b2533-129">Pens</span></span>](pens.md)
-   <span data-ttu-id="b2533-130">[Druck-und Druck Spooler](/previous-versions//dd162860(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b2533-130">[Printing and Print Spooler](/previous-versions//dd162860(v=vs.85))</span></span>
-   [<span data-ttu-id="b2533-131">Rechtecke</span><span class="sxs-lookup"><span data-stu-id="b2533-131">Rectangles</span></span>](rectangles.md)
-   [<span data-ttu-id="b2533-132">Regionen</span><span class="sxs-lookup"><span data-stu-id="b2533-132">Regions</span></span>](regions.md)

## <a name="related-topics"></a><span data-ttu-id="b2533-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b2533-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2533-134">DirectX</span><span class="sxs-lookup"><span data-stu-id="b2533-134">DirectX</span></span>](https://msdn.microsoft.com/library/aa302281.aspx)
</dt> <dt>

[<span data-ttu-id="b2533-135">GDI+</span><span class="sxs-lookup"><span data-stu-id="b2533-135">GDI+</span></span>](../gdiplus/-gdiplus-gdi-start.md)
</dt> <dt>

[<span data-ttu-id="b2533-136">OpenGL</span><span class="sxs-lookup"><span data-stu-id="b2533-136">OpenGL</span></span>](../opengl/opengl.md)
</dt> <dt>

[<span data-ttu-id="b2533-137">Windows-Abbild Erfassung</span><span class="sxs-lookup"><span data-stu-id="b2533-137">Windows Image Acquisition</span></span>](../wia/-wia-startpage.md)
</dt> </dl>

 

 
