---
title: CD3D11 Helper-Strukturen
description: Direct3D 11 definiert mehrere Hilfsstrukturen, die Sie zum Erstellen von Direct3D-Strukturen verwenden können. Diese Hilfsstrukturen Verhalten sich wie C++-Klassen.
ms.assetid: E44951D9-7830-4825-B7FA-CF98CC0D024C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 578e8fb398ef5348146f9623f98f0b6d01414a50
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104474686"
---
# <a name="cd3d11-helper-structures"></a>CD3D11 Helper-Strukturen

Direct3D 11 definiert mehrere Hilfsstrukturen, die Sie zum Erstellen von Direct3D-Strukturen verwenden können. Diese Hilfsstrukturen Verhalten sich wie C++-Klassen.


## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                         | BESCHREIBUNG                                                                                                                         |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**CD3D11 \_ Rect**](/windows/win32/api/d3d11/ns-d3d11-cd3d11_rect)<br/>                                                | Stellt ein Rechteck dar und stellt Hilfsmethoden zum Erstellen von Rechtecke bereit.<br/>                                         |
| [**CD3D11- \_ Feld**](/windows/win32/api/d3d11/ns-d3d11-cd3d11_box)<br/>                                                  | Stellt ein Feld dar und stellt Hilfsmethoden zum Erstellen von Feldern bereit.<br/>                                                    |
| [**CD3D11 \_ tiefen \_ Schablone-Schablone \_**](/windows/win32/api/d3d11/ns-d3d11-cd3d11_depth_stencil_desc)<br/>                  | Stellt eine Tiefe Struktur Zustands Struktur dar und stellt Hilfsmethoden zum Erstellen von tiefen Schablone dar.<br/> |
| [**CD3D11 \_ Blend- \_ Entsc**](/windows/desktop/api/D3D11/ns-d3d11-cd3d11_blend_desc)<br/>                                   | Stellt eine Blend-Status Struktur dar und stellt Hilfsmethoden zum Erstellen von Blend-Zustands Strukturen bereit.<br/>                 |
| [**CD3D11 \_ Rasterizer- \_ Abteilung**](/windows/win32/api/d3d11/ns-d3d11-cd3d11_rasterizer_desc)<br/>                         | Stellt eine Rasterizer-State-Struktur dar und stellt Hilfsmethoden zum Erstellen von Rasterizer-State-Strukturen bereit.<br/>       |
| [**CD3D11- \_ Puffer \_**](/windows/desktop/api/D3D11/ns-d3d11-cd3d11_buffer_desc)<br/>                                 | Stellt einen Puffer dar und stellt Hilfsmethoden zum Erstellen von Puffern bereit.<br/>                                               |
| [**CD3D11 \_ TEXTURE1D- \_ Abteilung**](/windows/win32/api/d3d11/ns-d3d11-cd3d11_texture1d_desc)<br/>                           | Stellt eine 1D-Textur dar und stellt Hilfsmethoden zum Erstellen von 1D-Texturen bereit.<br/>                                       |
| [**CD3D11 \_ TEXTURE2D- \_ Abteilung**](/windows/win32/api/d3d11/ns-d3d11-cd3d11_texture2d_desc)<br/>                           | Stellt eine 2D-Textur dar und stellt Hilfsmethoden zum Erstellen von 2D-Texturen bereit.<br/>                                       |
| [**CD3D11 \_ TEXTURE3D- \_ Abteilung**](/windows/win32/api/d3d11/ns-d3d11-cd3d11_texture3d_desc)<br/>                           | Stellt eine 3D-Textur dar und stellt Hilfsmethoden zum Erstellen von 3D-Texturen bereit.<br/>                                       |
| [**CD3D11 \_ Shader- \_ Ressourcen \_ Ansicht \_ (Debug)**](/windows/win32/api/d3d11/ns-d3d11-cd3d11_shader_resource_view_desc)<br/>   | Stellt eine Shader-Ressourcen Ansicht dar und stellt Hilfsmethoden zum Erstellen von Shader-Ressourcen Ansichten bereit.<br/>                   |
| [**CD3D11 \_ \_ \_ renderzielansicht \_ DESC**](/windows/win32/api/d3d11/ns-d3d11-cd3d11_render_target_view_desc)<br/>       | Stellt eine renderzielansicht dar und stellt Hilfsmethoden zum Erstellen von renderzielsichten bereit.<br/>                       |
| [**CD3D11 \_ Viewport**](/windows/win32/api/d3d11/ns-d3d11-cd3d11_viewport)<br/>                                        | Stellt einen Viewport dar und stellt Hilfsmethoden zum Erstellen von Viewports bereit.<br/>                                           |
| [**CD3D11 \_ tiefen \_ Schablone \_ anzeigen \_**](/windows/win32/api/d3d11/ns-d3d11-cd3d11_depth_stencil_view_desc)<br/>       | Stellt eine Ansicht der tiefen Schablone dar und stellt Hilfsmethoden zum Erstellen von tiefen Schablonen Ansichten bereit.<br/>                       |
| [**CD3D11 \_ unsortierter \_ \_ Zugriffsansicht \_ Deaktivieren**](/windows/win32/api/d3d11/ns-d3d11-cd3d11_unordered_access_view_desc)<br/> | Stellt eine Ansicht für ungeordnete Zugriffe dar und stellt Hilfsmethoden zum Erstellen von Ansichten für ungeordneten Zugriff bereit.<br/>                 |
| [**CD3D11 \_ Sampler- \_ Abteilung**](/windows/win32/api/d3d11/ns-d3d11-cd3d11_sampler_desc)<br/>                               | Stellt einen samplerzustand dar und bietet Hilfsmethoden zum Erstellen von samplerzuständen.<br/>                                 |
| [**CD3D11 \_ Abfrage \_ Absteigend**](/windows/win32/api/d3d11/ns-d3d11-cd3d11_query_desc)<br/>                                   | Stellt eine Abfrage dar und stellt Hilfsmethoden zum Erstellen von Abfragen bereit.<br/>                                                |
| [**CD3D11 \_ Counter-Wert \_**](/windows/win32/api/d3d11/ns-d3d11-cd3d11_counter_desc)<br/>                               | Stellt einen Zähler dar und stellt Hilfsmethoden zum Erstellen von Indikatoren bereit.<br/>                                             |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Referenz für Direct3D 11](d3d11-graphics-reference.md)
</dt> </dl>

 

