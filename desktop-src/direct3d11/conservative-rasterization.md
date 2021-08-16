---
title: Direct3D 11.3 Konservative Rasterung
description: Die konservative Rasterung erhöht die Sicherheit beim Pixelrendering, was insbesondere für Algorithmen zur Kollisionserkennung hilfreich ist.
ms.assetid: 83F223C0-9282-4149-86CF-471B88829F76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd33b7c7d237fc30adb349f1c1b24ce16c2740ce93fc97445a6e3f69d0949aeb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119408570"
---
# <a name="direct3d-113-conservative-rasterization"></a>Direct3D 11.3 Konservative Rasterung

Die konservative Rasterung erhöht die Sicherheit beim Pixelrendering, was insbesondere für Algorithmen zur Kollisionserkennung hilfreich ist.

-   [Übersicht](#overview)
-   [Interaktionen mit der Pipeline](#interactions-with-the-pipeline)
-   [Details zur Implementierung](#implementation-details)
-   [API-Zusammenfassung](#api-summary)
-   [Zugehörige Themen](#related-topics)

## <a name="overview"></a>Übersicht

Konservative Rasterung bedeutet, dass alle Pixel, die mindestens teilweise von einem gerenderten Primitiven abgedeckt sind, gerastert werden, was bedeutet, dass der Pixelshader aufgerufen wird. Das normale Verhalten ist die Stichprobenentnahme, die nicht verwendet wird, wenn die konservative Rasterung aktiviert ist.

Die konservative Rasterung ist in einer Reihe von Situationen nützlich, z. B. zur Sicherheit bei der Kollisionserkennung, Verdeckungs-Culling und Sichtbarkeitserkennung.

Die folgende Abbildung zeigt beispielsweise ein grünes Dreieck, das mit konservativer Rasterung gerendert wird. Der browne Bereich wird als "Unsicherkeitsregion" bezeichnet– eine Region, in der Rundungsfehler und andere Probleme den genauen Dimensionen des Dreiecks eine gewisse Unsicherheit verleihen. Die roten Dreiecke an jedem Scheitelpunkt zeigen, wie der Unsicherheitsbereich berechnet wird. Die großen grauen Quadrate zeigen die Pixel an, die gerendert werden. Die rosafarbenen Quadrate zeigen Pixel, die mithilfe der "Regel oben links" gerendert werden, die ins Spiel kommt, wenn der Rand des Dreiecks den Rand der Pixel überschreitet. Es können falsch positive Ergebnisse (Pixel festgelegt, die nicht vorhanden sein sollten) vorhanden sein, die das System normalerweise, aber nicht immer mit Cull aufweist.

![zeigt die Regel oben links an.](images/conservative-rasterization-0.png)

## <a name="interactions-with-the-pipeline"></a>Interaktionen mit der Pipeline

Viele Details dazu, wie die konservative Rasterung mit der Grafikpipeline interagiert, finden Sie unter [D3D12 Konservative Rasterung.](/windows/desktop/direct3d12/conservative-rasterization)

## <a name="implementation-details"></a>Details zur Implementierung

Der in Direct3D 12 unterstützte Typ der Rasterung wird manchmal als "überschätzungskonservative Rasterung" bezeichnet. Es gibt auch das Konzept der "antikonservativen Rasterung", was bedeutet, dass nur Pixel, die vollständig von einem gerenderten Primitiven abgedeckt sind, gerastert werden. Durch die Verwendung von Eingabeabdeckungsdaten stehen über den Pixel-Shader konservative Rasterinformationen zur Verfügung, und nur überschätzte konservative Rasterung ist als Rasterungsmodus verfügbar.

Wenn ein Teil eines Primitiven ein Pixel überlappt, wird dieses Pixel als abgedeckt betrachtet und dann gerastert. Wenn ein Rand oder eine Ecke eines Primitiven auf den Rand oder die Ecke eines Pixels fällt, ist die Anwendung der "Regel oben links" implementierungsspezifisch. Für Implementierungen, die degenerate Dreiecke unterstützen, muss ein degeneriertes Dreieck entlang einer Kante oder Ecke jedoch mindestens ein Pixel abdecken.

Konservative Rasterungsimplementierungen können auf unterschiedlichen Hardwarekomponenten variieren und falsch positive Ergebnisse erzeugen, was bedeutet, dass sie fälschlicherweise entscheiden können, dass Pixel abgedeckt sind. Dies kann aufgrund von implementierungsspezifischen Details wie primitivem Wachstum oder Ausrichtungsfehlern in den fixierten Scheitelpunktkoordinaten auftreten, die bei der Rasterung verwendet werden. Falsch positive Ergebnisse (in Bezug auf Scheitelpunktkoordinaten mit festem Punkt) sind gültig, da einige falsch positive Ergebnisse erforderlich sind, damit eine Implementierung eine Abdeckungsauswertung für nachgestellte Scheitelpunkte durchführen kann (d. h. Scheitelpunktkoordinaten, die von Gleitkommakoordinaten in den im Rasterizer verwendeten 16,8-Fixpunkt konvertiert wurden), aber die Abdeckung berücksichtigen, die von den ursprünglichen Gleitkomma-Scheitelpunktkoordinaten erzeugt wird.

Konservative Rasterungsimplementierungen erzeugen keine falschen Negativen in Bezug auf die Gleitkomma-Scheitelpunktkoordinaten für nicht degenerierte primitive Post-Snap-Primitive: Wenn ein Teil eines Primitives einen Teil eines Pixels überlappt, wird dieses Pixel gerastet.

Dreiecke, die degeneriert sind (doppelte Indizes in einem Indexpuffer oder collinear in 3D) oder nach der Konvertierung mit festem Punkt (collineare Scheitelpunkte im Rasterizer) degeneriert werden, können möglicherweise gelöscht werden. Beides sind gültige Verhaltensweisen. Degenerate Dreiecke müssen als rückwärts gerichtet betrachtet werden. Wenn also ein bestimmtes Verhalten für eine Anwendung erforderlich ist, kann sie das Hintergesichts-Culling verwenden oder einen Test für die Vorderseite verwenden. Degenerierte Dreiecke verwenden die Werte, die Vertex 0 zugewiesen sind, für alle interpolierten Werte.

Es gibt drei Hardwareunterstützungsebenen, zusätzlich zur Möglichkeit, dass die Hardware dieses Feature nicht unterstützt.

-   Ebene 1 unterstützt 1/2 Pixel unsichere Regionen, ohne dass nach dem Andocken degeneriert wird. Dies eignet sich gut für das Kachelrendering, einen Texturat atlas, die Generierung von Lichtkarten und Subpixelschattenkarten.
-   Ebene 2 fügt Nach-Snap-Degenerate und 1/256 Unsicherheitsregionen hinzu. Außerdem wird unterstützung für die CPU-basierte Algorithmusbeschleunigung (z. B. Voxelisierung) hinzugefügt.
-   Ebene 3 fügt 1/512 Unsicherheitsregionen und eine innere Eingabeabdeckung hinzu und unterstützt Okklusions-Culling. Die Eingabeabdeckung fügt `SV_InnerCoverage` hlsl (High Level Shading Language) den neuen Wert hinzu. Dies ist eine 32-Bit-Skalar-Ganzzahl, die bei der Eingabe in einen Pixel-Shader angegeben werden kann und die antippend konservativen Rasterungsinformationen darstellt (d. amp;n.b. ob ein Pixel garantiert vollständig abgedeckt wird).

## <a name="api-summary"></a>API-Zusammenfassung

Die folgenden Methoden, Strukturen, Enumerationen und Hilfsklassen verweisen auf die konservative Rasterung:

-   [**D3D11 \_ RASTERIZER \_ DESC2:**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_rasterizer_desc2) Struktur, die die Rasterizerbeschreibung aufweist, und notiert die CD3D12 \_ RASTERIZER \_ DESC2-Hilfsklasse zum Erstellen von Rasterizerbeschreibungen.
-   [**D3D11 \_ \_KONSERVATIVER \_ RASTERISIERUNGSMODUS:**](/windows/desktop/api/D3D11_3/ne-d3d11_3-d3d11_conservative_rasterization_mode) Enumerationswerte für den Modus (ein oder aus).
-   [**D3D11 \_ FEATURE \_ DATA \_ D3D11 \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) : Struktur mit der Supportebene.
-   [**D3D11 \_ CONSERVATIVE \_ RASTERIZATION \_ TIER**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_conservative_rasterization_tier) : Enumerationswerte für jede Ebene der Unterstützung durch die Hardware.
-   [**ID3D11Device::CheckFeatureSupport:**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) Methode für den Zugriff auf die unterstützten Features.

## <a name="related-topics"></a>Zugehörige Themen
* [Direct3D 11.3-Features](direct3d-11-3-features.md)