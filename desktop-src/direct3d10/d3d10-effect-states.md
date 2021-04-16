---
description: Effekt Zustände sind Name-Wert-Paare in Form eines Ausdrucks.
ms.assetid: 4612c6bd-bc1f-42ad-8465-c0d4b577d1db
title: Effektzustandsgruppen (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c132db3a5258cbe3573ddc5103df8b3cbcf2085d
ms.sourcegitcommit: 628fda3e63fd1d513ce9a5f55be8bbc4af4b2a4b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104351739"
---
# <a name="effect-state-groups-direct3d-10"></a>Effektzustandsgruppen (Direct3D 10)

Effekt Zustände sind Name-Wert-Paare in Form eines Ausdrucks.

## <a name="blend-state"></a>Blend-Status

| | |
|-|-|
| **Alpha atocoverageenable**, **blendenable**, **srcblend**, **destblend**, **blendop**, **srcblendalpha**, **destblendalpha**, **blendopalpha**, **rendertargetschreitemask** | Mitglieder von [ **d3d10 \_ Blend- \_ ABSC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc) |

## <a name="depth-and-stencil-state"></a>Tiefen-und Schablonen Zustand

| | |
|-|-|
| **depthenable**, **depthwrite temask**, **depthfunc**, **stencilenable**, **stencilread Mask**, **stencilwrite temask** | Mitglieder der [ **d3d10- \_ tiefen \_ Schablone \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc) |
| frontfakesttcilfail * *, **frontfakestin cilzfail**, **frontfakesteincilpass**, **frontfakesteincilfunc**, **backfakestdcilfail**, **backfakesteincilzfail**, **backfakesteincilpass**, **backfakesteincilfunc** | Mitglied von [ **d3d10 \_ tiefen \_ Schablone (encilop \_** )](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencilop_desc) |

## <a name="rasterizer-state"></a>Status des Rasterizers

| | |
|-|-|
| FillMode | [**D3d10 \_ Füll \_ Modus**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_fill_mode) |
| CullMode | [**D3d10- \_ cull- \_ Modus**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cull_mode) |
| **frontcounter Uhrzeigersinn**, **depthbias**, **depthbiasclamp**, **slopescaleddepthbias**, **zclipenable**, **scissorenable**, **multisampleenable**, **antialiasedlineenable** | Mitglieder des [ **d3d10 \_ Rasterizer \_** -Moduls](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc) |

## <a name="sampler-state"></a>Samplerstatus

| | |
|-|-|
| **Filter**, **adressssu**, **adressssv**, **AddressW**, **miplodbias**, **MaxAnisotropy**, **comparisonfunc**, **BorderColor**, **minlod**, **maxlod** | Mitglieder des [ **d3d10 \_ - \_ samplerentsc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_sampler_desc) |

Beispiele hierfür finden Sie unter [Sampler Type (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-sampler.md) .

## <a name="effect-object-state"></a>Effekt Objektstatus

| This Effect-Objekt | Entsprechung |
|-|-|
| Rasterizerstate | Ein [Rasterizer State](#rasterizer-state) State-Objekt. |
| Depthstencilstate | Ein [tiefen-und Schablonen Zustands](#depth-and-stencil-state) Objekt. |
| Blendstate | Ein [Blend](#blend-state) -Zustands Objekt. |
| Titellink | Ein kompiliertes Vertex-Shader-Objekt. |
| Pixelshader | Ein kompiliertes Pixel-Shader-Objekt. |
| Geometryshader | Ein kompiliertes Geometry-Shader-Objekt. |
| DS \_ stencilref ab \_ blendfactor ab \_ samplemask | Mitglieder von [**d3d10 \_ Pass \_**](/windows/desktop/api/d3d10effect/ns-d3d10effect-d3d10_pass_desc)(Debug). |

## <a name="defining-and-using-state-objects"></a>Definieren und Verwenden von Zustands Objekten

Zustands Objekte werden in FX-Dateien im folgenden Format deklariert. *Stateobjecttype* ist einer der oben aufgeführten Zustände, und der *Member Name* ist der Name eines beliebigen Members, der einen nicht standardmäßigen Wert hat.

```
StateObjectType ObjectName {
 MemberName = value;
 ...
 MemberName = value;
};
```

Wenn Sie z. b. ein Blend-Zustands Objekt mit Alpha atocoverageenable und blendenable \[ 0 \] auf **false** festlegen möchten, wird der folgende Code verwendet.

```
BlendState NoBlend {
 AlphaToCoverageEnable = FALSE;
 BlendEnable[0] = FALSE;
};
```

Das State-Objekt wird auf eine Technik Übergabe mithilfe einer der setstategroup-Funktionen angewendet, die in der [Effekt Techniken-Syntax (Direct3D 10)](d3d10-effect-technique-syntax.md)beschrieben werden. Wenn Sie z. b. das oben beschriebene blendstate-Objekt anwenden möchten, wird der folgende Code verwendet.

```
SetBlendState( NoBlend, float4( 0.0f, 0.0f, 0.0f, 0.0f ), 0xFFFFFFFF );
```

Ein Tutorial, in dem die Verwendung von Zuständen beschrieben wird, finden Sie unter [Zustands Verwaltung](https://msdn.microsoft.com/library/Ee416550(v=VS.85).aspx).

## <a name="related-topics"></a>Zugehörige Themen

* [Syntax der Effekt Technik](d3d10-effect-technique-syntax.md)
* [Effekt Format (Direct3D 10)](d3d10-effect-format.md)
