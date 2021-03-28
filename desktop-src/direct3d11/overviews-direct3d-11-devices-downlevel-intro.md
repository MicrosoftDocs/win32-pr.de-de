---
title: Direct3D-Featureebenen
description: In diesem Thema werden Direct3D Funktionsebenen erläutert.
ms.assetid: 5ad0525c-249f-452d-950b-df8fa2addde2
keywords:
- DX-Funktionsebene
- DirectX-Featureebene
- Funktionsebene, DX
- Funktionsebene, DirectX
ms.topic: article
ms.date: 09/01/2020
ms.openlocfilehash: 82667a7a2e02d675185fd65c318aeed10db79844
ms.sourcegitcommit: 85bd7112570865dd2136e0d05bd0a4132e6313ec
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2020
ms.locfileid: "104039749"
---
# <a name="direct3d-feature-levels"></a>Direct3D-Featureebenen

Zur Bewältigung der Vielfalt von Grafikkarten auf neuen und vorhandenen Computern führt Microsoft Direct3D 11 das Konzept von featureebenen ein. In diesem Thema werden Direct3D Funktionsebenen erläutert.

Jede Grafikkarte implementiert eine bestimmte Ebene der Microsoft DirectX-Funktionalität (DX), abhängig von den installierten GPUs (Graphics Processing Units). In früheren Versionen von Microsoft Direct3D konnten Sie die Version von Direct3D, die die Videokarte implementiert hat, ermitteln und dann die Anwendung entsprechend programmieren.

Mit Direct3D 11 wird ein neues Paradigma namens Funktionsebenen eingeführt. Eine Featureebene ist ein klar definierter Satz mit GPU-Funktionen. Beispielsweise implementiert die 9 \_ 1-Funktionsebene die in Microsoft Direct3D 9 implementierte Funktionalität, die die Funktionen von Shader-Modellen [PS \_ 2 \_ x](../direct3dhlsl/dx9-graphics-reference-asm-ps-2-x.md) und [vs \_ 2 \_ x](../direct3dhlsl/dx9-graphics-reference-asm-vs-2-x.md)verfügbar macht, während die 11-0-Funktions \_ Ebene die in Direct3D 11 implementierte Funktionalität implementiert.

Wenn Sie nun ein Gerät erstellen, können Sie versuchen, ein Gerät für die gewünschte Funktionsebene zu erstellen. Wenn die Geräte Erstellung funktioniert, ist diese Featureebene vorhanden. Falls nicht, wird diese Featureebene von der Hardware nicht unterstützt. Sie können entweder versuchen, ein Gerät auf einer niedrigeren Funktionsebene neu zu erstellen, oder Sie können die Anwendung beenden. Weitere Informationen zum Erstellen eines Geräts finden Sie unter der [**D3D11CreateDevice**](/windows/win32/api/D3D11/nf-d3d11-d3d11createdevice) -Funktion.

Mithilfe von featurestufen können Sie eine Anwendung für Direct3D 9, Microsoft Direct3D 10 oder Direct3D 11 entwickeln und dann auf 9, 10 oder 11 Hardware ausführen (mit einigen Ausnahmen), z. b., wenn neue 11 Features nicht auf einer vorhandenen 9-Karte ausgeführt werden. Im folgenden sind einige weitere grundlegende Eigenschaften von featureebenen aufgeführt:

- Eine GPU, mit der ein Gerät erstellt werden kann, entspricht der Funktion dieser Featureebene oder überschreitet diese.
- Eine Featureebene umfasst immer die Funktionalität früherer oder niedrigerer featureebenen.
- Eine Featureebene impliziert keine Leistung, sondern nur Funktionen. Die Leistung ist abhängig von der Hardware Implementierung.
- Wählen Sie eine Featureebene aus, wenn Sie ein Direct3D 11-Gerät erstellen.

Informationen zu Einschränkungen bei der Erstellung von Geräten mit nicht-Hardware-Typ auf bestimmten featureebenen finden Sie unter [Einschränkungen beim Erstellen von Warp-und Referenz Geräten](overviews-direct3d-11-devices-limitations.md).

Vergleichen Sie die Features für jede Featureebene, um Sie bei der Entscheidung zu unterstützen, mit welcher Funktionsebene Sie zu entwerfen.

Der [Verweis Bereich 10level9](d3d11-graphics-reference-10level9.md) listet die Unterschiede zwischen der Art und Weise, wie sich verschiedene [**ID3D11Device**](/windows/win32/api/D3D11/nn-d3d11-id3d11device) -und [**Verknüpfung id3d11devicecontext aus**](/windows/win32/api/D3D11/nn-d3d11-id3d11devicecontext) -Methoden auf verschiedenen 10 Level9-featureebenen

## <a name="formats-of-version-numbers"></a>Formate von Versionsnummern

Es gibt drei Formate für Direct3D-Versionen, Shader-Modelle und Funktionsebenen.

- Direct3D-Versionen verwenden einen Zeitraum; beispielsweise Direct3D 12,0.
- Shadermodelle verwenden einen Zeitraum; beispielsweise Shader-Modell 5,1.
- Funktionsebenen verwenden einen Unterstrich. Beispiel: featurestufe 12 \_ 0.

## <a name="feature-support-for-feature-levels-12_1-through-9_3"></a>Funktions Unterstützung für featureebenen 12_1 bis 9_3

Die folgenden Features sind für die aufgeführten Funktionsebenen verfügbar. Die Überschriften in der obersten Zeile sind Direct3D-Funktionsebenen. Die Überschriften in der linken Spalte sind Features. Siehe auch [Fußnoten für die Tabellen](#footnotes-for-the-tables).

| Funktions \\ Ebene der Features | 12 \_ 1<sup>0</sup> | 12 \_ 0<sup>0</sup> | 11 \_ 1<sup>1</sup> | 11 \_ 0 | 10 \_ 1 | 10 \_ 0 | 9 \_ 3<sup>7</sup> |
|-|-|-|-|-|-|-|-|
| Shadermodell (D3D11) | 5,0<sup>2</sup> | 5,0<sup>2</sup> | 5,0<sup>2</sup> | 5,0<sup>2</sup> | 4.x | 4,0 | 2,0 (4 \_ 0 \_ Ebene \_ 9 \_ 3) \[ vs \_ 2 \_ a/PS \_ 2 \_ x \] <sup>5</sup> |
| Shadermodell (D3D12) | 5,1<sup>2</sup> | 5,1<sup>2</sup> | 5,1<sup>2</sup> | 5,1<sup>2</sup> | – | – | – |
| [Gekachelte Ressourcen](tiled-resources.md) | Instanzen<sup>6</sup> | Instanzen<sup>6</sup> | Optional | Optional | Nein | Nein | Nein |
| [Konservative Rasterung](conservative-rasterization.md) | Tier1<sup>6</sup> | Optional | Optional | Nein | Nein | Nein | Nein |
| [Reihen folgen Ansichten für Rasterizer](rasterizer-order-views.md) | Ja | Optional | Optional | Nein | Nein | Nein | Nein |
| [Min/Max-Filter](/windows/win32/api/D3D11/ne-d3d11-d3d11_filter) | Ja | Ja | Optional | Nein | Nein | Nein | Nein |
| Karten Standard Puffer | Optional | Optional | Optional | Optional | Nein | Nein | Nein |
| [Von Shader festgelegter Schablonenreferenzwert](shader-specified-stencil-reference-value.md) | Optional | Optional | Optional | Nein | Nein | Nein | Nein |
| Typisierte nicht geordnete zugriffsansichts Ladungen | 18 Formate, optional | 18 Formate, optional | 3 Formate, optionaler | 3 Formate, optionaler | Nein | Nein | Nein |
| [Geometrie-Shader](/previous-versions/bb205146(v=vs.85)) | Ja | Ja | Ja | Ja | Ja | Ja | Nein |
| [Stream ausgehend](./d3d10-graphics-programming-guide-output-stream-stage.md) | Ja | Ja | Ja | Ja | Ja | Ja | Nein |
| [DirectCompute/Compute-Shader](direct3d-11-advanced-stages-compute-shader.md) | Ja | Ja | Ja | Ja | Optional | Optional | – |
| <b>Funktions \\ Ebene der Features</b> | <b>12 \_ 1<sup>0</sup></b> | <b>12 \_ 0<sup>0</sup></b> | <b>11 \_ 1<sup>1</sup></b> | <b>11 \_ 0</b> | <b>10 \_ 1</b> | <b>10 \_ 0</b> | <b>9 \_ 3<sup>7</sup></b> |
| [Hülle und Domänen-Shader](direct3d-11-advanced-stages-tessellation.md) | Ja | Ja | Ja | Ja | Nein | Nein | Nein |
| [Textur Ressourcen Arrays](overviews-direct3d-11-resources-textures-intro.md) | Ja | Ja | Ja | Ja | Ja | Ja | Nein |
| [Cubemap-Ressourcen Arrays](overviews-direct3d-11-resources-textures-intro.md) | Ja | Ja | Ja | Ja | Ja | Nein | Nein |
| [BC4/BC5-Komprimierung](../direct3d10/d3d10-graphics-programming-guide-resources-block-compression.md) | Ja | Ja | Ja | Ja | Ja | Ja | Nein |
| [BC6H/bzw bc7-Komprimierung](texture-block-compression-in-direct3d-11.md) | Ja | Ja | Ja | Ja | Nein | Nein | Nein |
| [Alpha-zu-Abdeckung](./d3d10-graphics-programming-guide-blend-state.md) | Ja | Ja | Ja | Ja | Ja | Ja | Nein |
| [Erweiterte Formate (BGRA usw.)](overviews-direct3d-11-devices-downlevel-exceptions.md) | Ja | Ja | Ja | Ja | Optional | Optional | Ja |
| [10-Bit-XR-Format mit hoher Farbtiefe](overviews-direct3d-11-devices-downlevel-exceptions.md) | Ja | Ja | Ja | Ja | Optional | Optional | – |
| [Logik Vorgänge (Ausgabe Zusammenführung)](/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) | Ja | Ja | Ja | Optional<sup>1</sup> | Optional<sup>1</sup> | Optional<sup>1</sup> | Nein |
| Ziel unabhängige rasterisierung | Ja | Ja | Ja | Nein | Nein | Nein | Nein |
| [Mehrere Renderziel (MRT) mit forcedsamplecount 1](/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) | Ja | Ja | Ja | Optional<sup>1</sup> | Optional<sup>1</sup> | Optional<sup>1</sup> | Nein |
| UAV-Slots | 64 | 64 | 64 | 8 | 1 | 1 | Nicht zutreffend |
| <b>Funktions \\ Ebene der Features</b> | <b>12 \_ 1<sup>0</sup></b> | <b>12 \_ 0<sup>0</sup></b> | <b>11 \_ 1<sup>1</sup></b> | <b>11 \_ 0</b> | <b>10 \_ 1</b> | <b>10 \_ 0</b> | <b>9 \_ 3<sup>7</sup></b> |
| UAVs in jeder Phase | Ja | Ja | Ja | Nein | Nein | Nein | – |
| [Maximale Anzahl erzwungener Stichproben für das reine UAV-Rendering](/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) | 16 | 16 | 16 | 8 | – | – | – |
| Konstante Puffer versetzen und Teil Aktualisierungen | Ja | Ja | Ja | Optional<sup>1</sup> | Optional<sup>1</sup> | Optional<sup>1</sup> | Ja<sup>1</sup> |
| bpp-Formate (16 Bits pro Pixel) | Ja | Ja | Ja | Optional<sup>1</sup> | Optional<sup>1</sup> | Optional<sup>1</sup> | Optional<sup>1</sup> |
| Max Texture-Dimension | 16384 | 16384 | 16384 | 16384 | 8192 | 8192 | 4096 |
| Maximale cubemap-Dimension | 16384 | 16384 | 16384 | 16384 | 8192 | 8192 | 4096 |
| Maximaler volumenblock | 2048 | 2048 | 2048 | 2048 | 2048 | 2048 | 256 |
| Maximale Textur Wiederholung | 16384 | 16384 | 16384 | 16384 | 8192 | 8192 | 8192 |
| Maximale Anisotropie | 16 | 16 | 16 | 16 | 16 | 16 | 16 |
| Maximale Anzahl primitiver | 2 ^ 32 – 1 | 2 ^ 32 – 1 | 2 ^ 32 – 1 | 2 ^ 32 – 1 | 2 ^ 32 – 1 | 2 ^ 32 – 1 | 1048575 |
| Maximaler Scheitelpunkt Index | 2 ^ 32 – 1 | 2 ^ 32 – 1 | 2 ^ 32 – 1 | 2 ^ 32 – 1 | 2 ^ 32 – 1 | 2 ^ 32 – 1 | 1048575 |
| Maximale Eingabe Slots | 32 | 32 | 32 | 32 | 32 | 16 | 16 |
| Gleichzeitige Renderziele | 8 | 8 | 8 | 8 | 8 | 8 | 4 |
| Okklusions Abfragen | Ja | Ja | Ja | Ja | Ja | Ja | Ja |
| <b>Funktions \\ Ebene der Features</b> | <b>12 \_ 1<sup>0</sup></b> | <b>12 \_ 0<sup>0</sup></b> | <b>11 \_ 1<sup>1</sup></b> | <b>11 \_ 0</b> | <b>10 \_ 1</b> | <b>10 \_ 0</b> | <b>9 \_ 3<sup>7</sup></b> |
| Separates Alpha Blend | Ja | Ja | Ja | Ja | Ja | Ja | Ja |
| Einmal spiegeln | Ja | Ja | Ja | Ja | Ja | Ja | Ja |
| Überlappende Scheitelpunkt Elemente | Ja | Ja | Ja | Ja | Ja | Ja | Ja |
| Unabhängige Schreib Masken | Ja | Ja | Ja | Ja | Ja | Ja | Ja |
| Instancing | Ja | Ja | Ja | Ja | Ja | Ja | Ja<sup>7</sup> |
| Nicht-Powers-von-2 bedingt<sup>3</sup> | Nein | Nein | Nein | Nein | Nein | Nein | Ja |
| Nonpowers-of-2 bedingungslos<sup>4</sup> | Ja | Ja | Ja | Ja | Ja | Ja | Nein |

## <a name="feature-support-for-feature-levels-9_2-and-9_1"></a>Funktions Unterstützung für Funktionsebenen 9_2 und 9_1

Die folgenden Features sind für die aufgeführten Funktionsebenen verfügbar. Die Überschriften in der obersten Zeile sind Direct3D-Funktionsebenen. Die Überschriften in der linken Spalte sind Features. Siehe auch [Fußnoten für die Tabellen](#footnotes-for-the-tables).

| Funktions \\ Ebene der Features | 9 \_ 2 | 9 \_ 1 |
|-|-|-|
| Shadermodell (D3D11) | 2,0 (4 \_ 0 \_ Ebene \_ 9 \_ 1) | 2,0 (4 \_ 0 \_ Ebene \_ 9 \_ 1) |
| Shadermodell (D3D12) | – | – |
| [Gekachelte Ressourcen](tiled-resources.md) | Nein | Nein |
| [Konservative Rasterung](conservative-rasterization.md) | Nein | Nein |
| [Reihen folgen Ansichten für Rasterizer](rasterizer-order-views.md) | Nein | Nein |
| [Min/Max-Filter](/windows/win32/api/D3D11/ne-d3d11-d3d11_filter) | Nein | Nein |
| Karten Standard Puffer | Nein | Nein |
| [Von Shader festgelegter Schablonenreferenzwert](shader-specified-stencil-reference-value.md) | Nein | Nein |
| Typisierte nicht geordnete zugriffsansichts Ladungen | Nein | Nein |
| [Geometrie-Shader](/previous-versions/bb205146(v=vs.85)) | Nein | Nein |
| [Stream ausgehend](./d3d10-graphics-programming-guide-output-stream-stage.md) | Nein | Nein |
| [DirectCompute/Compute-Shader](direct3d-11-advanced-stages-compute-shader.md) | – | – |
| [Hülle und Domänen-Shader](direct3d-11-advanced-stages-tessellation.md) | Nein | Nein |
| [Textur Ressourcen Arrays](overviews-direct3d-11-resources-textures-intro.md) | Nein | Nein |
| [Cubemap-Ressourcen Arrays](overviews-direct3d-11-resources-textures-intro.md) | Nein | Nein |
| [BC4/BC5-Komprimierung](../direct3d10/d3d10-graphics-programming-guide-resources-block-compression.md) | Nein | Nein |
| <b>Funktions \\ Ebene der Features</b> | <b>9 \_ 2</b> | <b>9 \_ 1</b> |
| [BC6H/bzw bc7-Komprimierung](texture-block-compression-in-direct3d-11.md) | Nein | Nein |
| [Alpha-zu-Abdeckung](./d3d10-graphics-programming-guide-blend-state.md) | Nein | Nein |
| [Erweiterte Formate (BGRA usw.)](overviews-direct3d-11-devices-downlevel-exceptions.md) | Ja | Ja |
| [10-Bit-XR-Format mit hoher Farbtiefe](overviews-direct3d-11-devices-downlevel-exceptions.md) | – | – |
| [Logik Vorgänge (Ausgabe Zusammenführung)](/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) | Nein | Nein |
| Ziel unabhängige rasterisierung | Nein | Nein |
| [Mehrere Renderziel (MRT) mit forcedsamplecount 1](/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) | Nein | Nein |
| UAV-Slots | – | – |
| UAVs in jeder Phase | – | – |
| [Maximale Anzahl erzwungener Stichproben für das reine UAV-Rendering](/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) | – | – |
| Konstante Puffer versetzen und Teil Aktualisierungen | Ja<sup>1</sup> | Ja<sup>1</sup> |
| bpp-Formate (16 Bits pro Pixel) | Optional<sup>1</sup> | Optional<sup>1</sup> |
| Max Texture-Dimension | 2048 | 2048 |
| Maximale cubemap-Dimension | 512 | 512 |
| Maximaler volumenblock | 256 | 256 |
| Maximale Textur Wiederholung | 2048 | 128 |
| <b>Funktions \\ Ebene der Features</b> | <b>9 \_ 2</b> | <b>9 \_ 1</b> |
| Maximale Anisotropie | 16 | 2 |
| Maximale Anzahl primitiver | 1048575 | 65.535 |
| Maximaler Scheitelpunkt Index | 1048575 | 65534 |
| Maximale Eingabe Slots | 16 | 16 |
| Gleichzeitige Renderziele | 1 | 1 |
| Okklusions Abfragen | Ja | Nein |
| Separates Alpha Blend | Ja | Nein |
| Einmal spiegeln | Ja | Nein |
| Überlappende Scheitelpunkt Elemente | Ja | Nein |
| Unabhängige Schreib Masken | Nein | Nein |
| Instancing | Nein | Nein |
| Nicht-Powers-von-2 bedingt<sup>3</sup> | Ja | Ja |
| Nonpowers-of-2 bedingungslos<sup>4</sup> | Nein | Nein |

## <a name="footnotes-for-the-tables"></a>Fußnoten für die Tabellen

<sup>0</sup> erfordert die Direct3D 11,3-oder Direct3D 12-Laufzeit.

<sup>1</sup> erfordert die Direct3D 11,1-Laufzeit.

<sup>2</sup> das Shadermodell 5,0 und höher kann optional Shader mit doppelter Genauigkeit, erweiterte Shader mit doppelter Genauigkeit, die **SAD4** -Shader-Anweisung und Shader mit teilweiser Genauigkeit unterstützen. Um die für DirectX 11 verfügbaren Shader-Modell 5,0-Optionen zu bestimmen, wenden Sie sich an [**ID3D11Device:: checkfeaturesupport**](/windows/win32/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport). Die Kompatibilität hängt von der Hardware ab, auf der Sie ausgeführt werden. Das Shader-Modell 5,1 und höher wird nur über die DirectX 12-API unterstützt, unabhängig von der verwendeten Funktionsebene. DirectX 11 unterstützt nur das Shader-Modell 5,0. Die DirectX 12-API gilt nur für die Featureebene 11 \_ 0.

<sup>3</sup> bei den featureebenen 9 \_ 1, 9 \_ 2 und 9 \_ 3 unterstützt das Anzeigegerät die Verwendung von 2D-Texturen mit Dimensionen, bei denen es sich nicht um zwei unter zwei Bedingungen handelt. Erstens kann nur eine MIP-Map-Ebene für jede Textur erstellt werden, und zweitens sind keine Wrap-Sampler-Modi für Texturen zulässig (d. h. die **adressssu**-, **adressvc**-und **AddressW** -Member von [**D3D11 \_ Sampler \_ DESC**](/windows/win32/api/D3D11/ns-d3d11-d3d11_sampler_desc) können nicht auf [**D3D11 \_ Texture \_ Address \_ Wrap**](/windows/win32/api/D3D11/ne-d3d11-d3d11_texture_address_mode)festgelegt werden).

<sup>4</sup> bei den featureebenen 10 \_ 0, 10 \_ 1 und 11 \_ 0 unterstützt das Anzeigegerät bedingungslos die Verwendung von 2D-Texturen mit Dimensionen, die keine zweidimensionalen Funktionen sind.

<sup>5</sup> Vertex Shader 2A mit 256-Anweisungen, 32 temporäre Register, statische Fluss Steuerung der Tiefe 4, dynamische Fluss Steuerung der Tiefe 24 und D3DVS20CAPS- \_ Prädikat. Pixel-Shader 2X mit 512-Anweisungen, 32 temporäre Register, statische Fluss Steuerung der Tiefe 4, dynamische Fluss Steuerung der Tiefe 24, D3DPS20CAPS,,) \_ , D3DPS20CAPS \_ gradientinstructions, D3DPS20CAPS \_ prediation, D3DPS20CAPS \_ nodependentleslimit und D3DPS20CAPS \_ notexinstructionlimit.

<sup>6</sup> höhere Ebenen sind optional.

<sup>7</sup> für Funktionsebene 9_3 werden nur die unterstützten Renderingmethoden **gezeichnet**, **drawindexed** und **drawindexinstanxed** unterstützt. Außerdem wird bei Featureebene 9_3 das Rendering von Punkt Listen nur für das Rendering über **Draw** unterstützt.

Ausführliche Informationen zur Formatunterstützung auf verschiedenen Hardware Funktionsebenen finden Sie unter:

- [DXGI-Format Unterstützung für Direct3D Featureebene 12,1 Hardware](../direct3ddxgi/hardware-support-for-direct3d-12-1-formats.md)
- [DXGI-Format Unterstützung für Direct3D Featureebene 12,0 Hardware](../direct3ddxgi/hardware-support-for-direct3d-12-0-formats.md)
- [DXGI-Format Unterstützung für Direct3D Featureebene 11,1 Hardware](../direct3ddxgi/format-support-for-direct3d-11-1-feature-level-hardware.md)
- [DXGI-Format Unterstützung für Direct3D Featureebene 11,0 Hardware](../direct3ddxgi/format-support-for-direct3d-11-0-feature-level-hardware.md)
- [Hardware Unterstützung für Direct3D 10level9-Formate](/previous-versions/ff471324(v=vs.85))
- [Hardware Unterstützung für Direct3D 10,1-Formate](/previous-versions/cc627091(v=vs.85))
- [Hardware Unterstützung für Direct3D 10-Formate](/previous-versions/cc627090(v=vs.85))

## <a name="related-topics"></a>Zugehörige Themen

* [Direct3D 11 auf downlevelhardware](overviews-direct3d-11-devices-downlevel.md)
* [Hardware Funktionsebenen (Direct3D 12)](../direct3d12/hardware-feature-levels.md)
