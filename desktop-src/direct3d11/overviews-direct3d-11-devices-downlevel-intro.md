---
title: Direct3D-Featureebenen
description: In diesem Thema werden Direct3D-Featureebenen erläutert.
ms.assetid: 5ad0525c-249f-452d-950b-df8fa2addde2
keywords:
- DX-Featureebene
- DirectX-Featureebene
- Featureebene, DX
- Featureebene, DirectX
ms.topic: article
ms.date: 09/01/2020
ms.openlocfilehash: e1ca80faa816ff7601f0a33893a708fafa7f2d3f
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812046"
---
# <a name="direct3d-feature-levels"></a>Direct3D-Featureebenen

> [!NOTE]
> **Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.**

Um die Vielfalt von Grafikkarten auf neuen und vorhandenen Computern zu bewältigen, führt Microsoft Direct3D 11 das Konzept der Featureebenen ein. In diesem Thema werden Direct3D-Featureebenen erläutert.

Jede Grafikkarte implementiert abhängig von den installierten Grafikprozessoren (GPUs) eine bestimmte Ebene der Microsoft DirectX-Funktionalität (DX). In früheren Versionen von Microsoft Direct3D konnten Sie die Version von Direct3D ermitteln, die die Grafikkarte implementiert hat, und dann Ihre Anwendung entsprechend programmieren.

Mit Direct3D 11 wird ein neues Paradigma eingeführt, das als Featureebenen bezeichnet wird. Eine Featureebene ist ein klar definierter Satz mit GPU-Funktionen. Beispielsweise implementiert die \_ Featureebene 9 1 die In Microsoft Direct3D 9 implementierte Funktionalität, die die Funktionen der Shadermodelle [ps \_ 2 \_ x](../direct3dhlsl/dx9-graphics-reference-asm-ps-2-x.md) und [ \_ 2 \_ x](../direct3dhlsl/dx9-graphics-reference-asm-vs-2-x.md)verfügbar macht, während die \_ 11 0-Featureebene die Funktionalität implementiert, die in Direct3D 11 implementiert wurde.

Wenn Sie nun ein Gerät erstellen, können Sie versuchen, ein Gerät für die Featureebene zu erstellen, die Sie anfordern möchten. Wenn die Geräteerstellung funktioniert, ist diese Featureebene vorhanden, falls nicht, unterstützt die Hardware diese Featureebene nicht. Sie können entweder versuchen, ein Gerät auf einer niedrigeren Featureebene neu zu erstellen, oder Sie können die Anwendung beenden. Weitere Informationen zum Erstellen eines Geräts finden Sie unter der [**D3D11CreateDevice-Funktion.**](/windows/win32/api/D3D11/nf-d3d11-d3d11createdevice)

Mithilfe von Featureebenen können Sie eine Anwendung für Direct3D 9, Microsoft Direct3D 10 oder Direct3D 11 entwickeln und dann auf 9, 10 oder 11 Hardware ausführen (mit einigen Ausnahmen, z. B. werden neue 11-Features nicht auf einer vorhandenen 9-Karte ausgeführt). Im Folgenden finden Sie einige weitere grundlegende Eigenschaften von Featureebenen:

- Eine GPU, mit der ein Gerät erstellt werden kann, erfüllt oder überschreitet die Funktionalität dieser Featureebene.
- Eine Featureebene enthält immer die Funktionalität früherer oder niedrigerer Featureebenen.
- Eine Funktionsebene impliziert nicht die Leistung, sondern nur die Funktionalität. Die Leistung hängt von der Hardwareimplementierungen ab.
- Wählen Sie eine Funktionsebene aus, wenn Sie ein Direct3D 11-Gerät erstellen.

Informationen zu Einschränkungen beim Erstellen von Geräten vom Typ "Nonhardware" auf bestimmten Featureebenen finden Sie unter [Einschränkungen beim Erstellen von WARP- und Referenzgeräten.](overviews-direct3d-11-devices-limitations.md)

Um Sie bei der Entscheidung zu unterstützen, mit welcher Featureebene Sie entwerfen möchten, vergleichen Sie die Features für jede Featureebene.

Im Abschnitt [Referenz zu 10Level9](d3d11-graphics-reference-10level9.md) werden die Unterschiede zwischen den verschiedenen [**Methoden ID3D11Device**](/windows/win32/api/D3D11/nn-d3d11-id3d11device) und [**ID3D11DeviceContext**](/windows/win32/api/D3D11/nn-d3d11-id3d11devicecontext) auf verschiedenen 10Level9-Featureebenen aufgelistet.

## <a name="formats-of-version-numbers"></a>Formate von Versionsnummern

Es gibt drei Formate für Direct3D-Versionen, Shadermodelle und Featureebenen.

- Direct3D-Versionen verwenden einen Punkt. Beispiel: Direct3D 12.0.
- Shadermodelle verwenden einen Punkt. Beispiel: Shadermodell 5.1.
- Featureebenen verwenden einen Unterstrich. Beispiel: Featureebene 12 \_ 0.

## <a name="feature-support-for-feature-levels-12_2-through-9_3"></a>Featureunterstützung für die Featureebenen 12_2 bis 9_3

Die folgenden Features sind für die aufgeführten Featureebenen verfügbar. Die Überschriften in der oberen Zeile sind Direct3D-Featureebenen. Die Überschriften in der linken Spalte sind Features. Siehe auch [Fußnoten für die Tabellen](#footnotes-for-the-tables).

| \\Featureebene | 12 \_ 2<sup>8</sup> | 12 \_ 1<sup>0</sup> | 12 \_ 0<sup>0</sup> | 11 \_ 1<sup>1</sup> | 11 \_ 0 | 10 \_ 1 | 10 \_ 0 | 9 \_ 3<sup>7</sup> |
|-|-|-|-|-|-|-|-|-|
| Shadermodell (D3D11) | Nicht zutreffend | 5.0<sup>2</sup> | 5.0<sup>2</sup> | 5.0<sup>2</sup> | 5.0<sup>2</sup> | 4.x | 4.0 | 2.0 (4 \_ 0 \_ Ebene \_ 9 \_ 3) \[ im Vergleich zu \_ 2 \_ a/ps \_ 2 x \_ \] <sup>5</sup> |
| Shadermodell (D3D12) | 6,5 | 5.1<sup>2</sup> | 5.1<sup>2</sup> | 5.1<sup>2</sup> | 5.1<sup>2</sup> | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend |
| [Gekachelte Ressourcen](tiled-resources.md) | Ebene 3 | Ebene<sup>2 6</sup> | Ebene<sup>2 6</sup> | Optional | Optional | Nein | Nein | Nein |
| [Konservative Rasterung](conservative-rasterization.md) | Ebene 3 | Ebene<sup>1 6</sup> | Optional | Optional | Nein | Nein | Nein | Nein |
| [Rasterizer-Auftragsansichten](rasterizer-order-views.md) | Ja | Ja | Optional | Optional | Nein | Nein | Nein | Nein |
| [Mindest-/Maximalfilter](/windows/win32/api/D3D11/ne-d3d11-d3d11_filter) | Ja | Ja | Ja | Optional | Nein | Nein | Nein | Nein |
| Zuordnen des Standardpuffers | Nicht zutreffend | Optional | Optional | Optional | Optional | Nein | Nein | Nein |
| [Von Shader festgelegter Schablonenreferenzwert](shader-specified-stencil-reference-value.md) | Optional | Optional | Optional | Optional | Nein | Nein | Nein | Nein |
| Typisiertes Laden von ungeordneten Zugriffsansichten | 18 Formate, optionaler | 18 Formate, optionaler | 18 Formate, optionaler | 3 Formate, optionaler | 3 Formate, optionaler | Nein | Nein | Nein |
| [Geometrie-Shader](/previous-versions/bb205146(v=vs.85)) | Ja | Ja | Ja | Ja | Ja | Ja | Ja | Nein |
| [Stream Out](./d3d10-graphics-programming-guide-output-stream-stage.md) | Ja | Ja | Ja | Ja | Ja | Ja | Ja | Nein |
| [DirectCompute/Compute-Shader](direct3d-11-advanced-stages-compute-shader.md) | Ja | Ja | Ja | Ja | Ja | Optional | Optional | Nicht zutreffend |
| <b>\\Featureebene</b> | <b>12 \_ 2<sup>8</sup></b> | <b>12 \_ 1<sup>0</sup></b> | <b>12 \_ 0<sup>0</sup></b> | <b>11 \_ 1<sup>1</sup></b> | <b>11 \_ 0</b> | <b>10 \_ 1</b> | <b>10 \_ 0</b> | <b>9 \_ 3<sup>7</sup></b> |
| [Shader für Hüllen und Domänen](direct3d-11-advanced-stages-tessellation.md) | Ja | Ja | Ja | Ja | Ja | Nein | Nein | Nein |
| [Texturressourcenarrays](overviews-direct3d-11-resources-textures-intro.md) | Ja | Ja | Ja | Ja | Ja | Ja | Ja | Nein |
| [Cubemap-Ressourcenarrays](overviews-direct3d-11-resources-textures-intro.md) | Ja | Ja | Ja | Ja | Ja | Ja | Nein | Nein |
| [BC4/BC5-Komprimierung](../direct3d10/d3d10-graphics-programming-guide-resources-block-compression.md) | Ja | Ja | Ja | Ja | Ja | Ja | Ja | Nein |
| [BC6H/BC7-Komprimierung](texture-block-compression-in-direct3d-11.md) | Ja | Ja | Ja | Ja | Ja | Nein | Nein | Nein |
| [Alpha-to-Coverage](./d3d10-graphics-programming-guide-blend-state.md) | Ja | Ja | Ja | Ja | Ja | Ja | Ja | Nein |
| [Erweiterte Formate (BGRA, so weiter)](overviews-direct3d-11-devices-downlevel-exceptions.md) | Ja | Ja | Ja | Ja | Ja | Optional | Optional | Ja |
| [10-Bit-XR-Format mit hoher Farbtiefe](overviews-direct3d-11-devices-downlevel-exceptions.md) | Ja | Ja | Ja | Ja | Ja | Optional | Optional | Nicht zutreffend |
| [Logikvorgänge (Ausgabefusion)](/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) | Ja | Ja | Ja | Ja | Optional<sup>1</sup> | Optional<sup>1</sup> | Optional<sup>1</sup> | Nein |
| Zielunabhängige Rasterung | Ja | Ja | Ja | Ja | Nein | Nein | Nein | Nein |
| [Mehrere Renderziel (MRT) mit ForcedSampleCount 1](/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) | Ja | Ja | Ja | Ja | Optional<sup>1</sup> | Optional<sup>1</sup> | Optional<sup>1</sup> | Nein |
| UAV-Slots | Mehrstufige<sup>9</sup> | 64 | 64 | 64 | 8 | 1 | 1 | Nicht zutreffend |
| <b>\\Featureebene</b> | <b>12 \_ 2<sup>8</sup></b> | <b>12 \_ 1<sup>0</sup></b> | <b>12 \_ 0<sup>0</sup></b> | <b>11 \_ 1<sup>1</sup></b> | <b>11 \_ 0</b> | <b>10 \_ 1</b> | <b>10 \_ 0</b> | <b>9 \_ 3<sup>7</sup></b> |
| UAVs in jeder Phase | Ja | Ja | Ja | Ja | Nein | Nein | Nein | – |
| [Maximale Anzahl erzwungener Stichproben für nur UAV-Rendering](/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) | 16 | 16 | 16 | 16 | 8 | Nicht zutreffend | Nicht zutreffend | Nicht zutreffend |
| Konstante Pufferabsetzung und Teilaktualisierungen | Ja | Ja | Ja | Ja | Optional<sup>1</sup> | Optional<sup>1</sup> | Optional<sup>1</sup> | Ja<sup>1</sup> |
| 16 Bits pro Pixel (bpp) | Ja | Ja | Ja | Ja | Optional<sup>1</sup> | Optional<sup>1</sup> | Optional<sup>1</sup> | Optional<sup>1</sup> |
| Max. Texturdimension | 16384 | 16384 | 16384 | 16384 | 16384 | 8192 | 8192 | 4096 |
| Max. Cubemapdimension | 16384 | 16384 | 16384 | 16384 | 16384 | 8192 | 8192 | 4096 |
| Max Volume Extent | 2048 | 2048 | 2048 | 2048 | 2048 | 2048 | 2048 | 256 |
| Max Texture Repeat | 16384 | 16384 | 16384 | 16384 | 16384 | 8192 | 8192 | 8192 |
| Max. Anisotropie | 16 | 16 | 16 | 16 | 16 | 16 | 16 | 16 |
| Maximale Anzahl primitiver Typen | 2^32 – 1 | 2^32 – 1 | 2^32 – 1 | 2^32 – 1 | 2^32 – 1 | 2^32 – 1 | 2^32 – 1 | 1048575 |
| Max. Scheitelpunktindex | 2^32 – 1 | 2^32 – 1 | 2^32 – 1 | 2^32 – 1 | 2^32 – 1 | 2^32 – 1 | 2^32 – 1 | 1048575 |
| Max. Eingabeslots | 32 | 32 | 32 | 32 | 32 | 32 | 16 | 16 |
| Gleichzeitige Renderziele | 8 | 8 | 8 | 8 | 8 | 8 | 8 | 4 |
| Okklusionsabfragen | Ja | Ja | Ja | Ja | Ja | Ja | Ja | Ja |
| <b>\\Featureebene</b> | <b>12 \_ 2<sup>8</sup></b> | <b>12 \_ 1<sup>0</sup></b> | <b>12 \_ 0<sup>0</sup></b> | <b>11 \_ 1<sup>1</sup></b> | <b>11 \_ 0</b> | <b>10 \_ 1</b> | <b>10 \_ 0</b> | <b>9 \_ 3<sup>7</sup></b> |
| Separate Alphablendung | Ja | Ja | Ja | Ja | Ja | Ja | Ja | Ja |
| Spiegelung einmal | Ja | Ja | Ja | Ja | Ja | Ja | Ja | Ja |
| Überlappende Scheitelpunktelemente | Ja | Ja | Ja | Ja | Ja | Ja | Ja | Ja |
| Unabhängige Schreibmasken | Ja | Ja | Ja | Ja | Ja | Ja | Ja | Ja |
| Instancing | Ja | Ja | Ja | Ja | Ja | Ja | Ja | Ja<sup>7</sup> |
| Nonpowers-of-2 bedingt<sup>3</sup> | Nein | Nein | Nein | Nein | Nein | Nein | Nein | Ja |
| Nonpowers-of-2 bedingungslos<sup>4</sup> | Ja | Ja | Ja | Ja | Ja | Ja | Ja | Nein |

## <a name="feature-support-for-feature-levels-9_2-and-9_1"></a>Featureunterstützung für Featureebenen 9_2 und 9_1

Die folgenden Features sind für die aufgeführten Featureebenen verfügbar. Die Überschriften in der oberen Zeile sind Direct3D-Featureebenen. Die Überschriften in der linken Spalte sind Features. Siehe auch [Fußnoten für die Tabellen](#footnotes-for-the-tables).

| \\Featureebene | 9 \_ 2 | 9 \_ 1 |
|-|-|-|
| Shadermodell (D3D11) | 2.0 (4 \_ 0 \_ Level \_ 9 \_ 1) | 2.0 (4 \_ 0 \_ Level \_ 9 \_ 1) |
| Shadermodell (D3D12) | Nicht zutreffend | Nicht zutreffend |
| [Gekachelte Ressourcen](tiled-resources.md) | Nein | Nein |
| [Konservative Rasterung](conservative-rasterization.md) | Nein | Nein |
| [Rasterizer-Reihenfolgenansichten](rasterizer-order-views.md) | Nein | Nein |
| [Mindest-/Maximalfilter](/windows/win32/api/D3D11/ne-d3d11-d3d11_filter) | Nein | Nein |
| Standardpuffer zuordnen | Nein | Nein |
| [Von Shader festgelegter Schablonenreferenzwert](shader-specified-stencil-reference-value.md) | Nein | Nein |
| Typierte ungeordnete Zugriffsansichtslasten | Nein | Nein |
| [Geometrie-Shader](/previous-versions/bb205146(v=vs.85)) | Nein | Nein |
| [StreamEnd](./d3d10-graphics-programming-guide-output-stream-stage.md) | Nein | Nein |
| [DirectCompute/Compute-Shader](direct3d-11-advanced-stages-compute-shader.md) | Nicht zutreffend | Nicht zutreffend |
| [Hülle und Domänen-Shader](direct3d-11-advanced-stages-tessellation.md) | Nein | Nein |
| [Texturressourcenarrays](overviews-direct3d-11-resources-textures-intro.md) | Nein | Nein |
| [Cubemap-Ressourcenarrays](overviews-direct3d-11-resources-textures-intro.md) | Nein | Nein |
| [BC4/BC5-Komprimierung](../direct3d10/d3d10-graphics-programming-guide-resources-block-compression.md) | Nein | Nein |
| <b>\\Featureebene</b> | <b>9 \_ 2</b> | <b>9 \_ 1</b> |
| [BC6H/BC7-Komprimierung](texture-block-compression-in-direct3d-11.md) | Nein | Nein |
| [Alpha-to-Coverage](./d3d10-graphics-programming-guide-blend-state.md) | Nein | Nein |
| [Erweiterte Formate (BGRA, so weiter)](overviews-direct3d-11-devices-downlevel-exceptions.md) | Ja | Ja |
| [10-Bit-XR-Format mit hoher Farbtiefe](overviews-direct3d-11-devices-downlevel-exceptions.md) | Nicht zutreffend | Nicht zutreffend |
| [Logikvorgänge (Ausgabefusion)](/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) | Nein | Nein |
| Zielunabhängige Rasterung | Nein | Nein |
| [Mehrere Renderziel (MRT) mit ForcedSampleCount 1](/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) | Nein | Nein |
| UAV-Slots | Nicht zutreffend | Nicht zutreffend |
| UAVs in jeder Phase | Nicht zutreffend | Nicht zutreffend |
| [Maximale Anzahl erzwungener Stichproben für nur UAV-Rendering](/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) | Nicht zutreffend | Nicht zutreffend |
| Konstante Pufferaussetzung und Teilupdates | Ja<sup>1</sup> | Ja<sup>1</sup> |
| BPP-Formate (16 Bit pro Pixel) | Optional<sup>1</sup> | Optional<sup>1</sup> |
| Max. Texturdimension | 2048 | 2048 |
| Max. Cubemapdimension | 512 | 512 |
| Max Volume Extent | 256 | 256 |
| Maximale Textur wiederholen | 2048 | 128 |
| <b>\\Featureebene</b> | <b>9 \_ 2</b> | <b>9 \_ 1</b> |
| Max. Anisotropie | 16 | 2 |
| Max. Anzahl primitiver Typen | 1048575 | 65.535 |
| Max. Scheitelpunktindex | 1048575 | 65534 |
| Max. Eingabeslots | 16 | 16 |
| Gleichzeitige Renderziele | 1 | 1 |
| Okklusionsabfragen | Ja | Nein |
| Separate Alphablendung | Ja | Nein |
| Spiegelung einmal | Ja | Nein |
| Überlappende Vertexelemente | Ja | Nein |
| Unabhängige Schreibmasken | Nein | Nein |
| Instancing | Nein | Nein |
| Nonpowers-of-2 bedingt<sup>3</sup> | Ja | Ja |
| Nonpowers-of-2 bedingungslos<sup>4</sup> | Nein | Nein |

## <a name="footnotes-for-the-tables"></a>Fußnoten für die Tabellen

<sup>0</sup> Erfordert die Direct3D 11.3- oder Direct3D 12-Runtime.

<sup>1</sup> Erfordert die Direct3D 11.1-Runtime.

<sup>2</sup> Shadermodell 5.0 und höher kann optional Shader mit doppelter Genauigkeit, erweiterte Shader mit doppelter Genauigkeit, die SAD4-Shaderanweisung und Shader mit teilweiser Genauigkeit unterstützen.  Um die Shadermodell 5.0-Optionen zu bestimmen, die für DirectX 11 verfügbar sind, rufen Sie [**ID3D11Device::CheckFeatureSupport**](/windows/win32/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport)auf. Die Kompatibilität hängt davon ab, auf welcher Hardware Sie ausgeführt werden. Shadermodell 5.1 und höher wird nur über die DirectX 12-API unterstützt, unabhängig von der verwendeten Featureebene. DirectX 11 unterstützt nur bis zu Shadermodell 5.0. Die DirectX 12-API sinkt nur auf Featureebene 11 \_ 0.

<sup>3</sup> Auf den Featureebenen \_ 9 1, \_ 9 2 und 9 \_ 3 unterstützt das Anzeigegerät die Verwendung von 2D-Texturen mit Dimensionen, die unter zwei Bedingungen keine Potenzen von zwei sind. Erstens kann nur eine MIP-Kartenebene für jede Textur erstellt werden, und zweitens sind keine Wrap-Samplermodi für Texturen zulässig (d.b. die **Member AddressU,** **AddressV** und **AddressW** von [**D3D11 \_ SAMPLER \_ DESC**](/windows/win32/api/D3D11/ns-d3d11-d3d11_sampler_desc) können nicht auf [**D3D11 \_ TEXTURE ADDRESS \_ \_ WRAP**](/windows/win32/api/D3D11/ne-d3d11-d3d11_texture_address_mode)festgelegt werden).

<sup>4</sup> Auf den Featureebenen 10 \_ 0, 10 \_ 1 und 11 \_ 0 unterstützt das Anzeigegerät bedingungslos die Verwendung von 2D-Texturen mit Dimensionen, die keine Potenzen von zwei sind.

<sup>5</sup> Vertex-Shader 2a mit 256 Anweisungen, 32 temporären Registern, statische Flusssteuerung von Tiefe 4, dynamische Flusssteuerung von Tiefe 24 und D3DVS20CAPS-PRÄDIKATION. \_ Pixelshader 2x mit 512 Anweisungen, 32 temporäre Register, statische Flusssteuerung von Tiefe 4, dynamische Flusssteuerung der Tiefe 24, D3DPS20CAPS \_ ARBITRARYSWIZZLE, D3DPS20CAPS \_ GRADIENTINSTRUCTIONS, D3DPS20CAPS \_ PREDICATION, D3DPS20CAPS \_ NODEPENDENTREADLIMIT und D3DPS20CAPS \_ NOTEXINSTRUCTIONLIMIT.

<sup>6</sup> Höhere Ebenen optional.

<sup>7</sup> Für Featureebene 9_3 werden nur die Renderingmethoden **Draw,** **DrawIndexed** und **DrawIndexInstanced** unterstützt. Auch für Featureebene 9_3 wird das Rendern von Punktlisten nur für das Rendern über **Zeichnen** unterstützt.

<sup>8</sup> Erfordert die Direct3D 12-Runtime.

<sup>9</sup> In der Direct3D 12-API gibt es Grenzwerte für die Anzahl der Deskriptoren in einem CBV/SRV/UAV-Heap. Weitere Informationen finden Sie [unter Hardwareebenen.](../direct3d12/hardware-support.md) Separat gibt es eine Beschränkung der Anzahl von UAVs in allen Deskriptortabellen in allen Phasen, die auf [der Ressourcenbindungsebene](https://microsoft.github.io/DirectX-Specs/d3d/ResourceBinding.html#levels-of-hardware-support)basiert.

Ausführliche Informationen zur Formatunterstützung auf verschiedenen Hardwarefeatureebenen finden Sie unter:

- [DXGI-Formatunterstützung für Direct3D Feature Level 12.1-Hardware](../direct3ddxgi/hardware-support-for-direct3d-12-1-formats.md)
- [DXGI-Formatunterstützung für Direct3D Feature Level 12.0-Hardware](../direct3ddxgi/hardware-support-for-direct3d-12-0-formats.md)
- [DXGI-Formatunterstützung für Direct3D-Featureebene 11.1-Hardware](../direct3ddxgi/format-support-for-direct3d-11-1-feature-level-hardware.md)
- [DXGI-Formatunterstützung für Direct3D Feature Level 11.0-Hardware](../direct3ddxgi/format-support-for-direct3d-11-0-feature-level-hardware.md)
- [Hardwareunterstützung für Direct3D 10Level9-Formate](/previous-versions/ff471324(v=vs.85))
- [Hardwareunterstützung für Direct3D 10.1-Formate](/previous-versions/cc627091(v=vs.85))
- [Hardwareunterstützung für Direct3D 10-Formate](/previous-versions/cc627090(v=vs.85))

## <a name="related-topics"></a>Zugehörige Themen

* [Direct3D 11 auf kompatibler Hardware](overviews-direct3d-11-devices-downlevel.md)
* [Hardwarefeatureebenen (Direct3D 12)](../direct3d12/hardware-feature-levels.md)