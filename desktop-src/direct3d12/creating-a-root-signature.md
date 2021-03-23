---
title: Erstellen einer Stamm Signatur
description: Stamm Signaturen sind eine komplexe Datenstruktur, die Struktur-Strukturen enthält.
ms.assetid: 565B28C1-DBD1-42B6-87F9-70743E4A2E4A
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9660f35c349342d147a61a6b4ce9c02a4a1abab
ms.sourcegitcommit: 65af948af39d1a31885a1b688f5dbfe955d7eba1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/18/2020
ms.locfileid: "104548658"
---
# <a name="creating-a-root-signature"></a><span data-ttu-id="5dd8f-103">Erstellen einer Stamm Signatur</span><span class="sxs-lookup"><span data-stu-id="5dd8f-103">Creating a Root Signature</span></span>

<span data-ttu-id="5dd8f-104">Stamm Signaturen sind eine komplexe Datenstruktur, die Struktur-Strukturen enthält.</span><span class="sxs-lookup"><span data-stu-id="5dd8f-104">Root signatures are a complex data structure containing nested structures.</span></span> <span data-ttu-id="5dd8f-105">Diese können Programm gesteuert mithilfe der unten stehenden Datenstruktur Definition definiert werden (die Methoden zum Initialisieren von Membern umfasst).</span><span class="sxs-lookup"><span data-stu-id="5dd8f-105">These can be defined programmatically using the data structure definition below (which includes methods to help initialize members).</span></span> <span data-ttu-id="5dd8f-106">Alternativ dazu können Sie in High Level Shading Language (HLSL) erstellt werden – dies bietet den Vorteil, dass der Compiler frühzeitig überprüft, ob das Layout mit dem Shader kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="5dd8f-106">Alternatively, they can be authored in High Level Shading Language (HLSL) – giving the advantage that the compiler will validate early that the layout is compatible with the shader.</span></span>

<span data-ttu-id="5dd8f-107">Die API zum Erstellen einer Stamm Signatur übernimmt eine serialisierte (eigenständige, Zeiger freie) Version der layoutbeschreibung, die unten beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="5dd8f-107">The API for creating a root signature takes in a serialized (self contained, pointer free) version of the layout description described below.</span></span> <span data-ttu-id="5dd8f-108">Eine Methode wird bereitgestellt, um diese serialisierte Version aus der C++-Datenstruktur zu generieren, aber eine andere Möglichkeit zum Abrufen einer serialisierten Stamm Signatur Definition besteht darin, Sie aus einem Shader abzurufen, der mit einer Stamm Signatur kompiliert wurde.</span><span class="sxs-lookup"><span data-stu-id="5dd8f-108">A method is provided for generating this serialized version from the C++ data structure, but another way to obtain a serialized root signature definition is to retrieve it from a shader that has been compiled with a root signature.</span></span>

<span data-ttu-id="5dd8f-109">Wenn Sie Treiber Optimierungen für Stamm Signatur Deskriptoren und-Daten nutzen möchten, lesen Sie die Stamm [Signatur Version 1,1](root-signature-version-1-1.md) .</span><span class="sxs-lookup"><span data-stu-id="5dd8f-109">If you wish to take advantage of driver optimizations for root signature descriptors and data, refer to [Root Signature Version 1.1](root-signature-version-1-1.md)</span></span>

-   [<span data-ttu-id="5dd8f-110">Deskriptortabellenbindungstypen</span><span class="sxs-lookup"><span data-stu-id="5dd8f-110">Descriptor Table Bind Types</span></span>](#descriptor-table-bind-types)
-   [<span data-ttu-id="5dd8f-111">Deskriptorbereich</span><span class="sxs-lookup"><span data-stu-id="5dd8f-111">Descriptor Range</span></span>](#descriptor-range)
-   [<span data-ttu-id="5dd8f-112">Deskriptortabellenlayout</span><span class="sxs-lookup"><span data-stu-id="5dd8f-112">Descriptor Table Layout</span></span>](#descriptor-table-layout)
-   [<span data-ttu-id="5dd8f-113">Stamm Konstanten</span><span class="sxs-lookup"><span data-stu-id="5dd8f-113">Root Constants</span></span>](#root-constants)
-   [<span data-ttu-id="5dd8f-114">Stamm Deskriptor</span><span class="sxs-lookup"><span data-stu-id="5dd8f-114">Root Descriptor</span></span>](#root-descriptor)
-   [<span data-ttu-id="5dd8f-115">Shader-Sichtbarkeit</span><span class="sxs-lookup"><span data-stu-id="5dd8f-115">Shader Visibility</span></span>](#shader-visibility)
-   [<span data-ttu-id="5dd8f-116">Stamm Signatur Definition</span><span class="sxs-lookup"><span data-stu-id="5dd8f-116">Root Signature Definition</span></span>](#root-signature-definition)
-   [<span data-ttu-id="5dd8f-117">Serialisierung/Deserialisierung der Datenstruktur der Stamm Signatur</span><span class="sxs-lookup"><span data-stu-id="5dd8f-117">Root Signature Data Structure Serialization / Deserialization</span></span>](/windows)
-   [<span data-ttu-id="5dd8f-118">API zur Stamm Signatur Erstellung</span><span class="sxs-lookup"><span data-stu-id="5dd8f-118">Root Signature Creation API</span></span>](#root-signature-creation-api)
-   [<span data-ttu-id="5dd8f-119">Stamm Signatur in Pipeline Zustands Objekten</span><span class="sxs-lookup"><span data-stu-id="5dd8f-119">Root Signature in Pipeline State Objects</span></span>](#root-signature-in-pipeline-state-objects)
-   [<span data-ttu-id="5dd8f-120">Code zum Definieren einer Stamm Signatur der Version 1,1</span><span class="sxs-lookup"><span data-stu-id="5dd8f-120">Code for Defining a Version 1.1 Root Signature</span></span>](#code-for-defining-a-version-11-root-signature)
-   [<span data-ttu-id="5dd8f-121">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="5dd8f-121">Related topics</span></span>](#related-topics)

## <a name="descriptor-table-bind-types"></a><span data-ttu-id="5dd8f-122">Deskriptortabellenbindungstypen</span><span class="sxs-lookup"><span data-stu-id="5dd8f-122">Descriptor Table Bind Types</span></span>

<span data-ttu-id="5dd8f-123">Der [**\_ \_ Enumerationstyp D3D12 deskriptorbereichstyp \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) definiert die Typen von Deskriptoren, auf die als Teil einer deskriptortabellenlayoutdefinition verwiesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="5dd8f-123">The enum [**D3D12\_DESCRIPTOR\_RANGE\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) defines the types of descriptors that can be referenced as part of a descriptor table layout definition.</span></span>

<span data-ttu-id="5dd8f-124">Es ist ein Bereich, sodass z. b., wenn ein Teil einer Deskriptortabelle 100 Srvs hat, dieser Bereich in einem Eintrag anstelle von 100 deklariert werden kann.</span><span class="sxs-lookup"><span data-stu-id="5dd8f-124">It is a range so that, for example if part of a descriptor table has 100 SRVs, that range can be declared in one entry rather than 100.</span></span> <span data-ttu-id="5dd8f-125">Daher ist eine deskriptortabellendefinition eine Auflistung von Bereichen.</span><span class="sxs-lookup"><span data-stu-id="5dd8f-125">So a descriptor table definition is a collection of ranges.</span></span>

``` syntax
typedef enum D3D12_DESCRIPTOR_RANGE_TYPE
{
  D3D12_DESCRIPTOR_RANGE_TYPE_SRV,
  D3D12_DESCRIPTOR_RANGE_TYPE_UAV,
  D3D12_DESCRIPTOR_RANGE_TYPE_CBV,
  D3D12_DESCRIPTOR_RANGE_TYPE_SAMPLER
} D3D12_DESCRIPTOR_RANGE_TYPE;
```

## <a name="descriptor-range"></a><span data-ttu-id="5dd8f-126">Deskriptorbereich</span><span class="sxs-lookup"><span data-stu-id="5dd8f-126">Descriptor Range</span></span>

<span data-ttu-id="5dd8f-127">Die [**D3D12- \_ deskriptorbereichstruktur \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) definiert einen Bereich von Deskriptoren eines bestimmten Typs (z. b. Srvs) innerhalb einer Deskriptortabelle.</span><span class="sxs-lookup"><span data-stu-id="5dd8f-127">The [**D3D12\_DESCRIPTOR\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) structure defines a range of descriptors of a given type (such as SRVs) within a descriptor table.</span></span>

<span data-ttu-id="5dd8f-128">Das- `D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND` Makro kann in der Regel für den- `OffsetInDescriptorsFromTableStart` Parameter des [**D3D12- \_ \_ Deskriptorbereichs**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range)verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5dd8f-128">The `D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND` macro can typically be used for the `OffsetInDescriptorsFromTableStart` parameter of [**D3D12\_DESCRIPTOR\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range).</span></span> <span data-ttu-id="5dd8f-129">Dies bedeutet, dass der Deskriptorbereich angefügt wird, der nach dem vorherigen in der Deskriptortabelle definiert wird.</span><span class="sxs-lookup"><span data-stu-id="5dd8f-129">This means append the descriptor range being defined after the previous one in the descriptor table.</span></span> <span data-ttu-id="5dd8f-130">Wenn die Anwendung Alias Deskriptoren haben möchte oder aus irgendeinem Grund Slots überspringen soll, kann Sie auf einen beliebigen Offset festgelegt werden `OffsetInDescriptorsFromTableStart` .</span><span class="sxs-lookup"><span data-stu-id="5dd8f-130">If the application wants to alias descriptors or for some reason wants to skip slots, it can set `OffsetInDescriptorsFromTableStart` to whatever offset is desired.</span></span> <span data-ttu-id="5dd8f-131">Das Definieren von überlappenden Bereichen unterschiedlicher Typen ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="5dd8f-131">Defining overlapping ranges of different types is invalid.</span></span>

<span data-ttu-id="5dd8f-132">Der Satz von shaderregistern, der durch die Kombination von `RangeType` ,, und angegeben wird, `NumDescriptors` `BaseShaderRegister` `RegisterSpace` kann nicht auf Deklarationen in einer Stamm Signatur mit allgemeiner [**D3D12- \_ Shader- \_ Sicht**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) Weise in Konflikt geraten bzw. überlappen.</span><span class="sxs-lookup"><span data-stu-id="5dd8f-132">The set of shader registers specified by the combination of `RangeType`, `NumDescriptors`, `BaseShaderRegister`, and `RegisterSpace` cannot conflict or overlap across any declarations in a root signature that have common [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) (refer to the shader visibility section below).</span></span>

## <a name="descriptor-table-layout"></a><span data-ttu-id="5dd8f-133">Deskriptortabellenlayout</span><span class="sxs-lookup"><span data-stu-id="5dd8f-133">Descriptor Table Layout</span></span>

<span data-ttu-id="5dd8f-134">Die [**D3D12 \_ - \_ stammdeskriptortabellenstruktur \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) deklariert das Layout einer Deskriptortabelle als eine Auflistung von Deskriptorbereichen, die in einem deskriptorheap nacheinander angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="5dd8f-134">The [**D3D12\_ROOT\_DESCRIPTOR\_TABLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) structure declares the layout of a descriptor table as a collection of descriptor ranges that appear one after the other in a descriptor heap.</span></span> <span data-ttu-id="5dd8f-135">Samplers sind in derselben Deskriptortabelle wie CBV/UAV/Srvs nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="5dd8f-135">Samplers are not allowed in the same descriptor table as CBV/UAV/SRVs.</span></span>

<span data-ttu-id="5dd8f-136">Diese Struktur wird verwendet, wenn der Stammtyp des Signatur Slots auf festgelegt ist `D3D12_ROOT_PARAMETER_TYPE_DESCRIPTOR_TABLE` .</span><span class="sxs-lookup"><span data-stu-id="5dd8f-136">This struct is used when the root signature slot type is set to `D3D12_ROOT_PARAMETER_TYPE_DESCRIPTOR_TABLE`.</span></span>

<span data-ttu-id="5dd8f-137">Verwenden Sie zum Festlegen einer Grafik (CBV-, SRV-, UAV-, Sampler-) [**Deskriptortabelle ID3D12GraphicsCommandList:: setgraphicsrootdescriptortable**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable).</span><span class="sxs-lookup"><span data-stu-id="5dd8f-137">To set a graphics (CBV, SRV, UAV, Sampler) descriptor table, use [**ID3D12GraphicsCommandList::SetGraphicsRootDescriptorTable**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable).</span></span>

<span data-ttu-id="5dd8f-138">Um eine COMPUTE-Deskriptortabelle festzulegen, verwenden Sie [**ID3D12GraphicsCommandList:: setcomputerootdescriptortable**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable).</span><span class="sxs-lookup"><span data-stu-id="5dd8f-138">To set a compute descriptor table, use [**ID3D12GraphicsCommandList::SetComputeRootDescriptorTable**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable).</span></span>

## <a name="root-constants"></a><span data-ttu-id="5dd8f-139">Stamm Konstanten</span><span class="sxs-lookup"><span data-stu-id="5dd8f-139">Root Constants</span></span>

<span data-ttu-id="5dd8f-140">Die Struktur der D3D12-Stamm [**\_ \_ Konstanten**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) deklariert Konstanten Inline in der Stamm Signatur, die in Shadern als ein konstanter Puffer angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="5dd8f-140">The [**D3D12\_ROOT\_CONSTANTS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) structure declares constants inline in the root signature that appear in shaders as one constant buffer.</span></span>

<span data-ttu-id="5dd8f-141">Diese Struktur wird verwendet, wenn der Stammtyp des Signatur Slots auf festgelegt ist `D3D12_ROOT_PARAMETER_TYPE_32BIT_CONSTANTS` .</span><span class="sxs-lookup"><span data-stu-id="5dd8f-141">This struct is used when the root signature slot type is set to `D3D12_ROOT_PARAMETER_TYPE_32BIT_CONSTANTS`.</span></span>

## <a name="root-descriptor"></a><span data-ttu-id="5dd8f-142">Stamm Deskriptor</span><span class="sxs-lookup"><span data-stu-id="5dd8f-142">Root Descriptor</span></span>

<span data-ttu-id="5dd8f-143">Die [**D3D12 \_ - \_ stammdeskriptorstruktur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) deklariert Deskriptoren (die in Shadern angezeigt werden) Inline in der Stamm Signatur.</span><span class="sxs-lookup"><span data-stu-id="5dd8f-143">The [**D3D12\_ROOT\_DESCRIPTOR**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) structure declares descriptors (that appear in shaders) inline in the root signature.</span></span>

<span data-ttu-id="5dd8f-144">Diese Struktur wird verwendet, wenn der Stammtyp des Signatur Slots auf oder festgelegt ist `D3D12_ROOT_PARAMETER_TYPE_CBV` `D3D12_ROOT_PARAMETER_TYPE_SRV` `D3D12_ROOT_PARAMETER_TYPE_UAV` .</span><span class="sxs-lookup"><span data-stu-id="5dd8f-144">This struct is used when the root signature slot type is set to `D3D12_ROOT_PARAMETER_TYPE_CBV`, `D3D12_ROOT_PARAMETER_TYPE_SRV` or `D3D12_ROOT_PARAMETER_TYPE_UAV`.</span></span>

## <a name="shader-visibility"></a><span data-ttu-id="5dd8f-145">Shader-Sichtbarkeit</span><span class="sxs-lookup"><span data-stu-id="5dd8f-145">Shader Visibility</span></span>

<span data-ttu-id="5dd8f-146">Der Member der [**D3D12 \_ Shader \_ Visibility**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) -Enumeration, die in den Shader Visibility-Parameter des [**D3D12 \_ root- \_ Parameters**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) festgelegt ist, bestimmt, welche Shader den Inhalt eines bestimmten Stamm Signatur Slots sehen.</span><span class="sxs-lookup"><span data-stu-id="5dd8f-146">The member of [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) enum set into the shader visibility parameter of [**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) determines which shaders see the contents of a given root signature slot.</span></span> <span data-ttu-id="5dd8f-147">COMPUTE verwendet immer \_ alle (da es nur eine aktive Phase gibt).</span><span class="sxs-lookup"><span data-stu-id="5dd8f-147">Compute always uses \_ALL (since there is only one active stage).</span></span> <span data-ttu-id="5dd8f-148">Grafiken können auswählen. Wenn jedoch all verwendet wird \_ , sehen alle Shader-Stufen, was an den Stamm Signatur Slot gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="5dd8f-148">Graphics can choose, but if it uses \_ALL, all shader stages see whatever is bound at the root signature slot.</span></span>

<span data-ttu-id="5dd8f-149">Eine Verwendung der Shader-Sichtbarkeit besteht darin, Shadern zu unterstützen, die erstellt werden, die unterschiedliche Bindungen pro Shader-Stufe mithilfe eines überlappenden Namespace erwarten</span><span class="sxs-lookup"><span data-stu-id="5dd8f-149">One use of shader visibility is to help with shaders that are authored expecting different bindings per shader stage using an overlapping namespace.</span></span> <span data-ttu-id="5dd8f-150">Beispielsweise kann ein Vertex-Shader Folgendes deklarieren:</span><span class="sxs-lookup"><span data-stu-id="5dd8f-150">For example, a vertex shader may declare:</span></span>

 

<span data-ttu-id="5dd8f-151">Texture2D foo: Register (T0); "</span><span class="sxs-lookup"><span data-stu-id="5dd8f-151">Texture2D foo : register(t0);"</span></span>

 

<span data-ttu-id="5dd8f-152">Außerdem kann der Pixelshader Folgendes deklarieren:</span><span class="sxs-lookup"><span data-stu-id="5dd8f-152">and the pixel shader may also declare:</span></span>

 

<span data-ttu-id="5dd8f-153">Texture2D Bar: Register (T0);</span><span class="sxs-lookup"><span data-stu-id="5dd8f-153">Texture2D bar : register(t0);</span></span>

<span data-ttu-id="5dd8f-154">Wenn die Anwendung eine Stamm Signatur Bindung an T0 Visibility all vornimmt \_ , sehen beide Shader dieselbe Textur.</span><span class="sxs-lookup"><span data-stu-id="5dd8f-154">If the application makes a root signature binding to t0 VISIBILITY\_ALL, both shaders see the same texture.</span></span> <span data-ttu-id="5dd8f-155">Wenn der Shader definiert, dass jeder Shader verschiedene Texturen anzeigen soll, kann er 2 Stamm Signatur Slots mit Sichtbarkeit \_ Vertex und \_ Pixel definieren.</span><span class="sxs-lookup"><span data-stu-id="5dd8f-155">If the shader defines actually wants each shader to see different textures, it can define 2 root signature slots with VISIBILITY\_VERTEX and \_PIXEL.</span></span> <span data-ttu-id="5dd8f-156">Unabhängig von der Sichtbarkeit in einem Stamm Signatur Slot hat Sie immer die gleichen Kosten (nur in Abhängigkeit davon, was der slottype ist), bis zu einer maximalen maximalen Stamm Signatur Größe.</span><span class="sxs-lookup"><span data-stu-id="5dd8f-156">No matter what the visibility is on a root signature slot, it always has the same cost (cost only depending on what the SlotType is) towards one fixed maximum root signature size.</span></span>

<span data-ttu-id="5dd8f-157">Bei Low-End-D3D11-Hardware \_ wird die Sichtbarkeit von Shader ebenfalls berücksichtigt, wenn die Größe von deskriptortabellen in einem Stamm Layout überprüft wird, da einige D3D11-Hardware nur eine maximale Menge an Bindungen pro Phase unterstützen kann.</span><span class="sxs-lookup"><span data-stu-id="5dd8f-157">On low end D3D11 hardware, SHADER\_VISIBILITY is also taken into account used when validating the sizes of descriptor tables in a root layout, since some D3D11 hardware can only support a maximum amount of bindings per-stage.</span></span> <span data-ttu-id="5dd8f-158">Diese Einschränkungen gelten nur, wenn Sie auf niedriger Ebene Hardware ausführen und nicht mehr moderne Hardware einschränken.</span><span class="sxs-lookup"><span data-stu-id="5dd8f-158">These restrictions are only imposed when running on low tier hardware and do not limit more modern hardware at all.</span></span>

<span data-ttu-id="5dd8f-159">Wenn für eine Stamm Signatur mehrere deskriptortabellen definiert sind, die sich im Namespace gegenseitig überlappen (die Register Bindungen an den Shader) und jeder von Ihnen \_ für die Sichtbarkeit angibt, ist das Layout ungültig (bei der Erstellung tritt ein Fehler auf).</span><span class="sxs-lookup"><span data-stu-id="5dd8f-159">If a root signature has multiple descriptor tables defined that overlap each other in namespace (the register bindings to the shader) and any one of them specifies \_ALL for visibility, the layout is invalid (creation will fail).</span></span>

## <a name="root-signature-definition"></a><span data-ttu-id="5dd8f-160">Stamm Signatur Definition</span><span class="sxs-lookup"><span data-stu-id="5dd8f-160">Root Signature Definition</span></span>

<span data-ttu-id="5dd8f-161">Die [**D3D12-Stamm \_ Signatur- \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) -Struktur kann deskriptortabellen und Inline Konstanten enthalten, die jeweils durch die D3D12-Stamm [**\_ \_ Parameter**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) Struktur und den [**\_ \_ \_ Enumerationstyp D3D12 root Parametertyp**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_parameter_type)definiert werden.</span><span class="sxs-lookup"><span data-stu-id="5dd8f-161">The [**D3D12\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) structure can contain descriptor tables and inline constants, each slot type defined by the [**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) structure and the enum [**D3D12\_ROOT\_PARAMETER\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_parameter_type).</span></span>

<span data-ttu-id="5dd8f-162">Um einen Stamm Signatur Slot zu initiieren, lesen Sie die Methoden **\* \* \* setcomputeroot** und **\* \* \* setgraphicsroot** von [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist).</span><span class="sxs-lookup"><span data-stu-id="5dd8f-162">To initiate a root signature slot, refer to the **SetComputeRoot\*\*\*** and **SetGraphicsRoot\*\*\*** methods of [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist).</span></span>

<span data-ttu-id="5dd8f-163">Statische Samplern werden in der Stamm Signatur mithilfe der [**D3D12 \_ static \_ -**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) samplerstruktur beschrieben.</span><span class="sxs-lookup"><span data-stu-id="5dd8f-163">Static samplers are described in the root signature using the [**D3D12\_STATIC\_SAMPLER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) structure.</span></span>

<span data-ttu-id="5dd8f-164">Eine Anzahl von Flags schränkt den Zugriff bestimmter Shader auf die Stamm Signatur ein. Weitere Informationen finden Sie unter [**D3D12 \_ root \_ Signature \_ Flags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags).</span><span class="sxs-lookup"><span data-stu-id="5dd8f-164">A number of flags limit the access of certain shaders to the root signature, refer to [**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags).</span></span>

## <a name="root-signature-data-structure-serialization--deserialization"></a><span data-ttu-id="5dd8f-165">Serialisierung/Deserialisierung der Datenstruktur der Stamm Signatur</span><span class="sxs-lookup"><span data-stu-id="5dd8f-165">Root Signature Data Structure Serialization / Deserialization</span></span>

<span data-ttu-id="5dd8f-166">Die in diesem Abschnitt beschriebenen Methoden werden von D3D12Core.dll exportiert und stellen Methoden zum Serialisieren und Deserialisieren einer Stamm Signatur Datenstruktur bereit.</span><span class="sxs-lookup"><span data-stu-id="5dd8f-166">The methods described in this section are exported by D3D12Core.dll and provide methods for serializing and deserializing a root signature data structure.</span></span>

<span data-ttu-id="5dd8f-167">Beim Erstellen einer Stamm Signatur wird die serialisierte Form an die API übermittelt.</span><span class="sxs-lookup"><span data-stu-id="5dd8f-167">The serialized form is what is passed into the API when creating a root signature.</span></span> <span data-ttu-id="5dd8f-168">Wenn ein Shader mit einer Stamm Signatur erstellt wurde (wenn diese Funktion hinzugefügt wird), enthält der kompilierte Shader bereits eine serialisierte Stamm Signatur.</span><span class="sxs-lookup"><span data-stu-id="5dd8f-168">If a shader has been authored with a root signature in it (when that capability is added), then the compiled shader will contain a serialized root signature in it already.</span></span>

<span data-ttu-id="5dd8f-169">Wenn eine Anwendung prozedurale eine [**D3D12-Stamm \_ \_ Signatur \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) -Datenstruktur generiert, muss Sie das serialisierte Formular mithilfe von [**D3D12SerializeRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializerootsignature)erstellen.</span><span class="sxs-lookup"><span data-stu-id="5dd8f-169">If an application procedurally generates a [**D3D12\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) data structure, it must make the serialized form using [**D3D12SerializeRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializerootsignature).</span></span> <span data-ttu-id="5dd8f-170">Die Ausgabe von, die an [**ID3D12Device:: | aterootsignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature)übergeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="5dd8f-170">The output of that can be passed into [**ID3D12Device::CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature).</span></span>

<span data-ttu-id="5dd8f-171">Wenn eine Anwendung bereits über eine serialisierte Stamm Signatur verfügt oder über einen kompilierten Shader verfügt, der eine Stamm Signatur enthält, und die Layoutdefinition Programm gesteuert ermitteln möchte (als "Reflektion" bezeichnet), kann [**D3D12CreateRootSignatureDeserializer**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createrootsignaturedeserializer) aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="5dd8f-171">If an application has a serialized root signature already, or has a compiled shader that contains a root signature and wishes to programmatically discover the layout definition (known as "reflection"), [**D3D12CreateRootSignatureDeserializer**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createrootsignaturedeserializer) can be called.</span></span> <span data-ttu-id="5dd8f-172">Dadurch wird eine [**ID3D12RootSignatureDeserializer**](/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignaturedeserializer) -Schnittstelle generiert, die eine Methode zum Zurückgeben der deserialisierten [**D3D12 \_ root \_ Signature \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) -Datenstruktur enthält.</span><span class="sxs-lookup"><span data-stu-id="5dd8f-172">This generates an [**ID3D12RootSignatureDeserializer**](/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignaturedeserializer) interface, which contains a method to return the deserialized [**D3D12\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) data structure.</span></span> <span data-ttu-id="5dd8f-173">Die-Schnittstelle besitzt die Lebensdauer der deserialisierten Datenstruktur.</span><span class="sxs-lookup"><span data-stu-id="5dd8f-173">The interface owns the lifetime of the deserialized data structure.</span></span>

## <a name="root-signature-creation-api"></a><span data-ttu-id="5dd8f-174">API zur Stamm Signatur Erstellung</span><span class="sxs-lookup"><span data-stu-id="5dd8f-174">Root Signature Creation API</span></span>

<span data-ttu-id="5dd8f-175">Die [**ID3D12Device:: kreaterootsignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature) -API übernimmt eine serialisierte Version einer Stamm Signatur.</span><span class="sxs-lookup"><span data-stu-id="5dd8f-175">The [**ID3D12Device::CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature) API takes in a serialized version of a root signature.</span></span>

## <a name="root-signature-in-pipeline-state-objects"></a><span data-ttu-id="5dd8f-176">Stamm Signatur in Pipeline Zustands Objekten</span><span class="sxs-lookup"><span data-stu-id="5dd8f-176">Root Signature in Pipeline State Objects</span></span>

<span data-ttu-id="5dd8f-177">Die Methoden zum Erstellen des Pipeline Zustands ([**ID3D12Device:: anategraphicspipelinestate**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) und [**ID3D12Device:: aufgabencomputepipelinestate**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcomputepipelinestate) ) akzeptieren eine optionale [**ID3D12RootSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature) -Schnittstelle als Eingabeparameter (gespeichert in einer [**D3D12- \_ Grafik \_ Pipeline \_ State \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) -Struktur).</span><span class="sxs-lookup"><span data-stu-id="5dd8f-177">The methods to create pipeline state ([**ID3D12Device::CreateGraphicsPipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) and [**ID3D12Device::CreateComputePipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcomputepipelinestate) ) take an optional [**ID3D12RootSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature) interface as an input parameter (stored in a [**D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) structure).</span></span> <span data-ttu-id="5dd8f-178">Dadurch wird jede bereits in den Shadern bereits Stamm Signatur überschrieben.</span><span class="sxs-lookup"><span data-stu-id="5dd8f-178">This will override any root signature already in the shaders.</span></span>

<span data-ttu-id="5dd8f-179">Wenn eine Stamm Signatur an eine der Create Pipeline State-Methoden übergeben wird, wird diese Stamm Signatur anhand aller Shader in der PSO aus Kompatibilitätsgründen überprüft und an den Treiber übergeben, der für alle Shader verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5dd8f-179">If a root signature is passed into one of the create pipeline state methods, this root signature is validated against all the shaders in the PSO for compatibility and given to the driver to use with all the shaders.</span></span> <span data-ttu-id="5dd8f-180">Wenn einer der Shader eine andere Stamm Signatur aufweist, wird er durch die an der API über gegebene Stamm Signatur ersetzt.</span><span class="sxs-lookup"><span data-stu-id="5dd8f-180">If any of the shaders has a different root signature in it, it gets replaced by the root signature passed in at the API.</span></span> <span data-ttu-id="5dd8f-181">Wenn eine Stamm Signatur nicht übergeben wird, müssen alle an übergebenen Shader über eine Stamm Signatur verfügen, und Sie müssen mit – versehen werden.</span><span class="sxs-lookup"><span data-stu-id="5dd8f-181">If a root signature is not passed in, all shaders passed in must have a root signature and they must match – this will be given to the driver.</span></span> <span data-ttu-id="5dd8f-182">Durch das Festlegen eines PSO in einer Befehlsliste oder eines Pakets wird die Stamm Signatur nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="5dd8f-182">Setting a PSO on a command list or bundle does not change the root signature.</span></span> <span data-ttu-id="5dd8f-183">Dies wird durch die Methoden [**setgraphicsrootsignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootsignature) und [**setcomputerootsignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootsignature)erreicht.</span><span class="sxs-lookup"><span data-stu-id="5dd8f-183">That is accomplished by the methods [**SetGraphicsRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootsignature) and [**SetComputeRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootsignature).</span></span> <span data-ttu-id="5dd8f-184">Wenn/Dispatch (Compute) aufgerufen wird, muss die Anwendung sicherstellen, dass das aktuelle PSO mit der aktuellen Stamm Signatur übereinstimmt. Andernfalls ist das Verhalten nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="5dd8f-184">By the time draw(graphics)/dispatch(compute) is invoked, the application must ensure that the current PSO matches the current root signature; otherwise, the behavior is undefined.</span></span>

## <a name="code-for-defining-a-version-11-root-signature"></a><span data-ttu-id="5dd8f-185">Code zum Definieren einer Stamm Signatur der Version 1,1</span><span class="sxs-lookup"><span data-stu-id="5dd8f-185">Code for Defining a Version 1.1 Root Signature</span></span>

<span data-ttu-id="5dd8f-186">Im folgenden Beispiel wird gezeigt, wie eine Stamm Signatur im folgenden Format erstellt wird:</span><span class="sxs-lookup"><span data-stu-id="5dd8f-186">The example below shows how to create a root signature with the following format:</span></span>



|                        |                                                |                                              |
|------------------------|------------------------------------------------|----------------------------------------------|
| <span data-ttu-id="5dd8f-187">**Rootparameterindex**</span><span class="sxs-lookup"><span data-stu-id="5dd8f-187">**RootParameterIndex**</span></span> | <span data-ttu-id="5dd8f-188">**Contents**</span><span class="sxs-lookup"><span data-stu-id="5dd8f-188">**Contents**</span></span>                                   |                                              |
| <span data-ttu-id="5dd8f-189">\[0\]</span><span class="sxs-lookup"><span data-stu-id="5dd8f-189">\[0\]</span></span>                  | <span data-ttu-id="5dd8f-190">Stamm Konstanten: {B2}</span><span class="sxs-lookup"><span data-stu-id="5dd8f-190">Root constants: { b2 }</span></span>                         | <span data-ttu-id="5dd8f-191">(1 CBV)</span><span class="sxs-lookup"><span data-stu-id="5dd8f-191">(1 CBV)</span></span>                                      |
| <span data-ttu-id="5dd8f-192">\[1\]</span><span class="sxs-lookup"><span data-stu-id="5dd8f-192">\[1\]</span></span>                  | <span data-ttu-id="5dd8f-193">Deskriptortabelle: {T2-T7, U0-U3}</span><span class="sxs-lookup"><span data-stu-id="5dd8f-193">Descriptor table: { t2-t7, u0-u3 }</span></span>             | <span data-ttu-id="5dd8f-194">(6 Srvs + 4 UAVs)</span><span class="sxs-lookup"><span data-stu-id="5dd8f-194">(6 SRVs + 4 UAVs)</span></span>                            |
| <span data-ttu-id="5dd8f-195">\[2\]</span><span class="sxs-lookup"><span data-stu-id="5dd8f-195">\[2\]</span></span>                  | <span data-ttu-id="5dd8f-196">Root CBV: {B0}</span><span class="sxs-lookup"><span data-stu-id="5dd8f-196">Root CBV: { b0 }</span></span>                               | <span data-ttu-id="5dd8f-197">(1 CBV, statische Daten)</span><span class="sxs-lookup"><span data-stu-id="5dd8f-197">(1 CBV, static data)</span></span>                         |
| <span data-ttu-id="5dd8f-198">\[3\]</span><span class="sxs-lookup"><span data-stu-id="5dd8f-198">\[3\]</span></span>                  | <span data-ttu-id="5dd8f-199">Deskriptortabelle: {S0-S1}</span><span class="sxs-lookup"><span data-stu-id="5dd8f-199">Descriptor table: { s0-s1 }</span></span>                    | <span data-ttu-id="5dd8f-200">(2 Samplers)</span><span class="sxs-lookup"><span data-stu-id="5dd8f-200">(2 Samplers)</span></span>                                 |
| <span data-ttu-id="5dd8f-201">\[4\]</span><span class="sxs-lookup"><span data-stu-id="5dd8f-201">\[4\]</span></span>                  | <span data-ttu-id="5dd8f-202">Deskriptortabelle: {T8-ungebunden}</span><span class="sxs-lookup"><span data-stu-id="5dd8f-202">Descriptor table: { t8 - unbounded }</span></span>           | <span data-ttu-id="5dd8f-203">(ungebunden \# von Srvs, flüchtige Deskriptoren)</span><span class="sxs-lookup"><span data-stu-id="5dd8f-203">(unbounded \# of SRVs, volatile descriptors)</span></span> |
| <span data-ttu-id="5dd8f-204">\[5\]</span><span class="sxs-lookup"><span data-stu-id="5dd8f-204">\[5\]</span></span>                  | <span data-ttu-id="5dd8f-205">Deskriptortabelle: {(T0, festplattenspeicher1)-ungebunden}</span><span class="sxs-lookup"><span data-stu-id="5dd8f-205">Descriptor table: { (t0, space1) - unbounded }</span></span> | <span data-ttu-id="5dd8f-206">(ungebunden \# von Srvs, flüchtige Deskriptoren)</span><span class="sxs-lookup"><span data-stu-id="5dd8f-206">(unbounded \# of SRVs, volatile descriptors)</span></span> |
| <span data-ttu-id="5dd8f-207">\[6\]</span><span class="sxs-lookup"><span data-stu-id="5dd8f-207">\[6\]</span></span>                  | <span data-ttu-id="5dd8f-208">Deskriptortabelle: {B1}</span><span class="sxs-lookup"><span data-stu-id="5dd8f-208">Descriptor table: { b1 }</span></span>                       | <span data-ttu-id="5dd8f-209">(1 CBV, statische Daten)</span><span class="sxs-lookup"><span data-stu-id="5dd8f-209">(1 CBV, static data)</span></span>                         |



 

<span data-ttu-id="5dd8f-210">Wenn die meisten Teile der Stamm Signatur in den meisten Fällen verwendet werden, kann es besser sein, die Stamm Signatur zu häufig zu ändern.</span><span class="sxs-lookup"><span data-stu-id="5dd8f-210">If most parts of the root signature get used most of the time it can be better than having to switch the root signature too frequently.</span></span> <span data-ttu-id="5dd8f-211">Anwendungen sollten Einträge in der Stamm Signatur von der am häufigsten zu den geringsten Änderungen sortieren.</span><span class="sxs-lookup"><span data-stu-id="5dd8f-211">Applications should sort entries in the root signature from most frequently changing to least.</span></span> <span data-ttu-id="5dd8f-212">Wenn eine APP die Bindungen in einen beliebigen Teil der Stamm Signatur ändert, muss der Treiber möglicherweise eine Kopie des root-Signatur Zustands erstellen, was zu nicht trivialen Kosten werden kann, wenn er über viele Zustandsänderungen hinweg multipliziert wird.</span><span class="sxs-lookup"><span data-stu-id="5dd8f-212">When an app changes the bindings to any part of the root signature, the driver may have to make a copy of some or all of root signature state, which can become a nontrivial cost when multiplied across many state changes.</span></span>

<span data-ttu-id="5dd8f-213">Außerdem wird durch die Stamm Signatur ein statischer Sampler definiert, der die anisotrope Textur Filterung im Shader-Register S3 durchführt.</span><span class="sxs-lookup"><span data-stu-id="5dd8f-213">In addition, the root signature will define a static sampler that does anisotropic texture filtering at shader register s3.</span></span>

<span data-ttu-id="5dd8f-214">Nachdem diese Stamm Signatur gebunden ist, können deskriptortabellen, root CBV und Konstanten dem \[ Parameter Bereich 0.. 6 zugewiesen werden \] .</span><span class="sxs-lookup"><span data-stu-id="5dd8f-214">After this root signature is bound, descriptor tables, root CBV and constants can be assigned to the \[0..6\] parameter space.</span></span> <span data-ttu-id="5dd8f-215">Beispielsweise können deskriptortabellen (Bereiche in einem deskriptorheap) an jeden der Stamm Parameter \[ 1 \] und \[ 3.. 6 gebunden \] werden.</span><span class="sxs-lookup"><span data-stu-id="5dd8f-215">e.g. descriptor tables (ranges in a descriptor heap) can be bound at each of root parameters \[1\] and \[3..6\].</span></span>

``` syntax
CD3DX12_DESCRIPTOR_RANGE1 DescRange[6];

DescRange[0].Init(D3D12_DESCRIPTOR_RANGE_SRV,6,2); // t2-t7
DescRange[1].Init(D3D12_DESCRIPTOR_RANGE_UAV,4,0); // u0-u3
DescRange[2].Init(D3D12_DESCRIPTOR_RANGE_SAMPLER,2,0); // s0-s1
DescRange[3].Init(D3D12_DESCRIPTOR_RANGE_SRV,-1,8, 0,
                  D3D12_DESCRIPTOR_RANGE_FLAG_DESCRIPTORS_VOLATILE); // t8-unbounded
DescRange[4].Init(D3D12_DESCRIPTOR_RANGE_SRV,-1,0,1,
                  D3D12_DESCRIPTOR_RANGE_FLAG_DESCRIPTORS_VOLATILE); 
                                                            // (t0,space1)-unbounded
DescRange[5].Init(D3D12_DESCRIPTOR_RANGE_CBV,1,1,
                  D3D12_DESCRIPTOR_RANGE_FLAG_DATA_STATIC); // b1

CD3DX12_ROOT_PARAMETER1 RP[7];

RP[0].InitAsConstants(3,2); // 3 constants at b2
RP[1].InitAsDescriptorTable(2,&DescRange[0]); // 2 ranges t2-t7 and u0-u3
RP[2].InitAsConstantBufferView(0, 0, 
                               D3D12_ROOT_DESCRIPTOR_FLAG_DATA_STATIC); // b0
RP[3].InitAsDescriptorTable(1,&DescRange[2]); // s0-s1
RP[4].InitAsDescriptorTable(1,&DescRange[3]); // t8-unbounded
RP[5].InitAsDescriptorTable(1,&DescRange[4]); // (t0,space1)-unbounded
RP[6].InitAsDescriptorTable(1,&DescRange[5]); // b1

CD3DX12_STATIC_SAMPLER StaticSamplers[1];
StaticSamplers[0].Init(3, D3D12_FILTER_ANISOTROPIC); // s3
CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC RootSig(7,RP,1,StaticSamplers);
ID3DBlob* pSerializedRootSig;
CheckHR(D3D12SerializeVersionedRootSignature(&RootSig,pSerializedRootSig)); 

ID3D12RootSignature* pRootSignature;
hr = CheckHR(pDevice->CreateRootSignature(
    pSerializedRootSig->GetBufferPointer(),pSerializedRootSig->GetBufferSize(),
    __uuidof(ID3D12RootSignature),
    &pRootSignature));
```

<span data-ttu-id="5dd8f-216">Der folgende Code veranschaulicht, wie die obige Stamm Signatur in einer Grafik Befehlsliste verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="5dd8f-216">The following code illustrates how the above root signature might be used on a graphics command list.</span></span>

``` syntax
InitializeMyDescriptorHeapContentsAheadOfTime(); // for simplicity of the 
                                                 // example
CreatePipelineStatesAhreadOfTime(pRootSignature); // The root signature is passed into 
                                     // shader / pipeline state creation
...

ID3D12DescriptorHeap* pHeaps[2] = {pCommonHeap, pSamplerHeap};
pGraphicsCommandList->SetDescriptorHeaps(pHeaps,2);
pGraphicsCommandList->SetGraphicsRootSignature(pRootSignature);
pGraphicsCommandList->SetGraphicsRootDescriptorTable(
                        6,heapOffsetForMoreData,DescRange[5].NumDescriptors);
pGraphicsCommandList->SetGraphicsRootDescriptorTable(5,heapOffsetForMisc,5000); 
pGraphicsCommandList->SetGraphicsRootDescriptorTable(4,heapOffsetForTerrain,20000);
pGraphicsCommandList->SetGraphicsRootDescriptorTable(
                        3,heapOffsetForSamplers,DescRange[2].NumDescriptors);
pGraphicsCommandList->SetComputeRootConstantBufferView(2,pDynamicCBHeap,&CBVDesc);

MY_PER_DRAW_STUFF stuff;
InitMyPerDrawStuff(&stuff);
pGraphicsCommandList->SetSetGraphicsRoot32BitConstants(
                        0,&stuff,0,RTSlot[0].Constants.Num32BitValues);

SetMyRTVAndOtherMiscBindings();

for(UINT i = 0; i < numObjects; i++)
{
    pGraphicsCommandList->SetPipelineState(PSO[i]);
    pGraphicsCommandList->SetGraphicsRootDescriptorTable(
                    1,heapOffsetForFooAndBar[i],DescRange[1].NumDescriptors);
    pGraphicsCommandList->SetGraphicsRoot32BitConstant(0,&i,1,drawIDOffset);
    SetMyIndexBuffers(i);
    pGraphicsCommandList->DrawIndexedInstanced(...);
}
```

## <a name="related-topics"></a><span data-ttu-id="5dd8f-217">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="5dd8f-217">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5dd8f-218">Stamm Signaturen</span><span class="sxs-lookup"><span data-stu-id="5dd8f-218">Root Signatures</span></span>](root-signatures.md)
</dt> <dt>

[<span data-ttu-id="5dd8f-219">Angeben von Stamm Signaturen in HLSL</span><span class="sxs-lookup"><span data-stu-id="5dd8f-219">Specifying Root Signatures in HLSL</span></span>](specifying-root-signatures-in-hlsl.md)
</dt> <dt>

[<span data-ttu-id="5dd8f-220">Verwenden einer Stamm Signatur</span><span class="sxs-lookup"><span data-stu-id="5dd8f-220">Using a Root Signature</span></span>](using-a-root-signature.md)
</dt> </dl>

 

 
