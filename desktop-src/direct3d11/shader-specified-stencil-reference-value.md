---
title: Shader– Angegebener Schablonenverweiswert (Direct3D 11-Grafiken)
description: Erfahren Sie mehr über den Schablonenverweiswert in Direct3D 11-Grafiken. Wenn Pixel-Shader den Schablonenverweiswert verwenden können, können Schablonenvorgänge mit feiner Kontrolle kontrolliert werden.
ms.assetid: 6E336623-9746-4872-ADC1-C5489F53D7AE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d68d780c7a800f4291b3cce01c6f974cdeedaa8f590fc76fdf8afa8b3fb3c5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119632310"
---
# <a name="shader-specified-stencil-reference-value-direct3d-11-graphics"></a>Shader– Angegebener Schablonenverweiswert (Direct3D 11-Grafiken)

Wenn Pixel-Shader den Schablonenverweiswert anstelle des von der API angegebenen Werts aus geben, wird eine sehr präzise Steuerung von Schablonenvorgängen ermöglicht.

Der angegebene Shaderwert ersetzt den  API-angegebenen Schablonenverweiswert für diesen Aufruf. Dies bedeutet, dass die Änderung sowohl den Schablonentest beeinflusst als auch wenn die Schablonen op D3D11 STENCIL OP REPLACE (ein Member von \_ \_ \_ [**D3D11 \_ STENCIL \_ OP**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_stencil_op)) verwendet wird, um den Verweiswert in den Schablonenpuffer zu schreiben.

In früheren Versionen von D3D11 kann der Schablonenverweiswert nur von der [**ID3D11DeviceContext::OMSetDepthStencilState-Methode**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetdepthstencilstate) angegeben werden. Dies bedeutet, dass dieser Wert nur für eine Granularität pro Zeichnen definiert werden kann. Mit diesem D3D11.3-Feature können Entwickler den Schablonenverweiswert ( ) lesen und verwenden, der von einem Pixel-Shader ausgegeben wird. Dies bedeutet, dass er für eine Granularität pro Pixel oder pro Beispiel angegeben werden `SV_StencilRef` kann.

Dieses Feature ist in D3D11.3 optional. Überprüfen Sie zum Testen der Unterstützung das boolesche Feld von `PSSpecifiedStencilRefSupported` [**D3D11 \_ FEATURE \_ DATA \_ D3D11 \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) mit [**ID3D11Device::CheckFeatureSupport.**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport)

Hier ist ein Beispiel für die Verwendung von `SV_StencilRef` in einem Pixel-Shader:

``` syntax
uint main2(float4 c : COORD) : SV_StencilRef
{
    return uint(c.x);
}
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D 11.3-Features](direct3d-11-3-features.md)
</dt> <dt>

[Shadermodell 5.1](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> </dl>

 

 
