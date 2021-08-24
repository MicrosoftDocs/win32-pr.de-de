---
title: CD3D11-Hilfsstrukturen
description: Direct3D 11 definiert mehrere Hilfsstrukturen, die Sie zum Erstellen von Direct3D-Strukturen verwenden können. Diese Hilfsstrukturen verhalten sich wie C++-Klassen.
ms.assetid: E44951D9-7830-4825-B7FA-CF98CC0D024C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dd7cb23ce625903b55a136c64d42264ad3b45a651258959f0ca7416380bed4d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119792080"
---
# <a name="cd3d11-helper-structures"></a>CD3D11-Hilfsstrukturen

Direct3D 11 definiert mehrere Hilfsstrukturen, die Sie zum Erstellen von Direct3D-Strukturen verwenden können. Diese Hilfsstrukturen verhalten sich wie C++-Klassen.


## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                         | Beschreibung                                                                                                                         |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**CD3D11 \_ RECT**](/windows/win32/api/d3d11/ns-d3d11-cd3d11_rect)<br/>                                                | Stellt ein Rechteck dar und stellt Benutzerfreundlichkeitsmethoden zum Erstellen von Rechtecke zur Verfügung.<br/>                                         |
| [**CD3D11 \_ BOX**](/windows/win32/api/d3d11/ns-d3d11-cd3d11_box)<br/>                                                  | Stellt ein Feld dar und stellt Benutzerfreundlichkeitsmethoden zum Erstellen von Feldern zur Verfügung.<br/>                                                    |
| [**CD3D11 \_ DEPTH \_ STENCIL \_ DESC**](/windows/win32/api/d3d11/ns-d3d11-cd3d11_depth_stencil_desc)<br/>                  | Stellt eine Tiefen-Schablonen-Zustandsstruktur dar und stellt Benutzerfreundlichkeitsmethoden zum Erstellen von Tiefen-Schablonen-Zustandsstrukturen zur Verfügung.<br/> |
| [**CD3D11 \_ BLEND \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-cd3d11_blend_desc)<br/>                                   | Stellt eine Überblendzustandsstruktur dar und stellt Benutzerfreundlichkeitsmethoden zum Erstellen von Blendzustandsstrukturen zur Verfügung.<br/>                 |
| [**CD3D11 \_ RASTERIZER \_ DESC**](/windows/win32/api/d3d11/ns-d3d11-cd3d11_rasterizer_desc)<br/>                         | Stellt eine Rasterizer-Zustandsstruktur dar und stellt Benutzerfreundlichkeitsmethoden zum Erstellen von Rasterizer-Zustandsstrukturen zur Verfügung.<br/>       |
| [**CD3D11 \_ BUFFER \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-cd3d11_buffer_desc)<br/>                                 | Stellt einen Puffer dar und stellt Benutzerfreundlichkeitsmethoden zum Erstellen von Puffern zur Verfügung.<br/>                                               |
| [**CD3D11 \_ TEXTURE1D \_ DESC**](/windows/win32/api/d3d11/ns-d3d11-cd3d11_texture1d_desc)<br/>                           | Stellt eine 1D-Textur dar und stellt Benutzerfreundlichkeitsmethoden zum Erstellen von 1D-Texturen zur Verfügung.<br/>                                       |
| [**CD3D11 \_ TEXTURE2D \_ DESC**](/windows/win32/api/d3d11/ns-d3d11-cd3d11_texture2d_desc)<br/>                           | Stellt eine 2D-Textur dar und stellt Benutzerfreundlichkeitsmethoden zum Erstellen von 2D-Texturen zur Verfügung.<br/>                                       |
| [**CD3D11 \_ TEXTURE3D \_ DESC**](/windows/win32/api/d3d11/ns-d3d11-cd3d11_texture3d_desc)<br/>                           | Stellt eine 3D-Textur dar und stellt Benutzerfreundlichkeitsmethoden zum Erstellen von 3D-Texturen zur Verfügung.<br/>                                       |
| [**CD3D11 \_ SHADER \_ RESOURCE \_ VIEW \_ DESC**](/windows/win32/api/d3d11/ns-d3d11-cd3d11_shader_resource_view_desc)<br/>   | Stellt eine Shader-Ressourcenansicht dar und stellt Benutzerfreundlichkeitsmethoden zum Erstellen von Shader-Ressourcenansichten zur Verfügung.<br/>                   |
| [**CD3D11 \_ RENDER \_ TARGET \_ VIEW \_ DESC**](/windows/win32/api/d3d11/ns-d3d11-cd3d11_render_target_view_desc)<br/>       | Stellt eine Renderzielansicht dar und stellt Benutzerfreundlichkeitsmethoden zum Erstellen von Renderzielansichten zur Verfügung.<br/>                       |
| [**CD3D11 \_ VIEWPORT**](/windows/win32/api/d3d11/ns-d3d11-cd3d11_viewport)<br/>                                        | Stellt einen Viewport dar und stellt Benutzerfreundlichkeitsmethoden zum Erstellen von Viewports zur Verfügung.<br/>                                           |
| [**CD3D11 \_ \_ TIEFEN-SCHABLONENANSICHT \_ \_ DESC**](/windows/win32/api/d3d11/ns-d3d11-cd3d11_depth_stencil_view_desc)<br/>       | Stellt eine Tiefen-Schablonenansicht dar und stellt Benutzerfreundlichkeitsmethoden zum Erstellen von Tiefen-Schablonenansichten zur Verfügung.<br/>                       |
| [**CD3D11 \_ UNORDERED \_ ACCESS \_ VIEW \_ DESC**](/windows/win32/api/d3d11/ns-d3d11-cd3d11_unordered_access_view_desc)<br/> | Stellt eine Ansicht mit ungeordneten Zugriffsberechtigungen dar und stellt Benutzerfreundlichkeitsmethoden zum Erstellen von Ansichten mit ungeordneten Zugriffen zur Verfügung.<br/>                 |
| [**CD3D11 \_ SAMPLER \_ DESC**](/windows/win32/api/d3d11/ns-d3d11-cd3d11_sampler_desc)<br/>                               | Stellt einen Samplerzustand dar und stellt Benutzerfreundlichkeitsmethoden zum Erstellen von Samplerzuständen zur Verfügung.<br/>                                 |
| [**CD3D11 \_ QUERY \_ DESC**](/windows/win32/api/d3d11/ns-d3d11-cd3d11_query_desc)<br/>                                   | Stellt eine Abfrage dar und stellt Benutzerfreundlichkeitsmethoden zum Erstellen von Abfragen zur Verfügung.<br/>                                                |
| [**CD3D11 \_ COUNTER \_ DESC**](/windows/win32/api/d3d11/ns-d3d11-cd3d11_counter_desc)<br/>                               | Stellt einen Zähler dar und stellt Benutzerfreundlichkeitsmethoden zum Erstellen von Leistungsindikatoren zur Verfügung.<br/>                                             |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Referenz für Direct3D 11](d3d11-graphics-reference.md)
</dt> </dl>

 

