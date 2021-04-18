---
title: Ressourcen Enumerationen (Direct3D 11-Grafiken)
description: Enumerationen werden verwendet, um Informationen darüber anzugeben, wie Ressourcen während des Renderings erstellt und aufgerufen werden.
ms.assetid: b547819b-7006-40b5-84a4-adf198048051
keywords:
- Enumerationen, Direct3D 11-Ressource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6124fcbc93cb0069152dd20d3b4b3bf0f4be60d
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104976952"
---
# <a name="resource-enumerations-direct3d-11-graphics"></a>Ressourcen Enumerationen (Direct3D 11-Grafiken)

Enumerationen werden verwendet, um Informationen darüber anzugeben, wie Ressourcen während des Renderings erstellt und aufgerufen werden.


## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                               | BESCHREIBUNG                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**D3D11 \_ Bind- \_ Flag**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)<br/>                                                             | Gibt an, wie eine Ressource an die Pipeline gebunden wird.<br/>                                                                                                                                 |
| [**D3D11 \_ bufferex \_ SRV- \_ Flag**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bufferex_srv_flag)<br/>                                            | Gibt an, wie eine Puffer Ressource angezeigt wird.<br/>                                                                                                                                          |
| [**D3D11 \_ buffer \_ UAV- \_ Flag**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_buffer_uav_flag)<br/>                                                | Identifiziert Ansichtsoptionen für ungeordnete Zugriffe für eine Puffer Ressource.<br/>                                                                                                                    |
| [**D3D11 \_ Überprüfen von \_ Multisample \_ Quality \_ Levels- \_ Flag**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_check_multisample_quality_levels_flag)<br/> | Gibt Aufschluss über das Überprüfen von Qualitäts Ebenen mit mehreren Beispielen.<br/>                                                                                                                                |
| [**D3D11 \_ CPU \_ - \_ Zugriffsflag**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cpu_access_flag)<br/>                                                | Gibt die Typen des für eine Ressource zulässigen CPU-Zugriffs an.<br/>                                                                                                                          |
| [**D3D11 \_ DSV- \_ Dimension**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_dsv_dimension)<br/>                                                     | Gibt an, wie auf eine Ressource zugegriffen werden kann, die in einer Ansicht der tiefen Schablone verwendet wird.<br/>                                                                                                                   |
| [**D3D11 \_ DSV- \_ Flag**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_dsv_flag)<br/>                                                               | Optionen für die Anzeige der tiefen Schablone.<br/>                                                                                                                                                        |
| [**D3D11- \_ Karte**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map)<br/>                                                                          | Identifiziert eine Ressource, auf die der CPU-Lese-und Schreibvorgang zugreifen soll. Anwendungen können eines oder mehrere dieser Flags kombinieren.<br/>                                                      |
| [**D3D11 \_ map- \_ Flag**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map_flag)<br/>                                                               | Gibt an, wie die CPU reagieren soll, wenn eine Anwendung die [**Verknüpfung id3d11devicecontext aus:: Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) -Methode für eine von der GPU verwendete Ressource aufruft.<br/> |
| [**D3D11- \_ Ressourcen \_ Dimension**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_dimension)<br/>                                           | Identifiziert den Typ der verwendeten Ressource.<br/>                                                                                                                                        |
| [**D3D11 \_ \_ ressourcenmisc- \_ Flag**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)<br/>                                          | Identifiziert Optionen für Ressourcen.<br/>                                                                                                                                                  |
| [**D3D11 \_ RTV- \_ Dimension**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_rtv_dimension)<br/>                                                     | Diese Flags identifizieren den Typ der Ressource, die als Renderziel angezeigt wird.<br/>                                                                                                  |
| [**D3D11 \_ SRV- \_ Dimension**](/previous-versions/windows/desktop/legacy/ff476217(v=vs.85))<br/>                                                     | Diese Flags identifizieren den Typ der Ressource, die als Shader-Ressource angezeigt wird.<br/>                                                                                                |
| [**D3D11 \_ Standard- \_ \_ Qualitäts \_ Ebenen mit mehreren Beispielen**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_standard_multisample_quality_levels)<br/>       | Gibt einen mehrdimensionalen Mustertyp an.<br/>                                                                                                                                             |
| [**D3D11- \_ Textur \_ Layout**](/windows/desktop/api/D3D11_3/ne-d3d11_3-d3d11_texture_layout)<br/>                                                   | Gibt Textur Layout-Optionen an.<br/>                                                                                                                                                  |
| [**D3D11 \_ Tile \_ - \_ kopierflag**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_tile_copy_flag)<br/>                                                 | Gibt an, wie eine Kachel kopiert wird.<br/>                                                                                                                                                     |
| [**D3D11 Tile-Zuordnungs \_ \_ \_ Flag**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_tile_mapping_flag)<br/>                                           | Gibt an, wie ein Kachel Zuordnungs Vorgang durchgeführt wird.<br/>                                                                                                                                |
| [**D3D11 \_ Tile \_ Range- \_ Flag**](/windows/desktop/api/d3d11_2/ne-d3d11_2-d3d11_tile_range_flag)<br/>                                                | Gibt einen Bereich von Kachel Zuordnungen an, der mit [**ID3D11DeviceContext2:: updatetiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles)verwendet werden soll.<br/>                                                      |
| [**D3D11 \_ UAV- \_ Dimension**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_uav_dimension)<br/>                                                     | Optionen für ungeordnete Zugriffs Ansicht.<br/>                                                                                                                                                     |
| [**D3D11- \_ Verwendung**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)<br/>                                                                      | Identifiziert die erwartete Ressourcenverwendung während des Renderings. Die Verwendung gibt direkt an, ob die CPU und/oder die Grafikverarbeitungseinheit (Graphics Processing Unit, GPU) auf eine Ressource zugreifen kann.<br/>              |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ressourcen Verweis](d3d11-graphics-reference-resource.md)
</dt> </dl>

 

