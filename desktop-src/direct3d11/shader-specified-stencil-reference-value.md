---
title: Von Shader angegebener Schablone-Verweis Wert (Direct3D 11 Grafiken)
description: Wenn Sie Pixel-Shader ermöglichen, den Schablonen Verweis Wert auszugeben, anstatt die API-Angabe zu verwenden, ist eine sehr präzise Steuerung von Schablone-Vorgängen möglich.
ms.assetid: 6E336623-9746-4872-ADC1-C5489F53D7AE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65a089ec8ab56a1cf00021f97bb40cf86fe42f04
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104340007"
---
# <a name="shader-specified-stencil-reference-value-direct3d-11-graphics"></a>Von Shader angegebener Schablone-Verweis Wert (Direct3D 11 Grafiken)

Wenn Sie Pixel-Shader ermöglichen, den Schablonen Verweis Wert auszugeben, anstatt die API-Angabe zu verwenden, ist eine sehr präzise Steuerung von Schablone-Vorgängen möglich.

Der angegebene Shader-Wert ersetzt den von der API angegebenen *Schablone-Verweis Wert* für diesen Aufruf, d. h. die Änderung wirkt sich auf den Schablonen Test aus, und wenn der "Schablone op D3D11 \_ Schablone op \_ Replace" \_ (ein Member von [**D3D11 \_ Schablone \_ op**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_stencil_op)) zum Schreiben des Verweis Werts in den Schablonen Puffer verwendet wird.

In früheren Versionen von D3D11 kann der Schablonen Verweis Wert nur von der [**Verknüpfung id3d11devicecontext aus:: omsetdepthstencilstate**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetdepthstencilstate) -Methode angegeben werden. Dies bedeutet, dass dieser Wert nur für die Granularität pro zeichnen definiert werden kann. Dieses D3D 11.3-Feature ermöglicht Entwicklern das Lesen und Verwenden des Schablonen Verweis Werts ( `SV_StencilRef` ), der von einem Pixelshader ausgegeben wird. Dies bedeutet, dass er in einer Granularität pro Pixel oder pro Stichprobe angegeben werden kann.

Diese Funktion ist in D3D 11.3 optional. Um die Unterstützung zu testen, überprüfen Sie das `PSSpecifiedStencilRefSupported` boolesche Feld [**D3D11 \_ Feature \_ Data \_ D3D11 \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) using [**ID3D11Device:: checkfeaturesupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) .

Im folgenden finden Sie ein Beispiel für die Verwendung von `SV_StencilRef` in einem Pixelshader:

``` syntax
uint main2(float4 c : COORD) : SV_StencilRef
{
    return uint(c.x);
}
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D 11,3-Features](direct3d-11-3-features.md)
</dt> <dt>

[Shadermodell 5,1](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> </dl>

 

 
