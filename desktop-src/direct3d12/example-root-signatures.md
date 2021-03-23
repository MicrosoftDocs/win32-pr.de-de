---
title: Beispiel Stamm Signaturen
description: Der folgende Abschnitt zeigt die Stamm Signaturen, die bei der Komplexität variieren, von leer bis vollständig.
ms.assetid: 493D35C9-2A90-4688-BD7E-74B9EB2B4E72
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19d09d355cc1c96d77670c5536400f0b3f93c097
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104314"
---
# <a name="example-root-signatures"></a><span data-ttu-id="3985d-103">Beispiel Stamm Signaturen</span><span class="sxs-lookup"><span data-stu-id="3985d-103">Example Root Signatures</span></span>

<span data-ttu-id="3985d-104">Der folgende Abschnitt zeigt die Stamm Signaturen, die bei der Komplexität variieren, von leer bis vollständig.</span><span class="sxs-lookup"><span data-stu-id="3985d-104">The following section shows root signatures varying in complexity from empty to completely full.</span></span>

-   [<span data-ttu-id="3985d-105">Eine leere Stamm Signatur</span><span class="sxs-lookup"><span data-stu-id="3985d-105">An empty root signature</span></span>](#an-empty-root-signature)
-   [<span data-ttu-id="3985d-106">Eine Konstante</span><span class="sxs-lookup"><span data-stu-id="3985d-106">One constant</span></span>](#one-constant)
-   [<span data-ttu-id="3985d-107">Hinzufügen einer Stamm Konstanten-Puffer Ansicht</span><span class="sxs-lookup"><span data-stu-id="3985d-107">Adding a root Constant Buffer View</span></span>](#adding-a-root-constant-buffer-view)
-   [<span data-ttu-id="3985d-108">Bindungs deskriptortabellen</span><span class="sxs-lookup"><span data-stu-id="3985d-108">Binding descriptor tables</span></span>](#binding-descriptor-tables)
-   [<span data-ttu-id="3985d-109">Eine komplexere Stamm Signatur</span><span class="sxs-lookup"><span data-stu-id="3985d-109">A more complex root signature</span></span>](#a-more-complex-root-signature)
-   [<span data-ttu-id="3985d-110">Streaming-Shader-Ressourcen Sichten</span><span class="sxs-lookup"><span data-stu-id="3985d-110">Streaming Shader Resource Views</span></span>](#streaming-shader-resource-views)
-   [<span data-ttu-id="3985d-111">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="3985d-111">Related topics</span></span>](#related-topics)

## <a name="an-empty-root-signature"></a><span data-ttu-id="3985d-112">Eine leere Stamm Signatur</span><span class="sxs-lookup"><span data-stu-id="3985d-112">An empty root signature</span></span>

![eine leere Stamm Signatur hat keine Bindungen.](images/root-tables-0.png)

<span data-ttu-id="3985d-114">Eine leere Stamm Signatur ist wahrscheinlich nicht nützlich, kann aber in einem trivialen Renderingdurchlauf verwendet werden, der nur den Eingabe Assembler verwendet, und minimale Scheitelpunkt-und Pixel-Shader, die nicht auf Deskriptoren zugreifen.</span><span class="sxs-lookup"><span data-stu-id="3985d-114">An empty root signature is unlikely to be useful, but could be used in a trivial rendering pass with use of only the input assembler, and minimal vertex and pixel shaders that do not access any descriptors.</span></span> <span data-ttu-id="3985d-115">Außerdem sind die Phasen Blend, Renderziel und tiefen Schablone verfügbar, auch mit einer leeren Stamm Signatur.</span><span class="sxs-lookup"><span data-stu-id="3985d-115">Also the blend stage, render target and depth-stencil stages are available, even with an empty root signature.</span></span>

## <a name="one-constant"></a><span data-ttu-id="3985d-116">Eine Konstante</span><span class="sxs-lookup"><span data-stu-id="3985d-116">One constant</span></span>

![eine einzelne Stamm Konstante](images/root-tables-constant.png)

<span data-ttu-id="3985d-118">Der API-Bindungs Slot ist der Ort, an dem das Root-Argument für diesen Parameter an der Befehlslisten-Daten Satz Zeit gebunden wird.</span><span class="sxs-lookup"><span data-stu-id="3985d-118">The API bind slot is where the root argument for this parameter will be bound at command list record time.</span></span> <span data-ttu-id="3985d-119">Die Anzahl der API-Bindungs Slots ist implizit, basierend auf der Reihenfolge der Parameter in der Stamm Signatur (die erste ist immer null).</span><span class="sxs-lookup"><span data-stu-id="3985d-119">The number of the API bind slots is implicit, based on the order of the parameters in the root signature (the first is always zero).</span></span> <span data-ttu-id="3985d-120">Der HLSL-Bindungs Slot ist der Ort, an dem der Shader anzeigt, dass der Root-Parameter angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="3985d-120">The HLSL bind slot is where the shader will see the root parameter show up.</span></span> <span data-ttu-id="3985d-121">Der Typ ("uint" im obigen Beispiel) ist der Hardware nicht bekannt, aber es handelt sich nur um einen Kommentar im Image. die Hardware sieht einfach nur das einzige DWORD als Inhalt.</span><span class="sxs-lookup"><span data-stu-id="3985d-121">The type ("uint" in the above example) is not known to the hardware but is just a comment in the image, the hardware will simply see the single DWORD as the contents.</span></span>

<span data-ttu-id="3985d-122">Um eine Konstante an der Befehlslisten-Daten Satz Zeit zu binden, wird ein Befehl ähnlich dem folgenden verwendet:</span><span class="sxs-lookup"><span data-stu-id="3985d-122">To bind a constant at command-list record time, a command similar to the following would be used:</span></span>

``` syntax
pCmdList->SetComputeRoot32BitConstant(0,seed); // 0 is the parameter index, seed is used by the shaders
```

## <a name="adding-a-root-constant-buffer-view"></a><span data-ttu-id="3985d-123">Hinzufügen einer Stamm Konstanten-Puffer Ansicht</span><span class="sxs-lookup"><span data-stu-id="3985d-123">Adding a root Constant Buffer View</span></span>

![Fügt der Stamm Signatur eine Konstante Puffer Ansicht hinzu.](images/root-tables-cbv.png)

<span data-ttu-id="3985d-125">In diesem Beispiel werden zwei Stamm Konstanten und eine Stamm Konstante-Puffer Ansicht (CBV) gezeigt, die zwei DWORD-Slots kostet.</span><span class="sxs-lookup"><span data-stu-id="3985d-125">This example shows two root constants, and a root Constant Buffer View (CBV) that costs two DWORD slots.</span></span>

<span data-ttu-id="3985d-126">Verwenden Sie zum Binden einer Konstanten Puffer Ansicht einen Befehl wie den folgenden.</span><span class="sxs-lookup"><span data-stu-id="3985d-126">To bind a constant buffer view use a command such as the following.</span></span> <span data-ttu-id="3985d-127">Beachten Sie, dass der erste Parameter (2) der Slot ist, der im Bild angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="3985d-127">Note the first parameter (2) is the slot shown in the image.</span></span> <span data-ttu-id="3985d-128">In der Regel wird ein Array von Konstanten eingerichtet und dann den Shadern bei B0 als CBV zur Verfügung gestellt.</span><span class="sxs-lookup"><span data-stu-id="3985d-128">Typically an array of constants will be set up and then made available to the shaders at b0 as a CBV.</span></span>

``` syntax
pCmdList->SetGraphicsRootConstantBufferView(2,GPUVAForCurrDynamicConstants);
```

## <a name="binding-descriptor-tables"></a><span data-ttu-id="3985d-129">Bindungs deskriptortabellen</span><span class="sxs-lookup"><span data-stu-id="3985d-129">Binding descriptor tables</span></span>

![Fügt der Stamm Signatur deskriptortabellen hinzu.](images/root-tables-2.png)

<span data-ttu-id="3985d-131">Dieses Beispiel zeigt die Verwendung von zwei deskriptortabellen. eine Tabelle mit fünf Deskriptoren, die zur Ausführungszeit in einem CBV \_ -SRV \_ -UAV-deskriptorheap verfügbar ist, und eine andere Tabelle mit zwei Deskriptoren, die zur Ausführungszeit in einem Sampler-deskriptorheap angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="3985d-131">This example shows the use of two descriptor tables; one declaring a table of five descriptors that will be available at execution time in a CBV\_SRV\_UAV descriptor heap, and another declaring a table of two descriptors that will show up at execution time in a sampler descriptor heap.</span></span>

<span data-ttu-id="3985d-132">Zum Binden von deskriptortabellen beim Aufzeichnen einer Befehlsliste.</span><span class="sxs-lookup"><span data-stu-id="3985d-132">To bind descriptor tables when recording a command list.</span></span>

``` syntax
pCmdList->SetComputeRootDescriptorTable(1, handleToCurrentMaterialDataInHeap);
pCmdList->SetComputeRootDescriptorTable(2, handleToCurrentMaterialDataInSamplerHeap);
```

<span data-ttu-id="3985d-133">Ein weiteres Feature der Stamm Signatur ist die Stamm Konstante float4, die vier DWords groß ist.</span><span class="sxs-lookup"><span data-stu-id="3985d-133">Another feature of the root signature is the float4 root constant that is four DWORDS in size.</span></span> <span data-ttu-id="3985d-134">Mit dem folgenden Befehl werden nur die beiden mittleren DWords der vier Daten gebunden.</span><span class="sxs-lookup"><span data-stu-id="3985d-134">The following command binds just the middle two DWORDS of the four.</span></span>

``` syntax
pCmdList->SetComputeRoot32BitConstants(0,2,myFloat2Array,1);  // 2 constants starting at offset 1 (middle 2 values in float4)
```

## <a name="a-more-complex-root-signature"></a><span data-ttu-id="3985d-135">Eine komplexere Stamm Signatur</span><span class="sxs-lookup"><span data-stu-id="3985d-135">A more complex root signature</span></span>

![eine komplexe Stamm Signatur mit vielen Elementen](images/root-tables-3.png)

<span data-ttu-id="3985d-137">Dieses Beispiel zeigt eine Dichte Stamm Signatur mit den meisten Typen von Einträgen.</span><span class="sxs-lookup"><span data-stu-id="3985d-137">This example shows a dense root signature with most types of entries.</span></span> <span data-ttu-id="3985d-138">Zwei der deskriptortabellen (in den Slots 3 und 6) enthalten Arrays für die unbegrenzte Größe.</span><span class="sxs-lookup"><span data-stu-id="3985d-138">Two of the descriptor tables (at slots 3 and 6) include unbounded size arrays.</span></span> <span data-ttu-id="3985d-139">Der Aufwand für die Anwendung besteht darin, nur gültige Deskriptoren in einem Heap zu berühren.</span><span class="sxs-lookup"><span data-stu-id="3985d-139">The burden here is on the application to only touch valid descriptors in a heap.</span></span> <span data-ttu-id="3985d-140">Unbegrenzte oder sehr große Arrays erfordern Hardwareebene 2 + Ressourcen Bindungs Unterstützung.</span><span class="sxs-lookup"><span data-stu-id="3985d-140">Unbounded, or very large arrays, require hardware tier 2+ of resource binding support.</span></span>

<span data-ttu-id="3985d-141">Es gibt zwei statische Samplern (gebunden ohne Stamm Signatur Slots).</span><span class="sxs-lookup"><span data-stu-id="3985d-141">There are two static samplers (bound without requiring root signature slots).</span></span>

<span data-ttu-id="3985d-142">An Slot 9 werden UAV U4 und UAV-U5 mit dem gleichen deskriptortabellenoffset deklariert.</span><span class="sxs-lookup"><span data-stu-id="3985d-142">At slot 9, UAV u4 and UAV u5 are declared at the same descriptor table offset.</span></span> <span data-ttu-id="3985d-143">Dies wird für einen Alias Deskriptor verwendet, und ein Deskriptor im Arbeitsspeicher wird in den HLSL-Shadern sowohl als als auch als "..." angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3985d-143">This is use of an aliased descriptor, one descriptor in memory will show up as both u4 and u5 in the HLSL shaders.</span></span> <span data-ttu-id="3985d-144">In diesem Fall muss der Shader mit der Option "d3d10 \_ Shader \_ Resources \_ \_ Alias" oder der `/res_may_alias` Option oder in FXC kompiliert werden.</span><span class="sxs-lookup"><span data-stu-id="3985d-144">In this case the shader must be compiled with the D3D10\_SHADER\_RESOURCES\_MAY\_ALIAS option, or the or `/res_may_alias` option in FXC.</span></span> <span data-ttu-id="3985d-145">Mit Alias Deskriptoren kann ein Deskriptor an mehrere Bindungs Punkte gebunden werden, ohne dass Änderungen an den Shadern vorgenommen werden müssen.</span><span class="sxs-lookup"><span data-stu-id="3985d-145">Aliased descriptors enable one descriptor to be bound to multiple bind points, without having to make any changes to the shaders.</span></span>

## <a name="streaming-shader-resource-views"></a><span data-ttu-id="3985d-146">Streaming-Shader-Ressourcen Sichten</span><span class="sxs-lookup"><span data-stu-id="3985d-146">Streaming Shader Resource Views</span></span>

![Streaming-Shader-Ressourcen Sichten in dieser Stamm Signatur](images/root-tables-4.png)

<span data-ttu-id="3985d-148">Diese Stamm Signatur veranschaulicht ein Szenario, in dem alle Srvs in ein und aus einem großen Array gestreamt werden.</span><span class="sxs-lookup"><span data-stu-id="3985d-148">This root signature illustrates a scenario where all SRVs are streamed in and out of one large array.</span></span> <span data-ttu-id="3985d-149">Zur Ausführungszeit kann eine Deskriptortabelle einmal festgelegt werden, wenn die Stamm Signatur festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="3985d-149">At execution time, a descriptor table can be set once when the root signature is set.</span></span> <span data-ttu-id="3985d-150">Anschließend werden alle Textur Lesevorgänge durch die Indizierung in das Array durch Konstanten durch die ersten Stamm Argumente durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="3985d-150">Then all texture reads are done by indexing into the array via constants fed via the first few root arguments.</span></span> <span data-ttu-id="3985d-151">Es ist nur ein einzelner deskriptorheap erforderlich, und er wird nur aktualisiert, wenn Texturen in oder aus freien deskriptorslots gestreamt werden.</span><span class="sxs-lookup"><span data-stu-id="3985d-151">Only a single descriptor heap is needed, and is only updated as textures are streamed in or out of free descriptor slots.</span></span>

<span data-ttu-id="3985d-152">Die deskriptoroffsets im großen Heap werden durch Shader identifiziert, die die Konstanten in den konstanten Puffer Sichten verwenden.</span><span class="sxs-lookup"><span data-stu-id="3985d-152">The descriptor offsets in the large heap are identified by shaders using the constants in the Constant Buffer Views.</span></span> <span data-ttu-id="3985d-153">Wenn ein Shader z. b. eine Material-ID erhält, kann er mit der-Konstante in das ein großes Array indizieren, um auf den erforderlichen Deskriptor (der auf die erforderliche Textur verweist) zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="3985d-153">For example, if a shader is given a material ID, it can index into the one large array using the constant to access the required descriptor (which references the required texture).</span></span>

<span data-ttu-id="3985d-154">Für dieses Szenario ist Hardware mit Ressourcen Bindung Instanzen + erforderlich.</span><span class="sxs-lookup"><span data-stu-id="3985d-154">This scenario requires hardware with resource binding tier2+.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3985d-155">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="3985d-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3985d-156">Hardware Ebenen für die Ressourcen Bindung</span><span class="sxs-lookup"><span data-stu-id="3985d-156">Resource Binding Hardware Tiers</span></span>](hardware-support.md)
</dt> <dt>

[<span data-ttu-id="3985d-157">Ressourcen Bindung in HLSL</span><span class="sxs-lookup"><span data-stu-id="3985d-157">Resource Binding in HLSL</span></span>](resource-binding-in-hlsl.md)
</dt> <dt>

[<span data-ttu-id="3985d-158">Stamm Signaturen</span><span class="sxs-lookup"><span data-stu-id="3985d-158">Root Signatures</span></span>](root-signatures.md)
</dt> </dl>

 

 




