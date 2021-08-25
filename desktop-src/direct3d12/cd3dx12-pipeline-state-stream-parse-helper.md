---
title: CD3DX12_PIPELINE_STATE_STREAM_PARSE_HELPER -Struktur (D3dx12.h)
description: Erstellt ein internes CD3DX12 PIPELINE STATE STREAM-Objekt aus \_ \_ \_ Unterobjektdetails, die an die entsprechenden Memberfunktionen übergeben werden. Diese Struktur implementiert die ID3DX12PipelineParserCallbacks-Schnittstelle.
ms.assetid: 7D4FFD1D-9FA3-4482-A67B-E742611030BC
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_PARSE_HELPER-Struktur
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
ms.openlocfilehash: d20c34fb2c32cc588a12ac820cd80083d3c3139fa85cbf36810379a21618e80c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119851250"
---
# <a name="cd3dx12_pipeline_state_stream_parse_helper-structure"></a>CD3DX12 \_ PIPELINE STATE STREAM PARSE \_ \_ \_ \_ HELPER-Struktur

Erstellt ein internes CD3DX12 PIPELINE STATE STREAM-Objekt aus \_ \_ \_ Unterobjektdetails, die an die entsprechenden Memberfunktionen übergeben werden. Diese Struktur implementiert die [**ID3DX12PipelineParserCallbacks-Schnittstelle.**](id3dx12pipelineparsercallbacks.md)

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

**PipelineStream**
</dt> <dd>

Der interne [**CD3DX12 \_ PIPELINE STATE \_ \_ STREAM1**](cd3dx12-pipeline-state-stream1.md). Der aktuelle Zustand stellt den kumulativen Effekt von Rückrufmethoden dar, die für dieses Objekt aufgerufen wurden.

</dd> <dt>

**FlagsCb(D3D12 \_ PIPELINE \_ STATE \_ FLAGS-Flags)**
</dt> <dd>

Initialisiert den **Flags-Member** von **PipelineStream unter** Verwendung des Werts des *Flags-Parameters.*

</dd> <dt>

**NodeMaskCb(UINT NodeMask)**
</dt> <dd>

Initialisiert den **NodeMask-Member** von **PipelineStream unter** Verwendung des Werts des *Nodemask-Parameters.*

</dd> <dt>

**RootSignatureCb(ID3D12RootSignature \* pRootSignature)**
</dt> <dd>

Initialisiert den **pRootSignature-Member** von **PipelineStream unter** Verwendung des Werts des *pRootSignature-Parameters.*

</dd> <dt>

**InputLayoutCb(const D3D12 \_ INPUT \_ LAYOUT \_ DESC& InputLayout)**
</dt> <dd>

Initialisiert den **InputLayout-Member** von **PipelineStream unter** Verwendung des Werts des *InputLayout-Parameters.*

</dd> <dt>

**IBStripCutValueCb(D3D12 \_ INDEX \_ BUFFER \_ STRIP \_ CUT \_ VALUE IBStripCutValue)**
</dt> <dd>

Initialisiert das **IBStripCutValue-Member** von **PipelineStream unter** Verwendung des Werts des *IBStripCutValue-Parameters.*

</dd> <dt>

**PrimitiveTopologyTypeCb(D3D12 \_ PRIMITIVE \_ TOPOLOGY \_ TYPE PrimitiveTopologyType)**
</dt> <dd>

Initialisiert den **PrimitiveTopologyType-Member** von **PipelineStream unter** Verwendung des Werts des *PrimitiveTopologyType-Parameters.*

</dd> <dt>

**VSCb(const D3D12 \_ SHADER \_ BYTECODE& VS)**
</dt> <dd>

Initialisiert den **VS-Member** (Vertex-Shader) von **PipelineStream unter** Verwendung des Werts des *VS-Parameters.*

</dd> <dt>

**GSCb(const D3D12 \_ SHADER \_ BYTECODE& GS)**
</dt> <dd>

Initialisiert den **GS-Member** (geometry shader) von **PipelineStream unter** Verwendung des Werts des *GS-Parameters.*

</dd> <dt>

**StreamOutputCb(const D3D12 \_ STREAM \_ OUTPUT \_ DESC& StreamOutput)**
</dt> <dd>

Initialisiert den **StreamOutput-Member** von **PipelineStream unter** Verwendung des Werts des *StreamOutput-Parameters.*

</dd> <dt>

**HSCb(const D3D12 \_ SHADER \_ BYTECODE& HS)**
</dt> <dd>

Initialisiert den **HS-Member** (Hüllen-Shader) von **PipelineStream unter** Verwendung des Werts des *HS-Parameters.*

</dd> <dt>

**DSCb(const D3D12 \_ SHADER \_ BYTECODE& DS)**
</dt> <dd>

Initialisiert den **DS-Member** (Domänen-Shader) von **PipelineStream unter** Verwendung des Werts des *DS-Parameters.*

</dd> <dt>

**PSCb(const D3D12 \_ SHADER \_ BYTECODE& PS)**
</dt> <dd>

Initialisiert den **PS-Member** (Pixel-Shader) von **PipelineStream unter** Verwendung des Werts des *PS-Parameters.*

</dd> <dt>

**CSCb(const D3D12 \_ SHADER \_ BYTECODE& CS)**
</dt> <dd>

Initialisiert den **CS-Member** von **PipelineStream unter** Verwendung des Werts des *CS-Parameters.*

</dd> <dt>

**BlendStateCb(const D3D12 \_ BLEND \_ DESC& BlendState)**
</dt> <dd>

Initialisiert den **BlendState-Member** von **PipelineStream unter** Verwendung des Werts des *BlendState-Parameters.*

</dd> <dt>

**DepthStencilStateCb(const D3D12 \_ DEPTH \_ STENCIL \_ DESC& DepthStencilState)**
</dt> <dd>

Initialisiert den **DepthStencilState-Member** von **PipelineStream** unter Verwendung des Werts des *DepthStencilState-Parameters,* einer [**D3D12 \_ \_ DEPTH-SCHABLONE \_ DESC.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)

</dd> <dt>

**DepthStencilState1Cb(const D3D12 \_ DEPTH \_ STENCIL \_ DESC1& DepthStencilState)**
</dt> <dd>

Initialisiert den **DepthStencilState-Member** von **PipelineStream** unter Verwendung des Werts des *DepthStencilState-Parameters,* einer [**D3D12 \_ \_ DEPTH-SCHABLO \_ DESC1.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1)

</dd> <dt>

**DSVFormatCb(DXGI \_ FORMAT DSVFormat)**
</dt> <dd>

Initialisiert den **DSVFormat-Member** von **PipelineStream unter** Verwendung des Werts des *DSVFormat-Parameters.*

</dd> <dt>

**RasterizerStateCb(const D3D12 \_ RASTERIZER \_ DESC& RasterizerState)**
</dt> <dd>

Initialisiert den **RasterizerState-Member** von **PipelineStream unter** Verwendung des Werts des *RasterizerState-Parameters.*

</dd> <dt>

**RTVFormatsCb(const D3D12 \_ RT \_ FORMAT \_ ARRAY& RTVFormats)**
</dt> <dd>

Initialisiert den **RTVFormats-Member** von **PipelineStream unter** Verwendung des Werts des *RTVFormats-Parameters.*

</dd> <dt>

**SampleDescCb(const DXGI \_ SAMPLE \_ DESC& SampleDesc)**
</dt> <dd>

Initialisiert den **SampleDesc-Member** von **PipelineStream unter** Verwendung des Werts des *SampleDesc-Parameters.*

</dd> <dt>

**SampleMaskCb(UINT SampleMask)**
</dt> <dd>

Initialisiert den **SampleMask-Member** von **PipelineStream unter** Verwendung des Werts des *SampleMask-Parameters.*

</dd> <dt>

**ViewInstancingCb(const D3D12 \_ VIEW \_ INSTANCING \_ DESC& ViewInstancingDesc)**
</dt> <dd>

Initialisiert das **ViewInstancingDesc-Member** von **PipelineStream** unter Verwendung des Werts des *ViewInstancingDesc-Parameters.*

</dd> <dt>

**CachedPSOCb(const D3D12 \_ CACHED \_ PIPELINE \_ STATE& CachedPSO)**
</dt> <dd>

Initialisiert den **CachedPSO-Member** von **PipelineStream unter** Verwendung des Werts des *CachedPSO-Parameters.*

</dd> <dt>

**ErrorBadInputParameter(UINT)**
</dt> <dd>

Führt keine Aktion aus.

</dd> <dt>

**ErrorDuplicateSubobject(D3D12 \_ PIPELINE \_ STATE \_ SUBOBJECT \_ TYPE)**
</dt> <dd>

Führt keine Aktion aus.

</dd> <dt>

**ErrorUnknownSubobject(UINT)**
</dt> <dd>

Führt keine Aktion aus.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Wenn die Daten als zweiter Parameter an die [**D3DX12ParsePipelineStream-Funktion**](d3dx12parsepipelinestream.md) übergeben werden, werden die Details des internen [**CD3DX12 \_ PIPELINE STATE \_ \_ STREAM1-Objekts**](cd3dx12-pipeline-state-stream1.md) aus dem [**D3D12 \_ PIPELINE STATE STREAM \_ \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_pipeline_state_stream_desc) geklont, der als erster Parameter übergeben wird. Dieser Prozess überprüft die Quellstreambeschreibung. Wenn D3DX12ParsePipelineStream **S \_ OK** zurückgibt, sind sowohl die Quellstreambeschreibung als auch die resultierende **CD3DX12 \_ PIPELINE STATE \_ \_ STREAM1PipelineStream** gültig. Andernfalls sind beide ungültig. Ungültige Streams und andere Fehler werden nur über den Rückgabewert von D3DX12ParsePipelineStream gemeldet. diese Struktur implementiert die Fehlerrückrufe, um nichts zu tun.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Hilfsstrukturen für Direct3D 12](helper-structures-for-d3d12.md)
</dt> <dt>

[**ID3DX12PipelineParserCallbacks**](id3dx12pipelineparsercallbacks.md)
</dt> </dl>

 

 





