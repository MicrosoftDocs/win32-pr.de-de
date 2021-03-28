---
title: Reihen folgen Ansichten für Rasterizer
description: Mithilfe geordneter Ansichten von Rasterizer (ROVs) kann der Pixel-Shader-Code UAV-Bindungen mit einer Deklaration markieren, die die normalen Anforderungen für die Reihenfolge der Ergebnisse der Grafik Pipeline für UAVs ändert.
ms.assetid: 7FCFCD28-E68D-4594-8879-937F57245507
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d891701aeaadd6f4474aeed8303d9b0046d1b656
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102082"
---
# <a name="rasterizer-order-views"></a>Reihen folgen Ansichten für Rasterizer

Mithilfe geordneter Ansichten von Rasterizer (ROVs) kann der Pixel-Shader-Code UAV-Bindungen mit einer Deklaration markieren, die die normalen Anforderungen für die Reihenfolge der Ergebnisse der Grafik Pipeline für UAVs ändert. Dadurch können OIT-Algorithmen (Order Independent Transparenz) funktionieren, die deutlich bessere renderingergebnisse bieten, wenn mehrere transparente Objekte in einer Ansicht aufeinander zueinander stehen.

-   [Übersicht](#overview)
-   [Implementierungsdetails](#implementation-details)
-   [API-Zusammenfassung](#api-summary)
-   [Zugehörige Themen](#related-topics)

## <a name="overview"></a>Übersicht

Standard Grafik Pipelines haben möglicherweise Probleme mit der ordnungsgemäßen Zusammensetzung mehrerer Texturen, die Transparenz enthalten. Objekte wie z. b. Drahtzäune, Rauch, Feuer, Vegetation und farbige Glas verwenden Transparenz, um den gewünschten Effekt zu erzielen. Es treten Probleme auf, wenn mehrere Texturen, die Transparenz enthalten, aufeinander zueinander stehen (Feuer vor einem Fence vor einem Glasgebäude, das eine Vegetations enthält). Mithilfe geordneter Ansichten (ROVs) für Rasterizer können die zugrunde liegenden OIT-Algorithmen die Features der Hardware verwenden, um die Transparenz Reihenfolge ordnungsgemäß aufzulösen. Transparenz wird vom Pixelshader behandelt.

Mithilfe geordneter Ansichten von Rasterizer (ROVs) kann der Pixel-Shader-Code UAV-Bindungen mit einer Deklaration markieren, die die normalen Anforderungen für die Reihenfolge der Ergebnisse der Grafik Pipeline für UAVs ändert.

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

-   [**D3D11 \_ Raster \_ DESC2**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_rasterizer_desc2) : Struktur mit der Beschreibung des Rasterizers. Beachten Sie die CD3D12 \_ Raster \_ DESC2 Helper-Klasse zum Erstellen von Raster-Beschreibungen.
-   [**D3D11 \_ Feature \_ Data \_ D3D11 \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) : Struktur mit dem booleschen Wert `ROVsSupported` , der die Unterstützung angibt.
-   [**ID3D11Device:: checkfeaturesupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) : Methode für den Zugriff auf die unterstützten Funktionen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D 11,3-Features](direct3d-11-3-features.md)
</dt> <dt>

[Shadermodell 5,1](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> </dl>

 

 