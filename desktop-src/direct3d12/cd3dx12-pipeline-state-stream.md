---
title: CD3DX12_PIPELINE_STATE_STREAM-Struktur (D3dx12. h)
description: Eine hilfsstruktur zum Erstellen und arbeiten mit Grafiken und Compute-Pipeline Zuständen über eine kombinierte Schnittstelle. Weitere Informationen finden Sie unter D3D12 \_ Graphics \_ Pipeline \_ State \_ DESC and D3D12 \_ Compute \_ Pipeline \_ State \_ DESC. | CD3DX12_PIPELINE_STATE_STREAM-Struktur (D3dx12. h)
ms.assetid: C0CEFC67-72B3-4A8D-9C88-381990FC9898
keywords:
- CD3DX12_PIPELINE_STATE_STREAM Struktur
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d52b9090fa1d3870027bbe360164627472c039e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353702"
---
# <a name="cd3dx12_pipeline_state_stream-structure"></a><span data-ttu-id="4b48f-106">CD3DX12 \_ Pipeline \_ State \_ Stream-Struktur</span><span class="sxs-lookup"><span data-stu-id="4b48f-106">CD3DX12\_PIPELINE\_STATE\_STREAM structure</span></span>

<span data-ttu-id="4b48f-107">Eine hilfsstruktur zum Erstellen und arbeiten mit Grafiken und Compute-Pipeline Zuständen über eine kombinierte Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="4b48f-107">A helper structure for creating and working with graphics and compute pipeline states through a combined interface.</span></span> <span data-ttu-id="4b48f-108">Weitere Informationen finden Sie unter [**D3D12 \_ Graphics \_ Pipeline \_ State \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) and [**D3D12 \_ Compute \_ Pipeline \_ State \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc).</span><span class="sxs-lookup"><span data-stu-id="4b48f-108">See [**D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) and [**D3D12\_COMPUTE\_PIPELINE\_STATE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc).</span></span>

<span data-ttu-id="4b48f-109">CD3DX12 \_ Pipeline \_ State \_ Stream unterstützt Windows 10 Creators Update und höher, unterstützt jedoch keine neuen Features des Fall Creators Updates, wie z. b. Ansichts Instanziierung.</span><span class="sxs-lookup"><span data-stu-id="4b48f-109">CD3DX12\_PIPELINE\_STATE\_STREAM supports Windows 10 Creators Update and newer but doesn't support new features of the Fall Creators update, such as view instancing.</span></span> <span data-ttu-id="4b48f-110">Verwenden Sie stattdessen [**CD3DX12 \_ Pipeline \_ State \_ STREAM1**](https://www.bing.com/search?q=**CD3DX12\_PIPELINE\_STATE\_STREAM1**) , um die Funktionen des Fall Creators Updates zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="4b48f-110">To support features of the Fall Creators update, use [**CD3DX12\_PIPELINE\_STATE\_STREAM1**](https://www.bing.com/search?q=**CD3DX12\_PIPELINE\_STATE\_STREAM1**) instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b48f-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="4b48f-111">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM {
  CD3DX12_PIPELINE_STATE_STREAM                       CD3DX12_PIPELINE_STATE_STREAM();
  CD3DX12_PIPELINE_STATE_STREAM                       CD3DX12_PIPELINE_STATE_STREAM(const D3D12_GRAPHICS_PIPELINE_STATE_DESC& Desc);
  CD3DX12_PIPELINE_STATE_STREAM                       CD3DX12_PIPELINE_STATE_STREAM(const D3D12_COMPUTE_PIPELINE_STATE_DESC& Desc);
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



## <a name="members"></a><span data-ttu-id="4b48f-112">Member</span><span class="sxs-lookup"><span data-stu-id="4b48f-112">Members</span></span>

<dl> <dt>

<span data-ttu-id="4b48f-113">**CD3DX12 \_ Pipeline \_ State \_ Stream ()**</span><span class="sxs-lookup"><span data-stu-id="4b48f-113">**CD3DX12\_PIPELINE\_STATE\_STREAM()**</span></span>
</dt> <dd>

<span data-ttu-id="4b48f-114">Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12 Pipeline- \_ \_ Zustandsdaten \_ Stroms.</span><span class="sxs-lookup"><span data-stu-id="4b48f-114">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM.</span></span>

</dd> <dt>

<span data-ttu-id="4b48f-115">**CD3DX12 \_ Pipeline \_ State \_ Stream (konstant D3D12 \_ Grafik \_ Pipeline \_ Status \_ DESC& DESC)**</span><span class="sxs-lookup"><span data-stu-id="4b48f-115">**CD3DX12\_PIPELINE\_STATE\_STREAM(const D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC& Desc)**</span></span>
</dt> <dd>

<span data-ttu-id="4b48f-116">Erstellt eine neue Instanz eines CD3DX12 \_ Pipeline \_ Zustandsdaten \_ Stroms, der mit Werten initialisiert wird, die aus einer **CD3DX12 \_ Pipeline \_ State \_ Stream** -Struktur kopiert wurden.</span><span class="sxs-lookup"><span data-stu-id="4b48f-116">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM, initialized with values copied from a **CD3DX12\_PIPELINE\_STATE\_STREAM** structure.</span></span>

</dd> <dt>

<span data-ttu-id="4b48f-117">**CD3DX12 \_ Pipeline \_ State \_ Stream (konstant D3D12 \_ Compute \_ Pipeline \_ State \_ DESC& DESC)**</span><span class="sxs-lookup"><span data-stu-id="4b48f-117">**CD3DX12\_PIPELINE\_STATE\_STREAM(const D3D12\_COMPUTE\_PIPELINE\_STATE\_DESC& Desc)**</span></span>
</dt> <dd>

<span data-ttu-id="4b48f-118">Erstellt eine neue Instanz eines CD3DX12 \_ Pipeline \_ Zustandsdaten \_ Stroms, der mit Werten initialisiert wird, die aus einer **CD3DX12 \_ Pipeline \_ State \_ Stream** -Struktur kopiert wurden.</span><span class="sxs-lookup"><span data-stu-id="4b48f-118">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM, initialized with values copied from a **CD3DX12\_PIPELINE\_STATE\_STREAM** structure.</span></span>

</dd> <dt>

<span data-ttu-id="4b48f-119">**GraphicsDescV0()**</span><span class="sxs-lookup"><span data-stu-id="4b48f-119">**GraphicsDescV0()**</span></span>
</dt> <dd>

<span data-ttu-id="4b48f-120">Gibt den Inhalt des CD3DX12 \_ Pipeline \_ State- \_ Streamobjekts als D3D12- \_ Grafik \_ Pipeline \_ State- \_ DESC-Struktur nach Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="4b48f-120">returns the contents of the CD3DX12\_PIPELINE\_STATE\_STREAM object as a D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC structure by value.</span></span> <span data-ttu-id="4b48f-121">Beachten Sie, \_ dass \_ der D3D12 graphics Pipeline \_ State \_ DESC den **CS** -Member nicht enthält, sodass dieser Wert bei der Konvertierung verloren geht.</span><span class="sxs-lookup"><span data-stu-id="4b48f-121">Note that D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC does not include the **CS** member, so this value is lost in the conversion.</span></span>

</dd> <dt>

<span data-ttu-id="4b48f-122">**ComputeDescV0()**</span><span class="sxs-lookup"><span data-stu-id="4b48f-122">**ComputeDescV0()**</span></span>
</dt> <dd>

<span data-ttu-id="4b48f-123">Gibt den Inhalt des CD3DX12 \_ Pipeline- \_ \_ StatusStream-Objekts als \_ D3D12 Compute \_ Pipeline \_ State \_ DESC-Struktur nach Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="4b48f-123">returns the contents of the CD3DX12\_PIPELINE\_STATE\_STREAM object as a D3D12\_COMPUTE\_PIPELINE\_STATE\_DESC structure by value.</span></span> <span data-ttu-id="4b48f-124">Beachten Sie, \_ dass der D3D12 Compute \_ Pipeline \_ State \_ **UNSC nicht das Input Layout** enthält. **ibstrip Page Value**, **primitivetopologytype**, **vs**, **GS**, **streamoutput**, **HS**, **DS**, **PS**, **blendstate**, **depthschablone cilstate**, **dsvformat**, **rasterizerstate**, **numrootsignature**, **r tvformats**, **SampleDesc** oder **samplemask** -Member, sodass diese Werte bei der Konvertierung verloren gehen.</span><span class="sxs-lookup"><span data-stu-id="4b48f-124">Note that D3D12\_COMPUTE\_PIPELINE\_STATE\_DESC does not include the **InputLayout**, **IBStripCutValue**, **PrimitiveTopologyType**, **VS**, **GS**, **StreamOutput**, **HS**, **DS**, **PS**, **BlendState**, **DepthStencilState**, **DSVFormat**, **RasterizerState**, **NumRootSignature**, **RTVFormats**, **SampleDesc**, or **SampleMask** members, so these values are lost in the conversion.</span></span>

</dd> <dt>

<span data-ttu-id="4b48f-125">**Flags**</span><span class="sxs-lookup"><span data-stu-id="4b48f-125">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="4b48f-126">Beschreibt die Pipeline-Statusflags, die Funktionen wie "Tool Debuggen" steuern.</span><span class="sxs-lookup"><span data-stu-id="4b48f-126">Describes the pipeline state flags, which control features such as "tool debug".</span></span>

</dd> <dt>

<span data-ttu-id="4b48f-127">**Nodemask**</span><span class="sxs-lookup"><span data-stu-id="4b48f-127">**NodeMask**</span></span>
</dt> <dd>

<span data-ttu-id="4b48f-128">Beschreibt die Pipeline Status-Knoten Maske, die verwendet wird, um die Knoten (physischen Adapter des Geräts) zu identifizieren, für die das PSO in Szenarien mit mehreren Adaptern gilt. jedes Bit in der Maske entspricht einem einzelnen Knoten.</span><span class="sxs-lookup"><span data-stu-id="4b48f-128">Describes the pipeline state node mask, which is used to identify the nodes (physical adapters of the device) that the PSO applies to in Multi-Adapter scenarios; each bit in the mask corresponds to a single node.</span></span> <span data-ttu-id="4b48f-129">Legen Sie für Szenarien mit einem einzelnen Adapter diesen Wert auf 0 fest.</span><span class="sxs-lookup"><span data-stu-id="4b48f-129">For single-adapter scenarios, set this value to 0.</span></span>

</dd> <dt>

<span data-ttu-id="4b48f-130">**prootsignature**</span><span class="sxs-lookup"><span data-stu-id="4b48f-130">**pRootSignature**</span></span>
</dt> <dd>

<span data-ttu-id="4b48f-131">Beschreibt die Stamm Signatur.</span><span class="sxs-lookup"><span data-stu-id="4b48f-131">Describes the root signature.</span></span>

</dd> <dt>

<span data-ttu-id="4b48f-132">**Input Layout**</span><span class="sxs-lookup"><span data-stu-id="4b48f-132">**InputLayout**</span></span>
</dt> <dd>

<span data-ttu-id="4b48f-133">Beschreibt das Eingabepuffer Format für die Eingabe-Assembler-Stufe.</span><span class="sxs-lookup"><span data-stu-id="4b48f-133">Describes the input-buffer format for the input-assembler stage</span></span>

</dd> <dt>

<span data-ttu-id="4b48f-134">**Ibstripcutvalue**</span><span class="sxs-lookup"><span data-stu-id="4b48f-134">**IBStripCutValue**</span></span>
</dt> <dd>

<span data-ttu-id="4b48f-135">Beschreibt den speziellen Indexwert des Eingabe Puffers, der bei Verwendung der Dreieck-Strip-Topologie einen Ausschneide Wert (Diskontinuität) angibt.</span><span class="sxs-lookup"><span data-stu-id="4b48f-135">Describes the special index value of the input buffer that indicates a cut (discontinuity) when using triangle-strip topology.</span></span>

</dd> <dt>

<span data-ttu-id="4b48f-136">**Primitivetopologytype**</span><span class="sxs-lookup"><span data-stu-id="4b48f-136">**PrimitiveTopologyType**</span></span>
</dt> <dd>

<span data-ttu-id="4b48f-137">Beschreibt die primitive Topologie und deren Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="4b48f-137">Describes the primitive topology and its order.</span></span>

</dd> <dt>

<span data-ttu-id="4b48f-138">**Jews**</span><span class="sxs-lookup"><span data-stu-id="4b48f-138">**VS**</span></span>
</dt> <dd>

<span data-ttu-id="4b48f-139">Beschreibt den Scheitelpunkt-Shader.</span><span class="sxs-lookup"><span data-stu-id="4b48f-139">Describes the vertex shader.</span></span>

</dd> <dt>

<span data-ttu-id="4b48f-140">**GS**</span><span class="sxs-lookup"><span data-stu-id="4b48f-140">**GS**</span></span>
</dt> <dd>

<span data-ttu-id="4b48f-141">Beschreibt den Geometry-Shader.</span><span class="sxs-lookup"><span data-stu-id="4b48f-141">Describes the geometry shader.</span></span>

</dd> <dt>

<span data-ttu-id="4b48f-142">**Streamoutput**</span><span class="sxs-lookup"><span data-stu-id="4b48f-142">**StreamOutput**</span></span>
</dt> <dd>

<span data-ttu-id="4b48f-143">Beschreibt den Ausgabepuffer für das Streaming.</span><span class="sxs-lookup"><span data-stu-id="4b48f-143">Describes the streaming output-buffer.</span></span>

</dd> <dt>

<span data-ttu-id="4b48f-144">**Jh**</span><span class="sxs-lookup"><span data-stu-id="4b48f-144">**HS**</span></span>
</dt> <dd>

<span data-ttu-id="4b48f-145">Beschreibt den Rumpf-Shader.</span><span class="sxs-lookup"><span data-stu-id="4b48f-145">Describes the hull shader.</span></span>

</dd> <dt>

<span data-ttu-id="4b48f-146">**DS**</span><span class="sxs-lookup"><span data-stu-id="4b48f-146">**DS**</span></span>
</dt> <dd>

<span data-ttu-id="4b48f-147">Beschreibt den Domänen-Shader.</span><span class="sxs-lookup"><span data-stu-id="4b48f-147">Describes the domain shader.</span></span>

</dd> <dt>

<span data-ttu-id="4b48f-148">**PS**</span><span class="sxs-lookup"><span data-stu-id="4b48f-148">**PS**</span></span>
</dt> <dd>

<span data-ttu-id="4b48f-149">Beschreibt den Pixelshader.</span><span class="sxs-lookup"><span data-stu-id="4b48f-149">Describes the pixel shader.</span></span>

</dd> <dt>

<span data-ttu-id="4b48f-150">**CS**</span><span class="sxs-lookup"><span data-stu-id="4b48f-150">**CS**</span></span>
</dt> <dd>

<span data-ttu-id="4b48f-151">Beschreibt den Compute-Shader.</span><span class="sxs-lookup"><span data-stu-id="4b48f-151">Describes the compute shader.</span></span>

</dd> <dt>

<span data-ttu-id="4b48f-152">**Blendstate**</span><span class="sxs-lookup"><span data-stu-id="4b48f-152">**BlendState**</span></span>
</dt> <dd>

<span data-ttu-id="4b48f-153">Beschreibt den Blend-Zustand.</span><span class="sxs-lookup"><span data-stu-id="4b48f-153">Describes the blend state.</span></span>

</dd> <dt>

<span data-ttu-id="4b48f-154">**Depthstencilstate**</span><span class="sxs-lookup"><span data-stu-id="4b48f-154">**DepthStencilState**</span></span>
</dt> <dd>

<span data-ttu-id="4b48f-155">Beschreibt den Status der tiefen Schablone.</span><span class="sxs-lookup"><span data-stu-id="4b48f-155">Describes the depth-stencil state.</span></span>

</dd> <dt>

<span data-ttu-id="4b48f-156">**Dsvformat**</span><span class="sxs-lookup"><span data-stu-id="4b48f-156">**DSVFormat**</span></span>
</dt> <dd>

<span data-ttu-id="4b48f-157">Beschreibt das Format der tiefen Schablone.</span><span class="sxs-lookup"><span data-stu-id="4b48f-157">Describes the depth-stencil format.</span></span>

</dd> <dt>

<span data-ttu-id="4b48f-158">**Rasterizerstate**</span><span class="sxs-lookup"><span data-stu-id="4b48f-158">**RasterizerState**</span></span>
</dt> <dd>

<span data-ttu-id="4b48f-159">Beschreibt den Status des Rasterizers.</span><span class="sxs-lookup"><span data-stu-id="4b48f-159">Describes the rasterizer state.</span></span>

</dd> <dt>

<span data-ttu-id="4b48f-160">**RTV-Formate**</span><span class="sxs-lookup"><span data-stu-id="4b48f-160">**RTVFormats**</span></span>
</dt> <dd>

<span data-ttu-id="4b48f-161">Beschreibt die renderzielformate.</span><span class="sxs-lookup"><span data-stu-id="4b48f-161">Describes the render target formats.</span></span>

</dd> <dt>

<span data-ttu-id="4b48f-162">**Sampledäsc**</span><span class="sxs-lookup"><span data-stu-id="4b48f-162">**SampleDesc**</span></span>
</dt> <dd>

<span data-ttu-id="4b48f-163">Beschreibt die Stichproben Anzahl und-Qualität.</span><span class="sxs-lookup"><span data-stu-id="4b48f-163">Describes the sample count and quality.</span></span>

</dd> <dt>

<span data-ttu-id="4b48f-164">**Samplemask**</span><span class="sxs-lookup"><span data-stu-id="4b48f-164">**SampleMask**</span></span>
</dt> <dd>

<span data-ttu-id="4b48f-165">Beschreibt die Beispiel Maske, die mit dem Blend-Status verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4b48f-165">Describes the sample mask used with the blend state.</span></span>

</dd> <dt>

<span data-ttu-id="4b48f-166">**Cachedpso**</span><span class="sxs-lookup"><span data-stu-id="4b48f-166">**CachedPSO**</span></span>
</dt> <dd>

<span data-ttu-id="4b48f-167">Beschreibt ein zwischengespeichertes PSO.</span><span class="sxs-lookup"><span data-stu-id="4b48f-167">Describes a cached PSO.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4b48f-168">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4b48f-168">Remarks</span></span>

<span data-ttu-id="4b48f-169">CD3DX12 \_ Pipeline \_ State \_ Stream unterstützt Windows 10 Creators Update und höher, unterstützt jedoch keine untergeordneten Typen, die in Windows 10 Fall Creators Update hinzugefügt wurden, z. b. für Ansichts Instanziierung.</span><span class="sxs-lookup"><span data-stu-id="4b48f-169">CD3DX12\_PIPELINE\_STATE\_STREAM supports Windows 10 Creators Update and newer, but doesn not support subobject types added in Windows 10 Fall Creators update, such as for view instancing.</span></span> <span data-ttu-id="4b48f-170">Verwenden Sie stattdessen [**CD3DX12 \_ Pipeline \_ State \_ STREAM1**](https://www.bing.com/search?q=**CD3DX12\_PIPELINE\_STATE\_STREAM1**) , um untergeordnete Typen zu unterstützen, die im Fall Creators Update hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="4b48f-170">To support subobject types added in the Fall Creators update, use [**CD3DX12\_PIPELINE\_STATE\_STREAM1**](https://www.bing.com/search?q=**CD3DX12\_PIPELINE\_STATE\_STREAM1**) instead.</span></span>

<span data-ttu-id="4b48f-171">Die barrierefreien Element Variablen dieser Struktur sind alle Typedefs der CD3DX12 \_ Pipeline State Stream-Unterordner \_ \_ \_ Vorlage, die die untergeordneten typmarker-und untergeordneten Daten in ein einzelnes Objekt kombiniert, das für eine Datenstrom Beschreibung geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="4b48f-171">The accessible member variables of this structure are all typedefs of the CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT template, which combines the subobject type-marker and subobject data into a single object suitable for a stream description.</span></span>

<span data-ttu-id="4b48f-172">Diese Typedefs lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="4b48f-172">Those typedefs are:</span></span>

<span data-ttu-id="4b48f-173"><dl> </dl></span><span class="sxs-lookup"><span data-stu-id="4b48f-173"><dl> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="4b48f-174">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4b48f-174">Requirements</span></span>



| <span data-ttu-id="4b48f-175">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4b48f-175">Requirement</span></span> | <span data-ttu-id="4b48f-176">Wert</span><span class="sxs-lookup"><span data-stu-id="4b48f-176">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="4b48f-177">Header</span><span class="sxs-lookup"><span data-stu-id="4b48f-177">Header</span></span><br/> | <dl> <span data-ttu-id="4b48f-178"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b48f-178"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b48f-179">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4b48f-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b48f-180">Strukturen des Hilfsprogramms für D3D12</span><span class="sxs-lookup"><span data-stu-id="4b48f-180">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="4b48f-181">**CD3DX12 \_ Pipeline \_ Status \_ STREAM1**</span><span class="sxs-lookup"><span data-stu-id="4b48f-181">**CD3DX12\_PIPELINE\_STATE\_STREAM1**</span></span>](cd3dx12-pipeline-state-stream1.md)
</dt> <dt>

[<span data-ttu-id="4b48f-182">**D3D12- \_ Grafik \_ Pipeline \_ Status \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="4b48f-182">**D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc)
</dt> <dt>

[<span data-ttu-id="4b48f-183">**D3D12 \_ Compute \_ Pipeline \_ State \_ Debug**</span><span class="sxs-lookup"><span data-stu-id="4b48f-183">**D3D12\_COMPUTE\_PIPELINE\_STATE\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc)
</dt> </dl>

 

 





