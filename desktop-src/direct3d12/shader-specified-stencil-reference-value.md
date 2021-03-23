---
title: Shader-angegebener Schablone-Verweis Wert (Direct3D 12-Grafiken)
description: Wenn Sie Pixel-Shader ermöglichen, den Schablonen Verweis Wert auszugeben, anstatt die API-Angabe zu verwenden, ist eine sehr präzise Steuerung von Schablone-Vorgängen möglich.
ms.assetid: F58B1930-F12E-4FA4-A15C-A3C2B8705033
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6a8b7697cc06594b3e2ffc717cbded9e6832129
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104548699"
---
# <a name="shader-specified-stencil-reference-value-direct3d-12-graphics"></a>Shader-angegebener Schablone-Verweis Wert (Direct3D 12-Grafiken)

Wenn Sie Pixel-Shader ermöglichen, den Schablonen Verweis Wert auszugeben, anstatt die API-Angabe zu verwenden, ist eine sehr präzise Steuerung von Schablone-Vorgängen möglich.

Der Schablonen Verweis Wert wird normalerweise von der [**ID3D12GraphicsCommandList:: omsetstencilref**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetstencilref) -Methode angegeben. Diese Methode legt den Schablonen Verweis Wert auf eine Granularität pro zeichnen fest. Dieser Wert kann jedoch durch den Pixelshader überschrieben werden.

Diese D3D12-Funktion (und D3D 11.3) ermöglicht Entwicklern das Lesen und Verwenden des Schablonen Verweis Werts (*SV \_ stencilref*), der von einem Pixelshader ausgegeben wird. Dadurch wird eine Granularität pro Pixel oder pro Stichprobe ermöglicht.

Der angegebene Shader-Wert ersetzt den von der API angegebenen Verweis Wert für diesen Aufruf, d. h. die Änderung wirkt sich auf den Schablonen Test aus, und wenn der Schablonen Vorgang D3D12 \_ Schablone \_ op \_ Replace (ein Member von [**D3D12 \_ Schablone \_ op**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op)) zum Schreiben des Verweis Werts in den Schablonen Puffer verwendet wird.

Diese Funktion ist sowohl in D3D12 als auch D3D 11.3 optional. Um die Unterstützung zu testen, überprüfen Sie das boolesche Feld *psspecifiedstencilrefsupported* von [**D3D12 \_ Feature \_ Data \_ D3D12 \_ Optionen**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) mithilfe von [**checkfeaturesupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport).

Im folgenden finden Sie ein Beispiel für die Verwendung von *SV \_ stencilref* in einem Pixelshader:

``` syntax
uint main2(float4 c : COORD) : SV_StencilRef
{
    return uint(c.x);
}
```

## <a name="related-topics"></a>Verwandte Themen

<dl> <dt>

[Darstellung](rendering.md)
</dt> <dt>

[Ressourcen Bindung in HLSL](resource-binding-in-hlsl.md)
</dt> <dt>

[Shadermodell 5,1](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> <dt>

[Angeben von Stamm Signaturen in HLSL](specifying-root-signatures-in-hlsl.md)
</dt> </dl>

 

 
