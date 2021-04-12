---
description: Anwendungen verwenden den Schablonen Puffer, um Pixel in einem Bild zu maskieren. Die Maske steuert, ob das Pixel gezeichnet wird. Einige der gängigeren Effekte sind unten dargestellt.
ms.assetid: 984f0a98-4a74-44c3-a9d0-f5d3f12f7e4e
title: Techniken für Schablonen Puffer (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c2dcc05475a3ddfc13e456faf60ec2d11e271a9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392882"
---
# <a name="stencil-buffer-techniques-direct3d-9"></a><span data-ttu-id="08f30-105">Techniken für Schablonen Puffer (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="08f30-105">Stencil Buffer Techniques (Direct3D 9)</span></span>

<span data-ttu-id="08f30-106">Anwendungen verwenden den Schablonen Puffer, um Pixel in einem Bild zu maskieren.</span><span class="sxs-lookup"><span data-stu-id="08f30-106">Applications use the stencil buffer to mask pixels in an image.</span></span> <span data-ttu-id="08f30-107">Die Maske steuert, ob das Pixel gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="08f30-107">The mask controls whether the pixel is drawn or not.</span></span> <span data-ttu-id="08f30-108">Einige der gängigeren Effekte sind unten dargestellt.</span><span class="sxs-lookup"><span data-stu-id="08f30-108">Some of the more common effects are shown below.</span></span>

-   [<span data-ttu-id="08f30-109">Zusammensetzung</span><span class="sxs-lookup"><span data-stu-id="08f30-109">Compositing</span></span>](compositing.md)
-   [<span data-ttu-id="08f30-110">Wird abgebrochen</span><span class="sxs-lookup"><span data-stu-id="08f30-110">Decaling</span></span>](decaling.md)
-   [<span data-ttu-id="08f30-111">Wird aufgelöst, ausgeblendet und durchstreifen</span><span class="sxs-lookup"><span data-stu-id="08f30-111">Dissolves, Fades, and Swipes</span></span>](dissolves--fades--and-swipes.md)
-   [<span data-ttu-id="08f30-112">Kontur und Silhouetten</span><span class="sxs-lookup"><span data-stu-id="08f30-112">Outlines and Silhouettes</span></span>](outlines-and-silhouettes.md)
-   [<span data-ttu-id="08f30-113">Zweiseitige Schablone</span><span class="sxs-lookup"><span data-stu-id="08f30-113">Two-Sided Stencil</span></span>](two-sided-stencil.md)

<span data-ttu-id="08f30-114">Der Schablonen Puffer aktiviert oder deaktiviert das Zeichnen auf der Renderingzieloberfläche auf Pixel Basis.</span><span class="sxs-lookup"><span data-stu-id="08f30-114">The stencil buffer enables or disables drawing to the rendering target surface on a pixel-by-pixel basis.</span></span> <span data-ttu-id="08f30-115">Auf der grundlegendsten Ebene ermöglicht es Anwendungen, Abschnitte des gerenderten Bilds so zu maskieren, dass Sie nicht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="08f30-115">At its most fundamental level, it enables applications to mask sections of the rendered image so that they are not displayed.</span></span> <span data-ttu-id="08f30-116">Anwendungen verwenden häufig Schablonen Puffer für besondere Effekte, wie z. b. auflösen, herabsetzen und gliedern.</span><span class="sxs-lookup"><span data-stu-id="08f30-116">Applications often use stencil buffers for special effects such as dissolves, decaling, and outlining.</span></span>

<span data-ttu-id="08f30-117">Schablonen Puffer Informationen werden in die z-Puffer Daten eingebettet.</span><span class="sxs-lookup"><span data-stu-id="08f30-117">Stencil buffer information is embedded in the z-buffer data.</span></span> <span data-ttu-id="08f30-118">Die Anwendung kann die [**IDirect3D9:: CheckDeviceFormat**](/windows/desktop/api) -Methode verwenden, um die Unterstützung von Hardware Schablonen zu prüfen, wie im folgenden Codebeispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="08f30-118">Your application can use the [**IDirect3D9::CheckDeviceFormat**](/windows/desktop/api) method to check for hardware stencil support, as shown in the following code example.</span></span>


```
// Reject devices that cannot perform 8-bit stencil buffering. 
// The following example assumes that pCaps is a valid pointer 
// to an initialized D3DCAPS9 structure. 

if( FAILED( m_pD3D->CheckDeviceFormat( pCaps->AdapterOrdinal,
                                       pCaps->DeviceType,  
                                       Format,  
                                       D3DUSAGE_DEPTHSTENCIL, 
                                       D3DRTYPE_SURFACE,
                                       D3DFMT_D24S8 ) ) )
return E_FAIL;
```



<span data-ttu-id="08f30-119">[**IDirect3D9:: CheckDeviceFormat**](/windows/desktop/api) ermöglicht Ihnen die Auswahl eines zu erstellenden Geräts basierend auf den Funktionen dieses Geräts.</span><span class="sxs-lookup"><span data-stu-id="08f30-119">[**IDirect3D9::CheckDeviceFormat**](/windows/desktop/api) allows you to choose a device to create based on the capabilities of that device.</span></span> <span data-ttu-id="08f30-120">In diesem Fall werden Geräte, die 8-Bit-Schablonen Puffer nicht unterstützen, abgelehnt.</span><span class="sxs-lookup"><span data-stu-id="08f30-120">In this case, devices that do not support 8-bit stencil buffers are rejected.</span></span> <span data-ttu-id="08f30-121">Beachten Sie, dass dies nur eine mögliche Verwendung für **IDirect3D9:: CheckDeviceFormat**; ist. Weitere Informationen finden Sie [unter Bestimmen des Hardware Supports (Direct3D 9)](determining-hardware-support.md).</span><span class="sxs-lookup"><span data-stu-id="08f30-121">Note that this is only one possible use for **IDirect3D9::CheckDeviceFormat**; for details see [Determining Hardware Support (Direct3D 9)](determining-hardware-support.md).</span></span>

## <a name="how-the-stencil-buffer-works"></a><span data-ttu-id="08f30-122">Funktionsweise des Schablonen Puffers</span><span class="sxs-lookup"><span data-stu-id="08f30-122">How the Stencil Buffer Works</span></span>

<span data-ttu-id="08f30-123">Direct3D führt einen Test für den Inhalt des Schablonen Puffers auf Pixel Basis aus.</span><span class="sxs-lookup"><span data-stu-id="08f30-123">Direct3D performs a test on the contents of the stencil buffer on a pixel-by-pixel basis.</span></span> <span data-ttu-id="08f30-124">Für jedes Pixel in der Ziel Oberfläche wird ein Test mit dem entsprechenden Wert im Schablonen Puffer, einem Schablonen Verweis Wert und einem Schablone-Maskenwert durchführt.</span><span class="sxs-lookup"><span data-stu-id="08f30-124">For each pixel in the target surface, it performs a test using the corresponding value in the stencil buffer, a stencil reference value, and a stencil mask value.</span></span> <span data-ttu-id="08f30-125">Wenn der Test ausgeführt wird, führt Direct3D eine Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="08f30-125">If the test passes, Direct3D performs an action.</span></span> <span data-ttu-id="08f30-126">Der Test wird mithilfe der folgenden Schritte ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="08f30-126">The test is performed using the following steps.</span></span>

1.  <span data-ttu-id="08f30-127">Führt eine bitweise AND-Operation des Schablonen Verweis Werts mit der Schablonen Maske aus.</span><span class="sxs-lookup"><span data-stu-id="08f30-127">Perform a bitwise AND operation of the stencil reference value with the stencil mask.</span></span>
2.  <span data-ttu-id="08f30-128">Führt eine bitweise AND-Operation des Schablonen Puffer Werts für das aktuelle Pixel mit der Schablonen Maske aus.</span><span class="sxs-lookup"><span data-stu-id="08f30-128">Perform a bitwise AND operation of the stencil buffer value for the current pixel with the stencil mask.</span></span>
3.  <span data-ttu-id="08f30-129">Vergleichen Sie das Ergebnis von Schritt 1 mit dem Ergebnis von Schritt 2 mit der Vergleichsfunktion.</span><span class="sxs-lookup"><span data-stu-id="08f30-129">Compare the result of step 1 to the result of step 2, using the comparison function.</span></span>

<span data-ttu-id="08f30-130">Diese Schritte sind im folgenden Codebeispiel dargestellt.</span><span class="sxs-lookup"><span data-stu-id="08f30-130">These steps are shown in the following code example.</span></span>


```
(StencilRef & StencilMask) CompFunc (StencilBufferValue & StencilMask)
```




```
StencilBufferValue
```



<span data-ttu-id="08f30-131">der Inhalt des Schablonen Puffers für das aktuelle Pixel.</span><span class="sxs-lookup"><span data-stu-id="08f30-131">is the contents of the stencil buffer for the current pixel.</span></span> <span data-ttu-id="08f30-132">In diesem Codebeispiel wird das kaufmännische und-Zeichen (&) verwendet, um die bitweise AND-Operation darzustellen.</span><span class="sxs-lookup"><span data-stu-id="08f30-132">This code example uses the ampersand (&) symbol to represent the bitwise AND operation.</span></span>


```
StencilMask
```



<span data-ttu-id="08f30-133">stellt den Wert der Schablonen Maske dar.</span><span class="sxs-lookup"><span data-stu-id="08f30-133">represents the value of the stencil mask, and</span></span>


```
StencilRef
```



<span data-ttu-id="08f30-134">stellt den Schablonen Verweis Wert dar.</span><span class="sxs-lookup"><span data-stu-id="08f30-134">represents the stencil reference value.</span></span>


```
CompFunc
```



<span data-ttu-id="08f30-135">ist die Vergleichsfunktion.</span><span class="sxs-lookup"><span data-stu-id="08f30-135">is the comparison function.</span></span>

<span data-ttu-id="08f30-136">Das aktuelle Pixel wird auf die Ziel Oberfläche geschrieben, wenn der Schablonen Test verstrichen ist, und wird andernfalls ignoriert.</span><span class="sxs-lookup"><span data-stu-id="08f30-136">The current pixel is written to the target surface if the stencil test passes, and is ignored otherwise.</span></span> <span data-ttu-id="08f30-137">Das Standard Vergleichs Verhalten besteht darin, das Pixel zu schreiben, unabhängig davon, wie sich jeder bitweise Vorgang ausstellt (D3DCMP \_ Always).</span><span class="sxs-lookup"><span data-stu-id="08f30-137">The default comparison behavior is to write the pixel, no matter how each bitwise operation turns out (D3DCMP\_ALWAYS).</span></span> <span data-ttu-id="08f30-138">Sie können dieses Verhalten ändern, indem Sie den Wert des D3DRS \_ stencilfunc-renderzustands ändern und einen Member des [**D3DCMPFUNC**](./d3dcmpfunc.md) -enumerierten Typs übergeben, um die gewünschte Vergleichsfunktion zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="08f30-138">You can change this behavior by changing the value of the D3DRS\_STENCILFUNC render state, passing a member of the [**D3DCMPFUNC**](./d3dcmpfunc.md) enumerated type to identify the desired comparison function.</span></span>

<span data-ttu-id="08f30-139">Die Anwendung kann den Vorgang des Schablonen Puffers anpassen.</span><span class="sxs-lookup"><span data-stu-id="08f30-139">Your application can customize the operation of the stencil buffer.</span></span> <span data-ttu-id="08f30-140">Sie kann die Vergleichsfunktion, die Schablonen Maske und den Schablonen Verweis Wert festlegen.</span><span class="sxs-lookup"><span data-stu-id="08f30-140">It can set the comparison function, the stencil mask, and the stencil reference value.</span></span> <span data-ttu-id="08f30-141">Außerdem kann Sie die Aktion steuern, die Direct3D durchführt, wenn der Schablonen Test erfolgreich verläuft oder fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="08f30-141">It can also control the action that Direct3D takes when the stencil test passes or fails.</span></span> <span data-ttu-id="08f30-142">Weitere Informationen finden Sie unter [Status des Schablone-Puffers (Direct3D 9)](stencil-buffer-state.md).</span><span class="sxs-lookup"><span data-stu-id="08f30-142">For more information, see [Stencil Buffer State (Direct3D 9)](stencil-buffer-state.md).</span></span>

## <a name="examples"></a><span data-ttu-id="08f30-143">Beispiele</span><span class="sxs-lookup"><span data-stu-id="08f30-143">Examples</span></span>

<span data-ttu-id="08f30-144">Die folgenden Codebeispiele veranschaulichen das Einrichten des Schablonen Puffers.</span><span class="sxs-lookup"><span data-stu-id="08f30-144">The following code examples demonstrate setting up the stencil buffer.</span></span>


```
// Enable stencil testing
pDevice->SetRenderState(D3DRS_STENCILENABLE, TRUE);

// Specify the stencil comparison function
pDevice->SetRenderState(D3DRS_STENCILFUNC, D3DCMP_EQUAL);

// Set the comparison reference value
pDevice->SetRenderState(D3DRS_STENCILREF, 0);

//  Specify a stencil mask 
pDevice->SetRenderState(D3DRS_STENCILMASK, 0);
```



<span data-ttu-id="08f30-145">Der Schablonen Verweis Wert ist standardmäßig 0 (null).</span><span class="sxs-lookup"><span data-stu-id="08f30-145">By default, the stencil reference value is zero.</span></span> <span data-ttu-id="08f30-146">Jeder ganzzahlige Wert ist gültig.</span><span class="sxs-lookup"><span data-stu-id="08f30-146">Any integer value is valid.</span></span> <span data-ttu-id="08f30-147">Direct3D führt ein bitweises and des Schablonen Verweis Werts und einen Schablonen Maskenwert vor dem Schablonen Test aus.</span><span class="sxs-lookup"><span data-stu-id="08f30-147">Direct3D performs a bitwise AND of the stencil reference value and a stencil mask value before the stencil test.</span></span>

<span data-ttu-id="08f30-148">Abhängig vom Schablone-Vergleich können Sie steuern, welche Pixel Informationen geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="08f30-148">You can control what pixel information is written out depending on the stencil comparison.</span></span>


```
// A write mask controls what is written
pDevice->SetRenderState(D3DRS_STENCILWRITEMASK, D3DSTENCILOP_KEEP);
// Specify when to write stencil data
pDevice->SetRenderState(D3DRS_STENCILFAIL, D3DSTENCILOP_KEEP);
```



<span data-ttu-id="08f30-149">Sie können eine eigene Formel für den Wert schreiben, den Sie in den Schablonen Puffer schreiben möchten, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="08f30-149">You can write your own formula for the value you want written into the stencil buffer as shown in the following example.</span></span>


```
NewStencilBufferValue = (StencilBufferValue & ~StencilWriteMask) | 
                        (StencilWriteMask & StencilOp(StencilBufferValue))
```



## <a name="related-topics"></a><span data-ttu-id="08f30-150">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="08f30-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08f30-151">Pixel Pipeline</span><span class="sxs-lookup"><span data-stu-id="08f30-151">Pixel Pipeline</span></span>](pixel-pipeline.md)
</dt> </dl>

 

 
