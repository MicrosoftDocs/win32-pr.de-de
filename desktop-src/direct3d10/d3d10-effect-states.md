---
description: Effektzustände sind Name-Wert-Paare in Form eines Ausdrucks.
ms.assetid: 4612c6bd-bc1f-42ad-8465-c0d4b577d1db
title: Effektzustandsgruppen (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4617f786b984c96b271600e05b3ea8da9b5701fd
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335569"
---
# <a name="effect-state-groups-direct3d-10"></a>Effektzustandsgruppen (Direct3D 10)

Effektzustände sind Name-Wert-Paare in Form eines Ausdrucks.

## <a name="blend-state"></a>Überblenden des Zustands

| Auswirkungszustand | Group |
|-|-|
| **ALPHATOCOVERAGEENABLE**, **BLENDENABLE**, **SRCBLEND**, **DESTBLEND**, **BLENDOP**, **SRCBLENDALPHA**, **DESTBLENDALPHA**, **BLENDOPALPHA**, **RENDERTARGETWRITEMASK** | Elemente von [ **D3D10 \_ BLEND \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc) |

## <a name="depth-and-stencil-state"></a>Tiefen- und Schablonenzustand

| Auswirkungszustand| Group |
|-|-|
| **DEPTHENABLE**, **DEPTHWRITEMASK**, **DEPTHFUNC**, **STENCILENABLE**, **STENCILREADMASK**, **STENCILWRITEMASK** | Elemente der [ **D3D10 \_ \_ DEPTH-SCHABLONE \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc) |
| **FRONTFACESTENCILFAIL**, **FRONTFACESTENCILZFAIL**, **FRONTFACESTENCILPASS**, **FRONTFACESTENCILFUNC**, **BACKFACESTENCILFAIL**, **BACKFACESTENCILZFAIL**, **BACKFACESTENCILPASS**, **BACKFACESTENCILFUNC** | Member von [ **D3D10 \_ DEPTH \_ STENCILOP \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencilop_desc) |

## <a name="rasterizer-state"></a>Status des Rasterizers

| Auswirkungszustand| Group |
|-|-|
| Fillmode | [**FÜLLMODUS D3D10 \_ \_**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_fill_mode) |
| CULLMODE | [**D3D10 \_ \_ CULL-MODUS**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cull_mode) |
| **FRONTCOUNTERCLOCKWISE**, **DEPTHBIAS**, **DEPTHBIASCLAMP**, **VERSKALIERTDEPTHBIAS**, **ZCLIPENABLE**, **SCISSORENABLE**, **MULTISAMPLEENABLE**, **ANTIALIASEDLINEENABLE** | Elemente von [ **D3D10 \_ RASTERIZER \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc) |

## <a name="sampler-state"></a>Samplerzustand

| Auswirkungszustand | Group |
|-|-|
| **Filter**, **AddressU**, **AddressV**, **AddressW**, **MipLODBias**, **MaxAnisotropy**, **ComparisonFunc**, **BorderColor**, **MinLOD**, **MaxLOD** | Member von [ **D3D10 \_ SAMPLER \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_sampler_desc) |

Beispiele finden Sie unter [Sampler type (DirectX HLSL) (Samplertyp (DirectX HLSL)).](../direct3dhlsl/dx-graphics-hlsl-sampler.md)

## <a name="effect-object-state"></a>Effect-Objektzustand

| Dieses Effektobjekt | Entsprechung |
|-|-|
| RASTERIZERSTATE | Ein [Zustandsobjekt des Rasterizerzustands.](#rasterizer-state) |
| DEPTHSTENCILSTATE | Ein [Tiefen- und Schablonenzustandsobjekt.](#depth-and-stencil-state) |
| BLENDSTATE | Ein [Blend State State-Objekt.](#blend-state) |
| VERTEXSHADER | Ein kompiliertes Vertex-Shaderobjekt. |
| Pixelshader | Ein kompiliertes Pixelshaderobjekt. |
| GEOMETRYSHADER | Ein kompiliertes geometry-Shaderobjekt. |
| DS \_ STENCILREF AB \_ BLENDFACTOR AB \_ SAMPLEMASK | Member von [**D3D10 \_ PASS \_ DESC**](/windows/desktop/api/d3d10effect/ns-d3d10effect-d3d10_pass_desc). |

## <a name="defining-and-using-state-objects"></a>Definieren und Verwenden von Zustandsobjekten

Zustandsobjekte werden in FX-Dateien im folgenden Format deklariert. *StateObjectType* ist einer der oben aufgeführten Zustände, und *MemberName* ist der Name jedes Mitglieds, das einen nicht standardmäßigen Wert hat.

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

Das Zustandsobjekt wird mithilfe einer der SetStateGroup-Funktionen, die unter [Effect Technique Syntax (Direct3D 10)](d3d10-effect-technique-syntax.md)beschrieben sind, auf einen Technikpass angewendet. Um beispielsweise das oben beschriebene BlendState-Objekt anzuwenden, wird der folgende Code verwendet.

```
SetBlendState( NoBlend, float4( 0.0f, 0.0f, 0.0f, 0.0f ), 0xFFFFFFFF );
```

Ein Tutorial, in dem die Verwendung von Status beschrieben wird, finden Sie [unter Zustandsverwaltung.](https://msdn.microsoft.com/library/Ee416550(v=VS.85).aspx)

## <a name="related-topics"></a>Zugehörige Themen

* [Syntax der Effekttechnik](d3d10-effect-technique-syntax.md)
* [Effect-Format (Direct3D 10)](d3d10-effect-format.md)
