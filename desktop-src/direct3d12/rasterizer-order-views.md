---
title: Rasterizer-geordnete Ansichten
description: Mithilfe von Rasterizer-geordneten Sichten (ROVs) können Pixel-Shader-Code ungeordnete Zugriffs Ansichts Bindungen mit einer Deklaration markieren, die die normalen Anforderungen für die Reihenfolge der Ergebnisse der Grafik Pipeline für UAVs ändert.
ms.assetid: D308BF3E-8CBE-4DF0-B020-4D202E858D99
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a19988d3f3eec39e8fc298a2fc13031ecc29e3e8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548724"
---
# <a name="rasterizer-ordered-views"></a>Rasterizer-geordnete Ansichten

Rasterizer-geordnete Sichten (ROVs) ermöglichen es dem Pixelshader-Code, UAV-Bindungen (ungeordnete Zugriffs Ansicht) mit einer Deklaration zu markieren, die die normalen Anforderungen für die Reihenfolge der Ergebnisse der Grafik Pipeline für UAVs ändert. Dies ermöglicht die Funktionsweise von "Order-Independent Transparenz (OIT)"-Algorithmen, die deutlich bessere renderingergebnisse bieten, wenn mehrere transparente Objekte in einer Ansicht aufeinander zueinander stehen.

-   [Übersicht](#overview)
-   [Implementierungsdetails](#implementation-details)
-   [API-Zusammenfassung](#api-summary)
-   [Verwandte Themen](#related-topics)

## <a name="overview"></a>Überblick

Standard Grafik Pipelines haben möglicherweise Probleme mit der ordnungsgemäßen Zusammensetzung mehrerer Texturen, die Transparenz enthalten. Objekte wie z. b. Drahtzäune, Rauch, Feuer, Vegetation und farbige Glas verwenden Transparenz, um den gewünschten Effekt zu erzielen. Es treten Probleme auf, wenn mehrere Texturen, die Transparenz enthalten, aufeinander zueinander stehen (Feuer vor einem Fence vor einem Glasgebäude, das eine Vegetations enthält). Rasterizer-geordnete Sichten (ROVs) ermöglichen es den zugrunde liegenden OIT-Algorithmen, Features der Hardware zu verwenden, um die Transparenz Reihenfolge ordnungsgemäß aufzulösen. Transparenz wird vom Pixelshader behandelt.

Rasterizer-geordnete Sichten (ROVs) ermöglichen es Pixelshader-Code, UAV-Bindungen mit einer Deklaration zu markieren, die die normalen Anforderungen für die Reihenfolge der Ergebnisse der Grafik Pipeline für UAVs ändert.

ROVs garantieren die Reihenfolge von UAV-Zugriffen für beliebige Paare von überlappenden Pixelshader-aufrufen. In diesem Fall bedeutet "überlappende", dass die Aufrufe von denselben zeichnen-aufrufen generiert werden und die gleiche Pixel Koordinate gemeinsam verwenden, wenn der Ausführungs Modus für die Pixelfrequenz und das gleiche Pixel und die gleiche Stichproben Koordinate im Modus für die Stichproben Häufigkeit ausgeführt werden.

Die Reihenfolge, in der sich überlappende Rows-Zugriffe von pixelshaderaufrufen ausführen, ist mit der Reihenfolge identisch, in der die Geometrie übermittelt wird. Dies bedeutet, dass bei überlappenden Pixelshader-aufrufen die von einem Pixelshader-Aufruf ausgeführten Rows-Schreibvorgänge verfügbar sein müssen, um von einem nachfolgenden Aufruf gelesen zu werden, und keine Auswirkungen auf Lesevorgänge durch einen vorherigen Aufruf haben dürfen. Von einem Pixelshader-Aufruf ausgeführte Row-Lesevorgänge müssen Schreibvorgänge durch einen vorherigen Aufruf widerspiegeln und dürfen keine Schreibvorgänge durch einen nachfolgenden Aufruf widerspiegeln. Dies ist für UAVs wichtig, da Sie explizit aus den in der Ausgabe Invarianz Garantie ausgelassenen Garantien weggelassen werden, die normalerweise durch die festgelegte Reihenfolge der Ergebnisse der Grafik Pipeline

## <a name="implementation-details"></a>Details zur Implementierung

Rasterizer-geordnete Sichten (ROVs) werden mit den folgenden neuen HLSL-Objekten (High Level Shader Language) deklariert und sind nur für den Pixelshader verfügbar:

-   `RasterizerOrderedBuffer`
-   `RasterizerOrderedByteAddressBuffer`
-   `RasterizerOrderedStructuredBuffer`
-   `RasterizerOrderedTexture1D`
-   `RasterizerOrderedTexture1DArray`
-   `RasterizerOrderedTexture2D`
-   `RasterizerOrderedTexture2DArray`
-   `RasterizerOrderedTexture3D`

Verwenden Sie diese Objekte auf die gleiche Weise wie andere UAV-Objekte (z. b `RWBuffer` . usw.).

## <a name="api-summary"></a>API-Zusammenfassung

ROVs sind ein nur-HLSL-Konstrukt, das unterschiedliche Verhaltens Semantik auf UAVs anwendet. Alle für UAVs relevanten APIs sind auch für ROVs relevant. Beachten Sie, dass die folgende Methode, Struktur und Hilfsklasse auf den Rasterizer verweisen:

-   [**D3D12 \_ Raster \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc) -Debug: Struktur mit der Beschreibung des Rasterizers.
-   [**D3D12 \_ Feature \_ Data \_ D3D12 \_ Optionen**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) : Struktur mit einem booleschen Wert, der die Unterstützung angibt.
-   [**Checkfeaturesupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) : Methode für den Zugriff auf die unterstützten Funktionen.
-   [**CD3DX12 \_ Raster \_ DESC**](cd3dx12-rasterizer-desc.md) : Hilfsklasse zum Erstellen von Raster-Beschreibungen.
-   [**D3D12 \_ Grafik \_ Pipeline \_ Status \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) : Struktur, die den Pipeline Status enthält.

## <a name="related-topics"></a>Verwandte Themen

* [Konservative rasterisierung](conservative-rasterization.md)
* [Darstellung](rendering.md)
* [Ressourcen Bindung in HLSL](resource-binding-in-hlsl.md)
* [Shadermodell 5,1](/windows/desktop/direct3dhlsl/shader-model-5-1)