---
title: Erstellen einer Stammsignatur
description: Stammsignaturen sind eine komplexe Datenstruktur, die geschachtelte Strukturen enthält.
ms.assetid: 565B28C1-DBD1-42B6-87F9-70743E4A2E4A
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed993618e021656dbc9377882e2961f7f0d62263
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335644"
---
# <a name="creating-a-root-signature"></a><span data-ttu-id="f3ca3-103">Erstellen einer Stammsignatur</span><span class="sxs-lookup"><span data-stu-id="f3ca3-103">Creating a Root Signature</span></span>

<span data-ttu-id="f3ca3-104">Stammsignaturen sind eine komplexe Datenstruktur, die geschachtelte Strukturen enthält.</span><span class="sxs-lookup"><span data-stu-id="f3ca3-104">Root signatures are a complex data structure containing nested structures.</span></span> <span data-ttu-id="f3ca3-105">Diese können programmgesteuert mithilfe der unten angegebenen Datenstrukturdefinition definiert werden (einschließlich Methoden zum Initialisieren von Membern).</span><span class="sxs-lookup"><span data-stu-id="f3ca3-105">These can be defined programmatically using the data structure definition below (which includes methods to help initialize members).</span></span> <span data-ttu-id="f3ca3-106">Alternativ können sie in HLSL (High Level Shading Language) erstellt werden, was den Vorteil bietet, dass der Compiler frühzeitig überprüft, ob das Layout mit dem Shader kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="f3ca3-106">Alternatively, they can be authored in High Level Shading Language (HLSL) – giving the advantage that the compiler will validate early that the layout is compatible with the shader.</span></span>

<span data-ttu-id="f3ca3-107">Die API zum Erstellen einer Stammsignatur verwendet eine serialisierte (eigenständige, zeigerfreie) Version der unten beschriebenen Layoutbeschreibung.</span><span class="sxs-lookup"><span data-stu-id="f3ca3-107">The API for creating a root signature takes in a serialized (self contained, pointer free) version of the layout description described below.</span></span> <span data-ttu-id="f3ca3-108">Eine Methode zum Generieren dieser serialisierten Version aus der C++-Datenstruktur wird bereitgestellt. Eine weitere Möglichkeit zum Abrufen einer serialisierten Stammsignaturdefinition besteht jedoch im Abrufen aus einem Shader, der mit einer Stammsignatur kompiliert wurde.</span><span class="sxs-lookup"><span data-stu-id="f3ca3-108">A method is provided for generating this serialized version from the C++ data structure, but another way to obtain a serialized root signature definition is to retrieve it from a shader that has been compiled with a root signature.</span></span>

<span data-ttu-id="f3ca3-109">Wenn Sie Treiberoptimierungen für Stammsignaturdeskriptoren und -daten nutzen möchten, lesen Sie [Root Signature Version 1.1.](root-signature-version-1-1.md)</span><span class="sxs-lookup"><span data-stu-id="f3ca3-109">If you wish to take advantage of driver optimizations for root signature descriptors and data, refer to [Root Signature Version 1.1](root-signature-version-1-1.md)</span></span>

-   [<span data-ttu-id="f3ca3-110">Deskriptortabellen-Bindungstypen</span><span class="sxs-lookup"><span data-stu-id="f3ca3-110">Descriptor Table Bind Types</span></span>](#descriptor-table-bind-types)
-   [<span data-ttu-id="f3ca3-111">Deskriptorbereich</span><span class="sxs-lookup"><span data-stu-id="f3ca3-111">Descriptor Range</span></span>](#descriptor-range)
-   [<span data-ttu-id="f3ca3-112">Deskriptortabellenlayout</span><span class="sxs-lookup"><span data-stu-id="f3ca3-112">Descriptor Table Layout</span></span>](#descriptor-table-layout)
-   [<span data-ttu-id="f3ca3-113">Stammkonst constants</span><span class="sxs-lookup"><span data-stu-id="f3ca3-113">Root Constants</span></span>](#root-constants)
-   [<span data-ttu-id="f3ca3-114">Stammdeskriptor</span><span class="sxs-lookup"><span data-stu-id="f3ca3-114">Root Descriptor</span></span>](#root-descriptor)
-   [<span data-ttu-id="f3ca3-115">Shadersichtbarkeit</span><span class="sxs-lookup"><span data-stu-id="f3ca3-115">Shader Visibility</span></span>](#shader-visibility)
-   [<span data-ttu-id="f3ca3-116">Stammsignaturdefinition</span><span class="sxs-lookup"><span data-stu-id="f3ca3-116">Root Signature Definition</span></span>](#root-signature-definition)
-   [<span data-ttu-id="f3ca3-117">Serialisierung/Deserialisierung der Stammsignaturdatenstruktur</span><span class="sxs-lookup"><span data-stu-id="f3ca3-117">Root Signature Data Structure Serialization / Deserialization</span></span>](/windows)
-   [<span data-ttu-id="f3ca3-118">Api zum Erstellen von Stammsignaturen</span><span class="sxs-lookup"><span data-stu-id="f3ca3-118">Root Signature Creation API</span></span>](#root-signature-creation-api)
-   [<span data-ttu-id="f3ca3-119">Stammsignatur in Pipelinezustandsobjekten</span><span class="sxs-lookup"><span data-stu-id="f3ca3-119">Root Signature in Pipeline State Objects</span></span>](#root-signature-in-pipeline-state-objects)
-   [<span data-ttu-id="f3ca3-120">Code zum Definieren einer Stammsignatur der Version 1.1</span><span class="sxs-lookup"><span data-stu-id="f3ca3-120">Code for Defining a Version 1.1 Root Signature</span></span>](#code-for-defining-a-version-11-root-signature)
-   [<span data-ttu-id="f3ca3-121">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="f3ca3-121">Related topics</span></span>](#related-topics)

## <a name="descriptor-table-bind-types"></a><span data-ttu-id="f3ca3-122">Deskriptortabellen-Bindungstypen</span><span class="sxs-lookup"><span data-stu-id="f3ca3-122">Descriptor Table Bind Types</span></span>

<span data-ttu-id="f3ca3-123">Die Enumeration [**D3D12 \_ DESCRIPTOR \_ RANGE \_ TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) definiert die Typen von Deskriptoren, auf die als Teil einer Deskriptortabellenlayoutdefinition verwiesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="f3ca3-123">The enum [**D3D12\_DESCRIPTOR\_RANGE\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) defines the types of descriptors that can be referenced as part of a descriptor table layout definition.</span></span>

<span data-ttu-id="f3ca3-124">Es handelt sich um einen Bereich, sodass dieser Bereich beispielsweise in einem Eintrag deklariert werden kann, wenn ein Teil einer Deskriptortabelle 100 SRVs enthält, anstatt in 100.</span><span class="sxs-lookup"><span data-stu-id="f3ca3-124">It is a range so that, for example if part of a descriptor table has 100 SRVs, that range can be declared in one entry rather than 100.</span></span> <span data-ttu-id="f3ca3-125">Eine Deskriptortabellendefinition ist also eine Auflistung von Bereichen.</span><span class="sxs-lookup"><span data-stu-id="f3ca3-125">So a descriptor table definition is a collection of ranges.</span></span>

``` syntax
typedef enum D3D12_DESCRIPTOR_RANGE_TYPE
{
  D3D12_DESCRIPTOR_RANGE_TYPE_SRV,
  D3D12_DESCRIPTOR_RANGE_TYPE_UAV,
  D3D12_DESCRIPTOR_RANGE_TYPE_CBV,
  D3D12_DESCRIPTOR_RANGE_TYPE_SAMPLER
} D3D12_DESCRIPTOR_RANGE_TYPE;
```

## <a name="descriptor-range"></a><span data-ttu-id="f3ca3-126">Deskriptorbereich</span><span class="sxs-lookup"><span data-stu-id="f3ca3-126">Descriptor Range</span></span>

<span data-ttu-id="f3ca3-127">Die [**D3D12 \_ DESCRIPTOR \_ RANGE-Struktur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) definiert einen Deskriptorbereich eines bestimmten Typs (z. B. SRVs) innerhalb einer Deskriptortabelle.</span><span class="sxs-lookup"><span data-stu-id="f3ca3-127">The [**D3D12\_DESCRIPTOR\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) structure defines a range of descriptors of a given type (such as SRVs) within a descriptor table.</span></span>

<span data-ttu-id="f3ca3-128">Das `D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND` Makro kann in der Regel für den `OffsetInDescriptorsFromTableStart` -Parameter von [**D3D12 \_ DESCRIPTOR \_ RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range)verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f3ca3-128">The `D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND` macro can typically be used for the `OffsetInDescriptorsFromTableStart` parameter of [**D3D12\_DESCRIPTOR\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range).</span></span> <span data-ttu-id="f3ca3-129">Dies bedeutet, dass der Deskriptorbereich, der nach dem vorherigen in der Deskriptortabelle definiert wird, angefügt wird.</span><span class="sxs-lookup"><span data-stu-id="f3ca3-129">This means append the descriptor range being defined after the previous one in the descriptor table.</span></span> <span data-ttu-id="f3ca3-130">Wenn die Anwendung Aliasdeskriptoren verwenden oder Aus irgendeinem Grund Slots überspringen möchte, kann sie `OffsetInDescriptorsFromTableStart` auf den gewünschten Offset festlegen.</span><span class="sxs-lookup"><span data-stu-id="f3ca3-130">If the application wants to alias descriptors or for some reason wants to skip slots, it can set `OffsetInDescriptorsFromTableStart` to whatever offset is desired.</span></span> <span data-ttu-id="f3ca3-131">Das Definieren überlappender Bereiche verschiedener Typen ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="f3ca3-131">Defining overlapping ranges of different types is invalid.</span></span>

<span data-ttu-id="f3ca3-132">Der Satz von Shaderregistern, die durch die Kombination von , , und angegeben werden, `RangeType` kann keine Konflikte oder `NumDescriptors` `BaseShaderRegister` `RegisterSpace` Überschneidungen zwischen Deklarationen in einer Stammsignatur mit allgemeiner [**D3D12-SHADER-SICHTBARKEIT \_ \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) verursachen (weitere Informationen finden Sie im Abschnitt zur Shadersichtbarkeit weiter unten).</span><span class="sxs-lookup"><span data-stu-id="f3ca3-132">The set of shader registers specified by the combination of `RangeType`, `NumDescriptors`, `BaseShaderRegister`, and `RegisterSpace` cannot conflict or overlap across any declarations in a root signature that have common [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) (refer to the shader visibility section below).</span></span>

## <a name="descriptor-table-layout"></a><span data-ttu-id="f3ca3-133">Deskriptortabellenlayout</span><span class="sxs-lookup"><span data-stu-id="f3ca3-133">Descriptor Table Layout</span></span>

<span data-ttu-id="f3ca3-134">Die [**D3D12 \_ ROOT \_ DESCRIPTOR \_ TABLE-Struktur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) deklariert das Layout einer Deskriptortabelle als Auflistung von Deskriptorbereichen, die nacheinander in einem Deskriptorheap angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="f3ca3-134">The [**D3D12\_ROOT\_DESCRIPTOR\_TABLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) structure declares the layout of a descriptor table as a collection of descriptor ranges that appear one after the other in a descriptor heap.</span></span> <span data-ttu-id="f3ca3-135">Sampler sind in derselben Deskriptortabelle nicht zulässig wie CBV/UAV/SRVs.</span><span class="sxs-lookup"><span data-stu-id="f3ca3-135">Samplers are not allowed in the same descriptor table as CBV/UAV/SRVs.</span></span>

<span data-ttu-id="f3ca3-136">Diese Struktur wird verwendet, wenn der Stammsignaturslottyp auf festgelegt `D3D12_ROOT_PARAMETER_TYPE_DESCRIPTOR_TABLE` ist.</span><span class="sxs-lookup"><span data-stu-id="f3ca3-136">This struct is used when the root signature slot type is set to `D3D12_ROOT_PARAMETER_TYPE_DESCRIPTOR_TABLE`.</span></span>

<span data-ttu-id="f3ca3-137">Um eine Grafikdeskriptortabelle (CBV, SRV, UAV, Sampler) festzulegen, verwenden Sie [**ID3D12GraphicsCommandList::SetGraphicsRootDescriptorTable**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable).</span><span class="sxs-lookup"><span data-stu-id="f3ca3-137">To set a graphics (CBV, SRV, UAV, Sampler) descriptor table, use [**ID3D12GraphicsCommandList::SetGraphicsRootDescriptorTable**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable).</span></span>

<span data-ttu-id="f3ca3-138">Um eine Computedeskriptortabelle festzulegen, verwenden Sie [**ID3D12GraphicsCommandList::SetComputeRootDescriptorTable**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable).</span><span class="sxs-lookup"><span data-stu-id="f3ca3-138">To set a compute descriptor table, use [**ID3D12GraphicsCommandList::SetComputeRootDescriptorTable**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable).</span></span>

## <a name="root-constants"></a><span data-ttu-id="f3ca3-139">Stammkonstanten</span><span class="sxs-lookup"><span data-stu-id="f3ca3-139">Root Constants</span></span>

<span data-ttu-id="f3ca3-140">Die [**D3D12 \_ ROOT \_ CONSTANTS-Struktur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) deklariert Konstanten inline in der Stammsignatur, die in Shadern als ein konstanter Puffer angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="f3ca3-140">The [**D3D12\_ROOT\_CONSTANTS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) structure declares constants inline in the root signature that appear in shaders as one constant buffer.</span></span>

<span data-ttu-id="f3ca3-141">Diese Struktur wird verwendet, wenn der Stammsignaturslottyp auf festgelegt `D3D12_ROOT_PARAMETER_TYPE_32BIT_CONSTANTS` ist.</span><span class="sxs-lookup"><span data-stu-id="f3ca3-141">This struct is used when the root signature slot type is set to `D3D12_ROOT_PARAMETER_TYPE_32BIT_CONSTANTS`.</span></span>

## <a name="root-descriptor"></a><span data-ttu-id="f3ca3-142">Stammdeskriptor</span><span class="sxs-lookup"><span data-stu-id="f3ca3-142">Root Descriptor</span></span>

<span data-ttu-id="f3ca3-143">Die [**D3D12 \_ ROOT \_ DESCRIPTOR-Struktur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) deklariert Deskriptoren (die in Shadern angezeigt werden) inline in der Stammsignatur.</span><span class="sxs-lookup"><span data-stu-id="f3ca3-143">The [**D3D12\_ROOT\_DESCRIPTOR**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) structure declares descriptors (that appear in shaders) inline in the root signature.</span></span>

<span data-ttu-id="f3ca3-144">Diese Struktur wird verwendet, wenn der Stammsignaturslottyp auf `D3D12_ROOT_PARAMETER_TYPE_CBV` oder `D3D12_ROOT_PARAMETER_TYPE_SRV` festgelegt `D3D12_ROOT_PARAMETER_TYPE_UAV` ist.</span><span class="sxs-lookup"><span data-stu-id="f3ca3-144">This struct is used when the root signature slot type is set to `D3D12_ROOT_PARAMETER_TYPE_CBV`, `D3D12_ROOT_PARAMETER_TYPE_SRV` or `D3D12_ROOT_PARAMETER_TYPE_UAV`.</span></span>

## <a name="shader-visibility"></a><span data-ttu-id="f3ca3-145">Shadersichtbarkeit</span><span class="sxs-lookup"><span data-stu-id="f3ca3-145">Shader Visibility</span></span>

<span data-ttu-id="f3ca3-146">Der Member der [**D3D12 \_ SHADER VISIBILITY-Aufumerierung, \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) der im Shader-Sichtbarkeitsparameter von [**D3D12 \_ ROOT \_ PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) festgelegt ist, bestimmt, welche Shader den Inhalt eines bestimmten Stammsignaturslots sehen.</span><span class="sxs-lookup"><span data-stu-id="f3ca3-146">The member of [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) enum set into the shader visibility parameter of [**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) determines which shaders see the contents of a given root signature slot.</span></span> <span data-ttu-id="f3ca3-147">Compute verwendet immer \_ ALL (da es nur eine aktive Phase gibt).</span><span class="sxs-lookup"><span data-stu-id="f3ca3-147">Compute always uses \_ALL (since there is only one active stage).</span></span> <span data-ttu-id="f3ca3-148">Grafiken können auswählen, aber wenn sie ALL verwendet, sehen alle Shaderstufen, was am \_ Stammsignaturslot gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="f3ca3-148">Graphics can choose, but if it uses \_ALL, all shader stages see whatever is bound at the root signature slot.</span></span>

<span data-ttu-id="f3ca3-149">Eine Verwendung der Shadersichtbarkeit ist die Unterstützung bei Shadern, die erstellt wurden und unterschiedliche Bindungen pro Shaderphase mithilfe eines überlappenden Namespace erwarten.</span><span class="sxs-lookup"><span data-stu-id="f3ca3-149">One use of shader visibility is to help with shaders that are authored expecting different bindings per shader stage using an overlapping namespace.</span></span> <span data-ttu-id="f3ca3-150">Beispielsweise kann ein Vertex-Shader Folgendes deklarieren:</span><span class="sxs-lookup"><span data-stu-id="f3ca3-150">For example, a vertex shader may declare:</span></span>

```hlsl
Texture2D foo : register(t0);
```

<span data-ttu-id="f3ca3-151">und der Pixel-Shader kann auch Folgendes deklarieren:</span><span class="sxs-lookup"><span data-stu-id="f3ca3-151">and the pixel shader may also declare:</span></span>

```hlsl
Texture2D bar : register(t0);
```

<span data-ttu-id="f3ca3-152">Wenn die Anwendung eine Stammsignaturbindung an t0 VISIBILITY ALL vort, sehen beide \_ Shader dieselbe Textur.</span><span class="sxs-lookup"><span data-stu-id="f3ca3-152">If the application makes a root signature binding to t0 VISIBILITY\_ALL, both shaders see the same texture.</span></span> <span data-ttu-id="f3ca3-153">Wenn der Shader definiert, dass jeder Shader tatsächlich unterschiedliche Texturen sehen soll, kann er zwei Stammsignaturslots mit VISIBILITY \_ VERTEX und \_ PIXEL definieren.</span><span class="sxs-lookup"><span data-stu-id="f3ca3-153">If the shader defines actually wants each shader to see different textures, it can define 2 root signature slots with VISIBILITY\_VERTEX and \_PIXEL.</span></span> <span data-ttu-id="f3ca3-154">Unabhängig davon, welche Sichtbarkeit für einen Stammsignaturslot gilt, hat er immer die gleichen Kosten (Kosten nur abhängig vom SlotType) für eine feste maximale Größe der Stammsignatur.</span><span class="sxs-lookup"><span data-stu-id="f3ca3-154">No matter what the visibility is on a root signature slot, it always has the same cost (cost only depending on what the SlotType is) towards one fixed maximum root signature size.</span></span>

<span data-ttu-id="f3ca3-155">Auf Low-End-D3D11-Hardware wird SHADER VISIBILITY auch bei der Validierung der Größe von Deskriptortabellen in einem Stammlayout berücksichtigt, da einige D3D11-Hardware nur eine maximale Anzahl von Bindungen pro Stufe unterstützen \_ kann.</span><span class="sxs-lookup"><span data-stu-id="f3ca3-155">On low end D3D11 hardware, SHADER\_VISIBILITY is also taken into account used when validating the sizes of descriptor tables in a root layout, since some D3D11 hardware can only support a maximum amount of bindings per-stage.</span></span> <span data-ttu-id="f3ca3-156">Diese Einschränkungen gelten nur bei der Ausführung auf niedriger Hardwareebene und schränken keine modernere Hardware ein.</span><span class="sxs-lookup"><span data-stu-id="f3ca3-156">These restrictions are only imposed when running on low tier hardware and do not limit more modern hardware at all.</span></span>

<span data-ttu-id="f3ca3-157">Wenn für eine Stammsignatur mehrere Deskriptortabellen definiert sind, die sich im Namespace überlappen (die Registerbindungen an den Shader), und eine davon \_ all für die Sichtbarkeit angibt, ist das Layout ungültig (die Erstellung schlägt fehl).</span><span class="sxs-lookup"><span data-stu-id="f3ca3-157">If a root signature has multiple descriptor tables defined that overlap each other in namespace (the register bindings to the shader) and any one of them specifies \_ALL for visibility, the layout is invalid (creation will fail).</span></span>

## <a name="root-signature-definition"></a><span data-ttu-id="f3ca3-158">Stammsignaturdefinition</span><span class="sxs-lookup"><span data-stu-id="f3ca3-158">Root Signature Definition</span></span>

<span data-ttu-id="f3ca3-159">Die [**D3D12 \_ ROOT SIGNATURE \_ \_ DESC-Struktur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) kann Deskriptortabellen und Inlinekonstanten enthalten, wobei jeder Slottyp durch die [**D3D12 \_ ROOT \_ PARAMETER-Struktur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) und die Enumeration [**D3D12 \_ ROOT PARAMETER \_ \_ TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_parameter_type)definiert wird.</span><span class="sxs-lookup"><span data-stu-id="f3ca3-159">The [**D3D12\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) structure can contain descriptor tables and inline constants, each slot type defined by the [**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) structure and the enum [**D3D12\_ROOT\_PARAMETER\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_parameter_type).</span></span>

<span data-ttu-id="f3ca3-160">Informationen zum Initiieren eines Stammsignaturslots finden Sie in den Methoden **SetComputeRoot \* \* \*** und **\* \* \* SetGraphicsRoot** von [**ID3D12GraphicsCommandList.**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist)</span><span class="sxs-lookup"><span data-stu-id="f3ca3-160">To initiate a root signature slot, refer to the **SetComputeRoot\*\*\*** and **SetGraphicsRoot\*\*\*** methods of [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist).</span></span>

<span data-ttu-id="f3ca3-161">Statische Sampler werden in der Stammsignatur mithilfe der [**D3D12 \_ STATIC \_ SAMPLER-Struktur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f3ca3-161">Static samplers are described in the root signature using the [**D3D12\_STATIC\_SAMPLER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) structure.</span></span>

<span data-ttu-id="f3ca3-162">Eine Reihe von Flags schränkt den Zugriff bestimmter Shader auf die Stammsignatur ein. Weitere Informationen finden Sie unter [**D3D12 \_ ROOT \_ SIGNATURE \_ FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags).</span><span class="sxs-lookup"><span data-stu-id="f3ca3-162">A number of flags limit the access of certain shaders to the root signature, refer to [**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags).</span></span>

## <a name="root-signature-data-structure-serialization--deserialization"></a><span data-ttu-id="f3ca3-163">Serialisierung/Deserialisierung der Stammsignaturdatenstruktur</span><span class="sxs-lookup"><span data-stu-id="f3ca3-163">Root Signature Data Structure Serialization / Deserialization</span></span>

<span data-ttu-id="f3ca3-164">Die in diesem Abschnitt beschriebenen Methoden werden von D3D12Core.dll exportiert und stellen Methoden zum Serialisieren und Deserialisieren einer Stammsignaturdatenstruktur bereit.</span><span class="sxs-lookup"><span data-stu-id="f3ca3-164">The methods described in this section are exported by D3D12Core.dll and provide methods for serializing and deserializing a root signature data structure.</span></span>

<span data-ttu-id="f3ca3-165">Das serialisierte Formular wird beim Erstellen einer Stammsignatur an die API übergeben.</span><span class="sxs-lookup"><span data-stu-id="f3ca3-165">The serialized form is what is passed into the API when creating a root signature.</span></span> <span data-ttu-id="f3ca3-166">Wenn ein Shader mit einer Stammsignatur erstellt wurde (wenn diese Funktion hinzugefügt wird), enthält der kompilierte Shader bereits eine serialisierte Stammsignatur.</span><span class="sxs-lookup"><span data-stu-id="f3ca3-166">If a shader has been authored with a root signature in it (when that capability is added), then the compiled shader will contain a serialized root signature in it already.</span></span>

<span data-ttu-id="f3ca3-167">Wenn eine Anwendung prozedural eine [**D3D12 \_ ROOT \_ SIGNATURE \_ DESC-Datenstruktur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) generiert, muss sie das serialisierte Formular mithilfe von [**D3D12SerializeRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializerootsignature)erstellen.</span><span class="sxs-lookup"><span data-stu-id="f3ca3-167">If an application procedurally generates a [**D3D12\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) data structure, it must make the serialized form using [**D3D12SerializeRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializerootsignature).</span></span> <span data-ttu-id="f3ca3-168">Die Ausgabe von , die an [**ID3D12Device::CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature)übergeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="f3ca3-168">The output of that can be passed into [**ID3D12Device::CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature).</span></span>

<span data-ttu-id="f3ca3-169">Wenn eine Anwendung bereits über eine serialisierte Stammsignatur verfügt oder über einen kompilierten Shader verfügt, der eine Stammsignatur enthält und die Layoutdefinition (als "Reflektion" bezeichnet) programmgesteuert entdecken möchte, kann [**D3D12CreateRootSignatureDeserializer**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createrootsignaturedeserializer) aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="f3ca3-169">If an application has a serialized root signature already, or has a compiled shader that contains a root signature and wishes to programmatically discover the layout definition (known as "reflection"), [**D3D12CreateRootSignatureDeserializer**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createrootsignaturedeserializer) can be called.</span></span> <span data-ttu-id="f3ca3-170">Dadurch wird eine [**ID3D12RootSignatureDeserializer-Schnittstelle**](/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignaturedeserializer) generiert, die eine Methode zum Zurückgeben der deserialisierten [**D3D12 \_ ROOT SIGNATURE \_ \_ DESC-Datenstruktur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) enthält.</span><span class="sxs-lookup"><span data-stu-id="f3ca3-170">This generates an [**ID3D12RootSignatureDeserializer**](/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignaturedeserializer) interface, which contains a method to return the deserialized [**D3D12\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) data structure.</span></span> <span data-ttu-id="f3ca3-171">Die Schnittstelle besitzt die Lebensdauer der deserialisierten Datenstruktur.</span><span class="sxs-lookup"><span data-stu-id="f3ca3-171">The interface owns the lifetime of the deserialized data structure.</span></span>

## <a name="root-signature-creation-api"></a><span data-ttu-id="f3ca3-172">Api zum Erstellen von Stammsignaturen</span><span class="sxs-lookup"><span data-stu-id="f3ca3-172">Root Signature Creation API</span></span>

<span data-ttu-id="f3ca3-173">Die [**ID3D12Device::CreateRootSignature-API**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature) verwendet eine serialisierte Version einer Stammsignatur.</span><span class="sxs-lookup"><span data-stu-id="f3ca3-173">The [**ID3D12Device::CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature) API takes in a serialized version of a root signature.</span></span>

## <a name="root-signature-in-pipeline-state-objects"></a><span data-ttu-id="f3ca3-174">Stammsignatur in Pipelinezustandsobjekten</span><span class="sxs-lookup"><span data-stu-id="f3ca3-174">Root Signature in Pipeline State Objects</span></span>

<span data-ttu-id="f3ca3-175">Die Methoden zum Erstellen des Pipelinezustands ([**ID3D12Device::CreateGraphicsPipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) und [**ID3D12Device::CreateComputePipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcomputepipelinestate) ) verwenden eine optionale [**ID3D12RootSignature-Schnittstelle**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature) als Eingabeparameter (gespeichert in einer [**D3D12 \_ GRAPHICS PIPELINE STATE \_ \_ \_ DESC-Struktur).**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc)</span><span class="sxs-lookup"><span data-stu-id="f3ca3-175">The methods to create pipeline state ([**ID3D12Device::CreateGraphicsPipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) and [**ID3D12Device::CreateComputePipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcomputepipelinestate) ) take an optional [**ID3D12RootSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature) interface as an input parameter (stored in a [**D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) structure).</span></span> <span data-ttu-id="f3ca3-176">Dadurch werden alle Stammsignaturen überschrieben, die sich bereits in den Shadern enthalten.</span><span class="sxs-lookup"><span data-stu-id="f3ca3-176">This will override any root signature already in the shaders.</span></span>

<span data-ttu-id="f3ca3-177">Wenn eine Stammsignatur an eine der Methoden zum Erstellen des Pipelinezustands übergeben wird, wird diese Stammsignatur anhand aller Shader im PSO auf Kompatibilität überprüft und dem Treiber zur Verwendung mit allen Shadern übergeben.</span><span class="sxs-lookup"><span data-stu-id="f3ca3-177">If a root signature is passed into one of the create pipeline state methods, this root signature is validated against all the shaders in the PSO for compatibility and given to the driver to use with all the shaders.</span></span> <span data-ttu-id="f3ca3-178">Wenn einer der Shader über eine andere Stammsignatur verfügt, wird er durch die Stammsignatur ersetzt, die an die API übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="f3ca3-178">If any of the shaders has a different root signature in it, it gets replaced by the root signature passed in at the API.</span></span> <span data-ttu-id="f3ca3-179">Wenn keine Stammsignatur übergeben wird, müssen alle übergebenen Shader über eine Stammsignatur verfügen und übereinstimmen. Dies wird an den Treiber übergeben.</span><span class="sxs-lookup"><span data-stu-id="f3ca3-179">If a root signature is not passed in, all shaders passed in must have a root signature and they must match – this will be given to the driver.</span></span> <span data-ttu-id="f3ca3-180">Das Festlegen eines PSO für eine Befehlsliste oder ein Paket ändert nicht die Stammsignatur.</span><span class="sxs-lookup"><span data-stu-id="f3ca3-180">Setting a PSO on a command list or bundle does not change the root signature.</span></span> <span data-ttu-id="f3ca3-181">Dies wird durch die Methoden [**SetGraphicsRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootsignature) und [**SetComputeRootSignature erreicht.**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootsignature)</span><span class="sxs-lookup"><span data-stu-id="f3ca3-181">That is accomplished by the methods [**SetGraphicsRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootsignature) and [**SetComputeRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootsignature).</span></span> <span data-ttu-id="f3ca3-182">Wenn draw(graphics)/dispatch(compute) aufgerufen wird, muss die Anwendung sicherstellen, dass das aktuelle PSO der aktuellen Stammsignatur entspricht. Andernfalls ist das Verhalten nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="f3ca3-182">By the time draw(graphics)/dispatch(compute) is invoked, the application must ensure that the current PSO matches the current root signature; otherwise, the behavior is undefined.</span></span>

## <a name="code-for-defining-a-version-11-root-signature"></a><span data-ttu-id="f3ca3-183">Code zum Definieren einer Stammsignatur der Version 1.1</span><span class="sxs-lookup"><span data-stu-id="f3ca3-183">Code for Defining a Version 1.1 Root Signature</span></span>

<span data-ttu-id="f3ca3-184">Das folgende Beispiel zeigt, wie Sie eine Stammsignatur im folgenden Format erstellen:</span><span class="sxs-lookup"><span data-stu-id="f3ca3-184">The example below shows how to create a root signature with the following format:</span></span>



| <span data-ttu-id="f3ca3-185">RootParameterIndex</span><span class="sxs-lookup"><span data-stu-id="f3ca3-185">RootParameterIndex</span></span>                       | <span data-ttu-id="f3ca3-186">Inhalte</span><span class="sxs-lookup"><span data-stu-id="f3ca3-186">Contents</span></span>                                               | <span data-ttu-id="f3ca3-187">Werte</span><span class="sxs-lookup"><span data-stu-id="f3ca3-187">Values</span></span>                                             |
|------------------------|------------------------------------------------|----------------------------------------------|                                              
| <span data-ttu-id="f3ca3-188">\[0\]</span><span class="sxs-lookup"><span data-stu-id="f3ca3-188">\[0\]</span></span>                  | <span data-ttu-id="f3ca3-189">Stammkonstanten: { b2 }</span><span class="sxs-lookup"><span data-stu-id="f3ca3-189">Root constants: { b2 }</span></span>                         | <span data-ttu-id="f3ca3-190">(1 CBV)</span><span class="sxs-lookup"><span data-stu-id="f3ca3-190">(1 CBV)</span></span>                                      |
| <span data-ttu-id="f3ca3-191">\[1\]</span><span class="sxs-lookup"><span data-stu-id="f3ca3-191">\[1\]</span></span>                  | <span data-ttu-id="f3ca3-192">Deskriptortabelle: { t2-t7, u0-u3 }</span><span class="sxs-lookup"><span data-stu-id="f3ca3-192">Descriptor table: { t2-t7, u0-u3 }</span></span>             | <span data-ttu-id="f3ca3-193">(6 SRVs + 4 UAVs)</span><span class="sxs-lookup"><span data-stu-id="f3ca3-193">(6 SRVs + 4 UAVs)</span></span>                            |
| <span data-ttu-id="f3ca3-194">\[2\]</span><span class="sxs-lookup"><span data-stu-id="f3ca3-194">\[2\]</span></span>                  | <span data-ttu-id="f3ca3-195">Stamm-CBV: { b0 }</span><span class="sxs-lookup"><span data-stu-id="f3ca3-195">Root CBV: { b0 }</span></span>                               | <span data-ttu-id="f3ca3-196">(1 CBV, statische Daten)</span><span class="sxs-lookup"><span data-stu-id="f3ca3-196">(1 CBV, static data)</span></span>                         |
| <span data-ttu-id="f3ca3-197">\[3\]</span><span class="sxs-lookup"><span data-stu-id="f3ca3-197">\[3\]</span></span>                  | <span data-ttu-id="f3ca3-198">Deskriptortabelle: { s0-s1 }</span><span class="sxs-lookup"><span data-stu-id="f3ca3-198">Descriptor table: { s0-s1 }</span></span>                    | <span data-ttu-id="f3ca3-199">(2 Sampler)</span><span class="sxs-lookup"><span data-stu-id="f3ca3-199">(2 Samplers)</span></span>                                 |
| <span data-ttu-id="f3ca3-200">\[4\]</span><span class="sxs-lookup"><span data-stu-id="f3ca3-200">\[4\]</span></span>                  | <span data-ttu-id="f3ca3-201">Deskriptortabelle: { t8 – ungebunden }</span><span class="sxs-lookup"><span data-stu-id="f3ca3-201">Descriptor table: { t8 - unbounded }</span></span>           | <span data-ttu-id="f3ca3-202">(ungebunden \# von SRVs, flüchtige Deskriptoren)</span><span class="sxs-lookup"><span data-stu-id="f3ca3-202">(unbounded \# of SRVs, volatile descriptors)</span></span> |
| <span data-ttu-id="f3ca3-203">\[5\]</span><span class="sxs-lookup"><span data-stu-id="f3ca3-203">\[5\]</span></span>                  | <span data-ttu-id="f3ca3-204">Deskriptortabelle: { (t0, space1) - unbounded }</span><span class="sxs-lookup"><span data-stu-id="f3ca3-204">Descriptor table: { (t0, space1) - unbounded }</span></span> | <span data-ttu-id="f3ca3-205">(ungebunden \# von SRVs, flüchtige Deskriptoren)</span><span class="sxs-lookup"><span data-stu-id="f3ca3-205">(unbounded \# of SRVs, volatile descriptors)</span></span> |
| <span data-ttu-id="f3ca3-206">\[6\]</span><span class="sxs-lookup"><span data-stu-id="f3ca3-206">\[6\]</span></span>                  | <span data-ttu-id="f3ca3-207">Deskriptortabelle: { b1 }</span><span class="sxs-lookup"><span data-stu-id="f3ca3-207">Descriptor table: { b1 }</span></span>                       | <span data-ttu-id="f3ca3-208">(1 CBV, statische Daten)</span><span class="sxs-lookup"><span data-stu-id="f3ca3-208">(1 CBV, static data)</span></span>                         |



 

<span data-ttu-id="f3ca3-209">Wenn die meisten Teile der Stammsignatur meistens verwendet werden, kann dies besser sein, als die Stammsignatur zu häufig wechseln zu müssen.</span><span class="sxs-lookup"><span data-stu-id="f3ca3-209">If most parts of the root signature get used most of the time it can be better than having to switch the root signature too frequently.</span></span> <span data-ttu-id="f3ca3-210">Anwendungen sollten Einträge in der Stammsignatur von den am häufigsten geänderten in die geringsten Einträge sortieren.</span><span class="sxs-lookup"><span data-stu-id="f3ca3-210">Applications should sort entries in the root signature from most frequently changing to least.</span></span> <span data-ttu-id="f3ca3-211">Wenn eine App die Bindungen an einen beliebigen Teil der Stammsignatur ändert, muss der Treiber möglicherweise eine Kopie eines oder aller Stammsignaturstatus erstellen. Dies kann zu nicht typischen Kosten werden, wenn er mit vielen Zustandsänderungen multipliziert wird.</span><span class="sxs-lookup"><span data-stu-id="f3ca3-211">When an app changes the bindings to any part of the root signature, the driver may have to make a copy of some or all of root signature state, which can become a nontrivial cost when multiplied across many state changes.</span></span>

<span data-ttu-id="f3ca3-212">Darüber hinaus definiert die Stammsignatur einen statischen Sampler, der eine isisotrope Texturfilterung im Shaderregister s3 vort.</span><span class="sxs-lookup"><span data-stu-id="f3ca3-212">In addition, the root signature will define a static sampler that does anisotropic texture filtering at shader register s3.</span></span>

<span data-ttu-id="f3ca3-213">Nachdem diese Stammsignatur gebunden wurde, können Deskriptortabellen, Stamm-CBV und Konstanten dem \[ 0..6-Parameterbereich \] zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="f3ca3-213">After this root signature is bound, descriptor tables, root CBV and constants can be assigned to the \[0..6\] parameter space.</span></span> <span data-ttu-id="f3ca3-214">Beispielsweise können Deskriptortabellen (Bereiche in einem Deskriptorhap) an jeden der Stammparameter 1 und \[ \] \[ 3..6 gebunden \] werden.</span><span class="sxs-lookup"><span data-stu-id="f3ca3-214">e.g. descriptor tables (ranges in a descriptor heap) can be bound at each of root parameters \[1\] and \[3..6\].</span></span>

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

<span data-ttu-id="f3ca3-215">Der folgende Code veranschaulicht, wie die oben genannte Stammsignatur in einer Grafikbefehlsliste verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="f3ca3-215">The following code illustrates how the above root signature might be used on a graphics command list.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="f3ca3-216">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f3ca3-216">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f3ca3-217">Stammsignaturen</span><span class="sxs-lookup"><span data-stu-id="f3ca3-217">Root Signatures</span></span>](root-signatures.md)
</dt> <dt>

[<span data-ttu-id="f3ca3-218">Festlegen von Stammsignaturen in HLSL</span><span class="sxs-lookup"><span data-stu-id="f3ca3-218">Specifying Root Signatures in HLSL</span></span>](specifying-root-signatures-in-hlsl.md)
</dt> <dt>

[<span data-ttu-id="f3ca3-219">Verwenden einer Stammsignatur</span><span class="sxs-lookup"><span data-stu-id="f3ca3-219">Using a Root Signature</span></span>](using-a-root-signature.md)
</dt> </dl>

 

 
