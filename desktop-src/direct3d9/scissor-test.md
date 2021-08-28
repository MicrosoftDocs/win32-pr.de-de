---
description: Der Scissor-Test zullt Pixel, die sich außerhalb des Scissor-Rechtecks befinden, einem benutzerdefinierten rechteckigen Unterabschnitt des Renderziels.
ms.assetid: deff4f54-4a2f-4d9a-98a7-a69d5fc0853d
title: Scissor-Test (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1d44b7670d67e7944e9d6e2587ed0011a6244eecef509495b90c71ff0753073
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746515"
---
# <a name="scissor-test-direct3d-9"></a>Scissor-Test (Direct3D 9)

Der Scissor-Test zullt Pixel, die sich außerhalb des Scissor-Rechtecks befinden, einem benutzerdefinierten rechteckigen Unterabschnitt des Renderziels.

Das Scissor-Rechteck kann verwendet werden, um den Bereich des Renderziels anzugeben, in dem die Spielwelt gezeichnet wird. Der Bereich außerhalb des Rechtecks wird gecullt und kann der GRAFISCHEN Benutzeroberfläche eines Spiels widmen. Der Scissor-Test kann nicht rechteckige Bereiche nicht cullen.

Scissor-Rechtecke können nicht größer als das Renderziel, aber größer als der Viewport festgelegt werden.

Das Scissor-Rechteck wird von einem Geräterenderingzustand verwaltet. Ein Scissor-Test wird aktiviert oder deaktiviert, indem der Renderzustand auf **TRUE** oder **FALSE festgelegt wird.** Dieser Test wird ausgeführt, nachdem die Fragmentfarbe berechnet wurde, aber vor dem Alphatest. [**IDirect3DDevice9::SetRenderTarget**](/windows/desktop/api) setzt das Scissor-Rechteck analog zum Zurücksetzen des Viewports auf das vollständige Renderziel zurück. [**IDirect3DDevice9::SetScissorRect**](/windows/desktop/api) wird von stateblocks aufgezeichnet, [**und IDirect3DDevice9::CreateStateBlock**](/windows/desktop/api) mit der Einstellung all state (D3DSBT \_ ALL-Wert in [**D3DSTATEBLOCKTYPE).**](./d3dstateblocktype.md) Der Scissor-Test wirkt sich auch auf den [**IDirect3DDevice9::Clear-Vorgang des Geräts**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear) aus.


```
// Methods
HRESULT IDirect3DDevice9::SetScissorRect(CONST RECT* pRect); 
HRESULT IDirect3DDevice9::GetScissorRect(RECT* pRect); 

// New RenderState, values are TRUE or FALSE 
D3DRS_SCISSORTESTENABLE 

// New hardware cap 
D3D9CAPS.RasterCaps -> D3DPRASTERCAPS_SCISSORTEST;
```



Das Standardmäßige Scissor-Rechteck ist der vollständige Viewport.

Scissor-Tests werden direkt nach Abschluss der Pixelverarbeitung durch einen Pixel-Shader oder die Feste Funktionspipeline durchgeführt, wie im folgenden Diagramm dargestellt.

![Diagramm, in dem der Scissor-Test relativ zu anderen Schritten ausgeführt wird](images/scissor-test.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelpipeline](pixel-pipeline.md)
</dt> </dl>

 

 
