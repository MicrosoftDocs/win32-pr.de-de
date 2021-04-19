---
description: Der Scheren-Test das Culling-Pixel, die sich außerhalb des Scheren Rechtecks befinden, ein benutzerdefinierter rechteckiger unter Abschnitt des Renderziels.
ms.assetid: deff4f54-4a2f-4d9a-98a7-a69d5fc0853d
title: Scissor-Test (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66c4298182ab2bb6302c19111e2970d23cef311d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106338884"
---
# <a name="scissor-test-direct3d-9"></a>Scissor-Test (Direct3D 9)

Der Scheren-Test das Culling-Pixel, die sich außerhalb des Scheren Rechtecks befinden, ein benutzerdefinierter rechteckiger unter Abschnitt des Renderziels.

Das Scheren-Rechteck kann verwendet werden, um den Bereich des Renderziels anzugeben, in dem die Spiel Welt gezeichnet wird. Der Bereich außerhalb des Rechtecks ist ein herausgefiltert werden und kann für die GUI eines Spiels verwendet werden. Der Scheren-Test kann nicht rechteckige Bereiche umkreisen.

Scissor-Rechtecke können nicht größer als das Renderziel festgelegt werden, Sie können jedoch größer als der Viewport festgelegt werden.

Das Scheren Rechteck wird von einem Geräte-Rendering-Zustand verwaltet. Ein Scheren Test wird aktiviert oder deaktiviert, indem renderstate auf " **true** " oder " **false**" festgelegt wird. Dieser Test wird nach dem Berechnen der fragmentfarbe, aber vor dem Alpha Test ausgeführt. [**IDirect3DDevice9:: SetRenderTarget**](/windows/desktop/api) setzt das Scheren Rechteck auf das vollständige Renderziel zurück, analog zum Zurücksetzen des Viewports. [**IDirect3DDevice9:: czcissorrect**](/windows/desktop/api) wird von stateblocks aufgezeichnet, und [**IDirect3DDevice9:: kreatestateblock**](/windows/desktop/api) mit der Einstellung All State (D3DSBT \_ all Value in [**D3DSTATEBLOCKTYPE**](./d3dstateblocktype.md)). Der Scheren-Test wirkt sich auch auf den Device [**IDirect3DDevice9:: Clear**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear) -Vorgang aus.


```
// Methods
HRESULT IDirect3DDevice9::SetScissorRect(CONST RECT* pRect); 
HRESULT IDirect3DDevice9::GetScissorRect(RECT* pRect); 

// New RenderState, values are TRUE or FALSE 
D3DRS_SCISSORTESTENABLE 

// New hardware cap 
D3D9CAPS.RasterCaps -> D3DPRASTERCAPS_SCISSORTEST;
```



Das standardmäßige Scheren-Rechteck ist der vollständige Viewport.

Das Testen von Scissor erfolgt erst, nachdem die Pixel Verarbeitung von einem Pixelshader oder der Fixed-Funktions Pipeline abgeschlossen wurde. Dies ist im folgenden Diagramm dargestellt.

![Diagramm der Ausführung von Scheren Tests in Bezug auf andere Schritte](images/scissor-test.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixel Pipeline](pixel-pipeline.md)
</dt> </dl>

 

 
