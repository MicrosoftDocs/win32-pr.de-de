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
# <a name="cd3dx12_pipeline_state_stream-structure"></a>CD3DX12 \_ Pipeline \_ State \_ Stream-Struktur

Eine hilfsstruktur zum Erstellen und arbeiten mit Grafiken und Compute-Pipeline Zuständen über eine kombinierte Schnittstelle. Weitere Informationen finden Sie unter [**D3D12 \_ Graphics \_ Pipeline \_ State \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) and [**D3D12 \_ Compute \_ Pipeline \_ State \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc).

CD3DX12 \_ Pipeline \_ State \_ Stream unterstützt Windows 10 Creators Update und höher, unterstützt jedoch keine neuen Features des Fall Creators Updates, wie z. b. Ansichts Instanziierung. Verwenden Sie stattdessen [**CD3DX12 \_ Pipeline \_ State \_ STREAM1**](https://www.bing.com/search?q=**CD3DX12\_PIPELINE\_STATE\_STREAM1**) , um die Funktionen des Fall Creators Updates zu unterstützen.

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

**CD3DX12 \_ Pipeline \_ State \_ Stream ()**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12 Pipeline- \_ \_ Zustandsdaten \_ Stroms.

</dd> <dt>

**CD3DX12 \_ Pipeline \_ State \_ Stream (konstant D3D12 \_ Grafik \_ Pipeline \_ Status \_ DESC& DESC)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 \_ Pipeline \_ Zustandsdaten \_ Stroms, der mit Werten initialisiert wird, die aus einer **CD3DX12 \_ Pipeline \_ State \_ Stream** -Struktur kopiert wurden.

</dd> <dt>

**CD3DX12 \_ Pipeline \_ State \_ Stream (konstant D3D12 \_ Compute \_ Pipeline \_ State \_ DESC& DESC)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 \_ Pipeline \_ Zustandsdaten \_ Stroms, der mit Werten initialisiert wird, die aus einer **CD3DX12 \_ Pipeline \_ State \_ Stream** -Struktur kopiert wurden.

</dd> <dt>

**GraphicsDescV0()**
</dt> <dd>

Gibt den Inhalt des CD3DX12 \_ Pipeline \_ State- \_ Streamobjekts als D3D12- \_ Grafik \_ Pipeline \_ State- \_ DESC-Struktur nach Wert zurück. Beachten Sie, \_ dass \_ der D3D12 graphics Pipeline \_ State \_ DESC den **CS** -Member nicht enthält, sodass dieser Wert bei der Konvertierung verloren geht.

</dd> <dt>

**ComputeDescV0()**
</dt> <dd>

Gibt den Inhalt des CD3DX12 \_ Pipeline- \_ \_ StatusStream-Objekts als \_ D3D12 Compute \_ Pipeline \_ State \_ DESC-Struktur nach Wert zurück. Beachten Sie, \_ dass der D3D12 Compute \_ Pipeline \_ State \_ **UNSC nicht das Input Layout** enthält. **ibstrip Page Value**, **primitivetopologytype**, **vs**, **GS**, **streamoutput**, **HS**, **DS**, **PS**, **blendstate**, **depthschablone cilstate**, **dsvformat**, **rasterizerstate**, **numrootsignature**, **r tvformats**, **SampleDesc** oder **samplemask** -Member, sodass diese Werte bei der Konvertierung verloren gehen.

</dd> <dt>

**Flags**
</dt> <dd>

Beschreibt die Pipeline-Statusflags, die Funktionen wie "Tool Debuggen" steuern.

</dd> <dt>

**Nodemask**
</dt> <dd>

Beschreibt die Pipeline Status-Knoten Maske, die verwendet wird, um die Knoten (physischen Adapter des Geräts) zu identifizieren, für die das PSO in Szenarien mit mehreren Adaptern gilt. jedes Bit in der Maske entspricht einem einzelnen Knoten. Legen Sie für Szenarien mit einem einzelnen Adapter diesen Wert auf 0 fest.

</dd> <dt>

**prootsignature**
</dt> <dd>

Beschreibt die Stamm Signatur.

</dd> <dt>

**Input Layout**
</dt> <dd>

Beschreibt das Eingabepuffer Format für die Eingabe-Assembler-Stufe.

</dd> <dt>

**Ibstripcutvalue**
</dt> <dd>

Beschreibt den speziellen Indexwert des Eingabe Puffers, der bei Verwendung der Dreieck-Strip-Topologie einen Ausschneide Wert (Diskontinuität) angibt.

</dd> <dt>

**Primitivetopologytype**
</dt> <dd>

Beschreibt die primitive Topologie und deren Reihenfolge.

</dd> <dt>

**Jews**
</dt> <dd>

Beschreibt den Scheitelpunkt-Shader.

</dd> <dt>

**GS**
</dt> <dd>

Beschreibt den Geometry-Shader.

</dd> <dt>

**Streamoutput**
</dt> <dd>

Beschreibt den Ausgabepuffer für das Streaming.

</dd> <dt>

**Jh**
</dt> <dd>

Beschreibt den Rumpf-Shader.

</dd> <dt>

**DS**
</dt> <dd>

Beschreibt den Domänen-Shader.

</dd> <dt>

**PS**
</dt> <dd>

Beschreibt den Pixelshader.

</dd> <dt>

**CS**
</dt> <dd>

Beschreibt den Compute-Shader.

</dd> <dt>

**Blendstate**
</dt> <dd>

Beschreibt den Blend-Zustand.

</dd> <dt>

**Depthstencilstate**
</dt> <dd>

Beschreibt den Status der tiefen Schablone.

</dd> <dt>

**Dsvformat**
</dt> <dd>

Beschreibt das Format der tiefen Schablone.

</dd> <dt>

**Rasterizerstate**
</dt> <dd>

Beschreibt den Status des Rasterizers.

</dd> <dt>

**RTV-Formate**
</dt> <dd>

Beschreibt die renderzielformate.

</dd> <dt>

**Sampledäsc**
</dt> <dd>

Beschreibt die Stichproben Anzahl und-Qualität.

</dd> <dt>

**Samplemask**
</dt> <dd>

Beschreibt die Beispiel Maske, die mit dem Blend-Status verwendet wird.

</dd> <dt>

**Cachedpso**
</dt> <dd>

Beschreibt ein zwischengespeichertes PSO.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

CD3DX12 \_ Pipeline \_ State \_ Stream unterstützt Windows 10 Creators Update und höher, unterstützt jedoch keine untergeordneten Typen, die in Windows 10 Fall Creators Update hinzugefügt wurden, z. b. für Ansichts Instanziierung. Verwenden Sie stattdessen [**CD3DX12 \_ Pipeline \_ State \_ STREAM1**](https://www.bing.com/search?q=**CD3DX12\_PIPELINE\_STATE\_STREAM1**) , um untergeordnete Typen zu unterstützen, die im Fall Creators Update hinzugefügt wurden.

Die barrierefreien Element Variablen dieser Struktur sind alle Typedefs der CD3DX12 \_ Pipeline State Stream-Unterordner \_ \_ \_ Vorlage, die die untergeordneten typmarker-und untergeordneten Daten in ein einzelnes Objekt kombiniert, das für eine Datenstrom Beschreibung geeignet ist.

Diese Typedefs lauten wie folgt:

<dl> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Strukturen des Hilfsprogramms für D3D12](helper-structures-for-d3d12.md)
</dt> <dt>

[**CD3DX12 \_ Pipeline \_ Status \_ STREAM1**](cd3dx12-pipeline-state-stream1.md)
</dt> <dt>

[**D3D12- \_ Grafik \_ Pipeline \_ Status \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc)
</dt> <dt>

[**D3D12 \_ Compute \_ Pipeline \_ State \_ Debug**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc)
</dt> </dl>

 

 





