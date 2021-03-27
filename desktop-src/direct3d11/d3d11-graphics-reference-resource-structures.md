---
title: Ressourcen Strukturen (Direct3D 11-Grafiken)
description: Strukturen werden verwendet, um Ressourcen zu erstellen und zu verwenden.
ms.assetid: a29e01ac-8aa1-4a40-ad4d-3b738e129436
keywords:
- Strukturen, Direct3D 11-Ressource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5020792e1fb56a52e7a4354964c45bb5d65bbba4
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "103858612"
---
# <a name="resource-structures-direct3d-11-graphics"></a>Ressourcen Strukturen (Direct3D 11-Grafiken)

Strukturen werden verwendet, um Ressourcen zu erstellen und zu verwenden.


## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                         | BESCHREIBUNG                                                                                                       |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [**D3D11- \_ Puffer \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc)<br/>                                   | Beschreibt eine Puffer Ressource.<br/>                                                                           |
| [**D3D11 \_ \_ -Puffer-RTV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_rtv)<br/>                                     | Gibt die Elemente in einer Puffer Ressource an, die in einer renderzielansicht verwendet werden sollen.<br/>                            |
| [**D3D11- \_ Puffer- \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_srv)<br/>                                     | Gibt die Elemente in einer Puffer Ressource an, die in einer Shader-Ressourcen Ansicht verwendet werden sollen.<br/>                          |
| [**D3D11- \_ Puffer- \_ UAV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_uav)<br/>                                     | Beschreibt die Elemente in einem Puffer, die in einer Ansicht mit ungeordneten Zugriffen verwendet werden sollen.<br/>                                  |
| [**D3D11 \_ bufferex \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_bufferex_srv)<br/>                                 | Beschreibt die Elemente in einer rohpuffer Ressource, die in einer Shader-Resource-Ansicht verwendet werden soll.<br/>                      |
| [**D3D11 \_ tiefen \_ Schablone \_ anzeigen \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_view_desc)<br/>         | Gibt die unter Ressourcen einer Textur an, auf die von einer Ansicht der tiefen Schablone aus zugegriffen werden kann.<br/>                 |
| [**D3D11 zugeordnete unter \_ \_ geordnete Quelle**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_mapped_subresource)<br/>                     | Bietet Zugriff auf die Daten der untergeordneten Quelle.<br/>                                                                   |
| [**D3D11- \_ gepackte \_ MIP- \_ Abteilung**](/windows/desktop/api/d3d11_2/ns-d3d11_2-d3d11_packed_mip_desc)<br/>                          | Beschreibt die Kachel Struktur einer gekachelten Ressource mit Mipmaps. <br/>                                        |
| [**D3D11 \_ \_ \_ renderzielansicht \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_render_target_view_desc)<br/>         | Gibt die unter Ressourcen aus einer Ressource an, auf die über eine renderzielsicht zugegriffen werden kann.<br/>             |
| [**D3D11 \_ \_ \_ renderzielsicht \_ DESC1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_render_target_view_desc1)<br/>       | Beschreibt die unter Ressourcen aus einer Ressource, auf die über eine renderzielsicht zugegriffen werden kann.<br/>             |
| [**D3D11 \_ Shader- \_ Ressourcen \_ Ansicht \_ (Debug)**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_shader_resource_view_desc)<br/>     | Beschreibt eine Shader-Ressourcen Ansicht.<br/>                                                                      |
| [**D3D11- \_ Shader- \_ Ressourcen \_ Ansicht \_ DESC1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_shader_resource_view_desc1)<br/>   | Beschreibt eine Shader-Ressourcen Ansicht.<br/>                                                                      |
| [**D3D11 \_ subresource- \_ Daten**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data)<br/>                         | Gibt Daten für die Initialisierung eines unter Berichts an.<br/>                                                         |
| [**D3D11-unter \_ geordnete \_ tiult**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_subresource_tiling)<br/>                     | Beschreibt ein gespeichertes unter Quell Volume.<br/>                                                                  |
| [**D3D11 \_ TEX1D \_ array- \_ DSV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_array_dsv)<br/>                          | Gibt die unter Ressourcen aus einem Array von 1D-Texturen an, die in einer tiefen Schablonen Ansicht verwendet werden sollen.<br/>                |
| [**D3D11 \_ TEX1D \_ array \_ -RTV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_array_rtv)<br/>                          | Gibt die unter Ressourcen aus einem Array von 1D-Texturen an, die in einer renderzielansicht verwendet werden sollen.<br/>                |
| [**D3D11 \_ TEX1D- \_ Array ( \_ SRV)**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_array_srv)<br/>                          | Gibt die unter Ressourcen aus einem Array von 1D-Texturen an, die in einer Shader-Ressourcen Ansicht verwendet werden sollen.<br/>              |
| [**D3D11 \_ TEX1D \_ array- \_ UAV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_array_uav)<br/>                          | Beschreibt ein Array von 1D-Textur Ressourcen ohne geordneter Zugriff.<br/>                                           |
| [**D3D11 \_ TEX1D \_ DSV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_dsv)<br/>                                       | Gibt die untergeordnete Quelle aus einer 1D-Textur an, auf die eine Ansicht der tiefen Schablone zugreifen kann.<br/>                |
| [**D3D11 \_ TEX1D \_ RTV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_rtv)<br/>                                       | Gibt die untergeordnete Quelle aus einer 1D-Textur an, die in einer renderzielansicht verwendet werden soll.<br/>                            |
| [**D3D11 \_ TEX1D \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_srv)<br/>                                       | Gibt die untergeordnete Quelle aus einer 1D-Textur an, die in einer Shader-Resource-Ansicht verwendet werden soll.<br/>                          |
| [**D3D11 \_ TEX1D \_ UAV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_uav)<br/>                                       | Beschreibt eine nicht geordnete Access-1D-Textur Ressource.<br/>                                                      |
| [**D3D11 \_ TEX2D \_ array- \_ DSV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_array_dsv)<br/>                          | Gibt die unter Ressourcen aus einem 2D-Array Array an, auf das eine Ansicht der tiefen Schablone zugreifen kann.<br/>      |
| [**D3D11 \_ TEX2D \_ array \_ -RTV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_array_rtv)<br/>                          | Gibt die unter Ressourcen aus einem Array von 2D-Texturen an, die in einer renderzielansicht verwendet werden sollen.<br/>                |
| [**D3D11 \_ TEX2D \_ array \_ RTV1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-d3d11_tex2d_array_rtv1)<br/>                        | Beschreibt die unter Ressourcen aus einem Array von 2D-Texturen, die in einer renderzielansicht verwendet werden sollen.<br/>                |
| [**D3D11 \_ TEX2D- \_ Array ( \_ SRV)**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_array_srv)<br/>                          | Gibt die unter Ressourcen aus einem Array von 2D-Texturen an, die in einer Shader-Ressourcen Ansicht verwendet werden sollen.<br/>              |
| [**D3D11 \_ TEX2D \_ array \_ SRV1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-d3d11_tex2d_array_srv1)<br/>                        | Beschreibt die unter Ressourcen aus einem Array von 2D-Texturen, die in einer Shader-Resource-Ansicht verwendet werden sollen.<br/>              |
| [**D3D11 \_ TEX2D \_ array- \_ UAV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_array_uav)<br/>                          | Beschreibt ein Array von 2D-Textur Ressourcen ohne geordneter Zugriff.<br/>                                           |
| [**D3D11 \_ TEX2D \_ array \_ UAV1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-d3d11_tex2d_array_uav1)<br/>                        | Beschreibt ein Array von 2D-Textur Ressourcen ohne geordneter Zugriff.<br/>                                           |
| [**D3D11 \_ TEX2D \_ DSV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_dsv)<br/>                                       | Gibt die untergeordnete Quelle aus einer 2D-Textur an, auf die eine Ansicht der tiefen Schablone zugreifen kann.<br/>                |
| [**D3D11 \_ TEX2D \_ RTV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_rtv)<br/>                                       | Gibt die untergeordnete Quelle aus einer 2D-Textur an, die in einer renderzielansicht verwendet werden soll.<br/>                            |
| [**D3D11 \_ TEX2D \_ RTV1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-d3d11_tex2d_rtv1)<br/>                                     | Beschreibt die unter Berichte aus einer 2D-Textur, die in einer renderzielansicht verwendet werden soll.<br/>                            |
| [**D3D11 \_ TEX2D \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_srv)<br/>                                       | Gibt die untergeordnete Quelle aus einer 2D-Textur an, die in einer Shader-Resource-Ansicht verwendet werden soll.<br/>                          |
| [**D3D11 \_ TEX2D \_ SRV1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-d3d11_tex2d_srv1)<br/>                                     | Beschreibt die unter Berichte aus einer 2D-Textur, die in einer Shader-Resource-Ansicht verwendet werden soll.<br/>                          |
| [**D3D11 \_ TEX2D \_ UAV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_uav)<br/>                                       | Beschreibt eine 2D-Textur Ressource mit ungeordneter Zugriffsberechtigung.<br/>                                                      |
| [**D3D11 \_ TEX2D \_ UAV1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-d3d11_tex2d_uav1)<br/>                                     | Beschreibt eine 2D-Textur Ressource mit ungeordneter Zugriffsberechtigung.<br/>                                                      |
| [**D3D11 \_ TEX2DMS \_ array- \_ DSV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2dms_array_dsv)<br/>                      | Gibt die unter Ressourcen aus einem Array von Multisampling-2D-Texturen für eine Ansicht der tiefen Schablone an.<br/>         |
| [**D3D11 \_ TEX2DMS \_ array \_ -RTV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2dms_array_rtv)<br/>                      | Gibt die unter Ressourcen aus einem Array von Multisampling-2D-Texturen an, die in einer renderzielansicht verwendet werden sollen.<br/> |
| [**D3D11 \_ TEX2DMS- \_ Array ( \_ SRV)**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2dms_array_srv)<br/>                      | Gibt die unter Ressourcen aus einem Array von Multisampling-2D-Texturen an, die in einer Shader-Resource-Ansicht verwendet werden sollen.<br/> |
| [**D3D11 \_ TEX2DMS \_ DSV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2dms_dsv)<br/>                                   | Gibt die untergeordnete Quelle aus einer Multisampling-2D-Textur an, auf die eine Ansicht der tiefen Schablone zugreifen kann.<br/>   |
| [**D3D11 \_ TEX2DMS \_ RTV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2dms_rtv)<br/>                                   | Gibt die untergeordnete Quelle aus einer Multisampling-2D-Textur an, die in einer renderzielansicht verwendet werden soll.<br/>               |
| [**D3D11 \_ TEX2DMS \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2dms_srv)<br/>                                   | Gibt die unter Ressourcen aus einer Multisampling-2D-Textur an, die in einer Shader-Resource-Ansicht verwendet werden soll.<br/>            |
| [**D3D11 \_ TEX3D \_ RTV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex3d_rtv)<br/>                                       | Gibt die unter Ressourcen aus einer 3D-Textur an, die in einer renderzielansicht verwendet werden soll.<br/>                           |
| [**D3D11 \_ TEX3D \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex3d_srv)<br/>                                       | Gibt die unter Ressourcen aus einer 3D-Textur an, die in einer Shader-Resource-Ansicht verwendet werden soll.<br/>                         |
| [**D3D11 \_ TEX3D \_ UAV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex3d_uav)<br/>                                       | Beschreibt eine 3D-Textur Ressource mit ungeordneter Zugriffsberechtigung.<br/>                                                      |
| [**D3D11 \_ Texcube- \_ array \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texcube_array_srv)<br/>                      | Gibt die unter Ressourcen aus einem Array von Cube-Texturen an, die in einer Shader-Ressourcen Ansicht verwendet werden sollen.<br/>            |
| [**D3D11 \_ Texcube- \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texcube_srv)<br/>                                   | Gibt die untergeordnete Quelle aus einer cubetextur an, die in einer Shader-Resource-Ansicht verwendet werden soll.<br/>                        |
| [**D3D11 \_ TEXTURE1D- \_ Abteilung**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture1d_desc)<br/>                             | Beschreibt eine 1D-Textur.<br/>                                                                                |
| [**D3D11 \_ TEXTURE2D- \_ Abteilung**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc)<br/>                             | Beschreibt eine 2D-Textur.<br/>                                                                                |
| [**D3D11 \_ TEXTURE2D \_ DESC1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_texture2d_desc1)<br/>                           | Beschreibt eine 2D-Textur.<br/>                                                                                |
| [**D3D11 \_ TEXTURE3D- \_ Abteilung**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture3d_desc)<br/>                             | Beschreibt eine 3D-Textur.<br/>                                                                                |
| [**D3D11 \_ TEXTURE3D \_ DESC1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_texture3d_desc1)<br/>                           | Beschreibt eine 3D-Textur.<br/>                                                                                |
| [**D3D11 \_ Tile- \_ Regions \_ Größe**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_region_size)<br/>                        | Beschreibt die Größe eines gekachelten Bereichs.<br/>                                                                  |
| [**D3D11 \_ gekachelte \_ Ressourcen \_ Koordinate**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tiled_resource_coordinate)<br/>      | Beschreibt die Koordinaten einer gekachelten Ressource.<br/>                                                         |
| [**D3D11- \_ Kachel \_ Form**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_shape)<br/>                                     | Beschreibt die Form einer Kachel durch Angeben der Abmessungen.<br/>                                            |
| [**D3D11 \_ unsortierter \_ \_ Zugriffsansicht \_ Deaktivieren**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_unordered_access_view_desc)<br/>   | Gibt die unter Ressourcen aus einer Ressource an, auf die mithilfe einer Ansicht für ungeordneten Zugriff zugegriffen werden kann.<br/>         |
| [**D3D11 \_ unsortierter \_ Zugriffs \_ Ansicht \_ DESC1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_unordered_access_view_desc1)<br/> | Beschreibt die unter Ressourcen aus einer Ressource, auf die mithilfe einer Ansicht für ungeordneten Zugriff zugegriffen werden kann.<br/>         |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ressourcen Verweis](d3d11-graphics-reference-resource.md)
</dt> </dl>

 

 





