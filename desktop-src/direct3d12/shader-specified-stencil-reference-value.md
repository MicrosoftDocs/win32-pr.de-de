---
title: Vom Shader angegebener Schablonenverweiswert (Direct3D 12-Grafiken)
description: Erfahren Sie mehr über den Schablonenverweiswert in Direct3D 12-Grafiken. Das Aktivieren von Pixel-Shadern für die Verwendung von Schablonenverweiswerten ermöglicht eine fein kontrollierte Steuerung von Schablonenvorgängen.
ms.assetid: F58B1930-F12E-4FA4-A15C-A3C2B8705033
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fee212d7c2573402ad38bc19040e5c60a89c090
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408313"
---
# <a name="shader-specified-stencil-reference-value-direct3d-12-graphics"></a>Vom Shader angegebener Schablonenverweiswert (Direct3D 12-Grafiken)

Das Aktivieren von Pixel-Shadern zum Ausgeben des Schablonenverweiswerts anstelle des von der API angegebenen Werts ermöglicht eine sehr präzise Steuerung von Schablonenvorgängen.

Der Schablonenverweiswert wird normalerweise von der [**ID3D12GraphicsCommandList::OMSetStencilRef-Methode**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetstencilref) angegeben. Diese Methode legt den Schablonenverweiswert auf eine Granularität pro Zeichnen fest. Dieser Wert kann jedoch vom Pixelshader überschrieben werden.

Dieses D3D12-Feature (und D3D11.3) ermöglicht Entwicklern das Lesen und Verwenden des Schablonenverweiswerts *(SV \_ StencilRef),* der von einem Pixel-Shader ausgegeben wird, und ermöglicht eine Granularität pro Pixel oder pro Stichprobe.

Der angegebene Shaderwert ersetzt den von der API angegebenen Verweiswert für diesen Aufruf. Dies bedeutet, dass sich die Änderung auf den Schablonentest auswirkt und wenn der Schablonenvorgang D3D12 \_ STENCIL \_ OP \_ REPLACE (ein Member von [**D3D12 \_ STENCIL \_ OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op)) verwendet wird, um den Verweiswert in den Schablonenpuffer zu schreiben.

Dieses Feature ist sowohl in D3D12 als auch in D3D11.3 optional. Um die Unterstützung zu testen, überprüfen Sie das boolesche Feld *PSSpecifiedStencilRefSupported* von [**D3D12 \_ FEATURE DATA \_ \_ D3D12 \_ OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) mit [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport).

Hier sehen Sie ein Beispiel für die Verwendung von *SV \_ StencilRef* in einem Pixel-Shader:

``` syntax
uint main2(float4 c : COORD) : SV_StencilRef
{
    return uint(c.x);
}
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Darstellung](rendering.md)
</dt> <dt>

[Ressourcenbindung in HLSL](resource-binding-in-hlsl.md)
</dt> <dt>

[Shadermodell 5.1](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> <dt>

[Festlegen von Stammsignaturen in HLSL](specifying-root-signatures-in-hlsl.md)
</dt> </dl>

 

 
