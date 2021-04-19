---
description: In Direct3D 10 wird der Gerätestatus in Zustands Objekte gruppiert, wodurch die Kosten für Zustandsänderungen erheblich reduziert werden.
ms.assetid: b2839da9-60ed-4f6c-9cc7-eac53647cca7
title: Zustands Objekte (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a06e8603361a83049440774cfd2e12b4148b183
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342751"
---
# <a name="state-objects-direct3d-10"></a><span data-ttu-id="7be9a-103">Zustands Objekte (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="7be9a-103">State Objects (Direct3D 10)</span></span>

<span data-ttu-id="7be9a-104">In Direct3D 10 wird der Gerätestatus in Zustands Objekte gruppiert, wodurch die Kosten für Zustandsänderungen erheblich reduziert werden.</span><span class="sxs-lookup"><span data-stu-id="7be9a-104">In Direct3D 10, device state is grouped into state objects which greatly reduce the cost of state changes.</span></span> <span data-ttu-id="7be9a-105">Es gibt mehrere State-Objekte, die jeweils zum Initialisieren eines Zustands Satzes für eine bestimmte Pipeline Phase entwickelt wurden.</span><span class="sxs-lookup"><span data-stu-id="7be9a-105">There are several state objects, and each one is designed to initialize a set of state for a particular pipeline stage.</span></span> <span data-ttu-id="7be9a-106">Sie können bis zu 4096 für jeden Typ von Zustands Objekt erstellen.</span><span class="sxs-lookup"><span data-stu-id="7be9a-106">You can create up to 4096 of each type of state object.</span></span>

-   [<span data-ttu-id="7be9a-107">Eingabe-Layoutstatus</span><span class="sxs-lookup"><span data-stu-id="7be9a-107">Input-Layout State</span></span>](#input-layout-state)
-   [<span data-ttu-id="7be9a-108">Status des Rasterizers</span><span class="sxs-lookup"><span data-stu-id="7be9a-108">Rasterizer State</span></span>](#rasterizer-state)
-   [<span data-ttu-id="7be9a-109">Status der tiefen Schablone</span><span class="sxs-lookup"><span data-stu-id="7be9a-109">Depth-Stencil State</span></span>](#depth-stencil-state)
-   [<span data-ttu-id="7be9a-110">Blend-Status</span><span class="sxs-lookup"><span data-stu-id="7be9a-110">Blend State</span></span>](#blend-state)
-   [<span data-ttu-id="7be9a-111">Samplerstatus</span><span class="sxs-lookup"><span data-stu-id="7be9a-111">Sampler State</span></span>](#sampler-state)
-   [<span data-ttu-id="7be9a-112">Leistungsaspekte</span><span class="sxs-lookup"><span data-stu-id="7be9a-112">Performance Considerations</span></span>](#performance-considerations)
-   [<span data-ttu-id="7be9a-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7be9a-113">Related topics</span></span>](#related-topics)

## <a name="input-layout-state"></a><span data-ttu-id="7be9a-114">Input-Layout Status</span><span class="sxs-lookup"><span data-stu-id="7be9a-114">Input-Layout State</span></span>

<span data-ttu-id="7be9a-115">Diese Gruppe von Status (siehe [**d3d10 \_ input \_ Element \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc)Debug) bestimmt, wie die [Eingabe-Assembler-Phase](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage.md) Daten aus den Eingabe Puffern ausliest und für die Verwendung durch den Vertexshader assembliert.</span><span class="sxs-lookup"><span data-stu-id="7be9a-115">This group of state (see [**D3D10\_INPUT\_ELEMENT\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc)) dictates how the [input-assembler stage](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage.md) reads data out of the input buffers and assembles it for use by the vertex shader.</span></span> <span data-ttu-id="7be9a-116">Dies schließt den Zustand ein, z. b. die Anzahl der Elemente im Eingabepuffer und die Signatur der Eingabedaten.</span><span class="sxs-lookup"><span data-stu-id="7be9a-116">This includes state such as the number of elements in the input buffer and the signature of the input data.</span></span> <span data-ttu-id="7be9a-117">Bei der Eingabe-Assembler-Phase handelt es sich um eine neue Phase in der Pipeline, deren Aufgabe das Streamen primitiver Daten aus dem Arbeitsspeicher in die Pipeline ist.</span><span class="sxs-lookup"><span data-stu-id="7be9a-117">The input-assembler stage is a new stage in the pipeline whose job is to stream primitives from memory into the pipeline.</span></span>

<span data-ttu-id="7be9a-118">Informationen zum Erstellen eines Input-Layout-State-Objekts finden Sie unter " [**kreateinputlayout**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createinputlayout)".</span><span class="sxs-lookup"><span data-stu-id="7be9a-118">To create a input-layout-state object, see [**CreateInputLayout**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createinputlayout).</span></span>

## <a name="rasterizer-state"></a><span data-ttu-id="7be9a-119">Status des Rasterizers</span><span class="sxs-lookup"><span data-stu-id="7be9a-119">Rasterizer State</span></span>

<span data-ttu-id="7be9a-120">Diese Gruppe von Status (siehe [**d3d10 \_ Raster \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc)Debug) initialisiert die [Raster-Stufe](../direct3d11/d3d10-graphics-programming-guide-rasterizer-stage.md).</span><span class="sxs-lookup"><span data-stu-id="7be9a-120">This group of state (see [**D3D10\_RASTERIZER\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc)) initializes the [rasterizer stage](../direct3d11/d3d10-graphics-programming-guide-rasterizer-stage.md).</span></span> <span data-ttu-id="7be9a-121">Dieses Objekt enthält einen Zustand, wie z. b. Fill-oder auslesen-Modi, das Aktivieren eines Scheren Rechtecks für das Clipping und das Festlegen von Multisampling</span><span class="sxs-lookup"><span data-stu-id="7be9a-121">This object includes state such as fill or cull modes, enabling a scissor rectangle for clipping, and setting multisample parameters.</span></span> <span data-ttu-id="7be9a-122">In dieser Phase werden primitive in Pixel gerengt, die Vorgänge wie das Abschneiden und die Zuordnung von primitiven zum Viewport ausführen.</span><span class="sxs-lookup"><span data-stu-id="7be9a-122">This stage rasterizes primitives into pixels, performing operations like clipping and mapping primitives to the viewport.</span></span>

<span data-ttu-id="7be9a-123">Informationen zum Erstellen eines Rasterizer-State-Objekts finden Sie unter " [**kreaterasterizerstate**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createrasterizerstate)".</span><span class="sxs-lookup"><span data-stu-id="7be9a-123">To create a rasterizer-state object, see [**CreateRasterizerState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createrasterizerstate).</span></span>

## <a name="depth-stencil-state"></a><span data-ttu-id="7be9a-124">Depth-Stencil Status</span><span class="sxs-lookup"><span data-stu-id="7be9a-124">Depth-Stencil State</span></span>

<span data-ttu-id="7be9a-125">Diese Gruppe von Status (siehe [**d3d10 \_ tiefen \_ Schablone \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc)) initialisiert den tiefen Schablone-Teil der [Ausgabe-Fusion-Phase](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md).</span><span class="sxs-lookup"><span data-stu-id="7be9a-125">This group of state (see [**D3D10\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc)) initializes the depth-stencil portion of the [output-merger stage](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md).</span></span> <span data-ttu-id="7be9a-126">Genauer gesagt, initialisiert dieses Objekt Tiefe und Schablonen Tests.</span><span class="sxs-lookup"><span data-stu-id="7be9a-126">More specifically, this object initializes depth and stencil testing.</span></span>

<span data-ttu-id="7be9a-127">Informationen zum Erstellen eines tiefen Schablone-Status Objekts finden Sie unter " [**kreatedepthstencilstate**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createdepthstencilstate)".</span><span class="sxs-lookup"><span data-stu-id="7be9a-127">To create a depth-stencil-state object, see [**CreateDepthStencilState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createdepthstencilstate).</span></span>

## <a name="blend-state"></a><span data-ttu-id="7be9a-128">Blend-Status</span><span class="sxs-lookup"><span data-stu-id="7be9a-128">Blend State</span></span>

<span data-ttu-id="7be9a-129">Diese Gruppe von Status (siehe [**d3d10 \_ Blend \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc)) initialisiert den Mischungs Teil der [Ausgabe-Fusion-Phase](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md).</span><span class="sxs-lookup"><span data-stu-id="7be9a-129">This group of state (see [**D3D10\_BLEND\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc)) initializes the blending portion of the [output-merger stage](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md).</span></span>

<span data-ttu-id="7be9a-130">Informationen zum Erstellen eines Blend-State-Objekts finden Sie unter " [**kreateblendstate**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createblendstate)".</span><span class="sxs-lookup"><span data-stu-id="7be9a-130">To create a blend-state object, see [**CreateBlendState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createblendstate).</span></span>

## <a name="sampler-state"></a><span data-ttu-id="7be9a-131">Samplerstatus</span><span class="sxs-lookup"><span data-stu-id="7be9a-131">Sampler State</span></span>

<span data-ttu-id="7be9a-132">Diese Gruppe von Status (siehe [**d3d10 \_ Sampler \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_sampler_desc)Debug) Initialisiert ein samplerobjekt.</span><span class="sxs-lookup"><span data-stu-id="7be9a-132">This group of state (see [**D3D10\_SAMPLER\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_sampler_desc)) initializes a sampler object.</span></span> <span data-ttu-id="7be9a-133">Ein samplerobjekt wird von den Shader-Stufen zum Filtern von Texturen im Speicher verwendet.</span><span class="sxs-lookup"><span data-stu-id="7be9a-133">A sampler object is used by the shader stages to filter textures in memory.</span></span>



|                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7be9a-134">Unterschiede zwischen Direct3D 9 und Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="7be9a-134">Differences between Direct3D 9 and Direct3D 10:</span></span><br/> <span data-ttu-id="7be9a-135">In Direct3D 10 ist das samplerobjekt nicht mehr an eine bestimmte Textur gebunden. es wird lediglich beschrieben, wie das Filtern bei einer beliebigen angefügten Ressource durchzuführen ist.</span><span class="sxs-lookup"><span data-stu-id="7be9a-135">In Direct3D 10, the sampler object is no longer bound to a specific texture - it just describes how to do filtering given any attached resource.</span></span> |



 

<span data-ttu-id="7be9a-136">Informationen zum Erstellen eines samplerstatusobjekts finden Sie unter " [**kreatesamplerstate**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createsamplerstate)".</span><span class="sxs-lookup"><span data-stu-id="7be9a-136">To create a sampler-state object, see [**CreateSamplerState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createsamplerstate).</span></span>

## <a name="performance-considerations"></a><span data-ttu-id="7be9a-137">Überlegungen zur Leistung</span><span class="sxs-lookup"><span data-stu-id="7be9a-137">Performance Considerations</span></span>

<span data-ttu-id="7be9a-138">Das Entwerfen der API für die Verwendung von Zustands Objekten führt zu mehreren Leistungsvorteilen.</span><span class="sxs-lookup"><span data-stu-id="7be9a-138">Designing the API to use state objects creates several performance advantages.</span></span> <span data-ttu-id="7be9a-139">Dazu gehört das Überprüfen des Zustands zum Zeitpunkt der Objekt Erstellung, das Aktivieren des zwischen Speicherns von Zustands Objekten in der Hardware und das deutlich reduzieren des Zustands, der während eines Zustands Einstellungs-API-Aufrufes übergeben wird (durch Übergabe eines Handles an das Zustands Objekt anstelle des-Zustands).</span><span class="sxs-lookup"><span data-stu-id="7be9a-139">These include validating state at object creation time, enabling caching of state objects in hardware, and greatly reducing the amount of state that is passed during a state-setting API call (by passing a handle to the state object instead of the state).</span></span>

<span data-ttu-id="7be9a-140">Um diese Leistungsverbesserungen zu erzielen, sollten Sie Ihre Zustands Objekte erstellen, wenn Ihre Anwendung gestartet wird, und zwar vor der Renderschleife.</span><span class="sxs-lookup"><span data-stu-id="7be9a-140">To achieve these performance improvements, you should create your state objects when your application starts up, well before your render loop.</span></span> <span data-ttu-id="7be9a-141">Zustands Objekte sind unveränderlich, d. h., nachdem Sie erstellt wurden, können Sie Sie nicht mehr ändern.</span><span class="sxs-lookup"><span data-stu-id="7be9a-141">State objects are immutable, that is, once they are created, you cannot change them.</span></span> <span data-ttu-id="7be9a-142">Stattdessen müssen Sie Sie löschen und neu erstellen.</span><span class="sxs-lookup"><span data-stu-id="7be9a-142">Instead you must destroy and recreate them.</span></span> <span data-ttu-id="7be9a-143">Um diese Einschränkung zu umgehen, können Sie bis zu 4096 für jeden Typ von Zustands Objekten erstellen.</span><span class="sxs-lookup"><span data-stu-id="7be9a-143">To cope with this restriction, you can create up to 4096 of each type of state objects.</span></span> <span data-ttu-id="7be9a-144">Beispielsweise können Sie mehrere samplerobjekte mit unterschiedlichen samplerstatuskombinationen erstellen.</span><span class="sxs-lookup"><span data-stu-id="7be9a-144">For example, you could create several sampler objects with various sampler-state combinations.</span></span> <span data-ttu-id="7be9a-145">Die Änderung des samplerstatus wird dann durch Aufrufen der entsprechenden Set-API durchgeführt, die ein Handle an das Objekt übergibt (im Gegensatz zum samplerzustand).</span><span class="sxs-lookup"><span data-stu-id="7be9a-145">Changing the sampler state is then accomplished by calling the appropriate Set API which passes a handle to the object (as opposed to the sampler state).</span></span> <span data-ttu-id="7be9a-146">Dadurch wird der Aufwand für jeden Rendering-Frame erheblich reduziert, um den Status zu ändern, da die Anzahl der Aufrufe und die Datenmenge erheblich reduziert wird.</span><span class="sxs-lookup"><span data-stu-id="7be9a-146">This significantly reduces the amount of overhead during each render frame for changing state since the number of calls and the amount of data are greatly reduced.</span></span>

<span data-ttu-id="7be9a-147">Wahlweise können Sie auch das Effektsystem verwenden, das die effiziente Erstellung und Zerstörung von Zustands Objekten für die Anwendung automatisch verwaltet.</span><span class="sxs-lookup"><span data-stu-id="7be9a-147">Alternatively, you can choose to use the effect system which will automatically manage efficient creation and destruction of state objects for your application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7be9a-148">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7be9a-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7be9a-149">API-Features (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="7be9a-149">API Features (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-api-features.md)
</dt> </dl>

 

 
