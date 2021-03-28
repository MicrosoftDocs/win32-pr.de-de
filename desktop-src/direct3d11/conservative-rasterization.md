---
title: Direct3D 11,3 konservative rasterisierung
description: Die konservative rasterisierung sorgt für ein gewisses Maß an Sicherheit für das Pixel Rendering. Dies ist insbesondere bei Algorithmen zum Erkennen von Kollisionen hilfreich.
ms.assetid: 83F223C0-9282-4149-86CF-471B88829F76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 003cb7e31c1380943318b34f9308f6b5e72d6e51
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104209325"
---
# <a name="direct3d-113-conservative-rasterization"></a>Direct3D 11,3 konservative rasterisierung

Die konservative rasterisierung sorgt für ein gewisses Maß an Sicherheit für das Pixel Rendering. Dies ist insbesondere bei Algorithmen zum Erkennen von Kollisionen hilfreich.

-   [Übersicht](#overview)
-   [Interaktionen mit der Pipeline](#interactions-with-the-pipeline)
-   [Implementierungsdetails](#implementation-details)
-   [API-Zusammenfassung](#api-summary)
-   [Zugehörige Themen](#related-topics)

## <a name="overview"></a>Übersicht

Die konservative rasterisierung bedeutet, dass alle Pixel, die zumindest teilweise von einem gerenderten primitiven abgedeckt werden, rasterisiert sind. Dies bedeutet, dass der Pixelshader aufgerufen wird. Normales Verhalten ist die Stichprobenentnahme, die nicht verwendet wird, wenn die konservative rasterisierung aktiviert ist.

Die konservative rasterisierung ist in einer Reihe von Situationen nützlich, einschließlich der Sicherheit bei der Kollisionserkennung, der Okklusions Erkennung und der Sichtbarkeits Erkennung.

Die folgende Abbildung zeigt z. b. ein grünes Dreieck, das mit konservativer rasterisierung gerendert wird. Der braune Bereich wird als "Ungewissheit-Region" bezeichnet. bei einer Region, in der Rundungsfehler und andere Probleme zu den genauen Dimensionen des Dreiecks eine gewisse Ungewissheit führen. Die roten Dreiecke in jedem Scheitelpunkt zeigen, wie der unsicher-Bereich berechnet wird. Die großen grauen Quadrate zeigen die Pixel an, die gerendert werden. In den rosa Quadraten werden Pixel angezeigt, die mit der "Top-Left"-Regel gerendert werden. diese wird wiedergegeben, wenn der Rand des Dreiecks den Rand der Pixel überschreitet. Es können falsch positive Ergebnisse (Pixel festgelegt werden, die nicht vorhanden sein sollten) sein, die das System normalerweise aber nicht immer umschlägt.

![zeigt die linke obere Regel an.](images/conservative-rasterization-0.png)

## <a name="interactions-with-the-pipeline"></a>Interaktionen mit der Pipeline

Ausführliche Informationen dazu, wie die konservative rasterisierung mit der Grafik Pipeline interagiert, finden Sie unter [D3D12 konservative Rasterung](/windows/desktop/direct3d12/conservative-rasterization).

## <a name="implementation-details"></a>Details zur Implementierung

Der Typ der in Direct3D 12 unterstützten rasterisierung wird manchmal als "überschätzte konservative rasterisierung" bezeichnet. Es gibt auch das Konzept der "unterschätzten konservative rasterisierung", was bedeutet, dass nur Pixel, die vollständig von einem gerenderten primitiven abgedeckt werden, rasterisiert werden. Unterschätzte konservative rasterisierungsinformationen sind über den Pixelshader durch die Verwendung von Eingabe Abdeckungs Daten verfügbar, und nur die überschätzte konservative rasterisierung ist als rasterisierungsmodus verfügbar.

Wenn ein beliebiger Teil eines primitiven ein Pixel überlappt, wird dieses Pixel als abgedeckt betrachtet und dann rasteriert. Wenn ein Rand oder eine Ecke eines primitiven entlang der Kante oder Ecke eines Pixels fällt, ist die Anwendung der "Top-Left-Regel" Implementierungs spezifisch. Bei Implementierungen, die degenerierte Dreiecke unterstützen, muss ein degeneriertes Dreieck an einer Kante oder Ecke jedoch mindestens ein Pixel abdecken.

Konservative Rasterung-Implementierungen können sich auf unterschiedlichen Hardware unterscheiden, und es werden falsche positiv Ergebnisse erzeugt. Dies bedeutet, dass Sie fälschlicherweise festlegen können, dass Pixel abgedeckt werden. Dies kann aufgrund von Implementierungs spezifischen Details auftreten, wie z. b. primitive ansteigende oder Ausrichtungsfehler, die in den in der rasterisierung verwendeten festen Punkt Vertex-Koordinaten enthalten sind. Der Grund, warum falsch positive Ergebnisse (in Bezug auf Scheitelpunkt Koordinaten mit festem Punkt) gültig sind, liegt darin, dass einige falsch positive Ergebnisse erforderlich sind, damit eine Implementierung die Abdeckungs Auswertung für nach gestellte Scheitel Punkte (d. h. vertexkoordinaten, die von Gleit Komma Zahlen in den in der Rasterizer verwendeten Fixed-Punkt 16,8 konvertiert wurden, berücksichtigen jedoch die Abdeckung, die von den ursprünglichen Gleit Komma Koordinaten des Vertex erzeugt wurde.

Konservative Rasterung-Implementierungen generieren keine falschen negativen in Bezug auf die Vertex-Gleit Komma Koordinaten für nicht degenerierte Post-Snap-primitive: Wenn ein beliebiger Teil eines primitiven einen Teil eines Pixels überlappt, wird dieses Pixel rasteriert.

Dreiecke, die deseriell sind (doppelte Indizes in einem Index Puffer oder kollinear in 3D) oder nach der fest Komma Konvertierung (kollinear Vertices in the Rasterizer) deseriell werden. Beide sind ein gültiges Verhalten. Degenerierte Dreiecke müssen als "zurück" betrachtet werden. Wenn also ein bestimmtes Verhalten für eine Anwendung erforderlich ist, kann es die Hintergrund Erkennung oder den Test für die Vorderseite verwenden. Degenerierte Dreiecke verwenden die den Scheitel Punkten 0 zugewiesenen Werte für alle interpoliert-Werte.

Es gibt drei Ebenen von Hardwareunterstützung, zusätzlich zur Möglichkeit, dass die Hardware dieses Feature nicht unterstützt.

-   Ebene 1 unterstützt 1/2 Pixel-Unsicherheitsbereiche, und keine Post-Snap-Ins werden deaktiviert. Dies eignet sich gut für das gekachelte Rendering, einen Textur Atlas, eine Licht Zuordnungs Generierung und unter Pixel Schatten Zuordnungen.
-   Ebene 2 fügt Post-Snap-in-und 1/256-Sicherheitsbereiche hinzu. Außerdem wird Unterstützung für die CPU-basierte Beschleunigung von Algorithmen (z. b. voxelization) hinzugefügt.
-   Ebene 3 fügt 1/512-Sicherheitsbereiche, innere Eingabe Abdeckung und Unterstützung der Okklusions Berechnung ein. Die Eingabe Abdeckung fügt den neuen Wert der `SV_InnerCoverage` High Level Shading Language (HLSL) hinzu. Dies ist eine ganzzahlige 32-Bit-Ganzzahl, die für die Eingabe an einen PixelShader angegeben werden kann, und stellt die unterschätzten Informationen zur konservativen rasterisierung dar (d. h., ob ein Pixel garantiert vollständig abgedeckt ist).

## <a name="api-summary"></a>API-Zusammenfassung

Die folgenden Methoden, Strukturen, Enumerationsklassen und Hilfsklassen verweisen auf die konservative rasterisierung:

-   [**D3D11 \_ Raster \_ DESC2**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_rasterizer_desc2) : Struktur mit der Beschreibung des Rasterizers. Beachten Sie die CD3D12 \_ Raster \_ DESC2 Helper-Klasse zum Erstellen von Raster-Beschreibungen.
-   [**D3D11 \_ Konservativer \_ rasterisierungsmodus \_**](/windows/desktop/api/D3D11_3/ne-d3d11_3-d3d11_conservative_rasterization_mode) : Enumeration-Werte für den Modus (ein oder aus).
-   [**D3D11 \_ Feature \_ Data \_ D3D11 \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) : die Struktur, die die Ebene der Unterstützung enthält.
-   [**D3D11 \_ Konservative \_ rasterization- \_ Ebene**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_conservative_rasterization_tier) : Enumerationswerte für jede Ebene der Unterstützung durch die Hardware.
-   [**ID3D11Device:: checkfeaturesupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) : Methode für den Zugriff auf die unterstützten Funktionen.

## <a name="related-topics"></a>Zugehörige Themen
* [Direct3D 11,3-Features](direct3d-11-3-features.md)