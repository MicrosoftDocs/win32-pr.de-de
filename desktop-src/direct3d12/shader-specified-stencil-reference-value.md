---
title: Shader– Angegebener Schablonenverweiswert (Direct3D 12-Grafiken)
description: Erfahren Sie mehr über den Schablonenverweiswert in Direct3D 12-Grafiken. Wenn Pixel-Shader den Schablonenverweiswert verwenden können, können Schablonenvorgänge mit feiner Kontrolle kontrolliert werden.
ms.assetid: F58B1930-F12E-4FA4-A15C-A3C2B8705033
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 012c405a8ee28781d8e69d61da037a385781feeb2255aa544259c45615cb8c69
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989455"
---
# <a name="shader-specified-stencil-reference-value-direct3d-12-graphics"></a>Shader– Angegebener Schablonenverweiswert (Direct3D 12-Grafiken)

Wenn Pixel-Shader den Schablonenverweiswert anstelle des von der API angegebenen Werts ausgaben können, können Schablonenvorgänge sehr präzise kontrolliert werden.

Der Schablonenverweiswert wird normalerweise von der [**ID3D12GraphicsCommandList::OMSetStencilRef-Methode**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetstencilref) angegeben. Diese Methode legt den Schablonenverweiswert auf eine Granularität pro Zeichnen fest. Dieser Wert kann jedoch vom Pixel-Shader überschrieben werden.

Dieses D3D12-Feature (und D3D11.3) ermöglicht Entwicklern das Lesen und Verwenden des Schablonenverweiswerts *(SV \_ StencilRef),* der von einem Pixel-Shader ausgegeben wird, wodurch eine Granularität pro Pixel oder pro Beispiel ermöglicht wird.

Der angegebene Shaderwert ersetzt den von der API angegebenen Verweiswert für diesen Aufruf. Dies bedeutet, dass die Änderung sowohl den Schablonentest beeinflusst als auch wenn der Schablonenvorgang D3D12 STENCIL OP REPLACE (ein Member von \_ \_ \_ [**D3D12 \_ STENCIL \_ OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op)) verwendet wird, um den Verweiswert in den Schablonenpuffer zu schreiben.

Dieses Feature ist sowohl in D3D12 als auch in D3D11.3 optional. Um die Unterstützung zu testen, überprüfen Sie das boolesche Feld *PSSpecifiedStencilRefSupported* von [**D3D12 \_ FEATURE DATA \_ \_ D3D12 \_ OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) mit [**checkFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport).

Hier ist ein Beispiel für die Verwendung von *SV \_ StencilRef* in einem Pixel-Shader:

``` syntax
uint main2(float4 c : COORD) : SV_StencilRef
{
    return uint(c.x);
}
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Rendering](rendering.md)
</dt> <dt>

[Ressourcenbindung in HLSL](resource-binding-in-hlsl.md)
</dt> <dt>

[Shadermodell 5.1](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> <dt>

[Festlegen von Stammsignaturen in HLSL](specifying-root-signatures-in-hlsl.md)
</dt> </dl>

 

 
