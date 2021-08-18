---
title: Hardwarefeatureebenen
description: Beschreibt die Funktionalität der Hardwarefeatureebenen 11 0 bis \_ \_ 12 1.
ms.assetid: B8304E29-A532-464E-8FAF-075228D8FB73
keywords:
- DX-Featureebene
- DirectX-Featureebene
- Featureebene, DX
- Featureebene, DirectX
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf069baca3d9ff56c0d3d98e79bb553df7e8acf1fadf7b5888c5b5d211f7a874
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124148"
---
# <a name="hardware-feature-levels"></a>Hardwarefeatureebenen

Beschreibt die Funktionalität der Hardwarefeatureebenen 11 0 bis \_ \_ 12 1.

-   [Nummerierungssysteme](#numbering-systems)
-   [Unterstützung auf Featureebene](#feature-level-support)
-   [Hardwareunterstützung für DXGI-Formate](#hardware-support-for-dxgi-formats)
-   [Zugehörige Themen](#related-topics)

Um die Vielfalt der Grafikkarten auf neuen und vorhandenen Computern zu bewältigen, hat Microsoft Direct3D 11 das Konzept der Featureebenen eingeführt. Jede Grafikkarte implementiert abhängig von den installierten Grafikprozessoren (GPUs) eine bestimmte Ebene der Microsoft DirectX-Funktionalität (DX). Eine Featureebene ist ein klar definierter Satz von GPU-Funktionen. Beispielsweise implementiert die Featureebene 11 0 die Funktionalität, die \_ in Direct3D 11 implementiert wurde.

Wenn Sie nun ein Gerät erstellen, können Sie versuchen, ein Gerät für die Featureebene zu erstellen, die Sie anfordern möchten. Wenn die Geräteerstellung funktioniert, ist diese Featureebene vorhanden, ander denn, die Hardware unterstützt diese Featureebene nicht. Sie können entweder versuchen, ein Gerät auf einer niedrigeren Featureebene neu zu erstellen, oder Sie können die Anwendung beenden.

Die grundlegenden Eigenschaften von Featureebenen sind:

-   Alle Direct3D 12-Treiber verfügen über Featureebene 11 \_ 0 oder besser.
-   Eine GPU, mit der ein Gerät erstellt werden kann, erfüllt oder überschreitet die Funktionalität dieser Featureebene.
-   Eine Featureebene umfasst immer die Funktionalität vorheriger oder niedrigerer Featureebenen.
-   Eine Featureebene impliziert nicht die Leistung, sondern nur die Funktionalität. Die Leistung hängt von der Hardwareimplementierung ab.
-   Eine Featureebene wird ausgewählt, wenn [**Sie D3D12CreateDevice aufrufen.**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createdevice)
-   Ausführlichere Informationen zu unterstützten Features (insbesondere die in der folgenden Tabelle als *Optional* gekennzeichneten Features, was bedeutet, dass die Hardware das Feature unterstützen kann, aber nicht erforderlich ist), rufen [**Sie CheckFeatureSupport auf.**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport)

Informationen zu Einschränkungen beim Erstellen von Geräten ohne Hardwaretyp auf bestimmten Featureebenen finden Sie unter Einschränkungen beim Erstellen von [WARP- und Referenzgeräten.](/windows/desktop/direct3d11/overviews-direct3d-11-devices-limitations) Weitere Informationen zur Einführung von Featureebenen finden Sie in der Direct3D 11-Dokumentation zu [Direct3D-Featureebenen.](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro)

## <a name="numbering-systems"></a>Nummerierungssysteme

Hardwarefeatureebenen *sind nicht* identisch mit API-Versionen. Es gibt beispielsweise eine D3D11.3-API, aber es gibt keine 11 \_ 3-Hardwarefeatureebene. Featureebenen werden in der [**\_ D3D-Aufzählfunktionsebene \_**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level) definiert.

Es gibt drei unterschiedliche Nummerierungssysteme:

-   Direct3D-Versionen verwenden einen Zeitraum. Beispiel: Direct3D 12.0.
-   Shadermodelle verwenden einen Zeitraum. Beispiel: Shadermodell 5.1.
-   Featureebenen verwenden einen Unterstrich. Beispiel: Featureebene 12 \_ 0.

## <a name="feature-level-support"></a>Unterstützung auf Featureebene

Die folgenden Features sind für jede Direct3D-Featureebene verfügbar.

Die Überschriften in der oberen Zeile sind Direct3D-Featureebenen. Die Überschriften in der linken Spalte sind Features.



| \\Featureebene                                                                                                 | 12 \_ 1⁰                    | 12 \_ 0⁰                    | 11 \_ 1                   | 11 \_ 0                    |
|--------------------------------------------------------------------------------------------------------------------------|---------------------------|---------------------------|--------------------------|--------------------------|
| Shadermodell                                                                                                             | 5,1                       | 5,1                       | 5.12                     | 5.12                     |
| [Ressourcenbindungsebene](hardware-support.md)                                                                            | Ebene 2                    | Ebene 2                    | Ebene1                   | Ebene1                   |
| [Gekachelte Ressourcen](/windows/desktop/api/d3d12/ne-d3d12-d3d12_tiled_resources_tier)                                                                        | Ebene 2                    | Ebene 2                    | Optional                 | Optional                 |
| [Konservative Rasterung](conservative-rasterization.md)                                                             | Ebene1                    | Optional                  | Optional                 | Nein                       |
| [Geordnete Rasterizeransichten](rasterizer-order-views.md)                                                                   | Ja                       | Optional                  | Optional                 | Nein                       |
| [Mindest-/Maximalfilter](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter)                                                                                      | Ja                       | Ja                       | Optional                 | Nein                       |
| Standardpuffer zuordnen                                                                                                       | Optional                  | Optional                  | Optional                 | Optional                 |
| [Von Shader festgelegter Schablonenreferenzwert](shader-specified-stencil-reference-value.md)                                 | Optional                  | Optional                  | Optional                 | Nein                       |
| [Typierte ungeordnete Zugriffsansichtslasten](typed-unordered-access-view-loads.md)                                               | 18 Formate, optionaler | 18 Formate, optionaler | 3 Formate, optionaler | 3 Formate, optionaler |
| [Geometrie-Shader](/previous-versions//bb205146(v=vs.85)) | Ja                       | Ja                       | Ja                      | Ja                      |
| [StreamEnd](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-stream-stage)                                            | Ja                       | Ja                       | Ja                      | Ja                      |
| [DirectCompute/Compute-Shader](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader)                                  | Ja                       | Ja                       | Ja                      | Ja                      |
| [Hülle und Domänen-Shader](/windows/desktop/direct3d11/direct3d-11-advanced-stages-tessellation)                                           | Ja                       | Ja                       | Ja                      | Ja                      |
| [Texturressourcenarrays](/windows/desktop/direct3d11/overviews-direct3d-11-resources-textures-intro)                                     | Ja                       | Ja                       | Ja                      | Ja                      |
| [Cubemap-Ressourcenarrays](/windows/desktop/direct3d11/overviews-direct3d-11-resources-textures-intro)                                     | Ja                       | Ja                       | Ja                      | Ja                      |
| [BC1-zu-BC7-Komprimierung](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-block-compression)                        | Ja                       | Ja                       | Ja                      | Ja                      |
| [Alpha-to-Coverage](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-blend-state)         | Ja                       | Ja                       | Ja                      | Ja                      |
| [Logikvorgänge (Ausgabefusion)](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options)                                          | Ja                       | Ja                       | Ja                      | Optional                 |
| Zielunabhängige Rasterung                                                                                         | Ja                       | Ja                       | Ja                      | Nein                       |
| [Mehrere Renderziel (MRT) mit ForcedSampleCount 1](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options)                      | Ja                       | Ja                       | Ja                      | Optional                 |
| [Maximale Anzahl erzwungener Stichproben für nur UAV-Rendering](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options)                            | 16                        | 16                        | 16                       | 8                        |
| Max. Texturdimension                                                                                                    | 16384                     | 16384                     | 16384                    | 16384                    |
| Max. Cubemapdimension                                                                                                    | 16384                     | 16384                     | 16384                    | 16384                    |
| Max Volume Extent                                                                                                        | 2048                      | 2048                      | 2048                     | 2048                     |
| Maximale Textur wiederholen                                                                                                       | 16384                     | 16384                     | 16384                    | 16384                    |
| Max. Anisotropie                                                                                                           | 16                        | 16                        | 16                       | 16                       |
| Max. Anzahl primitiver Typen                                                                                                      | 2^32 – 1                  | 2^32 – 1                  | 2^32 – 1                 | 2^32 – 1                 |
| Max. Scheitelpunktindex                                                                                                         | 2^32 – 1                  | 2^32 – 1                  | 2^32 – 1                 | 2^32 – 1                 |
| Max. Eingabeslots                                                                                                          | 32                        | 32                        | 32                       | 32                       |
| Gleichzeitige Renderziele                                                                                              | 8                         | 8                         | 8                        | 8                        |
| Okclusion Queries (Okclusion-Abfragen)                                                                                                        | Ja                       | Ja                       | Ja                      | Ja                      |
| Separate Alphablendung                                                                                                     | Ja                       | Ja                       | Ja                      | Ja                      |
| Spiegelung einmal                                                                                                              | Ja                       | Ja                       | Ja                      | Ja                      |
| Überlappende Scheitelpunktelemente                                                                                              | Ja                       | Ja                       | Ja                      | Ja                      |
| Unabhängige Schreibmasken                                                                                                  | Ja                       | Ja                       | Ja                      | Ja                      |
| Instancing                                                                                                               | Ja                       | Ja                       | Ja                      | Ja                      |



 

-   ⁰ erfordert die Direct3D 11.3- oder Direct3D 12-Runtime.
-   ¹ Erfordert die Direct3D 11.1-Runtime.
-   Das Shadermodell 5.0 kann optional Shader mit doppelter Genauigkeit, erweiterte Shader mit doppelter Genauigkeit, **die ANWEISUNG SAD4-Shader** und Shader mit teilweiser Genauigkeit unterstützen. Rufen Sie [**ID3D12Device::CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport)auf, um die verfügbaren Optionen des Shadermodells 5.0 zu bestimmen. Ein gewisses Maß an Kompatibilität hängt davon ab, auf welcher Hardware Sie ausführen: Shadermodell 5.1 wird nur auf Hardware unterstützt, die die DirectX 12-API unterstützt, unabhängig von der verwendeten Funktionsebene. DirectX 11-Hardware unterstützt nur bis zu Shadermodell 5.0. Die DirectX 12-API wird nur auf Featureebene 11 \_ 0 heruntergefahren.
-   2 Höhere Ebenen sind optional.
-   Für die Featureebenen 12 0 und 12 1 ist die \_ \_ Direct3D 11.3- oder Direct3D 12-Runtime erforderlich.
-   Für Featureebene 11 \_ 1 ist die Direct3D 11.1-Runtime erforderlich.
-   Für Featureebene 11 \_ 0 ist die Direct3D 11.0-Runtime erforderlich.

## <a name="hardware-support-for-dxgi-formats"></a>Hardwareunterstützung für DXGI-Formate

Informationen zum Anzeigen von Tabellen mit DXGI-Formaten und Hardwarefeatures finden Sie unter:

-   [DXGI-Formatunterstützung für Direct3D-Hardware auf Featureebene 12.1](/windows/desktop/direct3ddxgi/hardware-support-for-direct3d-12-1-formats)
-   [DXGI-Formatunterstützung für Direct3D-Hardware auf Featureebene 12.0](/windows/desktop/direct3ddxgi/hardware-support-for-direct3d-12-0-formats)
-   [DXGI-Formatunterstützung für Direct3D-Hardware auf Featureebene 11.1](/windows/desktop/direct3ddxgi/format-support-for-direct3d-11-1-feature-level-hardware)
-   [DXGI-Formatunterstützung für Direct3D-Hardware auf Featureebene 11.0](/windows/desktop/direct3ddxgi/format-support-for-direct3d-11-0-feature-level-hardware)
-   [Hardwareunterstützung für Direct3D 10Level9-Formate](/previous-versions//ff471324(v=vs.85))
-   [Hardwareunterstützung für Direct3D 10.1-Formate](/previous-versions//cc627091(v=vs.85))
-   [Hardwareunterstützung für Direct3D 10-Formate](/previous-versions//cc627090(v=vs.85))

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Abfragen der Funktionalität](capability-querying.md)
</dt> <dt>

[Grundlegendes zu Direct3D 12](directx-12-getting-started.md)
</dt> </dl>

 

 
