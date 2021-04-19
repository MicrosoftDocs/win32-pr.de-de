---
title: CD3DX12_PIPELINE_STATE_STREAM1-Struktur (D3dx12. h)
description: Eine hilfsstruktur zum Erstellen und arbeiten mit Grafiken und Compute-Pipeline Zuständen über eine kombinierte Schnittstelle. Weitere Informationen finden Sie unter D3D12 \_ Graphics \_ Pipeline \_ State \_ DESC and D3D12 \_ Compute \_ Pipeline \_ State \_ DESC. | CD3DX12_PIPELINE_STATE_STREAM1-Struktur (D3dx12. h)
ms.assetid: 4D3E4D99-E820-4220-92F3-4924791E780F
keywords:
- CD3DX12_PIPELINE_STATE_STREAM1 Struktur
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdd04f58f4f123850c60b67ff9358f6f1f934373
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361182"
---
# <a name="cd3dx12_pipeline_state_stream1-structure"></a><span data-ttu-id="b2b37-106">CD3DX12 \_ Pipeline \_ State \_ STREAM1-Struktur</span><span class="sxs-lookup"><span data-stu-id="b2b37-106">CD3DX12\_PIPELINE\_STATE\_STREAM1 structure</span></span>

<span data-ttu-id="b2b37-107">Eine hilfsstruktur zum Erstellen und arbeiten mit Grafiken und Compute-Pipeline Zuständen über eine kombinierte Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="b2b37-107">A helper structure for creating and working with graphics and compute pipeline states through a combined interface.</span></span> <span data-ttu-id="b2b37-108">Weitere Informationen finden Sie unter [**D3D12 \_ Graphics \_ Pipeline \_ State \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) and [**D3D12 \_ Compute \_ Pipeline \_ State \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc).</span><span class="sxs-lookup"><span data-stu-id="b2b37-108">See [**D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) and [**D3D12\_COMPUTE\_PIPELINE\_STATE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc).</span></span>

<span data-ttu-id="b2b37-109">CD3DX12 \_ Pipeline \_ State \_ STREAM1 unterstützt das Windows 10 Fall Creators Update mit neuen Funktionen, wie z. b. Ansichts Instanziierung.</span><span class="sxs-lookup"><span data-stu-id="b2b37-109">CD3DX12\_PIPELINE\_STATE\_STREAM1 supports the Windows 10 Fall Creators Update with new features such as view instancing.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2b37-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="b2b37-110">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM1 {
  CD3DX12_PIPELINE_STATE_STREAM1                      CD3DX12_PIPELINE_STATE_STREAM1();
  CD3DX12_PIPELINE_STATE_STREAM1                      CD3DX12_PIPELINE_STATE_STREAM1(const D3D12_GRAPHICS_PIPELINE_STATE_DESC& Desc);
  CD3DX12_PIPELINE_STATE_STREAM1                      CD3DX12_PIPELINE_STATE_STREAM1(const D3D12_COMPUTE_PIPELINE_STATE_DESC& Desc);
  D3D12_GRAPHICS_PIPELINE_STATE_DESC                  GraphicsDescV0();
  D3D12_COMPUTE_PIPELINE_STATE_DESC                   ComputeDescV0();
  CD3DX12_PIPELINE_STATE_STREAM_FLAGS                 Flags;
  CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK             NodeMask;
  CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE        pRootSignature;
  CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT          InputLayout;
  CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE    IBStripCutValue;
  CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY    PrimitiveTopologyType;
  CD3DX12_PIPELINE_STATE_STREAM_VS                    VS;
  CD3DX12_PIPELINE_STATE_STREAM_GS                    GS;
  CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT         StreamOutput;
  CD3DX12_PIPELINE_STATE_STREAM_HS                    HS;
  CD3DX12_PIPELINE_STATE_STREAM_DS                    DS;
  CD3DX12_PIPELINE_STATE_STREAM_PS                    PS;
  CD3DX12_PIPELINE_STATE_STREAM_CS                    CS;
  CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC            BlendState;
  CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1        DepthStencilState;
  CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT  DSVFormat;
  CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER            RasterizerState;
  CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS RTVFormats;
  CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC           SampleDesc;
  CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK           SampleMask;
  CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO            CachedPSO;
};
```



## <a name="members"></a><span data-ttu-id="b2b37-111">Member</span><span class="sxs-lookup"><span data-stu-id="b2b37-111">Members</span></span>

<dl> <dt>

<span data-ttu-id="b2b37-112">**CD3DX12 \_ Pipeline \_ State \_ STREAM1 ()**</span><span class="sxs-lookup"><span data-stu-id="b2b37-112">**CD3DX12\_PIPELINE\_STATE\_STREAM1()**</span></span>
</dt> <dd>

<span data-ttu-id="b2b37-113">Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12- \_ Pipeline \_ Zustands \_ STREAM1.</span><span class="sxs-lookup"><span data-stu-id="b2b37-113">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM1.</span></span>

</dd> <dt>

<span data-ttu-id="b2b37-114">**CD3DX12 \_ Pipeline \_ State \_ STREAM1 (konstant D3D12 \_ Grafik \_ Pipeline \_ State \_ DESC& DESC)**</span><span class="sxs-lookup"><span data-stu-id="b2b37-114">**CD3DX12\_PIPELINE\_STATE\_STREAM1(const D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC& Desc)**</span></span>
</dt> <dd>

<span data-ttu-id="b2b37-115">Erstellt eine neue Instanz eines CD3DX12- \_ Pipeline \_ Zustands \_ STREAM1, die mit Werten initialisiert wird, die aus einer **CD3DX12 \_ Pipeline \_ State \_ STREAM1** -Struktur kopiert wurden.</span><span class="sxs-lookup"><span data-stu-id="b2b37-115">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM1, initialized with values copied from a **CD3DX12\_PIPELINE\_STATE\_STREAM1** structure.</span></span>

</dd> <dt>

<span data-ttu-id="b2b37-116">**CD3DX12 \_ Pipeline \_ State \_ STREAM1 (konstant D3D12 \_ Compute \_ Pipeline \_ State Debug \_& de)**</span><span class="sxs-lookup"><span data-stu-id="b2b37-116">**CD3DX12\_PIPELINE\_STATE\_STREAM1(const D3D12\_COMPUTE\_PIPELINE\_STATE\_DESC& Desc)**</span></span>
</dt> <dd>

<span data-ttu-id="b2b37-117">Erstellt eine neue Instanz eines CD3DX12- \_ Pipeline \_ Zustands \_ STREAM1, die mit Werten initialisiert wird, die aus einer **CD3DX12 \_ Pipeline \_ State \_ STREAM1** -Struktur kopiert wurden.</span><span class="sxs-lookup"><span data-stu-id="b2b37-117">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM1, initialized with values copied from a **CD3DX12\_PIPELINE\_STATE\_STREAM1** structure.</span></span>

</dd> <dt>

<span data-ttu-id="b2b37-118">**GraphicsDescV0()**</span><span class="sxs-lookup"><span data-stu-id="b2b37-118">**GraphicsDescV0()**</span></span>
</dt> <dd>

<span data-ttu-id="b2b37-119">Gibt den Inhalt des CD3DX12 \_ Pipeline \_ State STREAM1- \_ Objekts als D3D12- \_ Grafik \_ Pipeline \_ State- \_ DESC-Struktur nach Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="b2b37-119">returns the contents of the CD3DX12\_PIPELINE\_STATE\_STREAM1 object as a D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC structure by value.</span></span> <span data-ttu-id="b2b37-120">Beachten Sie, \_ dass \_ der D3D12 graphics Pipeline \_ State \_ DESC den **CS** -Member nicht enthält, sodass dieser Wert bei der Konvertierung verloren geht.</span><span class="sxs-lookup"><span data-stu-id="b2b37-120">Note that D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC does not include the **CS** member, so this value is lost in the conversion.</span></span>

</dd> <dt>

<span data-ttu-id="b2b37-121">**ComputeDescV0()**</span><span class="sxs-lookup"><span data-stu-id="b2b37-121">**ComputeDescV0()**</span></span>
</dt> <dd>

<span data-ttu-id="b2b37-122">Gibt den Inhalt des CD3DX12 \_ Pipeline \_ State STREAM1- \_ Objekts als D3D12 \_ Compute \_ Pipeline State- \_ \_ Struktur nach Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="b2b37-122">returns the contents of the CD3DX12\_PIPELINE\_STATE\_STREAM1 object as a D3D12\_COMPUTE\_PIPELINE\_STATE\_DESC structure by value.</span></span> <span data-ttu-id="b2b37-123">Beachten Sie, \_ dass der D3D12 Compute \_ Pipeline \_ State \_ **UNSC nicht das Input Layout** enthält. **ibstrip Page Value**, **primitivetopologytype**, **vs**, **GS**, **streamoutput**, **HS**, **DS**, **PS**, **blendstate**, **depthschablone cilstate**, **dsvformat**, **rasterizerstate**, **numrootsignature**, **r tvformats**, **SampleDesc** oder **samplemask** -Member, sodass diese Werte bei der Konvertierung verloren gehen.</span><span class="sxs-lookup"><span data-stu-id="b2b37-123">Note that D3D12\_COMPUTE\_PIPELINE\_STATE\_DESC does not include the **InputLayout**, **IBStripCutValue**, **PrimitiveTopologyType**, **VS**, **GS**, **StreamOutput**, **HS**, **DS**, **PS**, **BlendState**, **DepthStencilState**, **DSVFormat**, **RasterizerState**, **NumRootSignature**, **RTVFormats**, **SampleDesc**, or **SampleMask** members, so these values are lost in the conversion.</span></span>

</dd> <dt>

<span data-ttu-id="b2b37-124">**Flags**</span><span class="sxs-lookup"><span data-stu-id="b2b37-124">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="b2b37-125">Beschreibt die Pipeline-Statusflags, die Funktionen wie "Tool Debuggen" steuern.</span><span class="sxs-lookup"><span data-stu-id="b2b37-125">Describes the pipeline state flags, which control features such as "tool debug".</span></span>

</dd> <dt>

<span data-ttu-id="b2b37-126">**Nodemask**</span><span class="sxs-lookup"><span data-stu-id="b2b37-126">**NodeMask**</span></span>
</dt> <dd>

<span data-ttu-id="b2b37-127">Beschreibt die Pipeline Status-Knoten Maske, die verwendet wird, um die Knoten (physischen Adapter des Geräts) zu identifizieren, für die das PSO in Szenarien mit mehreren Adaptern gilt. jedes Bit in der Maske entspricht einem einzelnen Knoten.</span><span class="sxs-lookup"><span data-stu-id="b2b37-127">Describes the pipeline state node mask, which is used to identify the nodes (physical adapters of the device) that the PSO applies to in Multi-Adapter scenarios; each bit in the mask corresponds to a single node.</span></span> <span data-ttu-id="b2b37-128">Legen Sie für Szenarien mit einem einzelnen Adapter diesen Wert auf 0 fest.</span><span class="sxs-lookup"><span data-stu-id="b2b37-128">For single-adapter scenarios, set this value to 0.</span></span>

</dd> <dt>

<span data-ttu-id="b2b37-129">**prootsignature**</span><span class="sxs-lookup"><span data-stu-id="b2b37-129">**pRootSignature**</span></span>
</dt> <dd>

<span data-ttu-id="b2b37-130">Beschreibt die Stamm Signatur.</span><span class="sxs-lookup"><span data-stu-id="b2b37-130">Describes the root signature.</span></span>

</dd> <dt>

<span data-ttu-id="b2b37-131">**Input Layout**</span><span class="sxs-lookup"><span data-stu-id="b2b37-131">**InputLayout**</span></span>
</dt> <dd>

<span data-ttu-id="b2b37-132">Beschreibt das Eingabepuffer Format für die Eingabe-Assembler-Stufe.</span><span class="sxs-lookup"><span data-stu-id="b2b37-132">Describes the input-buffer format for the input-assembler stage</span></span>

</dd> <dt>

<span data-ttu-id="b2b37-133">**Ibstripcutvalue**</span><span class="sxs-lookup"><span data-stu-id="b2b37-133">**IBStripCutValue**</span></span>
</dt> <dd>

<span data-ttu-id="b2b37-134">Beschreibt den speziellen Indexwert des Eingabe Puffers, der bei Verwendung der Dreieck-Strip-Topologie einen Ausschneide Wert (Diskontinuität) angibt.</span><span class="sxs-lookup"><span data-stu-id="b2b37-134">Describes the special index value of the input buffer that indicates a cut (discontinuity) when using triangle-strip topology.</span></span>

</dd> <dt>

<span data-ttu-id="b2b37-135">**Primitivetopologytype**</span><span class="sxs-lookup"><span data-stu-id="b2b37-135">**PrimitiveTopologyType**</span></span>
</dt> <dd>

<span data-ttu-id="b2b37-136">Beschreibt die primitive Topologie und deren Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="b2b37-136">Describes the primitive topology and its order.</span></span>

</dd> <dt>

<span data-ttu-id="b2b37-137">**Jews**</span><span class="sxs-lookup"><span data-stu-id="b2b37-137">**VS**</span></span>
</dt> <dd>

<span data-ttu-id="b2b37-138">Beschreibt den Scheitelpunkt-Shader.</span><span class="sxs-lookup"><span data-stu-id="b2b37-138">Describes the vertex shader.</span></span>

</dd> <dt>

<span data-ttu-id="b2b37-139">**GS**</span><span class="sxs-lookup"><span data-stu-id="b2b37-139">**GS**</span></span>
</dt> <dd>

<span data-ttu-id="b2b37-140">Beschreibt den Geometry-Shader.</span><span class="sxs-lookup"><span data-stu-id="b2b37-140">Describes the geometry shader.</span></span>

</dd> <dt>

<span data-ttu-id="b2b37-141">**Streamoutput**</span><span class="sxs-lookup"><span data-stu-id="b2b37-141">**StreamOutput**</span></span>
</dt> <dd>

<span data-ttu-id="b2b37-142">Beschreibt den Ausgabepuffer für das Streaming.</span><span class="sxs-lookup"><span data-stu-id="b2b37-142">Describes the streaming output-buffer.</span></span>

</dd> <dt>

<span data-ttu-id="b2b37-143">**Jh**</span><span class="sxs-lookup"><span data-stu-id="b2b37-143">**HS**</span></span>
</dt> <dd>

<span data-ttu-id="b2b37-144">Beschreibt den Rumpf-Shader.</span><span class="sxs-lookup"><span data-stu-id="b2b37-144">Describes the hull shader.</span></span>

</dd> <dt>

<span data-ttu-id="b2b37-145">**DS**</span><span class="sxs-lookup"><span data-stu-id="b2b37-145">**DS**</span></span>
</dt> <dd>

<span data-ttu-id="b2b37-146">Beschreibt den Domänen-Shader.</span><span class="sxs-lookup"><span data-stu-id="b2b37-146">Describes the domain shader.</span></span>

</dd> <dt>

<span data-ttu-id="b2b37-147">**PS**</span><span class="sxs-lookup"><span data-stu-id="b2b37-147">**PS**</span></span>
</dt> <dd>

<span data-ttu-id="b2b37-148">Beschreibt den Pixelshader.</span><span class="sxs-lookup"><span data-stu-id="b2b37-148">Describes the pixel shader.</span></span>

</dd> <dt>

<span data-ttu-id="b2b37-149">**CS**</span><span class="sxs-lookup"><span data-stu-id="b2b37-149">**CS**</span></span>
</dt> <dd>

<span data-ttu-id="b2b37-150">Beschreibt den Compute-Shader.</span><span class="sxs-lookup"><span data-stu-id="b2b37-150">Describes the compute shader.</span></span>

</dd> <dt>

<span data-ttu-id="b2b37-151">**Blendstate**</span><span class="sxs-lookup"><span data-stu-id="b2b37-151">**BlendState**</span></span>
</dt> <dd>

<span data-ttu-id="b2b37-152">Beschreibt den Blend-Zustand.</span><span class="sxs-lookup"><span data-stu-id="b2b37-152">Describes the blend state.</span></span>

</dd> <dt>

<span data-ttu-id="b2b37-153">**Depthstencilstate**</span><span class="sxs-lookup"><span data-stu-id="b2b37-153">**DepthStencilState**</span></span>
</dt> <dd>

<span data-ttu-id="b2b37-154">Beschreibt den Status der tiefen Schablone.</span><span class="sxs-lookup"><span data-stu-id="b2b37-154">Describes the depth-stencil state.</span></span>

</dd> <dt>

<span data-ttu-id="b2b37-155">**Dsvformat**</span><span class="sxs-lookup"><span data-stu-id="b2b37-155">**DSVFormat**</span></span>
</dt> <dd>

<span data-ttu-id="b2b37-156">Beschreibt das Format der tiefen Schablone.</span><span class="sxs-lookup"><span data-stu-id="b2b37-156">Describes the depth-stencil format.</span></span>

</dd> <dt>

<span data-ttu-id="b2b37-157">**Rasterizerstate**</span><span class="sxs-lookup"><span data-stu-id="b2b37-157">**RasterizerState**</span></span>
</dt> <dd>

<span data-ttu-id="b2b37-158">Beschreibt den Status des Rasterizers.</span><span class="sxs-lookup"><span data-stu-id="b2b37-158">Describes the rasterizer state.</span></span>

</dd> <dt>

<span data-ttu-id="b2b37-159">**RTV-Formate**</span><span class="sxs-lookup"><span data-stu-id="b2b37-159">**RTVFormats**</span></span>
</dt> <dd>

<span data-ttu-id="b2b37-160">Beschreibt die renderzielformate.</span><span class="sxs-lookup"><span data-stu-id="b2b37-160">Describes the render target formats.</span></span>

</dd> <dt>

<span data-ttu-id="b2b37-161">**Sampledäsc**</span><span class="sxs-lookup"><span data-stu-id="b2b37-161">**SampleDesc**</span></span>
</dt> <dd>

<span data-ttu-id="b2b37-162">Beschreibt die Stichproben Anzahl und-Qualität.</span><span class="sxs-lookup"><span data-stu-id="b2b37-162">Describes the sample count and quality.</span></span>

</dd> <dt>

<span data-ttu-id="b2b37-163">**Samplemask**</span><span class="sxs-lookup"><span data-stu-id="b2b37-163">**SampleMask**</span></span>
</dt> <dd>

<span data-ttu-id="b2b37-164">Beschreibt die Beispiel Maske, die mit dem Blend-Status verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b2b37-164">Describes the sample mask used with the blend state.</span></span>

</dd> <dt>

<span data-ttu-id="b2b37-165">**Cachedpso**</span><span class="sxs-lookup"><span data-stu-id="b2b37-165">**CachedPSO**</span></span>
</dt> <dd>

<span data-ttu-id="b2b37-166">Beschreibt ein zwischengespeichertes PSO.</span><span class="sxs-lookup"><span data-stu-id="b2b37-166">Describes a cached PSO.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b2b37-167">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b2b37-167">Remarks</span></span>

<span data-ttu-id="b2b37-168">[**CD3DX12 \_ Der Pipeline \_ Status- \_ Stream**](https://www.bing.com/search?q=**CD3DX12\_PIPELINE\_STATE\_STREAM**) unterstützt das Windows 10 Fall Creators Update, unterstützt jedoch keine untergeordneten Typen, die in Windows 10 Fall Creators Update hinzugefügt wurden, z. b. für die Ansichts Instanzierung.</span><span class="sxs-lookup"><span data-stu-id="b2b37-168">[**CD3DX12\_PIPELINE\_STATE\_STREAM**](https://www.bing.com/search?q=**CD3DX12\_PIPELINE\_STATE\_STREAM**) supports the Windows 10 Fall Creators Update, but doesn't support subobject types added in Windows 10 Fall Creators update, such as for view instancing.</span></span> <span data-ttu-id="b2b37-169">Verwenden Sie \_ stattdessen CD3DX12 Pipeline \_ State STREAM1, um die neuen untergeordneten Typen zu unterstützen \_ .</span><span class="sxs-lookup"><span data-stu-id="b2b37-169">To support the new subobject types, use CD3DX12\_PIPELINE\_STATE\_STREAM1 instead.</span></span>

<span data-ttu-id="b2b37-170">Die barrierefreien Element Variablen dieser Struktur sind alle Typedefs der CD3DX12 \_ Pipeline State Stream-Unterordner \_ \_ \_ Vorlage, die die untergeordneten typmarker-und untergeordneten Daten in ein einzelnes Objekt kombiniert, das für eine Datenstrom Beschreibung geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="b2b37-170">The accessible member variables of this structure are all typedefs of the CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT template, which combines the subobject type-marker and subobject data into a single object suitable for a stream description.</span></span>

<span data-ttu-id="b2b37-171">Diese Typedefs lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="b2b37-171">Those typedefs are:</span></span>

<span data-ttu-id="b2b37-172"><dl> </dl></span><span class="sxs-lookup"><span data-stu-id="b2b37-172"><dl> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="b2b37-173">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b2b37-173">Requirements</span></span>



| <span data-ttu-id="b2b37-174">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b2b37-174">Requirement</span></span> | <span data-ttu-id="b2b37-175">Wert</span><span class="sxs-lookup"><span data-stu-id="b2b37-175">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b2b37-176">Header</span><span class="sxs-lookup"><span data-stu-id="b2b37-176">Header</span></span><br/> | <dl> <span data-ttu-id="b2b37-177"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2b37-177"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2b37-178">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b2b37-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2b37-179">Strukturen des Hilfsprogramms für D3D12</span><span class="sxs-lookup"><span data-stu-id="b2b37-179">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="b2b37-180">**CD3DX12 \_ Pipeline \_ State- \_ Stream**</span><span class="sxs-lookup"><span data-stu-id="b2b37-180">**CD3DX12\_PIPELINE\_STATE\_STREAM**</span></span>](cd3dx12-pipeline-state-stream.md)
</dt> <dt>

[<span data-ttu-id="b2b37-181">**D3D12- \_ Grafik \_ Pipeline \_ Status \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="b2b37-181">**D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc)
</dt> <dt>

[<span data-ttu-id="b2b37-182">**D3D12 \_ Compute \_ Pipeline \_ State \_ Debug**</span><span class="sxs-lookup"><span data-stu-id="b2b37-182">**D3D12\_COMPUTE\_PIPELINE\_STATE\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc)
</dt> </dl>

 

 





