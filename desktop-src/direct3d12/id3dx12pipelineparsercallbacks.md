---
title: ID3DX12PipelineParserCallbacks-Schnittstelle (D3DX12. h)
description: Eine Schnittstelle, die eine Auflistung der von der D3DX12parsePipelineStream Helper-Funktion verwendeten Parser-und Fehler Rückrufe darstellt.
ms.assetid: CBC04D17-2E19-4755-B1CB-FC42BF5083E5
keywords:
- ID3DX12PipelineParserCallbacks-Schnittstelle
- ID3DX12PipelineParserCallbacks-Schnittstelle, beschrieben
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b0061746da589c30e4745dfa3e4dc573f7b5d52
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106371929"
---
# <a name="id3dx12pipelineparsercallbacks-interface"></a>ID3DX12PipelineParserCallbacks-Schnittstelle

Eine Schnittstelle, die eine Auflistung der von der [**D3DX12parsePipelineStream**](d3dx12parsepipelinestream.md) Helper-Funktion verwendeten Parser-und Fehler Rückrufe darstellt.

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DX12PipelineParserCallbacks** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                                    | BESCHREIBUNG                                                                                                                                                                  |
|:------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BlendStateCb**](id3dx12pipelineparsercallbacks-blendstatecb.md)                       | Ruft den untergeordneten Blend-Zustands Beschreibungs Rückruf eines Objekts auf, das diese Schnittstelle implementiert.<br/>                                                                 |
| [**CachedPSOCb**](id3dx12pipelineparsercallbacks-cachedpsocb.md)                         | Ruft den zwischengespeicherten PSO (Pipeline State Object)-untergeordneten Rückruf eines Objekts auf, das diese Schnittstelle implementiert.<br/>                                                      |
| [**CSCb**](id3dx12pipelineparsercallbacks-cscb.md)                                       | Ruft den Compute-Shader-untergeordneten Rückruf eines Objekts auf, das diese Schnittstelle implementiert.<br/>                                                                          |
| [**DepthStencilState1Cb**](id3dx12pipelineparsercallbacks-depthstencilstate1cb.md)       | Ruft den unterbobject-Rückruf der tiefen Schablone ([**D3D12 \_ tiefen \_ Schablone \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1)) eines Objekts auf, das diese Schnittstelle implementiert.<br/> |
| [**DepthStencilStateCb**](id3dx12pipelineparsercallbacks-dsvformatcb.md)                 | Ruft den untergeordneten Rückruf eines Objekts, das diese Schnittstelle implementiert, mit dem tiefen Schablone-Wert Format auf.<br/>                                                              |
| [**DepthStencilStateCb**](id3dx12pipelineparsercallbacks-depthstencilstatecb.md)         | Ruft den Unterbrechungs Status der tiefen Schablone eines Objekts auf, das diese Schnittstelle implementiert.<br/>                                                                     |
| [**DSCb**](id3dx12pipelineparsercallbacks-dscb.md)                                       | Ruft den Domänen-shadersubobject-Rückruf eines Objekts auf, das diese Schnittstelle implementiert.<br/>                                                                           |
| [**ErrorBadInputParameter**](id3dx12pipelineparsercallbacks-errorbadinputparameter.md)   | Ruft den ungültigen Eingabeparameter-Fehler Rückruf eines Objekts auf, das diese Schnittstelle implementiert.<br/>                                                                         |
| [**ErrorDuplicateSubobject**](id3dx12pipelineparsercallbacks-errorduplicatesubobject.md) | Ruft den doppelten untergeordneten Fehler Rückruf eines Objekts auf, das diese Schnittstelle implementiert.<br/>                                                                         |
| [**ErrorUnknownSubobject**](id3dx12pipelineparsercallbacks-errorunknownsubobject.md)     | Ruft den unbekannten untergeordneten Fehler Rückruf eines Objekts auf, das diese Schnittstelle implementiert.<br/>                                                                           |
| [**FlagsCb**](id3dx12pipelineparsercallbacks-flagscb.md)                                 | Ruft den untergeordneten Flags-Rückruf eines Objekts auf, das diese Schnittstelle implementiert.<br/>                                                                                   |
| [**GSCb**](id3dx12pipelineparsercallbacks-gscb.md)                                       | Ruft den Geometry-shadersubobject-Rückruf eines Objekts auf, das diese Schnittstelle implementiert.<br/>                                                                         |
| [**HSCb**](id3dx12pipelineparsercallbacks-hscb.md)                                       | Ruft den Hull-Shader-untergeordneten Rückruf eines Objekts auf, das diese Schnittstelle implementiert.<br/>                                                                             |
| [**IBStripCutValueCb**](id3dx12pipelineparsercallbacks-ibstripcutvaluecb.md)             | Ruft den untergeordneten Rückruf Wert des Index Puffers eines Objekts auf, das diese Schnittstelle implementiert.<br/>                                                            |
| [**InputLayoutCb**](id3dx12pipelineparsercallbacks-inputlayoutcb.md)                     | Ruft das Eingabe Layout-untergeordnete Rückruf eines Objekts auf, das diese Schnittstelle implementiert.<br/>                                                                            |
| [**Nodemaskcb**](id3dx12pipelineparsercallbacks-nodemaskcb.md)                           | Ruft den nodemask-untergeordneten Rückruf eines Objekts auf, das diese Schnittstelle implementiert.<br/>                                                                                |
| [**PrimitiveTopologyTypeCb**](id3dx12pipelineparsercallbacks-primitivetopologytypecb.md) | Ruft den untergeordneten Topologietyp-Rückruf eines Objekts auf, das diese Schnittstelle implementiert.<br/>                                                                 |
| [**PSCb**](id3dx12pipelineparsercallbacks-pscb.md)                                       | Ruft den pixelshadersubobject-Rückruf eines Objekts auf, das diese Schnittstelle implementiert.<br/>                                                                            |
| [**RasterizerStateCb**](id3dx12pipelineparsercallbacks-rasterizerstatecb.md)             | Ruft den Zustands Beschreibungs Rückruf für den Raster eines Objekts auf, das diese Schnittstelle implementiert.<br/>                                                            |
| [**Rootsignaturecb**](id3dx12pipelineparsercallbacks-rootsignaturecb.md)                 | Ruft den untergeordneten Signatur-untergeordneten Rückruf eines Objekts auf, das diese Schnittstelle implementiert.<br/>                                                                          |
| [**RTVFormatsCb**](id3dx12pipelineparsercallbacks-rtvformatscb.md)                       | Ruft den untergeordneten Rückruf des renderzielformatarrays eines Objekts auf, das diese Schnittstelle implementiert.<br/>                                                              |
| [**SampleDescCb**](id3dx12pipelineparsercallbacks-sampledesccb.md)                       | Ruft den Beispiel Beschreibungs-Rückruf eines Objekts auf, das diese Schnittstelle implementiert.<br/>                                                                      |
| [**SampleMaskCb**](id3dx12pipelineparsercallbacks-samplemaskcb.md)                       | Ruft den Sample Mask-Unterordner Rückruf eines Objekts auf, das diese Schnittstelle implementiert.<br/>                                                                             |
| [**StreamOutputCb**](id3dx12pipelineparsercallbacks-streamoutputcb.md)                   | Ruft den untergeordneten Datenstrom-Ausgabe Beschreibungs Rückruf eines Objekts auf, das diese Schnittstelle implementiert.<br/>                                                               |
| [**VSCb**](id3dx12pipelineparsercallbacks-vscb.md)                                       | Ruft den Vertex-shadersubobject-Rückruf eines Objekts auf, das diese Schnittstelle implementiert.<br/>                                                                           |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX12. h</dt> </dl>  |
| Bibliothek<br/> | <dl> <dt>D3D12. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Hilfsschnittstellen für Direct3D 12](helper-interfaces-for-d3d12.md)
</dt> <dt>

[**D3DX12parsePipelineStream**](d3dx12parsepipelinestream.md)
</dt> </dl>

 

 





