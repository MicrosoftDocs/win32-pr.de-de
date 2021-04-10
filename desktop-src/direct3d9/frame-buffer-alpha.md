---
description: Die Alpha Mischung des Frame Puffers unterscheidet sich von Scheitelpunkt Alpha, Material Alpha und Textur Alpha.
ms.assetid: 3664215d-ad03-400e-beab-b0421cf6b693
title: Frame-Puffer Alpha (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb310e2c66f43282e65425fd0d6c6a24961accaa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123859"
---
# <a name="frame-buffer-alpha-direct3d-9"></a><span data-ttu-id="0cfc0-103">Frame-Puffer Alpha (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0cfc0-103">Frame Buffer Alpha (Direct3D 9)</span></span>

<span data-ttu-id="0cfc0-104">Die Alpha Mischung des Frame Puffers unterscheidet sich von Scheitelpunkt Alpha, Material Alpha und Textur Alpha.</span><span class="sxs-lookup"><span data-stu-id="0cfc0-104">Frame buffer alpha-blending is a bit different than vertex alpha, material alpha, and texture alpha.</span></span> <span data-ttu-id="0cfc0-105">Vertex, Material und Textur-Alpha legen Transparenzwerte fest, die nur für den aktuellen primitiven verwendet werden und selbst keine Auswirkung auf andere primitive haben.</span><span class="sxs-lookup"><span data-stu-id="0cfc0-105">Vertex, material, and texture alpha set transparency values that are used only for the current primitive, and by themselves have no effect on other primitives.</span></span> <span data-ttu-id="0cfc0-106">Mit dem Frame Puffer Alpha-Blending wird gesteuert, wie das aktuelle primitive mit vorhandenen Pixeln im Frame Puffer kombiniert wird, um eine endgültige Pixelfarbe zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="0cfc0-106">Frame buffer alpha-blending controls how the current primitive is combined with existing pixels in the frame buffer to yield a final pixel color.</span></span>

<span data-ttu-id="0cfc0-107">Beim Durchführen einer Alpha Mischung werden zwei Farben kombiniert: eine Quellfarbe und eine Zielfarbe.</span><span class="sxs-lookup"><span data-stu-id="0cfc0-107">When performing alpha blending, two colors are being combined: a source color and a destination color.</span></span> <span data-ttu-id="0cfc0-108">Die Quellfarbe wird vom transparenten Objekt abgeleitet, die Zielfarbe ist die Farbe, die sich bereits am Pixel Speicherort befindet.</span><span class="sxs-lookup"><span data-stu-id="0cfc0-108">The source color is from the transparent object, the destination color is the color already at the pixel location.</span></span> <span data-ttu-id="0cfc0-109">Die Zielfarbe ist das Ergebnis des Renderings eines anderen Objekts hinter dem transparenten Objekt, d. h. dem Objekt, das durch das transparente Objekt sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="0cfc0-109">The destination color is the result of rendering some other object that is behind the transparent object, that is, the object that will be visible through the transparent object.</span></span> <span data-ttu-id="0cfc0-110">Alpha Blending verwendet eine Formel, um das Verhältnis zwischen den Quell-und Ziel Objekten zu steuern.</span><span class="sxs-lookup"><span data-stu-id="0cfc0-110">Alpha blending uses a formula to control the ratio between the source and destination objects.</span></span>


```
Final Color = ObjectColor * SourceBlendFactor + PixelColor * DestinationBlendFactor 
```



<span data-ttu-id="0cfc0-111">Objectcolor ist der Beitrag des primitiven, der an der aktuellen Pixelposition gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="0cfc0-111">ObjectColor is the contribution from the primitive being rendered at the current pixel location.</span></span> <span data-ttu-id="0cfc0-112">Pixel Color ist der Beitrag des Frame Puffers an der aktuellen Pixelposition.</span><span class="sxs-lookup"><span data-stu-id="0cfc0-112">PixelColor is the contribution from the frame buffer at the current pixel location.</span></span>

<span data-ttu-id="0cfc0-113">Eine Reihe von Alpha Blend-Faktoren, die verwendet werden können, sind unten aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="0cfc0-113">The set of alpha blend factors that can be used are listed below.</span></span>



| <span data-ttu-id="0cfc0-114">Blend-modusfaktor</span><span class="sxs-lookup"><span data-stu-id="0cfc0-114">Blend mode factor</span></span>         | <span data-ttu-id="0cfc0-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0cfc0-115">Description</span></span>                                                                                                                                                                              |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0cfc0-116">D3DBLEND \_ 0</span><span class="sxs-lookup"><span data-stu-id="0cfc0-116">D3DBLEND\_ZERO</span></span>            | <span data-ttu-id="0cfc0-117">(0, 0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="0cfc0-117">(0, 0, 0, 0)</span></span>                                                                                                                                                                             |
| <span data-ttu-id="0cfc0-118">D3DBLEND \_</span><span class="sxs-lookup"><span data-stu-id="0cfc0-118">D3DBLEND\_ONE</span></span>             | <span data-ttu-id="0cfc0-119">(1, 1, 1, 1)</span><span class="sxs-lookup"><span data-stu-id="0cfc0-119">(1, 1, 1, 1)</span></span>                                                                                                                                                                             |
| <span data-ttu-id="0cfc0-120">D3DBLEND \_ srccolor</span><span class="sxs-lookup"><span data-stu-id="0cfc0-120">D3DBLEND\_SRCCOLOR</span></span>        | <span data-ttu-id="0cfc0-121">(RS, GS, SB, as)</span><span class="sxs-lookup"><span data-stu-id="0cfc0-121">(Rs, Gs, Bs, As)</span></span>                                                                                                                                                                         |
| <span data-ttu-id="0cfc0-122">D3DBLEND- \_ invsrccolor</span><span class="sxs-lookup"><span data-stu-id="0cfc0-122">D3DBLEND\_INVSRCCOLOR</span></span>     | <span data-ttu-id="0cfc0-123">(1-RS, 1-GS, 1-SB, 1-AS)</span><span class="sxs-lookup"><span data-stu-id="0cfc0-123">(1-Rs, 1-Gs, 1-Bs, 1-As)</span></span>                                                                                                                                                                 |
| <span data-ttu-id="0cfc0-124">D3DBLEND \_ srcalpha</span><span class="sxs-lookup"><span data-stu-id="0cfc0-124">D3DBLEND\_SRCALPHA</span></span>        | <span data-ttu-id="0cfc0-125">(AS, as, as, as)</span><span class="sxs-lookup"><span data-stu-id="0cfc0-125">(As, As, As, As)</span></span>                                                                                                                                                                         |
| <span data-ttu-id="0cfc0-126">D3DBLEND- \_ invsrcalpha</span><span class="sxs-lookup"><span data-stu-id="0cfc0-126">D3DBLEND\_INVSRCALPHA</span></span>     | <span data-ttu-id="0cfc0-127">(1-AS, 1-AS, 1-AS, 1-AS)</span><span class="sxs-lookup"><span data-stu-id="0cfc0-127">(1-As, 1-As, 1-As, 1-As)</span></span>                                                                                                                                                                 |
| <span data-ttu-id="0cfc0-128">D3DBLEND \_ -Debug</span><span class="sxs-lookup"><span data-stu-id="0cfc0-128">D3DBLEND\_DESTALPHA</span></span>       | <span data-ttu-id="0cfc0-129">(AD, AD, AD, AD)</span><span class="sxs-lookup"><span data-stu-id="0cfc0-129">(Ad, Ad, Ad, Ad)</span></span>                                                                                                                                                                         |
| <span data-ttu-id="0cfc0-130">D3DBLEND- \_ invwastalpha</span><span class="sxs-lookup"><span data-stu-id="0cfc0-130">D3DBLEND\_INVDESTALPHA</span></span>    | <span data-ttu-id="0cfc0-131">(1-AD, 1-AD, 1-AD, 1-AD)</span><span class="sxs-lookup"><span data-stu-id="0cfc0-131">(1-Ad, 1-Ad, 1-Ad, 1-Ad)</span></span>                                                                                                                                                                 |
| <span data-ttu-id="0cfc0-132">D3DBLEND \_ destcolor</span><span class="sxs-lookup"><span data-stu-id="0cfc0-132">D3DBLEND\_DESTCOLOR</span></span>       | <span data-ttu-id="0cfc0-133">(RD, GD, BD, AD)</span><span class="sxs-lookup"><span data-stu-id="0cfc0-133">(Rd, Gd, Bd, Ad)</span></span>                                                                                                                                                                         |
| <span data-ttu-id="0cfc0-134">D3DBLEND \_ invdestcolor</span><span class="sxs-lookup"><span data-stu-id="0cfc0-134">D3DBLEND\_INVDESTCOLOR</span></span>    | <span data-ttu-id="0cfc0-135">(1-RD, 1-GD, 1-BD, 1-AD)</span><span class="sxs-lookup"><span data-stu-id="0cfc0-135">(1-Rd, 1-Gd, 1-Bd, 1-Ad)</span></span>                                                                                                                                                                 |
| <span data-ttu-id="0cfc0-136">D3DBLEND \_ srcalphasat</span><span class="sxs-lookup"><span data-stu-id="0cfc0-136">D3DBLEND\_SRCALPHASAT</span></span>     | <span data-ttu-id="0cfc0-137">(f, f, f, 1); f = min (AS, 1-AD)</span><span class="sxs-lookup"><span data-stu-id="0cfc0-137">(f, f, f, 1); f = min(As, 1-Ad)</span></span>                                                                                                                                                          |
| <span data-ttu-id="0cfc0-138">D3DBLEND \_ bothsrcalpha</span><span class="sxs-lookup"><span data-stu-id="0cfc0-138">D3DBLEND\_BOTHSRCALPHA</span></span>    | <span data-ttu-id="0cfc0-139">Veraltet für DirectX 6 und höher.</span><span class="sxs-lookup"><span data-stu-id="0cfc0-139">Obsolete for DirectX 6 and later.</span></span> <span data-ttu-id="0cfc0-140">Sie können denselben Effekt erzielen, indem Sie die Quell-und Ziel-Blend-Faktoren auf D3DBLEND \_ srcalpha und D3DBLEND \_ invsrcalpha in separaten Aufrufen festlegen.</span><span class="sxs-lookup"><span data-stu-id="0cfc0-140">You can achieve the same effect by setting the source and destination blend factors to D3DBLEND\_SRCALPHA and D3DBLEND\_INVSRCALPHA in separate calls.</span></span> |
| <span data-ttu-id="0cfc0-141">D3DBLEND \_ bothinvsrcalpha</span><span class="sxs-lookup"><span data-stu-id="0cfc0-141">D3DBLEND\_BOTHINVSRCALPHA</span></span> | <span data-ttu-id="0cfc0-142">Veraltet für DirectX 6.</span><span class="sxs-lookup"><span data-stu-id="0cfc0-142">Obsolete for DirectX 6.</span></span> <span data-ttu-id="0cfc0-143">Sie können denselben Effekt erzielen, indem Sie die Quell-und Ziel-Blend-Faktoren \_ in separaten Aufrufen auf D3DBLEND invsrcalpha und D3DBLEND \_ srcalpha festlegen.</span><span class="sxs-lookup"><span data-stu-id="0cfc0-143">You can achieve the same effect by setting the source and destination blend factors to D3DBLEND\_INVSRCALPHA and D3DBLEND\_SRCALPHA in separate calls.</span></span>           |
| <span data-ttu-id="0cfc0-144">D3DBLEND \_ blendfactor</span><span class="sxs-lookup"><span data-stu-id="0cfc0-144">D3DBLEND\_BLENDFACTOR</span></span>     | <span data-ttu-id="0cfc0-145">Verwenden Sie "Color. r", "Color. g", "Color. b" und "Color. a" aus der D3DRS \_ blendfactor-Einstellung.</span><span class="sxs-lookup"><span data-stu-id="0cfc0-145">Use color.r, color.g, color.b, and color.a obtained from the D3DRS\_BLENDFACTOR setting.</span></span>                                                                                                 |
| <span data-ttu-id="0cfc0-146">D3DBLEND- \_ invblendfactor</span><span class="sxs-lookup"><span data-stu-id="0cfc0-146">D3DBLEND\_INVBLENDFACTOR</span></span>  | <span data-ttu-id="0cfc0-147">Verwenden Sie 1-Color. r, 1-Color. g, 1-Color. b und 1-Color. a aus der D3DRS \_ blendfactor-Einstellung.</span><span class="sxs-lookup"><span data-stu-id="0cfc0-147">Use 1-color.r, 1-color.g, 1-color.b, and 1-color.a obtained from the D3DRS\_BLENDFACTOR setting.</span></span>                                                                                         |



 

<span data-ttu-id="0cfc0-148">Direct3D verwendet den D3DRS \_ AlphaBlendEnable-Rendering-Status, um Alpha-Transparenz-Blending zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="0cfc0-148">Direct3D uses the D3DRS\_ALPHABLENDENABLE render state to enable alpha transparency blending.</span></span> <span data-ttu-id="0cfc0-149">Der Typ der durchgeführten Alpha Mischung hängt von den D3DRS \_ srcblend-und D3DRS \_ destblend-Rendering-Zuständen ab.</span><span class="sxs-lookup"><span data-stu-id="0cfc0-149">The type of alpha blending that is done depends on the D3DRS\_SRCBLEND and D3DRS\_DESTBLEND render states.</span></span> <span data-ttu-id="0cfc0-150">Quell-und Ziel-Blend-Zustände werden paarweise verwendet.</span><span class="sxs-lookup"><span data-stu-id="0cfc0-150">Source and destination blend states are used in pairs.</span></span> <span data-ttu-id="0cfc0-151">Mit dem folgenden Code Fragment wird der Source Blend-Status auf D3DBLEND \_ srccolor und den Ziel-Blend-Zustand auf D3DBLEND \_ invsrccolor festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0cfc0-151">The following code fragment sets the source blend state to D3DBLEND\_SRCCOLOR and the destination blend state to D3DBLEND\_INVSRCCOLOR.</span></span>


```
// This code fragment assumes that lpD3DDevice is a 
//   valid pointer to a device.

// Enable alpha blending.
lpD3DDevice->SetRenderState(D3DRS_ALPHABLENDENABLE, 
                            TRUE);

// Set the source blend state.
lpD3DDevice->SetRenderState(D3DRS_SRCBLEND, 
                            D3DBLEND_SRCCOLOR);

// Set the destination blend state.
lpD3DDevice->SetRenderState(D3DRS_DESTBLEND, 
                            D3DBLEND_INVSRCCOLOR);
```



<span data-ttu-id="0cfc0-152">Dieser Code führt eine lineare Mischung zwischen der Quellfarbe (die Farbe des primitiven, das an der aktuellen Position gerendert wird) und der Zielfarbe (die Farbe an der aktuellen Position im Frame Puffer) aus.</span><span class="sxs-lookup"><span data-stu-id="0cfc0-152">This code performs a linear blend between the source color (the color of the primitive being rendered at the current location) and the destination color (the color at the current location in the frame buffer).</span></span> <span data-ttu-id="0cfc0-153">Die resultierende Darstellung ähnelt einem duktglas, wenn ein Teil der Farbe des Zielobjekts über das Quell Objekt übertragen wird. der Rest der Datei wird anscheinend aufgenommen.</span><span class="sxs-lookup"><span data-stu-id="0cfc0-153">The resulting appearance is similar to tinted glass in that some of the color of the destination object seems to be transmitted through the source object; the rest of it appears to be absorbed.</span></span>

<span data-ttu-id="0cfc0-154">Viele dieser Blend-Faktoren erfordern, dass Alpha Werte in der Textur ordnungsgemäß funktionieren.</span><span class="sxs-lookup"><span data-stu-id="0cfc0-154">Many of these blend factors require alpha values in the texture to operate correctly.</span></span> <span data-ttu-id="0cfc0-155">Daher ist die Anwendung bei Verwendung von Scheitelpunkt oder Material Alpha beschränkt, auf welche Modi interessante Ergebnisse erzeugt werden.</span><span class="sxs-lookup"><span data-stu-id="0cfc0-155">Thus, when using vertex or material alpha, the application is restricted as to which modes will produce interesting results.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0cfc0-156">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0cfc0-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0cfc0-157">Alpha Blending</span><span class="sxs-lookup"><span data-stu-id="0cfc0-157">Alpha Blending</span></span>](alpha-blending.md)
</dt> </dl>

 

 



