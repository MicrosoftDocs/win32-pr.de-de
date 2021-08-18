---
title: CD3DX12_PIPELINE_STATE_STREAM -Struktur (D3dx12.h)
description: Eine Hilfsstruktur zum Erstellen und Arbeiten mit Grafik- und Computepipelinezuständen über eine kombinierte Schnittstelle. Siehe D3D12 \_ GRAPHICS \_ PIPELINE STATE \_ \_ DESC und D3D12 \_ COMPUTE PIPELINE STATE \_ \_ \_ DESC. | CD3DX12_PIPELINE_STATE_STREAM -Struktur (D3dx12.h)
ms.assetid: C0CEFC67-72B3-4A8D-9C88-381990FC9898
keywords:
- CD3DX12_PIPELINE_STATE_STREAM-Struktur
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
ms.openlocfilehash: 95e45c46c39a21aaeb53a2980fa3c082947e92cd5bb4ab3eccbbb225001a6504
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117733982"
---
# <a name="cd3dx12_pipeline_state_stream-structure"></a>CD3DX12 \_ PIPELINE \_ STATE \_ STREAM-Struktur

Eine Hilfsstruktur zum Erstellen und Arbeiten mit Grafik- und Computepipelinezuständen über eine kombinierte Schnittstelle. Siehe [**D3D12 \_ GRAPHICS PIPELINE STATE \_ \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) und [**D3D12 \_ COMPUTE PIPELINE STATE \_ \_ \_ DESC.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc)

CD3DX12 PIPELINE STATE STREAM unterstützt Windows 10 Creators Update und neuere, aber keine neuen Features des Fall Creators-Updates, z. B. \_ \_ \_ Ansichtsinstancing. Um Features des Fall Creators-Updates zu unterstützen, verwenden Sie stattdessen [**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM1.**](https://www.bing.com/search?q=**CD3DX12\_PIPELINE\_STATE\_STREAM1**)

## <a name="syntax"></a>Syntax


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



## <a name="members"></a>Member

<dl> <dt>

**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM()**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12 \_ PIPELINE \_ STATE \_ STREAM.

</dd> <dt>

**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM(const D3D12 \_ GRAPHICS \_ PIPELINE \_ STATE \_ DESC& Desc)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 PIPELINE STATE STREAM, initialisiert mit Werten, die aus einer \_ \_ \_ **CD3DX12 \_ PIPELINE \_ STATE \_ STREAM-Struktur kopiert** wurden.

</dd> <dt>

**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM(const D3D12 \_ COMPUTE \_ PIPELINE \_ STATE \_ DESC& Desc)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 PIPELINE STATE STREAM, initialisiert mit Werten, die aus einer \_ \_ \_ **CD3DX12 \_ PIPELINE \_ STATE \_ STREAM-Struktur kopiert** wurden.

</dd> <dt>

**GraphicsDescV0()**
</dt> <dd>

gibt den Inhalt des CD3DX12 PIPELINE STATE STREAM-Objekts als \_ \_ \_ D3D12 \_ GRAPHICS PIPELINE STATE \_ \_ \_ DESC-Struktur nach Wert zurück. Beachten Sie, dass D3D12 GRAPHICS PIPELINE STATE DESC den CS-Member nicht enthält, sodass dieser Wert \_ bei der Konvertierung verloren \_ \_ \_ geht. 

</dd> <dt>

**ComputeDescV0()**
</dt> <dd>

gibt den Inhalt des CD3DX12 \_ PIPELINE STATE STREAM-Objekts als \_ \_ D3D12 \_ COMPUTE PIPELINE STATE \_ \_ \_ DESC-Struktur nach Wert zurück. Beachten Sie, dass D3D12 COMPUTE PIPELINE STATE DESC nicht \_ die \_ Elemente \_ \_ **InputLayout,** **IBStripCutValue,** **PrimitiveTopologyType,** **VS**, **GS,** **StreamOutput,** **HS,** **DS,** **PS,** **BlendState,** **DepthStencilState,** **DSVFormat,** **RasterizerState,** **NumRootSignature,** **RTVFormats,** **SampleDesc** oder **SampleMask** enthält, sodass diese Werte bei der Konvertierung verloren gehen.

</dd> <dt>

**Flags**
</dt> <dd>

Beschreibt die Pipelinezustandsflags, die Funktionen wie "Tooldebuggen" steuern.

</dd> <dt>

**NodeMask**
</dt> <dd>

Beschreibt die Knotenmaske für den Pipelinezustand, mit der die Knoten (physische Adapter des Geräts) identifiziert werden, für die das PSO in Szenarien mit mehreren Adaptern gilt. Jedes Bit in der Maske entspricht einem einzelnen Knoten. Legen Sie für Szenarien mit einem einzelnen Adapter diesen Wert auf 0 fest.

</dd> <dt>

**pRootSignature**
</dt> <dd>

Beschreibt die Stammsignatur.

</dd> <dt>

**InputLayout**
</dt> <dd>

Beschreibt das Eingabepufferformat für die Eingabe-Assembler-Phase.

</dd> <dt>

**IBStripCutValue**
</dt> <dd>

Beschreibt den speziellen Indexwert des Eingabepuffers, der einen Schnitt (Diskontinuität) bei Verwendung einer Dreiecksleistentopologie angibt.

</dd> <dt>

**PrimitiveTopologyType**
</dt> <dd>

Beschreibt die primitive Topologie und deren Reihenfolge.

</dd> <dt>

**Vs**
</dt> <dd>

Beschreibt den Vertex-Shader.

</dd> <dt>

**GS**
</dt> <dd>

Beschreibt den Geometrie-Shader.

</dd> <dt>

**StreamOutput**
</dt> <dd>

Beschreibt den Streamingausgabepuffer.

</dd> <dt>

**Hs**
</dt> <dd>

Beschreibt den Hüllen-Shader.

</dd> <dt>

**DS**
</dt> <dd>

Beschreibt den Domänen-Shader.

</dd> <dt>

**Ps**
</dt> <dd>

Beschreibt den Pixel-Shader.

</dd> <dt>

**CS**
</dt> <dd>

Beschreibt den Compute-Shader.

</dd> <dt>

**BlendState**
</dt> <dd>

Beschreibt den Überblendungszustand.

</dd> <dt>

**DepthStencilState**
</dt> <dd>

Beschreibt den Tiefen-Schablonenzustand.

</dd> <dt>

**DSVFormat**
</dt> <dd>

Beschreibt das Tiefen-Schablonenformat.

</dd> <dt>

**RasterizerState**
</dt> <dd>

Beschreibt den Rasterizerzustand.

</dd> <dt>

**RTVFormats**
</dt> <dd>

Beschreibt die Renderzielformate.

</dd> <dt>

**SampleDesc**
</dt> <dd>

Beschreibt die Anzahl und Qualität der Stichproben.

</dd> <dt>

**SampleMask**
</dt> <dd>

Beschreibt die Beispielmaske, die mit dem Überblendungszustand verwendet wird.

</dd> <dt>

**CachedPSO**
</dt> <dd>

Beschreibt ein zwischengespeichertes PSO.

</dd> </dl>

## <a name="remarks"></a>Hinweise

CD3DX12 PIPELINE STATE STREAM unterstützt Windows 10 Creators Update und neuere Typen, aber keine Unterobjekttypen, die im \_ \_ Windows 10 Fall Creators-Update hinzugefügt werden, z. B. für die Instanzion von \_ Sichten. Um im Fall Creators-Update hinzugefügte Unterobjekttypen zu unterstützen, verwenden Sie stattdessen [**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM1.**](https://www.bing.com/search?q=**CD3DX12\_PIPELINE\_STATE\_STREAM1**)

Die zugänglichen Membervariablen dieser Struktur sind alle Typedefs der CD3DX12 \_ PIPELINE \_ STATE STREAM \_ SUBOBJECT-Vorlage, die die Typmarkierungs- und Unterobjektdaten des Unterobjekts zu einem einzelnen Objekt kombiniert, das für eine Streambeschreibung geeignet \_ ist.

Diese Typedefs sind:

<dl> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Strukturen des Hilfsprogramms für D3D12](helper-structures-for-d3d12.md)
</dt> <dt>

[**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM1**](cd3dx12-pipeline-state-stream1.md)
</dt> <dt>

[**D3D12 \_ GRAPHICS \_ PIPELINE \_ STATE \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc)
</dt> <dt>

[**D3D12 \_ COMPUTE \_ PIPELINE \_ STATE \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc)
</dt> </dl>

 

 





