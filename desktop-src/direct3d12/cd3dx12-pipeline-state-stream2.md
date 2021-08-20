---
title: CD3DX12_PIPELINE_STATE_STREAM2 -Struktur (D3dx12.h)
description: Eine Hilfsstruktur zum Erstellen und Arbeiten mit Grafik- und Computepipelinezuständen über eine kombinierte Schnittstelle.
keywords:
- CD3DX12_PIPELINE_STATE_STREAM2-Struktur
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM2
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/03/2021
ms.openlocfilehash: 18b662217f5e2a59c7925e0f401a9288ea710e8a
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812335"
---
# <a name="cd3dx12_pipeline_state_stream2-structure"></a>CD3DX12_PIPELINE_STATE_STREAM2-Struktur

Eine Hilfsstruktur zum Erstellen und Arbeiten mit Grafik- und Computepipelinezuständen über eine kombinierte Schnittstelle. Siehe [**D3D12_GRAPHICS_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) und [**D3D12_COMPUTE_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc).

**CD3DX12_PIPELINE_STATE_STREAM2** Betriebssystem-Build 19041 und darüber (bei der es eine Gitternetz-Shaderpipeline gibt).

## <a name="syntax"></a>Syntax

```cpp
struct CD3DX12_PIPELINE_STATE_STREAM2
{
    CD3DX12_PIPELINE_STATE_STREAM2();
    CD3DX12_PIPELINE_STATE_STREAM2(const D3D12_GRAPHICS_PIPELINE_STATE_DESC& Desc) noexcept;
    CD3DX12_PIPELINE_STATE_STREAM2(const D3DX12_MESH_SHADER_PIPELINE_STATE_DESC& Desc) noexcept;
    CD3DX12_PIPELINE_STATE_STREAM2(const D3D12_COMPUTE_PIPELINE_STATE_DESC& Desc) noexcept;
    CD3DX12_PIPELINE_STATE_STREAM_FLAGS Flags;
    CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK NodeMask;
    CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE pRootSignature;
    CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT InputLayout;
    CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE IBStripCutValue;
    CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY PrimitiveTopologyType;
    CD3DX12_PIPELINE_STATE_STREAM_VS VS;
    CD3DX12_PIPELINE_STATE_STREAM_GS GS;
    CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT StreamOutput;
    CD3DX12_PIPELINE_STATE_STREAM_HS HS;
    CD3DX12_PIPELINE_STATE_STREAM_DS DS;
    CD3DX12_PIPELINE_STATE_STREAM_PS PS;
    CD3DX12_PIPELINE_STATE_STREAM_AS AS;
    CD3DX12_PIPELINE_STATE_STREAM_MS MS;
    CD3DX12_PIPELINE_STATE_STREAM_CS CS;
    CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC BlendState;
    CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1 DepthStencilState;
    CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT DSVFormat;
    CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER RasterizerState;
    CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS RTVFormats;
    CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC SampleDesc;
    CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK SampleMask;
    CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO CachedPSO;
    CD3DX12_PIPELINE_STATE_STREAM_VIEW_INSTANCING ViewInstancingDesc;
    D3D12_GRAPHICS_PIPELINE_STATE_DESC GraphicsDescV0() const noexcept;
    D3D12_COMPUTE_PIPELINE_STATE_DESC ComputeDescV0() const noexcept;
};
```

## <a name="members"></a>Member

`CD3DX12_PIPELINE_STATE_STREAM2`

Standardkonstruktor Erstellt eine neue, nicht initialisierte Instanz eines **CD3DX12_PIPELINE_STATE_STREAM2**.

`CD3DX12_PIPELINE_STATE_STREAM2(const D3D12_GRAPHICS_PIPELINE_STATE_DESC&)`

Konstruktor, der eine neue Instanz eines **-CD3DX12_PIPELINE_STATE_STREAM2** mit dem Inhalt einer -Struktur [**D3D12_GRAPHICS_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) initialisiert wird.

Anschließend müssen Sie Gitternetz- und Verstärkungs-Shader manuell **festlegen,** da sie in der -D3D12_GRAPHICS_PIPELINE_STATE_DESC.

`CD3DX12_PIPELINE_STATE_STREAM2(const D3DX12_MESH_SHADER_PIPELINE_STATE_DESC&)`

Konstruktor, der eine neue Instanz eines **-CD3DX12_PIPELINE_STATE_STREAM2** mit dem Inhalt einer -Struktur [**D3DX12_MESH_SHADER_PIPELINE_STATE_DESC**](d3dx12-mesh-shader-pipeline-state-desc.md) initialisiert wird.

`CD3DX12_PIPELINE_STATE_STREAM2(const D3D12_COMPUTE_PIPELINE_STATE_DESC&)`

Konstruktor, der eine neue Instanz eines **-CD3DX12_PIPELINE_STATE_STREAM2** mit dem Inhalt einer -Struktur [**D3D12_COMPUTE_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc) initialisiert wird.

`Flags`

Typ: **[CD3DX12_PIPELINE_STATE_STREAM_FLAGS](cd3dx12-pipeline-state-stream-flags.md)**

Flags (z. B. um anzugeben, dass der Pipelinezustand mit zusätzlichen Informationen kompiliert werden soll, um das Debuggen zu unterstützen).

`NodeMask`

Typ: **[CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK](cd3dx12-pipeline-state-stream-node-mask.md)**

Beschreibt die Knotenmaske für den Pipelinezustand, mit der die Knoten (physische Adapter des Geräts) identifiziert werden, für die das PSO in Szenarien mit mehreren Adaptern gilt. Jedes Bit in der Maske entspricht einem einzelnen Knoten. Verwenden Sie für Szenarien mit einem einzelnen Adapter 0.

`pRootSignature`

Typ: **[CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE](cd3dx12-pipeline-state-stream-root-signature.md)**

Beschreibt die Stammsignatur.

`InputLayout`

Typ: **[CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT](cd3dx12-pipeline-state-stream-input-layout.md)**

Beschreibt das Eingabepufferformat für die Eingabe-Assembler-Phase.

`IBStripCutValue`

Typ: **[CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE](cd3dx12-pipeline-state-stream-ib-strip-cut-value.md)**

Beschreibt den speziellen Indexwert des Eingabepuffers, der einen Schnitt (Diskontinuität) bei Verwendung einer Dreiecksleistentopologie angibt.

`PrimitiveTopologyType`

Typ: **[CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY](cd3dx12-pipeline-state-stream-primitive-topology.md)**

Beschreibt die primitive Topologie und deren Reihenfolge.

`VS`

Typ: **[CD3DX12_PIPELINE_STATE_STREAM_VS](cd3dx12-pipeline-state-stream-vs.md)**

Beschreibt den Vertex-Shader.

`GS`

Typ: **[CD3DX12_PIPELINE_STATE_STREAM_GS](cd3dx12-pipeline-state-stream-gs.md)**

Beschreibt den Geometrie-Shader.

`StreamOutput`

Typ: **[CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT](cd3dx12-pipeline-state-stream-stream-output.md)**

Beschreibt den Streamingausgabepuffer.

`HS`

Typ: **[CD3DX12_PIPELINE_STATE_STREAM_HS](cd3dx12-pipeline-state-stream-hs.md)**

Beschreibt den Hüllen-Shader.

`DS`

Typ: **[CD3DX12_PIPELINE_STATE_STREAM_DS](cd3dx12-pipeline-state-stream-ds.md)**

Beschreibt den Domänen-Shader.

`PS`

Typ: **[CD3DX12_PIPELINE_STATE_STREAM_PS](cd3dx12-pipeline-state-stream-ps.md)**

Beschreibt den Pixel-Shader.

`AS`

Typ: **CD3DX12_PIPELINE_STATE_STREAM_AS**

Beschreibt den Verstärkungs-Shader.

`MS`

Typ: **CD3DX12_PIPELINE_STATE_STREAM_MS**

Beschreibt den Gitternetz-Shader.

`CS`

Typ: **[CD3DX12_PIPELINE_STATE_STREAM_CS](cd3dx12-pipeline-state-stream-cs.md)**

Beschreibt den Compute-Shader.

`BlendState`

Typ: **[CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC](cd3dx12-pipeline-state-stream-blend-desc.md)**

Beschreibt den Überblendungszustand.

`DepthStencilState`

Typ: **[CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1](cd3dx12-pipeline-state-stream-depth-stencil1.md)**

Beschreibt den Tiefen-Schablonenzustand.

`DSVFormat`

Typ: **[CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT](cd3dx12-pipeline-state-stream-depth-stencil-format.md)**

Beschreibt das Tiefen-Schablonenformat.

`RasterizerState`

Typ: **[CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER](cd3dx12-pipeline-state-stream-rasterizer.md)**

Beschreibt den Rasterizerzustand.

`RTVFormats`

Typ: **[CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS](cd3dx12-pipeline-state-stream-render-target-formats.md)**

Beschreibt die Renderzielformate.

`SampleDesc`

Typ: **[CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC](cd3dx12-pipeline-state-stream-sample-desc.md)**

Beschreibt die Anzahl und Qualität der Stichproben.

`SampleMask`

Typ: **[CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK](cd3dx12-pipeline-state-stream-sample-mask.md)**

Beschreibt die Beispielmaske, die mit dem Überblendungszustand verwendet wird.

`CachedPSO`

Typ: **[CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO](cd3dx12-pipeline-state-stream-cached-pso.md)**

Beschreibt ein zwischengespeichertes PSO.

`ViewInstancingDesc`

Typ: **[CD3DX12_PIPELINE_STATE_STREAM_VIEW_INSTANCING](cd3dx12-pipeline-state-stream-view-instancing.md)**

Beschreibt eine Konfiguration der Ansichtsinstancierung.

`GraphicsDescV0`

Gibt [**D3D12_GRAPHICS_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc)zurück.

gibt den Inhalt  des CD3DX12_PIPELINE_STATE_STREAM2-Objekts als **D3D12_GRAPHICS_PIPELINE_STATE_DESC-Struktur** nach Wert zurück. **D3D12_GRAPHICS_PIPELINE_STATE_DESC** den CS-Member nicht  enthält, sodass der Wert bei der Konvertierung verloren geht.

`ComputeDescV0`

Gibt [**D3D12_COMPUTE_PIPELINE_STATE_DESC zurück.**](/windows/win32/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc)

gibt den Inhalt  des CD3DX12_PIPELINE_STATE_STREAM2-Objekts als **D3D12_COMPUTE_PIPELINE_STATE_DESC-Struktur** nach Wert zurück. **D3D12_COMPUTE_PIPELINE_STATE_DESC** enthält nicht die Member *InputLayout*, *IBStripCutValue*, *PrimitiveTopologyType*, *VS*, *GS*, *StreamOutput*, *HS*, *DS*, *PS*, *BlendState*, *DepthStencilState*, *DSVFormat*, *RasterizerState*, *NumRootSignature*, *RTVFormats*, *SampleDesc* und *SampleMask*, sodass diese Werte bei der Konvertierung verloren gehen.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header | [D3dx12.h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>Siehe auch

* [Hilfsstrukturen für Direct3D 12](helper-structures-for-d3d12.md)
