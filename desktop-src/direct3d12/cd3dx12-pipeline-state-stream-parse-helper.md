---
title: CD3DX12_PIPELINE_STATE_STREAM_PARSE_HELPER-Struktur (D3dx12. h)
description: Erstellt ein internes CD3DX12 \_ Pipeline \_ State \_ Stream-Objekt aus untergeordneten Details, die an die entsprechenden Element Funktionen übermittelt werden. Diese Struktur implementiert die ID3DX12PipelineParserCallbacks-Schnittstelle.
ms.assetid: 7D4FFD1D-9FA3-4482-A67B-E742611030BC
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_PARSE_HELPER Struktur
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_PARSE_HELPER
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44cc6228f690abd677e1adc8552293e440452ec5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106366620"
---
# <a name="cd3dx12_pipeline_state_stream_parse_helper-structure"></a><span data-ttu-id="8dc05-105">CD3DX12 \_ - \_ \_ \_ \_ Analyse hilfsstruktur des Pipeline Zustandsdaten Stroms</span><span class="sxs-lookup"><span data-stu-id="8dc05-105">CD3DX12\_PIPELINE\_STATE\_STREAM\_PARSE\_HELPER structure</span></span>

<span data-ttu-id="8dc05-106">Erstellt ein internes CD3DX12 \_ Pipeline \_ State \_ Stream-Objekt aus untergeordneten Details, die an die entsprechenden Element Funktionen übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="8dc05-106">Builds an internal CD3DX12\_PIPELINE\_STATE\_STREAM object from subobject details passed into the corresponding member functions.</span></span> <span data-ttu-id="8dc05-107">Diese Struktur implementiert die [**ID3DX12PipelineParserCallbacks**](id3dx12pipelineparsercallbacks.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="8dc05-107">This struct implements the [**ID3DX12PipelineParserCallbacks**](id3dx12pipelineparsercallbacks.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="8dc05-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="8dc05-108">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_PARSE_HELPER  : public ID3DX12PipelineParserCallbacks{
  CD3DX12_PIPELINE_STATE_STREAM1 PipelineStream;
  void                           FlagsCb(D3D12_PIPELINE_STATE_FLAGS Flags);
  void                           NodeMaskCb(UINT NodeMask);
  void                           RootSignatureCb(ID3D12RootSignature* pRootSignature);
  void                           InputLayoutCb(const D3D12_INPUT_LAYOUT_DESC& InputLayout);
  void                           IBStripCutValueCb(D3D12_INDEX_BUFFER_STRIP_CUT_VALUE IBStripCutValue);
  void                           PrimitiveTopologyTypeCb(D3D12_PRIMITIVE_TOPOLOGY_TYPE PrimitiveTopologyType);
  void                           VSCb(const D3D12_SHADER_BYTECODE& VS);
  void                           GSCb(const D3D12_SHADER_BYTECODE& GS);
  void                           StreamOutputCb(const D3D12_STREAM_OUTPUT_DESC& StreamOutput);
  void                           HSCb(const D3D12_SHADER_BYTECODE& HS);
  void                           DSCb(const D3D12_SHADER_BYTECODE& DS);
  void                           PSCb(const D3D12_SHADER_BYTECODE& PS);
  void                           CSCb(const D3D12_SHADER_BYTECODE& CS);
  void                           BlendStateCb(const D3D12_BLEND_DESC& BlendState);
  void                           DepthStencilStateCb(const D3D12_DEPTH_STENCIL_DESC& DepthStencilState);
  void                           DepthStencilState1Cb(const D3D12_DEPTH_STENCIL_DESC1& DepthStencilState);
  void                           DSVFormatCb(DXGI_FORMAT DSVFormat);
  void                           RasterizerStateCb(const D3D12_RASTERIZER_DESC& RasterizerState);
  void                           RTVFormatsCb(const D3D12_RT_FORMAT_ARRAY& RTVFormats);
  void                           SampleDescCb(const DXGI_SAMPLE_DESC& SampleDesc);
  void                           SampleMaskCb(UINT SampleMask);
  void                           ViewInstancingCb(const D3D12_VIEW_INSTANCING_DESC& ViewInstancingDesc);
  void                           CachedPSOCb(const D3D12_CACHED_PIPELINE_STATE& CachedPSO);
  void                           ErrorBadInputParameter(UINT);
  void                           ErrorDuplicateSubobject(D3D12_PIPELINE_STATE_SUBOBJECT_TYPE);
  void                           ErrorUnknownSubobject(UINT);
};
```



## <a name="members"></a><span data-ttu-id="8dc05-109">Member</span><span class="sxs-lookup"><span data-stu-id="8dc05-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="8dc05-110">**Pipelinestream**</span><span class="sxs-lookup"><span data-stu-id="8dc05-110">**PipelineStream**</span></span>
</dt> <dd>

<span data-ttu-id="8dc05-111">Der interne [**CD3DX12- \_ Pipeline \_ Status \_ STREAM1**](cd3dx12-pipeline-state-stream1.md).</span><span class="sxs-lookup"><span data-stu-id="8dc05-111">The internal [**CD3DX12\_PIPELINE\_STATE\_STREAM1**](cd3dx12-pipeline-state-stream1.md).</span></span> <span data-ttu-id="8dc05-112">Der aktuelle Zustand stellt den kumulativen Effekt von Rückruf Methoden dar, die für dieses Objekt aufgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="8dc05-112">Its current state represents the cumulative effect of callback methods that have been called on this object.</span></span>

</dd> <dt>

<span data-ttu-id="8dc05-113">**Flagscb (D3D12-Flags für \_ Pipeline-Statusflags \_ \_ )**</span><span class="sxs-lookup"><span data-stu-id="8dc05-113">**FlagsCb(D3D12\_PIPELINE\_STATE\_FLAGS Flags)**</span></span>
</dt> <dd>

<span data-ttu-id="8dc05-114">Initialisiert den **Flags** -Member von **Pipelinestream** mithilfe des Werts des *Flags* -Parameters.</span><span class="sxs-lookup"><span data-stu-id="8dc05-114">Initializes the **Flags** member of **PipelineStream** using the value of the *Flags* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="8dc05-115">**Nodemaskcb (uint nodemask)**</span><span class="sxs-lookup"><span data-stu-id="8dc05-115">**NodeMaskCb(UINT NodeMask)**</span></span>
</dt> <dd>

<span data-ttu-id="8dc05-116">Initialisiert den **nodemask** -Member von **Pipelinestream** mithilfe des Werts des *nodemask* -Parameters.</span><span class="sxs-lookup"><span data-stu-id="8dc05-116">Initializes the **NodeMask** member of **PipelineStream** using the value of the *Nodemask* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="8dc05-117">**Rootsignaturecb (ID3D12RootSignature \* prootsignature)**</span><span class="sxs-lookup"><span data-stu-id="8dc05-117">**RootSignatureCb(ID3D12RootSignature\* pRootSignature)**</span></span>
</dt> <dd>

<span data-ttu-id="8dc05-118">Initialisiert den **prootsignature** -Member von **Pipelinestream** mithilfe des Werts des *prootsignature* -Parameters.</span><span class="sxs-lookup"><span data-stu-id="8dc05-118">Initializes the **pRootSignature** member of **PipelineStream** using the value of the *pRootSignature* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="8dc05-119">**Inputlayoutcb (Konstante D3D12 \_ Eingabe \_ Layout \_& inputlayout)**</span><span class="sxs-lookup"><span data-stu-id="8dc05-119">**InputLayoutCb(const D3D12\_INPUT\_LAYOUT\_DESC& InputLayout)**</span></span>
</dt> <dd>

<span data-ttu-id="8dc05-120">Initialisiert den **inputlayout** -Member von **Pipelinestream** mithilfe des Werts des *inputlayout* -Parameters.</span><span class="sxs-lookup"><span data-stu-id="8dc05-120">Initializes the **InputLayout** member of **PipelineStream** using the value of the *InputLayout* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="8dc05-121">**Ibstripcutvaluecb (D3D12 \_ Index- \_ Puffer \_ Strip- \_ Ausschneide \_ Wert ibstripcutvalue)**</span><span class="sxs-lookup"><span data-stu-id="8dc05-121">**IBStripCutValueCb(D3D12\_INDEX\_BUFFER\_STRIP\_CUT\_VALUE IBStripCutValue)**</span></span>
</dt> <dd>

<span data-ttu-id="8dc05-122">Initialisiert den **ibstripcutvalue** -Member von **Pipelinestream** mithilfe des Werts des *ibstripcutvalue* -Parameters.</span><span class="sxs-lookup"><span data-stu-id="8dc05-122">Initializes the **IBStripCutValue** member of **PipelineStream** using the value of the *IBStripCutValue* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="8dc05-123">**Primitivetopologytypecb (D3D12 \_ primitiver \_ \_ Topologietyp primitivetopologytype)**</span><span class="sxs-lookup"><span data-stu-id="8dc05-123">**PrimitiveTopologyTypeCb(D3D12\_PRIMITIVE\_TOPOLOGY\_TYPE PrimitiveTopologyType)**</span></span>
</dt> <dd>

<span data-ttu-id="8dc05-124">Initialisiert den **primitivetopologytype** -Member von **Pipelinestream** mithilfe des Werts des *primitivetopologytype* -Parameters.</span><span class="sxs-lookup"><span data-stu-id="8dc05-124">Initializes the **PrimitiveTopologyType** member of **PipelineStream** using the value of the *PrimitiveTopologyType* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="8dc05-125">**Vscb (const D3D12 \_ Shader- \_ Bytecode& vs)**</span><span class="sxs-lookup"><span data-stu-id="8dc05-125">**VSCb(const D3D12\_SHADER\_BYTECODE& VS)**</span></span>
</dt> <dd>

<span data-ttu-id="8dc05-126">Initialisiert den **vs** (Vertex Shader)-Member von **Pipelinestream** mithilfe des Werts des *vs* -Parameters.</span><span class="sxs-lookup"><span data-stu-id="8dc05-126">Initializes the **VS** (vertex shader) member of **PipelineStream** using the value of the *VS* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="8dc05-127">**Gscb (Konstanten D3D12 \_ Shader- \_ Bytecode& GS)**</span><span class="sxs-lookup"><span data-stu-id="8dc05-127">**GSCb(const D3D12\_SHADER\_BYTECODE& GS)**</span></span>
</dt> <dd>

<span data-ttu-id="8dc05-128">Initialisiert den **GS** -Member (Geometry-Shader) von **Pipelinestream** mit dem Wert des *GS* -Parameters.</span><span class="sxs-lookup"><span data-stu-id="8dc05-128">Initializes the **GS** (geometry shader) member of **PipelineStream** using the value of the *GS* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="8dc05-129">**Streamoutputcb (Konstanten D3D12 \_ Stream \_ Output \_ DESC& streamoutput)**</span><span class="sxs-lookup"><span data-stu-id="8dc05-129">**StreamOutputCb(const D3D12\_STREAM\_OUTPUT\_DESC& StreamOutput)**</span></span>
</dt> <dd>

<span data-ttu-id="8dc05-130">Initialisiert den **streamoutput** -Member von **Pipelinestream** mithilfe des Werts des *streamoutput* -Parameters.</span><span class="sxs-lookup"><span data-stu-id="8dc05-130">Initializes the **StreamOutput** member of **PipelineStream** using the value of the *StreamOutput* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="8dc05-131">**Hscb (Konstanten D3D12 \_ Shader- \_ Bytecode& HS)**</span><span class="sxs-lookup"><span data-stu-id="8dc05-131">**HSCb(const D3D12\_SHADER\_BYTECODE& HS)**</span></span>
</dt> <dd>

<span data-ttu-id="8dc05-132">Initialisiert den **HS** -Member (Hull-Shader) von **Pipelinestream** mithilfe des Werts des *HS* -Parameters.</span><span class="sxs-lookup"><span data-stu-id="8dc05-132">Initializes the **HS** (hull shader) member of **PipelineStream** using the value of the *HS* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="8dc05-133">**Dscb (Konstanten D3D12 \_ Shader- \_ Bytecode& DS)**</span><span class="sxs-lookup"><span data-stu-id="8dc05-133">**DSCb(const D3D12\_SHADER\_BYTECODE& DS)**</span></span>
</dt> <dd>

<span data-ttu-id="8dc05-134">Initialisiert den **DS** -Member (Domänen-Shader) von **Pipelinestream** mithilfe des Werts des *DS* -Parameters.</span><span class="sxs-lookup"><span data-stu-id="8dc05-134">Initializes the **DS** (domain shader) member of **PipelineStream** using the value of the *DS* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="8dc05-135">**Pscb (Konstanten D3D12 \_ Shader- \_ Bytecode& PS)**</span><span class="sxs-lookup"><span data-stu-id="8dc05-135">**PSCb(const D3D12\_SHADER\_BYTECODE& PS)**</span></span>
</dt> <dd>

<span data-ttu-id="8dc05-136">Initialisiert den **PS** -Member (Pixel-Shader) von **Pipelinestream** mit dem Wert des *PS* -Parameters.</span><span class="sxs-lookup"><span data-stu-id="8dc05-136">Initializes the **PS** (pixel shader) member of **PipelineStream** using the value of the *PS* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="8dc05-137">**Cscb (Konstanten D3D12 \_ Shader- \_ Bytecode& CS)**</span><span class="sxs-lookup"><span data-stu-id="8dc05-137">**CSCb(const D3D12\_SHADER\_BYTECODE& CS)**</span></span>
</dt> <dd>

<span data-ttu-id="8dc05-138">Initialisiert den **CS** -Member von **Pipelinestream** mit dem Wert des *CS* -Parameters.</span><span class="sxs-lookup"><span data-stu-id="8dc05-138">Initializes the **CS** member of **PipelineStream** using the value of the *CS* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="8dc05-139">**Blendstatecb (konstant D3D12 \_ Blend- \_& blendstate)**</span><span class="sxs-lookup"><span data-stu-id="8dc05-139">**BlendStateCb(const D3D12\_BLEND\_DESC& BlendState)**</span></span>
</dt> <dd>

<span data-ttu-id="8dc05-140">Initialisiert den **blendstate** -Member von **Pipelinestream** mithilfe des Werts des *blendstate* -Parameters.</span><span class="sxs-lookup"><span data-stu-id="8dc05-140">Initializes the **BlendState** member of **PipelineStream** using the value of the *BlendState* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="8dc05-141">**Depthstencilstatecb (konstant D3D12 \_ Tiefe \_ Schablone \_ DESC& depthstencilstate)**</span><span class="sxs-lookup"><span data-stu-id="8dc05-141">**DepthStencilStateCb(const D3D12\_DEPTH\_STENCIL\_DESC& DepthStencilState)**</span></span>
</dt> <dd>

<span data-ttu-id="8dc05-142">Initialisiert den **depthstencilstate** -Member von **Pipelinestream** mit dem Wert des *depthstencilstate* -Parameters, einem [**D3D12- \_ tiefen Schablone- \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc).</span><span class="sxs-lookup"><span data-stu-id="8dc05-142">Initializes the **DepthStencilState** member of **PipelineStream** using the value of the *DepthStencilState* parameter, a [**D3D12\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc).</span></span>

</dd> <dt>

<span data-ttu-id="8dc05-143">**DepthStencilState1Cb (konstant D3D12 \_ Tiefe \_ Schablone \_ DESC1& depthstencilstate)**</span><span class="sxs-lookup"><span data-stu-id="8dc05-143">**DepthStencilState1Cb(const D3D12\_DEPTH\_STENCIL\_DESC1& DepthStencilState)**</span></span>
</dt> <dd>

<span data-ttu-id="8dc05-144">Initialisiert den **depthstencilstate** -Member von **Pipelinestream** mithilfe des Werts des *depthstencilstate* -Parameters, einer [**D3D12- \_ tiefen \_ Schablone \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1).</span><span class="sxs-lookup"><span data-stu-id="8dc05-144">Initializes the **DepthStencilState** member of **PipelineStream** using the value of the *DepthStencilState* parameter, a [**D3D12\_DEPTH\_STENCIL\_DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1).</span></span>

</dd> <dt>

<span data-ttu-id="8dc05-145">**Dsvformatcb (DXGI- \_ Format dsvformat)**</span><span class="sxs-lookup"><span data-stu-id="8dc05-145">**DSVFormatCb(DXGI\_FORMAT DSVFormat)**</span></span>
</dt> <dd>

<span data-ttu-id="8dc05-146">Initialisiert den **dsvformat** -Member von **Pipelinestream** mithilfe des Werts des *dsvformat* -Parameters.</span><span class="sxs-lookup"><span data-stu-id="8dc05-146">Initializes the **DSVFormat** member of **PipelineStream** using the value of the *DSVFormat* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="8dc05-147">**Rasterizerstatecb (Konstanten D3D12 \_ Rasterizer \_& rasterizerstate)**</span><span class="sxs-lookup"><span data-stu-id="8dc05-147">**RasterizerStateCb(const D3D12\_RASTERIZER\_DESC& RasterizerState)**</span></span>
</dt> <dd>

<span data-ttu-id="8dc05-148">Initialisiert den **rasterizerstate** -Member von **Pipelinestream** mithilfe des Werts des *rasterizerstate* -Parameters.</span><span class="sxs-lookup"><span data-stu-id="8dc05-148">Initializes the **RasterizerState** member of **PipelineStream** using the value of the *RasterizerState* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="8dc05-149">**Rtvformatscb (Konstante D3D12 \_ RT- \_ Format \_ Array& rtvformats)**</span><span class="sxs-lookup"><span data-stu-id="8dc05-149">**RTVFormatsCb(const D3D12\_RT\_FORMAT\_ARRAY& RTVFormats)**</span></span>
</dt> <dd>

<span data-ttu-id="8dc05-150">Initialisiert den **rtvformats** -Member von **Pipelinestream** mithilfe des Werts des *rtvformats* -Parameters.</span><span class="sxs-lookup"><span data-stu-id="8dc05-150">Initializes the **RTVFormats** member of **PipelineStream** using the value of the *RTVFormats* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="8dc05-151">**Sampledesccb (Konstante DXGI- \_ Beispiel \_& sampleresc)**</span><span class="sxs-lookup"><span data-stu-id="8dc05-151">**SampleDescCb(const DXGI\_SAMPLE\_DESC& SampleDesc)**</span></span>
</dt> <dd>

<span data-ttu-id="8dc05-152">Initialisiert den **sampledebug** -Member von **Pipelinestream** mit dem Wert des *sampledebug* -Parameters.</span><span class="sxs-lookup"><span data-stu-id="8dc05-152">Initializes the **SampleDesc** member of **PipelineStream** using the value of the *SampleDesc* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="8dc05-153">**Samplemaskcb (uint samplemask)**</span><span class="sxs-lookup"><span data-stu-id="8dc05-153">**SampleMaskCb(UINT SampleMask)**</span></span>
</dt> <dd>

<span data-ttu-id="8dc05-154">Initialisiert den **samplemask** -Member von **Pipelinestream** mit dem Wert des *samplemask* -Parameters.</span><span class="sxs-lookup"><span data-stu-id="8dc05-154">Initializes the **SampleMask** member of **PipelineStream** using the value of the *SampleMask* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="8dc05-155">**Viewinstancingcb (Konstanten D3D12 \_ Anzeigen der \_ Instanziierung \_& viewinstancingdesc)**</span><span class="sxs-lookup"><span data-stu-id="8dc05-155">**ViewInstancingCb(const D3D12\_VIEW\_INSTANCING\_DESC& ViewInstancingDesc)**</span></span>
</dt> <dd>

<span data-ttu-id="8dc05-156">Initialisiert den **viewinstancingdesc** -Member von **Pipelinestream** mithilfe des Werts des *viewinstancingdesc* -Parameters.</span><span class="sxs-lookup"><span data-stu-id="8dc05-156">Initializes the **ViewInstancingDesc** member of **PipelineStream** using the value of the *ViewInstancingDesc* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="8dc05-157">**Cachedpsocb (const D3D12 \_ zwischen gespeicherter \_ Pipeline \_ Status& cachedpso)**</span><span class="sxs-lookup"><span data-stu-id="8dc05-157">**CachedPSOCb(const D3D12\_CACHED\_PIPELINE\_STATE& CachedPSO)**</span></span>
</dt> <dd>

<span data-ttu-id="8dc05-158">Initialisiert den **cachedpso** -Member von **Pipelinestream** mithilfe des Werts des *cachedpso* -Parameters.</span><span class="sxs-lookup"><span data-stu-id="8dc05-158">Initializes the **CachedPSO** member of **PipelineStream** using the value of the *CachedPSO* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="8dc05-159">**Errorbadinputparameter (uint)**</span><span class="sxs-lookup"><span data-stu-id="8dc05-159">**ErrorBadInputParameter(UINT)**</span></span>
</dt> <dd>

<span data-ttu-id="8dc05-160">Führt keine Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="8dc05-160">Does nothing.</span></span>

</dd> <dt>

<span data-ttu-id="8dc05-161">**Errorduplieresubobject (D3D12 \_ Pipeline \_ State \_ SubObject \_ Type)**</span><span class="sxs-lookup"><span data-stu-id="8dc05-161">**ErrorDuplicateSubobject(D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE)**</span></span>
</dt> <dd>

<span data-ttu-id="8dc05-162">Führt keine Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="8dc05-162">Does nothing.</span></span>

</dd> <dt>

<span data-ttu-id="8dc05-163">**Errorunknownsubobject (uint)**</span><span class="sxs-lookup"><span data-stu-id="8dc05-163">**ErrorUnknownSubobject(UINT)**</span></span>
</dt> <dd>

<span data-ttu-id="8dc05-164">Führt keine Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="8dc05-164">Does nothing.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8dc05-165">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8dc05-165">Remarks</span></span>

<span data-ttu-id="8dc05-166">Wenn Sie als zweiter Parameter an die [**D3DX12ParsePipelineStream**](d3dx12parsepipelinestream.md) -Funktion übergeben werden, werden die Details des internen [**CD3DX12 \_ Pipeline \_ State \_ STREAM1**](cd3dx12-pipeline-state-stream1.md) -Objekts aus dem D3D12-Pipeline-zustandsstream- [**\_ \_ \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_pipeline_state_stream_desc) geklont, der als erster Parameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="8dc05-166">When passed as the second parameter to the [**D3DX12ParsePipelineStream**](d3dx12parsepipelinestream.md) function, the details of the internal [**CD3DX12\_PIPELINE\_STATE\_STREAM1**](cd3dx12-pipeline-state-stream1.md) object are cloned from the [**D3D12\_PIPELINE\_STATE\_STREAM\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_pipeline_state_stream_desc) passed as the first parameter.</span></span> <span data-ttu-id="8dc05-167">Bei diesem Prozess wird die Beschreibung des Quelldaten Stroms überprüft.</span><span class="sxs-lookup"><span data-stu-id="8dc05-167">This process validates the source stream description.</span></span> <span data-ttu-id="8dc05-168">Wenn D3DX12ParsePipelineStream **S \_ OK** zurückgibt, sind die Quelldaten Strom Beschreibung und der resultierende **CD3DX12- \_ Pipeline \_ Status \_ STREAM1PipelineStream** gültig; andernfalls sind beide ungültig.</span><span class="sxs-lookup"><span data-stu-id="8dc05-168">If D3DX12ParsePipelineStream returns **S\_OK**, then both the source stream description and the resulting **CD3DX12\_PIPELINE\_STATE\_STREAM1PipelineStream** are valid; otherwise both are invalid.</span></span> <span data-ttu-id="8dc05-169">Ungültige Streams und andere Fehler werden nur über den Rückgabewert von D3DX12ParsePipelineStream gemeldet. Diese Struktur implementiert die Fehler Rückrufe, um keine Aktion durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="8dc05-169">Invalid streams and other errors are reported only through the return value of D3DX12ParsePipelineStream; this structure implements the error callbacks to do nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="8dc05-170">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8dc05-170">Requirements</span></span>



| <span data-ttu-id="8dc05-171">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8dc05-171">Requirement</span></span> | <span data-ttu-id="8dc05-172">Wert</span><span class="sxs-lookup"><span data-stu-id="8dc05-172">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8dc05-173">Header</span><span class="sxs-lookup"><span data-stu-id="8dc05-173">Header</span></span><br/> | <dl> <span data-ttu-id="8dc05-174"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="8dc05-174"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8dc05-175">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8dc05-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8dc05-176">Hilfsstrukturen für Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="8dc05-176">Helper Structures for Direct3D 12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="8dc05-177">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="8dc05-177">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> </dl>

 

 





