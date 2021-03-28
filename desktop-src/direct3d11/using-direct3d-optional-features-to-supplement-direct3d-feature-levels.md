---
title: Verwenden von Direct3D 11 Feature-Daten zum ergänzen von Direct3D-Funktionsebenen
description: Erfahren Sie, wie Sie die Geräte Unterstützung auf optionale Features überprüfen, einschließlich der Features, die in neueren Versionen von Windows hinzugefügt wurden.
ms.assetid: 91D9706A-47C5-4220-8AC7-167095E74F74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dcc770812281ea89e8ebb68065aa68a00e1887d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315591"
---
# <a name="using-direct3d-11-feature-data-to-supplement-direct3d-feature-levels"></a>Verwenden von Direct3D 11 Feature-Daten zum ergänzen von Direct3D-Funktionsebenen

Erfahren Sie, wie Sie die Geräte Unterstützung auf optionale Features überprüfen, einschließlich der Features, die in neueren Versionen von Windows hinzugefügt wurden.

[Direct3D featureebenen](overviews-direct3d-11-devices-downlevel-intro.md) zeigen klar definierte Sätze von GPU-Funktionen an, die ungefähr verschiedenen Generationen von Grafikhardware entsprechen. Dadurch wird die Überprüfung der Hardware Qualität erheblich vereinfacht, und es wird auch eine konsistente Darstellung über eine Vielzahl verschiedener Geräte hinweg ermöglicht.

Zum berücksichtigen einiger Abweichungen in verschiedenen Hardware Implementierungen, einschließlich Legacy Hardware, Mobile Hardware und moderner Hardware, werden einige Features als optional eingestuft. Die Unterstützung für diese Features kann durch Aufrufen von [**ID3D11Device:: checkfeaturesupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) und durch Bereitstellen der relevanten D3D11- \_ Funktionsdaten Struktur bestimmt werden \_ \_ \* . In diesem Thema werden die verschiedenen optionalen Direct3D 11-Features beschrieben und erläutert, wie einige von Ihnen zusammenarbeiten und wie Sie die Überprüfung der einzelnen optionalen Features vermeiden können.

## <a name="how-to-check-for-optional-feature-support"></a>Überprüfen der optionalen Funktions Unterstützung

Nennen Sie [**ID3D11Device:: checkfeaturesupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport), und geben Sie die Struktur an, die das optionale Feature darstellt, das Sie verwenden möchten. Wenn die Methode **S \_ OK** zurückgibt, bedeutet dies, dass Sie eine Version der Direct3D-Laufzeit verwenden, die das optionale Feature unterstützt. Wenn **E \_ invalidArg** zurückgegeben wird, bedeutet dies, dass Sie eine Version von Direct3D 11 Runtime von vor dem Hinzufügen des optionalen Features haben. Dies bedeutet, dass das optionale Feature nicht verfügbar ist, zusammen mit allen anderen optionalen Features, die in derselben Version von Direct3D 11 oder höher eingeführt wurden.

## <a name="can-i-minimize-the-work-required-for-feature-support-checks"></a>Kann ich den Arbeitsaufwand für die Überprüfung von Featureunterstützung minimieren?

Zusätzlich zu der Direct3D 11-Laufzeit (in der Regel mit einer Windows-Version verknüpft) muss der Grafiktreiber ebenfalls aktuell genug sein, um das optionale Feature zu unterstützen. Die WDDM-Spezifikationen erfordern optionale Features, die unterstützt werden, wenn Sie von der Hardware unterstützt werden. Wenn ein Grafiktreiber eine der optionalen Features unterstützt, die in einer bestimmten Windows-Version hinzugefügt wurden, bedeutet dies in der Regel, dass der Grafiktreiber die anderen Features unterstützt, die in dieser Windows-Version hinzugefügt wurden. Wenn ein Gerätetreiber z. b. Schatten auf Featureebene 9 unterstützt, wissen Sie, dass der Gerätetreiber mindestens WDDM 1,2 ist.

**Hinweis**    Wenn ein Microsoft Direct3D-Gerät die [Featureebene](overviews-direct3d-11-devices-downlevel-intro.md) 11,1 unterstützt, werden alle optionalen Features, die von [**D3D11 \_ Feature \_ Data \_ D3D11- \_ Optionen**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) angegeben werden, automatisch unterstützt, ausgenommen **SAD4ShaderInstructions** und **extendeddoublesshaderinstructions**.

Die Laufzeit legt die folgenden Gruppierungen von Membern immer identisch fest. Das heißt, dass alle Werte in einer Gruppierung gleich " **true** " oder " **false** " sind:

-   **Verwerfen von "wridapisseenbydriver** " und " **flagsforupdateandcopyseenbydriver** "
-   **Clearview**, **copywithüberlappung**, **constantbufferpartialupdate**, **constantbufferoffsetting** und **mapnooverwrite teondynamicconstantbuffer**
-   **Mapnooverwrite teondynamicbuffersrv** und **multisamplertvwithforcedsamplerattone**

**Optionen auf Featureebene 11,2 ([**D3D11 \_ Feature \_ D3D11 \_ OPTIONS1**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature)):** die optionalen Funktionen, die von diesem Feld angegeben werden, sind unabhängig und müssen einzeln geprüft werden.

### <a name="feature-support-on-windows-rt-81-and-windows-phone-81-devices"></a>Funktions Unterstützung auf Windows RT 8,1-und Windows Phone 8,1-Geräten

Windows RT-Tablet-Geräte können eine Vielzahl von featureebenen und optionalen Features unterstützen, für reduzierten Stromverbrauch optimiert werden und anstelle von diskreten GPUs integrierte Grafiken verwenden. Windows Store-Apps für ARM-Geräte müssen die Featureebene 9,1 unterstützen. DirectX-Apps für Windows RT sollten optionale Features nutzen, mit denen Strom und Zyklen eingespart werden können, z. b. einfache Instanziierung, wenn diese verfügbar sind.

Windows Phone 8 Mobile Geräte unterstützen die Featureebene 9,3 mit bestimmten optionalen Features. Weitere Informationen finden Sie unter [Direct3D Feature Level 9 \_ 3 für Windows Phone 8](/previous-versions/windows/apps/jj714085(v=vs.105)).

## <a name="what-are-the-direct3d-11-optional-features"></a>Was sind die Direct3D 11 optionalen Features?

Im weiteren Verlauf dieses Artikels werden die in Direct3D 11,2 verfügbaren optionalen Features beschrieben. Funktionen werden in chronologischer Reihenfolge nach dem Hinzufügen beschrieben, damit Sie verstehen können, welche Features in verschiedenen Versionen von Direct3D 11 enthalten sind.

## <a name="optional-compute-shader-support-for-feature-level-10"></a>Optionale Unterstützung von Compute-Shader für Featureebene 10

Das folgende Feature ist für Geräte auf Featureebene 10 immer verfügbar:

**[**D3D11 \_ Feature \_ Data \_ d3d10 \_ X \_ Hardware \_ Optionen**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d10_x_hardware_options):** wenn dies der **Fall** ist, unterstützt das Gerät Compute-Shader. Dazu gehört auch die Unterstützung für Rohdaten und strukturierte Puffer.

Wenn die Featureebene 10 \_ 0 oder 10 \_ 1 dieses Feature unterstützt, wird das Gerät nicht garantiert, dass Compute-Shader 4,1 unterstützt wird. Apps sollten darauf vorbereitet sein, auf einen Compute-Shader 4,0 zurückzugreifen zu können, wenn [**ID3D11Device:: kreatecomputeshader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createcomputeshader) eine Ausnahme mit einem Compute-Shader 4,1-Programm auslöst.

## <a name="optional-capabilities-for-feature-level-9"></a>Optionale Funktionen für Featureebene 9

Die folgenden Funktionen werden für die Featureebene 9 ab Windows 8 hinzugefügt:

**[**D3D11 \_ Feature \_ Data \_ d3d9 \_ Optionen**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_options):** gibt die Unterstützung für die Wrap-Textur Adressierung mit nicht-Power-2-Texturen an. Wenn dies unterstützt wird, \_ kann der D3D11 Texture \_ Address \_ Mode \_ Wrap mit solchen Texturen verwendet werden.

**[**D3D11 \_ Feature \_ Data \_ d3d9 \_ Shadow- \_ Unterstützung**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_shadow_support):** gibt die Unterstützung für Vergleichs Samplern im Shader-Modell 4,0-Featureebene 9 x-Shader an \_ . Dies wird für tiefen Tests in Pixel-Shadern verwendet und ermöglicht die Unterstützung allgemeiner Techniken wie z. b. Schatten Zuordnung und Schablonen.

Das folgende Feature wurde für Geräte mit Featureebene 9 ab Windows 8.1 hinzugefügt:

**[**D3D11 \_ Feature \_ Data \_ d3d9 \_ Simple- \_ instanziierungsunterstützung \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_simple_instancing_support):** gibt Unterstützung für einfache instanziierungsfunktionen an, die möglicherweise auf DirectX 9-Ebenen-Hardware verfügbar sind Einfache Instanziierung bedeutet, dass alle **instancedatasteprate** -Member der [**D3D11 \_ input- \_ Element \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_input_element_desc) -Strukturen, die zum Definieren des Eingabe Layouts verwendet werden, gleich 1 sein müssen. Geräte, die Funktionsebene 9,3 oder höher unterstützen, beinhalten bereits vollständige Unterstützung für die Instanziierung

## <a name="optional-floating-point-precision-support-for-shader-programs"></a>Optionale Unterstützung für Gleit Komma Genauigkeit für Shader-Programme

**[**D3D11- \_ Featuredaten- \_ \_ Shader minimale \_ \_ Genauigkeits \_ Unterstützung**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_shader_min_precision_support):** die Felder in dieser Struktur geben die Länge von Gleit Komma Zahlen an, wenn die minimale Genauigkeit aktiviert ist, oder 0, wenn nur die vollständige 32-Bit-Gleit Komma Genauigkeit unterstützt wird.

Bei Featureebene 9-Geräten kann sich die minimale Genauigkeit für den Vertexshader vom Pixelshader unterscheiden. Die Genauigkeit für den Vertex-Shader wird im Feld "Zuweisung von" Zuweisung "" **zugeordnet** .

**[**D3D11 \_ Feature \_ Data \_ Doubles**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_doubles):** Geräte auf Featureebene 11 können Berechnungen mit doppelter Genauigkeit in Shader-Modell 5,0-Programmen unterstützen. Die Unterstützung für Berechnungen mit doppelter Genauigkeit innerhalb des Shaders bedeutet, dass Gleit Komma Zahlen in das Compute-Shader-Programm konvertiert werden können. Dies bietet den Vorteil der Berechnung höherer Genauigkeit in jedem shaderdurchlauf. Die Zahlen mit doppelter Genauigkeit müssen zurück in float-Werte konvertiert werden, bevor Sie in den Ausgabepuffer geschrieben werden. Beachten Sie, dass die Division mit doppelter Genauigkeit nicht unbedingt unterstützt wird.

## <a name="additional-capabilities-for-direct3d-112"></a>Zusätzliche Funktionen für Direct3D 11,2

Direct3D 11,2 fügt vier neue optionale Features hinzu, die von Direct3D 11-Geräten unterstützt werden können. Diese Features befinden sich in der [**D3D11 \_ Feature \_ Data \_ D3D11 \_ OPTIONS1**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options1) -Struktur:

**Tiledresourcestier:** Gibt die Unterstützung für gekachelte Ressourcen an und gibt die unterstützte Ebene an.

**Minmaxfiltering:** Gibt Unterstützung für \_ \_ die maximalen Filteroptionen D3D11 Filter minimal \_ \* und D3D11 \_ Filter \_ \_ \* an, die das Filterergebnis mit dem minimalen (oder maximalen) Wert vergleichen. Siehe [**D3D11 \_ Filter**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_filter).

**Clearviewalsosupportsdepthonlyformats:** Gibt die Unterstützung für das Löschen von tiefen Puffer Ressourcen Ansichten an.

**Mapondefaultbuffers:** Gibt die Unterstützung für die Zuordnung von renderzielpuffern an, die mit dem **\_ \_ Standardflag D3D11**

## <a name="tile-based-rendering"></a>Kachel basiertes Rendering

**[**D3D11 \_ Feature \_ Data \_ Architecture \_ Info**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_architecture_info):** gibt an, ob das Grafikgerät das Rendern von Befehlen ausführt, und führt standardmäßig ein Kachel basiertes Rendering aus. Dies kann als Hinweis für die Optimierung der Grafik-Engine verwendet werden.

## <a name="optional-features-for-development-and-debugging"></a>Optionale Features für Entwicklung und Debuggen

**D3D11 \_ \_Featuredaten \_ D3D11 \_ Optionen::D iscardapisseenbydriver:** Sie können dieses Mitglied während der Entwicklung überwachen, um Legacy Treiber auf Hardware auszuschließen, bei denen " [**verwerfen**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardview) " und " [**verwerfen**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardresource) " möglicherweise anderweitig vorteilhaft waren.

**[**D3D11 \_ Feature \_ Data \_ Marker- \_ Unterstützung**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_marker_support):** Dies wird unterstützt, wenn Hardware und Treiber Daten Markierungen für die GPU-Profilerstellung unterstützen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Geräte](overviews-direct3d-11-devices.md)
</dt> </dl>

 

 