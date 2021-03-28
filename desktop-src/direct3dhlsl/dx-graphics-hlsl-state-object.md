---
title: Statusobjekte
description: Verwenden Sie HLSL zum Definieren von Zustands Objekten.
ms.assetid: a02432dc-f354-48c0-a7ac-1ff502f3b1d1
ms.topic: article
ms.date: 2/2/2021
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 53bfc903f8bc1be56962e912b1c82f02faaf0c44
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104995286"
---
# <a name="state-objects"></a><span data-ttu-id="9b146-103">Statusobjekte</span><span class="sxs-lookup"><span data-stu-id="9b146-103">State Objects</span></span>

<span data-ttu-id="9b146-104">Mit Shader-Modellen 6,3 und höher haben Anwendungen die Möglichkeit, DXR-Zustands Objekte direkt in HLSL-Shader-Code zu definieren, zusätzlich zur Verwendung von Direct3D 12-APIs.</span><span class="sxs-lookup"><span data-stu-id="9b146-104">With shader models 6.3 and later, applications have the convenience and flexibility of being able to define DXR state objects directly in HLSL shader code in addition to using Direct3D 12 APIs.</span></span>

<span data-ttu-id="9b146-105">In HLSL werden Zustands Objekte mit der folgenden Syntax deklariert:</span><span class="sxs-lookup"><span data-stu-id="9b146-105">In HLSL, state objects are declared with this syntax:</span></span>

``` syntax
Type Name = 
{ 
    Field1,
    Field2,
    ...
};
```



| <span data-ttu-id="9b146-106">Element</span><span class="sxs-lookup"><span data-stu-id="9b146-106">Item</span></span>                                                                                         | <span data-ttu-id="9b146-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9b146-107">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9b146-108"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>**Sorte**</span><span class="sxs-lookup"><span data-stu-id="9b146-108"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>**Type**</span></span><br/>     | <span data-ttu-id="9b146-109">Identifiziert den Typ des untergeordneten Objekts.</span><span class="sxs-lookup"><span data-stu-id="9b146-109">Identifies the type of subobject.</span></span> <span data-ttu-id="9b146-110">Muss einer der unterstützten HLSL-untergeordneten Typen sein.</span><span class="sxs-lookup"><span data-stu-id="9b146-110">Must be one of the supported HLSL subobject types.</span></span><br/>     |
| <span data-ttu-id="9b146-111"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Benennen**</span><span class="sxs-lookup"><span data-stu-id="9b146-111"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**</span></span><br/>     | <span data-ttu-id="9b146-112">Eine ASCII-Zeichenfolge, die den Variablennamen eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="9b146-112">An ASCII string that uniquely identifies the variable name.</span></span><br/>                 |
| <span data-ttu-id="9b146-113"><span id="Field"></span><span id="field"></span><span id="FIELD"></span>**Feld [1, 2,...]**</span><span class="sxs-lookup"><span data-stu-id="9b146-113"><span id="Field"></span><span id="field"></span><span id="FIELD"></span>**Field[1, 2, ...]**</span></span><br/> | <span data-ttu-id="9b146-114">Felder des unter Objekts.</span><span class="sxs-lookup"><span data-stu-id="9b146-114">Fields of the subobject.</span></span> <span data-ttu-id="9b146-115">Bestimmte Felder für jeden Typ von untergeordneten Objekten werden im folgenden beschrieben.</span><span class="sxs-lookup"><span data-stu-id="9b146-115">Specific fields for each type of subobject are described below.</span></span><br/> |




<span data-ttu-id="9b146-116">Liste der untergeordneten Typen:</span><span class="sxs-lookup"><span data-stu-id="9b146-116">List of subobject types:</span></span>
-   [<span data-ttu-id="9b146-117">Stateobjectconfig</span><span class="sxs-lookup"><span data-stu-id="9b146-117">StateObjectConfig</span></span>](#stateobjectconfig)
-   [<span data-ttu-id="9b146-118">Globalrootsignature</span><span class="sxs-lookup"><span data-stu-id="9b146-118">GlobalRootSignature</span></span>](#globalrootsignature)
-   [<span data-ttu-id="9b146-119">Localrootsignature</span><span class="sxs-lookup"><span data-stu-id="9b146-119">LocalRootSignature</span></span>](#localrootsignature)
-   [<span data-ttu-id="9b146-120">Subobjectjeexportsassokation</span><span class="sxs-lookup"><span data-stu-id="9b146-120">SubobjectToExportsAssocation</span></span>](#subobjecttoexportsassocation)
-   [<span data-ttu-id="9b146-121">Raytracingshaderconfig</span><span class="sxs-lookup"><span data-stu-id="9b146-121">RaytracingShaderConfig</span></span>](#raytracingshaderconfig)
-   [<span data-ttu-id="9b146-122">Raytracingpipelineconfig</span><span class="sxs-lookup"><span data-stu-id="9b146-122">RaytracingPipelineConfig</span></span>](#raytracingpipelineconfig)
-   [<span data-ttu-id="9b146-123">"Testgruppe"</span><span class="sxs-lookup"><span data-stu-id="9b146-123">TriangleHitGroup</span></span>](#trianglehitgroup)
-   [<span data-ttu-id="9b146-124">Prozelinialprimitivehitgroup</span><span class="sxs-lookup"><span data-stu-id="9b146-124">ProceduralPrimitiveHitGroup</span></span>](#proceduralprimitivehitgroup)

## <a name="stateobjectconfig"></a><span data-ttu-id="9b146-125">Stateobjectconfig</span><span class="sxs-lookup"><span data-stu-id="9b146-125">StateObjectConfig</span></span>

<span data-ttu-id="9b146-126">Der untergeordnete Typ des stateobjectconfig-Objekts entspricht einer [D3D12_STATE_OBJECT_CONFIG](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_object_config) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="9b146-126">The StateObjectConfig subobject type corresponds to a [D3D12_STATE_OBJECT_CONFIG](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_object_config) structure.</span></span>

<span data-ttu-id="9b146-127">Sie verfügt über ein Feld, ein bitweises Flag, das eine oder beide von ist.</span><span class="sxs-lookup"><span data-stu-id="9b146-127">It has one field, a bitwise flag, which is one or both of</span></span>

* <span data-ttu-id="9b146-128">STATE_OBJECT_FLAGS_ALLOW_LOCAL_DEPENDENCIES_ON_EXTERNAL_DEFINITONS</span><span class="sxs-lookup"><span data-stu-id="9b146-128">STATE_OBJECT_FLAGS_ALLOW_LOCAL_DEPENDENCIES_ON_EXTERNAL_DEFINITONS</span></span>
* <span data-ttu-id="9b146-129">STATE_OBJECT_FLAGS_ALLOW_EXTERNAL_DEPENDENCIES_ON_LOCAL_DEFINITIONS</span><span class="sxs-lookup"><span data-stu-id="9b146-129">STATE_OBJECT_FLAGS_ALLOW_EXTERNAL_DEPENDENCIES_ON_LOCAL_DEFINITIONS</span></span>

<span data-ttu-id="9b146-130">oder 0 (null) für keines von beiden.</span><span class="sxs-lookup"><span data-stu-id="9b146-130">or, zero for neither of them.</span></span>

<span data-ttu-id="9b146-131">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="9b146-131">Example:</span></span>

```
StateObjectConfig MyStateObjectConfig = 
{ 
    STATE_OBJECT_FLAGS_ALLOW_LOCAL_DEPENDENCIES_ON_EXTERNAL_DEFINITONS
};
```

## <a name="globalrootsignature"></a><span data-ttu-id="9b146-132">Globalrootsignature</span><span class="sxs-lookup"><span data-stu-id="9b146-132">GlobalRootSignature</span></span>
<span data-ttu-id="9b146-133">Eine globalrootsignature entspricht einer [D3D12_GLOBAL_ROOT_SIGNATURE](/windows/win32/api/d3d12/ns-d3d12-d3d12_global_root_signature) Struktur.</span><span class="sxs-lookup"><span data-stu-id="9b146-133">A GlobalRootSignature corresponds to a [D3D12_GLOBAL_ROOT_SIGNATURE](/windows/win32/api/d3d12/ns-d3d12-d3d12_global_root_signature) structure.</span></span>

<span data-ttu-id="9b146-134">Die Felder bestehen aus einer Reihe von Zeichen folgen, die die Teile der Stamm Signatur beschreiben.</span><span class="sxs-lookup"><span data-stu-id="9b146-134">The fields consist of some number of strings describing the parts of the root signature.</span></span> <span data-ttu-id="9b146-135">Weitere Informationen hierzu finden Sie unter [Angeben von Stamm Signaturen in HLSL](../direct3d12/specifying-root-signatures-in-hlsl.md).</span><span class="sxs-lookup"><span data-stu-id="9b146-135">For reference on this, see [Specifying Root Signatures in HLSL](../direct3d12/specifying-root-signatures-in-hlsl.md).</span></span>

<span data-ttu-id="9b146-136">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="9b146-136">Example:</span></span>
```
GlobalRootSignature MyGlobalRootSignature =
{
    "DescriptorTable(UAV(u0)),"                     // Output texture
    "SRV(t0),"                                      // Acceleration structure
    "CBV(b0),"                                      // Scene constants
    "DescriptorTable(SRV(t1, numDescriptors = 2))"  // Static index and vertex buffers.
};
```

## <a name="localrootsignature"></a><span data-ttu-id="9b146-137">Localrootsignature</span><span class="sxs-lookup"><span data-stu-id="9b146-137">LocalRootSignature</span></span>
<span data-ttu-id="9b146-138">Eine localrootsignature entspricht einer [D3D12_LOCAL_ROOT_SIGNATURE](/windows/win32/api/d3d12/ns-d3d12-d3d12_local_root_signature) Struktur.</span><span class="sxs-lookup"><span data-stu-id="9b146-138">A LocalRootSignature corresponds to a [D3D12_LOCAL_ROOT_SIGNATURE](/windows/win32/api/d3d12/ns-d3d12-d3d12_local_root_signature) structure.</span></span>

<span data-ttu-id="9b146-139">Genau wie das untergeordnete Stamm Signatur Objekt bestehen die Felder aus einer Reihe von Zeichen folgen, die die Teile der Stamm Signatur beschreiben.</span><span class="sxs-lookup"><span data-stu-id="9b146-139">Just like the global root signature subobject, the fields consist of some number of strings describing the parts of the root signature.</span></span> <span data-ttu-id="9b146-140">Weitere Informationen hierzu finden Sie unter [Angeben von Stamm Signaturen in HLSL](../direct3d12/specifying-root-signatures-in-hlsl.md).</span><span class="sxs-lookup"><span data-stu-id="9b146-140">For reference on this, see [Specifying Root Signatures in HLSL](../direct3d12/specifying-root-signatures-in-hlsl.md).</span></span>

<span data-ttu-id="9b146-141">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="9b146-141">Example:</span></span>
```
LocalRootSignature MyLocalRootSignature = 
{
    "RootConstants(num32BitConstants = 4, b1)"  // Cube constants 
};
```

## <a name="subobjecttoexportsassocation"></a><span data-ttu-id="9b146-142">Subobjectjeexportsassokation</span><span class="sxs-lookup"><span data-stu-id="9b146-142">SubobjectToExportsAssocation</span></span>
<span data-ttu-id="9b146-143">Standardmäßig kann ein untergeordnetes Objekt, das nur in derselben Bibliothek wie ein Export deklariert ist, auf diesen Export angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="9b146-143">By default, a subobject merely declared in the same library as an export is able to apply to that export.</span></span> <span data-ttu-id="9b146-144">Anwendungen sind jedoch in der Lage, diese außer Kraft zu setzen und spezifische Informationen darüber zu erhalten, was das untergeordnete Objekt mit welchem Export ist.</span><span class="sxs-lookup"><span data-stu-id="9b146-144">However, applications have the ability to override that and get specific about what subobject goes with which export.</span></span> <span data-ttu-id="9b146-145">In HLSL wird diese "explizite Zuordnung" mithilfe von "SubObject-exportsassocation" durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="9b146-145">In HLSL, this "explicit association" is done using SubobjectToExportsAssocation.</span></span>

<span data-ttu-id="9b146-146">Ein subobjecttexportsassoationentspricht einer [D3D12_DXIL_SUBOBJECT_TO_EXPORTS_ASSOCIATION ](/windows/win32/api/d3d12/ns-d3d12-d3d12_dxil_subobject_to_exports_association) Struktur.</span><span class="sxs-lookup"><span data-stu-id="9b146-146">A SubobjectToExportsAssocation corresponds to a [D3D12_DXIL_SUBOBJECT_TO_EXPORTS_ASSOCIATION ](/windows/win32/api/d3d12/ns-d3d12-d3d12_dxil_subobject_to_exports_association) structure.</span></span>

<span data-ttu-id="9b146-147">Dieses untergeordnete Objekt wird mit der Syntax deklariert.</span><span class="sxs-lookup"><span data-stu-id="9b146-147">This subobject is declared with the syntax</span></span>

``` syntax
SubobjectToExportsAssocation Name = 
{ 
    SubobjectName,
    Exports
};
```

| <span data-ttu-id="9b146-148">Element</span><span class="sxs-lookup"><span data-stu-id="9b146-148">Item</span></span>                                                                                         | <span data-ttu-id="9b146-149">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9b146-149">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9b146-150"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Benennen**</span><span class="sxs-lookup"><span data-stu-id="9b146-150"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**</span></span><br/>     | <span data-ttu-id="9b146-151">Eine ASCII-Zeichenfolge, die den Variablennamen eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="9b146-151">An ASCII string that uniquely identifies the variable name.</span></span><br/>                 |
| <span data-ttu-id="9b146-152"><span id="SubobjectName"></span><span id="subobjectname"></span><span id="SUBOBJECTNAME"></span>**Subobjectname**</span><span class="sxs-lookup"><span data-stu-id="9b146-152"><span id="SubobjectName"></span><span id="subobjectname"></span><span id="SUBOBJECTNAME"></span>**SubobjectName**</span></span><br/>     | <span data-ttu-id="9b146-153">Eine Zeichenfolge, die ein exportiertes unter Objekt identifiziert.</span><span class="sxs-lookup"><span data-stu-id="9b146-153">String which identifies an exported subobject.</span></span><br/> |
| <span data-ttu-id="9b146-154"><span id="Exports"></span><span id="exports"></span><span id="EXPORTS"></span>**Ö**</span><span class="sxs-lookup"><span data-stu-id="9b146-154"><span id="Exports"></span><span id="exports"></span><span id="EXPORTS"></span>**Exports**</span></span><br/> | <span data-ttu-id="9b146-155">Eine Zeichenfolge, die eine durch Semikolons getrennte Liste der Exporte enthält.</span><span class="sxs-lookup"><span data-stu-id="9b146-155">String containing a semicolon-delimited list of exports.</span></span><br/> |


<span data-ttu-id="9b146-156">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="9b146-156">Example:</span></span>
```
SubobjectToExportsAssociation MyLocalRootSignatureAssociation =
{
    "MyLocalRootSignature",    // Subobject name
    "MyHitGroup;MyMissShader"  // Exports association 
};
```

<span data-ttu-id="9b146-157">Beachten Sie, dass beide Felder *exportierte* Namen verwenden.</span><span class="sxs-lookup"><span data-stu-id="9b146-157">Note that both fields use *exported* names.</span></span> <span data-ttu-id="9b146-158">Ein exportierter Name unterscheidet sich möglicherweise vom ursprünglichen Namen in HLSL, wenn die Anwendung die Export Umbenennung auswählt.</span><span class="sxs-lookup"><span data-stu-id="9b146-158">An exported name may be different from the original name in HLSL, if the application chooses to do export-renaming.</span></span>

## <a name="raytracingshaderconfig"></a><span data-ttu-id="9b146-159">Raytracingshaderconfig</span><span class="sxs-lookup"><span data-stu-id="9b146-159">RaytracingShaderConfig</span></span>

<span data-ttu-id="9b146-160">Ein raytracingshaderconfig entspricht einer [D3D12_RAYTRACING_SHADER_CONFIG](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_shader_config) Struktur.</span><span class="sxs-lookup"><span data-stu-id="9b146-160">A RaytracingShaderConfig corresponds to a [D3D12_RAYTRACING_SHADER_CONFIG](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_shader_config) structure.</span></span>

<span data-ttu-id="9b146-161">Dieses untergeordnete Objekt wird mit der Syntax deklariert.</span><span class="sxs-lookup"><span data-stu-id="9b146-161">This subobject is declared with the syntax</span></span>

``` syntax
RaytracingShaderConfig Name = 
{ 
    MaxPayloadSize,
    MaxAttributeSize
};
```

| <span data-ttu-id="9b146-162">Element</span><span class="sxs-lookup"><span data-stu-id="9b146-162">Item</span></span>                                                                                         | <span data-ttu-id="9b146-163">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9b146-163">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9b146-164"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Benennen**</span><span class="sxs-lookup"><span data-stu-id="9b146-164"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**</span></span><br/>     | <span data-ttu-id="9b146-165">Eine ASCII-Zeichenfolge, die den Variablennamen eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="9b146-165">An ASCII string that uniquely identifies the variable name.</span></span><br/>                 |
| <span data-ttu-id="9b146-166"><span id="MaxPayloadSize"></span><span id="maxpayloadsize"></span><span id="MAXPAYLOADSIZE"></span>**Maxpayloadsize**</span><span class="sxs-lookup"><span data-stu-id="9b146-166"><span id="MaxPayloadSize"></span><span id="maxpayloadsize"></span><span id="MAXPAYLOADSIZE"></span>**MaxPayloadSize**</span></span><br/>     | <span data-ttu-id="9b146-167">Numerischer Wert für den maximalen Speicherplatz für skalare (jeweils als 4 Bytes gezählt) in Ray-Nutzlasten für zugeordnete Raytracing-Shader.</span><span class="sxs-lookup"><span data-stu-id="9b146-167">Numerical value for the maximum storage for scalars (counted as 4 bytes each) in ray payloads for associated raytracing shaders.</span></span><br/> |
| <span data-ttu-id="9b146-168"><span id="MaxAttributeSize"></span><span id="maxattributesize"></span><span id="MAXATTRIBUTESIZE"></span>**Maxattributesize**</span><span class="sxs-lookup"><span data-stu-id="9b146-168"><span id="MaxAttributeSize"></span><span id="maxattributesize"></span><span id="MAXATTRIBUTESIZE"></span>**MaxAttributeSize**</span></span><br/> | <span data-ttu-id="9b146-169">Numerischer Wert für die maximale Anzahl von skalaren (jeweils als 4 Bytes gezählt), die für Attribute in zugeordneten Raytracing-Shadern verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="9b146-169">Numerical value for the maximum number of scalars (counted as 4 bytes each) that can be used for attributes in associated raytracing shaders.</span></span> <span data-ttu-id="9b146-170">Der Wert darf [D3D12_RAYTRACING_MAX_ATTRIBUTE_SIZE_IN_BYTES](../direct3d12/constants.md)nicht überschreiten.</span><span class="sxs-lookup"><span data-stu-id="9b146-170">The value cannot exceed [D3D12_RAYTRACING_MAX_ATTRIBUTE_SIZE_IN_BYTES](../direct3d12/constants.md).</span></span><br/> |


<span data-ttu-id="9b146-171">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="9b146-171">Example:</span></span>
```
RaytracingShaderConfig MyShaderConfig =
{
    16,  // Max payload size
    8    // Max attribute size
};
```

## <a name="raytracingpipelineconfig"></a><span data-ttu-id="9b146-172">Raytracingpipelineconfig</span><span class="sxs-lookup"><span data-stu-id="9b146-172">RaytracingPipelineConfig</span></span>

<span data-ttu-id="9b146-173">Ein raytracingpipelineconfig entspricht einer [D3D12_RAYTRACING_PIPELINE_CONFIG](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_pipeline_config) Struktur.</span><span class="sxs-lookup"><span data-stu-id="9b146-173">A RaytracingPipelineConfig corresponds to a [D3D12_RAYTRACING_PIPELINE_CONFIG](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_pipeline_config) structure.</span></span>

<span data-ttu-id="9b146-174">Dieses untergeordnete Objekt wird mit der Syntax deklariert.</span><span class="sxs-lookup"><span data-stu-id="9b146-174">This subobject is declared with the syntax</span></span>

``` syntax
RaytracingPipelineConfig Name = 
{ 
    MaxTraceRecursionDepth
};
```

| <span data-ttu-id="9b146-175">Element</span><span class="sxs-lookup"><span data-stu-id="9b146-175">Item</span></span>                                                                                         | <span data-ttu-id="9b146-176">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9b146-176">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9b146-177"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Benennen**</span><span class="sxs-lookup"><span data-stu-id="9b146-177"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**</span></span><br/>     | <span data-ttu-id="9b146-178">Eine ASCII-Zeichenfolge, die den Variablennamen eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="9b146-178">An ASCII string that uniquely identifies the variable name.</span></span><br/>                 |
| <span data-ttu-id="9b146-179"><span id="MaxTraceRecursionDepth"></span><span id="maxtracerecursiondepth"></span><span id="MAXTRACERECURSIONDEPTH"></span>**Maxtracerecursiontiefe**</span><span class="sxs-lookup"><span data-stu-id="9b146-179"><span id="MaxTraceRecursionDepth"></span><span id="maxtracerecursiondepth"></span><span id="MAXTRACERECURSIONDEPTH"></span>**MaxTraceRecursionDepth**</span></span><br/>     | <span data-ttu-id="9b146-180">Numerischer Grenzwert für die Ray-Rekursion in der Raytracing-Pipeline.</span><span class="sxs-lookup"><span data-stu-id="9b146-180">Numerical limit to use for ray recursion in the raytracing pipeline.</span></span> <span data-ttu-id="9b146-181">Dabei handelt es sich um eine Zahl zwischen 0 und einschließlich 31.</span><span class="sxs-lookup"><span data-stu-id="9b146-181">It is a number between 0 and 31, inclusive.</span></span> <br/> |


<span data-ttu-id="9b146-182">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="9b146-182">Example:</span></span>
```
RaytracingPipelineConfig MyPipelineConfig =
{
    1  // Max trace recursion depth
};
```
<span data-ttu-id="9b146-183">Da für die Raytracing-Rekursion Leistungskosten anfallen, sollten Anwendungen die niedrigste Rekursions Tiefe verwenden, die für die gewünschten Ergebnisse erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="9b146-183">Since there is a performance cost to raytracing recursion, applications should use the lowest recursion depth needed for the desired results.</span></span>

<span data-ttu-id="9b146-184">Wenn Shader-Aufrufe die maximale Rekursions Tiefe noch nicht erreicht haben, können Sie [traceray](../direct3d12/traceray-function.md) beliebig oft aufrufen.</span><span class="sxs-lookup"><span data-stu-id="9b146-184">If shader invocations haven't yet reached the maximum recursion depth, they can call [TraceRay](../direct3d12/traceray-function.md) any number of times.</span></span> <span data-ttu-id="9b146-185">Wenn die maximale Rekursions Tiefe erreicht oder überschritten wird, versetzt der Aufruf von traceray das Gerät in den entfernten Zustand.</span><span class="sxs-lookup"><span data-stu-id="9b146-185">But if they reach or exceed the maximum recursion depth, calling TraceRay puts the device into removed state.</span></span> <span data-ttu-id="9b146-186">Daher sollten Raytracing-Shader darauf achten, den Aufruf von traceray zu unterbinden, wenn Sie die maximale Rekursions Tiefe erreicht oder überschritten haben.</span><span class="sxs-lookup"><span data-stu-id="9b146-186">Therefore, raytracing shaders should take care to stop calling TraceRay if they've met or exceeded the maximum recursion depth.</span></span>

## <a name="trianglehitgroup"></a><span data-ttu-id="9b146-187">"Testgruppe"</span><span class="sxs-lookup"><span data-stu-id="9b146-187">TriangleHitGroup</span></span>

<span data-ttu-id="9b146-188">Eine "zanglehitgroup" entspricht einer [D3D12_HIT_GROUP_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_hit_group_desc) -Struktur, deren Type-Feld auf " [D3D12_HIT_GROUP_TYPE_TRIANGLES](/windows/win32/api/d3d12/ne-d3d12-d3d12_hit_group_type#constants)" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="9b146-188">A TriangleHitGroup corresponds to a [D3D12_HIT_GROUP_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_hit_group_desc) structure whose Type field is set to [D3D12_HIT_GROUP_TYPE_TRIANGLES](/windows/win32/api/d3d12/ne-d3d12-d3d12_hit_group_type#constants).</span></span>

<span data-ttu-id="9b146-189">Dieses untergeordnete Objekt wird mit der Syntax deklariert.</span><span class="sxs-lookup"><span data-stu-id="9b146-189">This subobject is declared with the syntax</span></span>

``` syntax
TriangleHitGroup Name = 
{ 
    AnyHitShader,
    ClosestHitShader
};
```

| <span data-ttu-id="9b146-190">Element</span><span class="sxs-lookup"><span data-stu-id="9b146-190">Item</span></span>                                                                                         | <span data-ttu-id="9b146-191">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9b146-191">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9b146-192"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Benennen**</span><span class="sxs-lookup"><span data-stu-id="9b146-192"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**</span></span><br/>     | <span data-ttu-id="9b146-193">Eine ASCII-Zeichenfolge, die den Variablennamen eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="9b146-193">An ASCII string that uniquely identifies the variable name.</span></span><br/>                 |
| <span data-ttu-id="9b146-194"><span id="AnyHitShader"></span><span id="anyhitshader"></span><span id="ANYHITSHADER"></span>**Anyhitshader**</span><span class="sxs-lookup"><span data-stu-id="9b146-194"><span id="AnyHitShader"></span><span id="anyhitshader"></span><span id="ANYHITSHADER"></span>**AnyHitShader**</span></span><br/>     | <span data-ttu-id="9b146-195">Der Zeichen folgen Name des anyhit-Shaders für die Treffer Gruppe oder eine leere Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="9b146-195">String name of the anyhit shader for the hit group, or an empty string.</span></span><br/> |
| <span data-ttu-id="9b146-196"><span id="ClosestHitShader"></span><span id="closesthitshader"></span><span id="CLOSESTHITSHADER"></span>**Closesthitshader**</span><span class="sxs-lookup"><span data-stu-id="9b146-196"><span id="ClosestHitShader"></span><span id="closesthitshader"></span><span id="CLOSESTHITSHADER"></span>**ClosestHitShader**</span></span><br/> | <span data-ttu-id="9b146-197">Der Zeichen folgen Name des nächstgelegenen Treffer-Shaders für die Treffer Gruppe oder eine leere Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="9b146-197">String name of the closest hit shader for the hit group, or an empty string.</span></span><br/> |


<span data-ttu-id="9b146-198">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="9b146-198">Example:</span></span>
```
TriangleHitGroup MyHitGroup =
{
    "",                    // AnyHit
    "MyClosestHitShader",  // ClosestHit
};
```

<span data-ttu-id="9b146-199">Beachten Sie, dass beide Felder *exportierte* Namen verwenden.</span><span class="sxs-lookup"><span data-stu-id="9b146-199">Note that both fields use *exported* names.</span></span> <span data-ttu-id="9b146-200">Ein exportierter Name unterscheidet sich möglicherweise vom ursprünglichen Namen in HLSL, wenn die Anwendung die Export Umbenennung auswählt.</span><span class="sxs-lookup"><span data-stu-id="9b146-200">An exported name may be different from the original name in HLSL, if the application chooses to do export-renaming.</span></span>

## <a name="proceduralprimitivehitgroup"></a><span data-ttu-id="9b146-201">Prozelinialprimitivehitgroup</span><span class="sxs-lookup"><span data-stu-id="9b146-201">ProceduralPrimitiveHitGroup</span></span>

<span data-ttu-id="9b146-202">Eine "prozebegruppe" ist eine [D3D12_HIT_GROUP_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_hit_group_desc) Struktur, deren Type-Feld auf " [D3D12_HIT_GROUP_TYPE_PROCEDURAL_PRIMITIVE](/windows/win32/api/d3d12/ne-d3d12-d3d12_hit_group_type#constants)" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="9b146-202">A ProceduralPrimitiveHitGroup corresponds to a [D3D12_HIT_GROUP_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_hit_group_desc) structure whose Type field is set to [D3D12_HIT_GROUP_TYPE_PROCEDURAL_PRIMITIVE](/windows/win32/api/d3d12/ne-d3d12-d3d12_hit_group_type#constants).</span></span>

<span data-ttu-id="9b146-203">Dieses untergeordnete Objekt wird mit der Syntax deklariert.</span><span class="sxs-lookup"><span data-stu-id="9b146-203">This subobject is declared with the syntax</span></span>

``` syntax
ProceduralPrimitiveHitGroup Name = 
{ 
    AnyHitShader,
    ClosestHitShader,
    IntersectionShader
};
```

| <span data-ttu-id="9b146-204">Element</span><span class="sxs-lookup"><span data-stu-id="9b146-204">Item</span></span>                                                                                         | <span data-ttu-id="9b146-205">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9b146-205">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9b146-206"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Benennen**</span><span class="sxs-lookup"><span data-stu-id="9b146-206"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**</span></span><br/>     | <span data-ttu-id="9b146-207">Eine ASCII-Zeichenfolge, die den Variablennamen eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="9b146-207">An ASCII string that uniquely identifies the variable name.</span></span><br/>                 |
| <span data-ttu-id="9b146-208"><span id="AnyHitShader"></span><span id="anyhitshader"></span><span id="ANYHITSHADER"></span>**Anyhitshader**</span><span class="sxs-lookup"><span data-stu-id="9b146-208"><span id="AnyHitShader"></span><span id="anyhitshader"></span><span id="ANYHITSHADER"></span>**AnyHitShader**</span></span><br/>     | <span data-ttu-id="9b146-209">Der Zeichen folgen Name des anyhit-Shaders für die Treffer Gruppe oder eine leere Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="9b146-209">String name of the anyhit shader for the hit group, or an empty string.</span></span><br/> |
| <span data-ttu-id="9b146-210"><span id="ClosestHitShader"></span><span id="closesthitshader"></span><span id="CLOSESTHITSHADER"></span>**Closesthitshader**</span><span class="sxs-lookup"><span data-stu-id="9b146-210"><span id="ClosestHitShader"></span><span id="closesthitshader"></span><span id="CLOSESTHITSHADER"></span>**ClosestHitShader**</span></span><br/> | <span data-ttu-id="9b146-211">Der Zeichen folgen Name des nächstgelegenen Treffer-Shaders für die Treffer Gruppe oder eine leere Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="9b146-211">String name of the closest hit shader for the hit group, or an empty string.</span></span><br/> |
| <span data-ttu-id="9b146-212"><span id="IntersectionShader"></span><span id="intersectionshader"></span><span id="INTERSECTIONSHADER"></span>**Intersectionshader**</span><span class="sxs-lookup"><span data-stu-id="9b146-212"><span id="IntersectionShader"></span><span id="intersectionshader"></span><span id="INTERSECTIONSHADER"></span>**IntersectionShader**</span></span><br/> | <span data-ttu-id="9b146-213">Der Zeichen folgen Name des Schnittstellen Shaders für die Treffer Gruppe oder eine leere Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="9b146-213">String name of the intersection shader for the hit group, or an empty string.</span></span><br/> |


<span data-ttu-id="9b146-214">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="9b146-214">Example:</span></span>
```
ProceduralPrimitiveHitGroup MyProceduralHitGroup
{
    "MyAnyHit",       // AnyHit
    "MyClosestHit",   // ClosestHit
    "MyIntersection"  // Intersection
};

```

<span data-ttu-id="9b146-215">Beachten Sie, dass in den drei Feldern *exportierte* Namen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9b146-215">Note that the three fields use *exported* names.</span></span> <span data-ttu-id="9b146-216">Ein exportierter Name unterscheidet sich möglicherweise vom ursprünglichen Namen in HLSL, wenn die Anwendung die Export Umbenennung auswählt.</span><span class="sxs-lookup"><span data-stu-id="9b146-216">An exported name may be different from the original name in HLSL, if the application chooses to do export-renaming.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b146-217">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9b146-217">Remarks</span></span>

<span data-ttu-id="9b146-218">Untergeordnete Objekte haben das Konzept "Association" oder "welches unter Objekt mit welchem Export".</span><span class="sxs-lookup"><span data-stu-id="9b146-218">Subobjects have the notion of "association", or "which subobject goes with which export".</span></span>

<span data-ttu-id="9b146-219">Beim Angeben von untergeordneten Elementen über den Shader-Code befolgt die Auswahl des untergeordneten Objekts, mit dem der Export erfolgt, den Regeln entsprechend den [Angaben in der DXR-Spezifikation](https://microsoft.github.io/DirectX-Specs/d3d/Raytracing.html#subobject-association-behavior).</span><span class="sxs-lookup"><span data-stu-id="9b146-219">When specifying subobjects through shader code, the choice of "which subobject goes with which export" follows the rules as outlined in the [DXR specification](https://microsoft.github.io/DirectX-Specs/d3d/Raytracing.html#subobject-association-behavior).</span></span> <span data-ttu-id="9b146-220">Stellen Sie sich vor, dass eine Anwendung über einen Export verfügt.</span><span class="sxs-lookup"><span data-stu-id="9b146-220">In particular, suppose an application has some export.</span></span> <span data-ttu-id="9b146-221">Wenn eine Anwendung den Export mit der Stamm Signatur a über Shader-Code und Stamm Signatur B über den Anwendungscode zuordnet, ist B der Wert, der verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9b146-221">If an application associates that export with root signature A through shader-code and root signature B through application code, B is the one that gets used.</span></span> <span data-ttu-id="9b146-222">Der Entwurf von "Use B" anstelle von "Fehler verursachen" gibt Anwendungen die Möglichkeit, dxil-Zuordnungen mithilfe von Anwendungscode bequem zu überschreiben, anstatt Shader erneut zu kompilieren, um nicht übereinstimmende Elemente aufzulösen.</span><span class="sxs-lookup"><span data-stu-id="9b146-222">The design of "use B" instead of "produce an error" gives applications the ability to conveniently override DXIL associations using application code, rather than be forced to recompile shaders to resolve mismatching things.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9b146-223">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9b146-223">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b146-224">DirectX-Entwickler-Blog Beitrag "New in D3D12 – DirectX Raytracing (DXR) unterstützt jetzt Bibliotheks-unter Objekte"</span><span class="sxs-lookup"><span data-stu-id="9b146-224">DirectX Developer Blog post "New in D3D12 – DirectX Raytracing (DXR) now supports library subobjects"</span></span>](https://devblogs.microsoft.com/directx/dxr-library-subobjects/)

[<span data-ttu-id="9b146-225">Funktionsspezifikation für DirectX-Raytracing (DXR)</span><span class="sxs-lookup"><span data-stu-id="9b146-225">DirectX Raytracing (DXR) Functional Spec</span></span>](https://microsoft.github.io/DirectX-Specs/d3d/Raytracing.html)

[<span data-ttu-id="9b146-226">Beispiel: D3D12RaytracingLibrarySubobjects</span><span class="sxs-lookup"><span data-stu-id="9b146-226">Sample: D3D12RaytracingLibrarySubobjects</span></span>](https://github.com/Microsoft/DirectX-Graphics-Samples/tree/develop/Samples/Desktop/D3D12Raytracing/src/D3D12RaytracingLibrarySubobjects)

</dt> </dl>