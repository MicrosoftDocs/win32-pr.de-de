---
title: ID3DX12PipelineParserCallbacks-Schnittstelle (D3DX12.h)
description: Eine Schnittstelle, die eine Auflistung von Parser- und Fehlerrückrufen darstellt, die von der D3DX12parsePipelineStream-Hilfsfunktion verwendet werden.
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
ms.openlocfilehash: f83e0987009e60d5e207a9531cc4809f6cfcfbd5b50360a583df8cb0c01898f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117733743"
---
# <a name="id3dx12pipelineparsercallbacks-interface"></a>ID3DX12PipelineParserCallbacks-Schnittstelle

Eine Schnittstelle, die eine Auflistung von Parser- und Fehlerrückrufen darstellt, die von der [**D3DX12parsePipelineStream-Hilfsfunktion**](d3dx12parsepipelinestream.md) verwendet werden.

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DX12PipelineParserCallbacks-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                                    | Beschreibung                                                                                                                                                                  |
|:------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BlendStateCb**](id3dx12pipelineparsercallbacks-blendstatecb.md)                       | Ruft den Rückruf des Unterobjekts für die Beschreibung des Blendzustands eines Objekts auf, das diese Schnittstelle implementiert.<br/>                                                                 |
| [**CachedPSOCb**](id3dx12pipelineparsercallbacks-cachedpsocb.md)                         | Ruft den zwischengespeicherten PSO(Pipeline State Object)-Unterobjektrückruf eines Objekts auf, das diese Schnittstelle implementiert.<br/>                                                      |
| [**CSCb**](id3dx12pipelineparsercallbacks-cscb.md)                                       | Ruft den Compute-Shader-Unterobjektrückruf eines Objekts auf, das diese Schnittstelle implementiert.<br/>                                                                          |
| [**DepthStencilState1Cb**](id3dx12pipelineparsercallbacks-depthstencilstate1cb.md)       | Ruft den Tiefenschablonenzustand [**(D3D12 \_ DEPTH \_ STENCIL \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1)) des Unterobjektrückrufs eines Objekts auf, das diese Schnittstelle implementiert.<br/> |
| [**DepthStencilStateCb**](id3dx12pipelineparsercallbacks-dsvformatcb.md)                 | Ruft den Rückruf des Unterobjektrückrufs für das Format des Tiefenschablonenwerts eines Objekts auf, das diese Schnittstelle implementiert.<br/>                                                              |
| [**DepthStencilStateCb**](id3dx12pipelineparsercallbacks-depthstencilstatecb.md)         | Ruft den Rückruf des Unterobjekts des Tiefenschablonenzustands eines Objekts auf, das diese Schnittstelle implementiert.<br/>                                                                     |
| [**DSCb**](id3dx12pipelineparsercallbacks-dscb.md)                                       | Ruft den Domänen-Shader-Unterobjektrückruf eines Objekts auf, das diese Schnittstelle implementiert.<br/>                                                                           |
| [**ErrorBadInputParameter**](id3dx12pipelineparsercallbacks-errorbadinputparameter.md)   | Ruft den Fehlerrückruf für ungültige Eingabeparameter eines Objekts auf, das diese Schnittstelle implementiert.<br/>                                                                         |
| [**ErrorDuplicateSubobject**](id3dx12pipelineparsercallbacks-errorduplicatesubobject.md) | Ruft den doppelten Unterobjektfehlerrückruf eines Objekts auf, das diese Schnittstelle implementiert.<br/>                                                                         |
| [**ErrorUnknownSubobject**](id3dx12pipelineparsercallbacks-errorunknownsubobject.md)     | Ruft den unbekannten Unterobjektfehlerrückruf eines Objekts auf, das diese Schnittstelle implementiert.<br/>                                                                           |
| [**FlagsCb**](id3dx12pipelineparsercallbacks-flagscb.md)                                 | Ruft den Flags-Unterobjektrückruf eines Objekts auf, das diese Schnittstelle implementiert.<br/>                                                                                   |
| [**GSCb**](id3dx12pipelineparsercallbacks-gscb.md)                                       | Ruft den Rückruf des Geometry Shader-Unterobjekts eines Objekts auf, das diese Schnittstelle implementiert.<br/>                                                                         |
| [**HSCb**](id3dx12pipelineparsercallbacks-hscb.md)                                       | Ruft den Rückruf des Unterobjekts des Hüllen-Shaders eines Objekts auf, das diese Schnittstelle implementiert.<br/>                                                                             |
| [**IBStripCutValueCb**](id3dx12pipelineparsercallbacks-ibstripcutvaluecb.md)             | Ruft den Indexpuffer-Strip-Cut-Wert-Unterobjektrückruf eines Objekts auf, das diese Schnittstelle implementiert.<br/>                                                            |
| [**InputLayoutCb**](id3dx12pipelineparsercallbacks-inputlayoutcb.md)                     | Ruft den Eingabelayout-Unterobjektrückruf eines Objekts auf, das diese Schnittstelle implementiert.<br/>                                                                            |
| [**NodemaskCb**](id3dx12pipelineparsercallbacks-nodemaskcb.md)                           | Ruft den Rückruf des Knotenmaskenunterobjekts eines Objekts auf, das diese Schnittstelle implementiert.<br/>                                                                                |
| [**PrimitiveTopologyTypeCb**](id3dx12pipelineparsercallbacks-primitivetopologytypecb.md) | Ruft den Rückruf des subobject-Objekts des primitiven Topologietyps eines Objekts auf, das diese Schnittstelle implementiert.<br/>                                                                 |
| [**PSCb**](id3dx12pipelineparsercallbacks-pscb.md)                                       | Ruft den Rückruf des Pixel-Shader-Unterobjekts eines Objekts auf, das diese Schnittstelle implementiert.<br/>                                                                            |
| [**RasterizerStateCb**](id3dx12pipelineparsercallbacks-rasterizerstatecb.md)             | Ruft den Rückruf des Unterobjekts der Rasterizerzustandsbeschreibung eines Objekts auf, das diese Schnittstelle implementiert.<br/>                                                            |
| [**RootSignatureCB**](id3dx12pipelineparsercallbacks-rootsignaturecb.md)                 | Ruft den Rückruf des Stammsignaturunterobjekts eines Objekts auf, das diese Schnittstelle implementiert.<br/>                                                                          |
| [**RTVFormatsCb**](id3dx12pipelineparsercallbacks-rtvformatscb.md)                       | Ruft den Unterobjektrückruf des Renderzielformatarrays eines Objekts auf, das diese Schnittstelle implementiert.<br/>                                                              |
| [**SampleDescCb**](id3dx12pipelineparsercallbacks-sampledesccb.md)                       | Ruft den Beispielbeschreibungs-Unterobjektrückruf eines Objekts auf, das diese Schnittstelle implementiert.<br/>                                                                      |
| [**SampleMaskCb**](id3dx12pipelineparsercallbacks-samplemaskcb.md)                       | Ruft den Beispielmasken-Unterobjektrückruf eines Objekts auf, das diese Schnittstelle implementiert.<br/>                                                                             |
| [**StreamOutputCb**](id3dx12pipelineparsercallbacks-streamoutputcb.md)                   | Ruft den Rückruf des Unterobjekts der Streamausgabebeschreibung eines Objekts auf, das diese Schnittstelle implementiert.<br/>                                                               |
| [**VSCb**](id3dx12pipelineparsercallbacks-vscb.md)                                       | Ruft den Vertex-Shader-Unterobjektrückruf eines Objekts auf, das diese Schnittstelle implementiert.<br/>                                                                           |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX12.h</dt> </dl>  |
| Bibliothek<br/> | <dl> <dt>D3D12.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Hilfsschnittstellen für Direct3D 12](helper-interfaces-for-d3d12.md)
</dt> <dt>

[**D3DX12parsePipelineStream**](d3dx12parsepipelinestream.md)
</dt> </dl>

 

 





