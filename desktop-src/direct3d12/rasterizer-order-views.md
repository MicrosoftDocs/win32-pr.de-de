---
title: Rasterizer-geordnete Ansichten
description: Rasterizer-geordnete Sichten (ROVs) ermöglichen dem Pixelshadercode, ungeordnete Zugriffsansichtsbindungen mit einer Deklaration zu markieren, die die normalen Anforderungen an die Reihenfolge der Grafikpipelineergebnisse für UAVs ändert.
ms.assetid: D308BF3E-8CBE-4DF0-B020-4D202E858D99
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 214098f70608d5f20d24edb1312593c6215abea12efecfc6eea97148e8855cce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118300981"
---
# <a name="rasterizer-ordered-views"></a>Rasterizer-geordnete Ansichten

Rasterizer-geordnete Ansichten (ROVs) ermöglichen dem Pixelshadercode das Markieren von UAV-Bindungen (Unordered Access View) mit einer Deklaration, die die normalen Anforderungen an die Reihenfolge der Grafikpipelineergebnisse für UAVs ändert. Dadurch können OIT-Algorithmen (Order-Independent Transparency) funktionieren, die viel bessere Renderingergebnisse liefern, wenn mehrere transparente Objekte in einer Ansicht miteinander in Einklang stehen.

-   [Übersicht](#overview)
-   [Details zur Implementierung](#implementation-details)
-   [API-Zusammenfassung](#api-summary)
-   [Zugehörige Themen](#related-topics)

## <a name="overview"></a>Übersicht

Standardmäßige Grafikpipelines haben möglicherweise Probleme beim ordnungsgemäßen Zusammensetzen mehrerer Texturen, die Transparenz enthalten. Objekte wie Wire Fences, Smoke, Fire,Wiederverwendung und Farbiges Glass verwenden Transparenz, um den gewünschten Effekt zu erzielen. Probleme treten auf, wenn mehrere Texturen, die Transparenz enthalten, miteinander in Einklang stehen (z. B. Qualm vor einem Zäunen vor einem Gebäude mit Brille). Rasterizer-geordnete Ansichten (ROVs) ermöglichen es den zugrunde liegenden OIT-Algorithmen, Features der Hardware zu verwenden, um zu versuchen, die Transparenzreihenfolge ordnungsgemäß aufzulösen. Transparenz wird vom Pixelshader behandelt.

Rasterizer-geordnete Sichten (ROVs) ermöglichen es dem Pixelshadercode, UAV-Bindungen mit einer Deklaration zu markieren, die die normalen Anforderungen an die Reihenfolge der Grafikpipelineergebnisse für UAVs ändert.

ROVs garantieren die Reihenfolge der UAV-Zugriffe für jedes Paar überlappender Pixel-Shaderaufrufe. In diesem Fall bedeutet "überlappend", dass die Aufrufe von den gleichen Zeichnen-Aufrufen generiert werden und die gleiche Pixelkoordinate verwenden, wenn sie sich im Ausführungsmodus der Pixelfrequenz befinden, und die gleiche Pixel- und Stichprobenkoordinate im Stichprobenhäufigkeitsmodus.

Die Reihenfolge, in der überlappende ROV-Zugriffe von Pixel-Shaderaufrufen ausgeführt werden, ist identisch mit der Reihenfolge, in der die Geometrie übermittelt wird. Dies bedeutet, dass ROV-Schreibvorgänge, die von einem Pixel-Shaderaufruf ausgeführt werden, bei überlappenden Pixel-Shaderaufrufen verfügbar sein müssen, damit sie bei einem nachfolgenden Aufruf gelesen werden können und sich nicht auf Lesevorgänge durch einen vorherigen Aufruf auswirken dürfen. ROV-Lesevorgänge, die von einem Pixel-Shaderaufruf ausgeführt werden, müssen Schreibvorgänge durch einen vorherigen Aufruf und keine Schreibvorgänge durch einen nachfolgenden Aufruf widerspiegeln. Dies ist für UAVs wichtig, da sie explizit aus den Ausgabeinvarianzgarantien weggelassen werden, die normalerweise durch die feste Reihenfolge der Grafikpipelineergebnisse festgelegt werden.

## <a name="implementation-details"></a>Details zur Implementierung

Rasterizer-geordnete Ansichten (ROVs) werden mit den folgenden neuen HLSL-Objekten (High Level Shader Language) deklariert und sind nur für den Pixel-Shader verfügbar:

-   `RasterizerOrderedBuffer`
-   `RasterizerOrderedByteAddressBuffer`
-   `RasterizerOrderedStructuredBuffer`
-   `RasterizerOrderedTexture1D`
-   `RasterizerOrderedTexture1DArray`
-   `RasterizerOrderedTexture2D`
-   `RasterizerOrderedTexture2DArray`
-   `RasterizerOrderedTexture3D`

Verwenden Sie diese Objekte auf die gleiche Weise wie andere UAV-Objekte (z. `RWBuffer` B. usw.).

## <a name="api-summary"></a>API-Zusammenfassung

ROVs sind ein rein HLSL-Konstrukt, das unterschiedliche Verhaltenssemantik auf UAVs anwendet. Alle APIs, die für UAVs relevant sind, sind auch für ROVs relevant. Beachten Sie, dass die folgende Methode, Strukturen und Hilfsklasse auf den Rasterizer verweisen:

-   [**D3D12 \_ RASTERIZER \_ DESC:**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc) Struktur mit der Rasterizerbeschreibung.
-   [**D3D12 \_ FEATURE \_ DATA \_ D3D12 \_ OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) : Struktur mit einem booleschen Wert, der die Unterstützung angibt.
-   [**CheckFeatureSupport:**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) Methode für den Zugriff auf die unterstützten Features.
-   [**CD3DX12 \_ RASTERIZER \_ DESC:**](cd3dx12-rasterizer-desc.md) Hilfsklasse zum Erstellen von Rasterizerbeschreibungen.
-   [**D3D12 \_ GRAPHICS \_ PIPELINE \_ STATE \_ DESC:**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) Struktur mit dem Pipelinezustand.

## <a name="related-topics"></a>Zugehörige Themen

* [Konservative Rasterung](conservative-rasterization.md)
* [Rendering](rendering.md)
* [Ressourcenbindung in HLSL](resource-binding-in-hlsl.md)
* [Shadermodell 5.1](/windows/desktop/direct3dhlsl/shader-model-5-1)