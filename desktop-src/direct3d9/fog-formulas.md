---
description: C++-Anwendungen können steuern, wie sich der Nebel auf die Farbe von Objekten in einer Szene auswirkt, indem Sie ändern, wie Microsoft Direct3D Nebeleffekte über die Distanz berechnet.
ms.assetid: b7148ae8-45c7-4dbe-8295-0335c7fdeff0
title: Nebel Formeln (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75150a00d491f1e3fc1ea1444209449c1c2a825d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860195"
---
# <a name="fog-formulas-direct3d-9"></a><span data-ttu-id="ed30b-103">Nebel Formeln (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="ed30b-103">Fog Formulas (Direct3D 9)</span></span>

<span data-ttu-id="ed30b-104">C++-Anwendungen können steuern, wie sich der Nebel auf die Farbe von Objekten in einer Szene auswirkt, indem Sie ändern, wie Microsoft Direct3D Nebeleffekte über die Distanz berechnet.</span><span class="sxs-lookup"><span data-stu-id="ed30b-104">C++ applications can control how fog affects the color of objects in a scene by changing how Microsoft Direct3D computes fog effects over distance.</span></span> <span data-ttu-id="ed30b-105">Der [**D3DFOGMODE**](./d3dfogmode.md) -Enumerationstyp enthält Elemente, die die drei Nebel Formeln bezeichnen.</span><span class="sxs-lookup"><span data-stu-id="ed30b-105">The [**D3DFOGMODE**](./d3dfogmode.md) enumerated type contains members that identify the three fog formulas.</span></span> <span data-ttu-id="ed30b-106">Alle Formeln berechnen einen Nebel Faktor als eine Funktion der Entfernung, wobei die Parameter angegeben werden, die von der Anwendung festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="ed30b-106">All formulas calculate a fog factor as a function of distance, given parameters that your application sets.</span></span>

## <a name="linear-fog"></a><span data-ttu-id="ed30b-107">Linearer Nebel</span><span class="sxs-lookup"><span data-stu-id="ed30b-107">Linear Fog</span></span>

<span data-ttu-id="ed30b-108">Dies wird mit der folgenden D3DFOG \_ linearen Gleichung festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ed30b-108">This is set with the following D3DFOG\_LINEAR equation.</span></span>

![Gleichung von Direct3D linear Nebel](images/fogliner.png)

<span data-ttu-id="ed30b-110">where</span><span class="sxs-lookup"><span data-stu-id="ed30b-110">where</span></span>

-   <span data-ttu-id="ed30b-111">Start ist der Abstand, bei dem die Nebeleffekte beginnen.</span><span class="sxs-lookup"><span data-stu-id="ed30b-111">start is the distance at which fog effects begin.</span></span>
-   <span data-ttu-id="ed30b-112">"End" ist die Entfernung, bei der die Auswirkungen von Nebel nicht mehr zunehmen.</span><span class="sxs-lookup"><span data-stu-id="ed30b-112">end is the distance at which fog effects no longer increase.</span></span>
-   <span data-ttu-id="ed30b-113">d stellt die Tiefe oder die Entfernung vom Standpunkt dar.</span><span class="sxs-lookup"><span data-stu-id="ed30b-113">d represents depth, or the distance from the viewpoint.</span></span> <span data-ttu-id="ed30b-114">Bei Bereichs basiertem Nebel ist der Wert für d der Abstand zwischen der Kameraposition und einem Scheitelpunkt.</span><span class="sxs-lookup"><span data-stu-id="ed30b-114">For range based fog, the value for d is the distance between the camera position and a vertex.</span></span> <span data-ttu-id="ed30b-115">Bei einem nicht Bereichs basierten Nebel ist der Wert für d der absolute Wert der Z-Koordinate im Kamerabereich.</span><span class="sxs-lookup"><span data-stu-id="ed30b-115">For non-range based fog, the value for d is the absolute value of the Z-coordinate in camera space.</span></span>

## <a name="exponential-fog"></a><span data-ttu-id="ed30b-116">Exponentieller Nebel</span><span class="sxs-lookup"><span data-stu-id="ed30b-116">Exponential Fog</span></span>

<span data-ttu-id="ed30b-117">Lineare und exponentielle Formeln werden sowohl für Pixel Nebel als auch für Scheitelpunkt Nebel unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ed30b-117">Linear and exponential formulas are supported for both pixel fog and vertex fog.</span></span>

<span data-ttu-id="ed30b-118">Dies wird mit der folgenden D3DFOG \_ Exp-Gleichung festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ed30b-118">This is set with the following D3DFOG\_EXP equation.</span></span>

![Gleichung des exponentiellen Direct3D-Nebel Werts](images/fogexp.png)

<span data-ttu-id="ed30b-120">where</span><span class="sxs-lookup"><span data-stu-id="ed30b-120">where</span></span>

-   <span data-ttu-id="ed30b-121">e ist die Basis des natürlichen Logarithmus (ungefähr 2,71828).</span><span class="sxs-lookup"><span data-stu-id="ed30b-121">e is the base of natural logarithms (approximately 2.71828).</span></span>
-   <span data-ttu-id="ed30b-122">die Dichte ist eine beliebige Nebeldichte, die zwischen 0,0 und 1,0 liegen kann.</span><span class="sxs-lookup"><span data-stu-id="ed30b-122">density is an arbitrary fog density that can range from 0.0 to 1.0.</span></span>
-   <span data-ttu-id="ed30b-123">d stellt die Tiefe oder die Entfernung vom Standpunkt dar, wie bereits erwähnt.</span><span class="sxs-lookup"><span data-stu-id="ed30b-123">d represents depth, or the distance from the viewpoint, as stated earlier.</span></span>

<span data-ttu-id="ed30b-124">Dies wird mit der folgenden D3DFOG \_ exp2 Gleichung festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ed30b-124">This is set with the following D3DFOG\_EXP2 equation.</span></span>

![Gleichung von Direct3D exponentiellem 2-Nebel](images/fogexp2.png)

<span data-ttu-id="ed30b-126">where</span><span class="sxs-lookup"><span data-stu-id="ed30b-126">where</span></span>

-   <span data-ttu-id="ed30b-127">e ist die Basis des natürlichen Logarithmus, wie oben angegeben.</span><span class="sxs-lookup"><span data-stu-id="ed30b-127">e is the base of natural logarithms as stated above.</span></span>
-   <span data-ttu-id="ed30b-128">die Dichte ist eine beliebige Nebeldichte, die wie oben angegeben zwischen 0,0 und 1,0 reichen kann.</span><span class="sxs-lookup"><span data-stu-id="ed30b-128">density is an arbitrary fog density that can range from 0.0 to 1.0 as stated above.</span></span>
-   <span data-ttu-id="ed30b-129">d stellt die Tiefe oder die Entfernung vom Standpunkt dar, wie oben angegeben.</span><span class="sxs-lookup"><span data-stu-id="ed30b-129">d represents depth, or the distance from the viewpoint, as stated above.</span></span>

> [!Note]  
> <span data-ttu-id="ed30b-130">Das System speichert den Nebel Faktor in der Alpha Komponente der Glanz Farbe eines Scheitel Punkts.</span><span class="sxs-lookup"><span data-stu-id="ed30b-130">The system stores the fog factor in the alpha component of the specular color for a vertex.</span></span> <span data-ttu-id="ed30b-131">Wenn Ihre Anwendung ihre eigene Transformation und Beleuchtung durchführt, können Sie die Werte für den Nebel Faktor manuell einfügen, damit Sie vom System während des Renderings angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="ed30b-131">If your application performs its own transformation and lighting, you can insert fog factor values manually, to be applied by the system during rendering.</span></span>

 

<span data-ttu-id="ed30b-132">Das folgende Diagramm zeigt diese Formeln, wobei allgemeine Werte als in den Formel Parametern verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ed30b-132">The following graph shows these formulas, using common values as in the formula parameters.</span></span>

![Diagramm der Nebel Formeln in der Entfernung und der Farbmenge](images/foggraph.png)

<span data-ttu-id="ed30b-134">D3DFOG \_ linear ist 1,0 am Anfang und 0,0 am Ende.</span><span class="sxs-lookup"><span data-stu-id="ed30b-134">D3DFOG\_LINEAR is 1.0 at start and 0.0 at end.</span></span> <span data-ttu-id="ed30b-135">Es wird nicht in Bezug auf die Near-oder Far-Plane gemessen.</span><span class="sxs-lookup"><span data-stu-id="ed30b-135">It is not measured relative to the near or far planes.</span></span>

<span data-ttu-id="ed30b-136">Wenn Direct3D Nebeleffekte berechnet, wird der Nebel Faktor aus einer der vorangehenden Gleichungen in der folgenden Mischungs Gleichung verwendet.</span><span class="sxs-lookup"><span data-stu-id="ed30b-136">When Direct3D calculates fog effects, it uses the fog factor from one of the preceding equations in the following blending equation.</span></span>

![Gleichung von Nebeleffekten für Direct3D](images/fogcalc.png)

<span data-ttu-id="ed30b-138">Mit dieser Formel wird die Farbe des aktuellen Polygons c durch den Nebel Faktor f effektiv skaliert, und das Produkt wird der Nebelfarbe C hinzugefügt, die durch die bitweise Umkehrung des Nebel Faktors skaliert wird.</span><span class="sxs-lookup"><span data-stu-id="ed30b-138">This formula effectively scales the color of the current polygon C by the fog factor f, and adds the product to the fog color C, scaled by the bitwise inverse of the fog factor.</span></span> <span data-ttu-id="ed30b-139">Der resultierende Farbwert ist eine Mischung aus der Nebelfarbe und der ursprünglichen Farbe als Faktor der Entfernung.</span><span class="sxs-lookup"><span data-stu-id="ed30b-139">The resulting color value is a blend of the fog color and the original color, as a factor of distance.</span></span> <span data-ttu-id="ed30b-140">Die Formel gilt für alle Geräte, die in Microsoft DirectX 7,0 und höher unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="ed30b-140">The formula applies to all devices supported in Microsoft DirectX 7.0 and later.</span></span> <span data-ttu-id="ed30b-141">Bei der Legacy-Anlauf Vorrichtung skaliert der Nebel Faktor die diffusen und Glanz Farben, die auf den Bereich von 0,0 und 1,0 (einschließlich) zugeschnitten sind.</span><span class="sxs-lookup"><span data-stu-id="ed30b-141">For the legacy ramp device, the fog factor scales the diffuse and specular color components, clamped to the range of 0.0 and 1.0, inclusive.</span></span> <span data-ttu-id="ed30b-142">Der Nebel Faktor beginnt in der Regel bei 1,0 für die nahe Ebene und sinkt auf der äußersten Ebene auf 0,0.</span><span class="sxs-lookup"><span data-stu-id="ed30b-142">The fog factor typically starts at 1.0 for the near plane and decreases to 0.0 at the far plane.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ed30b-143">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ed30b-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed30b-144">Nebel Typen</span><span class="sxs-lookup"><span data-stu-id="ed30b-144">Fog Types</span></span>](fog-types.md)
</dt> </dl>

 

 
