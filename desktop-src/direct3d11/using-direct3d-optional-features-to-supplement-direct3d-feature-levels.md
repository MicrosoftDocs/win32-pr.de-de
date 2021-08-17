---
title: Verwenden von Direct3D 11-Featuredaten zur Ergänzung von Direct3D-Featureebenen
description: Erfahren Sie, wie Sie die Geräteunterstützung für optionale Features überprüfen, einschließlich Features, die in neueren Versionen von Windows hinzugefügt wurden.
ms.assetid: 91D9706A-47C5-4220-8AC7-167095E74F74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03c2e7392f576b8c0dca059a4ef2fdd2ee6415230e5fd41e497d60899332f674
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124048"
---
# <a name="using-direct3d-11-feature-data-to-supplement-direct3d-feature-levels"></a>Verwenden von Direct3D 11-Featuredaten zur Ergänzung von Direct3D-Featureebenen

Erfahren Sie, wie Sie die Geräteunterstützung für optionale Features überprüfen, einschließlich Features, die in neueren Versionen von Windows hinzugefügt wurden.

[Direct3D-Featureebenen](overviews-direct3d-11-devices-downlevel-intro.md) geben klar definierte Sätze von GPU-Funktionen an, die ungefähr verschiedenen Generationen von Grafikhardware entsprechen. Dies vereinfacht die Überprüfung der Hardware-Kompatibilität erheblich und bietet außerdem eine konsistente Benutzeroberfläche für eine Vielzahl verschiedener Geräte.

Zur Berücksichtigung einiger Abweichungen zwischen verschiedenen Hardwareimplementierungen , einschließlich Legacyhardware, mobiler Hardware und moderner Hardware, werden einige Features als optional betrachtet. Die Unterstützung für diese Features kann durch Aufrufen von [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) und Bereitstellen der relevanten D3D11 \_ FEATURE \_ DATA-Struktur bestimmt \_ \* werden. In diesem Thema werden die verschiedenen optionalen Direct3D 11-Features beschrieben, wie einige von ihnen zusammenarbeiten und wie Sie die Überprüfung auf jedes einzelne optionale Feature vermeiden können.

## <a name="how-to-check-for-optional-feature-support"></a>Überprüfen auf optionale Featureunterstützung

Rufen Sie [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport)auf, und geben Sie die Struktur an, die das optionale Feature darstellt, das Sie verwenden möchten. Wenn die Methode **S \_ OK** zurückgibt, bedeutet dies, dass Sie eine Version der Direct3D-Runtime verwenden, die das optionale Feature unterstützt. Wenn **E \_ INVALIDARG** zurückgegeben wird, bedeutet dies, dass Sie über eine Version der Direct3D 11-Runtime verfügen, bevor das optionale Feature hinzugefügt wurde. Dies bedeutet, dass das optionale Feature nicht verfügbar ist, zusammen mit allen anderen optionalen Features, die in derselben Version von Direct3D 11 oder höher eingeführt wurden.

## <a name="can-i-minimize-the-work-required-for-feature-support-checks"></a>Kann ich den Aufwand minimieren, der für Funktionsunterstützungsprüfungen erforderlich ist?

Zusätzlich zur richtigen Direct3D 11-Runtime (normalerweise einer Windows-Version zugeordnet) muss der Grafiktreiber auch aktuell genug sein, um das optionale Feature zu unterstützen. Die WDDM-Spezifikationen erfordern optionale Features, die unterstützt werden müssen, wenn die Hardware sie unterstützen kann. Wenn ein Grafiktreiber also eines der optionalen Features unterstützt, die in einer bestimmten Version von Windows hinzugefügt wurden, bedeutet dies in der Regel, dass der Grafiktreiber die anderen Features unterstützt, die in dieser Version von Windows hinzugefügt wurden. Wenn ein Gerätetreiber beispielsweise Schatten auf Featureebene 9 unterstützt, wissen Sie, dass der Gerätetreiber mindestens WDDM 1.2 ist.

**Hinweis**  Wenn ein Microsoft [Direct3D-Gerät feature level](overviews-direct3d-11-devices-downlevel-intro.md) 11.1 unterstützt, werden alle optionalen Features, die durch [**D3D11 \_ FEATURE DATA \_ \_ D3D11 \_ OPTIONS**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) angegeben werden, mit Ausnahme von **SAD4ShaderInstructions** und **ExtendedDoublesShaderInstructions** automatisch unterstützt.

Die Runtime legt die folgenden Gruppierungen von Mitgliedern immer identisch fest. Das heißt, alle Werte in einer Gruppierung sind **TRUE** oder **FALSE** zusammen:

-   **DiscardAPIsSeenByDriver** und **FlagsForUpdateAndCopySeenByDriver**
-   **ClearView,** **CopyWithOverlap,** **ConstantBufferPartialUpdate,** **ConstantBufferOffsetting** und **MapNoOverwriteOnDynamicConstantBuffer**
-   **MapNoOverwriteOnDynamicBufferSRV** und **MultisampleRTVWithForcedSampleCountOne**

**Optionen auf Featureebene 11.2 ([**D3D11 \_ FEATURE \_ D3D11 \_ OPTIONS1**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature)):** Die von diesem Feld angegebenen optionalen Features sind unabhängig und müssen einzeln überprüft werden.

### <a name="feature-support-on-windows-rt-81-and-windows-phone-81-devices"></a>Featureunterstützung auf Windows RT 8.1- und Windows Phone 8.1-Geräten

Windows RT Tablet-Geräte können eine Vielzahl von Featureebenen und optionalen Features unterstützen, sind für einen geringeren Energieverbrauch optimiert und verwenden integrierte Grafiken anstelle diskreter GPUs. Windows Store Apps für ARM-Geräte müssen Featureebene 9.1 unterstützen. DirectX-Apps für Windows RT sollten von optionalen Features profitieren, die Energie und Zyklen sparen können ( z. B. einfache Instanziierung ), wenn sie verfügbar sind.

Windows Phone 8 mobile Geräte unterstützen Featureebene 9.3 mit bestimmten optionalen Features. Informationen zu Windows Phone 8 finden [Sie unter Direct3D feature level \_ 9 3 (Direct3D-Featureebene 9 3).](/previous-versions/windows/apps/jj714085(v=vs.105))

## <a name="what-are-the-direct3d-11-optional-features"></a>Was sind die optionalen Direct3D 11-Features?

Im weiteren Verlauf dieses Artikels werden die optionalen Features beschrieben, die in Direct3D 11.2 verfügbar sind. Features werden nach dem Hinzufügen in chronologischer Reihenfolge beschrieben, damit Sie ein Gefühl dafür erhalten können, welche Features in verschiedenen Versionen von Direct3D 11 vorhanden sind.

## <a name="optional-compute-shader-support-for-feature-level-10"></a>Optionale Unterstützung von Compute-Shadern für Featureebene 10

Das folgende Feature ist für Geräte auf Featureebene 10 immer verfügbar:

**[**D3D11 \_ FEATURE \_ DATA \_ D3D10 X HARDWARE OPTIONS (FEATUREDATEN D3D10 \_ X \_ \_ HARDWAREOPTIONEN):**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d10_x_hardware_options)** Wenn dies **TRUE** ist, unterstützt das Gerät Compute-Shader. Dies schließt unterstützung für unformatierte und strukturierte Puffer ein.

Wenn das Gerät der Featureebene \_ 10 0 oder \_ 10 1 dieses Feature unterstützt, ist es nicht garantiert, dass das Gerät Compute-Shader 4.1 unterstützt. Apps sollten darauf vorbereitet sein, auf einen Computeshader 4.0 zurückzugehen, wenn [**ID3D11Device::CreateComputeShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createcomputeshader) eine Ausnahme mit einem Computeshader 4.1-Programm auslöst.

## <a name="optional-capabilities-for-feature-level-9"></a>Optionale Funktionen für Featureebene 9

Die folgenden Features werden ab Windows 8 für Featureebene 9 hinzugefügt:

**[**D3D11 \_ FEATURE \_ DATA \_ D3D9 \_ OPTIONS**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_options):** Gibt die Unterstützung für die Adressierung von Wraptextur mit Texturen ohne Leistung von 2 Texturen an. Wenn dies unterstützt wird, kann D3D11 \_ TEXTURE ADDRESS MODE WRAP mit solchen \_ \_ \_ Texturen verwendet werden.

**[**D3D11 \_ FEATURE \_ DATA \_ D3D9 \_ SHADOW \_ SUPPORT**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_shadow_support):** Gibt unterstützung für Vergleichssamplings in Shadermodell 4.0 Featureebene 9 x \_ Shadern an. Dies wird für Tiefentests in Pixel-Shadern verwendet, sodass gängige Techniken wie Schattenzuordnung und Schablonen unterstützt werden.

Das folgende Feature wurde ab Windows 8.1 für Geräte der Featureebene 9 hinzugefügt:

**[**D3D11 \_ FEATURE \_ DATA \_ D3D9 \_ SIMPLE \_ INSTANCING \_ SUPPORT**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_simple_instancing_support):** Gibt unterstützung für einfache Instanziierungsfunktionen an, die möglicherweise auf DirectX 9-Level-Hardware verfügbar sind. Einfache Instanziierung bedeutet, dass alle **InstanceDataStepRate-Member** der [**D3D11 \_ INPUT ELEMENT \_ \_ DESC-Strukturen,**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_input_element_desc) die zum Definieren des Eingabelayouts verwendet werden, gleich 1 sein müssen. Geräte, die Featureebene 9.3 oder höher unterstützen, bieten bereits vollständige Unterstützung für die Instanziierung.

## <a name="optional-floating-point-precision-support-for-shader-programs"></a>Optionale Unterstützung der Gleitkommagenauigkeit für Shaderprogramme

**[**D3D11 \_ FEATURE \_ DATA \_ SHADER MIN PRECISION \_ \_ \_ SUPPORT**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_shader_min_precision_support):** Die Felder in dieser Struktur geben die Länge von Gleitkommazahlen an, wenn die minimale Genauigkeit aktiviert ist, oder 0, wenn nur die volle 32-Bit-Gleitkommagenauigkeit unterstützt wird.

Bei Geräten der Featureebene 9 kann sich die mindeste Genauigkeit für den Vertex-Shader vom Pixel-Shader unterscheiden. Die Genauigkeit für den Vertexshader wird im **Feld AllOtherShaderStagesMinPrecision** angegeben.

**[**D3D11 \_ FEATURE \_ DATA \_ DOUBLES:**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_doubles)** Geräte auf Featureebene 11 können Berechnungen mit doppelter Genauigkeit in Shadermodell 5.0-Programmen unterstützen. Die Unterstützung von Berechnungen mit doppelter Genauigkeit innerhalb des Shaders bedeutet, dass Gleitkommastellen innerhalb des Compute-Shaderprogramms in Doubles konvertiert werden können, was den Vorteil einer Berechnung mit höherer Genauigkeit innerhalb jedes Shaderdurchlaufs bietet. Die Zahlen mit doppelter Genauigkeit müssen wieder in Gleitkommawerte konvertiert werden, bevor sie in den Ausgabepuffer geschrieben werden. Beachten Sie, dass die Division mit doppelter Genauigkeit nicht unbedingt unterstützt wird.

## <a name="additional-capabilities-for-direct3d-112"></a>Zusätzliche Funktionen für Direct3D 11.2

Direct3D 11.2 fügt vier neue optionale Features hinzu, die von Direct3D 11-Geräten unterstützt werden können. Diese Features befinden sich in der [**D3D11 \_ FEATURE \_ DATA \_ D3D11 \_ OPTIONS1-Struktur:**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options1)

**TiledResourcesTier:** Gibt die Unterstützung für gekachelte Ressourcen und den unterstützten Tarif an.

**MinMaxFiltering:** Gibt die Unterstützung für die Filteroptionen D3D11 \_ FILTER \_ MINIMUM und \_ \* D3D11 FILTER MAXIMUM \_ \_ \_ \* an, die das Filterergebnis mit dem minimalen (oder maximalen) Wert vergleichen. Siehe [**D3D11 \_ FILTER**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_filter).

**ClearViewAlsoSupportsDepthOnlyFormats:** Gibt die Unterstützung für das Löschen von Tiefenpufferressourcensichten an.

**MapOnDefaultBuffers:** Gibt die Unterstützung für die Zuordnung von Renderzielpuffern an, die mit dem **D3D11 \_ USAGE \_ DEFAULT-Flag** erstellt wurden.

## <a name="tile-based-rendering"></a>Kachelbasiertes Rendering

**[**D3D11 \_ FEATURE DATA ARCHITECTURE \_ \_ \_ INFO**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_architecture_info):** Gibt an, ob das Grafikgerät Renderingbefehle batchet und standardmäßig kachelbasiertes Rendering ausführt. Dies kann als Hinweis für die Optimierung der Grafik-Engine verwendet werden.

## <a name="optional-features-for-development-and-debugging"></a>Optionale Features für Entwicklung und Debuggen

**D3D11 \_ FEATURE \_ DATA \_ D3D11 \_ OPTIONS::D iscardAPIsSeenByDriver:** Sie können dieses Element während der Entwicklung überwachen, um Legacytreiber auf Hardware auszuschließen, bei denen [**DiscardView**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardview) und [**DiscardResource**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardresource) andernfalls von Vorteil waren.

**[**D3D11 \_ FEATURE DATA MARKER \_ \_ \_ SUPPORT**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_marker_support):** Dies wird unterstützt, wenn die Hardware und der Treiber die Datenmarkierung für die GPU-Profilerstellung unterstützen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Geräte](overviews-direct3d-11-devices.md)
</dt> </dl>

 

 