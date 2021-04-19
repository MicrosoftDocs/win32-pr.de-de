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
# <a name="cd3dx12_pipeline_state_stream_parse_helper-structure"></a>CD3DX12 \_ - \_ \_ \_ \_ Analyse hilfsstruktur des Pipeline Zustandsdaten Stroms

Erstellt ein internes CD3DX12 \_ Pipeline \_ State \_ Stream-Objekt aus untergeordneten Details, die an die entsprechenden Element Funktionen übermittelt werden. Diese Struktur implementiert die [**ID3DX12PipelineParserCallbacks**](id3dx12pipelineparsercallbacks.md) -Schnittstelle.

## <a name="syntax"></a>Syntax


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



## <a name="members"></a>Member

<dl> <dt>

**Pipelinestream**
</dt> <dd>

Der interne [**CD3DX12- \_ Pipeline \_ Status \_ STREAM1**](cd3dx12-pipeline-state-stream1.md). Der aktuelle Zustand stellt den kumulativen Effekt von Rückruf Methoden dar, die für dieses Objekt aufgerufen wurden.

</dd> <dt>

**Flagscb (D3D12-Flags für \_ Pipeline-Statusflags \_ \_ )**
</dt> <dd>

Initialisiert den **Flags** -Member von **Pipelinestream** mithilfe des Werts des *Flags* -Parameters.

</dd> <dt>

**Nodemaskcb (uint nodemask)**
</dt> <dd>

Initialisiert den **nodemask** -Member von **Pipelinestream** mithilfe des Werts des *nodemask* -Parameters.

</dd> <dt>

**Rootsignaturecb (ID3D12RootSignature \* prootsignature)**
</dt> <dd>

Initialisiert den **prootsignature** -Member von **Pipelinestream** mithilfe des Werts des *prootsignature* -Parameters.

</dd> <dt>

**Inputlayoutcb (Konstante D3D12 \_ Eingabe \_ Layout \_& inputlayout)**
</dt> <dd>

Initialisiert den **inputlayout** -Member von **Pipelinestream** mithilfe des Werts des *inputlayout* -Parameters.

</dd> <dt>

**Ibstripcutvaluecb (D3D12 \_ Index- \_ Puffer \_ Strip- \_ Ausschneide \_ Wert ibstripcutvalue)**
</dt> <dd>

Initialisiert den **ibstripcutvalue** -Member von **Pipelinestream** mithilfe des Werts des *ibstripcutvalue* -Parameters.

</dd> <dt>

**Primitivetopologytypecb (D3D12 \_ primitiver \_ \_ Topologietyp primitivetopologytype)**
</dt> <dd>

Initialisiert den **primitivetopologytype** -Member von **Pipelinestream** mithilfe des Werts des *primitivetopologytype* -Parameters.

</dd> <dt>

**Vscb (const D3D12 \_ Shader- \_ Bytecode& vs)**
</dt> <dd>

Initialisiert den **vs** (Vertex Shader)-Member von **Pipelinestream** mithilfe des Werts des *vs* -Parameters.

</dd> <dt>

**Gscb (Konstanten D3D12 \_ Shader- \_ Bytecode& GS)**
</dt> <dd>

Initialisiert den **GS** -Member (Geometry-Shader) von **Pipelinestream** mit dem Wert des *GS* -Parameters.

</dd> <dt>

**Streamoutputcb (Konstanten D3D12 \_ Stream \_ Output \_ DESC& streamoutput)**
</dt> <dd>

Initialisiert den **streamoutput** -Member von **Pipelinestream** mithilfe des Werts des *streamoutput* -Parameters.

</dd> <dt>

**Hscb (Konstanten D3D12 \_ Shader- \_ Bytecode& HS)**
</dt> <dd>

Initialisiert den **HS** -Member (Hull-Shader) von **Pipelinestream** mithilfe des Werts des *HS* -Parameters.

</dd> <dt>

**Dscb (Konstanten D3D12 \_ Shader- \_ Bytecode& DS)**
</dt> <dd>

Initialisiert den **DS** -Member (Domänen-Shader) von **Pipelinestream** mithilfe des Werts des *DS* -Parameters.

</dd> <dt>

**Pscb (Konstanten D3D12 \_ Shader- \_ Bytecode& PS)**
</dt> <dd>

Initialisiert den **PS** -Member (Pixel-Shader) von **Pipelinestream** mit dem Wert des *PS* -Parameters.

</dd> <dt>

**Cscb (Konstanten D3D12 \_ Shader- \_ Bytecode& CS)**
</dt> <dd>

Initialisiert den **CS** -Member von **Pipelinestream** mit dem Wert des *CS* -Parameters.

</dd> <dt>

**Blendstatecb (konstant D3D12 \_ Blend- \_& blendstate)**
</dt> <dd>

Initialisiert den **blendstate** -Member von **Pipelinestream** mithilfe des Werts des *blendstate* -Parameters.

</dd> <dt>

**Depthstencilstatecb (konstant D3D12 \_ Tiefe \_ Schablone \_ DESC& depthstencilstate)**
</dt> <dd>

Initialisiert den **depthstencilstate** -Member von **Pipelinestream** mit dem Wert des *depthstencilstate* -Parameters, einem [**D3D12- \_ tiefen Schablone- \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc).

</dd> <dt>

**DepthStencilState1Cb (konstant D3D12 \_ Tiefe \_ Schablone \_ DESC1& depthstencilstate)**
</dt> <dd>

Initialisiert den **depthstencilstate** -Member von **Pipelinestream** mithilfe des Werts des *depthstencilstate* -Parameters, einer [**D3D12- \_ tiefen \_ Schablone \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1).

</dd> <dt>

**Dsvformatcb (DXGI- \_ Format dsvformat)**
</dt> <dd>

Initialisiert den **dsvformat** -Member von **Pipelinestream** mithilfe des Werts des *dsvformat* -Parameters.

</dd> <dt>

**Rasterizerstatecb (Konstanten D3D12 \_ Rasterizer \_& rasterizerstate)**
</dt> <dd>

Initialisiert den **rasterizerstate** -Member von **Pipelinestream** mithilfe des Werts des *rasterizerstate* -Parameters.

</dd> <dt>

**Rtvformatscb (Konstante D3D12 \_ RT- \_ Format \_ Array& rtvformats)**
</dt> <dd>

Initialisiert den **rtvformats** -Member von **Pipelinestream** mithilfe des Werts des *rtvformats* -Parameters.

</dd> <dt>

**Sampledesccb (Konstante DXGI- \_ Beispiel \_& sampleresc)**
</dt> <dd>

Initialisiert den **sampledebug** -Member von **Pipelinestream** mit dem Wert des *sampledebug* -Parameters.

</dd> <dt>

**Samplemaskcb (uint samplemask)**
</dt> <dd>

Initialisiert den **samplemask** -Member von **Pipelinestream** mit dem Wert des *samplemask* -Parameters.

</dd> <dt>

**Viewinstancingcb (Konstanten D3D12 \_ Anzeigen der \_ Instanziierung \_& viewinstancingdesc)**
</dt> <dd>

Initialisiert den **viewinstancingdesc** -Member von **Pipelinestream** mithilfe des Werts des *viewinstancingdesc* -Parameters.

</dd> <dt>

**Cachedpsocb (const D3D12 \_ zwischen gespeicherter \_ Pipeline \_ Status& cachedpso)**
</dt> <dd>

Initialisiert den **cachedpso** -Member von **Pipelinestream** mithilfe des Werts des *cachedpso* -Parameters.

</dd> <dt>

**Errorbadinputparameter (uint)**
</dt> <dd>

Führt keine Aktion aus.

</dd> <dt>

**Errorduplieresubobject (D3D12 \_ Pipeline \_ State \_ SubObject \_ Type)**
</dt> <dd>

Führt keine Aktion aus.

</dd> <dt>

**Errorunknownsubobject (uint)**
</dt> <dd>

Führt keine Aktion aus.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn Sie als zweiter Parameter an die [**D3DX12ParsePipelineStream**](d3dx12parsepipelinestream.md) -Funktion übergeben werden, werden die Details des internen [**CD3DX12 \_ Pipeline \_ State \_ STREAM1**](cd3dx12-pipeline-state-stream1.md) -Objekts aus dem D3D12-Pipeline-zustandsstream- [**\_ \_ \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_pipeline_state_stream_desc) geklont, der als erster Parameter übergeben wird. Bei diesem Prozess wird die Beschreibung des Quelldaten Stroms überprüft. Wenn D3DX12ParsePipelineStream **S \_ OK** zurückgibt, sind die Quelldaten Strom Beschreibung und der resultierende **CD3DX12- \_ Pipeline \_ Status \_ STREAM1PipelineStream** gültig; andernfalls sind beide ungültig. Ungültige Streams und andere Fehler werden nur über den Rückgabewert von D3DX12ParsePipelineStream gemeldet. Diese Struktur implementiert die Fehler Rückrufe, um keine Aktion durchzuführen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Hilfsstrukturen für Direct3D 12](helper-structures-for-d3d12.md)
</dt> <dt>

[**ID3DX12PipelineParserCallbacks**](id3dx12pipelineparsercallbacks.md)
</dt> </dl>

 

 





