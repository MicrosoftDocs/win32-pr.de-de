---
description: In Direct3D 10 wird der Gerätestatus in Zustandsobjekte eingekreist, wodurch die Kosten für Zustandsänderungen deutlich reduziert werden.
ms.assetid: b2839da9-60ed-4f6c-9cc7-eac53647cca7
title: Zustandsobjekte (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a51c05e3e220e510c462265941549f91e6368a9
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335424"
---
# <a name="state-objects-direct3d-10"></a><span data-ttu-id="3a950-103">Zustandsobjekte (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="3a950-103">State Objects (Direct3D 10)</span></span>

<span data-ttu-id="3a950-104">In Direct3D 10 wird der Gerätestatus in Zustandsobjekte eingekreist, wodurch die Kosten für Zustandsänderungen deutlich reduziert werden.</span><span class="sxs-lookup"><span data-stu-id="3a950-104">In Direct3D 10, device state is grouped into state objects which greatly reduce the cost of state changes.</span></span> <span data-ttu-id="3a950-105">Es gibt mehrere Zustandsobjekte, und jedes ist so konzipiert, dass ein Zustandssatz für eine bestimmte Pipelinephase initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="3a950-105">There are several state objects, and each one is designed to initialize a set of state for a particular pipeline stage.</span></span> <span data-ttu-id="3a950-106">Sie können bis zu 4096 der einzelnen Zustandsobjekttypen erstellen.</span><span class="sxs-lookup"><span data-stu-id="3a950-106">You can create up to 4096 of each type of state object.</span></span>

-   [<span data-ttu-id="3a950-107">Eingabelayoutzustand</span><span class="sxs-lookup"><span data-stu-id="3a950-107">Input-Layout State</span></span>](#input-layout-state)
-   [<span data-ttu-id="3a950-108">Status des Rasterizers</span><span class="sxs-lookup"><span data-stu-id="3a950-108">Rasterizer State</span></span>](#rasterizer-state)
-   [<span data-ttu-id="3a950-109">Tiefen-Schablonenzustand</span><span class="sxs-lookup"><span data-stu-id="3a950-109">Depth-Stencil State</span></span>](#depth-stencil-state)
-   [<span data-ttu-id="3a950-110">Blend-Zustand</span><span class="sxs-lookup"><span data-stu-id="3a950-110">Blend State</span></span>](#blend-state)
-   [<span data-ttu-id="3a950-111">Samplerzustand</span><span class="sxs-lookup"><span data-stu-id="3a950-111">Sampler State</span></span>](#sampler-state)
-   [<span data-ttu-id="3a950-112">Leistungsaspekte</span><span class="sxs-lookup"><span data-stu-id="3a950-112">Performance Considerations</span></span>](#performance-considerations)
-   [<span data-ttu-id="3a950-113">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="3a950-113">Related topics</span></span>](#related-topics)

## <a name="input-layout-state"></a><span data-ttu-id="3a950-114">Input-Layout Status</span><span class="sxs-lookup"><span data-stu-id="3a950-114">Input-Layout State</span></span>

<span data-ttu-id="3a950-115">Diese Zustandsgruppe (siehe [**D3D10 \_ INPUT \_ ELEMENT \_ DESC)**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc)bestimmt, wie die [Eingabe-Assembler-Stufe](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage.md) Daten aus den Eingabepuffern liest und für die Verwendung durch den Vertex-Shader zusammenstellen soll.</span><span class="sxs-lookup"><span data-stu-id="3a950-115">This group of state (see [**D3D10\_INPUT\_ELEMENT\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc)) dictates how the [input-assembler stage](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage.md) reads data out of the input buffers and assembles it for use by the vertex shader.</span></span> <span data-ttu-id="3a950-116">Dies schließt den Zustand ein, z. B. die Anzahl der Elemente im Eingabepuffer und die Signatur der Eingabedaten.</span><span class="sxs-lookup"><span data-stu-id="3a950-116">This includes state such as the number of elements in the input buffer and the signature of the input data.</span></span> <span data-ttu-id="3a950-117">Die Eingabe-Assembler-Phase ist eine neue Phase in der Pipeline, deren Aufgabe es ist, Primitive aus dem Arbeitsspeicher in die Pipeline zu streamen.</span><span class="sxs-lookup"><span data-stu-id="3a950-117">The input-assembler stage is a new stage in the pipeline whose job is to stream primitives from memory into the pipeline.</span></span>

<span data-ttu-id="3a950-118">Informationen zum Erstellen eines Eingabelayout-Zustandsobjekts finden Sie unter [**CreateInputLayout**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createinputlayout).</span><span class="sxs-lookup"><span data-stu-id="3a950-118">To create a input-layout-state object, see [**CreateInputLayout**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createinputlayout).</span></span>

## <a name="rasterizer-state"></a><span data-ttu-id="3a950-119">Status des Rasterizers</span><span class="sxs-lookup"><span data-stu-id="3a950-119">Rasterizer State</span></span>

<span data-ttu-id="3a950-120">Diese Zustandsgruppe (siehe [**D3D10 \_ RASTERIZER \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc)) initialisiert die [Rasterizerphase](../direct3d11/d3d10-graphics-programming-guide-rasterizer-stage.md).</span><span class="sxs-lookup"><span data-stu-id="3a950-120">This group of state (see [**D3D10\_RASTERIZER\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc)) initializes the [rasterizer stage](../direct3d11/d3d10-graphics-programming-guide-rasterizer-stage.md).</span></span> <span data-ttu-id="3a950-121">Dieses Objekt umfasst den Zustand, z. B. den Füll- oder CULL-Modus, das Aktivieren eines Scissor-Rechtecks zum Ausschneiden und das Festlegen von Multisampleparametern.</span><span class="sxs-lookup"><span data-stu-id="3a950-121">This object includes state such as fill or cull modes, enabling a scissor rectangle for clipping, and setting multisample parameters.</span></span> <span data-ttu-id="3a950-122">Diese Phase rastert Primitive in Pixel und führt Vorgänge wie Clipping und Zuordnen von Primitiven zum Viewport durch.</span><span class="sxs-lookup"><span data-stu-id="3a950-122">This stage rasterizes primitives into pixels, performing operations like clipping and mapping primitives to the viewport.</span></span>

<span data-ttu-id="3a950-123">Informationen zum Erstellen eines rasterizer-state-Objekts finden Sie unter [**CreateRasterizerState.**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createrasterizerstate)</span><span class="sxs-lookup"><span data-stu-id="3a950-123">To create a rasterizer-state object, see [**CreateRasterizerState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createrasterizerstate).</span></span>

## <a name="depth-stencil-state"></a><span data-ttu-id="3a950-124">Depth-Stencil Status</span><span class="sxs-lookup"><span data-stu-id="3a950-124">Depth-Stencil State</span></span>

<span data-ttu-id="3a950-125">Diese Statusgruppe (siehe [**D3D10 \_ DEPTH \_ STENCIL \_ DESC)**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc)initialisiert den Teil der Tiefenschablone der [Ausgabezusammenführungsphase.](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md)</span><span class="sxs-lookup"><span data-stu-id="3a950-125">This group of state (see [**D3D10\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc)) initializes the depth-stencil portion of the [output-merger stage](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md).</span></span> <span data-ttu-id="3a950-126">Genauer gesagt initialisiert dieses Objekt Tiefen- und Schablonentests.</span><span class="sxs-lookup"><span data-stu-id="3a950-126">More specifically, this object initializes depth and stencil testing.</span></span>

<span data-ttu-id="3a950-127">Informationen zum Erstellen eines Tiefenschablonenzustandsobjekts finden Sie unter [**CreateDepthStencilState.**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createdepthstencilstate)</span><span class="sxs-lookup"><span data-stu-id="3a950-127">To create a depth-stencil-state object, see [**CreateDepthStencilState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createdepthstencilstate).</span></span>

## <a name="blend-state"></a><span data-ttu-id="3a950-128">Blendzustand</span><span class="sxs-lookup"><span data-stu-id="3a950-128">Blend State</span></span>

<span data-ttu-id="3a950-129">Diese Statusgruppe (siehe [**D3D10 \_ BLEND \_ DESC)**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc)initialisiert den Mischungsteil der [Ausgabezusammenführungsphase](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md).</span><span class="sxs-lookup"><span data-stu-id="3a950-129">This group of state (see [**D3D10\_BLEND\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc)) initializes the blending portion of the [output-merger stage](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md).</span></span>

<span data-ttu-id="3a950-130">Informationen zum Erstellen eines Blend-State-Objekts finden Sie unter [**CreateBlendState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createblendstate).</span><span class="sxs-lookup"><span data-stu-id="3a950-130">To create a blend-state object, see [**CreateBlendState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createblendstate).</span></span>

## <a name="sampler-state"></a><span data-ttu-id="3a950-131">Samplerstatus</span><span class="sxs-lookup"><span data-stu-id="3a950-131">Sampler State</span></span>

<span data-ttu-id="3a950-132">Diese Statusgruppe (siehe [**D3D10 \_ SAMPLER \_ DESC)**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_sampler_desc)initialisiert ein Samplerobjekt.</span><span class="sxs-lookup"><span data-stu-id="3a950-132">This group of state (see [**D3D10\_SAMPLER\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_sampler_desc)) initializes a sampler object.</span></span> <span data-ttu-id="3a950-133">Ein Samplerobjekt wird von den Shaderstufen verwendet, um Texturen im Arbeitsspeicher zu filtern.</span><span class="sxs-lookup"><span data-stu-id="3a950-133">A sampler object is used by the shader stages to filter textures in memory.</span></span>



<span data-ttu-id="3a950-134">Unterschiede zwischen Direct3D 9 und Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="3a950-134">Differences between Direct3D 9 and Direct3D 10:</span></span>

- <span data-ttu-id="3a950-135">In Direct3D 10 ist das Samplerobjekt nicht mehr an eine bestimmte Textur gebunden. Es wird lediglich beschrieben, wie die Filterung bei einer angefügten Ressource durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3a950-135">In Direct3D 10, the sampler object is no longer bound to a specific texture, it just describes how to do filtering given any attached resource.</span></span>



 

<span data-ttu-id="3a950-136">Informationen zum Erstellen eines sampler-state-Objekts finden Sie unter [**CreateSamplerState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createsamplerstate).</span><span class="sxs-lookup"><span data-stu-id="3a950-136">To create a sampler-state object, see [**CreateSamplerState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createsamplerstate).</span></span>

## <a name="performance-considerations"></a><span data-ttu-id="3a950-137">Überlegungen zur Leistung</span><span class="sxs-lookup"><span data-stu-id="3a950-137">Performance Considerations</span></span>

<span data-ttu-id="3a950-138">Das Entwerfen der API für die Verwendung von Zustandsobjekten bietet mehrere Leistungsvorteile.</span><span class="sxs-lookup"><span data-stu-id="3a950-138">Designing the API to use state objects creates several performance advantages.</span></span> <span data-ttu-id="3a950-139">Dazu gehören das Überprüfen des Zustands zum Zeitpunkt der Objekterstellung, das Aktivieren der Zwischenspeicherung von Zustandsobjekten in der Hardware und die erhebliche Verringerung des Zustands, der während eines ZUSTANDSeinstellungs-API-Aufrufs übergeben wird (durch Übergeben eines Handles an das Zustandsobjekt anstelle des Zustands).</span><span class="sxs-lookup"><span data-stu-id="3a950-139">These include validating state at object creation time, enabling caching of state objects in hardware, and greatly reducing the amount of state that is passed during a state-setting API call (by passing a handle to the state object instead of the state).</span></span>

<span data-ttu-id="3a950-140">Um diese Leistungsverbesserungen zu erzielen, sollten Sie Ihre Zustandsobjekte erstellen, wenn die Anwendung gestartet wird, und zwar weit vor der Renderschleife.</span><span class="sxs-lookup"><span data-stu-id="3a950-140">To achieve these performance improvements, you should create your state objects when your application starts up, well before your render loop.</span></span> <span data-ttu-id="3a950-141">Zustandsobjekte sind unveränderlich, d. h., nachdem sie erstellt wurden, können Sie sie nicht mehr ändern.</span><span class="sxs-lookup"><span data-stu-id="3a950-141">State objects are immutable, that is, once they are created, you cannot change them.</span></span> <span data-ttu-id="3a950-142">Stattdessen müssen Sie sie zerstören und neu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3a950-142">Instead you must destroy and recreate them.</span></span> <span data-ttu-id="3a950-143">Um diese Einschränkung zu bewältigen, können Sie bis zu 4096 von jedem Typ von Zustandsobjekten erstellen.</span><span class="sxs-lookup"><span data-stu-id="3a950-143">To cope with this restriction, you can create up to 4096 of each type of state objects.</span></span> <span data-ttu-id="3a950-144">Beispielsweise können Sie mehrere Samplerobjekte mit verschiedenen Samplerzustandskombinationen erstellen.</span><span class="sxs-lookup"><span data-stu-id="3a950-144">For example, you could create several sampler objects with various sampler-state combinations.</span></span> <span data-ttu-id="3a950-145">Das Ändern des Samplerzustands wird dann durch Aufrufen der entsprechenden Set-API erreicht, die ein Handle an das Objekt übergibt (im Gegensatz zum Samplerzustand).</span><span class="sxs-lookup"><span data-stu-id="3a950-145">Changing the sampler state is then accomplished by calling the appropriate Set API which passes a handle to the object (as opposed to the sampler state).</span></span> <span data-ttu-id="3a950-146">Dadurch wird der Mehraufwand während jedes Renderframes zum Ändern des Zustands erheblich reduziert, da die Anzahl der Aufrufe und die Datenmenge erheblich reduziert werden.</span><span class="sxs-lookup"><span data-stu-id="3a950-146">This significantly reduces the amount of overhead during each render frame for changing state since the number of calls and the amount of data are greatly reduced.</span></span>

<span data-ttu-id="3a950-147">Alternativ können Sie das Effektsystem verwenden, das automatisch die effiziente Erstellung und Zerstörung von Zustandsobjekten für Ihre Anwendung verwaltet.</span><span class="sxs-lookup"><span data-stu-id="3a950-147">Alternatively, you can choose to use the effect system which will automatically manage efficient creation and destruction of state objects for your application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3a950-148">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3a950-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a950-149">API-Features (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="3a950-149">API Features (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-api-features.md)
</dt> </dl>

 

 
