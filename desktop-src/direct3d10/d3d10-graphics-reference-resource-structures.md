---
description: Strukturen, die zum Erstellen und Verwenden von Ressourcen verwendet werden.
ms.assetid: d8fe2ebe-349a-456e-9a5a-16f2d3419800
title: Ressourcen Strukturen (Direct3D 10-Grafiken)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4da964bf19c1ce5e1e5c4dfd0685df79b28ac5e3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342755"
---
# <a name="resource-structures-direct3d-10-graphics"></a>Ressourcen Strukturen (Direct3D 10-Grafiken)

Strukturen, die zum Erstellen und Verwenden von [Ressourcen](d3d10-graphics-programming-guide-resources-types.md)verwendet werden.



| Strukturen                                                                 | BESCHREIBUNG                                                                                                                                                   |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**D3d10- \_ Puffer \_**](/windows/desktop/api/D3D10/ns-d3d10-cd3d10_buffer_desc)                           | Die Beschreibung einer [Puffer](d3d10-graphics-programming-guide-resources-types.md) Ressource.                                                                     |
| [**D3d10 \_ \_ -Puffer-RTV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_buffer_rtv)                             | Beschreibt die Elemente in einem [Puffer](d3d10-graphics-programming-guide-resources-types.md) , die in einer renderzielansicht verwendet werden sollen.                                |
| [**D3d10- \_ Puffer- \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_buffer_srv)                             | Beschreibt die Elemente in einer [Puffer](d3d10-graphics-programming-guide-resources-types.md) Ressource, die in einer Shader-Resource-Ansicht verwendet werden soll.                         |
| [**D3d10 \_ tiefen \_ Schablone \_ anzeigen \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_view_desc) | Beschreibt eine Ansicht der tiefen Schablone.                                                                                                                               |
| [**D3d10 \_ zugeordnet \_ TEXTURE2D**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_mapped_texture2d)                 | Ermöglicht den Zugriff auf unter Berichtsdaten in einer [2D-Textur](d3d10-graphics-programming-guide-resources-types.md).                                                  |
| [**D3d10 \_ zugeordnet \_ TEXTURE3D**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_mapped_texture3d)                 | Ermöglicht den Zugriff auf unter Berichtsdaten in einer [3D-Textur](d3d10-graphics-programming-guide-resources-types.md).                                                  |
| [**D3d10 \_ \_ \_ renderzielansicht \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_render_target_view_desc) | Beschreibt eine renderzielansicht.                                                                                                                               |
| [**D3d10 \_ subresource- \_ Daten**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_subresource_data)                 | Gibt Daten für die Initialisierung einer Ressource an.                                                                                                                   |
| [**D3d10 \_ TEX1D \_ array- \_ DSV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex1d_array_dsv)                  | Gibt an, welche MipMap-Ebene und Texturen in einem [1D-Textur Array](d3d10-graphics-programming-guide-resources-types.md) in einer Ansicht der tiefen Schablone verwendet werden sollen.       |
| [**D3d10 \_ TEX1D \_ array \_ -RTV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex1d_array_rtv)                  | Gibt die unter Ressourcen aus einem Array von [1D-Texturen](d3d10-graphics-programming-guide-resources-types.md) an, die in einer renderzielansicht verwendet werden sollen.             |
| [**D3d10 \_ TEX1D- \_ Array ( \_ SRV)**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex1d_array_srv)                  | Gibt die MipMap-Ebenen und Texturen in einem [1D-Textur Array](d3d10-graphics-programming-guide-resources-types.md) an, das in einer Shader-Resource-Ansicht verwendet werden soll.      |
| [**D3d10 \_ TEX1D \_ DSV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex1d_dsv)                               | Gibt die unter Ressourcen aus einer [1D-Textur](d3d10-graphics-programming-guide-resources-types.md) an, die in einer Ansicht der tiefen Schablone verwendet werden sollen.                        |
| [**D3d10 \_ TEX1D \_ RTV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex1d_rtv)                               | Gibt die unter Ressourcen aus einer [1D-Textur](d3d10-graphics-programming-guide-resources-types.md) an, die in einer renderzielansicht verwendet werden sollen.                        |
| [**D3d10 \_ TEX1D \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex1d_srv)                               | Gibt die unter Ressourcen aus einer [1D-Textur](d3d10-graphics-programming-guide-resources-types.md) an, die in einer Shader-Ressourcen Ansicht verwendet werden sollen.                      |
| [**D3d10 \_ TEX2D \_ array- \_ DSV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2d_array_dsv)                  | Gibt an, welche MipMap-Ebene und welche Texturen in einem [2D-Textur Array](d3d10-graphics-programming-guide-resources-types.md) in einer Ansicht der tiefen Schablone verwendet werden sollen. |
| [**D3d10 \_ TEX2D \_ array \_ -RTV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2d_array_rtv)                  | Gibt an, welche MipMap-Ebene und welche Texturen in einem [2D-Textur Array](d3d10-graphics-programming-guide-resources-types.md) in einer renderzielansicht verwendet werden sollen. |
| [**D3d10 \_ TEX2D- \_ Array ( \_ SRV)**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2d_array_srv)                  | Gibt die unter Ressourcen aus einem Array von [2D-Texturen](d3d10-graphics-programming-guide-resources-types.md) an, die in einer Shader-Ressourcen Ansicht verwendet werden sollen.           |
| [**D3d10 \_ TEX2D \_ DSV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2d_dsv)                               | Gibt die unter Ressourcen aus einer [2D-Textur](d3d10-graphics-programming-guide-resources-types.md) an, die in einer Ansicht der tiefen Schablone verwendet werden sollen.                        |
| [**D3d10 \_ TEX2D \_ RTV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2d_rtv)                               | Gibt die unter Ressourcen aus einer [2D-Textur](d3d10-graphics-programming-guide-resources-types.md) an, die in einer renderzielansicht verwendet werden sollen.                        |
| [**D3d10 \_ TEX2D \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2d_srv)                               | Gibt die unter Ressourcen aus einer [2D-Textur](d3d10-graphics-programming-guide-resources-types.md) an, die in einer Shader-Ressourcen Ansicht verwendet werden sollen.                      |
| [**D3d10 \_ TEX2DMS \_ array- \_ DSV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2dms_array_dsv)              | Gibt die unter Ressourcen aus einem Array von [2D-Texturen](d3d10-graphics-programming-guide-resources-types.md) an, die in einer tiefen Schablonen Ansicht verwendet werden sollen.             |
| [**D3d10 \_ TEX2DMS \_ array \_ -RTV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2dms_array_rtv)              | Gibt die unter Ressourcen aus einem Array von [2D-Texturen](d3d10-graphics-programming-guide-resources-types.md) an, die in einer renderzielansicht verwendet werden sollen.             |
| [**D3d10 \_ TEX2DMS- \_ Array ( \_ SRV)**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2dms_array_srv)              | Gibt die unter Ressourcen aus einem Array von [2D-Texturen](d3d10-graphics-programming-guide-resources-types.md) an, die in einer Shader-Ressourcen Ansicht verwendet werden sollen.           |
| [**D3d10 \_ TEX2DMS \_ DSV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2dms_dsv)                           | Gibt die unter Ressourcen aus einer Multisampling- [2D-Textur](d3d10-graphics-programming-guide-resources-types.md) an, die in einer tiefen Schablonen Ansicht verwendet werden soll.           |
| [**D3d10 \_ TEX2DMS \_ RTV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2dms_rtv)                           | Gibt die unter Ressourcen aus einer Multisampling- [2D-Textur](d3d10-graphics-programming-guide-resources-types.md) an, die in einer renderzielansicht verwendet werden soll.           |
| [**D3d10 \_ TEX2DMS \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2dms_srv)                           | Gibt die unter Ressourcen aus einer Multisampling- [2D-Textur](d3d10-graphics-programming-guide-resources-types.md) an, die in einer Shader-Resource-Ansicht verwendet werden soll.         |
| [**D3d10 \_ TEX3D \_ RTV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex3d_rtv)                               | Gibt die unter Ressourcen aus einer [3D-Textur](d3d10-graphics-programming-guide-resources-types.md) an, die in einer renderzielansicht verwendet werden sollen.                        |
| [**D3d10 \_ TEX3D \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex3d_srv)                               | Gibt die unter Ressourcen aus einer [3D-Textur](d3d10-graphics-programming-guide-resources-types.md) an, die in einer Shader-Ressourcen Ansicht verwendet werden sollen.                      |
| [**D3d10 \_ Texcube- \_ array \_ SRV1**](/windows/desktop/api/d3d10_1/ns-d3d10_1-d3d10_texcube_array_srv1)            | Gibt die unter Ressourcen aus einer [cubetextur](d3d10-graphics-programming-guide-resources-types.md) an, die in einer Shader-Ressourcen Ansicht verwendet werden sollen.                    |
| [**D3d10 \_ Texcube- \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_texcube_srv)                           | Gibt die unter Ressourcen aus einer [cubetextur](d3d10-graphics-programming-guide-resources-types.md) an, die in einer Shader-Ressourcen Ansicht verwendet werden sollen.                    |
| [**D3d10 \_ TEXTURE1D- \_ Abteilung**](/windows/desktop/api/D3D10/ns-d3d10-cd3d10_texture1d_desc)                     | Beschreibt eine [1D-Textur](d3d10-graphics-programming-guide-resources-types.md) Ressource.                                                                      |
| [**D3d10 \_ TEXTURE2D- \_ Abteilung**](/windows/desktop/api/D3D10/ns-d3d10-cd3d10_texture2d_desc)                     | Beschreibt eine [2D-Textur](d3d10-graphics-programming-guide-resources-types.md) Ressource.                                                                      |
| [**D3d10 \_ TEXTURE3D- \_ Abteilung**](/windows/desktop/api/D3D10/ns-d3d10-cd3d10_texture3d_desc)                     | Beschreibt eine [3D-Textur](d3d10-graphics-programming-guide-resources-types.md) Ressource.                                                                      |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ressourcen Verweis](d3d10-graphics-reference-resource.md)
</dt> </dl>

 

 



