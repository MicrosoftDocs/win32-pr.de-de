---
description: Compositorübergang
ms.assetid: 7903ecd7-88fb-4277-82ee-a7f71cae0412
title: Compositorübergang
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75488e9dbdea4926c515f52352b42f68a2bfa679
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104566272"
---
# <a name="compositor-transition"></a><span data-ttu-id="deb1d-103">Compositorübergang</span><span class="sxs-lookup"><span data-stu-id="deb1d-103">Compositor Transition</span></span>

> [!Note]  
> <span data-ttu-id="deb1d-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="deb1d-104">\[Deprecated.</span></span> <span data-ttu-id="deb1d-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="deb1d-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="deb1d-106">Der Compositor-Übergang setzt ein unter Rechteck aus dem Vordergrund in ein bestimmtes Rechteck im Hintergrund zusammen, ohne den Rest des Hintergrunds zu ändern.</span><span class="sxs-lookup"><span data-stu-id="deb1d-106">The Compositor transition composites a subrectangle from the foreground into a designated rectangle on the background, without altering the rest of the background.</span></span> <span data-ttu-id="deb1d-107">Verwenden Sie diesen Übergang, um Effekte im Bildschirm oder Bild in Bildern zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="deb1d-107">Use this transition to create split-screen or picture-in-picture effects.</span></span>

<span data-ttu-id="deb1d-108">In der folgenden Abbildung ist der compositorübergang dargestellt:</span><span class="sxs-lookup"><span data-stu-id="deb1d-108">The following image shows the compositor transition:</span></span>

![compositorübergang](images/trans-compositor.png)

<span data-ttu-id="deb1d-110">Klassen-ID (CLSID): {BB44391D-6ABD-422f-9E2E-385C9DFF51FC}</span><span class="sxs-lookup"><span data-stu-id="deb1d-110">Class ID (CLSID): {BB44391D-6ABD-422f-9E2E-385C9DFF51FC}</span></span>

<span data-ttu-id="deb1d-111">CLSID-Variablen Name: CLSID \_ dxtcompositor</span><span class="sxs-lookup"><span data-stu-id="deb1d-111">CLSID Variable Name: CLSID\_DxtCompositor</span></span>

<span data-ttu-id="deb1d-112">Anzeige Name: "dxtcompositor"</span><span class="sxs-lookup"><span data-stu-id="deb1d-112">Friendly Name: "DxtCompositor"</span></span>

<span data-ttu-id="deb1d-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="deb1d-113">Properties</span></span>



| <span data-ttu-id="deb1d-114">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="deb1d-114">Property</span></span>   | <span data-ttu-id="deb1d-115">type</span><span class="sxs-lookup"><span data-stu-id="deb1d-115">Type</span></span> | <span data-ttu-id="deb1d-116">Standard</span><span class="sxs-lookup"><span data-stu-id="deb1d-116">Default</span></span> | <span data-ttu-id="deb1d-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="deb1d-117">Description</span></span>                                                    |
|------------|------|---------|----------------------------------------------------------------|
| <span data-ttu-id="deb1d-118">Höhe</span><span class="sxs-lookup"><span data-stu-id="deb1d-118">Height</span></span>     | <span data-ttu-id="deb1d-119">long</span><span class="sxs-lookup"><span data-stu-id="deb1d-119">long</span></span> | <span data-ttu-id="deb1d-120">0</span><span class="sxs-lookup"><span data-stu-id="deb1d-120">0</span></span>       | <span data-ttu-id="deb1d-121">Höhe des Ziel Rechtecks in Pixel.</span><span class="sxs-lookup"><span data-stu-id="deb1d-121">Height of the target rectangle, in pixels.</span></span>                     |
| <span data-ttu-id="deb1d-122">OffsetX</span><span class="sxs-lookup"><span data-stu-id="deb1d-122">OffsetX</span></span>    | <span data-ttu-id="deb1d-123">long</span><span class="sxs-lookup"><span data-stu-id="deb1d-123">long</span></span> | <span data-ttu-id="deb1d-124">0</span><span class="sxs-lookup"><span data-stu-id="deb1d-124">0</span></span>       | <span data-ttu-id="deb1d-125">Horizontaler Offset des Ziel Rechtecks in Pixel.</span><span class="sxs-lookup"><span data-stu-id="deb1d-125">Horizontal offset of the target rectangle, in pixels.</span></span>          |
| <span data-ttu-id="deb1d-126">OffsetY</span><span class="sxs-lookup"><span data-stu-id="deb1d-126">OffsetY</span></span>    | <span data-ttu-id="deb1d-127">long</span><span class="sxs-lookup"><span data-stu-id="deb1d-127">long</span></span> | <span data-ttu-id="deb1d-128">0</span><span class="sxs-lookup"><span data-stu-id="deb1d-128">0</span></span>       | <span data-ttu-id="deb1d-129">Vertikaler Offset des Ziel Rechtecks in Pixel.</span><span class="sxs-lookup"><span data-stu-id="deb1d-129">Vertical offset of the target rectangle, in pixels.</span></span>            |
| <span data-ttu-id="deb1d-130">SrcHeight</span><span class="sxs-lookup"><span data-stu-id="deb1d-130">SrcHeight</span></span>  | <span data-ttu-id="deb1d-131">long</span><span class="sxs-lookup"><span data-stu-id="deb1d-131">long</span></span> | <span data-ttu-id="deb1d-132">0</span><span class="sxs-lookup"><span data-stu-id="deb1d-132">0</span></span>       | <span data-ttu-id="deb1d-133">Die Höhe des unter Rechtecks in der Quelle in Pixel.</span><span class="sxs-lookup"><span data-stu-id="deb1d-133">The height of the subrectangle on the source, in pixels.</span></span>       |
| <span data-ttu-id="deb1d-134">Srcoffsetx</span><span class="sxs-lookup"><span data-stu-id="deb1d-134">SrcOffsetX</span></span> | <span data-ttu-id="deb1d-135">long</span><span class="sxs-lookup"><span data-stu-id="deb1d-135">long</span></span> | <span data-ttu-id="deb1d-136">0</span><span class="sxs-lookup"><span data-stu-id="deb1d-136">0</span></span>       | <span data-ttu-id="deb1d-137">Die x-Koordinate des unter Rechtecks in der Quelle in Pixel.</span><span class="sxs-lookup"><span data-stu-id="deb1d-137">The x-coordinate of the subrectangle on the source, in pixels.</span></span> |
| <span data-ttu-id="deb1d-138">Srcoff-Ty</span><span class="sxs-lookup"><span data-stu-id="deb1d-138">SrcOffsetY</span></span> | <span data-ttu-id="deb1d-139">long</span><span class="sxs-lookup"><span data-stu-id="deb1d-139">long</span></span> | <span data-ttu-id="deb1d-140">0</span><span class="sxs-lookup"><span data-stu-id="deb1d-140">0</span></span>       | <span data-ttu-id="deb1d-141">Die y-Koordinate des unter Rechtecks in der Quelle in Pixel.</span><span class="sxs-lookup"><span data-stu-id="deb1d-141">The y-coordinate of the subrectangle on the source, in pixels.</span></span> |
| <span data-ttu-id="deb1d-142">SrcWidth</span><span class="sxs-lookup"><span data-stu-id="deb1d-142">SrcWidth</span></span>   | <span data-ttu-id="deb1d-143">long</span><span class="sxs-lookup"><span data-stu-id="deb1d-143">long</span></span> | <span data-ttu-id="deb1d-144">0</span><span class="sxs-lookup"><span data-stu-id="deb1d-144">0</span></span>       | <span data-ttu-id="deb1d-145">Die Breite des unter Rechtecks in der Quelle in Pixel.</span><span class="sxs-lookup"><span data-stu-id="deb1d-145">The width of the subrectangle on the source, in pixels.</span></span>        |
| <span data-ttu-id="deb1d-146">Breite</span><span class="sxs-lookup"><span data-stu-id="deb1d-146">Width</span></span>      | <span data-ttu-id="deb1d-147">long</span><span class="sxs-lookup"><span data-stu-id="deb1d-147">long</span></span> | <span data-ttu-id="deb1d-148">0</span><span class="sxs-lookup"><span data-stu-id="deb1d-148">0</span></span>       | <span data-ttu-id="deb1d-149">Breite des Ziel Rechtecks in Pixel.</span><span class="sxs-lookup"><span data-stu-id="deb1d-149">Width of the target rectangle, in pixels.</span></span>                      |



 

<span data-ttu-id="deb1d-150">Diese Eigenschaften werden im folgenden Diagramm veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="deb1d-150">The following diagram illustrates these properties:</span></span>

![Compositor-Eigenschaften](images/compmeasure.png)

## <a name="related-topics"></a><span data-ttu-id="deb1d-152">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="deb1d-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="deb1d-153">Übergänge und Effekte</span><span class="sxs-lookup"><span data-stu-id="deb1d-153">Transitions and Effects</span></span>](transitions-and-effects.md)
</dt> </dl>

 

 



