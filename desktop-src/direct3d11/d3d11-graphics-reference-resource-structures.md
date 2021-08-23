---
title: Ressourcenstrukturen (Direct3D 11-Grafiken)
description: Strukturen werden zum Erstellen und Verwenden von Ressourcen verwendet.
ms.assetid: a29e01ac-8aa1-4a40-ad4d-3b738e129436
keywords:
- strukturen, Direct3D 11-Ressource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acff7e10538910082dcd15220cb41a2ec360c24472837a569530f0b306313db3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119125124"
---
# <a name="resource-structures-direct3d-11-graphics"></a>Ressourcenstrukturen (Direct3D 11-Grafiken)

Strukturen werden zum Erstellen und Verwenden von Ressourcen verwendet.


## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                         | Beschreibung                                                                                                       |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [**D3D11 \_ BUFFER \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc)<br/>                                   | Beschreibt eine Pufferressource.<br/>                                                                           |
| [**D3D11 \_ BUFFER \_ RTV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_rtv)<br/>                                     | Gibt die Elemente in einer Pufferressource an, die in einer Renderzielansicht verwendet werden sollen.<br/>                            |
| [**D3D11 \_ BUFFER \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_srv)<br/>                                     | Gibt die Elemente in einer Pufferressource an, die in einer Shader-Ressourcenansicht verwendet werden sollen.<br/>                          |
| [**D3D11 \_ BUFFER \_ UAV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_uav)<br/>                                     | Beschreibt die Elemente in einem Puffer, die in einer Ansicht mit ungeordneten Zugriffen verwendet werden sollen.<br/>                                  |
| [**D3D11 \_ BUFFEREX \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_bufferex_srv)<br/>                                 | Beschreibt die Elemente in einer rohen Pufferressource, die in einer Shader-Ressourcenansicht verwendet werden soll.<br/>                      |
| [**D3D11 \_ \_ TIEFENSCHABLONENANSICHT \_ \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_view_desc)<br/>         | Gibt die Unterressourcen einer Textur an, auf die über eine Tiefenschablonenansicht zugegriffen werden kann.<br/>                 |
| [**ZUGEORDNETE \_ \_ D3D11-UNTERRESSOURCE**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_mapped_subresource)<br/>                     | Ermöglicht den Zugriff auf Unterressourcendaten.<br/>                                                                   |
| [**D3D11 \_ PACKED \_ MIP \_ DESC**](/windows/desktop/api/d3d11_2/ns-d3d11_2-d3d11_packed_mip_desc)<br/>                          | Beschreibt die Kachelstruktur einer gekachelten Ressource mit Mipmaps. <br/>                                        |
| [**D3D11 \_ \_ \_ RENDERZIELANSICHT \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_render_target_view_desc)<br/>         | Gibt die Unterressourcen einer Ressource an, auf die über eine Renderzielansicht zugegriffen werden kann.<br/>             |
| [**D3D11 \_ \_ \_ RENDERZIELANSICHT \_ DESC1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_render_target_view_desc1)<br/>       | Beschreibt die Unterressourcen einer Ressource, auf die über eine Renderzielansicht zugegriffen werden kann.<br/>             |
| [**D3D11 \_ \_ SHADER-RESSOURCENANSICHT \_ \_ DESC**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_shader_resource_view_desc)<br/>     | Beschreibt eine Shader-Ressourcenansicht.<br/>                                                                      |
| [**D3D11 \_ \_ SHADER-RESSOURCENANSICHT \_ \_ DESC1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_shader_resource_view_desc1)<br/>   | Beschreibt eine Shader-Ressourcenansicht.<br/>                                                                      |
| [**D3D11 \_ SUBRESOURCE \_ DATA**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data)<br/>                         | Gibt Daten zum Initialisieren einer Unterressource an.<br/>                                                         |
| [**D3D11 \_ SUBRESOURCE \_ TILING**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_subresource_tiling)<br/>                     | Beschreibt ein gekacheltes Unterressourcenvolume.<br/>                                                                  |
| [**D3D11 \_ TEX1D \_ ARRAY \_ DSV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_array_dsv)<br/>                          | Gibt die Unterressourcen aus einem Array von 1D-Texturen an, die in einer Tiefenschablonenansicht verwendet werden sollen.<br/>                |
| [**D3D11 \_ TEX1D \_ ARRAY \_ RTV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_array_rtv)<br/>                          | Gibt die Unterressourcen aus einem Array von 1D-Texturen an, die in einer Renderzielansicht verwendet werden sollen.<br/>                |
| [**D3D11 \_ TEX1D \_ ARRAY \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_array_srv)<br/>                          | Gibt die Unterressourcen aus einem Array von 1D-Texturen an, die in einer Shader-Ressourcenansicht verwendet werden sollen.<br/>              |
| [**D3D11 \_ TEX1D \_ ARRAY \_ UAV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_array_uav)<br/>                          | Beschreibt ein Array von 1D-Texturressourcen mit ungeordneten Zugriffen.<br/>                                           |
| [**D3D11 \_ TEX1D \_ DSV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_dsv)<br/>                                       | Gibt die Unterressource aus einer 1D-Textur an, auf die eine Tiefenschablonenansicht zugreifen kann.<br/>                |
| [**D3D11 \_ TEX1D \_ RTV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_rtv)<br/>                                       | Gibt die Unterressource aus einer 1D-Textur an, die in einer Renderzielansicht verwendet werden soll.<br/>                            |
| [**D3D11 \_ TEX1D \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_srv)<br/>                                       | Gibt die Unterressource aus einer 1D-Textur an, die in einer Shader-Ressourcenansicht verwendet werden soll.<br/>                          |
| [**D3D11 \_ TEX1D \_ UAV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_uav)<br/>                                       | Beschreibt eine 1D-Texturressource mit ungeordneten Zugriffen.<br/>                                                      |
| [**D3D11 \_ TEX2D \_ ARRAY \_ DSV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_array_dsv)<br/>                          | Gibt die Unterressourcen aus arraybasierten 2D-Texturen an, auf die eine Tiefenschablonenansicht zugreifen kann.<br/>      |
| [**D3D11 \_ TEX2D \_ ARRAY \_ RTV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_array_rtv)<br/>                          | Gibt die Unterressourcen aus einem Array von 2D-Texturen an, die in einer Renderzielansicht verwendet werden sollen.<br/>                |
| [**D3D11 \_ TEX2D \_ ARRAY \_ RTV1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-d3d11_tex2d_array_rtv1)<br/>                        | Beschreibt die Unterressourcen aus einem Array von 2D-Texturen, die in einer Renderzielansicht verwendet werden sollen.<br/>                |
| [**D3D11 \_ TEX2D \_ ARRAY \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_array_srv)<br/>                          | Gibt die Unterressourcen aus einem Array von 2D-Texturen an, die in einer Shader-Ressourcenansicht verwendet werden sollen.<br/>              |
| [**D3D11 \_ TEX2D \_ ARRAY \_ SRV1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-d3d11_tex2d_array_srv1)<br/>                        | Beschreibt die Unterressourcen aus einem Array von 2D-Texturen, die in einer Shader-Ressourcenansicht verwendet werden sollen.<br/>              |
| [**D3D11 \_ TEX2D \_ ARRAY \_ UAV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_array_uav)<br/>                          | Beschreibt ein Array von 2D-Texturressourcen mit ungeordneten Zugriffen.<br/>                                           |
| [**D3D11 \_ TEX2D \_ ARRAY \_ UAV1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-d3d11_tex2d_array_uav1)<br/>                        | Beschreibt ein Array von 2D-Texturressourcen mit ungeordneten Zugriffen.<br/>                                           |
| [**D3D11 \_ TEX2D \_ DSV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_dsv)<br/>                                       | Gibt die Unterressource aus einer 2D-Textur an, auf die eine Tiefenschablonenansicht zugreifen kann.<br/>                |
| [**D3D11 \_ TEX2D \_ RTV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_rtv)<br/>                                       | Gibt die Unterressource aus einer 2D-Textur an, die in einer Renderzielansicht verwendet werden soll.<br/>                            |
| [**D3D11 \_ TEX2D \_ RTV1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-d3d11_tex2d_rtv1)<br/>                                     | Beschreibt die Unterressource aus einer 2D-Textur, die in einer Renderzielansicht verwendet werden soll.<br/>                            |
| [**D3D11 \_ TEX2D \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_srv)<br/>                                       | Gibt die Unterressource aus einer 2D-Textur an, die in einer Shader-Ressourcenansicht verwendet werden soll.<br/>                          |
| [**D3D11 \_ TEX2D \_ SRV1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-d3d11_tex2d_srv1)<br/>                                     | Beschreibt die Unterressource aus einer 2D-Textur, die in einer Shader-Ressourcenansicht verwendet werden soll.<br/>                          |
| [**D3D11 \_ TEX2D \_ UAV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_uav)<br/>                                       | Beschreibt eine 2D-Texturressource mit ungeordneten Zugriffen.<br/>                                                      |
| [**D3D11 \_ TEX2D \_ UAV1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-d3d11_tex2d_uav1)<br/>                                     | Beschreibt eine 2D-Texturressource mit ungeordneten Zugriffen.<br/>                                                      |
| [**D3D11 \_ TEX2DMS \_ ARRAY \_ DSV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2dms_array_dsv)<br/>                      | Gibt die Unterressourcen aus einem Array von mehrsampigen 2D-Texturen für eine Tiefenschablonenansicht an.<br/>         |
| [**D3D11 \_ TEX2DMS \_ ARRAY \_ RTV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2dms_array_rtv)<br/>                      | Gibt die Unterressourcen aus einem Array von multisampled 2D-Texturen an, die in einer Renderzielansicht verwendet werden sollen.<br/> |
| [**D3D11 \_ TEX2DMS \_ ARRAY \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2dms_array_srv)<br/>                      | Gibt die Unterressourcen aus einem Array von multisampled 2D-Texturen an, die in einer Shader-Ressourcenansicht verwendet werden sollen.<br/> |
| [**D3D11 \_ TEX2DMS \_ DSV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2dms_dsv)<br/>                                   | Gibt die Unterressource aus einer mehrsampigen 2D-Textur an, auf die eine Tiefenschablonenansicht zugreifen kann.<br/>   |
| [**D3D11 \_ TEX2DMS \_ RTV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2dms_rtv)<br/>                                   | Gibt die Unterressource aus einer multisampled-2D-Textur an, die in einer Renderzielansicht verwendet werden soll.<br/>               |
| [**D3D11 \_ TEX2DMS \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2dms_srv)<br/>                                   | Gibt die Unterressourcen aus einer mehrsampigen 2D-Textur an, die in einer Shader-Ressourcenansicht verwendet werden soll.<br/>            |
| [**D3D11 \_ TEX3D \_ RTV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex3d_rtv)<br/>                                       | Gibt die Unterressourcen aus einer 3D-Textur an, die in einer Renderzielansicht verwendet werden sollen.<br/>                           |
| [**D3D11 \_ TEX3D \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex3d_srv)<br/>                                       | Gibt die Unterressourcen aus einer 3D-Textur an, die in einer Shader-Ressourcenansicht verwendet werden sollen.<br/>                         |
| [**D3D11 \_ TEX3D \_ UAV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex3d_uav)<br/>                                       | Beschreibt eine 3D-Texturressource mit ungeordneten Zugriffen.<br/>                                                      |
| [**D3D11 \_ TEXCUBE \_ ARRAY \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texcube_array_srv)<br/>                      | Gibt die Unterressourcen aus einem Array von Cubetexturen an, die in einer Shader-Ressourcenansicht verwendet werden sollen.<br/>            |
| [**D3D11 \_ TEXCUBE \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texcube_srv)<br/>                                   | Gibt die Unterressource aus einer Cubetextur an, die in einer Shaderressourcenansicht verwendet werden soll.<br/>                        |
| [**D3D11 \_ TEXTURE1D \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture1d_desc)<br/>                             | Beschreibt eine 1D-Textur.<br/>                                                                                |
| [**D3D11 \_ TEXTURE2D \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc)<br/>                             | Beschreibt eine 2D-Textur.<br/>                                                                                |
| [**D3D11 \_ TEXTURE2D \_ DESC1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_texture2d_desc1)<br/>                           | Beschreibt eine 2D-Textur.<br/>                                                                                |
| [**D3D11 \_ TEXTURE3D \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture3d_desc)<br/>                             | Beschreibt eine 3D-Textur.<br/>                                                                                |
| [**D3D11 \_ TEXTURE3D \_ DESC1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_texture3d_desc1)<br/>                           | Beschreibt eine 3D-Textur.<br/>                                                                                |
| [**GRÖßE DER \_ D3D11-KACHELREGION \_ \_**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_region_size)<br/>                        | Beschreibt die Größe eines gekachelten Bereich.<br/>                                                                  |
| [**D3D11– \_ GEKACHELTE \_ \_ RESSOURCENKOORDINATE**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tiled_resource_coordinate)<br/>      | Beschreibt die Koordinaten einer gekachelten Ressource.<br/>                                                         |
| [**D3D11 \_ TILE \_ SHAPE**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_shape)<br/>                                     | Beschreibt die Form einer Kachel durch Angabe ihrer Dimensionen.<br/>                                            |
| [**D3D11 \_ UNORDERED \_ ACCESS \_ VIEW \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_unordered_access_view_desc)<br/>   | Gibt die Unterressourcen einer Ressource an, auf die über eine ansicht mit ungeordneten Zugriffen zugegriffen werden kann.<br/>         |
| [**D3D11 \_ UNORDERED \_ ACCESS \_ VIEW \_ DESC1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_unordered_access_view_desc1)<br/> | Beschreibt die Unterressourcen einer Ressource, auf die über eine ansicht mit ungeordneten Zugriffen zugegriffen werden kann.<br/>         |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ressourcenreferenz](d3d11-graphics-reference-resource.md)
</dt> </dl>

 

 





