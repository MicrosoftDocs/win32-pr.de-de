---
title: Hardware Funktionsebenen
description: Beschreibt die Funktionalität der- \_ Hardware Funktionsebenen von 11 bis 12 \_ 1.
ms.assetid: B8304E29-A532-464E-8FAF-075228D8FB73
keywords:
- DX-Funktionsebene
- DirectX-Featureebene
- Funktionsebene, DX
- Funktionsebene, DirectX
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d464f6cc52539e31fee5e234af2c045dfff7e413
ms.sourcegitcommit: 218b1ff779402c3ebe1786679e1aa80a5c0d6c95
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "104548637"
---
# <a name="hardware-feature-levels"></a>Hardware Funktionsebenen

Beschreibt die Funktionalität der- \_ Hardware Funktionsebenen von 11 bis 12 \_ 1.

-   [Nummerierungssysteme](#numbering-systems)
-   [Unterstützung auf Funktionsebene](#feature-level-support)
-   [Hardware Unterstützung für DXGI-Formate](#hardware-support-for-dxgi-formats)
-   [Verwandte Themen](#related-topics)

Zur Bewältigung der Vielfalt von Grafikkarten auf neuen und vorhandenen Computern wurde mit Microsoft Direct3D 11 das Konzept von featureebenen eingeführt. Jede Grafikkarte implementiert eine bestimmte Ebene der Microsoft DirectX-Funktionalität (DX), abhängig von den installierten GPUs (Graphics Processing Units). Eine Featureebene ist ein gut definierter Satz von GPU-Funktionen. Beispielsweise implementiert die 11- \_ 0-Funktionsebene die in Direct3D 11 implementierte Funktionalität.

Wenn Sie nun ein Gerät erstellen, können Sie versuchen, ein Gerät für die gewünschte Funktionsebene zu erstellen. Wenn die Geräte Erstellung funktioniert, ist diese Featureebene vorhanden. Falls nicht, wird diese Featureebene von der Hardware nicht unterstützt. Sie können entweder versuchen, ein Gerät auf einer niedrigeren Funktionsebene neu zu erstellen, oder Sie können die Anwendung beenden.

Die grundlegenden Eigenschaften von featureebenen sind:

-   Alle Direct3D 12-Treiber sind die Featureebene 11 \_ 0 oder höher.
-   Eine GPU, mit der ein Gerät erstellt werden kann, entspricht der Funktion dieser Featureebene oder überschreitet diese.
-   Eine Featureebene umfasst immer die Funktionalität früherer oder niedrigerer featureebenen.
-   Eine Featureebene impliziert keine Leistung, sondern nur Funktionen. Die Leistung ist abhängig von der Hardware Implementierung.
-   Eine Featureebene wird ausgewählt, wenn Sie [**D3D12CreateDevice**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createdevice)aufgerufen haben.
-   Ausführlichere Informationen zu den unterstützten Funktionen (insbesondere die in der folgenden Tabelle aufgeführten *optionalen* ), was bedeutet, dass die Hardware die Funktion unterstützt, jedoch nicht erforderlich ist, finden Sie unter [**checkfeaturesupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport).

Informationen zu Einschränkungen bei der Erstellung von Geräten ohne Hardwaretyp auf bestimmten featureebenen finden Sie unter [Einschränkungen beim Erstellen von Warp-und Referenz Geräten](/windows/desktop/direct3d11/overviews-direct3d-11-devices-limitations). Weitere Informationen zur Einführung von featureebenen finden Sie in der Dokumentation zu Direct3D 11 auf [Direct3D-featureebenen](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro).

## <a name="numbering-systems"></a>Nummerierungssysteme

Die Hardware Funktionsebenen sind *nicht* mit den API-Versionen identisch. Es gibt z. b. eine D3D 11.3-API, aber es gibt keine 11- \_ 3-Hardware Funktionsebene. Funktionsebenen werden in der D3D-Aufzählungs [**\_ \_ Ebene**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level) definiert.

Es gibt drei unterschiedliche Nummerierungssysteme:

-   Direct3D-Versionen verwenden einen Zeitraum; beispielsweise Direct3D 12,0.
-   Shadermodelle verwenden einen Zeitraum; beispielsweise Shader-Modell 5,1.
-   Funktionsebenen verwenden einen Unterstrich. Beispiel: featurestufe 12 \_ 0.

## <a name="feature-level-support"></a>Unterstützung auf Funktionsebene

Die folgenden Features sind für jede Direct3D-Funktionsebene verfügbar.

Die Überschriften in der obersten Zeile sind Direct3D-Funktionsebenen. Die Überschriften in der linken Spalte sind Features.



| Funktions \\ Ebene der Features                                                                                                 | 12 \_ 1 ⁰                    | 12 \_ 0 ⁰                    | 11 \_ 1 ¹                   | 11 \_ 0                    |
|--------------------------------------------------------------------------------------------------------------------------|---------------------------|---------------------------|--------------------------|--------------------------|
| Shadermodell                                                                                                             | 5,1                       | 5,1                       | 5,1 ²                     | 5,1 ²                     |
| [Ressourcen Bindungs Ebene](hardware-support.md)                                                                            | Instanzen ³                    | Instanzen ³                    | Tier1 ³                   | Tier1 ³                   |
| [Gekachelte Ressourcen](/windows/desktop/api/d3d12/ne-d3d12-d3d12_tiled_resources_tier)                                                                        | Instanzen ³                    | Instanzen ³                    | Optional                 | Optional                 |
| [Konservative rasterisierung](conservative-rasterization.md)                                                             | Tier1 ³                    | Optional                  | Optional                 | Nein                       |
| [Geordnete Ansichten des Rasterizers](rasterizer-order-views.md)                                                                   | Ja                       | Optional                  | Optional                 | Nein                       |
| [Min/Max-Filter](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter)                                                                                      | Ja                       | Ja                       | Optional                 | Nein                       |
| Karten Standard Puffer                                                                                                       | Optional                  | Optional                  | Optional                 | Optional                 |
| [Von Shader angegebener Schablone-Verweis Wert](shader-specified-stencil-reference-value.md)                                 | Optional                  | Optional                  | Optional                 | Nein                       |
| [Typisierte nicht geordnete zugriffsansichts Ladungen](typed-unordered-access-view-loads.md)                                               | 18 Formate, optional | 18 Formate, optional | 3 Formate, optionaler | 3 Formate, optionaler |
| [Geometrie-Shader](/previous-versions//bb205146(v=vs.85)) | Ja                       | Ja                       | Ja                      | Ja                      |
| [Stream ausgehend](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-stream-stage)                                            | Ja                       | Ja                       | Ja                      | Ja                      |
| [DirectCompute/Compute-Shader](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader)                                  | Ja                       | Ja                       | Ja                      | Ja                      |
| [Hülle und Domänen-Shader](/windows/desktop/direct3d11/direct3d-11-advanced-stages-tessellation)                                           | Ja                       | Ja                       | Ja                      | Ja                      |
| [Textur Ressourcen Arrays](/windows/desktop/direct3d11/overviews-direct3d-11-resources-textures-intro)                                     | Ja                       | Ja                       | Ja                      | Ja                      |
| [Cubemap-Ressourcen Arrays](/windows/desktop/direct3d11/overviews-direct3d-11-resources-textures-intro)                                     | Ja                       | Ja                       | Ja                      | Ja                      |
| [BC1-Komprimierung](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-block-compression)                        | Ja                       | Ja                       | Ja                      | Ja                      |
| [Alpha-zu-Abdeckung](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-blend-state)         | Ja                       | Ja                       | Ja                      | Ja                      |
| [Logik Vorgänge (Ausgabe Zusammenführung)](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options)                                          | Ja                       | Ja                       | Ja                      | Optional                 |
| Ziel unabhängige rasterisierung                                                                                         | Ja                       | Ja                       | Ja                      | Nein                       |
| [Mehrere Renderziel (MRT) mit forcedsamplecount 1](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options)                      | Ja                       | Ja                       | Ja                      | Optional                 |
| [Maximale Anzahl erzwungener Stichproben für das reine UAV-Rendering](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options)                            | 16                        | 16                        | 16                       | 8                        |
| Max Texture-Dimension                                                                                                    | 16384                     | 16384                     | 16384                    | 16384                    |
| Maximale cubemap-Dimension                                                                                                    | 16384                     | 16384                     | 16384                    | 16384                    |
| Maximaler volumenblock                                                                                                        | 2048                      | 2048                      | 2048                     | 2048                     |
| Maximale Textur Wiederholung                                                                                                       | 16384                     | 16384                     | 16384                    | 16384                    |
| Maximale Anisotropie                                                                                                           | 16                        | 16                        | 16                       | 16                       |
| Maximale Anzahl primitiver                                                                                                      | 2 ^ 32 – 1                  | 2 ^ 32 – 1                  | 2 ^ 32 – 1                 | 2 ^ 32 – 1                 |
| Maximaler Scheitelpunkt Index                                                                                                         | 2 ^ 32 – 1                  | 2 ^ 32 – 1                  | 2 ^ 32 – 1                 | 2 ^ 32 – 1                 |
| Maximale Eingabe Slots                                                                                                          | 32                        | 32                        | 32                       | 32                       |
| Gleichzeitige Renderziele                                                                                              | 8                         | 8                         | 8                        | 8                        |
| Okklusions Abfragen                                                                                                        | Ja                       | Ja                       | Ja                      | Ja                      |
| Separates Alpha Blend                                                                                                     | Ja                       | Ja                       | Ja                      | Ja                      |
| Einmal spiegeln                                                                                                              | Ja                       | Ja                       | Ja                      | Ja                      |
| Überlappende Scheitelpunkt Elemente                                                                                              | Ja                       | Ja                       | Ja                      | Ja                      |
| Unabhängige Schreib Masken                                                                                                  | Ja                       | Ja                       | Ja                      | Ja                      |
| Instancing                                                                                                               | Ja                       | Ja                       | Ja                      | Ja                      |



 

-   ⁰ erfordert die Direct3D 11,3-oder Direct3D 12-Laufzeit.
-   ¹ erfordert die Direct3D 11,1-Laufzeit.
-   ² Shadermodell 5,0 kann optional Shader mit doppelter Genauigkeit, erweiterte Shader mit doppelter Genauigkeit, die **SAD4** -Shader-Anweisung und Shader mit teilweiser Genauigkeit unterstützen. Um die verfügbaren Shader Model 5,0-Optionen zu bestimmen, nennen Sie [**ID3D12Device:: checkfeaturesupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport). Die Kompatibilität hängt von der Hardware ab, auf der Sie ausgeführt werden: das Shader-Modell 5,1 wird nur auf Hardware unterstützt, die die DirectX 12-API unterstützt, unabhängig von der verwendeten Funktionsebene. Die DirectX 11-Hardware unterstützt nur das Shader-Modell 5,0. Die DirectX 12-API gilt nur für die Featureebene 11 \_ 0.
-   ³ höhere Ebenen sind optional.
-   Die Funktionsebenen 12 \_ 0 und 12 \_ 1 erfordern die Laufzeit Direct3D 11,3 oder Direct3D 12.
-   Die Funktionsebene 11 \_ 1 erfordert die Direct3D 11,1-Laufzeit.
-   Die Funktionsebene 11 \_ 0 erfordert die Direct3D 11,0-Laufzeit.

## <a name="hardware-support-for-dxgi-formats"></a>Hardware Unterstützung für DXGI-Formate

Weitere Informationen zum Anzeigen von Tabellen mit DXGI-Formaten und Hardwarefunktionen finden Sie unter:

-   [DXGI-Format Unterstützung für Direct3D Featureebene 12,1 Hardware](/windows/desktop/direct3ddxgi/hardware-support-for-direct3d-12-1-formats)
-   [DXGI-Format Unterstützung für Direct3D Featureebene 12,0 Hardware](/windows/desktop/direct3ddxgi/hardware-support-for-direct3d-12-0-formats)
-   [DXGI-Format Unterstützung für Direct3D Featureebene 11,1 Hardware](/windows/desktop/direct3ddxgi/format-support-for-direct3d-11-1-feature-level-hardware)
-   [DXGI-Format Unterstützung für Direct3D Featureebene 11,0 Hardware](/windows/desktop/direct3ddxgi/format-support-for-direct3d-11-0-feature-level-hardware)
-   [Hardware Unterstützung für Direct3D 10level9-Formate](/previous-versions//ff471324(v=vs.85))
-   [Hardware Unterstützung für Direct3D 10,1-Formate](/previous-versions//cc627091(v=vs.85))
-   [Hardware Unterstützung für Direct3D 10-Formate](/previous-versions//cc627090(v=vs.85))

## <a name="related-topics"></a>Verwandte Themen

<dl> <dt>

[Funktions Abfrage](capability-querying.md)
</dt> <dt>

[Grundlegendes zu Direct3D 12](directx-12-getting-started.md)
</dt> </dl>

 

 
