---
title: Effekt Zustands Gruppen (Direct3D 11)
description: Effekt Zustände sind Name-Wert-Paare in Form eines Ausdrucks.
ms.assetid: 87883483-4fa6-4362-807e-53b79b7d1370
keywords:
- Auswirkung, Zustands Gruppen (Direct3D 11)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58def71b6362706eb831129b1d222ef3d1cc9341
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948768"
---
# <a name="effect-state-groups-direct3d-11"></a>Effekt Zustands Gruppen (Direct3D 11)

Effekt Zustände sind Name-Wert-Paare in Form eines Ausdrucks.

-   [Blend-Status](#blend-state)
-   [Tiefen-und Schablonen Zustand](#depth-and-stencil-state)
-   [Status des Rasterizers](#rasterizer-state)
-   [Samplerstatus](#sampler-state)
-   [Effekt Objektstatus](#effect-object-state)
-   [Definieren und Verwenden von Zustands Objekten](#defining-and-using-state-objects)
-   [Zugehörige Themen](#related-topics)

## <a name="blend-state"></a>Blend-Status



|                                                                                                                       |                                                           |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| Alpha atocoverageenableblendenablesrcblenddestblendblendop srcblendalphadestblendalphablendopalpharendertargetwrite temask | Mitglieder von [ **D3D11 \_ Blend- \_ ABSC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc) |



 

## <a name="depth-and-stencil-state"></a>Tiefen-und Schablonen Zustand



|                                                                                                                                                                |                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| Depthenabledepthschreitemaskdepthfuncstencilenablestencilsynchmaskstencilschreitemask                                                                                 | Mitglieder der [ **D3D11- \_ tiefen \_ Schablone \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)    |
| Frontfakestincilfailfrontfakestincilzfailfrontfabackfakestincilfailbackfakestincilzfailbackfakestbeiendestinfazfailbackfac | Mitglied von [ **D3D11 \_ tiefen \_ Schablone (encilop \_** )](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencilop_desc) |



 

## <a name="rasterizer-state"></a>Status des Rasterizers



|                                                                                                                                 |                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| FillMode                                                                                                                        | [**D3D11 \_ Füll \_ Modus**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_fill_mode)                        |
| CullMode                                                                                                                        | [**D3D11- \_ cull- \_ Modus**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cull_mode)                        |
| frontcounterclockwisedepthbiasdepthbiasklamslopescaleddepthbias zclipenablescissorenablemultisampleenableantialiasedlineenable | Mitglieder des [ **D3D11 \_ Rasterizer \_** -Moduls](/windows/desktop/api/D3D11/ns-d3d11-d3d11_rasterizer_desc) |



 

## <a name="sampler-state"></a>Samplerstatus



|                                                                                                     |                                                               |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| Filter adressu adressensu adressu adressw miplodbias MaxAnisotropy comparisonfunc BorderColor minlod maxlod | Mitglieder des [ **D3D11 \_ - \_ samplerentsc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_sampler_desc) |



 

Beispiele hierfür finden Sie unter [Sampler Type (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-sampler) .

## <a name="effect-object-state"></a>Effekt Objektstatus



| This Effect-Objekt                          | Entsprechung                                                             |
|---------------------------------------------|---------------------------------------------------------------------|
| Rasterizerstate                             | Ein [Rasterizer State](#rasterizer-state) State-Objekt.               |
| Depthstencilstate                           | Ein [tiefen-und Schablonen Zustands](#depth-and-stencil-state) Objekt. |
| Blendstate                                  | Ein [Blend](#blend-state) -Zustands Objekt.                         |
| Titellink                                | Ein kompiliertes Vertex-Shader-Objekt.                                    |
| Pixelshader                                 | Ein kompiliertes Pixel-Shader-Objekt.                                     |
| Geometryshader                              | Ein kompiliertes Geometry-Shader-Objekt.                                  |
| DS \_ stencilrefab \_ blendfactor ab \_ samplemask | Mitglieder von [**Bibliothek d3dx11 \_ Pass \_**](d3dx11-pass-desc.md)(Debug).          |



 

## <a name="defining-and-using-state-objects"></a>Definieren und Verwenden von Zustands Objekten

Zustands Objekte werden in FX-Dateien im folgenden Format deklariert. Stateobjecttype ist einer der oben aufgeführten Zustände und der Name eines beliebigen Members, der einen nicht standardmäßigen Wert hat.


```
StateObjectType ObjectName {
  MemberName = value;
  ...
  MemberName = value;
};
    
```



Wenn Sie z. b. ein Blend-Zustands Objekt mit Alpha atocoverageenable und blendenable \[ 0 \] auf **false** einrichten möchten, wird der folgende Code verwendet.


```
BlendState NoBlend {
  AlphaToCoverageEnable = FALSE;
  BlendEnable[0] = FALSE;
};
    
```



Das State-Objekt wird auf eine Technik Übergabe mithilfe einer der setstategroup-Funktionen angewendet, die unter [Effekt Technik Syntax (Direct3D 11)](d3d11-effect-technique-syntax.md)beschrieben werden. Wenn Sie z. b. das oben beschriebene blendstate-Objekt anwenden möchten, wird der folgende Code verwendet.


```
SetBlendState( NoBlend, float4( 0.0f, 0.0f, 0.0f, 0.0f ), 0xFFFFFFFF );
    
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Syntax der Effekt Technik](d3d11-effect-technique-syntax.md)
</dt> <dt>

[Effekt Format (Direct3D 11)](d3d11-effect-format.md)
</dt> </dl>

 

 