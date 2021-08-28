---
title: 10Level9 ID3D11Gerätemethoden
description: In diesem Abschnitt werden die Unterschiede zwischen den einzelnen Featureebenen 10Level9 und D3D FEATURE LEVEL 11 0 und höher für die \_ \_ \_ \_ ID3D11Device-Methoden aufgeführt.
ms.assetid: c3bc32a9-8d97-430b-be6a-b4935d7ac56c
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f467e47d7ba623f1c28111cf3bf7cc6a07da8317
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475786"
---
# <a name="10level9-id3d11device-methods"></a>10Level9 ID3D11Gerätemethoden

In diesem Abschnitt werden die Unterschiede zwischen den einzelnen Featureebenen 10Level9 und D3D FEATURE LEVEL 11 0 und höher für die \_ \_ \_ \_ [**ID3D11Device-Methoden**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) aufgeführt.

-   [ID3D11Device::CheckCounter](#id3d11devicecheckcounter)
-   [ID3D11Device::CheckFormatSupport](#id3d11devicecheckformatsupport)
-   [ID3D11Device::CheckMultisampleQualityLevels](#id3d11devicecheckmultisamplequalitylevels)
-   [ID3D11Device::CreateBlendState](#id3d11devicecreateblendstate)
-   [ID3D11Device::CreateBlendState1](#id3d11devicecreateblendstate1)
-   [ID3D11Device::CreateBuffer](#id3d11devicecreatebuffer)
-   [ID3D11Device::CreateCounter](#id3d11devicecreatecounter)
-   [ID3D11Device::CreateDepthStencilView](#id3d11devicecreatedepthstencilview)
-   [ID3D11Device::CreateDomainShader](#id3d11devicecreatedomainshader)
-   [ID3D11Device::CreateGeometryShader](#id3d11devicecreategeometryshader)
-   [ID3D11Device::CreateGeometryShaderWithStreamOutput](#id3d11devicecreategeometryshaderwithstreamoutput)
-   [ID3D11Device::CreateHullShader](#id3d11devicecreatehullshader)
-   [ID3D11Device::CreateInputLayout](#id3d11devicecreateinputlayout)
-   [ID3D11Device::CreatePixelShader](#id3d11devicecreatepixelshader)
-   [ID3D11Device::CreatePredicate](#id3d11devicecreatepredicate)
-   [ID3D11Device::CreateQuery](#id3d11devicecreatequery)
-   [ID3D11Device::CreateRasterizerState](#id3d11devicecreaterasterizerstate)
-   [ID3D11Device::CreateRenderTargetView](#id3d11devicecreaterendertargetview)
-   [ID3D11Device::CreateSamplerState](#id3d11devicecreatesamplerstate)
-   [ID3D11Device::CreateShaderResourceView](#id3d11devicecreateshaderresourceview)
-   [ID3D11Device::CreateTexture1D](#id3d11devicecreatetexture1d)
-   [ID3D11Device::CreateTexture2D](#id3d11devicecreatetexture2d)
-   [ID3D11Device::CreateTexture3D](#id3d11devicecreatetexture3d)
-   [ID3D11Device::CreateUnorderedAccessView](#id3d11devicecreateunorderedaccessview)
-   [ID3D11Device::CreateVertexShader](#id3d11devicecreatevertexshader)
-   [ID3D11Device::OpenSharedResource](#id3d11deviceopensharedresource)
-   [Zugehörige Themen](#related-topics)

## <a name="id3d11devicecheckcounter"></a>ID3D11Device::CheckCounter




| Featureebene | Verhaltensunterschiede | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Geräteabhängige Leistungsindikatoren werden optional unterstützt. Verwenden <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkcounterinfo"><strong>Sie ID3D11Device::CheckCounterInfo,</strong></a> um die Unterstützung zu ermitteln.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecheckformatsupport"></a>ID3D11Device::CheckFormatSupport




| Featureebene | Verhaltensunterschiede | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Weitere Informationen finden Sie unter Formatunterstützung <a href="overviews-direct3d-11-devices-downlevel-intro.md">nach Featureebene</a>${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecheckmultisamplequalitylevels"></a>ID3D11Device::CheckMultisampleQualityLevels




| Featureebene | Verhaltensunterschiede | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Featureebenen bieten keine Garantien in Bezug auf die MSAA-Unterstützung.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecreateblendstate"></a>ID3D11Device::CreateBlendState



| Featureebene              | Verhaltensunterschiede                                                                                                                                                                                                                                                                                                                                             |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 1  | AlphaToCoverageEnable muss FALSE **sein.**<br/> Die ersten vier BlendEnables müssen alle denselben Wert haben.<br/> D3D11 \_ BLEND \_ SRC \_ ALPHASAT wird nicht unterstützt.<br/> Dual-Source-Farbmischung wird nicht unterstützt (SrcBlend oder DestBlend mit SRC1 im Namen)<br/>                                                                                |
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 2  | AlphaToCoverageEnable muss FALSE **sein.**<br/> Die ersten vier BlendEnables müssen alle denselben Wert haben.<br/> Die ersten vier RenderTargetWriteMasks müssen alle denselben Wert haben.<br/> D3D11 \_ BLEND \_ SRC \_ ALPHASAT wird nicht unterstützt.<br/> Dual-Source-Farbmischung wird nicht unterstützt (SrcBlend oder DestBlend mit SRC1 im Namen)<br/> |
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 3  | AlphaToCoverageEnable muss FALSE **sein.**<br/> Die ersten vier BlendEnables müssen alle denselben Wert haben.<br/> D3D11 \_ BLEND \_ SRC \_ ALPHASAT wird nicht unterstützt.<br/> Dual-Source-Farbmischung wird nicht unterstützt (SrcBlend oder DestBlend mit SRC1 im Namen)<br/>                                                                                |
| \_D3D-FEATUREEBENE \_ \_ 10 \_ 0 | Fügt alpha-to-coverage hinzu                                                                                                                                                                                                                                                                                                                                           |



 

## <a name="id3d11devicecreateblendstate1"></a>ID3D11Device::CreateBlendState1



| Featureebene              | Verhaltensunterschiede                                                                                                                                                                                                                                                                                                                                         |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 1  | Nicht unterstützt<br/>                                                                                                                                                                                                                                                                                                                                       |
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 2  | Nicht unterstützt<br/>                                                                                                                                                                                                                                                                                                                                       |
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 3  | Nicht unterstützt<br/>                                                                                                                                                                                                                                                                                                                                       |
| \_D3D-FEATUREEBENE \_ \_ 10 \_ 0 | Das *OutputMergerLogicOp-Member* wurde [**zu D3D11 FEATURE DATA \_ \_ \_ D3D11 \_ OPTIONS**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options)hinzugefügt, um die Unterstützung logischer Vorgänge zu bestimmen (bitweise Logikvorgänge zwischen Pixel-Shaderausgabe und Renderzielinhalt finden Sie unter [**D3D11 \_ RENDER TARGET BLEND \_ \_ \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-d3d11_render_target_blend_desc1)). |



 

## <a name="id3d11devicecreatebuffer"></a>ID3D11Device::CreateBuffer




| Featureebene | Verhaltensunterschiede | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Puffer können keine Renderzielansichten haben.<br /> Puffer müssen genau einen der D3D11_BIND_VERTEX_BUFFER, D3D11_BIND_INDEX_BUFFER oder D3D11_BIND_CONSTANT_BUFFER.<br /> Lässt nur Indexpuffer mit dem DXGI_FORMAT_R16_UINT zu. <br /> | 
| D3D_FEATURE_LEVEL_9_2 |  Puffer können keine Renderzielansichten haben.<br /> Puffer müssen genau einen der D3D11_BIND_VERTEX_BUFFER, D3D11_BIND_INDEX_BUFFER oder D3D11_BIND_CONSTANT_BUFFER.<br /> Ermöglicht Indexpuffer mit dem DXGI_FORMAT_R16_UINT und DXGI_FORMAT_R32_UINT Formaten wie D3D_FEATURE_LEVEL_10_0 und höher. <br /> ${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecreatecounter"></a>ID3D11Device::CreateCounter




| Featureebene | Verhaltensunterschiede | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Wird auf 9.*-Featureebene nicht unterstützt.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecreatedepthstencilview"></a>ID3D11Device::CreateDepthStencilView




| Featureebene | Verhaltensunterschiede | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Unterstützt keine zweiseitige Schablone.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecreatedomainshader"></a>ID3D11Device::CreateDomainShader




| Featureebene | Verhaltensunterschiede | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Wird auf 9.* oder 10.*-Featureebene nicht unterstützt. ${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 
| D3D_FEATURE_LEVEL_10_0 | 
| D3D_FEATURE_LEVEL_10_1 | 




 

## <a name="id3d11devicecreategeometryshader"></a>ID3D11Device::CreateGeometryShader




| Featureebene | Verhaltensunterschiede | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Wird auf 9.*-Featureebene nicht unterstützt.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecreategeometryshaderwithstreamoutput"></a>ID3D11Device::CreateGeometryShaderWithStreamOutput




| Featureebene | Verhaltensunterschiede | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Wird auf 9.*-Featureebene nicht unterstützt.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecreatehullshader"></a>ID3D11Device::CreateHullShader




| Featureebene | Verhaltensunterschiede | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Wird auf 9.* oder 10.* Featureebene nicht unterstützt.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 
| D3D_FEATURE_LEVEL_10_0 | 
| D3D_FEATURE_LEVEL_10_1 | 




 

## <a name="id3d11devicecreateinputlayout"></a>ID3D11Device::CreateInputLayout



| Featureebene             | Verhaltensunterschiede                                                                                              |
|---------------------------|-------------------------------------------------------------------------------------------------------------------|
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 1 | D3D11 INPUT \_ \_ PER \_ INSTANCE \_ DATA wird nicht unterstützt.                                                                |
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 2 | D3D11 INPUT \_ \_ PER \_ INSTANCE \_ DATA wird nicht unterstützt.                                                                |
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 3 | Vertexstream 0 (null) muss D3D11 \_ INPUT \_ PER \_ VERTEX DATA \_ aufweisen, wenn Datenströme D3D11 \_ INPUT PER \_ \_ VERTEX \_ DATA aufweisen. |



 

Ausführliche Informationen dazu, welche Formate für Scheitelpunktdaten auf jeder [Featureebene](overviews-direct3d-11-devices-downlevel-intro.md) verwendet werden können, finden Sie im Diagramm format support by feature level (Formatunterstützung nach Featureebene).

## <a name="id3d11devicecreatepixelshader"></a>ID3D11Device::CreatePixelShader



| Featureebene             | Verhaltensunterschiede                                    |
|---------------------------|---------------------------------------------------------|
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 1 | Muss ps \_ 4 \_ 0 \_ Level \_ 9 \_ 1 verwenden                          |
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 2 | Muss ps \_ 4 \_ 0 \_ Level \_ 9 \_ 1 verwenden                          |
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 3 | Muss ps \_ 4 \_ 0 \_ Level \_ 9 \_ 3 oder ps \_ 4 \_ 0 Level \_ \_ 9 \_ 1 verwenden |



 

## <a name="id3d11devicecreatepredicate"></a>ID3D11Device::CreatePredicate




| Featureebene | Verhaltensunterschiede | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Wird auf 9.*-Featureebene nicht unterstützt.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecreatequery"></a>ID3D11Device::CreateQuery



| Featureebene             | Verhaltensunterschiede                                                                                                                                  |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 1 | Ereignisabfragen werden unterstützt. Zeitstempelabfragen sind optional: Rufen [**Sie CreateQuery**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createquery) auf, um die Unterstützung zu bestimmen.               |
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 2 | Ereignis- und Verdeckungsabfragen werden unterstützt. Zeitstempelabfragen sind optional: Rufen [**Sie CreateQuery**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createquery) auf, um die Unterstützung zu bestimmen. |
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 3 | Ereignis- und Verdeckungsabfragen werden unterstützt. Zeitstempelabfragen sind optional: Rufen [**Sie CreateQuery**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createquery) auf, um die Unterstützung zu bestimmen. |



 

## <a name="id3d11devicecreaterasterizerstate"></a>ID3D11Device::CreateRasterizerState




| Featureebene | Verhaltensunterschiede | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | DepthClipEnable muss <strong>TRUE</strong>sein. DepthBiasClamp muss auf 0.${REMOVE}$ festgelegt werden.<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecreaterendertargetview"></a>ID3D11Device::CreateRenderTargetView




| Featureebene | Verhaltensunterschiede | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Kann nur Renderzielansichten von Texture2D-Objekten unterstützen.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecreatesamplerstate"></a>ID3D11Device::CreateSamplerState




| Featureebene | Verhaltensunterschiede | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Vergleichsfilter werden nicht unterstützt.<br /> Die Rahmenfarbe muss innerhalb von [0,1] sein.<br /> Min LOD darf nicht als Bruchteil verwendet werden<br /> Max. LOD muss FLT_MAX<br /> Die maximale Anisotropie ist 2.<br /> D3D11_TEXTURE_ADDRESS_MIRRORONCE nicht unterstützt.<br /> | 
| D3D_FEATURE_LEVEL_9_2 |  Vergleichsfilter werden nicht unterstützt.<br /> Die Rahmenfarbe muss innerhalb von [0,1] sein.<br /> Min LOD darf nicht als Bruchteil verwendet werden<br /> Max. LOD muss FLT_MAX<br /> Die maximale Anisotropie beträgt 16.<br /> ${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecreateshaderresourceview"></a>ID3D11Device::CreateShaderResourceView



| Featureebene             | MostDetailedMip plus MipLevels müssen die niedrigste LOD (kleinste Unterressource) enthalten. | Die Ansicht muss alle Ressourcenarrayelemente enthalten. |
|---------------------------|------------------------------------------------------------------------------|-----------------------------------------------|
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 1 | Ja                                                                          | ja                                           |
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 2 | Ja                                                                          | Ja                                           |
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 3 | Ja                                                                          | Ja                                           |



 

## <a name="id3d11devicecreatetexture1d"></a>ID3D11Device::CreateTexture1D




| Featureebene | Verhaltensunterschiede | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Wird auf 9.*-Featureebene nicht unterstützt.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecreatetexture2d"></a>ID3D11Device::CreateTexture2D

Texture2D-Ressourcen haben Grenzwerte für ihre Breite und Höhe, die sich je nach [Featureebene unterscheiden.](overviews-direct3d-11-devices-downlevel-intro.md) In den Featureebenen 9 3 sind die folgenden Mindestwerte garantiert, und einzelne \_ Implementierungen können die Anforderungen überschreiten.



| Featureebene             | Wenn MipCount > 1 ist, müssen Dimensionen eine ganzzahl | Unterstützte Mindesttexturdimension | Cubetexturdimensionen müssen eine Zweierleistung aufweisen. | Wenn MISC \_ TEXTURECUBE festgelegt ist, ist ArraySize: | Wenn MISC \_ TEXTURECUBE nicht festgelegt ist, ist ArraySize. |
|---------------------------|--------------------------------------------------------------|-------------------------------------|-----------------------------------------------|------------------------------------------------|----------------------------------------------------|
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 1 | Ja                                                          | 2048                                | Ja                                           | 6                                              | 1                                                  |
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 2 | Ja                                                          | 2048                                | Ja                                           | 6                                              | 1                                                  |
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 3 | Ja                                                          | 4096                                | Ja                                           | 6                                              | 1                                                  |



 

In der vorherigen Tabelle ist der vollständige Name von **MISC \_ TEXTURECUBE** [**D3D11 \_ RESOURCE \_ MISC \_ TEXTURECUBE.**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)

Folgendes gilt für alle 9 \_ \* [Featureebenen:](overviews-direct3d-11-devices-downlevel-intro.md)

-   Bei Verwendung von D3D11 USAGE DEFAULT oder \_ \_ D3D11 \_ USAGE \_ IMMUTABLE darf BindFlags nicht 0 (null) sein.
-   Bei Verwendung von D3D11 \_ BIND \_ DEPTH \_ STENCIL muss MipLevels 1 sein.
-   Wenn Sie die D3D11 \_ BIND \_ \_ SHADER-RESSOURCE verwenden, muss SampleDesc.Count 1 sein.
-   Bei Verwendung von D3D11 BIND PRESENT darf die Ressource \_ \_ keine D3D11 \_ BIND \_ SHADER-RESSOURCE \_ haben.
-   Wenn D3D10 DDI RESOURCE MISC SHARED verwendet wird, darf format nicht \_ \_ \_ \_ DXGI \_ FORMAT \_ R8G8B8A8 UNORM oder \_ DXGI FORMAT \_ \_ R8G8B8A8 \_ UNORM \_ SRGB sein.

## <a name="id3d11devicecreatetexture3d"></a>ID3D11Device::CreateTexture3D



| Featureebene             | Maximale Dimension (beliebige Achse) | Dimensionen müssen eine Zweierleistung haben. |
|---------------------------|------------------------------|---------------------------------|
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 1 | 256                          | Ja                             |
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 2 | 512                          | Ja                             |
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 3 | 512                          | Ja                             |



 

Wenn die Ressource D3D11 \_ USAGE \_ DEFAULT oder D3D11 \_ USAGE \_ IMMUTABLE ist, darf BindFlags nicht 0 (null) sein.

## <a name="id3d11devicecreateunorderedaccessview"></a>ID3D11Device::CreateUnorderedAccessView




| Featureebene | Verhaltensunterschiede | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Wird auf 9.*-Featureebene nicht unterstützt.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecreatevertexshader"></a>ID3D11Device::CreateVertexShader



| Featureebene             | Verhaltensunterschiede                                    |
|---------------------------|---------------------------------------------------------|
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 1 | Muss im Vergleich zu \_ 4 \_ 0 \_ Level \_ 9 \_ 1                          |
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 2 | Muss im Vergleich zu \_ 4 \_ 0 \_ Level \_ 9 \_ 1                          |
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 3 | Muss im Vergleich \_ zu 4 \_ 0 \_ Level \_ 9 \_ 3 oder \_ 4 \_ 0 Level \_ \_ 9 \_ 1 |



 

## <a name="id3d11deviceopensharedresource"></a>ID3D11Device::OpenSharedResource




| Featureebene | Verhaltensunterschiede | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 |  Verwenden <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport"><strong>Sie ID3D11Device::CheckFeatureSupport</strong></a> mit dem <a href="/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature"><strong>D3D11_FEATURE_FORMAT_SUPPORT2-Wert</strong></a> und der <a href="/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_format_support2"><strong>D3D11_FEATURE_DATA_FORMAT_SUPPORT2-Struktur,</strong></a> um zu bestimmen, ob ein Format freigegeben werden kann. Wenn das Format freigegeben werden kann, <strong>gibt CheckFeatureSupport</strong> <a href="/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2"><strong>das</strong></a> D3D11_FORMAT_SUPPORT2_SHAREABLE zurück.<br /><blockquote>[!Note]<br />[<strong>DXGI_FORMAT_R8G8B8A8_UNORM</strong>](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) und <strong>DXGI_FORMAT_R8G8B8A8_UNORM_SRGB</strong> bei Verwendung von Featureebene 9 nie gemeinsam verwendet werden können, auch wenn das Gerät optionale Featureunterstützung für <strong>D3D11_FORMAT_SUPPORT_SHAREABLE.</strong> Der Versuch, freigegebene Ressourcen mit DXGI-Formaten <strong>DXGI_FORMAT_R8G8B8A8_UNORM</strong> und DXGI_FORMAT_R8G8B8A8_UNORM_SRGB zu erstellen, wird immer <strong>fehlschlagen,</strong> es sei denn, die Featureebene ist 10_0 oder höher.</blockquote><br /> ${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[10Level9-Referenz](d3d11-graphics-reference-10level9.md)
</dt> </dl>

 

