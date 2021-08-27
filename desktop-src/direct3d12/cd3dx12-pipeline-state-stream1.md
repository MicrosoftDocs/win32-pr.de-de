---
title: CD3DX12_PIPELINE_STATE_STREAM1 -Struktur (D3dx12.h)
description: Eine Hilfsstruktur zum Erstellen und Arbeiten mit Grafik- und Computepipelinezuständen über eine kombinierte Schnittstelle. Siehe [D3D12_GRAPHICS_PIPELINE_STATE_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) und [D3D12_COMPUTE_PIPELINE_STATE_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc).
ms.assetid: 4D3E4D99-E820-4220-92F3-4924791E780F
keywords:
- CD3DX12_PIPELINE_STATE_STREAM1-Struktur
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
ms.openlocfilehash: 219b198ae5c2da6d6e74db933d4c26771aa63975
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812539"
---
# <a name="cd3dx12_pipeline_state_stream1-structure"></a>CD3DX12_PIPELINE_STATE_STREAM1-Struktur

Eine Hilfsstruktur zum Erstellen und Arbeiten mit Grafik- und Computepipelinezuständen über eine kombinierte Schnittstelle. Siehe [D3D12_GRAPHICS_PIPELINE_STATE_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) und [D3D12_COMPUTE_PIPELINE_STATE_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc).

CD3DX12_PIPELINE_STATE_STREAM1 unterstützt die Windows 10 Fall Creators Update mit neuen Features wie der Ansichtsinstancierung.

Weitere [CD3DX12_PIPELINE_STATE_STREAM2](cd3dx12-pipeline-state-stream2.md) unterstützung für Betriebssystem-Build 19041 und darüber (bei der es eine Gitternetz-Shaderpipeline gibt).

## <a name="syntax"></a>Syntax


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



## <a name="members"></a>Member

<dl> <dt>

**CD3DX12_PIPELINE_STATE_STREAM1()**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12_PIPELINE_STATE_STREAM1.

</dd> <dt>

**CD3DX12_PIPELINE_STATE_STREAM1(const D3D12_GRAPHICS_PIPELINE_STATE_DESC& Desc)**
</dt> <dd>

Erstellt eine neue Instanz eines -CD3DX12_PIPELINE_STATE_STREAM1, initialisiert mit Werten, die aus einer CD3DX12_PIPELINE_STATE_STREAM1 **werden.**

</dd> <dt>

**CD3DX12_PIPELINE_STATE_STREAM1(const D3D12_COMPUTE_PIPELINE_STATE_DESC& Desc)**
</dt> <dd>

Erstellt eine neue Instanz eines -CD3DX12_PIPELINE_STATE_STREAM1, initialisiert mit Werten, die aus einer CD3DX12_PIPELINE_STATE_STREAM1 **werden.**

</dd> <dt>

**GraphicsDescV0()**
</dt> <dd>

gibt den Inhalt des CD3DX12_PIPELINE_STATE_STREAM1-Objekts als D3D12_GRAPHICS_PIPELINE_STATE_DESC-Struktur nach Wert zurück. Beachten Sie, D3D12_GRAPHICS_PIPELINE_STATE_DESC den **CS-Member** nicht enthält, sodass dieser Wert bei der Konvertierung verloren geht.

</dd> <dt>

**ComputeDescV0()**
</dt> <dd>

gibt den Inhalt des CD3DX12_PIPELINE_STATE_STREAM1-Objekts als D3D12_COMPUTE_PIPELINE_STATE_DESC Struktur nach Wert zurück. Beachten Sie, dass D3D12_COMPUTE_PIPELINE_STATE_DESC die Member **InputLayout**, **IBStripCutValue**, **PrimitiveTopologyType**, **VS**, **GS**, **StreamOutput**, **HS**, **DS**, **PS**, **BlendState**, **DepthStencilState**, **DSVFormat**, **RasterizerState**, **NumRootSignature,** **RTVFormats,** **SampleDesc** oder **SampleMask** nicht enthält, sodass diese Werte bei der Konvertierung verloren gehen.

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

[CD3DX12_PIPELINE_STATE_STREAM](cd3dx12-pipeline-state-stream.md) unterstützt die Windows 10 Fall Creators Update, aber keine Unterobjekttypen, die im Fall Creators-Update Windows 10 hinzugefügt werden, z. B. für die Instanzinstancierung von Sichten. Um die neuen Unterobjekttypen zu unterstützen, verwenden **Sie CD3DX12_PIPELINE_STATE_STREAM1.**

Die zugänglichen Membervariablen dieser Struktur sind [](/windows/win32/direct3d12/cd3dx12-pipeline-state-stream-subobject) alle Typdefinitionen der CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT-Vorlage, die die Typmarker- und Unterobjektdaten des Unterobjekts zu einem einzelnen Objekt kombiniert, das für eine Streambeschreibung geeignet ist.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header | [D3dx12.h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>Siehe auch

* [Hilfsstrukturen für D3D12](helper-structures-for-d3d12.md)
* [**CD3DX12_PIPELINE_STATE_STREAM**](cd3dx12-pipeline-state-stream.md)
* [**D3D12_GRAPHICS_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc)
* [**D3D12_COMPUTE_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc)
