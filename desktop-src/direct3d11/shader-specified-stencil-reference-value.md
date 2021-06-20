---
title: Vom Shader angegebener Schablonenverweiswert (Direct3D 11-Grafiken)
description: Erfahren Sie mehr über den Schablonenverweiswert in Direct3D 11-Grafiken. Das Aktivieren von Pixel-Shadern für die Verwendung des Schablonenverweiswerts ermöglicht eine fein kontrollierte Steuerung von Schablonenvorgängen.
ms.assetid: 6E336623-9746-4872-ADC1-C5489F53D7AE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0e8a34d53bc7f30dc2a91fafabb561dff7a1e96
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408103"
---
# <a name="shader-specified-stencil-reference-value-direct3d-11-graphics"></a>Vom Shader angegebener Schablonenverweiswert (Direct3D 11-Grafiken)

Die Aktivierung von Pixel-Shadern zum Ausgeben des Schablonenverweiswerts anstelle des von der API angegebenen Werts ermöglicht eine sehr präzise Steuerung von Schablonenvorgängen.

Der angegebene Shaderwert ersetzt den von der API angegebenen *Schablonenverweiswert* für diesen Aufruf. Dies bedeutet, dass sich die Änderung sowohl auf den Schablonentest auswirkt als auch wenn stencil op D3D11 \_ STENCIL \_ OP REPLACE \_ (ein Member von [**D3D11 \_ STENCIL \_ OP**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_stencil_op)) verwendet wird, um den Verweiswert in den Schablonenpuffer zu schreiben.

In früheren Versionen von D3D11 kann der Schablonenverweiswert nur von der [**ID3D11DeviceContext::OMSetDepthStencilState-Methode**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetdepthstencilstate) angegeben werden. Dies bedeutet, dass dieser Wert nur mit einer Granularität pro Zeichnen definiert werden kann. Dieses D3D11.3-Feature ermöglicht Entwicklern das Lesen und Verwenden des Schablonenverweiswerts (), der `SV_StencilRef` von einem Pixel-Shader ausgegeben wird. Dies bedeutet, dass er für eine Pixel- oder Stichprobengranularität angegeben werden kann.

Dieses Feature ist in D3D11.3 optional. Überprüfen Sie zum Testen der Unterstützung das `PSSpecifiedStencilRefSupported` boolesche Feld [**D3D11 \_ FEATURE DATA \_ \_ D3D11 \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) mit [**ID3D11Device::CheckFeatureSupport.**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport)

Hier sehen Sie ein Beispiel für die Verwendung von `SV_StencilRef` in einem Pixel-Shader:

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

 

 
