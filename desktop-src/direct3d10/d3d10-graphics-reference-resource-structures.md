---
description: Strukturen, die zum Erstellen und Verwenden von Ressourcen verwendet werden.
ms.assetid: d8fe2ebe-349a-456e-9a5a-16f2d3419800
title: Ressourcenstrukturen (Direct3D 10-Grafiken)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5eb45ff5d77d7bb0417b54b88a4014e2a96f522d2e026c778efcd05d23f624bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635020"
---
# <a name="resource-structures-direct3d-10-graphics"></a>Ressourcenstrukturen (Direct3D 10-Grafiken)

Strukturen, die zum Erstellen und Verwenden von Ressourcen [verwendet werden.](d3d10-graphics-programming-guide-resources-types.md)



| Strukturen                                                                 | Beschreibung                                                                                                                                                   |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**D3D10 \_ BUFFER \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-cd3d10_buffer_desc)                           | Beschreibung einer [Pufferressource.](d3d10-graphics-programming-guide-resources-types.md)                                                                     |
| [**D3D10 \_ BUFFER \_ RTV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_buffer_rtv)                             | Beschreibt die Elemente in einem [Puffer, die](d3d10-graphics-programming-guide-resources-types.md) in einer Renderzielansicht verwendet werden sollen.                                |
| [**D3D10 \_ BUFFER \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_buffer_srv)                             | Beschreibt die Elemente in einer [Pufferressource,](d3d10-graphics-programming-guide-resources-types.md) die in einer Shaderressourcenansicht verwendet werden.                         |
| [**D3D10 \_ DEPTH \_ STENCIL \_ VIEW \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_view_desc) | Beschreibt eine Tiefen-Schablonenansicht.                                                                                                                               |
| [**D3D10 \_ MAPPED \_ TEXTURE2D**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_mapped_texture2d)                 | Ermöglicht den Zugriff auf Unterressourcendaten in einer [2D-Textur.](d3d10-graphics-programming-guide-resources-types.md)                                                  |
| [**D3D10 \_ MAPPED \_ TEXTURE3D**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_mapped_texture3d)                 | Ermöglicht den Zugriff auf Unterressourcendaten in einer [3D-Textur.](d3d10-graphics-programming-guide-resources-types.md)                                                  |
| [**D3D10 \_ RENDER \_ TARGET \_ VIEW \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_render_target_view_desc) | Beschreibt eine Renderzielansicht.                                                                                                                               |
| [**D3D10 \_ SUBRESOURCE \_ DATA**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_subresource_data)                 | Gibt Daten zum Initialisieren einer Ressource an.                                                                                                                   |
| [**D3D10 \_ TEX1D \_ ARRAY \_ DSV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex1d_array_dsv)                  | Gibt an, welche Mipmapebene und Texturen in einem [1D-Texturarray](d3d10-graphics-programming-guide-resources-types.md) in einer Tiefen-Schablonenansicht verwendet werden.       |
| [**D3D10 \_ TEX1D \_ ARRAY \_ RTV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex1d_array_rtv)                  | Gibt die Unterressourcen aus einem Array von [1D-Texturen](d3d10-graphics-programming-guide-resources-types.md) an, die in einer Renderzielansicht verwendet werden.             |
| [**D3D10 \_ TEX1D \_ ARRAY \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex1d_array_srv)                  | Gibt die Mipmapebenen und Texturen in einem [1D-Texturarray](d3d10-graphics-programming-guide-resources-types.md) an, das in einer Shaderressourcenansicht verwendet werden soll.      |
| [**D3D10 \_ TEX1D \_ DSV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex1d_dsv)                               | Gibt die Unterressourcen aus einer [1D-Textur](d3d10-graphics-programming-guide-resources-types.md) an, die in einer Tiefen-Schablonenansicht verwendet werden.                        |
| [**D3D10 \_ TEX1D \_ RTV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex1d_rtv)                               | Gibt die Unterressourcen aus einer [1D-Textur](d3d10-graphics-programming-guide-resources-types.md) an, die in einer Renderzielansicht verwendet werden soll.                        |
| [**D3D10 \_ TEX1D \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex1d_srv)                               | Gibt die Unterressourcen aus einer [1D-Textur](d3d10-graphics-programming-guide-resources-types.md) an, die in einer Shaderressourcenansicht verwendet werden.                      |
| [**D3D10 \_ TEX2D \_ ARRAY \_ DSV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2d_array_dsv)                  | Gibt an, welche mipmap-Ebene und welche Texturen in einem [2D-Texturarray](d3d10-graphics-programming-guide-resources-types.md) in einer Tiefen-Schablonenansicht verwendet werden. |
| [**D3D10 \_ TEX2D \_ ARRAY \_ RTV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2d_array_rtv)                  | Gibt an, welche mipmap-Ebene und welche Texturen in einem [2D-Texturarray](d3d10-graphics-programming-guide-resources-types.md) in einer Renderzielansicht verwendet werden. |
| [**D3D10 \_ TEX2D \_ ARRAY \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2d_array_srv)                  | Gibt die Unterressourcen aus einem Array von [2D-Texturen](d3d10-graphics-programming-guide-resources-types.md) an, die in einer Shaderressourcenansicht verwendet werden.           |
| [**D3D10 \_ TEX2D \_ DSV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2d_dsv)                               | Gibt die Unterressourcen aus einer [2D-Textur](d3d10-graphics-programming-guide-resources-types.md) an, die in einer Tiefen-Schablonenansicht verwendet werden.                        |
| [**D3D10 \_ TEX2D \_ RTV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2d_rtv)                               | Gibt die Unterressourcen aus einer [2D-Textur](d3d10-graphics-programming-guide-resources-types.md) an, die in einer Renderzielansicht verwendet werden.                        |
| [**D3D10 \_ TEX2D \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2d_srv)                               | Gibt die Unterressourcen aus einer [2D-Textur](d3d10-graphics-programming-guide-resources-types.md) an, die in einer Shaderressourcenansicht verwendet werden.                      |
| [**D3D10 \_ TEX2DMS \_ ARRAY \_ DSV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2dms_array_dsv)              | Gibt die Unterressourcen aus einem Array von [2D-Texturen](d3d10-graphics-programming-guide-resources-types.md) an, die in einer Tiefen-Schablonenansicht verwendet werden.             |
| [**D3D10 \_ TEX2DMS \_ ARRAY \_ RTV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2dms_array_rtv)              | Gibt die Unterressourcen aus einem Array von [2D-Texturen](d3d10-graphics-programming-guide-resources-types.md) an, die in einer Renderzielansicht verwendet werden.             |
| [**D3D10 \_ TEX2DMS \_ ARRAY \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2dms_array_srv)              | Gibt die Unterressourcen aus einem Array von [2D-Texturen](d3d10-graphics-programming-guide-resources-types.md) an, die in einer Shaderressourcenansicht verwendet werden.           |
| [**D3D10 \_ TEX2DMS \_ DSV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2dms_dsv)                           | Gibt die Unterressourcen aus einer [2D-Textur](d3d10-graphics-programming-guide-resources-types.md) mit mehrerenAmpeln an, die in einer Tiefen-Schablonenansicht verwendet werden.           |
| [**D3D10 \_ TEX2DMS \_ RTV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2dms_rtv)                           | Gibt die Unterressourcen aus einer [multisampled-2D-Textur](d3d10-graphics-programming-guide-resources-types.md) an, die in einer Renderzielansicht verwendet werden soll.           |
| [**D3D10 \_ TEX2DMS \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2dms_srv)                           | Gibt die Unterressourcen aus einer [multisampled-2D-Textur](d3d10-graphics-programming-guide-resources-types.md) an, die in einer Shaderressourcenansicht verwendet werden soll.         |
| [**D3D10 \_ TEX3D \_ RTV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex3d_rtv)                               | Gibt die Unterressourcen aus einer [3D-Textur](d3d10-graphics-programming-guide-resources-types.md) an, die in einer Renderzielansicht verwendet werden.                        |
| [**D3D10 \_ TEX3D \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex3d_srv)                               | Gibt die Unterressourcen aus einer [3D-Textur](d3d10-graphics-programming-guide-resources-types.md) an, die in einer Shaderressourcenansicht verwendet werden.                      |
| [**D3D10 \_ TEXCUBE \_ ARRAY \_ SRV1**](/windows/desktop/api/d3d10_1/ns-d3d10_1-d3d10_texcube_array_srv1)            | Gibt die Unterressourcen aus einer Cubetextur an, [die](d3d10-graphics-programming-guide-resources-types.md) in einer Shaderressourcenansicht verwendet werden sollen.                    |
| [**D3D10 \_ TEXCUBE \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_texcube_srv)                           | Gibt die Unterressourcen aus einer Cubetextur an, [die](d3d10-graphics-programming-guide-resources-types.md) in einer Shaderressourcenansicht verwendet werden sollen.                    |
| [**D3D10 \_ TEXTURE1D \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-cd3d10_texture1d_desc)                     | Beschreibt eine [1D-Texturressource.](d3d10-graphics-programming-guide-resources-types.md)                                                                      |
| [**D3D10 \_ TEXTURE2D \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-cd3d10_texture2d_desc)                     | Beschreibt eine [2D-Texturressource.](d3d10-graphics-programming-guide-resources-types.md)                                                                      |
| [**D3D10 \_ TEXTURE3D \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-cd3d10_texture3d_desc)                     | Beschreibt eine [3D-Texturressource.](d3d10-graphics-programming-guide-resources-types.md)                                                                      |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ressourcenreferenz](d3d10-graphics-reference-resource.md)
</dt> </dl>

 

 



