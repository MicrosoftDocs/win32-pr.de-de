---
title: Ressourcenenumerationen (Direct3D 11-Grafiken)
description: Enumerationen werden verwendet, um Informationen darüber anzugeben, wie Ressourcen während des Renderings erstellt und darauf zugegriffen wird.
ms.assetid: b547819b-7006-40b5-84a4-adf198048051
keywords:
- Enumerationen, Direct3D 11-Ressource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6965eabfdb66c5459da799830cba9e87312566910e0dea84d400cb39b39127e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119126064"
---
# <a name="resource-enumerations-direct3d-11-graphics"></a>Ressourcenenumerationen (Direct3D 11-Grafiken)

Enumerationen werden verwendet, um Informationen darüber anzugeben, wie Ressourcen während des Renderings erstellt und darauf zugegriffen wird.


## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                               | BESCHREIBUNG                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**D3D11 \_ \_ BIND-FLAG**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)<br/>                                                             | Gibt an, wie eine Ressource an die Pipeline gebunden wird.<br/>                                                                                                                                 |
| [**D3D11 \_ BUFFEREX \_ \_ SRV-FLAG**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bufferex_srv_flag)<br/>                                            | Gibt an, wie eine Pufferressource angezeigt wird.<br/>                                                                                                                                          |
| [**D3D11 \_ BUFFER \_ UAV \_ FLAG**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_buffer_uav_flag)<br/>                                                | Identifiziert Optionen für die Ansicht für ungeordneten Zugriff für eine Pufferressource.<br/>                                                                                                                    |
| [**D3D11 \_ CHECK \_ MULTISAMPLE \_ QUALITY \_ LEVELS \_ FLAG**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_check_multisample_quality_levels_flag)<br/> | Identifiziert, wie Multisample-Qualitätsstufen überprüft werden.<br/>                                                                                                                                |
| [**D3D11 \_ CPU \_ ACCESS \_ FLAG**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cpu_access_flag)<br/>                                                | Gibt die Typen des CPU-Zugriffs an, die für eine Ressource zulässig sind.<br/>                                                                                                                          |
| [**D3D11 \_ DSV \_ DIMENSION**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_dsv_dimension)<br/>                                                     | Gibt an, wie auf eine Ressource zugegriffen wird, die in einer Tiefenschablonenansicht verwendet wird.<br/>                                                                                                                   |
| [**D3D11 \_ \_ DSV-FLAG**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_dsv_flag)<br/>                                                               | Optionen für die Tiefenschablonenansicht.<br/>                                                                                                                                                        |
| [**D3D11 \_ MAP**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map)<br/>                                                                          | Identifiziert eine Ressource, auf die von der CPU zum Lesen und Schreiben zugegriffen werden soll. Anwendungen können eines oder mehrere dieser Flags kombinieren.<br/>                                                      |
| [**\_D3D11-ZUORDNUNGSFLAG \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map_flag)<br/>                                                               | Gibt an, wie die CPU reagieren soll, wenn eine Anwendung die [**ID3D11DeviceContext::Map-Methode**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) für eine Ressource aufruft, die von der GPU verwendet wird.<br/> |
| [**\_D3D11-RESSOURCENDIMENSION \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_dimension)<br/>                                           | Gibt den Typ der verwendeten Ressource an.<br/>                                                                                                                                        |
| [**D3D11 \_ RESOURCE \_ MISC \_ FLAG**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)<br/>                                          | Identifiziert Optionen für Ressourcen.<br/>                                                                                                                                                  |
| [**D3D11 \_ RTV \_ DIMENSION**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_rtv_dimension)<br/>                                                     | Diese Flags identifizieren den Typ der Ressource, die als Renderziel angezeigt wird.<br/>                                                                                                  |
| [**D3D11 \_ \_ SRV-DIMENSION**](/previous-versions/windows/desktop/legacy/ff476217(v=vs.85))<br/>                                                     | Diese Flags identifizieren den Typ der Ressource, die als Shaderressource angezeigt wird.<br/>                                                                                                |
| [**D3D11 \_ STANDARD \_ MULTISAMPLE-QUALITÄTSSTUFEN \_ \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_standard_multisample_quality_levels)<br/>       | Gibt einen Mustertyp mit mehreren Stichproben an.<br/>                                                                                                                                             |
| [**D3D11 \_ \_ TEXTURLAYOUT**](/windows/desktop/api/D3D11_3/ne-d3d11_3-d3d11_texture_layout)<br/>                                                   | Gibt Texturlayoutoptionen an.<br/>                                                                                                                                                  |
| [**D3D11- \_ \_ \_ KACHELKOPIEFLAG**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_tile_copy_flag)<br/>                                                 | Gibt an, wie eine Kachel kopiert wird.<br/>                                                                                                                                                     |
| [**\_ \_ KACHELZUORDNUNGSFLAG D3D11 \_**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_tile_mapping_flag)<br/>                                           | Gibt an, wie ein Kachelzuordnungsvorgang ausgeführt wird.<br/>                                                                                                                                |
| [**\_D3D11-KACHELBEREICHSFLAG \_ \_**](/windows/desktop/api/d3d11_2/ne-d3d11_2-d3d11_tile_range_flag)<br/>                                                | Gibt einen Bereich von Kachelzuordnungen an, der mit [**ID3D11DeviceContext2::UpdateTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles)verwendet werden soll.<br/>                                                      |
| [**D3D11 \_ \_ UAV-DIMENSION**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_uav_dimension)<br/>                                                     | Optionen für die Ansicht "Unordered Access".<br/>                                                                                                                                                     |
| [**D3D11-NUTZUNG \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)<br/>                                                                      | Identifiziert die erwartete Ressourcenverwendung während des Renderings. Die Nutzung gibt direkt an, ob die CPU und/oder die Grafikverarbeitungseinheit (GPU) auf eine Ressource zugreifen kann.<br/>              |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ressourcenreferenz](d3d11-graphics-reference-resource.md)
</dt> </dl>

 

