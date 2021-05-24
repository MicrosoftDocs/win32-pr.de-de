---
title: Effektzustandsgruppen (Direct3D 11)
description: Effektzustände sind Name-Wert-Paare in Form eines Ausdrucks.
ms.assetid: 87883483-4fa6-4362-807e-53b79b7d1370
keywords:
- Effect, Zustandsgruppen (Direct3D 11)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5a757926d8c4c259adc94f505a778cf73233b5a
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335334"
---
# <a name="effect-state-groups-direct3d-11"></a>Effektzustandsgruppen (Direct3D 11)

Effektzustände sind Name-Wert-Paare in Form eines Ausdrucks.

-   [Blend-Zustand](#blend-state)
-   [Tiefen- und Schablonenzustand](#depth-and-stencil-state)
-   [Status des Rasterizers](#rasterizer-state)
-   [Samplerzustand](#sampler-state)
-   [Effect-Objektzustand](#effect-object-state)
-   [Definieren und Verwenden von Zustandsobjekten](#defining-and-using-state-objects)
-   [Verwandte Themen](#related-topics)

## <a name="blend-state"></a>Blend-Zustand



| Auswirkungszustand                                                                                                                      | Group                                                          |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| ALPHATOCOVERAGEENABLEBLENDENABLESRCBLENDDESTBLENDBLENDOP SRCBLENDALPHADESTBLENDALPHABLENDOPALPHARENDERTARGETWRITEMASK | Elemente von [ **D3D11 \_ BLEND \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc) |



 

## <a name="depth-and-stencil-state"></a>Tiefen- und Schablonenzustand



|  Auswirkungszustand                                                                                                                                                              | Group                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| DEPTHENABLEDEPTHWRITEMASKDEPTHFUNCSTENCILENABLESTENCILREADMASKSTENCILWRITEMASK                                                                                 | Elemente von [ **D3D11 \_ DEPTH \_ STENCIL \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)    |
| FRONTFACESTENCILFAILFRONTFACESTENCILZFAILFRONTFACESTENCILPASSFRONTFACESTENCILFUNCBACKFACESTENCILFAILBACKFACESTENCILZFAILBACKFACESTENCILPASSBACKFACESTENCILFUNC | Member von [ **D3D11 \_ DEPTH \_ STENCILOP \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencilop_desc) |



 

## <a name="rasterizer-state"></a>Rasterizerstatus



| Auswirkungszustand                                                                                                                                | Group                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| Fillmode                                                                                                                        | [**\_ \_ D3D11-FÜLLMODUS**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_fill_mode)                        |
| CULLMODE                                                                                                                        | [**D3D11 \_ \_ CULL-MODUS**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cull_mode)                        |
| FRONTCOUNTERCLOCKWISEDEPTHBIASDEPTHBIASCLAMPSSCALEDDEPTHBIAS ZCLIPENABLESCISSORENABLEMULTISAMPLEENABLEANTIALIASEDLINEENABLE | Member von [ **D3D11 \_ RASTERIZER \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_rasterizer_desc) |



 

## <a name="sampler-state"></a>Samplerstatus



| Auswirkungszustand                                                                                                    | Group                                                              |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| Filter AddressU AddressV AddressW MipLODBias MaxAnisotropy ComparisonFunc BorderColor MinLOD MaxLOD | Member von [ **D3D11 \_ SAMPLER \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_sampler_desc) |



 

Beispiele finden Sie unter [Sampler Type (DirectX HLSL) (Sampler-Typ (DirectX HLSL)).](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-sampler)

## <a name="effect-object-state"></a>Effect-Objektzustand



| Dieses Effect-Objekt                          | Entsprechung                                                             |
|---------------------------------------------|---------------------------------------------------------------------|
| RASTERIZERSTATE                             | Ein [Zustandsobjekt des Rasterizerzustands.](#rasterizer-state)               |
| DEPTHSTENCILSTATE                           | Ein [Tiefen- und Schablonenzustandsobjekt.](#depth-and-stencil-state) |
| BLENDSTATE                                  | Ein [Blend State-Zustandsobjekt.](#blend-state)                         |
| VERTEXSHADER                                | Ein kompiliertes Vertex-Shaderobjekt.                                    |
| Pixelshader                                 | Ein kompiliertes Pixel-Shaderobjekt.                                     |
| GEOMETRYSHADER                              | Ein kompiliertes Geometrie-Shaderobjekt.                                  |
| DS \_ STENCILREFAB \_ BLENDFACTORAB \_ SAMPLEMASK | Member von [**D3DX11 \_ PASS \_ DESC**](d3dx11-pass-desc.md).          |



 

## <a name="defining-and-using-state-objects"></a>Definieren und Verwenden von Zustandsobjekten

Zustandsobjekte werden in FX-Dateien im folgenden Format deklariert. StateObjectType ist einer der oben aufgeführten Zustände, und MemberName ist der Name jedes Mitglieds, das einen nicht standardmäßigen Wert hat.


```
StateObjectType ObjectName {
  MemberName = value;
  ...
  MemberName = value;
};
    
```



Wenn Sie beispielsweise ein Blend-Zustandsobjekt einrichten möchten, bei dem AlphaToCoverageEnable und BlendEnable 0 auf FALSE festgelegt sind, wird der folgende \[ \] Code verwendet. 


```
BlendState NoBlend {
  AlphaToCoverageEnable = FALSE;
  BlendEnable[0] = FALSE;
};
    
```



Das Zustandsobjekt wird mithilfe einer der Unter Effect [Technique Syntax (Direct3D 11)](d3d11-effect-technique-syntax.md)beschriebenen SetStateGroup-Funktionen auf einen Technikpass angewendet. Um beispielsweise das oben beschriebene BlendState-Objekt anzuwenden, wird der folgende Code verwendet.


```
SetBlendState( NoBlend, float4( 0.0f, 0.0f, 0.0f, 0.0f ), 0xFFFFFFFF );
    
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Syntax der Effekttechnik](d3d11-effect-technique-syntax.md)
</dt> <dt>

[Effect-Format (Direct3D 11)](d3d11-effect-format.md)
</dt> </dl>

 

 